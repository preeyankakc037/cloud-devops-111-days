
# Day 10
#111DaysOfLearningForChange 

**Amazon CloudFront**

Amazon CloudFront is a CDN that delivers content globally with low latency by caching it at edge locations. It reduces load on origin servers and improves performance. Used for fast content delivery, websites, APIs, and media streaming.

**Amazon Redshift**

Amazon Redshift is a fully managed data warehouse designed for large-scale analytics and complex queries. It is optimized for OLAP workloads and works well with BI tools. Used for analytics, reporting, and big data queries (not transactions).

**Amazon Kinesis Data Firehose**

Amazon Kinesis Data Firehose is a fully managed service that collects, transforms, and loads streaming data into destinations like S3, Redshift, or Elasticsearch. It automatically scales and requires no management. Used for real-time data ingestion and analytics pipelines.

**AWS Elastic Beanstalk**

AWS Elastic Beanstalk is a PaaS service that lets you deploy and manage applications without handling infrastructure. You upload code, and it automatically provisions EC2, load balancers, and scaling. Used for quick app deployment with minimal management.

**AWS OpsWorks**

AWS OpsWorks is a configuration management service using Chef/Puppet to automate server setup and management. It gives more control than Beanstalk but requires more effort. Used for custom infrastructure automation.

**Amazon SQS**

Amazon Simple Queue Service is a fully managed message queue that decouples systems and stores messages until processed. It ensures reliability and handles spikes. Used for asynchronous processing and decoupled architectures.

**Amazon Athena**

Amazon Athena is a serverless service that lets you run SQL queries directly on data stored in S3 without loading it into a database. Used for ad-hoc analysis and querying logs/data in S3.

**AWS CloudTrail**

AWS CloudTrail records all API calls and user activity in your AWS account for auditing and security. Used for compliance, monitoring, and tracking changes.

**Proxies & Performance**
Forward Proxy (VPN concept)

**A forward proxy** sits between client and internet, hiding the client identity (like VPN). Used for privacy, filtering, and outbound control.

**Reverse Proxy (Nginx concept)**

A reverse proxy sits in front of servers, handling requests and forwarding to backend (like load balancer). Used for security, load balancing, caching.

**RDS Proxy**

Amazon RDS Proxy is a managed proxy that pools and manages database connections, improving scalability and avoiding overload. Used when many connections (like Lambda → DB).

**Memcached vs Redis**
Memcached → simple, multi-threaded, faster for basic caching
Redis → more powerful (persistence, data structures), slightly heavier



Simple cache → Memcached
Advanced cache / persistence → Redis
AWS KMS

AWS Key Management Service is a managed service to create and control encryption keys used to secure data across AWS services. Used for encryption, compliance, and security control.