# 🟢 Day 5 — Kubernetes Services (ClusterIP & NodePort)


This repository demonstrates Kubernetes Services using an nginx application.


## 🎯 Services Covered


1. ClusterIP Service
2. NodePort (Auto-assigned)
3. NodePort (Custom Port)
4. Loadbalancer
5. ExternalName


---


## 🚀 Deploy Application
```
kubectl apply -f deployment.yaml
```
## Create Services
```
kubectl apply -f clusterip.yaml
kubectl apply -f nodePort-auto.yaml
kubectl apply -f nodePort-custom.yaml
kubectl apply -f loadbalancer.yaml
kubectl apply -f externalName.yaml
```

## 🔍 Verify
```
kubectl get svc  
kubectl get pods -o wide
```
## 🌐 Access Application
ClusterIP (internal only)
```
kubectl port-forward svc/clusterip 8080:80
http://<NodeIP>:<NodePort>
```
Example (Minikube):

minikube service nginx-nodeport
## 🧹 Cleanup
kubectl delete -f .
## 📚 Concepts Learned

- Kubernetes Services

- ClusterIP vs NodePort

- Service selectors

- Pod networking & load balancing

👨‍💻 Author

Md Nahid Hasan  
DevOps / Cloud Learner

⭐ Star this repo if it helps you!