# Day 38: Analytics (AWS)

## Goal

Understand core analytics services by **use-case + when to choose what** (very high exam weight).



## Core Strategy for Analytics Questions

* Batch vs Real-time?
* Structured vs Streaming data?
* Query vs Transform vs Visualize?



## 📊 Query & Data Analysis

### Amazon Athena

* Serverless SQL queries directly on S3
* Pay per data scanned
* “query S3 using SQL” → Athena




## 🔄 ETL (Extract, Transform, Load)

### AWS Glue

* Serverless ETL + Data Catalog
* Crawlers auto-detect schema
* “ETL + serverless + schema discovery” → Glue


### AWS Data Pipeline (Legacy)

* Scheduled data movement
* Avoid in exam → prefer Glue




## 📦 Big Data Processing

### Amazon EMR

* Managed Hadoop/Spark cluster
* Use Spot for cost savings
* “big data cluster / Spark / Hadoop” → EMR



## 🌊 Streaming Data

### Amazon Kinesis

* Real-time streaming

**Kinesis Data Streams**

* Custom processing, real-time
* You manage consumers

**Kinesis Firehose**

* Fully managed delivery
* Sends to S3, Redshift, OpenSearch

“real-time streaming” → Kinesis


## 🗄️ Data Lake

### AWS Lake Formation

* Build & secure data lakes on S3
* Fine-grained access control
* “data lake governance” → Lake Formation



## 📥 External Data

### AWS Data Exchange

* Subscribe to 3rd-party datasets
* Delivered to S3
* “buy external data” → Data Exchange



## 📨 Messaging / Streaming Alternative

### Amazon MSK (Managed Kafka)

* Use when Kafka API required
* Otherwise prefer Kinesis



## 🔍 Search & Log Analytics

### Amazon OpenSearch

* Full-text search + log analytics
* Kibana dashboards
* “logs / search / analytics dashboard” → OpenSearch



## 📈 Visualization (BI)

### Amazon QuickSight

* Serverless dashboards
* Connects to AWS data sources
* “BI dashboard / visualization” → QuickSight



## 🏢 Data Warehouse

### Amazon Redshift

* Columnar data warehouse (OLAP)
* Massive parallel processing (MPP)
* data warehouse / analytics at scale” → Redshift



## High-Yield Exam Shortcuts

* Query S3 → Athena
* ETL → Glue
* Big data cluster → EMR
* Streaming → Kinesis
* Data lake → Lake Formation
* Kafka → MSK
* Logs/search → OpenSearch
* Dashboards → QuickSight
* Data warehouse → Redshift

---

## 🧪 Common Exam Traps

* Athena vs Redshift → Athena = S3 query, Redshift = warehouse
* Kinesis vs MSK → Kinesis preferred unless Kafka needed
* Glue vs Data Pipeline → Glue (serverless, modern)
* Firehose vs Streams → Firehose = no code, Streams = custom processing



## ⚡ Final 1-Line Memory Trick

👉 "Analytics = store (S3) → process (Glue/EMR/Kinesis) → query (Athena/Redshift) → visualize (QuickSight)"
