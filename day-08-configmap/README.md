# 🟢 Day 8 — Kubernetes ConfigMap

This project demonstrates how to use **ConfigMaps** in Kubernetes to manage application configuration separately from application code.

---

## 📌 What is Covered

In this project, the following concepts are demonstrated:

- Creating a ConfigMap
- Mounting a ConfigMap as a file inside a Pod
- Injecting ConfigMap values as environment variables

---

## 🚀 Apply Configuration

Apply the Kubernetes manifests in the following order:

```
kubectl apply -f configmap.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
## 🔍 Verification Steps
Check ConfigMaps
```
kubectl get configmap
kubectl describe configmap app-config
```
Check Pods
```
kubectl get pods
```
## 🧪 Verify Inside the Pod
Access the Pod shell
```
kubectl exec -it <pod-name> -- /bin/sh
```
## 🌱 Verify Environment Variables
Inside the Pod, run:
```
echo $APP_ENV
echo $APP_VERSION
```
These values should match the data defined in the ConfigMap.

## 📄 Verify Mounted ConfigMap File
If the ConfigMap is mounted as a file, verify it using:
```
cat /config/app.properties
```
This file is generated automatically from the ConfigMap keys and values.

## 📝 Summary
- ConfigMaps store non-sensitive configuration data

- They can be consumed by Pods as environment variables or files

- ConfigMaps help keep application configuration separate from code

- Any Pod or Deployment can reference a ConfigMap when needed

