# IP Addresses and Routing

Internet Protocol (IP) addresses identify network interfaces for packet delivery. Routers forward packets between networks; addresses and routes can change, so a domain name is often a more convenient way for people to select a service.

## Curiosity questions and answers

### 42. How does your computer find Google's server?

The browser first typically resolves the requested domain through DNS to one or more IP addresses. The device then sends packets through its local network and internet service provider; routers forward them toward the destination network. Large services may use load balancers, anycast, and geographically distributed infrastructure, so a resolved address need not point to one fixed physical machine.

### 44. What is an IP address?

An IP address is a numeric address used by Internet Protocol to deliver packets to a network interface. IPv4 and IPv6 are the main versions. An address identifies a network endpoint for routing purposes; it does not necessarily identify a person or a single permanent computer.

### 49. How does your request travel thousands of kilometres?

Data is split into packets and sent over links such as Wi-Fi, fiber, and undersea cables. Routers make forwarding decisions based on destination addresses, and packets can take different paths. Protocols such as TCP can provide ordered, reliable delivery above IP, while encryption protects application data in transit when HTTPS is used.
