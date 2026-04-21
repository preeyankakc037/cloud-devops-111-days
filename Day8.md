# Day 8 
#111DaysOfLearningForChange 

**AWS Storage Basics: Block vs Object Storage + EBS
Big Picture First**

AWS storage mainly comes in two important styles:

>Block Storage → like a hard drive

>Object Storage → like a giant warehouse of files


1. Block Storage (EBS concept lives here)
What is Block Storage?

Block storage breaks data into fixed-size blocks and stores them separately. Each block can be accessed directly.

Think:

Like a computer hard disk
OS can read/write specific blocks quickly
AWS Service: Amazon EBS (Elastic Block Store)
What is EBS?

EBS provides block storage volumes for EC2 instances.

Attached to EC2 like a virtual hard disk
Data persists even if EC2 is stopped
Key Properties of EBS
Block-level storage
Attached to a single EC2 instance at a time (in most cases)
Persistent storage (data survives reboot/stop)
High performance (low latency)
EBS Use Case

Example:

EC2 running a database (MySQL)
Database needs fast read/write
EBS acts as its disk storage
Simple Mental Model

EC2 = Computer
EBS = Hard drive connected to that computer

2. Object Storage
What is Object Storage?

Object storage stores data as complete objects.

Each object contains:

Data (file)
Metadata (information about file)
Unique ID
AWS Service: Amazon S3

S3 is the main object storage service in AWS.

Key Properties of Object Storage
Stores complete files, not blocks
Highly scalable (virtually unlimited)
Accessible over HTTP/HTTPS
Not directly attached to EC2
Object Storage Use Case

Example:

Storing images, videos, backups
Website assets (CSS, JS, images)
Data lakes and analytics
Simple Mental Model

S3 = Giant online storage warehouse
Each file = a labeled box with metadata

Block vs Object Storage (VERY IMPORTANT)
Feature	Block Storage (EBS)	Object Storage (S3)
Structure	Fixed-size blocks	Full objects (files)
Access	Direct block access	Via API (HTTP)
Speed	Fast (low latency)	Slower than EBS
Attachment	Attached to EC2	Independent service
Scalability	Limited per volume	Virtually unlimited
Use case	Databases, OS disks	Images, backups, data lakes
Critical Exam Understanding
When to use EBS?
Need OS disk for EC2
Need fast database storage
Need persistent storage attached to a server
When to use S3?
Store files (images, videos, backups)
Static website hosting
Big data storage
Trick AWS likes to test

```
If question says:

“Attach storage to EC2 like a hard disk” → EBS
“Store and retrieve files at scale” → S3
“Data must persist after EC2 stops” → EBS
“Unlimited storage for objects” → S3
One-line Revision
Block storage (EBS): hard-disk-like storage attached to EC2 for fast, persistent data access
Object storage (S3): scalable file storage system where data is stored as objects with metadata