# Requests and Responses

Clients and servers exchange requests and responses to ask for information or trigger an operation. A useful API defines the message format, response meanings, error behavior, and timing expectations.

## Curiosity questions and answers

### 54. What is a request?

A request is a message asking a service to perform an operation or provide a resource. In HTTP it includes a method, target URL, headers, and sometimes a body. Requests can fail because of invalid input, missing permissions, network problems, or service errors.

### 55. What is a response?

A response is the server's message back to the client. An HTTP response includes a status code, headers, and often a body. The status code communicates broad outcomes, while the body may contain data or an error explanation. Clients should handle unsuccessful responses and malformed data rather than assuming every request succeeds.

### 56. Why do APIs commonly use JSON?

JSON is a text-based format supported by most programming languages and easy to inspect, transmit, and parse. It represents objects, arrays, strings, numbers, booleans, and null. It is not always the best choice: binary formats can be smaller or faster, and JSON's data model does not directly represent every type.

### 59. What happens if an API takes 10 seconds to respond?

The client waits until the response arrives or its timeout expires. The delay may make the interface feel unresponsive and can tie up resources. Well-designed clients show progress, use reasonable timeouts, and may retry only when safe; APIs should measure latency and avoid duplicate side effects if clients retry.

### 60. What happens if the API server is completely down?

Requests may time out, fail to connect, or receive an error from an intermediary. The client should communicate the failure and preserve work where appropriate. Operators may use monitoring, redundancy, health checks, and recovery procedures, but retries need limits and backoff to avoid worsening an outage.
