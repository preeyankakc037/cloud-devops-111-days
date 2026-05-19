# Day 36 – AWS Cheat Sheet
111DaysOfLearningForChange

CHEATSHEET

## Amazon S3

* Storage Class Analysis

  * Analyze access patterns
  * Transition: Standard → Standard-IA

* When access pattern is unknown

  * Use S3 Intelligent-Tiering

* Access with CloudFront

  * Origin Access Identity (OAI)

* Signed Access

  * Signed URL: Single file access
  * Signed Cookies: Multiple files / platform access

* Cost Note

  * Standard-IA may be cheaper than Glacier Instant Retrieval depending on usage

* Networking

  * S3 is not inside VPC
  * Uses public IP and public virtual interface

---

## VPC and Networking

* VPC Endpoint

  * Private connection to AWS services
  * Example: VPC → S3
  * Gateway Endpoint is free

* Gateway Endpoint

  * Used for S3 and DynamoDB

* VPC Peering

  * Connects only two VPCs
  * Does not support on-premises connectivity

* Transit Gateway

  * Connects multiple VPCs and on-premises
  * Supports star topology
  * Paid service

* Elastic IP

  * Default limit: 5 per account

* Bastion Host

  * Used to access private instances securely

---

## Databases

* DynamoDB

  * Supports DAX

* RDS

  * Does not support DAX

* Time Series Data

  * Use Amazon Timestream

---

## Security

* VPN

  * Encrypted communication

* Amazon Inspector

  * Detects vulnerabilities in:

    * EC2
    * ECR
    * Lambda
    * Code repositories and CI/CD

---

## Compute and Containers

* AWS Fargate

  * Serverless container execution

* Containers vs VM

  * Containers are lightweight and faster to deploy

* Temporary Queues

  * Reduce deployment cost and time

---

## Storage (EBS)

* Multi-Attach Volumes

  * Supported by io1 and io2

---

## High Availability vs Performance

* Read Replica

  * Improves read performance
  * Not for high availability

* Multi-AZ

  * Provides high availability
  * Automatic failover

---

## Load Balancing

* Elastic Load Balancer (ELB)

  * Distributes traffic across instances

---

## Dedicated Infrastructure

* Dedicated Hosts

  * Supports bring your own license (BYOL)

---

## Migration

* AWS Application Migration Service (MGN)

  * Replication
  * Cutover

---

## Data Streaming

* Kinesis Data Streams

  * On-Demand: Serverless
  * Provisioned: Manually managed

---

## Key Exam Notes

* S3 + VPC + DynamoDB → Gateway Endpoint
* Transit Gateway → Star topology + on-premises
* VPC Peering → Only two VPCs
* DynamoDB supports DAX, RDS does not
* Multi-AZ is for availability, Read Replica is for performance
* S3 is outside VPC
* Elastic IP limit is 5
