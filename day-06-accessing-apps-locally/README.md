# 🟢 Day 6 — Accessing Apps Locally (Minikube)

On Day 6, I learned how to access applications running inside a Kubernetes cluster **from my local machine (browser)**.  
The focus was on **Services**, **NodePort**, and **minikube tunnel** in a local Minikube environment.

---

## 🔹 What is a Service?
In Kubernetes, a **Service** provides a **stable network endpoint** to access Pods.

- Pod IPs can change
- A Service IP stays stable
- Services use **labels and selectors** to connect to Pods

👉 Without a Service, accessing Pods reliably is difficult.

---

## 🔹 ClusterIP, NodePort, and LoadBalancer

- **ClusterIP** → Accessible only inside the cluster  
- **NodePort** → Accessible using Node IP and a fixed port  
- **LoadBalancer** → Provides an external IP (mainly in cloud environments)

---

## 🔹 What is Minikube Tunnel?

`minikube tunnel` is a command that allows **LoadBalancer-type Services to work in a local Minikube cluster**.

In a local setup:
- There is no real cloud load balancer
- `EXTERNAL-IP` remains `<pending>`

`minikube tunnel` solves this by **simulating an external IP**.

---

## 🔹 Why Use `minikube tunnel`?

- To test `type: LoadBalancer` Services locally
- To simulate an external IP in Minikube
- To access applications directly from a browser

---

## 🔹 Using Minikube Tunnel

```
minikube tunnel
```

