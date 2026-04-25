# Day 12 – AWS SAA-C03 Revision Notes (New Concepts Set 2)

## 1. AWS Step Functions
AWS Step Functions is a serverless orchestration service that allows you to coordinate multiple AWS services into workflows using state machines. It manages the sequence, retries, and error handling of tasks automatically. It is mainly used for building complex, reliable workflows and coordinating microservices.

---

## 2. Amazon DynamoDB
Amazon DynamoDB is a fully managed NoSQL database that provides fast and predictable performance with seamless scalability. It uses key-value and document data models and supports automatic scaling. It is mainly used for high-performance applications requiring low latency at any scale.

---

## 3. Amazon EFS (Elastic File System)
Amazon EFS is a scalable, managed file storage service that can be mounted on multiple EC2 instances simultaneously. It provides shared storage with a standard file system interface. It is mainly used for applications that require shared access to files across multiple instances.

---

## 4. AWS Secrets Manager
AWS Secrets Manager is a service used to securely store, retrieve, and rotate sensitive information such as database credentials, API keys, and passwords. It integrates with other AWS services for automatic secret rotation. It is mainly used for improving security by avoiding hardcoding sensitive data.

---

## 5. AWS Global Accelerator
AWS Global Accelerator improves the availability and performance of applications by routing user traffic through AWS global network infrastructure to the nearest healthy endpoint. It provides static IP addresses and uses intelligent routing. It is mainly used for improving global application performance and failover.

---

# Quick Revision Summary

- Step Functions: Workflow orchestration
- DynamoDB: NoSQL scalable database
- EFS: Shared file storage for EC2
- Secrets Manager: Secure secret storage
- Global Accelerator: Improve global performance

---

# Exam Tips

- If the question involves workflows with multiple steps and error handling, choose Step Functions.
- If low latency and massive scale database is needed, choose DynamoDB.
- If multiple EC2 instances need shared file access, choose EFS.
- If storing passwords or API keys securely, choose Secrets Manager.
- If improving global performance with static IP and routing, choose Global Accelerator.