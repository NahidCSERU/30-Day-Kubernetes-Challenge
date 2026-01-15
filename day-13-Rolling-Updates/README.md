# 🟢 Day 13 — Rolling Updates & Rollbacks in Kubernetes

This project is part of the **Kubernetes 30 Days Learning Challenge** and focuses on  
**Day 13: Rolling Updates and Rollback strategies using Kubernetes Deployments**.

Rolling updates are a critical feature in Kubernetes that allow applications to be updated
**without downtime**, while rollback enables quick recovery if a deployment fails.

---

## 🎯 Project Objectives

- Understand Kubernetes Rolling Updates
- Perform application updates using Deployment
- Learn how to rollback to a previous version
- Practice rollout monitoring and history inspection
- Gain production-ready deployment management skills

---

## 🧠 Concepts Covered

### 🔹 Rolling Update

A **Rolling Update** updates Pods gradually instead of all at once.
This ensures:
- Zero downtime
- Continuous availability
- Controlled rollout of new versions

Kubernetes replaces old Pods with new ones based on update strategy settings.

---

### 🔹 Rollback Deployment

A **Rollback** allows reverting a Deployment to a previous stable version
if a new release introduces errors or instability.

This is essential for:
- Production safety
- Fast recovery
- Release confidence

---

## 📄 rollout-commands.md

This file contains commonly used `kubectl rollout` commands to:
- Track deployment status
- View rollout history
- Undo failed deployments
- Rollback to specific revisions

---

## 🚀 How to Use This Project

1. Deploy an application using a Kubernetes Deployment
2. Update the container image version
3. Monitor rollout progress
4. Perform rollback if needed

All related commands are documented in `rollout-commands.md`.

---

## ✅ Best Practices

- Always use **Deployments** for stateless applications
- Monitor rollout status during updates
- Keep rollout history enabled
- Test updates in non-production environments first
- Combine rolling updates with readiness probes

---

## 📌 Key Learnings (Day 13)

- How Kubernetes performs zero-downtime updates
- How to monitor deployment rollouts
- How to rollback safely during failures
- Importance of controlled releases in production

---


## ⭐ Support

If this project helps you understand Kubernetes rolling updates and rollbacks,
please consider giving the repository a ⭐.

**Happy Learning 🚀  
Kubernetes 30 Days Challenge**
