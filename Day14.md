# AWS Well-Architected Framework – 6 Principles

## 1. Operational Excellence

### Focus
Run systems efficiently and improve continuously.

### Key Points
- Automate manual tasks
- Monitor workloads
- Respond to events
- Learn from failures
- Improve operations regularly

### Example
Using CloudWatch alarms + Lambda automation instead of manual monitoring.

---

## 2. Security

### Focus
Protect data, systems, and access.

### Key Points
- Least privilege access
- IAM roles and policies
- Encryption at rest and in transit
- Threat detection and logging
- Identity management

### Example
Using IAM Role for EC2 to access S3 instead of access keys.

---

## 3. Reliability

### Focus
Ensure systems recover from failures and stay available.

### Key Points
- Backup and recovery
- Fault tolerance
- Auto Scaling
- Multi-AZ deployment
- Disaster recovery planning

### Example
Using RDS Multi-AZ for high availability.

---

## 4. Performance Efficiency

### Focus
Use resources efficiently and scale when needed.

### Key Points
- Choose the right resource type
- Auto Scaling
- Serverless architecture
- Global content delivery
- Continuous performance monitoring

### Example
Using Lambda for short event-driven workloads instead of EC2.

---

## 5. Cost Optimization

### Focus
Avoid unnecessary costs and maximize value.

### Key Points
- Pay only for what you use
- Right-size resources
- Reserved Instances / Savings Plans
- Storage lifecycle policies
- Cost monitoring and budgeting

### Example
Moving old S3 data to Glacier for cheaper storage.

---

## 6. Sustainability

### Focus
Reduce environmental impact of cloud workloads.

### Key Points
- Use managed services
- Reduce idle resources
- Efficient scaling
- Optimize compute and storage
- Minimize unnecessary usage

### Example
Using serverless services instead of always-running EC2 instances.

---

# Quick Exam Mapping

| If Question Mentions | Principle |
|---|---|
| Monitoring + automation | Operational Excellence |
| Access control + encryption | Security |
| Failure recovery + uptime | Reliability |
| Right sizing + scaling | Performance Efficiency |
| Saving money + reducing waste | Cost Optimization |
| Energy efficiency + reducing impact | Sustainability |