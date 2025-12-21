# kubectl describe is an inspection and debugging command in Kubernetes.

👉 It shows detailed information about a resource, including:

- Current state (Status)

- Configuration details

- Events (Warning / Error / Info)

- In-depth information related to the resource

All output is shown in a human-readable format.

- 🔑 kubectl get shows only a summary
- 🔑 kubectl describe shows full internal details

- 🔹 Resources that can be described using kubectl describe (Complete List)

Below is a complete list of the most commonly used and practically important Kubernetes resource types that can be described.

## 🟦 Workload Resources
```
kubectl describe pod <pod-name>
kubectl describe deployment <deployment-name>
kubectl describe replicaset <replicaset-name>
kubectl describe statefulset <statefulset-name>
kubectl describe daemonset <daemonset-name>
kubectl describe job <job-name>
kubectl describe cronjob <cronjob-name>
```
## 🟩 Service & Networking
```
kubectl describe service <service-name>
kubectl describe endpoints <endpoints-name>
kubectl describe ingress <ingress-name>
kubectl describe networkpolicy <networkpolicy-name>
```
## 🟨 Storage Resources
```
kubectl describe persistentvolume <pv-name>
kubectl describe persistentvolumeclaim <pvc-name>
kubectl describe storageclass <storageclass-name>
```
## 🟥 Configuration & Security
```
kubectl describe configmap <configmap-name>
kubectl describe secret <secret-name>
kubectl describe serviceaccount <serviceaccount-name>
kubectl describe role <role-name>
kubectl describe rolebinding <rolebinding-name>
kubectl describe clusterrole <clusterrole-name>
kubectl describe clusterrolebinding <clusterrolebinding-name>
```
## 🟪 Cluster & Namespace Level
```
kubectl describe node <node-name>
kubectl describe namespace <namespace-name>
kubectl describe resourcequota <resourcequota-name>
kubectl describe limitrange <limitrange-name>
kubectl describe event <event-name>
kubectl describe events
```
## 🟧 Autoscaling
```
kubectl describe horizontalpodautoscaler <hpa-name>
```
## 🟫 Custom / Extension
```
kubectl describe customresourcedefinition <crd-name>
```