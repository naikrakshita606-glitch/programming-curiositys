# Encryption and CORS

Encryption uses keys to transform readable data into ciphertext that should be unreadable to parties without the necessary key. CORS, by contrast, is a browser policy controlling certain cross-origin web requests; it is not encryption or authentication.

## Curiosity questions and answers

### 74. What is encryption?

Encryption transforms plaintext into ciphertext using an algorithm and key so that only someone with the appropriate decryption key can recover the data. Symmetric encryption uses the same secret key to encrypt and decrypt; public-key cryptography uses a related key pair. HTTPS uses TLS to negotiate secure communication. Key protection and correct implementation are essential.

### 77. What is CORS?

Cross-Origin Resource Sharing (CORS) is a browser-enforced mechanism that lets a server specify which web origins may read certain cross-origin responses. The browser may send a preflight request before some requests. CORS is not a firewall and does not stop non-browser clients; API servers still need authentication, authorization, and input validation.
