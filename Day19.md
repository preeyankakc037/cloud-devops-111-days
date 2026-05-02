# Day19 of Learning for change 
#111DaysOfLearningForChange


Today, I practice some of the questions, I got half of them correct, and half of them wrong. So I practive the concepts I get wrong and why?

![alt text](image-9.png)


2. A media agency stores its re-creatable assets on Amazon Simple Storage Service (Amazon S3) buckets. The assets are accessed by a large number of users for the first few days and the frequency of access falls down drastically after a week. Although the assets would be accessed occasionally after the first week, but they must continue to be immediately accessible when required. The cost of maintaining all the assets on Amazon S3 storage is turning out to be very expensive and the agency is looking at reducing costs as much as possible.

* As an AWS Certified Solutions Architect – Associate, can you suggest a way to lower the storage costs while fulfilling the business requirements?

* Configure a lifecycle policy to transition the objects to Amazon S3 Standard-Infrequent Access (S3 Standard-IA) after 30 days
Configure a lifecycle policy to transition the objects to Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) after 7 days
 
* Configure a lifecycle policy to transition the objects to Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) after 30 days

* Configure a lifecycle policy to transition the objects to Amazon S3 Standard-Infrequent Access (S3 Standard-IA) after 7 days

> MY Answer 

![alt text](image-10.png)
![alt text](image-11.png)

Why answer was wrong? 

-> S3 One Zone-IA is cheaper and risker compared to S3 standard-IA and for recreatable data One Zone IA option was correct but for lifecycle the minimum storage duration is 30 days so it was wrong as i choose 7 days as per the question tricks saying not much accessible after  7 days. 

>**We must keep objects in S3 Standard for at least 30 days before moving them to any IA storage class.**



6. The development team at an e-commerce startup has set up multiple microservices running on Amazon EC2 instances under an Application Load Balancer. The team wants to route traffic to multiple back-end services based on the URL path of the HTTP header. So it wants requests for https://www.example.com/orders to go to a specific microservice and requests for https://www.example.com/products to go to another microservice.

Which of the following features of Application Load Balancers can be used for this use-case?

* Query string parameter-based routing
* HTTP header-based routing
* Host-based Routing
* Path-based Routing  *correct


-> 
 * Query string parameter-based routing
* HTTP header-based routing
* Host-based Routing

None of these three types of routing support requests based on the URL path of the HTTP header. Hence these three are incorrect.

| Routing Type                  | What it Uses    | Example                                 | When to Use                            | Matches `/orders` case? |
| ----------------------------- | --------------- | --------------------------------------- | -------------------------------------- | ----------------------- |
| **Path-based routing**        | URL path        | `example.com/orders`                    | Different microservices by path        | ✅ YES                   |
| **Host-based routing**        | Domain/hostname | `api.example.com` vs `shop.example.com` | Multiple apps on different domains     | ❌ NO                    |
| **HTTP header-based routing** | Request headers | `User-Agent: Mobile`                    | Route by device, language, app version | ❌ NO                    |
| **Query string routing**      | URL parameters  | `?category=books`                       | Filter-based routing (search, filters) | ❌ NO                    |


7. An e-commerce company is looking for a solution with high availability, as it plans to migrate its flagship application to a fleet of Amazon Elastic Compute Cloud (Amazon EC2) instances. The solution should allow for content-based routing as part of the architecture.

As a Solutions Architect, which of the following will you suggest for the company?


* Use a Network Load Balancer for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure a Private IP address to mask any failure of an instance
* Use an Auto Scaling group for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure a Public IP address to mask any failure of an instance
* Use an Auto Scaling group for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure an elastic IP address (EIP) to mask any failure of an instance
 * Use an Application Load Balancer for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure Auto Scaling group to mask any failure of an instance

Correct answer:

Use an Application Load Balancer for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure Auto Scaling group to mask any failure of an instance


Why

Use an Application Load Balancer because it supports content-based routing, and Auto Scaling ensures high availability by replacing failed EC2 instances automatically.