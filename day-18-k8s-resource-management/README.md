# Kubernetes Resource Management (CPU & Memory)

This project demonstrates how Kubernetes manages
**CPU and Memory requests & limits** for containers.

---

## 🚀 What You Will Learn

- Difference between requests vs limits
- How Kubernetes schedules pods
- How CPU throttling works
- What happens when memory limit exceeds
- Why resource management is critical in production

---

## 🧱 Architecture Concept

Pod → Container → Resource Requests/Limits  
Scheduler → Node selection based on requests

---

## 🛠 Prerequisites

- Kubernetes cluster (Minikube / Kind)
- kubectl installed

---

## ⚙️ Setup Steps

### 1️⃣ Start Cluster
```
minikube start
```
### 2️⃣ Deploy Application
```
kubectl apply -f resources.yaml
```
### 3️⃣ Verify Deployment
```
kubectl get pods
kubectl describe pod <pod-name>
```
---
## 🔍 Inspect Resource Allocation
```
kubectl describe pod <pod-name> | grep -A10 Limits
```

Check node usage:
```
kubectl top pod
kubectl top node
```
---
## 🧪 Testing Scenarios
**🔹 CPU Throttling**

- Pod will not exceed 500m CPU

- Kubernetes throttles CPU usage

**🔹 Memory Limit**

- If memory exceeds 256Mi

- Pod gets **OOMKilled**

- Pod restarts automatically
---
## 🧠 Interview Talking Points

- Why requests are used by scheduler

- Why limits protect cluster stability

- CPU is compressible, Memory is not

- What happens if limits are not set

- Relation with HPA & cluster autoscaling


---
## 📌 Best Practices

- Always define requests

- Set reasonable limits

- Avoid unlimited memory

- Tune based on monitoring data
