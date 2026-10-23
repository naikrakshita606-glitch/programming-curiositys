# DNS

The Domain Name System (DNS) is a distributed naming system that helps applications find network addresses associated with domain names.

## Curiosity questions and answers

### 41. What happens when you type `google.com` into a browser?

The browser interprets the text as a destination, checks relevant cached information, and usually asks a DNS resolver for an address. It then connects to a server, negotiates HTTPS when appropriate, sends an HTTP request, and renders the returned page and resources. Search results and page content are separate from the name lookup.

### 43. What is DNS?

DNS is a hierarchy of servers and records that maps names such as `example.com` to information such as IP addresses. A device typically asks a recursive resolver, which can query other DNS servers and cache answers for a limited time. DNS makes human-friendly names practical, but by itself it does not prove that a destination is trustworthy or encrypt the web connection.
