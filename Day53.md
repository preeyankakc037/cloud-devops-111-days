# Day 53 – AWS Cost Management & Optimization

Today I studied AWS cost management tools and optimization strategies to reduce cloud spending while maintaining performance.

---

## Cost Management Tools

### AWS Cost Explorer
- Visualize AWS spending over time
- Identify trends and usage patterns
- Forecast future costs

---

### AWS Budgets
- Set custom cost or usage limits
- Get alerts via:
  - Email
  - SNS notifications

---

### Cost & Usage Report (CUR)
- Most detailed billing dataset
- Delivered to Amazon S3
- Can be queried using Athena

---

### AWS Trusted Advisor
- Provides recommendations across:
  - Cost optimization
  - Security
  - Performance
  - Fault tolerance

---

### AWS Compute Optimizer
- Uses Machine Learning
- Recommends right-sized resources
- Covers:
  - EC2
  - EBS
  - Lambda
  - ECS

---

### AWS License Manager
- Tracks BYOL (Bring Your Own License)
- Supports:
  - SQL Server
  - Oracle
- Ensures license compliance

---

## Cost Optimization Patterns

### Reduce Data Transfer Costs
- Use **CloudFront**
  - Content served from Edge Locations
  - Reduces data transfer from EC2/S3

---

### Optimize Network Costs
- Use **Direct Connect**
  - Cheaper than internet egress for large data transfers

- Use **VPC Endpoints (S3/DynamoDB)**
  - Avoid NAT Gateway charges
  - Keeps traffic within AWS network

---

### Storage Optimization
- Use **S3 Lifecycle Policies**
  - Automatically move data to cheaper storage classes
  - Example: Standard → Glacier → Deep Archive

---

### Compute Optimization
- Use **Aurora Serverless / DynamoDB On-Demand**
  - Ideal for unpredictable workloads
  - Avoid paying for idle capacity

- Use **Spot Instances**
  - Very low cost compute
  - Best for fault-tolerant workloads (e.g., EMR task nodes)

---

### Database Cost Awareness
- RDS Read Replicas:
  - Same region → free data transfer
  - Cross-region → charged

---

## Key Exam Tips

- CloudFront reduces **data transfer cost**
- VPC Endpoint avoids **NAT Gateway charges**
- Spot Instances = **cheapest compute**
- CUR = **most detailed billing data**
- Compute Optimizer = **ML-based recommendations**

---

## Key Summary

- Cost Explorer = visualization
- Budgets = alerts
- CUR = deep billing data
- Trusted Advisor = recommendations
- Compute Optimizer = right-sizing
- Use architecture patterns to reduce cost effectively