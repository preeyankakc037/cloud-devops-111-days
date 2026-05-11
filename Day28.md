# Day28 of Learning for change 
#111DaysOfLearningForChange

Today I studied about Amazon EFS(Elastic File System)

![alt text](image-31.png)

# **Amazon EFS – Elastic File System**

**Throughput Modes**

Bursting:
* Throughput scales with storage size. For example, 1 TB storage provides baseline 50 MiB/s throughput with bursts to 100 MiB/s.
* Used when throughput needs track storage size with occasional spikes.


**Provisioned:**
* Allows setting a fixed throughput level independent of storage size.
* Good for workloads with predictable, steady throughput needs (e.g., large media processing pipelines).

**Elastic (recommended):**
* Automatically scales throughput up or down based on workload demands.
* Supports up to several GiB/s (up to 3 GiB/s reads, 1 GiB/s writes).
Best for unpredictable or spiky workloads.



# **Amazon EFS – Storage Tiers (Lifecycle management)**

Amazon EFS provides multiple storage tiers for cost optimization based on access patterns:

* Standard: For frequently accessed files, offering multi-AZ durability, suitable for production workloads.
* Infrequent Access (EFS-IA): Less frequently accessed files, lower storage cost but with retrieval fees.
* Archive: For rarely accessed data (a few times per year), roughly 50% cheaper than IA.
* Lifecycle management lets you automate transitions between these tiers based on file age or last access:

Optionally, files accessed in IA or Archive can be moved back to Standard to improve latency.

