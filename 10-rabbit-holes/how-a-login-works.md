# How a Login Works

Login is a sequence of client, network, server, and database operations. Details differ between services, but passwords should not be sent or stored as plain text.

## When I click Login, how does my password travel to the server and come back as “Login successful”?

The app sends credentials to a login endpoint over HTTPS, which protects them while in transit. The server validates the request, finds the account, and compares a password hash computed with the account's stored salt and password-hashing settings. If verification succeeds, it creates a session or issues a token and returns a response. The client stores the session credential using an appropriate protected mechanism and includes it on later requests. The server verifies it and checks authorization for each protected operation. HTTPS protects transit; it does not protect a compromised device or a breached server. See [authentication](../07-security/authentication.md), [authorization](../07-security/authorization.md), [hashing](../07-security/hashing.md), [encryption](../07-security/encryption.md), and [API requests and responses](../05-apis/request-response.md).

## What if someone changes an API request?

The client is under the user's control, so the server must assume requests can be modified. It validates all input and checks permissions against the actual account and resource before making changes. TLS prevents many network attackers from silently changing traffic in transit, but it does not stop the user from changing their own request before sending it. See [authorization](../07-security/authorization.md).

## What happens if two users try to modify the same database record at exactly the same time?

The database applies its concurrency rules: one operation may wait, both may succeed in a defined order, or one may fail with a conflict. Transactions help group changes, and optimistic version checks can detect that a record changed since it was read. The application must decide whether to retry, merge, or ask a user to resolve a conflict. See [database transactions](../06-databases/transactions.md).
