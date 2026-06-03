# Day 51 – AWS Route 53 & DNS Routing

Today I studied Amazon Route 53 and its DNS routing policies, health checks, and alias record behavior used for highly available and globally distributed applications.

---

## Amazon Route 53

- Fully managed DNS (Domain Name System) service
- Routes user requests to AWS or external resources
- Supports domain registration, DNS resolution, and traffic routing policies

---

## DNS Routing Policies

### Simple Routing
- Routes traffic to a single resource
- No health checks
- Used for basic, single-endpoint applications

---

### Weighted Routing
- Distributes traffic based on percentage
- Used for:
  - A/B testing
  - Gradual deployments
  - Canary releases

---

### Latency-Based Routing
- Routes users to the AWS region with lowest latency
- Improves performance for global users

---

### Geolocation Routing
- Routes traffic based on user location (country/continent)
- Useful for:
  - Content localization
  - Regulatory compliance

---

### Geoproximity Routing
- Routes based on geographic distance
- Allows biasing traffic toward specific regions
- Requires Route 53 Traffic Flow

---

### Failover Routing
- Active-passive setup
- Primary endpoint → Secondary endpoint
- Uses health checks to detect failures

---

### Multivalue Routing
- Returns multiple healthy IP addresses
- Basic health check support
- NOT a replacement for load balancers

---

## Health Checks

- Monitor endpoint health (HTTP, HTTPS, TCP)
- Used with:
  - Failover routing
  - Weighted routing
  - Latency routing
- Helps Route 53 avoid unhealthy endpoints

---

## Alias Records

- Route 53 specific feature
- Points DNS name to AWS resources directly

### Key Features
- Free (no extra cost per query)
- Can point to:
  - Elastic Load Balancers
  - CloudFront distributions
  - S3 static website endpoints
  - API Gateway
- Can be used at **zone apex** (example.com)

### Alias vs CNAME
- CNAME:
  - Cannot be used for root domain (zone apex)
- Alias:
  - Can point to root domain
  - AWS-native integration

---

## Key Exam Notes

- Simple → single endpoint, no health checks
- Weighted → traffic splitting for testing
- Latency → best performance routing
- Geolocation → location-based routing
- Geoproximity → distance + bias (Traffic Flow required)
- Failover → primary/secondary setup
- Multivalue → multiple healthy responses
- Alias → AWS resource DNS mapping (free + apex support)