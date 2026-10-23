# Authentication

Authentication is the process of verifying an identity or account claim. After authentication, an application may create a session or issue a token so later requests can be associated with that login.

## Curiosity questions and answers

### 71. How does a website know who you are after login?

The server verifies the sign-in credentials and typically creates a session. It sends the browser a session cookie or another credential, which is presented on later requests. The server checks it to find the authenticated account. Secure session design includes expiration, protection against theft, and invalidation at logout or when needed.

### 72. Where is your password stored?

A well-designed service stores a salted password hash, not the original password. The hash is produced by a password-hashing function designed to be expensive to guess, such as Argon2id, scrypt, or bcrypt with suitable parameters. It is stored in a protected server-side database; passwords should never be recoverable from that record.

### 79. What is a token?

A token is a piece of data that represents a credential or authorization claim. A bearer token grants whoever possesses it the associated access, so it must be protected like a password. Tokens may be opaque references stored by the server or signed structured tokens; signing does not automatically encrypt their contents.
