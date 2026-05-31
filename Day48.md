# Day 48 – AWS Serverless & Containers

Today I studied AWS Serverless and Containers concepts covering Lambda, ECS, EKS, API Gateway, and Elastic Beanstalk.

---

## AWS Lambda

* Serverless, event-driven compute service
* Automatically scales based on demand
* Pay per invocation
* Maximum execution timeout: 15 minutes

### Common Triggers

* Amazon S3
* DynamoDB Streams
* SQS
* API Gateway
* EventBridge
* SNS
* Kinesis
* Amazon Cognito

### Lambda@Edge

* Runs Lambda functions at CloudFront edge locations
* Used to modify requests and responses closer to users

---

## Amazon ECS (Elastic Container Service)

* Managed container orchestration service
* Supports Docker containers

### Launch Types

* EC2 Launch Type: You manage EC2 instances
* Fargate Launch Type: Serverless, AWS manages infrastructure

---

## Amazon EKS (Elastic Kubernetes Service)

* Managed Kubernetes service
* Used when Kubernetes API compatibility is required
* Suitable for teams already using Kubernetes tooling

---

## Amazon API Gateway

* Fully managed API management service
* Supports REST, HTTP, and WebSocket APIs
* Integrates with:

  * AWS Lambda
  * HTTP backends
  * AWS services

### Key Features

* Request throttling
* Authentication and authorization
* Caching

---

## AWS Elastic Beanstalk

* Platform as a Service (PaaS)
* Simplifies deployment of web applications
* Automatically handles provisioning, load balancing, scaling, and monitoring
* Best suited for simple web apps or lift-and-shift deployments

---

## Key Summary

* Lambda = event-driven serverless compute
* ECS = container orchestration (AWS native)
* EKS = Kubernetes managed service
* Fargate = serverless containers
* API Gateway = API management layer
* Elastic Beanstalk = PaaS for quick deployments
