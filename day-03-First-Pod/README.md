# 🟢 Day 3 — First Pod (Kubernetes)

## 📘 Objective

In this Day 3 project, we will learn:

- How to write a Pod YAML file
- How to create a Pod
- How to edit a running Pod
- How to delete a Pod

---

## 🔹 Prerequisites

Make sure the following are installed and running:

- Minikube
- kubectl
- A running Kubernetes cluster

Check cluster status:

```
minikube status
kubectl get nodes
```
## 🔹 Step 1: Create a Pod

Apply the Pod YAML file:
```
kubectl apply -f pod.yaml
```

Verify the Pod status:
```
kubectl get pods
```
## 🔹 Step 2: View Pod Details

Describe the Pod to see detailed information:
```
kubectl describe pod first-pod
```
## 🔹 Step 3: View Pod Logs

Check logs from the container running inside the Pod:
```
kubectl logs first-pod
```
## 🔹 Step 4: Edit the Pod

Edit the running Pod:
```
kubectl edit pod first-pod
```

Example: change the container image version
```
image: nginx:1.25
```

After saving the file, Kubernetes will automatically update the Pod.

## 🔹 Step 5: Delete the Pod

Delete the Pod from the cluster:
```
kubectl delete pod first-pod
```
## 🧠 Key Notes (Interview Ready)

- A Pod is the smallest deployable unit in Kubernetes

- A Pod can contain one or more containers

- Pods are ephemeral; data is lost when a Pod is deleted

- In production environments, Deployments are used instead of standalone Pods

## ✅ Expected Output

- `kubectl get pods` → STATUS should be Running

- NGINX default page in the browser (optional, via port-forwarding)

Port-forward command:
```
kubectl port-forward pod/first-pod 8080:80
```

Open in browser:
```
http://localhost:8080
```