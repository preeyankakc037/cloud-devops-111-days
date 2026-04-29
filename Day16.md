# ENIs and VPC Gateway Endpoints

## How do ENIs work in relation to VPC Gateways?

An **Elastic Network Interface (ENI)** is a virtual network card attached to an EC2 instance (or other AWS resource) within a VPC. It has a private IP address, a MAC address, security groups, and optionally a public or Elastic IP.

**VPC Gateways** — specifically **Internet Gateways (IGW)** and **NAT Gateways** — are separate constructs that operate at the VPC routing layer, not at the ENI level. Here's how they relate:

- **Internet Gateway**: When an EC2 instance with a public IP sends traffic to the internet, the IGW performs 1:1 NAT between the instance's private IP (on its ENI) and its public/Elastic IP. The ENI itself only ever holds the private IP — the public IP translation happens at the IGW.

- **NAT Gateway**: A NAT Gateway has its own ENI (managed by AWS) placed in a public subnet. Traffic from private-subnet instances flows out their ENI → through route table → to the NAT Gateway's ENI → through the IGW. The ENI is the physical attachment point; the gateway handles routing and address translation.

- **Transit Gateway / VPN Gateway**: These also attach to your VPC via ENIs under the hood. Traffic is routed to/from these gateways based on your VPC route tables, with ENIs acting as the on-ramp/off-ramp within each subnet.

**In short**: ENIs are the network attachment points for resources inside the VPC. Gateways are routing constructs that traffic is directed *toward* via route tables — ENIs don't directly "talk" to gateways; the route table connects them.

---

## VPC Gateway Endpoints — Are they only for S3 and DynamoDB?

**Yes — VPC Gateway Endpoints are exclusively for Amazon S3 and Amazon DynamoDB.** No other AWS services support this endpoint type.

### Why only these two?

Gateway Endpoints work by injecting a **prefix list route** directly into your VPC route table, pointing to the gateway endpoint instead of the internet. This approach has specific architectural requirements:

1. **AWS-owned, globally consistent IP ranges**: S3 and DynamoDB have well-defined, published IP prefix lists that AWS manages centrally. Gateway Endpoints rely on these stable prefix lists to populate route tables correctly.

2. **No ENI required**: Unlike Interface Endpoints (which use AWS PrivateLink and create an ENI in your subnet), Gateway Endpoints have no presence inside your VPC — they're just a route table entry pointing at an AWS-managed gateway. This makes them **free of charge**, since there's no ENI to bill for.

3. **High-throughput, foundational services**: S3 and DynamoDB are extremely high-traffic services. The gateway model scales horizontally without per-AZ ENI bottlenecks, making it well-suited for object storage and key-value workloads that generate massive request volumes.

4. **Legacy/architectural decision**: Gateway Endpoints predate PrivateLink. When AWS later built Interface Endpoints (PrivateLink-based), they made that the standard for all new service integrations. S3 and DynamoDB now support *both* endpoint types, but Gateway Endpoints remain available because they're free and sufficient for most use cases.

### Gateway vs. Interface Endpoints at a glance

| Feature | Gateway Endpoint | Interface Endpoint (PrivateLink) |
|---|---|---|
| Services supported | S3, DynamoDB only | 100+ AWS services |
| How it works | Route table entry | ENI in your subnet |
| Cost | Free | Hourly + data charges |
| DNS required | No | Yes (private DNS) |
| On-premises access | No | Yes (via Direct Connect / VPN) |
| Cross-region | No | No |

### When to use an Interface Endpoint for S3 instead

Even though S3 supports both, you'd prefer the **Interface Endpoint** when:
- Traffic originates from **on-premises** (via Direct Connect or VPN) and needs to reach S3 privately
- You need **endpoint policies with source IP** enforcement via private DNS
- You're in a hub-and-spoke Transit Gateway architecture where route table injection doesn't reach spoke VPCs