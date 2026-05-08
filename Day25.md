# Day25 of Learning for change 
#111DaysOfLearningForChange






# 1. CloudFront + S3 (Static Website)

## Pattern

* Amazon CloudFront in front
* Amazon S3 as origin

## Why?

* Global caching → low latency
* Reduces load on S3
* Cost optimization

## Key Exam Points

* Use **Origin Access Control (OAC)** → make S3 private
* CloudFront serves content, NOT S3 directly
* Use for static websites (HTML, CSS, JS)

## Trick

If question says:

* "global users + faster delivery" → CloudFront
* "secure S3 content" → OAC

---

# 2. CloudFront + ALB + EC2 (Dynamic Content)

## Pattern

* CloudFront → Application Load Balancer → Amazon EC2

## Why?

* Cache static parts
* Route dynamic traffic to backend

## Key Exam Points

* ALB handles HTTP/HTTPS routing
* EC2 runs application logic
* CloudFront reduces latency

## Trick

Static + Dynamic → CloudFront + ALB

---

# 3. SQS + Lambda (Event Processing)

## Pattern

* Amazon SQS → AWS Lambda

## Why?

* Decouple systems
* Async processing

## Key Exam Points

* Lambda polls SQS
* Visibility timeout must be tuned
* Supports batch processing

## Trick

If question says:

* "decouple + async" → SQS
* "no server management" → Lambda

---

# 4. SNS + SQS (Fan-Out Pattern)

## Pattern

* Amazon SNS → multiple SQS queues

## Why?

* One message → many consumers

## Key Exam Points

* Each SQS gets a copy
* Reliable delivery

## Trick

"Send same message to multiple systems" → SNS fan-out

---

# 5. API Gateway + Lambda (Serverless API)

## Pattern

* Amazon API Gateway → Lambda

## Why?

* Build APIs without servers

## Key Exam Points

* API Gateway handles HTTP
* Lambda executes logic
* Scales automatically

## Trick

If question says:

* "REST API + no servers" → API Gateway + Lambda

---

# 6. RDS + Multi-AZ (High Availability)

## Pattern

* Amazon RDS with Multi-AZ

## Why?

* Failover support

## Key Exam Points

* Synchronous replication
* Automatic failover
* Not for scaling reads

## Trick

"High availability" → Multi-AZ
"Read scaling" → Read Replicas

---

# 7. DynamoDB + DAX (Performance Boost)

## Pattern

* Amazon DynamoDB + DynamoDB Accelerator (DAX)

## Why?

* Microsecond latency

## Key Exam Points

* DAX = in-memory cache
* Improves read performance

## Trick

"Ultra fast reads" → DynamoDB + DAX

---

# 8. S3 + Lifecycle + Glacier (Cost Optimization)

## Pattern

* S3 → lifecycle → Amazon S3 Glacier

## Why?

* Move old data to cheaper storage

## Key Exam Points

* Automatic transitions
* Archive rarely accessed data

## Trick

"Reduce cost for old files" → lifecycle policy

---

# 9. CloudWatch + Auto Scaling (Reactive Scaling)

## Pattern

* Amazon CloudWatch → Auto Scaling → EC2

## Why?

* Scale based on metrics

## Key Exam Points

* CPU-based scaling
* Alarm triggers scaling

## Trick

"Scale when CPU high" → CloudWatch alarm

---

# 10. IAM + S3 Bucket Policy (Security Layers)

## Pattern

* AWS Identity and Access Management (IAM) + S3 policy

## Why?

* Fine-grained access control

## Key Exam Points

* Explicit DENY overrides ALLOW
* Policies combine together

## Trick

"Access issue despite allow" → check DENY

---

# 11. VPC + NAT Gateway (Private Internet Access)

## Pattern

* Private subnet → NAT Gateway → Internet

## Why?

* Instances access internet without being public

## Key Exam Points

* NAT in public subnet
* Private instances use it

## Trick

"Private instance needs internet" → NAT Gateway

---

# 12. Route 53 + Health Checks (Failover)

## Pattern

* Amazon Route 53 with health checks

## Why?

* Route traffic to healthy resources

## Key Exam Points

* DNS-based failover
* Active-passive setup

## Trick

"Failover routing" → Route 53 health check

---

# 13. ELB + Auto Scaling (Elastic Systems)

## Pattern

* Load Balancer + Auto Scaling + EC2

## Why?

* Handle traffic spikes

## Key Exam Points

* ELB distributes traffic
* Auto Scaling adjusts capacity

## Trick

"Traffic increases suddenly" → ELB + Auto Scaling

---

# 14. Step Functions + Lambda (Workflow Orchestration)

## Pattern

* AWS Step Functions → Lambda

## Why?

* Manage multi-step processes

## Key Exam Points

* State machine
* Error handling built-in

## Trick

"Complex workflow" → Step Functions

---

# 15. Kinesis + Lambda (Real-Time Processing)

## Pattern

* Amazon Kinesis → Lambda

## Why?

* Process streaming data

## Key Exam Points

* Real-time analytics
* Event-driven

## Trick

"Streaming data" → Kinesis
