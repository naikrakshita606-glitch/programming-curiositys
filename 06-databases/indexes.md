# Database Indexes

An index is an auxiliary data structure that helps a database find rows without scanning every row. It speeds selected reads at the cost of storage and work when indexed data changes.

## Curiosity questions and answers

### 69. Why do we need indexes?

Without a suitable index, a database may inspect many or all rows to answer a query. An index can locate matching rows faster, much like an index in a book. Indexes should match real query patterns: too many indexes consume disk and memory and can slow inserts, updates, and deletes.
