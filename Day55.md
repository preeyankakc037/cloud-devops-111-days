# Day 55 – AWS Mixed Concepts & Quick Revision

Today I revised random AWS concepts across multiple services to strengthen overall understanding and fill knowledge gaps.

---

## High Availability Basics

- Use **Multi-AZ deployments** for fault tolerance
- Deploy across **multiple Availability Zones**
- Use **Auto Scaling + Load Balancer** for resilience

---

## S3 Quick Notes

- 11 9’s durability (99.999999999%)
- Objects stored across multiple AZs
- Supports:
  - Versioning
  - Lifecycle policies
  - Replication (CRR & SRR)

---

## EC2 Quick Tips

- Use **Security Groups** → stateful firewall
- Use **NACLs** → stateless firewall
- Use **Placement Groups**:
  - Cluster → low latency
  - Spread → high availability
  - Partition → large distributed systems

---

## VPC Essentials

- Private vs Public Subnets
- Internet Gateway → public internet access
- NAT Gateway → outbound internet for private subnets
- Route Tables control traffic flow

---

## Load Balancer Recap

- ALB → HTTP/HTTPS (Layer 7)
- NLB → TCP/UDP (Layer 4)
- GLB → traffic inspection

---

## Serverless Recap

- Lambda → event-driven compute
- API Gateway → expose APIs
- DynamoDB → serverless database

---

## Security Quick Notes

- IAM → permissions
- KMS → encryption keys
- Secrets Manager → store credentials
- WAF → protect web apps

---

## Monitoring & Logging

- CloudWatch → metrics, logs, alarms
- CloudTrail → API activity tracking

---

## Cost Optimization Reminders

- Use **Spot Instances** for cheap compute
- Use **S3 lifecycle** to reduce storage cost
- Use **Auto Scaling** to avoid over-provisioning

---

## Key Summary

- Design for **high availability**
- Optimize for **cost and performance**
- Use **managed services whenever possible**
- Always follow **least privilege security**