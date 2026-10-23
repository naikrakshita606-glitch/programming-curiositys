# Authorization

Authorization determines what an authenticated identity is allowed to do. It should be checked by the server for each protected operation, using the requested resource and the user's current permissions.

## Curiosity questions and answers

### 76. What happens if someone changes an API request?

The server receives whatever request reaches it and must treat client-supplied data as untrusted. It validates inputs, checks authentication and authorization, and rejects operations the user may not perform. HTTPS helps prevent interception or modification in transit, but cannot stop a user from editing their own client request.

### 78. How does a server know whether you are authorized?

The server identifies the caller from a session or token, loads or verifies the relevant identity and permissions, and checks whether the requested action is allowed on that particular resource. Authorization must be enforced on the server, not inferred from hidden buttons or client-side state. Permissions can change, so sensitive actions may require fresh checks.

### 80. How can one careless line of code expose millions of users?

A small mistake can disable an access check, expose a database query, log credentials, or make private data available through a public endpoint. If the affected code serves a large system, one flaw can affect many accounts. Least privilege, secure defaults, code review, automated tests, monitoring, and rapid incident response reduce the chance and impact.
