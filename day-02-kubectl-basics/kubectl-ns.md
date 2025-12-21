# 📘 Kubernetes Namespaces

Namespaces are a way to **organize and isolate resources** in a Kubernetes cluster.  
They help separate environments like **development, testing, and production**, or different teams in a shared cluster.

---

## 🔹 Create a Namespace

Use the `kubectl create namespace` command to create a new namespace.

```
kubectl create namespace <namespace-name>
```
**Example:**
```
kubectl create namespace dev
kubectl create namespace test
```

✅ This is useful when you want to isolate resources like Pods, Services, and Deployments in a separate environment.

## 🔹 Delete a Namespace

Use the kubectl delete namespace command to delete an existing namespace.
Warning: This will delete all resources inside that namespace.
```
kubectl delete namespace <namespace-name>
```

**Example:**
```
kubectl delete namespace dev
kubectl delete namespace test
```

## 💡 Tip:

Always double-check before deleting a namespace to avoid unintended data loss.

You can check existing namespaces using:
```
kubectl get namespaces
```