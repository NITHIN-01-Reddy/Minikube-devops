# Kubernetes Local Cluster Setup using Minikube

## 📌 Objective

The objective of this project is to deploy and manage an application in a local Kubernetes cluster using Minikube. This task demonstrates core Kubernetes concepts such as deployments, services, scaling, and cluster management.

---

## 🛠️ Tools Used

* Minikube
* kubectl
* Docker

---

## 🚀 Project Overview

In this project, a local Kubernetes cluster was created using Minikube. An NGINX application was deployed using a Deployment configuration and exposed using a Service. The application was accessed through a browser, and scaling operations were performed to manage multiple pods.

---

## 📁 Project Structure

```
MiniKube-project/
│
├── deployment.yaml
├── service.yaml
├── README.md
└── screenshots/
```

---

## ⚙️ Steps Performed

### 1. Start Minikube Cluster

```bash
minikube start --driver=docker
```

---

### 2. Verify Cluster

```bash
kubectl get nodes
```

---

### 3. Create Deployment

A deployment was created using the following configuration:

* Application: NGINX
* Replicas: 2
* Container Port: 80

```bash
kubectl apply -f deployment.yaml
```

---

### 4. Verify Pods

```bash
kubectl get pods
```

---

### 5. Expose Application using Service

A NodePort service was created to expose the application externally.

```bash
kubectl apply -f service.yaml
kubectl get svc
```

---

### 6. Access Application

The application was accessed using:

```bash
minikube service my-service
```

The browser displayed the NGINX welcome page, confirming successful deployment.

---

### 7. Scale Deployment

The number of pods was increased from 2 to 4:

```bash
kubectl scale deployment my-app --replicas=4
```

---

### 8. Describe Pod

Detailed information about pods was retrieved:

```bash
kubectl describe pod <pod-name>
```

---

## 📸 Screenshots

The following screenshots are included in the `screenshots` folder:

* Node status (`kubectl get nodes`)
* Pod creation (`kubectl get pods`)
* Service details (`kubectl get svc`)
* Browser output (NGINX page)
* Scaled pods (4 replicas)
* Pod description

---

## 🎯 Key Concepts Learned

* Kubernetes cluster setup using Minikube
* Deployment and pod management
* Service creation and exposure
* Scaling applications in Kubernetes
* Inspecting resources using kubectl

---

## 📌 Outcome

This project successfully demonstrates how to deploy and manage containerized applications in Kubernetes. It provides hands-on experience with real-world DevOps practices such as scaling, service exposure, and cluster management.

---

## ✅ Conclusion

This task provided practical experience in working with Kubernetes and understanding how applications are deployed, exposed, and scaled in a cluster environment.

---
