# Day 9 — Kubernetes Secrets

This project demonstrates:

- Creating a Kubernetes Secret  
- Using a Secret as an Environment Variable  
- Mounting a Secret as a Volume (file)  

⚠️ Plain text secrets are used for learning purposes only.

---

## Apply

```
kubectl apply -f secret.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
## Verify
```
kubectl get secrets
kubectl describe secret app-secret
kubectl get pods
```
## Access the Pod and Check
```
kubectl exec -it <pod-name> -- /bin/sh
```
## Environment Variable Check
```
echo $DB_USER
echo $DB_PASSWORD
```
## File Check (Mounted Secret)
```
cat /secrets/DB_USER
cat /secrets/DB_PASSWORD
```