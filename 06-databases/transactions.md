# Database Transactions

A transaction groups database operations into a unit with defined commit and failure behavior. It helps applications make related changes consistently, especially when multiple users or processes work with the same data.

## Curiosity questions and answers

### 64. Where does the data physically go?

The database writes data to files managed by its storage engine, usually on persistent storage such as SSDs, often using a transaction log or journal. The operating system and hardware control the physical device, and databases may also keep frequently used data in RAM. Backups and replicas can store additional copies elsewhere; the exact layout depends on the database and deployment.

### What happens if two users modify the same record at the same time?

The database coordinates concurrent operations using mechanisms such as locks, multiversion concurrency control, and transaction isolation. Depending on the design, one update may wait, conflict, or be rejected; careless application logic can still overwrite a newer value. Transactions, constraints, version checks, and conflict-handling policies help preserve the intended result.
