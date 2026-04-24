Simple Routing

Simple routing sends all traffic to one single resource (like one server or one load balancer). There is no load balancing or failover—just a direct mapping from domain to resource. It is used when you have only one endpoint or don’t need advanced routing logic.

Weighted Routing

Weighted routing distributes traffic between multiple resources based on assigned percentages (like 70% to one server, 30% to another). It is used for A/B testing, gradual deployments, or load distribution across resources.

Failover Routing

Failover routing directs traffic to a primary resource, and if it becomes unhealthy, it automatically switches to a secondary (backup) resource. It uses health checks. It is used for high availability and disaster recovery.

Latency-Based Routing

Latency-based routing sends users to the resource with the lowest network latency (fastest response time). It is based on AWS region performance. It is used for improving user experience globally.

Geolocation Routing

Geolocation routing directs users based on their geographic location (country or continent). It is used when you want different content or restrictions based on user location (like legal compliance or localization).

Multi-Value Routing

Multi-value routing returns multiple healthy IP addresses to the client. It acts like basic load balancing but also performs health checks. It is used for simple load balancing without using ELB.

Geoproximity Routing

Geoproximity routing routes traffic based on distance between users and resources, and you can shift traffic using bias values. It is used when you want fine control over traffic distribution across regions.

IP-Based Routing

IP-based routing directs traffic based on the user’s IP address range. It is used for custom routing rules for specific networks, ISPs, or corporate users.