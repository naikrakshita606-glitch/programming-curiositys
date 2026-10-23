# Servers

A server is a computer program that provides a service to clients; the computer running it is also commonly called a server. Servers may run in a data center, at a company, or on a cloud provider's infrastructure.

## Curiosity questions and answers

### 91. Where does your application actually run after deployment?

It runs on infrastructure selected for the deployment: physical machines, virtual machines, containers, serverless platforms, or a combination. Web applications may also include code running in users' browsers. DNS and routing direct users to the deployed service, while databases and file storage may run separately.

### 95. What is a server?

A server is software that listens for requests and responds to clients, such as a web server returning pages or an application server handling business logic. It runs on a host computer and uses operating-system and network resources. A single machine can run multiple server programs, and one service can span many machines.

### 98. What happens when a server crashes?

Clients may see connection failures or timeouts. A process supervisor or platform may restart it, and load balancers may route traffic to healthy instances. Restarting does not repair the underlying cause, and in-progress work may be lost. Redundant instances, health checks, persistent storage, and recovery procedures reduce downtime and data loss.
