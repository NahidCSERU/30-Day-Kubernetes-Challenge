# 🟢 Day 12 — Kubernetes Probes (Liveness, Readiness, Startup)

This project is part of the **Kubernetes 30 Days Learning Challenge** and focuses on  
**Day 12: Kubernetes Probes** — a critical concept for building **reliable and self-healing applications**.

Kubernetes probes help determine:
- When a container should be restarted
- When a Pod is ready to receive traffic
- When an application is still starting up

---

## 🎯 Project Objectives

- Understand **Liveness Probe**
- Understand **Readiness Probe**
- Understand **Startup Probe**
- Implement probes in a Kubernetes workload
- Learn how Kubernetes performs health checks in production

---

## 🧠 Probes Overview

### 🔹 Liveness Probe
Checks whether the application is still running properly.  
If the probe fails, Kubernetes **restarts the container**.

📌 Use case:
- Detect application deadlocks
- Recover from hung processes

---

### 🔹 Readiness Probe
Checks whether the application is ready to accept traffic.  
If the probe fails, Kubernetes **stops sending traffic** to the Pod (no restart).

📌 Use case:
- Wait for database connection
- Graceful traffic handling during startup or overload

---

### 🔹 Startup Probe
Checks whether the application has started successfully.  
Until this probe succeeds, Kubernetes **disables liveness and readiness checks**.

📌 Use case:
- Slow-starting applications (Java, Spring Boot, legacy apps)

---

## 📄 probes.yaml

This file demonstrates a Kubernetes Pod using **all three probes**:
- HTTP-based health checks
- Realistic timing values
- Production-style configuration

---

## 🚀 How to Apply

```
kubectl apply -f probes.yaml
```
## 🔍 Verification

Check Pod status:
```
kubectl get pods
kubectl describe pod probes-demo
```

Simulate failures and observe:

- Container restarts (liveness)

- Traffic removal (readiness)