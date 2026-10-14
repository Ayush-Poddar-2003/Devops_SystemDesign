# Phase 6: Caching

## Why Caching?

Fetching data from a database every time can be slow  
If 10,000 users request the same data repeatedly, the database gets overloaded.

Solution :-  
Store frequently used data in a cache.

> Cache = Fast temporary storage.

---

## 1. Cache

A cache is a temporary storage layer used to quickly access frequently requested data.

> Cache stores frequently used data closer to the application.

---

## 2. Cache Hit
Requested data is found in the cache.

---

## 3. Cache Miss

Requested data is not found in cache.  

---

## 4. TTL (Time To Live)
TTL defines how long data remains in cache before it expires.

Why?  
To avoid serving outdated information.

---

## 5. Cache Invalidation
Removing or updating outdated cache data.

---

## 6. Redis

Redis is one of the most popular in-memory caching systems.

### Characteristics

```text
Very Fast
In-Memory
Used for Caching
```

### Common Usage

```text
User Sessions
Frequently Accessed Data
API Responses
```

---

## 7. CDN (Content Delivery Network)

A CDN stores copies of static files closer to users around the world.

### Example Files

```text
Images
Videos
CSS
JavaScript
```

### Without CDN

```text
India User
      ↓
US Server
```

Longer response time.

### With CDN

```text
India User
      ↓
Nearby CDN Server
```

Faster response.

### Remember

> CDN = Cache for static content distributed globally.

---

# Cache Flow Example

```text
User
 ↓
Angular App
 ↓
Backend API
 ↓
Cache

Cache Hit?
 ↓       ↓
Yes      No

Return   Database
Data       ↓
           Cache Updated
             ↓
          Return Data
```

---

# Quick Revision

```text
Cache
= Fast temporary storage

Cache Hit
= Data found in cache

Cache Miss
= Data not found in cache

TTL
= Cache expiry time

Cache Invalidation
= Remove/update stale data

Redis
= In-memory caching system

CDN
= Global cache for static content
```

### Senior Developer Translation

If someone says:

```text
"High cache hit rate."
```

It means:

> Most requests are being served from cache instead of the database.

If someone says:

```text
"Invalidate the cache."
```

It means:

> Remove old cached data so fresh data can be loaded.

If someone says:

```text
"Let's put Redis in front of the database."
```

It means:

> Use Redis to serve frequently requested data faster and reduce database load.