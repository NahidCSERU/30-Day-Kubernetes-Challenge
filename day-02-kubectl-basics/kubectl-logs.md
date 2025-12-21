# 📘 Kubernetes kubectl logs

`kubectl logs` is a **debugging and inspection command in Kubernetes**.  
It is used to view **the logs of containers inside a Pod**.

---

## 🔹 What `kubectl logs` Does?

- Shows what is happening **inside the container**
- Helps inspect **runtime errors, warnings, and info messages**
- Useful for debugging issues like **CrashLoopBackOff** or **image pull errors**

### 🔑 Key Points

- Works **only for Pod containers**
- If a Pod has **multiple containers**, use `-c <container-name>` to specify the container

---

## 🔹 Resources Where `kubectl logs` Works?

`kubectl logs` is primarily applicable to **Pod resources and their containers**.  
Here are the common commands:

### 📦 Pod
```bash
kubectl logs <pod-name>
```
### 📦 Specific container in a Pod
```
kubectl logs <pod-name> -c <container-name>
```
### 📦 Previous container logs (if the container crashed and restarted)
```
kubectl logs <pod-name> -c <container-name> --previous
```

### 💡 Tip:
kubectl logs does not work directly on Deployment, Service, Node, etc. because they are abstractions over Pods.
To see logs of a Deployment, you need to get the Pod name first and then check its logs.
