# Phase 3: Servers & Scaling

## 1. Server

A server is a machine or application that receives requests, processes them, and sends responses.

---

## 2. Instance

An instance is a running copy of an application or server.


### Why?

More instances can handle more users.

### Remember

> Instance = Running copy of an application.

---

## 3. Vertical Scaling

Increasing the power of an existing server.

---

## 4. Horizontal Scaling


Adding more servers instead of increasing the size of one server.

---

## 5. Load Balancer

A load balancer distributes incoming traffic across multiple servers.

---

## 6. Reverse Proxy

A reverse proxy sits between users and servers and forwards requests to the correct backend server.

Nginx was acting as a reverse proxy.

### Responsibilities

- Forward requests
- Security
- SSL handling
- Routing

### Remember

> Reverse Proxy = Middleman in front of servers.

---

## Load Balancer vs Reverse Proxy

```text
Load Balancer
= Distributes traffic

Reverse Proxy
= Receives and forwards traffic
```

A tool like Nginx can often do both jobs.

---

## 7. High Availability (HA)

Designing a system so it remains available even when failures occur.

---

## 8. Failover

Automatically switching to another server/system when the primary one fails.

---


### Real Project Mapping

```text
Backend API          → Server
Multiple Pods        → Instances
Nginx                → Reverse Proxy
Ingress              → Reverse Proxy + Routing
Multiple Replicas    → Horizontal Scaling
Multiple Pods Running→ High Availability
```