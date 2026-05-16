# Day33 of Learning for Change  
#111DaysOfLearningForChange  

Today I learned about **AWS Networking & VPC (Virtual Private Cloud)**:

* **VPC (Virtual Private Cloud)** – A private network in AWS where you control IP range, subnets, routing, and security.  

* **Regions & Availability Zones** – Regions are physical locations (like Mumbai), and AZs are isolated data centers inside them for high availability.  

* **CIDR Blocks** – Define the IP address range of your VPC (e.g., 10.0.0.0/16).  

* **Subnets** – Smaller networks inside a VPC:  
  - Public Subnet → Has internet access  
  - Private Subnet → No direct internet access (used for databases, secure apps)  

* **Routing Tables** – Rules that decide where network traffic goes (internet, private network, etc.).  

* **Internet Gateway (IGW)** – Allows communication between VPC and the internet.  

* **Security Groups** – Instance-level firewall (only allow rules, stateful).  

* **Network ACLs (NACLs)** – Subnet-level firewall (allow & deny rules, stateless).  

* **NAT Gateway** – Lets private subnet instances access the internet safely (outbound only).  

---

## Advanced Networking Concepts:

* **VPC Peering** – Connect two VPCs privately.  

* **VPC Endpoints** – Access AWS services (like S3) without using the internet.  

* **Bastion Host** – A secure jump server to access private instances.  

* **Elastic IP** – Static public IP address.  

* **VPC Flow Logs** – Monitor network traffic in your VPC.  

* **Direct Connect** – Dedicated private connection from on-premises to AWS.  

* **AWS Client VPN** – Secure remote access to AWS resources.  