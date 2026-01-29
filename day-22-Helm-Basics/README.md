# Day 22 Helm Basics Project

This project demonstrates Helm fundamentals by deploying an NGINX application
on Kubernetes using a custom Helm chart.

## ✅ Step 0: Helm Install (Local Machine)
**Linux / Mac**  
```
curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash
```
**Verify**
```
helm version
```
## ✅ Step 1: Create a Helm Chart

Create a new Helm chart using the following command:
```
helm create my-first-app
```

This command generates the following directory structure:
```
my-first-app/
├── Chart.yaml
├── values.yaml
├── templates/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── _helpers.tpl
```

👉 This directory is called a Helm Chart, which acts as a Kubernetes application package 📦.

## ✅ Step 2: Understand the Chart Structure (Quick Overview)
📄 **Chart.yaml**
```
name: my-first-app
version: 0.1.0
```

- Contains application metadata

- Defines chart name and version

📄 **values.yaml (Most Important File)**  
```
replicaCount: 1

image:
  repository: nginx
  tag: latest

```
From this file, you can control:

- Number of Pods (replicaCount)

- Container image and version

This makes configuration simple and reusable across environments.

## ✅ Step 3: Install the Application Using Helm

Run the following command to deploy the application:
```
helm install myapp ./my-first-app
```

Expected output:
```
NAME: myapp
STATUS: deployed
```

🎉 Congratulations! Your application has been successfully deployed using Helm.

## ✅ Step 4: Verify the Deployment

Check the running Pods and Services:
```
kubectl get pods
kubectl get svc
```

You should see:

- Running Pods

- A Service created for the application

## ✅ Step 5: Access the Application
**If you are using Minikube:**
```
minikube service myapp
```
**OR using port-forward:**
```
kubectl port-forward svc/myapp 8080:80
```

Open your browser and visit:
```
http://localhost:8080
```

🎯 If you see the Nginx Welcome Page, the deployment was successful.

## ✅ Step 6: Upgrade the Application (Helm Magic ✨)

Update `values.yaml`:
```
replicaCount: 3
```

Apply the change using:
```
helm upgrade myapp ./my-first-app
```

Verify:
```
kubectl get pods
```

👉 You should now see **3 running Pods 😎**   
No manual YAML editing or redeployment hassle.

## ✅ Step 7: Rollback (Production-Grade Feature)

View release history:
```
helm history myapp

```
Rollback to a previous version:
```
helm rollback myapp 1

```
👉 This rollback capability is a **key production-ready feature of Helm** 🔥.

## 📌 Summary

- Helm simplifies Kubernetes deployments

- Configuration is centralized via values.yaml

- Supports upgrades, versioning, and rollbacks

- Widely used in real-world DevOps and CI/CD pipelines