# 🟢 Day 4 — Deployments & ReplicaSets


This project demonstrates how to create and manage a Kubernetes **Deployment** using **nginx**.


## 🚀 Features


- Create a Kubernetes Deployment
- Manage ReplicaSets automatically
- Scale replicas up and down
- Production‑ready YAML structure


---


## 📦 Prerequisites


- Kubernetes Cluster (Minikube / Kind / Cloud)
- kubectl installed


---


## ⚙️ Deploy Application


```
kubectl apply -f deployment-nginx.yaml
```
Check deployment status:
```
kubectl get deployments
kubectl get pods
```
## 📈 Scale Replicas

Scale up:
```
kubectl scale deployment nginx-deployment --replicas=5
```
Scale down:
```
kubectl scale deployment nginx-deployment --replicas=2
```
## 🔍 Verify ReplicaSet
```
kubectl get rs
```
## 🧹 Cleanup
```
kubectl delete -f deployment-nginx.yaml
```
## 📚 Concepts Covered

- Kubernetes Deployment

- ReplicaSet

- Pod Template

- Declarative YAML

- Scaling Applications

## 👨‍💻 Author

Md Nahid Hasan  
DevOps / Cloud Enthusiast

⭐ If you like this repo, give it a star!