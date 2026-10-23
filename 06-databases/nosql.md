# NoSQL Databases

“NoSQL” covers several database models that do not primarily use the traditional relational-table model, including document, key-value, wide-column, and graph databases. Each has different query and consistency capabilities.

## Curiosity questions and answers

### 61. Why can’t we simply store everything in Python variables?

Variables usually exist only while a process is running. They are not inherently durable, shared between application instances, or queryable after a restart. A database provides persistent storage, structured queries, controlled concurrent access, and backup and recovery features.

### 62. Why do applications need databases?

Applications use databases to persist, retrieve, and update data reliably across sessions and processes. Databases can enforce rules, index searches, coordinate concurrent changes, and recover data after failures. The right data store depends on access patterns, scale, consistency needs, and operational constraints.

### 70. What is the difference between SQL and NoSQL?

SQL databases are typically relational, with tables and a standardized query language called SQL; they often support strong transactional guarantees. NoSQL refers to varied non-relational models, frequently chosen for particular data shapes or distribution needs. The distinction is not absolute: modern relational systems support flexible data, and NoSQL systems can provide transactions. Choose based on requirements, not the label alone.
