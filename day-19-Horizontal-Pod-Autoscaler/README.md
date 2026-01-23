# Day 19 — Horizontal Pod Autoscaler (HPA)

This project demonstrates how to configure and test Kubernetes Horizontal Pod Autoscaler (HPA)
using CPU-based autoscaling.

## 📌 Components
- PHP Apache Deployment
- ClusterIP Service
- Horizontal Pod Autoscaler
- BusyBox Load Generator

## 🚀 Prerequisites
- Kubernetes Cluster
- Metrics Server installed

```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```
## 📦 Deployment Steps
```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f hpa.yaml
```
## 🔥 Generate Load
```
kubectl apply -f load-generator.yaml
```
## 📊 Observe Autoscaling
```
kubectl get hpa
kubectl get pods -w
```
## 🧹 Cleanup
```
kubectl delete -f .
```
## 📚 Learning Outcome

- Understand HPA configuration

- CPU-based autoscaling

- Real-time load testing with BusyBox

⭐ If you find this useful, give the repo a star!
