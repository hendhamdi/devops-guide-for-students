# 📊 Monitoring Fundamentals: Prometheus & Grafana

Monitoring is a **core DevOps practice**.  
It allows teams to **observe system and application performance**, detect issues, and improve reliability.

---

## 🧩 What is Monitoring?

Monitoring means continuously observing the health of a system to:  

- Detect anomalies  
- Measure performance  
- Anticipate failures  
- Ensure service availability  

> "You cannot improve, secure, or stabilize what you do not measure."

---

## 🎯 Why Monitoring is Important

### 1️⃣ Rapid Incident Detection
Monitoring allows teams to know quickly if:  

- CPU is overloaded  
- Memory is saturated  
- Docker containers restart in a loop  
- Services become unstable  

### 2️⃣ Performance Tracking
It helps answer questions like:  

- Does my server have enough resources?  
- Which application consumes the most?  
- Should I scale infrastructure?  

### 3️⃣ Predicting Failures
By analyzing metrics history:  

- Detect abnormal trends  
- Prevent outages before impacting users  
- Improve overall system stability  

### 4️⃣ Monitoring vs Logs vs Security
| Element   | Role                                        |
|-----------|--------------------------------------------|
| Monitoring | System state & performance (CPU, RAM, availability) |
| Logs       | Application events (errors, requests)      |
| Security   | Vulnerabilities, attacks                   |

> Monitoring complements logs and security.

---

## 🧱 Monitoring Stack Overview

### Prometheus
- Collects and stores metrics  
- Provides a query language (PromQL)  
- Scrapes metrics from Node Exporter and cAdvisor  

### Node Exporter
- Monitors **Linux host system**  
- Metrics: CPU, RAM, Disk, Network  
- Helps identify if issues come from the server

### cAdvisor
- Monitors **Docker containers**  
- Metrics: CPU, RAM, I/O, container restarts  
- Helps identify which container causes issues

### Grafana
- Visualizes metrics in **dashboards**  
- Provides **real-time and historical analysis**  
- Enables sharing insights with teams

---

## 🖼️ Monitoring Architecture Diagram

![Prometheus & Grafana Monitoring](https://devopscube.com/content/images/2025/03/prometheus-architecture.gif "Prometheus & Grafana Monitoring")

*Diagram showing the Prometheus monitoring stack: exporters, scraping, and Grafana for visualization.*  
Source: Wikimedia Commons


---

## ⚙️ Deploying the Monitoring Stack with Docker Compose

```yaml
version: '3'
services:
  prometheus:
    image: prom/prometheus:latest
    container_name: monitoring_prometheus
    ports:
      - 9090:9090
    volumes:
      - ./prometheus.yml:/etc/prometheus/prometheus.yml

  node-exporter:
    image: prom/node-exporter:latest
    container_name: monitoring_node_exporter
    expose:
      - 9100

  cadvisor:
    image: gcr.io/cadvisor/cadvisor:latest
    container_name: monitoring_cadvisor
    expose:
      - 8080

  grafana:
    image: grafana/grafana:latest
    container_name: monitoring_grafana
    ports:
      - 3006:3000
```


- Access Prometheus: http://localhost:9090

- Access Grafana: http://localhost:3006 (admin/admin)

---

## 🔁 Monitoring in a DevOps Cycle

Code → CI/CD → Deployment → Monitoring → Alerts → Continuous Improvement

Without monitoring, DevOps is incomplete.

---

## 📌 Summary

Monitor host and containers

Detect incidents quickly

Visualize metrics clearly in Grafana dashboards

Stack is open-source, scalable, and standard

➡️ Next step in learning:

`resources/resources.md` → Free resources, courses, and guides for DevOps students
