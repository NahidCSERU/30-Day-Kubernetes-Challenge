# Kubernetes Ingress with NGINX Controller

This project demonstrates how to expose a Kubernetes application using
**NGINX Ingress Controller** instead of NodePort or LoadBalancer.

---

## 🚀 What You Will Learn

- What is Ingress in Kubernetes
- Difference between Service vs Ingress
- How NGINX Ingress Controller works
- How traffic flows from user → ingress → service → pod
- Host-based routing

---

## 🧱 Architecture Flow

User → Ingress Controller → Service (ClusterIP) → Pod (NGINX)

---

## 🛠 Prerequisites

- Kubernetes cluster (Minikube / Kind)
- kubectl installed
- Minikube ingress addon enabled

---

## ⚙️ Setup Steps

### 1️⃣ Start Minikube
```
minikube start
```
### 2️⃣ Enable Ingress Addon
```
minikube addons enable ingress
```

Verify:
```
kubectl get pods -n ingress-nginx
```
### 3️⃣ Deploy Application
```
kubectl apply -f app-deployment.yaml
kubectl apply -f app-service.yaml
```
### 4️⃣ Apply Ingress
```
kubectl apply -f ingress.yaml
```
### 5️⃣ Update Hosts File
```
sudo nano /etc/hosts
```
Add:
```
<minikube-ip> demo.local
```
Get IP:
```
minikube ip
```
### 6️⃣ Test in Browser

Open:
```
http://demo.local
```

You should see the NGINX welcome page 🎉

## 🔍 Verification Commands
```
kubectl get ingress
kubectl describe ingress demo-ingress
kubectl get svc
kubectl get pods
```
## 🧠 Interview Talking Points

- Why Ingress instead of NodePort?

- Ingress is NOT a load balancer

- Controller vs Ingress resource difference

- Path-based vs host-based routing

- How production uses ALB / NGINX / Traefik

## 📌 Real World Use Case

- Single LoadBalancer

- Multiple domains

- TLS termination

- Microservices routing