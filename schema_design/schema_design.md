
# Schema Design Documentation

This document explains database schema design fundamentals, different types of databases, and best practices for designing scalable, maintainable data models for real-world products.

---

## 1. Types of Databases

Choosing the right database depends on the nature of the application, data structure, and access patterns.

### 1.1 Relational Databases (SQL)
Examples: PostgreSQL, MySQL, SQLite, Oracle

- Data is stored in tables (rows & columns)
- Strong schema enforcement
- Supports joins and transactions
- Ideal for structured data and complex queries

Use cases:
- Financial systems
- E-commerce applications
- Enterprise systems

---

### 1.2 NoSQL Databases
Examples: MongoDB, Redis, Cassandra, DynamoDB

#### a) Document Databases
- Store data as JSON-like documents
- Flexible schema

Use cases:
- Content management
- Rapidly evolving data structures

#### b) Key-Value Stores
- Simple key-value pairs
- Extremely fast

Use cases:
- Caching
- Session storage

#### c) Column Stores
- Optimized for analytical queries

Use cases:
- Data analytics
- Time-series data

---

### 1.3 Choosing the Right Database

| Requirement | Database Type |
|------------|---------------|
| Structured data | Relational |
| Frequent joins | Relational |
| Rapid schema changes | Document DB |
| High read/write speed | Key-Value |
| Analytics | Column store |

---

## 2. Schema Design Basics

### What is Schema Design?

Schema design defines:
- Tables
- Columns
- Data types
- Relationships between tables

A good schema ensures:
- Data consistency
- Performance
- Scalability

---

## 3. Normalization

Normalization reduces data redundancy and improves data integrity.

### 3.1 First Normal Form (1NF)
- No repeating groups
- Atomic values only

Bad:
```
users(id, name, phones)
phones = "123,456"
````

Good:

```text
user_phones(user_id, phone)
```

---

### 3.2 Second Normal Form (2NF)

* Must be in 1NF
* No partial dependency on composite keys

---

### 3.3 Third Normal Form (3NF)

* Must be in 2NF
* No transitive dependencies

Example:
Separate user and address tables instead of duplicating address fields.

---

### When NOT to Fully Normalize

* Performance-critical systems
* Reporting-heavy queries

In such cases, **controlled denormalization** is acceptable.

---

## 4. Primary Keys

### Types of Primary Keys

#### Auto-increment IDs

```sql
id SERIAL PRIMARY KEY
```

Simple and fast

Predictable

---

#### UUIDs

Universally Unique Identifiers

```sql
id UUID PRIMARY KEY DEFAULT gen_random_uuid()
```

Globally unique

Great for distributed systems

Larger size and slightly slower indexing

---

### When to Use UUIDs

* Multi-service architecture
* Data created across multiple systems
* Security reasons (non-guessable IDs)

---

## 5. Indexing

Indexes improve query performance by allowing fast lookups.

### Common Index Types

#### Single-column Index

```sql
CREATE INDEX idx_users_email ON users(email);
```

#### Composite Index

```sql
CREATE INDEX idx_orders_user_date ON orders(user_id, created_at);
```

---

### When to Use Indexes

* Columns used in `WHERE`, `JOIN`, `ORDER BY`

### When NOT to Overuse Indexes

* High write operations (indexes slow down inserts/updates)
* Columns with very low cardinality

---

## 6. Joins

Joins combine data from multiple tables.

### Common Join Types

```sql
SELECT *
FROM orders
INNER JOIN users ON orders.user_id = users.id;
```

| Join Type  | Description               |
| ---------- | ------------------------- |
| INNER JOIN | Only matching rows        |
| LEFT JOIN  | All left + matching right |
| RIGHT JOIN | All right + matching left |
| FULL JOIN  | All rows from both tables |

---

### Best Practices for Joins

* Index foreign keys
* Avoid unnecessary joins
* Prefer explicit join conditions

---

## 7. Backup and Restore

### Why Backups Matter

* Prevent data loss
* Disaster recovery
* Migration safety

---

### Backup (PostgreSQL example)

```bash
pg_dump mydb > mydb_backup.sql
```

### Restore

```bash
psql mydb < mydb_backup.sql
```

---

### Best Practices

* Automate backups
* Test restore regularly
* Store backups securely (offsite)

---

## 8. Copying Table Data

### Copy data between tables

```sql
INSERT INTO archived_users
SELECT * FROM users WHERE is_active = false;
```

---

### Copy structure only

```sql
CREATE TABLE new_users AS TABLE users WITH NO DATA;
```

---

### Export table data (CSV)

```sql
COPY users TO '/tmp/users.csv' CSV HEADER;
```

---

## 9. Foreign Keys & Relationships

```sql
ALTER TABLE orders
ADD CONSTRAINT fk_user
FOREIGN KEY (user_id) REFERENCES users(id);
```

Benefits:

* Data integrity
* Prevent orphan records


## Summary

A good schema design:

* Ensures data integrity
* Scales with the product
* Supports future changes
* Balances normalization and performance

Understanding schema design is critical for building reliable and scalable backend systems.

