# Day 47 – AWS Networking & Content Delivery

## Networking and Content Delivery

### AWS Client VPN

* Managed OpenVPN-based solution
* Secure remote access to AWS and on-prem networks
* Works from any device with VPN client

### Amazon CloudFront

* Global Content Delivery Network (CDN)
* Caches content at Edge Locations worldwide
* Reduces latency for static and dynamic content

### AWS Direct Connect

* Dedicated private connection to AWS
* Consistent bandwidth and low latency
* Takes time to provision
* Not encrypted by default

### Elastic Load Balancing (ELB)

* Distributes incoming traffic across targets
* ALB: Layer 7 (HTTP/HTTPS)
* NLB: Layer 4 (TCP/UDP)
* GLB: Routes traffic to inspection appliances

### AWS Global Accelerator

* Uses AWS global backbone network
* Provides 2 static Anycast IPs
* Routes users to nearest healthy endpoint
* Ideal for non-cacheable TCP/UDP traffic

### AWS PrivateLink

* Private connectivity to AWS and partner services
* Traffic stays within AWS network
* No need for VPC peering or internet gateway

### Amazon Route 53

* Managed DNS service
* Supports multiple routing policies:

  * Simple
  * Weighted
  * Latency
  * Geolocation
  * Failover
  * Multivalue
* Includes health checks and domain registration

### AWS Site-to-Site VPN

* Encrypted IPsec VPN connection
* Connects on-premises to AWS VPC
* Uses public internet
* Quick to set up but variable latency

### AWS Transit Gateway

* Central hub for network connectivity
* Connects multiple VPCs and on-prem networks
* Supports transitive routing

### Amazon VPC

* Logically isolated virtual network
* Full control over networking setup:

  * IP ranges
  * Subnets
  * Route tables
  * Internet gateways
  * Security (NACLs, Security Groups)
