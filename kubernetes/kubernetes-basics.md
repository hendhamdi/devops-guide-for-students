# ☸️ Kubernetes Fundamentals

Kubernetes (K8s) is a **platform for managing containerized applications** across multiple machines.  
It helps you **deploy, scale, and maintain applications reliably**.

---

## 🧩 Why Kubernetes?

- Automates **deployment, scaling, and operations** of containers
- Ensures **high availability** and **load balancing**
- Works well with **CI/CD pipelines** and Docker containers
- Simplifies **management of complex applications**

---

## 🔄 Key Concepts

### Cluster
- A Kubernetes **cluster** is a group of machines (nodes) that run containers
- **Master node**: controls the cluster  
- **Worker nodes**: run the containers

### Pod
- The **smallest deployable unit** in Kubernetes  
- Can contain **one or more containers** that share networking and storage

### Deployment
- A **Deployment** manages Pods  
- Ensures the **desired number of Pods** are running

### Service
- Exposes your application to **internal or external traffic**  
- Types: ClusterIP, NodePort, LoadBalancer

### Namespace
- A way to **organize and isolate resources** in a cluster

---

## 🛠️ Typical Kubernetes Workflow

1. **Write Deployment YAML** – define your app, replicas, and container image  
2. **Create deployment** – `kubectl apply -f deployment.yaml`  
3. **Check Pods** – `kubectl get pods`  
4. **Expose service** – `kubectl expose deployment myapp --type=LoadBalancer --port=80`  
5. **Monitor** – `kubectl get all` / `kubectl logs <pod>`  

---

## 🖼️ Kubernetes Concept Diagram

![Kubernetes Cluster Architecture](https://upload.wikimedia.org/wikipedia/commons/8/8c/Kubernetes_Cluster_Architecture.png "Kubernetes Cluster Architecture")

*Diagram showing the main components of a Kubernetes cluster: control plane, nodes, pods, and services.*  
Source: Wikipedia / Wikimedia Commons


---

## 🔑 Kubernetes Commands Cheat Sheet

```bash
kubectl get nodes          # List all nodes
kubectl get pods           # List all pods
kubectl apply -f file.yaml # Apply deployment
kubectl delete pod <name>  # Delete a pod
kubectl logs <pod>         # View logs
```
---

## 📌 Summary

Kubernetes allows you to orchestrate containers at scale
It helps deploy, monitor, and manage applications reliably
A core tool for DevOps workflows with Docker and CI/CD

➡️ Next step in learning:

`monitoring/monitoring-basics.md` → Prometheus & Grafana fundamentals

