# Day 6 
#111DaysOfLearningForChange


Today first I am starting by clearing my doubts on DNS, I heard this name so many times but haven't googled deep down into it, 

**1.) What is Domain Name System?**
It's like a phonebook, we humans remembers google.com, but computers understand numbers called ip address like: 142.250.183 . This IP is equivalent to google.com.

>DNS translates the easy name into the IP address so our browser knows where to go.

So, we were in VPC and this actual thing start from this line when i didn't fully understand it; 

**“Instances in the default VPC also get assigned both public and private IPv4 DNS names,”**
it means Amazon EC2 instances gets easy-to-read names instead of only IP addresses.A public DNS name is used when accessing the instance from the internet, while a private DNS name is used for communication inside the VPC (between AWS resources). So instead of remembering numbers, AWS gives our instance a readable address—like giving our house both a street name and a private apartment number.

now what is Private and Public DNS

* Public DNS 
    
    It's a name used to reach our Amazon EC2 instance from the internet. It's linked to the instance's public IP address, so if someone outside AWS wants to connect they will use the public DNS name. 
    >We can think of it like our home address that anyone can use to send us a letter

* Private DNS 
    
    It's the name used only inside our VPC(our private AWS network). It is linked to the private IP address, so other AWS resources like servers or databases inside the same network use this name to communicate. 
    > We can think of this like a room number inside our house, useful for people already inside, but not for outsiders.

**2.) What is Subnet?**

A **subnet** is like dividing a big neighborhood into smaller streets. In AWS, your VPC is the whole neighborhood (private network), and subnets are the smaller sections inside it where you place your resources like Amazon EC2 instances. Some subnets are **public subnets**, where resources can connect to the internet (like houses on the main road), and some are **private subnets**, where resources stay hidden and only communicate internally (like houses inside a gated colony). This helps organize resources, improve security, and control network traffic easily.


> Example: for example I am building an online shopping website. I place a web server(the part users visit) in a public subnet so customers on the internet can access it. But the database, which stores customer details and payment information, is placed in a private subnet so no one from the internet can directly reach it. The web server can talk to the database inside the VPC, but outsiders cannot. This keeps sensitive data safer while still allowing the website to work smoothly.

# VPC To be continued..............

* We can create multiple Vpcs within a single AWS region; the default soft limit is 5 per region. 
* Each VPC can have up to 5 IPv4 CIDR blocks associated with it. 
* Each CIDR block size ranges from a minimum of /28 (16 IP address) to maximum of /16 (65,536 IP addresses )


**Private IPv4 Address Ranges in VPC (RFC 1918)**


A VPC (Virtual Private Cloud) is your own private network inside AWS. Since it is private, AWS only allows private IPv4 address ranges inside the VPC, not public internet IP addresses.

These private IP ranges are defined by RFC 1918:

* 10.0.0.0/8 → Large network range
* 172.16.0.0/12 → Medium network range
* 192.168.0.0/16 → Small network range

These IP addresses are used for internal communication between AWS resources like Amazon EC2 instances, databases, and applications inside the VPC.

> Example
If an EC2 instance has a private IP like 10.0.1.5, it means the instance is inside the private AWS network and cannot be directly accessed from the internet.

To access it from the internet, AWS must assign a public IP separately.

Simple Idea
Private IP = Used inside the VPC only
Public IP = Used to connect from the internet