# Day 58 – Hands-on with S3 & Bucket Policies

Today I worked practically with Amazon S3 and focused on understanding how access control really works beyond just creating a bucket.

---

## Creating an S3 Bucket

I started by creating an S3 bucket and explored different configuration options like:
- Region selection (important for latency & cost)
- Enabling versioning to protect against accidental deletion
- Default encryption using SSE-S3

I realized that bucket naming is globally unique, which reflects how S3 is a global service.

---

## Understanding Bucket Policies

After creating the bucket, I focused on **bucket policies**, which are JSON-based access control rules applied at the bucket level.

I experimented with:
- Allowing public read access to specific objects
- Restricting access based on IP address
- Granting access to specific IAM users

This helped me understand that bucket policies are **resource-based policies**, unlike IAM policies which are identity-based.

---

## IAM vs Bucket Policy

I compared both approaches:

- **IAM Policy** → attached to users/roles  
- **Bucket Policy** → attached to the S3 bucket  

Key insight:
Even if IAM allows access, a bucket policy can still deny it. **Explicit deny always wins.**

---

## Public Access Block Settings

I explored the "Block Public Access" feature and learned:
- It overrides bucket policies if enabled
- It’s a safety layer to prevent accidental exposure

This is critical in real-world scenarios where misconfigured policies can leak data.

---

## Object-Level Permissions

I also tested uploading objects and:
- Setting ACLs (Access Control Lists)
- Making objects public vs private

Then I learned that:
> ACLs are mostly legacy and AWS recommends using bucket policies instead.

---

## Key Learnings

- S3 security is a combination of:
  - IAM Policies
  - Bucket Policies
  - ACLs (less preferred)
  - Block Public Access

- Always follow **least privilege principle**
- Always double-check public access settings

---

## Final Thought

Today made it clear that S3 is simple on the surface but powerful and complex when it comes to **security and access control**. Misconfiguration can easily lead to data exposure, so understanding policies deeply is essential.