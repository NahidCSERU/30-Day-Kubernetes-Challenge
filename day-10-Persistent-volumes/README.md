# 📅 Day 10 — Persistent Volumes (PV & PVC)

This project is part of the **Kubernetes 30 Days Learning Challenge**, focusing on  
**Day 10: Persistent Volumes and Persistent Volume Claims**.

The goal of this project is to understand how Kubernetes handles **persistent storage**
using **Persistent Volumes (PV)** and **Persistent Volume Claims (PVC)**.

---

## 🎯 Project Objectives

- Create a Persistent Volume (PV)
- Create a Persistent Volume Claim (PVC)
- Understand the PV–PVC binding mechanism
- Practice writing clean and production-ready Kubernetes YAML files

---

## 🧠 Concepts Covered

### 🔹 Persistent Volume (PV)

A **Persistent Volume** is a cluster-level storage resource provisioned by an administrator.  
It exists independently of Pods and remains available even after Pods are deleted.

---

### 🔹 Persistent Volume Claim (PVC)

A **Persistent Volume Claim** is a request for storage made by a user or application.  
Kubernetes automatically binds the PVC to a suitable PV based on size, access mode, and storage class.

---

## 📂 Project Structure

```
Day-10-Persistent-Volumes/
│
├── pv.yaml
└── README.md
```
## 📄 pv.yaml

The `pv.yaml `file contains definitions for:

- A**Persistent Volume (PV)** with `1Gi` storage

- A **Persistent Volume Claim (PVC)** requesting `500Mi` storage

## 🚀 How to Apply

Apply the PV and PVC configuration using the following command:
```
kubectl apply -f pv.yaml
```
## 🔍 Verification

Check the status of the Persistent Volume and Persistent Volume Claim:
```
kubectl get pv
kubectl get pvc
```
**Expected Result**

- PV status should be: `Bound`

- PVC status should be: `Bound`

## 📌 Key Learnings (Day 10)

- Understanding Persistent Volumes and their lifecycle

- Creating and using Persistent Volume Claims

- Learning how Kubernetes binds PVCs to PVs

- Basics of persistent storage management in Kubernetes