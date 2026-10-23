# SQL Databases

SQL databases organize related data into tables and provide a language for querying and changing it. Relational database systems add constraints and transaction mechanisms to help keep data consistent.

## Curiosity questions and answers

### 63. What happens when you click “Save”?

The application validates the data and sends it to a backend, often through an API. The backend checks permissions and rules, then issues a database command inside a transaction. The database may validate constraints and write changes to durable storage or a log before confirming success. The application then reports the result; a button click alone does not guarantee data was saved.

### 65. What is a table?

A table is a named collection of rows with defined columns in a relational database. It represents a kind of entity or relationship, such as customers or orders. Constraints can specify which values are allowed and how tables relate.

### 66. What is a row?

A row is one record in a table, containing a value for each applicable column. For example, a customer row might hold an ID, name, and email. A primary key can distinguish it from other rows.

### 67. What is a column?

A column is a named attribute shared by rows, usually with a defined data type and optional constraints. An `email` column, for instance, stores email-related values. Choosing appropriate types and constraints helps prevent invalid data.

### 68. Why do we need primary keys?

A primary key uniquely identifies each row so applications and related tables can refer to the correct record. It prevents duplicate identifiers and supports relationships through foreign keys. Keys may be generated numbers, UUIDs, or meaningful natural values; the choice depends on data and system requirements.
