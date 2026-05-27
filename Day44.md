# Day 44: AWS Global Accelerator

## What I Learned Today

Today I learned about AWS Global Accelerator, a service that improves the availability and performance of applications with global users.

## 1. What is AWS Global Accelerator

AWS Global Accelerator is a networking service that routes user traffic through AWS global network to the nearest healthy endpoint.

Key Idea:

* Uses AWS edge locations
* Provides static IP addresses
* Improves latency and reliability

## 2. How It Works

Flow:

User Request
↓
Anycast IP (Global Accelerator)
↓
Nearest AWS Edge Location
↓
AWS Global Network
↓
Best Performing Region Endpoint

## 3. Important Concepts

Static IPs:

* Provides 2 fixed IP addresses
* No DNS changes needed

Anycast Routing:

* Traffic goes to nearest edge location automatically

Health Checks:

* Detects unhealthy endpoints
* Routes traffic to healthy ones

## 4. Endpoints

Global Accelerator routes traffic to endpoints such as:

* EC2 instances
* Application Load Balancer
* Network Load Balancer
* Elastic IP

## 5. Traffic Routing

Global Accelerator selects endpoint based on:

* Health
* Latency
* Configuration (weight, traffic dial)

## 6. Failover Mechanism

If endpoint fails:

Endpoint Unhealthy
↓
Health Check Fails
↓
Traffic redirected
↓
Healthy Endpoint

## 7. Global Accelerator vs CloudFront

Global Accelerator:

* Works at TCP/UDP level
* Improves performance for non-HTTP apps
* Uses static IPs

CloudFront:

* CDN for HTTP/HTTPS
* Caches content
* Uses DNS routing

## 8. When to Use

* Global applications with users worldwide
* Need low latency
* Need static IP addresses
* Real-time apps (gaming, IoT, APIs)

## Final Understanding

Today I understood that AWS Global Accelerator:

* Uses AWS global network for faster routing
* Improves availability with health checks
* Provides static IPs
* Helps route users to the best endpoint globally

## Quick Self Questions

1. What is AWS Global Accelerator?
2. What is Anycast routing?
3. How does Global Accelerator improve latency?
4. Difference between Global Accelerator and CloudFront?
5. What happens when an endpoint fails?
6. What are endpoints in Global Accelera
