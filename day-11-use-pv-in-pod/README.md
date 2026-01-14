# Kubernetes Persistent Volume Demo (PV + PVC)

## 📌 Project Overview
This project demonstrates how to use **PersistentVolume (PV)** and
**PersistentVolumeClaim (PVC)** in Kubernetes to provide persistent storage
to a Pod.

The goal is to prove that **data remains intact even if a Pod is deleted
and recreated**, which is a core concept in production Kubernetes workloads.

---

## 🧱 Architecture Overview

- **PersistentVolume (PV)**  
  - Cluster-scoped storage resource  
  - Represents actual physical storage

- **PersistentVolumeClaim (PVC)**  
  - Namespace-scoped storage request  
  - Abstracts storage details from the Pod

- **Pod**  
  - Uses PVC to mount persistent storage  
  - Does not directly interact with PV

Pod → PVC → PV → Physical Storage
## 🚀 How to Run (Minikube / Local Cluster)
### 1️⃣ Apply resources
```
kubectl apply -f pv-pod-app.yaml
```
### 2️⃣ Verify resources
```
kubectl get pv
kubectl get pvc
kubectl get pods
```
## 🧪 Persistence Test (Key Part)
### Step 1: Exec into Pod
```
kubectl exec -it pv-demo-pod -- /bin/sh
```
### Step 2: Create a file
```
echo "Hello from Persistent Volume" > /usr/share/nginx/html/index.html
```
### Step 3: Exit and delete Pod
```
kubectl delete pod pv-demo-pod
```
### Step 4: Recreate Pod
```
kubectl apply -f pv-pod-app.yaml
```
## ✅ Result
The file remains available after Pod recreation, proving that
the data is persisted using PV and PVC.

## 🧠 Key Learnings
- Pods are **ephemeral**, volumes are **persistent**

- PV is **cluster-scoped**, PVC is **namespace-scoped**

- Pods never use PV directly — they use PVC

- Storage is decoupled from application logic