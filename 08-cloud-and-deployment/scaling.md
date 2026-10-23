# Scaling Applications

Scaling means adjusting a system's capacity as demand changes. Teams measure bottlenecks and choose approaches such as optimizing code, adding machines, caching, queues, or partitioning data.

## Curiosity questions and answers

### 92. What happens when 1 user uses your application?

The user's device runs client code and sends requests to the application service. The service performs its logic, may access a database or other services, and sends results back. Even a single user depends on networking, deployment, error handling, and data storage.

### 93. What changes when 1 million users use it?

Request volume, concurrency, traffic, data size, and failure probability all grow. A system may need load balancing, multiple application instances, caching, queues, database capacity, observability, and careful capacity planning. The exact changes depend on usage patterns: one million occasional visitors differ from one million simultaneous active users.

### 94. Why can’t we simply buy one huge computer?

A single machine has finite CPU, memory, storage, and network capacity, and it is a single point of failure. Large machines can be expensive and may not scale smoothly. Distributed systems spread work across machines, but introduce network latency, coordination, and partial failures, so the right design balances cost, complexity, reliability, and demand.

### 99. How does Netflix/YouTube/Instagram handle millions of users?

Large services use many layers: geographically distributed infrastructure, load balancing, caching, storage systems, queues, monitoring, and specialized services. Video services deliver much of their data through content delivery networks close to viewers. Exact architectures change and are proprietary; the general lesson is to partition work, remove bottlenecks, and plan for failures rather than depend on one server.

### 100. If you had to build WhatsApp from scratch, what would you need?

At a minimum: clients, identity and authentication, APIs, message storage, real-time delivery, offline queues, notifications, media storage, encryption, contact and group management, abuse controls, and reliable deployment. You would also need a protocol and data model, backups, monitoring, scaling, privacy policies, and operational support. A learning prototype can start much smaller, but a production service must address security, reliability, and high concurrency.
