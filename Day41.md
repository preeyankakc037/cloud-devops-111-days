# Day 41: High Availability & Fault Tolerance (AWS)

## What I Learned Today

Today I focused on one of the most important AWS concepts: designing highly available and fault-tolerant systems.

## 1. High Availability vs Fault Tolerance

High Availability:

* Application remains available most of the time
* Uses multiple resources across Availability Zones

Fault Tolerance:

* System continues without interruption
* No downtime even if a component fails

## 2. AWS Regions and Availability Zones

Region:

* A geographic location (example: us-east-1)

Availability Zone:

* Isolated data centers inside a region

Flow:

User Request
↓
Route 53
↓
Region
↓
Multiple AZs

## 3. Multi-AZ Architecture

Application is deployed across multiple AZs.

Flow:

Load Balancer
↓        ↓
EC2 (AZ1)  EC2 (AZ2)

If one AZ fails, traffic is routed to the other.

## 4. Elastic Load Balancer (ELB)

* Distributes traffic across instances
* Improves availability and scalability

Types:

* Application Load Balancer
* Network Load Balancer

## 5. Auto Scaling Group (ASG)

Automatically adjusts number of EC2 instances.

Flow:

High Traffic → Add Instances
Low Traffic → Remove Instances

## 6. Health Checks

Used to monitor instance health.

Flow:

Instance fails
↓
Removed from Load Balancer
↓
New instance launched

## 7. Stateless vs Stateful Applications

Stateless:

* No data stored on instance
* Easy to scale

Stateful:

* Stores data
* Needs external storage

Best Practice:

* Use S3, RDS, or DynamoDB

## 8. Database High Availability (RDS Multi-AZ)

Primary DB
↓ (sync replication)
Standby DB

Automatic failover if primary fails.

## 9. Read Replicas

Used to scale read traffic.

Primary DB
↓
Read Replica 1
Read Replica 2

## 10. Amazon S3 Durability

* 99.999999999% durability
* Data stored across multiple AZs

## 11. Route 53 Routing Policies

* Simple
* Weighted
* Latency-based
* Failover

Failover Flow:

Primary Endpoint
↓
If unhealthy → Secondary Endpoint

## Final Understanding

Today I learned how AWS ensures systems are:

* Highly available
* Fault tolerant
* Scalable

Key services:

* EC2
* ELB
* Auto Scaling
* RDS
* S3
* Route 53

## Quick Self Questions

1. What is high availability?
2. What is fault tolerance?
3. What is Multi-AZ architecture?
4. What does a Load Balancer do?
5. How does Auto Scaling work?
6. What is RDS Multi-AZ?
7. What are read replicas?
8. Why is S3 durable?
9. What is Route 53 failover routing?
