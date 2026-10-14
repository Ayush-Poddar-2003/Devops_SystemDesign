# Phase 1: System Design Basics

## 1. System Design

Process of planning how different components of an application work together.

```text
Angular UI
    ↓
Backend API
    ↓
Database
```

This complete flow is a system.


> System Design = Blueprint of an application.

---

## 2. Scalability

Ability of a system to handle increasing users or workload without major performance issues.


> Scalability = Ability to handle more load.

---

## 3. Availability

How often a system is up and accessible to users.


> Is the service reachable?

> Availability = System uptime.

---

## 4. Reliability

Ability of a system to consistently perform correctly.

### Example

```text
User saves data 100 times
Data saves successfully 100 times
```
> Can users trust the system?

---

## 5. Performance
How efficiently a system completes its work.

- Speed
- Responsiveness
- Resource usage


> How well is the system performing?


---

## 6. Latency

Time taken for a request to travel from sender to receiver and return a response.

> How long does one request take?

> Latency = Waiting time.

---

## 7. Throughput

Amount of work a system can complete in a given time.


```text
Latency   = Time for one request
Throughput = Number of requests handled
```

---

## 8. Bottleneck

Slowest component that limits the performance of the entire system.

### Example

```text
Frontend  ✅ Fast
API       ✅ Fast
Database  ❌ Slow
```

Database becomes the bottleneck.

---

## 9. Single Point of Failure (SPOF)

A component whose failure can cause the entire system to stop working.

---

# Quick Revision

```text
System Design
= Application blueprint

Scalability
= Ability to handle growth

Availability
= System uptime

Reliability
= Consistent correctness

Performance
= Overall efficiency

Latency
= Time for one request

Throughput
= Work handled per unit time

Bottleneck
= Slowest component

Single Point of Failure (SPOF)
= One component whose failure can stop the system
```