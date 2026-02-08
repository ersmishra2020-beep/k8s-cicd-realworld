# CI/CD with Kubernetes – Real World DevOps Project

## 📌 Project Overview
This project demonstrates a **real-world CI/CD pipeline with Kubernetes**, covering modern DevOps practices such as automated builds, containerization, and advanced deployment strategies like **Blue-Green** and **Canary deployments**.

The goal of this project is to show **how applications are built, tested, packaged, and deployed automatically to a Kubernetes cluster** using industry-standard tools.

---

## 🧰 Tools & Technologies Used
- **GitHub** – Source code management
- **Docker** – Containerization
- **Kubernetes (K8s)** – Container orchestration
- **GitHub Actions** – CI/CD automation
- **Jenkins** (optional) – Enterprise CI/CD
- **Helm** – Kubernetes package manager
- **NGINX** – Sample application server

---

## 🏗️ Project Structure

---

## 🔄 CI/CD Pipeline Flow
1. Developer pushes code to GitHub
2. GitHub Actions / Jenkins pipeline triggers
3. Application is built
4. Docker image is created
5. Image is pushed to container registry
6. Kubernetes manifests / Helm charts are applied
7. Application is deployed to Kubernetes cluster


---

## 🚀 Deployment Strategies Implemented

### 1️⃣ Rolling Deployment
- Default Kubernetes strategy
- Pods are updated gradually
- No downtime, minimal resources

---

### 2️⃣ Blue-Green Deployment
- Two environments: **Blue (current)** and **Green (new)**
- Traffic switched instantly using Kubernetes Service
- Easy rollback by switching selector

**Best for:**  
✔ Critical production systems  
✔ Zero-downtime releases

---

### 3️⃣ Canary Deployment
- New version released to a small number of users
- Gradual traffic increase
- Metrics and logs monitored before full rollout

**Best for:**  
✔ Risk-sensitive features  
✔ Continuous experimentation

---

## 📦 Helm Usage
Helm is used to:
- Template Kubernetes YAML files
- Manage environment-specific configurations
- Perform easy upgrades and rollbacks

### Common Helm Commands
```bash
helm install myapp ./myapp
helm upgrade myapp ./myapp
helm rollback myapp 1
kubectl apply -f k8s-manifests/
kubectl get pods
kubectl get svc



