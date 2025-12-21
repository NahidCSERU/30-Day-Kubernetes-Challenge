# 📘 Kubernetes kubectl exec

`kubectl exec` is a Kubernetes command used to **execute commands inside a container of a Pod**.

---

## 🔹 What `kubectl exec` Does?

- Lets you **run shell commands inside a container**  
- Useful for **debugging, inspecting, and troubleshooting**  
- Can also be used to **open an interactive shell** inside a container  

### 🔑 Key Points

- Works **only on Pod containers**  
- If a Pod has **multiple containers**, use `-c <container-name>` to specify the container  
- Can run **both single commands or interactive shells**  

---

## 🔹 Resources Where `kubectl exec` Works

`kubectl exec` works primarily on **Pods and their containers**.  

### 📦 Pod
```
kubectl exec <pod-name> -- <command>
```
**Example:** 
```
kubectl exec my-pod -- ls /app
```
### 📦 Pod with specific container
```
kubectl exec <pod-name> -c <container-name> -- <command>
```

Example:
```
kubectl exec my-pod -c my-container -- ls /app
```
### 📦 Interactive shell inside a container
```
kubectl exec -it <pod-name> -- /bin/bash
```
or
```
kubectl exec -it <pod-name> -c <container-name> -- /bin/sh
```

### 💡 Tip:
kubectl exec does not work directly on Deployment, Service, Node, etc.
To run commands in a Deployment, first get the Pod name (kubectl get pods) and then exec into it.