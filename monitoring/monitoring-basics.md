# 🛡️ Monitoring Basics — Prometheus & Grafana

Monitoring is a **core DevOps practice** that helps ensure **system reliability, performance, and availability**.  
It allows teams to **detect issues early, analyze performance, and take proactive actions**.

---

## 🎯 Objectives

By the end of this guide, you will be able to:  
- Understand what monitoring is and why it is essential.  
- Monitor servers and Docker containers.  
- Centralize metrics with Prometheus.  
- Visualize and analyze metrics with Grafana.  
- Apply monitoring in a DevOps workflow.

---

## 🧩 What is Monitoring?

Monitoring is the **continuous observation of system health** to:  
- Detect anomalies.  
- Measure performance.  
- Prevent failures.  
- Ensure service availability.  

---

## 🔄 Why Monitoring is Essential

### 1️⃣ Fast Incident Detection
- Know immediately if: CPU is overloaded, memory is full, a container restarts, or a service fails.  
- Without monitoring ❌ → delayed detection.  
- With monitoring ✅ → immediate response.

### 2️⃣ Performance Tracking
- Answers questions like:  
  - Is the server resource usage optimal?  
  - Which application consumes the most resources?  
  - Should the infrastructure scale?

### 3️⃣ Failure Prediction
- Historical metrics allow spotting abnormal trends and **preventing outages** before they impact users.

### 4️⃣ Monitoring ≠ Logs ≠ Security
| Element    | Role                                         |
|-----------|---------------------------------------------|
| Monitoring | System health: CPU, RAM, availability       |
| Logs       | Application errors, requests                |
| Security   | Vulnerabilities, attacks                    |

Monitoring **complements logs and security**.

---

## 🧰 Monitoring Stack Overview

### Prometheus
- Collects and stores time-series metrics.  
- Scrapes metrics from servers and containers.  
- Supports querying with PromQL.

### Node Exporter
- Monitors Linux host metrics: CPU, RAM, disk, network.  
- Helps identify server-level issues.

### Grafana
- Creates **visual dashboards**.  
- Analyzes metrics in real-time.  
- Shares insights with teams.

---

## 🌐 Architecture Diagram

![Monitoring Architecture](https://miro.medium.com/v2/resize:fit:1200/1*v-ohSTzLH_AWPBFRM44d5Q.png "Monitoring Stack Architecture")

*Shows Prometheus, Node Exporter, and Grafana integration.*

---

## 📦 Deploying the Monitoring Stack

- Requires **Docker** and **Docker Compose**.
  
### Docker Compose Example

```yaml
version: "3"
services:
  prometheus:
    image: prom/prometheus:latest
    container_name: monitoring_prometheus
    ports:
      - 9090:9090
  node-exporter:
    image: prom/node-exporter:latest
    ports:
      - 9100:9100
  grafana:
    image: grafana/grafana:latest
    ports:
      - 3006:3000

```
Start the stack
```bash
docker compose up -d
```
Verify running containers
```bash
docker ps
```
Prometheus access: http://localhost:9090

Grafana access: http://localhost:3006
 (login: admin / admin)
 

### 📊 Recommended Dashboards
Node Exporter

Complete server resource view (CPU, RAM, disk, network)

Dashboard ID: 1860


### 🔁 Monitoring in the DevOps Cycle
Code → CI/CD → Deployment → Monitoring → Alerts → Continuous Improvement


Monitoring is essential for a complete DevOps workflow.


---

## 📌 Summary

- Monitors servers and containers
- Detects incidents quickly
- Provides clear visualizations
- Uses a standard and scalable stack
- Stack: Prometheus + Node Exporter + Grafana → robust, open-source, modern DevOps solution



➡️ Next step in learning:

`student-guide/resources.md` → Free resources, courses, and guides for DevOps students  
