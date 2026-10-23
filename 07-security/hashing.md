# Hashing

A cryptographic hash function maps input data to a fixed-size digest. Properly chosen cryptographic hashes are designed to make it impractical to recover the input or find a different input with the same digest.

## Curiosity questions and answers

### 73. Why shouldn’t passwords be stored as plain text?

If a database is exposed, plain-text passwords immediately reveal users' credentials, which may also be reused on other services. Instead, store a unique salt and a slow, purpose-built password hash. On login, hash the submitted password using the stored parameters and compare safely. A fast general-purpose hash like SHA-256 alone is not appropriate for password storage.

### 75. What is hashing?

Hashing computes a fixed-length digest from data. Cryptographic hashes support integrity checks and other security uses, but hashing is one-way by design and is not encryption. Password storage uses specialized slow hash functions to make large-scale guessing more expensive.
