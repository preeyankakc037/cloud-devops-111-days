# Day 2 CLOUD and DEVOPS 

**Day2**

1. History of AWS Le

    > Amazon Web Services (AWS) began in the early 2000s when Amazon realized its internal teams were repeatedly rebuilding the same infrastructure like servers and storage, slowing innovation. Under the vision of Jeff Bezos and leadership of Andy Jassy, Amazon transformed these internal tools into a public service, launching AWS in 2006 with services like S3 and EC2. This introduced the concept of cloud computing allowing businesses to access scalable computing resources on demand without owning physical hardware. AWS quickly gained adoption from startups and enterprises, fundamentally changing how software is built and deployed by making infrastructure faster, cheaper, and highly scalable, and ultimately revolutionizing the tech industry.
    
    Top companies that runs in aws are: Netflix, Twitch, LinkedIn

2. How AWS actually work 
    > For delivering high availability, low latency and resilient cloud services for workload of all sizes, AWS heavily depends on global infrastructure that can be categorized into, 
* **AWS Region** 
    
     What is not a region? 

        A country (India, Nepal, USA)
        A single data center
        A server or machine
        A software/service like S3 or EC2
            
    What actually is a region? 

    >An AWS Region is a specific geographic area where AWS operates multiple data centers (Availability Zones) to run cloud services. For example: Mumbai and Banglore region and these regions has muliple AZs.  
    * Services in AWS are mostly region scoped. 
    * Each Region operates independently to provide fault isolation, data residency, compliance, and low-latency access to users in various locations.


* **Availability Zones(AZs)**

    * AZs are basically the collections of mulitple physically seperated Data centers inside a region.
    * AZs are situated far enough apart to prevent outages impacting more than one, but close enough for low latency and high-speed data replication.
    * Deployment across multiple AZs enhances application fault tolerance and availability.

    

* **AWS Data Centers**

   * Data Centers are the physical facilities housing AWS computing, storage, and networking hardware.
   * Multiple data centers make up an Availability Zone; they provide redundancy, security, and continuous operation within AWS Regions.

* **AWS Edge Locations / Points of Presence**
   * Edge Locations, or Points of Presence, are AWS sites worldwide used primarily for caching content close to end users, powering services like Amazon CloudFront.
   * They enable faster content delivery, reduce latency, and improve user experience for globally distributed applications.

#111DaysOfLearningForChange #CodeForChange #Day1LearningForChange #CloudComputing #DevOps #AWS
