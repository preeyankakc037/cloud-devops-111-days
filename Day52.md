# Day 52 – High-Performing Architectures (CloudFront & Global Acceleration)

Today I studied how AWS improves application performance globally using CloudFront and traffic acceleration strategies.

---

## Amazon CloudFront (CDN)

- Global Content Delivery Network (CDN)
- Caches content at Edge Locations worldwide
- Reduces latency for users

### Supported Origins
- S3 Bucket (private or public)
- Application Load Balancer (ALB)
- EC2 instances
- S3 Static Website (treated as Custom Origin)
- On-premises servers

---

## Origin Access Control (OAC)

- Modern method to restrict S3 access
- Ensures only CloudFront can access private S3 content
- Replaces legacy **Origin Access Identity (OAI)**

⚠️ Exam Trap:
- OAC **does NOT work with S3 Static Website endpoints**
- These are treated as **Custom Origins**
- Bucket must be **public**

---

## Geo Restriction

- Restrict access by country
- Use cases:
  - Licensing restrictions
  - Compliance

👉 For more granular control (IP, paths):
- Use AWS WAF

---

## Cache Invalidation

- Removes cached objects from Edge Locations

### Key Points
- First 1,000 paths/month are free
- Useful for urgent updates

### Better Approach
- Use **file versioning**
  - Example: `image_v2.jpg`
- Avoids invalidation costs and delays

---

## Price Classes

- Control CDN cost by limiting Edge Locations

### Options
- Price Class All → Full global coverage
- Price Class 200 → Most regions
- Price Class 100 → Cheapest (limited regions)

---

## Global Accelerator vs CloudFront

| Feature            | CloudFront                         | Global Accelerator                     |
|------------------|----------------------------------|--------------------------------------|
| Purpose          | CDN (cache & deliver content)     | Improve global routing performance   |
| Protocol         | HTTP / HTTPS                      | TCP, UDP, HTTP                       |
| Caching          | ✅ Yes                            | ❌ No                                |
| IP Address       | Dynamic CDN IPs                   | 2 static Anycast IPs                 |
| Best Use Case    | Static/dynamic content delivery   | APIs, gaming, IoT, real-time apps    |

---

## Key Exam Traps

- S3 Website Endpoint = **Custom Origin** (not S3 origin)
- OAC only works with **S3 bucket origin**, not website endpoint
- Use **versioning over invalidation**
- CloudFront = caching
- Global Accelerator = no caching, better routing

---

## Key Summary

- CloudFront = CDN + caching + global performance
- OAC = secure private S3 access
- Geo Restriction = country-level control
- Invalidation = manual cache clearing (costly)
- Global Accelerator = fast routing for non-cacheable traffic