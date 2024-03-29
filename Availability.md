//Source: https://www.geeksforgeeks.org/availability-in-system-design/
          https://www.enjoyalgorithms.com/blog/availability-system-design-concept/
Definition
----------
In system design, availability refers to the proportion of time that a system or service is operational and accessible for use. It is a critical aspect of designing reliable and resilient systems, especially in the context of online services, websites, cloud-based applications, and other mission-critical systems.

How is availability measured?
-----------------------------
Availability is usually measured as a percentage and is often expressed in terms of “uptime” versus “downtime” over a given period. For instance, a system with 99% availability means it is expected to be operational and accessible 99% of the time, while the remaining 1% represents the allowable downtime.

How do we achieve high availability?
-----------------------------------
>Redundancy: Employ redundant components or servers to ensure that another can take over seamlessly if one fails. This can include redundancy at different levels, such as hardware, networking, and data centers.
>Load balancing: Distributing incoming requests across multiple servers or resources to prevent overload on any single component and improve overall system performance and fault tolerance.
>Failover mechanisms: Implementing automated processes to detect failures and switch to redundant systems without manual intervention.
>Disaster Recovery (DR): Having a comprehensive plan in place to recover the system in case of a catastrophic event that affects the primary infrastructure.
>Monitoring and Alerting: Implementing robust monitoring systems that can detect issues in real-time and notify administrators to take appropriate action promptly.
>Performance optimization: Ensuring that the system is designed and tuned to handle the expected load efficiently, reducing the risk of bottlenecks and failures.
>Scalability: Designing the system to scale easily by adding more resources when needed to accommodate increased demand.
