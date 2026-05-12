# Day29 of Learning for change  
#111DaysOfLearningForChange  

Today I studied Amazon Athena — a serverless interactive query service that allows SQL-based analysis directly on data stored in Amazon S3.

---

## Amazon Athena – Serverless SQL on S3

Amazon Athena is a fully managed query service that enables users to analyze data in Amazon S3 using standard SQL without requiring any infrastructure setup or maintenance.

It is commonly used as:
> A SQL query engine directly on top of Amazon S3 data.

---

## How Amazon Athena Works

1. Data is stored in Amazon S3
2. Schema is defined using AWS Glue Data Catalog
3. SQL queries are executed in Athena
4. Query results are returned immediately

---

## Key Features

### Serverless Architecture
- No servers to provision or manage
- Automatic scaling based on query demand

### SQL Query Support
- Standard SQL syntax
- Supports joins, aggregations, filtering, and complex queries

### Pay-per-Query Model
- You are charged based on the amount of data scanned
- No cost for idle usage

---

## Architecture Overview

- Amazon S3: Stores raw data (data lake)
- AWS Glue Data Catalog: Manages metadata and schema
- Amazon Athena: Executes SQL queries
- Amazon QuickSight (optional): Used for visualization

---

## Common Use Cases

### Log Analysis
- VPC Flow Logs
- AWS CloudTrail logs
- Application logs

### Business Intelligence
- Sales and revenue analysis
- Customer behavior insights

### Ad-hoc Data Exploration
- Quick analysis without building ETL pipelines

### Data Lake Analytics
- Query structured and semi-structured data such as CSV, JSON, and Parquet files

---
