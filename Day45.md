# Day 45 – AWS Storage Services

## #111DaysOfLearningForChange

---

## AWS Backup

* Centralized, policy-driven backup service
* Supports:

  * EC2
  * EBS
  * RDS
  * DynamoDB
  * EFS
  * FSx
  * Storage Gateway
* Simplifies compliance with backup retention policies

---

## Amazon EBS (Elastic Block Store)

* Persistent block storage for EC2
* Survives instance stop/restart
* Exists within a single Availability Zone

### Types

* gp3: General purpose SSD
* io2: High IOPS SSD
* st1: Throughput-optimized HDD
* sc1: Cold HDD

---

## Amazon EFS (Elastic File System)

* Managed NFS file system
* Shared across multiple Linux EC2 instances
* Multi-AZ by design
* Automatically scales
* Pay-as-you-use pricing model

---

## Amazon FSx

Managed file systems for specialized workloads:

* FSx for Lustre

  * High-performance workloads (HPC, ML)
  * Integrates with S3

* FSx for Windows File Server

  * SMB protocol
  * Active Directory integration

* FSx for NetApp ONTAP

  * Multi-protocol support

* FSx for OpenZFS

  * Supports ZFS-based migrations

---

## Amazon S3

* Object storage service
* 99.999999999% (11 nines) durability
* Data stored across at least 3 Availability Zones

### Features

* Versioning
* Lifecycle policies
* Replication
* Multiple storage classes:

  * Standard
  * Intelligent-Tiering
  * Standard-IA
  * Glacier
  * Deep Archive

---

## Amazon S3 Glacier

* Low-cost archival storage within S3

### Retrieval Options

* Instant Retrieval: Milliseconds

* Flexible Retrieval: 1 minute to 12 hours

* Deep Archive: 12 to 48 hours

* Most cost-effective for long-term storage

---

## AWS Storage Gateway

* Hybrid storage service connecting on-premises to AWS

### Modes

* S3 File Gateway

  * NFS/SMB access to S3

* Volume Gateway

  * iSCSI-based block storage

* Tape Gateway

  * Virtual tape library for backups

---

## Summary

* AWS Backup centralizes backup management
* EBS is block storage for EC2 (single AZ)
* EFS is shared file storage for Linux (multi-AZ)
* FSx provides specialized file systems
* S3 is durable object storage with multiple tiers
* Glacier is for archival storage
* Storage Gateway enables hybrid cloud storage
