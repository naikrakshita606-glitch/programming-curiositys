# What Happens When You Open Google?

Opening a website involves a chain of systems. The exact servers and network routes can vary from one visit to the next.

## When you enter `google.com`, how does your computer find another computer somewhere in the world?

The browser checks cached information and usually asks a DNS resolver to find an IP address for the domain. It opens a network connection to an address and port, possibly through a nearby content delivery network or other intermediary. With HTTPS, the browser and server establish TLS protection and the browser checks the server certificate. The browser sends an HTTP request; routers forward packets across networks, and the server returns a response that the browser renders. See [DNS](../04-internet/dns.md), [IP addresses](../04-internet/ip.md), [HTTP](../04-internet/http.md), and [HTTPS](../04-internet/https.md).

## When you upload a photo to Instagram, where does it go?

The app sends the photo, often in chunks or as a multipart upload, to a service over an encrypted connection. The service authenticates the account, checks the request, and stores the media in a storage system. It may process the image into different sizes or formats and distribute copies through caches or a content delivery network. Metadata and permissions may be stored separately in a database. The exact implementation is proprietary and can change. See [APIs](../05-apis/), [databases](../06-databases/), [cloud services](../08-cloud-and-deployment/cloud.md), and [servers](../08-cloud-and-deployment/server.md).

## How can millions of people use the same application at the same time?

They do not all use one program on one computer. A service can run multiple instances behind load balancers, distribute static content through caches, queue work that can happen later, and partition data across storage systems. Teams monitor bottlenecks and failures, then add or optimize capacity. Scaling introduces coordination and consistency challenges, so architecture depends on traffic and product needs. See [scaling](../08-cloud-and-deployment/scaling.md).

## If the Internet disappeared tomorrow, which parts of your application would still work?

Features that run entirely on a user's device and use locally stored data may continue to work. Features requiring remote APIs, cloud databases, authentication providers, or network-hosted files will be unavailable or limited. Offline-capable applications can queue changes and synchronize later, but they need conflict handling and clear user feedback. The boundary depends on what was cached and which local capabilities the app provides. See [APIs](../05-apis/), [servers](../08-cloud-and-deployment/server.md), and [cloud computing](../08-cloud-and-deployment/cloud.md).
