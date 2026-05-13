# Day30 of Learning for change  
#111DaysOfLearningForChange  

Today I studied Amazon CloudWatch, a monitoring and observability service used to track AWS resources, applications, and logs in real time.

---

## Amazon CloudWatch – Monitoring & Observability

Amazon CloudWatch is a fully managed service that provides monitoring for AWS resources and applications by collecting metrics, logs, and events.

It helps answer:
> “What is happening in my AWS environment right now?”

---

## CloudWatch Core Components

CloudWatch mainly consists of three key parts:

- Metrics (performance data)
- Logs (detailed event data)
- Metric Streams (real-time metric export)

---

## 1. Amazon CloudWatch Metrics

CloudWatch Metrics represent **numerical performance data over time** for AWS services and applications.

### Examples of Metrics:
- EC2 CPUUtilization
- Memory usage (via agent)
- NetworkIn / NetworkOut
- Lambda duration
- RDS connections

---

### Key Features

- Time-series data (measured over time)
- Used for monitoring system health
- Can trigger alarms when thresholds are breached
- Integrated with Auto Scaling

---

### Use Case

- Detect high CPU usage
- Monitor database performance
- Track application load

---

### Key Insight

CloudWatch Metrics answer:
> “Is my system healthy?”

---

## 2. CloudWatch Metric Streams

CloudWatch Metric Streams enable **real-time streaming of CloudWatch metrics** to external systems.

---

### How It Works

- CloudWatch Metrics are continuously streamed
- Data is sent to services like:
  - Amazon Kinesis Data Firehose
  - Third-party observability tools (Datadog, Splunk, etc.)

---

### Key Features

- Near real-time data delivery
- Continuous export of metrics
- Useful for external monitoring systems
- Reduces need for API polling

---

### Use Case

- Real-time dashboards
- Security analytics pipelines
- External observability platforms

---

### Key Insight

Metric Streams answer:
> “How can I send CloudWatch metrics in real time outside AWS?”

---

## 3. Amazon CloudWatch Logs

CloudWatch Logs store **detailed event-based logs** from AWS services and applications.

---

### Types of Logs

- Application logs
- System logs (EC2)
- Lambda execution logs
- VPC Flow Logs
- CloudTrail API logs

---

### Key Features

- Stores raw event data
- Used for debugging and troubleshooting
- Supports search and filtering
- Can be retained or archived

---

### Use Case

- Debug application errors
- Analyze API failures
- Security investigation

---

### Key Insight

CloudWatch Logs answer:
> “What exactly happened in my system?”

---

## 4. CloudWatch Logs Sources

Logs can be collected from multiple AWS services and environments.

---

### Common Sources

### Compute
- Amazon EC2 (via CloudWatch Agent)
- AWS Lambda (automatic logs)

---

### Networking
- VPC Flow Logs

---

### Security & Governance
- AWS CloudTrail logs (API activity)

---

### Storage
- Amazon S3 access logs (optional)

---

### Application
- Custom application logs (via SDK or CloudWatch Agent)

---

## Metrics vs Logs vs Metric Streams

| Feature | Type | Purpose |
|--------|------|---------|
| Metrics | Numerical data | Performance monitoring |
| Logs | Event data | Debugging & auditing |
| Metric Streams | Data pipeline | Real-time export |

---

## Common Use Cases

### Monitoring
- EC2 CPU usage
- Database performance

### Troubleshooting
- Application errors
- Lambda failures

### Security Monitoring
- Unauthorized API calls (CloudTrail logs)
- Network traffic analysis (VPC Flow Logs)

---

## Key Exam Insight

CloudWatch is used when the question involves:
- Monitoring AWS resources
- Tracking performance metrics
- Debugging application issues
- Collecting logs from AWS services

---

## Final Takeaway

Amazon CloudWatch is the central monitoring service in AWS that provides metrics, logs, and real-time streaming capabilities to help understand system performance, troubleshoot issues, and maintain operational health.