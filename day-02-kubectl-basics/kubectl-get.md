# kubectl get দিয়ে যেসব রিসোর্স দেখা যায়

`kubectl get` হচ্ছে Kubernetes-এর সবচেয়ে বেশি ব্যবহৃত কমান্ড।  
এটা দিয়ে আমরা ক্লাস্টারের বর্তমান অবস্থা দেখতে পারি—কি কি রিসোর্স চলছে, কয়টা pod, কোন service, কোন deployment ইত্যাদি।

নিচে **সবচেয়ে গুরুত্বপূর্ণ ও বাস্তবে ব্যবহৃত resource গুলো** লিস্ট করা হলো  
(Production কাজ ও শেখার জন্য যথেষ্ট)

---

## 🔹 Core / Basic Resources

| কমান্ড | কাজ |
|------|----|
| `kubectl get pods` | চলমান Pod গুলো দেখায় |
| `kubectl get pod` | একই (short form) |
| `kubectl get services` | Service list |
| `kubectl get svc` | Service (short form) |
| `kubectl get nodes` | Cluster-এর node list |
| `kubectl get namespaces` | Namespace list |
| `kubectl get ns` | Namespace (short form) |
| `kubectl get events` | Cluster events |

---

## 🔹 Workload Resources

| কমান্ড | কাজ |
|------|----|
| `kubectl get deployments` | Deployment list |
| `kubectl get deploy` | Deployment (short form) |
| `kubectl get replicasets` | ReplicaSet list |
| `kubectl get rs` | ReplicaSet (short form) |
| `kubectl get statefulsets` | Stateful application list |
| `kubectl get sts` | StatefulSet (short form) |
| `kubectl get daemonsets` | DaemonSet list |
| `kubectl get ds` | DaemonSet (short form) |
| `kubectl get jobs` | Job list |
| `kubectl get cronjobs` | Scheduled jobs list |

---

## 🔹 Configuration Resources

| কমান্ড | কাজ |
|------|----|
| `kubectl get configmaps` | ConfigMap list |
| `kubectl get cm` | ConfigMap (short form) |
| `kubectl get secrets` | Secrets list |
| `kubectl get secret` | Secret (short form) |
| `kubectl get serviceaccounts` | ServiceAccount list |
| `kubectl get sa` | ServiceAccount (short form) |

---

## 🔹 Networking Resources

| কমান্ড | কাজ |
|------|----|
| `kubectl get ingress` | Ingress list |
| `kubectl get ing` | Ingress (short form) |
| `kubectl get endpoints` | Service endpoints |
| `kubectl get ep` | Endpoints (short form) |
| `kubectl get networkpolicies` | Network policy list |
| `kubectl get netpol` | NetworkPolicy (short form) |

---

## 🔹 Storage Resources

| কমান্ড | কাজ |
|------|----|
| `kubectl get persistentvolumes` | PersistentVolume (PV) list |
| `kubectl get pv` | PersistentVolume |
| `kubectl get persistentvolumeclaims` | PVC list |
| `kubectl get pvc` | PersistentVolumeClaim |
| `kubectl get storageclasses` | StorageClass list |
| `kubectl get sc` | StorageClass |

---

## 🔹 RBAC / Security Resources

| কমান্ড | কাজ |
|------|----|
| `kubectl get roles` | Namespace role |
| `kubectl get rolebindings` | Role binding |
| `kubectl get clusterroles` | Cluster role |
| `kubectl get clusterrolebindings` | Cluster role binding |

---

## 🔹 Custom / Advanced Resources

| কমান্ড | কাজ |
|------|----|
| `kubectl get crd` | CustomResourceDefinition |
| `kubectl get all` | সব basic workload resource |

---

## ⚠️ Important Note

`kubectl get all` **সব Kubernetes resource দেখায় না**।  
এটা সাধারণত নিচের resource গুলোই দেখায়:

- Pod  
- Service (svc)  
- Deployment  
- ReplicaSet (rs)  
- StatefulSet  

---

## 📌 Summary

> **`kubectl get` = Kubernetes cluster-এর বর্তমান অবস্থা দেখার সবচেয়ে গুরুত্বপূর্ণ কমান্ড**

এই লিস্ট জানলে Kubernetes-এর প্রায় **৮০% day-to-day কাজ** কভার হয়ে যায়।
