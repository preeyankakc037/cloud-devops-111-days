# Day 5 #111DaysOfLearningForChange

* **Global Vs Region Scoped Services**

The AWS Global Services operate in every part of the world and therefore we do not need to select a particular location when using them. They are structured to handle resources on a global basis, that is, a single set up can handle all the resources around the world. To illustrate, AWS Identity and Access Management manages users and permissions worldwide, Amazon Route 53 routes traffic across the globe, Amazon CloudFront serves content promptly around the globe, and AWS WAF secures applications all over the world. Such services are primarily applied to the aspects that must be universal such as security, identity and content delivery.

AWS Region-Scoped Services are in a particular region, which means that we have to determine where our resources are going to be published and consumed. The regions are autonomous and thus, resources in one region do not necessarily interfere with another. Ec2, RDS, and S3 services of Amazon operate in a region of choice, which assists in offering faster service to the local users and makes failures localized to the region. This renders regional services significant in developing applications which require excellent speed, dependability, and the control of data location.

* **AWS SDK**

    * Libraries in various programming languages (e.g., JavaScript,    Python, Java).

    * Enables programmatic access to AWS services in applications.

    * Supports integrations, custom application development and automation.

    * Makes it easier to make calls to AWS APIs, perform authentication, and process responses.


* **IAM**
AWS Identity and Access Management (IAM) is an international AWS service that assists you to safely regulate who is permitted to sway your AWS resources and what they are permitted to do. It enables you to add users, groups, and roles including assigning permissions through policy, so only the appropriate people or services can access particular resources. Simply put, IAM serves as a gatekeeper to your AWS account in terms of security.