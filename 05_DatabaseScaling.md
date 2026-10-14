# Phase 5: Database Scaling

## Why Database Scaling?



As users increase, a single database may become slow.



```text
1,000 Users    ✅ Fast
100,000 Users  ✅ Okay
10,000,000 Users ❌ Slow
```

To handle more traffic, databases need scaling techniques.

---

## 1. Replication

Replication means keeping copies of the same database on multiple servers.


All databases contain the same data.

### Benefits

- Better availability
- Better performance
- Backup databases available

### Remember

> Replication = Multiple copies of the same database.

---

## 2. Primary / Replica


In replication, one database acts as the Primary and others act as Replicas.



Primary:

```text
Insert Data
Update Data
Delete Data
```

Replicas:

```text
Read Data
```


> Primary writes, replicas mostly read.

---

## 4. Database Partitioning

Splitting a large table into smaller pieces.

### Benefits

- Faster queries
- Easier maintenance

### Remember

> Partitioning = Divide a large table into smaller parts.

---

## 5. Database Sharding

Sharding means splitting data across multiple databases.



```text
Shard 1 → Users A-F
Shard 2 → Users G-M
Shard 3 → Users N-Z
```

---

### Sharding

```text
Different Data
Different Databases
```

Example:

```text
Shard1 → Users A-F

Shard2 → Users G-M

Shard3 → Users N-Z
```

### Quick Difference

```text
Replication
= Copy data

Sharding
= Divide data
```

---

## 6. Shard

Each individual database created after sharding.

Each stores part of the total data.

---

## 7. Shard Key

The field used to decide which shard should store data.

---

## 8. Hotspot

A hotspot occurs when one shard receives much more traffic than others.

> Hotspot = Uneven load distribution.

---

## 9. Replication Lag

The delay between Primary database updates and Replicas receiving those updates.

### Example

```text
Data Written
     ↓
Primary Updated Immediately

Replica Updated After 2 Seconds
```

### Issue

User may see:

```text
Latest Data in Primary ✅

Old Data in Replica ❌
```

---

# Quick Revision

```text
Replication
= Multiple copies of same database

Primary
= Handles writes

Replica
= Copy of primary

Read Replica
= Handles read operations

Partitioning
= Split large table

Sharding
= Split data across databases

Shard
= Single partitioned database

Shard Key
= Rule that decides shard

Hotspot
= One shard gets too much traffic

Replication Lag
= Delay between primary and replicas
```

# Most Important Terms

```text
1. Replication
2. Read Replica
3. Sharding
4. Shard
5. Shard Key
6. Hotspot
7. Replication Lag
```

# Real Project Understanding

```text
Performance Problem
        ↓
Replication
        ↓
More Read Capacity
```

```text
Database Too Large
        ↓
Sharding
        ↓
Multiple Databases
```

### Senior Developer Translation

If someone says:

```text
"We may need sharding."
```

They usually mean:

> One database is becoming too large, so let's split data across multiple databases.

If someone says:

```text
"Replication lag is causing stale data."
```

They mean:

> The replica database has not yet received the latest updates from the primary database.