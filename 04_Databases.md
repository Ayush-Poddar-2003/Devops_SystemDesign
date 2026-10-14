# Phase 4: Databases

## 1. SQL vs NoSQL

### SQL

SQL databases store data in tables with rows and columns.

### Examples

```text
MySQL
PostgreSQL
SQL Server
Oracle
```


### Characteristics

- Structured data
- Fixed schema
- Supports joins
- Strong consistency

---

### NoSQL

NoSQL databases store data in flexible formats.

### Examples

```text
MongoDB
Cassandra
Redis
DynamoDB
```


### Characteristics

- Flexible schema
- Easy to scale
- Suitable for large data volumes

---


## 2. Relational Database

A database where tables are related to each other.

---

## 3. Primary Key


A column that uniquely identifies each row.

---

## 4. Foreign Key

A column that references the primary key of another table.

---

## 5. Index


An index helps the database find data faster.

### Without Index

```text
Database checks
Row 1
Row 2
Row 3
...
Row 1,000,000
```

### With Index

```text
Database jumps directly to data
```
---

## 6. Query


A query is a request sent to a database.

---

## 7. Transaction

A transaction is a group of database operations treated as a single unit.

### Example

Bank Transfer

```text
Deduct ₹1000 from Account A
Add ₹1000 to Account B
```

Both operations must succeed together.

### Incorrect Situation

```text
Money deducted
Money not added
```

Problem!

### Correct Situation

```text
Both succeed
OR
Both fail
```


> Transaction = All or nothing.

---

## 8. ACID

ACID properties ensure reliable transactions.

---

### A - Atomicity

Either all operations happen or none happen.

```text
Success ✅
or
Rollback ✅
```


---

### C - Consistency

Database remains valid before and after transaction.

---

### I - Isolation

Multiple transactions do not interfere with each other.

---

### D - Durability

Once committed, data remains saved even after crashes.

---

## 9. Connection Pool

A collection of reusable database connections.

### Without Connection Pool

Every request:

```text
Create Connection
Use Connection
Close Connection
```

Very slow.

### With Connection Pool

```text
Reuse existing connections
```

Much faster.

---

# Quick Revision

```text
SQL
= Table-based database

NoSQL
= Flexible database

Relational Database
= Related tables

Primary Key
= Unique identifier

Foreign Key
= Reference to another table

Index
= Fast lookup

Query
= Database command

Transaction
= Group of operations

ACID
= Rules for reliable transactions

Connection Pool
= Reusable DB connections
```

