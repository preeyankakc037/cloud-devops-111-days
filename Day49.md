# Day 49 – AWS Compute

Today I studied AWS Compute services and how AWS provides scalable compute options across cloud, hybrid, and edge environments.

---

## AWS Batch

- Fully managed batch processing service
- Runs large-scale batch jobs using containers
- Automatically provisions compute resources
  - EC2 or Spot Instances
- Optimized for cost and scalability

---

## Amazon EC2 (Elastic Compute Cloud)

- Virtual servers in the cloud
- Highly customizable compute service

### Key Options
- Instance Types:
  - Compute Optimized
  - Memory Optimized
  - Storage Optimized
- Pricing Models:
  - On-Demand → pay per use
  - Reserved → long-term discount
  - Spot → cheapest, can be interrupted

---

## Amazon EC2 Auto Scaling

- Automatically adjusts number of EC2 instances

### Scaling Types
- Target Tracking → maintain specific metric (e.g., CPU)
- Step Scaling → scale in steps
- Scheduled Scaling → based on time
- Predictive Scaling → forecast-based scaling

---

## AWS Elastic Beanstalk

- Platform as a Service (PaaS)
- Deploy applications without managing infrastructure

### Supports
- Java, Node.js, Python, PHP, etc.

- Automatically handles:
  - Load balancing
  - Scaling
  - Monitoring

- Best for:
  - Lift-and-shift web applications

---

## AWS Outposts

- AWS infrastructure installed on-premises
- Extends AWS services to your data center

### Supports
- EC2
- RDS
- ECS

- Use case:
  - Low-latency or data residency requirements

---

## AWS Serverless Application Repository

- Collection of pre-built serverless apps
- Deploy directly into your AWS account
- Helps reuse architectures and speed up development

---

## VMware Cloud on AWS

- Run VMware workloads on AWS
- Uses AWS bare-metal infrastructure

### Benefits
- No refactoring needed
- Easy migration from on-prem VMware

---

## AWS Wavelength

- Brings AWS services closer to mobile users
- Runs inside 5G networks

### Benefits
- Ultra-low latency
- Ideal for:
  - Gaming
  - AR/VR
  - Real-time apps

---

## Key Summary

- EC2 = core compute service
- Auto Scaling = automatic scaling
- Batch = large-scale job processing
- Beanstalk = easy app deployment (PaaS)
- Outposts = hybrid AWS (on-prem)
- VMware Cloud = lift-and-shift VMware
- Wavelength = ultra-low latency edge compute