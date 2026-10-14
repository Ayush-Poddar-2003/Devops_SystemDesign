# Phase 2: Application Architecture

## 1. Client

Application that sends requests to a server and displays data to users.

---

## 2. Server

A server receives requests, processes them, and returns responses.

---

## 5. API

API (Application Programming Interface) is a way for applications to communicate with each other.

---

## 6. REST

Popular style for designing APIs using HTTP methods.



## 7. HTTP

HTTP (HyperText Transfer Protocol) is the protocol used for communication between client and server.

---

## 8. HTTPS

HTTPS is the secure version of HTTP.

---

## 9. Stateless

A stateless server does not remember previous requests.

### Example

Request 1:

```text
GET /profile
```

Request 2:

```text
GET /vehicles
```

Server treats both requests independently.

### Remember

> Stateless = No memory of previous requests.

---

## 10. Stateful

A stateful server remembers information between requests.

### Example

```text
Online Game
Chat Session
Video Call Session
```

Server maintains session information.

### Remember

> Stateful = Remembers previous interactions.

---

## Stateless vs Stateful

```text
Stateless
- No memory
- Easier to scale
- Common in REST APIs

Stateful
- Maintains session
- More complex scaling
- Used in live sessions
```

---

## 11. Monolith

A monolith is an application where all modules exist in a single codebase and deployment unit.

### Advantages

- Easy to start
- Simple deployment

### Disadvantages

- Harder to scale
- Harder to maintain as application grows

---

## 12. Microservices

Microservices split a large application into multiple smaller services.

Each service can run independently.

---

# Quick Revision

```text
Client
= Requests data

Server
= Provides data

Frontend
= User Interface

Backend
= Business Logic

API
= Communication bridge

REST
= Standard API style

HTTP
= Communication protocol

HTTPS
= Secure HTTP

Stateless
= No memory of previous requests

Stateful
= Remembers previous requests

Monolith
= Single application

Microservices
= Multiple independent services
```

# Most Important Terms

```text
1. Client
2. Server
3. Frontend
4. Backend
5. API
6. REST
7. HTTP / HTTPS
8. Microservices
```

### Real Project Mapping

```text
Angular App       → Frontend / Client
API Calls         → REST APIs
HTTPS URL         → Secure Communication
Java/.NET Service → Backend / Server
Vehicle APIs      → Microservices (in many 