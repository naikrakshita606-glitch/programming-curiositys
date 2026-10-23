# REST APIs

REST is an architectural style for networked systems, not a synonym for every HTTP API. RESTful designs typically treat information as resources and use a uniform interface, often HTTP methods and resource URLs.

## Curiosity questions and answers

### 57. What are HTTP methods?

HTTP methods describe the intended action for a request. `GET` retrieves a representation; `POST` submits data or asks the server to process an operation; `PUT` replaces a resource representation; `PATCH` applies a partial update; and `DELETE` requests removal. These meanings guide clients, servers, caches, and intermediaries, though the server must define its exact behavior.

### 58. Why do we have GET, POST, PUT, PATCH and DELETE?

Distinct methods make APIs easier to understand and enable consistent protocol behavior. `GET` is intended to be safe (not change server state), and `PUT` and `DELETE` are defined as idempotent: repeating the same request should have the same intended effect. `POST` is not generally idempotent, and `PATCH` idempotency depends on the operation. These properties help with retries and caching, but developers must implement them correctly.
