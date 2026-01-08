# 🟢 Day 7 — Mini Project 1
## Local Docker Image with Minikube


### 🎯 Objective
- Build Docker image locally
- Use Minikube internal Docker daemon
- Deploy custom image on Kubernetes


---


## 🧱 Step 1: Start Minikube


```
minikube start
```
## Step 2: Use Minikube Docker Daemon
eval $(minikube docker-env)

Verify:
```
docker ps
```
## 🐳 Step 3: Build Docker Image
```
docker build -t local-nginx:1.0 .
```
Confirm:
```
docker images
```
## 🚀 Step 4: Deploy to Kubernetes
```
kubectl apply -f deployment.yaml
```
Check:
```
kubectl get pods
```
## 🌐 Step 5: Access Application
```
kubectl port-forward deployment/local-nginx-deployment 8080:80
```
Open browser:
```
http://localhost:8080
```
## 🧠 Key Learnings

- Difference between local Docker & Minikube Docker

- Why imagePullPolicy: Never is required

- How Kubernetes runs custom local images

## 🧹 Cleanup
```
kubectl delete -f deployment.yaml  
minikube stop
```
## 👨‍💻 Author

Md Nahid Hasan  
DevOps / Cloud Learner

## ⭐ Star this repo if it helped you!