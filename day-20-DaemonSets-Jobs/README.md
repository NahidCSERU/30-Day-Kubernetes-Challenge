# Day 20 — DaemonSets & Jobs in Kubernetes

This project demonstrates the use of Kubernetes DaemonSet, Job, and CronJob
for running node-level tasks and batch workloads.

## 📦 Resources Included
- DaemonSet: Runs a logging pod on every node
- Job: Executes a one-time task
- CronJob: Runs scheduled jobs

## 🚀 Apply Resources

```
kubectl apply -f daemonset.yaml
kubectl apply -f job.yaml
kubectl apply -f cronjob.yaml
```
OR apply everything at once:
```
kubectl apply -f jobs-cronjobs.yaml
```
## 🔍 Verify
```
kubectl get daemonsets
kubectl get jobs
kubectl get cronjobs
kubectl get pods
```
## 📄 View Logs
```
kubectl logs <pod-name>
```
## 🧹 Cleanup
```
kubectl delete -f .
```
## 🎯 Learning Outcomes

- Understand DaemonSet use-cases (node monitoring, logging)

- Execute batch jobs using Job

- Schedule recurring tasks using CronJob

- Manage Kubernetes batch workloads professionally

⭐ Star this repository if you find it helpful!