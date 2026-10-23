# What Is an API?

An application programming interface (API) is a defined way for software components to request functionality or exchange data. A web API commonly uses HTTP, but APIs also exist in libraries, operating systems, and hardware.

## Curiosity questions and answers

### 51. What exactly is an API?

An API is a contract: it describes available operations, expected inputs, outputs, and errors. For a web API, a client might request a user's profile and receive structured data. The server can change its internal implementation while preserving the public contract, subject to compatibility rules.

### 52. Why can’t two applications simply access each other’s variables?

Applications commonly run in separate processes or on separate computers, with distinct memory spaces and security boundaries. Directly sharing memory across those boundaries would be unsafe and often impossible over a network. An API provides an explicit, controlled protocol for exchanging data without exposing internal state.

### 53. What happens when a React application calls a Node/Python API?

The browser's JavaScript code constructs an HTTP request, often with a method, URL, headers, and JSON body. It sends the request over the network to the API service. The server validates it, runs application logic, may read or write a database, and returns a status code and response body. The browser parses the result and updates the interface. CORS rules may affect browser access across origins; they are not a replacement for server authentication or authorization.
