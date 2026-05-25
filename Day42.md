# Day 42 – AWS Notes
#111DaysOfLearningForChange

Today I practice questions related to my SSA-CO3 Exam and here are some of the Learnings. 

## Global Accelerator

* Uses AWS global network to route traffic to optimal endpoints
* Supports TCP and UDP
* Provides static IP addresses
* Improves performance using Anycast routing
* Performs health checks and automatic failover

### Comparison with CloudFront

* CloudFront supports HTTP and HTTPS only
* Does not support UDP
* Global Accelerator supports UDP and non-HTTP use cases

---

## EBS (Elastic Block Store)

* Attached to a single EC2 instance
* Not designed for sharing across multiple ECS tasks on different instances

---

## EFS Throughput Modes

* Bursting Throughput Mode

  * Suitable for small to medium workloads
  * Performance depends on file system size and burst credits

* Provisioned Throughput Mode

  * Suitable for consistent high workloads
  * Fixed throughput independent of storage size

---

## Networking Concepts

* Public IP → Internet Gateway (IGW)

  * Enables internet access
  * Performs NAT for public instances

* Private IP → NAT Gateway / NAT Instance

  * Allows outbound internet access only

---

## Security Groups

Inbound rules can allow:

* Specific IP address (e.g., 1.2.3.4/32)
* CIDR range (e.g., 0.0.0.0/0)
* Another security group

---

## Patch Management

* AWS Systems Manager Quick Setup (Default Host Management)

  * Centralized patching solution
  * Low administrative overhead

---

## Service Control Policy (SCP)

* Deny in SCP overrides all permissions
* Applies to all users and roles including root user
* Does not affect service-linked roles

---

## Data Rollover Concept

* Automatically creates new files based on size or time limits
* Prevents performance issues from very large files

---

## Keyword-Based Decision Making

* Serverless → Lambda
* Cron job → EventBridge Scheduler
* Short execution → Lambda
* Cost-efficient → Avoid EC2 when possible

---

## AWS Config

* Tracks resource configuration
* Evaluates compliance against rules

---

## High Performance Workloads

Keywords:

* HPC cluster
* Sub-millisecond latency
* High throughput
* Parallel file access
* Large datasets (e.g., 150 TB)

Solution:

* Amazon FSx for Lustre

---

## IPv6 Networking

* Egress-Only Internet Gateway

  * Used only for IPv6 outbound traffic
  * Blocks inbound internet traffic

---

## Storage Services

* EFS

  * Primarily for Linux environments

* Amazon FSx

  * Designed for Windows file systems

---

## Core Networking Components

| Service          | Purpose                                 |
| ---------------- | --------------------------------------- |
| Internet Gateway | Public internet access (bi-directional) |
| NAT Gateway      | Outbound internet for private subnet    |
| VPC Endpoint     | Private access to AWS services          |

Summary:

* NAT → Private subnet to internet
* IGW → Public internet access
* VPC Endpoint → AWS service access without internet

---

## SQS Concepts

* Short Polling

  * Frequent checks, higher cost

* Long Polling

  * Waits for messages, more cost-efficient

* Visibility Timeout

  * Prevents duplicate processing

* Delay Timer

  * Delays message availability

---

## AWS WAF

* IP-based controls:

  * Allow or block IPs
  * Rate limiting per IP
  * Geo-based filtering

---

## Identity Concepts

* OIDC and JWT

  * OIDC issues JWT tokens
  * They are not the same

---

## Key Notes

* Global Accelerator supports UDP; CloudFront does not
* EBS is single-instance storage
* Use FSx for Lustre for HPC workloads
* Use Lambda for short, serverless tasks
* Use EventBridge for scheduled jobs
* Use egress-only IGW for IPv6 outbound traffic only
