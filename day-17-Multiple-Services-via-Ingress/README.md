# Kubernetes Ingress — Multiple Services Routing

This project demonstrates how to route traffic to **multiple Kubernetes services**
using a **single NGINX Ingress Controller** with path-based routing.

---

## 🚀 What You Will Learn

- Single Ingress → Multiple Services
- Path-based routing using Ingress
- Real-world microservices traffic flow
- How frontend & backend are exposed together
- Production-style ingress configuration

---

## 🧱 Architecture Flow

User
 → Ingress Controller
   → /web → web-service → web pods
   → /api → api-service → api pods

---

## 🛠 Prerequisites

- Minikube / Kind cluster
- kubectl installed
- NGINX Ingress Controller enabled

---

## ⚙️ Setup Steps

### 1️⃣ Start Cluster
```
minikube start
```
### 2️⃣ Enable Ingress
```
minikube addons enable ingress
```
### 3️⃣ Deploy Applications
```
kubectl apply -f app1-deployment.yaml
kubectl apply -f app1-service.yaml

kubectl apply -f app2-deployment.yaml
kubectl apply -f app2-service.yaml
```
### 4️⃣ Apply Ingress
```
kubectl apply -f ingress-multiple.yaml
```
### 5️⃣ Configure Hosts File
```
sudo nano /etc/hosts
```
Add:
```
<minikube-ip> app.local
```
### 6️⃣ Test
```
http://app.local/web
http://app.local/api
```
## 🔍 Verification
```
kubectl get ingress
kubectl describe ingress multi-service-ingress
kubectl get svc
kubectl get pods
```
## 🧠 Interview Talking Points

- Why single ingress for multiple services?

- Difference between path-based vs host-based routing

- Ingress vs API Gateway

- Production ingress patterns

- How TLS works with Ingress

## 🌍 Real-World Use Case

- Frontend + Backend in one domain

- Microservices routing

- Cost optimization (single LB)

- Clean external exposure

## 👨‍💻 Author

Kubernetes learning project for DevOps & Cloud roles.