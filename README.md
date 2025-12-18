#  30 Days Minikube Kubernetes Hands-On Roadmap
**(Daily 1–2 Hours Practice Plan)**


---

## 📌 Week 1 — Minikube Basics + Pods & Deployments

### 🟢 Day 1 — Minikube Setup
- Install Minikube  
- Install kubectl  
- Minikube start / stop / delete  
- Check cluster status  

📂 **GitHub**: `setup/` (install guide + notes)

---

### 🟢 Day 2 — kubectl Basics
- `kubectl get`
- `kubectl describe`
- `kubectl logs`
- `kubectl exec`
- Create / delete namespaces  

📂 **GitHub**: `cheatsheet.md`

---

### 🟢 Day 3 — First Pod
- Write Pod YAML
- `kubectl apply`
- `kubectl edit`
- `kubectl delete`

📂 **GitHub**: `pod.yaml`

---

### 🟢 Day 4 — Deployments & ReplicaSets
- Create Deployment
- Scale up / down replicas

📂 **GitHub**: `deployment-nginx.yaml`

---

### 🟢 Day 5 — Services
- ClusterIP
- NodePort
- Expose application

📂 **GitHub**: `service-nodeport.yaml`

---

### 🟢 Day 6 — Accessing Apps Locally
- `minikube service`
- `minikube tunnel`

📂 **GitHub**: `notes/` + screenshots

---

### 🟢 Day 7 — Mini Project 1
- Build local Docker image
- Use Minikube internal Docker daemon
- Deploy custom image

📂 **GitHub**:
- `Dockerfile`
- `deployment.yaml`

---

## 📌 Week 2 — Config, Secrets & Volumes

### 🟢 Day 8 — ConfigMap
- Create ConfigMap
- Mount as file
- Inject as environment variable

📂 **GitHub**: `configmap.yaml`

---

### 🟢 Day 9 — Secrets
- Use Secrets as env
- Mount Secrets as volume  
> ⚠️ Plain text allowed for learning purpose

📂 **GitHub**: `secret.yaml`

---

### 🟢 Day 10 — Persistent Volumes
- Create PV
- Create PVC

📂 **GitHub**: `pv-pvc.yaml`

---

### 🟢 Day 11 — Use PV in Pod
- Mount volume
- Verify data persistence

📂 **GitHub**: `pv-app.yaml`

---

### 🟢 Day 12 — Probes
- Liveness Probe
- Readiness Probe
- Startup Probe

📂 **GitHub**: `probes-example.yaml`

---

### 🟢 Day 13 — Rolling Updates
- Rolling update
- Rollback deployment

📂 **GitHub**: `rollout-commands.md`

---

### 🟢 Day 14 — Mini Project 2
A real application using:
- Deployment
- ConfigMap
- Secrets
- Persistent Volume
- NodePort Service

📂 **GitHub**: `full-app/`

---

## 📌 Week 3 — Networking, Ingress & Autoscaling

### 🟢 Day 15 — Kubernetes Networking
- Kubernetes DNS
- Service → Pod communication

📂 **GitHub**: `networking-notes.md`

---

### 🟢 Day 16 — Ingress Setup
- Enable Ingress addon
- NGINX Ingress Controller

📂 **GitHub**: `ingress.yaml`

---

### 🟢 Day 17 — Multiple Services via Ingress
- Route multiple services

📂 **GitHub**: `ingress-multiple.yaml`

---

### 🟢 Day 18 — Resource Management
- CPU & Memory requests
- CPU & Memory limits

📂 **GitHub**: `resources.yaml`

---

### 🟢 Day 19 — Horizontal Pod Autoscaler
- Configure HPA
- Generate load using BusyBox

📂 **GitHub**: `hpa.yaml`

---

### 🟢 Day 20 — DaemonSets & Jobs
- DaemonSet
- Job
- CronJob

📂 **GitHub**: `jobs-cronjobs.yaml`

---

### 🟢 Day 21 — Mini Project 3
Multi-service microservice application:
- Frontend
- Backend
- Database
- Ingress routing

📂 **GitHub**: `microservice-app/`

---

## 📌 Week 4 — Helm, Monitoring & Advanced Workflow

### 🟢 Day 22 — Helm Basics
- Install Helm
- Create first Helm chart

📂 **GitHub**: `helm-chart/`

---

### 🟢 Day 23 — Helm Templating
- Understand templates
- values.yaml variations

📂 **GitHub**: `values.yaml`

---

### 🟢 Day 24 — Deploy with Helm
- Deploy full app using Helm

📂 **GitHub**: Helm deploy logs + files

---

### 🟢 Day 25 — Monitoring
- Install Metrics Server
- `kubectl top nodes`
- `kubectl top pods`

📂 **GitHub**: `monitoring.md`

---

### 🟢 Day 26 — Kubernetes Dashboard
- Install Dashboard addon
- Secure token-based login

📂 **GitHub**: `dashboard-setup.md`

---

### 🟢 Day 27 — Local CI/CD Style Workflow
- Commit Kubernetes YAML
- Auto build Docker image (local)
- Apply manifests using script

📂 **GitHub**: `ci-local-script.sh`

---

### 🟢 Day 28 — Backup & Restore
- etcd backup (Minikube)
- Export Kubernetes manifests

📂 **GitHub**: `backup.md`

---

### 🟢 Day 29 — Troubleshooting Day
- CrashLoopBackOff
- Pending Pods
- ImagePullBackOff

📂 **GitHub**: `troubleshooting.md`

---

## 🚀 Day 30 — Final Project
**Production-like Kubernetes system on Minikube**

### Features:
- 3 Services
- Ingress routing
- Persistent Volume for Database
- ConfigMaps & Secrets
- Horizontal Autoscaling
- Helm chart based deployment

📂 **GitHub**: `final-project/`

---

## 🎯 Goal
By the end of 30 days you will be able to:
- Confidently work with Kubernetes
- Deploy real-world applications
- Understand DevOps & production workflows
- Prepare for Kubernetes interviews & real jobs 🚀
