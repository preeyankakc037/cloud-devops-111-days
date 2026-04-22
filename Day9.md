# Day 9 
#111DaysOfLearningForChange 

**Traffic Mirroring**

Traffic Mirroring in AWS lets you capture and inspect network traffic from your EC2 instances in real time by copying it to monitoring tools (like intrusion detection systems). It does not block or analyze threats itself—it simply gives you visibility into what’s happening inside your network. It’s mainly used for deep inspection, debugging, and security analysis when you want to see packet-level data.

**Amazon GuardDuty**

Amazon GuardDuty is a threat detection service that continuously monitors your AWS environment for suspicious activity using logs like VPC Flow Logs, DNS logs, and CloudTrail. It uses machine learning and threat intelligence to detect things like compromised instances, unusual API calls, or malware behavior. It does not block traffic—it detects and alerts you about potential threats.

**AWS Network Firewall**

AWS Network Firewall is a fully managed firewall that sits inside your VPC and actively filters and blocks traffic based on rules you define (like IPs, domains, ports, or protocols). It works at the network level to enforce security policies and prevent malicious traffic from entering or leaving your network.

**AWS Lambda**

AWS Lambda is a serverless compute service that runs your code automatically in response to events (like file uploads, API calls, or messages) without you managing servers. You only pay for execution time, and it scales instantly. It is mainly used for event-driven processing, automation, and backend logic, where you want code to run only when triggered.

**Amazon SQS (Simple Queue Service)**

Amazon Simple Queue Service is a fully managed message queue that allows different parts of a system to communicate asynchronously by sending and receiving messages. It helps decouple applications, ensuring that one component can continue working even if another is slow or temporarily unavailable. Messages are stored in the queue until they are processed.

**Amazon CloudFront**

Amazon CloudFront is a Content Delivery Network (CDN) that delivers your content (websites, images, videos, APIs) to users with low latency by caching it at edge locations around the world. Instead of users accessing your server directly, they get data from the nearest edge location, making applications faster and more scalable. It is mainly used for speed optimization, global content delivery, and reducing load on origin servers.

**Amazon API Gateway**

Amazon API Gateway is a fully managed service to create, publish, and manage APIs that act as a front door for applications. It handles tasks like request routing, authentication, rate limiting, and scaling, and commonly connects client requests to backend services like Lambda. It is mainly used for building secure, scalable APIs for applications.


**AWS Shield Advanced**

AWS Shield Advanced is a managed DDoS protection service that protects your AWS applications from large-scale Distributed Denial of Service (DDoS) attacks. It provides always-on detection and automatic mitigation of network and application layer attacks, and also gives access to AWS DDoS response team (DRT) support. It is mainly used for protecting high-value, internet-facing applications where uptime and security are critical.

**Elastic Load Balancer (ELB)**

Elastic Load Balancing is a service that automatically distributes incoming application traffic across multiple targets (like EC2 instances, containers, or IPs) to improve availability and fault tolerance. It ensures no single server gets overloaded and helps applications scale smoothly. It is mainly used for high availability, scalability, and fault tolerance of applications.

**Bastion Host**

A Bastion Host is a special EC2 instance placed in a public subnet that acts as a secure entry point to access private resources inside a VPC. Instead of exposing private servers directly to the internet, administrators first connect to the bastion host (via SSH or RDP), and then jump into private instances. It is mainly used for secure administrative access to private resources without exposing them publicly.