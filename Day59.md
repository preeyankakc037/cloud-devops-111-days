# Day 59 – VPC Deep Dive & Networking Behavior

Today I focused on understanding how networking actually works inside AWS by going deeper into VPC components and traffic flow instead of just memorizing definitions.

---

## Building a Custom VPC

I created a custom VPC instead of using the default one to understand everything from scratch:
- Defined my own CIDR block
- Created public and private subnets across multiple AZs
- Attached an Internet Gateway for public access

This helped me visualize how AWS networking is fully customizable and isolated.

---

## Public vs Private Subnets (Real Understanding)

I used to think public/private was just a label, but today I understood:

- A **public subnet** = has a route to Internet Gateway
- A **private subnet** = no direct route to Internet

So it's actually the **route table** that decides everything, not the subnet itself.

---

## NAT Gateway Practical Use

I set up a NAT Gateway in a public subnet and routed private subnet traffic through it.

Key learning:
- Instances in private subnet can access the internet (outbound only)
- But they cannot be accessed from the internet (inbound blocked)

This is critical for:
- App servers
- Databases
- Internal services

---

## Route Tables & Traffic Flow

I experimented with route tables and realized:

- Every subnet must be associated with a route table
- Routes define where traffic goes (IGW, NAT, local, etc.)

Example:
- `0.0.0.0/0 → IGW` = public access
- `0.0.0.0/0 → NAT` = private outbound

Understanding this made networking much clearer.

---

## Security Groups vs NACLs (Hands-on Insight)

Instead of just theory, I tested both:

### Security Groups
- Stateful
- Allow rules only
- Applied at instance level

### NACLs
- Stateless
- Allow + Deny rules
- Applied at subnet level

Big realization:
> Security Groups are the primary defense, NACLs are an optional extra layer.

---

## Bastion Host Concept

I launched a bastion host in a public subnet and used it to SSH into a private instance.

This helped me understand:
- How to securely access private resources
- Why we don’t expose private instances directly

---

## Key Learnings

- Networking in AWS is **route-driven**
- NAT Gateway is essential for private subnet internet access
- Security Groups handle most real-world security needs
- Proper VPC design = foundation of secure architecture

---

## Final Thought

Today was a big shift from theory to actual understanding. Instead of memorizing components, I now understand how traffic flows inside AWS, which is crucial for designing real-world architectures.