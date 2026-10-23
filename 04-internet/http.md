# HTTP

HTTP is an application protocol for exchanging requests and responses. Browsers, servers, APIs, and other software use it to describe resources and actions.

## Curiosity questions and answers

### 45. Why do we need ports?

An IP address helps packets reach a host; a port number helps the host deliver a network connection to the correct service or process. For example, HTTPS commonly uses port 443. Ports are transport-layer identifiers, not physical connectors, and firewalls or network configurations may affect whether they are reachable.

### 46. What is HTTP?

Hypertext Transfer Protocol defines how clients and servers exchange messages, including methods, headers, status codes, and optional bodies. HTTP itself does not encrypt data; HTTPS is HTTP protected by TLS. HTTP is stateless at the protocol level, while applications can use cookies or tokens to maintain session context.

### 48. What happens when you click a button on a website?

The browser runs the page's event-handling code. Depending on the button, it may update the page locally or create an HTTP request to a server. The request travels over a network connection, the server processes it, and the browser handles the response—perhaps updating the page. Validation and permissions must be checked on the server too; browser-side checks alone are not security controls.

### 50. How does the server know where to send the response?

The transport connection records the client endpoint, including its address and port, so the server can send data back over that connection. The client may be behind a router performing address translation, but the connection state lets replies return correctly. At the application level, HTTP responses correspond to requests on that connection.
