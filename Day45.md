# Day 46 – AWS Management, Governance & Media Services

## Management and Governance

### AWS Auto Scaling

* Central umbrella service to manage Auto Scaling across services
* Supports EC2, ECS, DynamoDB, Aurora, and more
* Unified interface for scaling policies

### AWS CloudFormation

* Infrastructure as Code (IaC)
* Define resources using JSON or YAML templates
* Deploy as reusable stacks

### AWS CloudTrail

* Logs all API activity in your AWS account
* Tracks: who, what, when, where
* Critical for auditing and compliance

### Amazon CloudWatch

* Monitoring for metrics, logs, and events
* Create alarms and dashboards
* Integrates with Auto Scaling and Lambda

### AWS CLI

* Command-line tool for AWS interaction
* Enables automation via scripts
* Useful for administration tasks

### AWS Compute Optimizer

* Uses ML to analyze resource usage
* Recommends optimal configurations
* Covers EC2, EBS, Lambda, ECS

### AWS Config

* Tracks configuration changes over time
* Maintains resource history
* Enables compliance rules

### AWS Control Tower

* Sets up secure multi-account environment
* Provides landing zone using best practices
* Built on AWS Organizations

### AWS Health Dashboard

* Personalized alerts for AWS events
* Notifies about outages and maintenance
* Resource-specific impact insights

### AWS License Manager

* Manages BYOL licenses
* Tracks usage across EC2 and on-prem
* Supports SQL Server, Oracle, etc.

### Amazon Managed Grafana

* Managed visualization service
* Integrates with CloudWatch, Prometheus
* Dashboards for metrics and observability

### Amazon Managed Service for Prometheus

* Managed time-series monitoring
* Prometheus-compatible queries
* Integrates with EKS and Grafana

### AWS Organizations

* Multi-account management
* Consolidated billing
* Organizational Units (OUs)
* Service Control Policies (SCPs)

### AWS Proton

* Managed deployment for container/serverless apps
* Platform teams define templates
* Developers self-serve deployments

### AWS Service Catalog

* Centralized approved service templates
* Uses CloudFormation
* Enables self-service provisioning

### AWS Systems Manager

* Operations management hub
* Tools: Run Command, Patch Manager, Session Manager, Parameter Store
* Works with EC2 and on-prem servers

### AWS Trusted Advisor

* Best practice recommendations
* Categories: cost, security, performance, fault tolerance
* Some checks require premium support

### AWS Well-Architected Tool

* Reviews workloads against 6 pillars
* Identifies risks and improvements

---

## Media Services

### Amazon Elastic Transcoder

* Legacy video transcoding service
* Converts media files from S3
* Optimizes playback across devices

### Amazon Kinesis Video Streams

* Ingests and stores video streams
* Supports real-time processing
* Integrates with Rekognition for analytics
