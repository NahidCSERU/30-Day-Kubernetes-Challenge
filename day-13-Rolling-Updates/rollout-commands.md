# 🔄 Kubernetes Rolling Updates & Rollback — Cheatsheet

This document contains essential `kubectl rollout` commands used to manage
Kubernetes Deployments during application updates.

---

## 🚀 Check Deployment Status

```
kubectl rollout status deployment/<deployment-name>
```
Example:
```
kubectl rollout status deployment/nginx-deployment
```
## 📝 View Rollout History
```
kubectl rollout history deployment/<deployment-name>
```

Shows all previous revisions of the Deployment.

## 🔍 View Details of a Specific Revision
```
kubectl rollout history deployment/<deployment-name> --revision=2
```
## 🔄 Update Deployment Image (Trigger Rolling Update)
```
kubectl set image deployment/<deployment-name> <container-name>=<image>:<tag>
```

Example:
```
kubectl set image deployment/nginx-deployment nginx=nginx:1.25
```
## ⏪ Rollback to Previous Version (Undo)
```
kubectl rollout undo deployment/<deployment-name>
```
Rolls back to the immediately previous revision.

## ⏪ Rollback to a Specific Revision
```
kubectl rollout undo deployment/<deployment-name> --to-revision=1
```
## ⏸️ Pause a Rollout
```
kubectl rollout pause deployment/<deployment-name>
```
Used to temporarily stop a rollout.

## ▶️ Resume a Rollout
```
kubectl rollout resume deployment/<deployment-name>
```
## ❌ Restart a Deployment
```
kubectl rollout restart deployment/<deployment-name>
```

Useful for:

- Config changes

- Secret updates

- Pod recreation

## 📌 Common Use Cases

- Zero-downtime application updates

- Quick rollback during failed releases

- Controlled production deployments

- Release verification and monitoring