# System Architecture (Unified)

## Overview
DevOps Simulator follows a **microservices architecture** designed for high availability, scalability, and flexibility.  
It supports both **stable (production & development)** and **experimental (AI-enhanced, multi-cloud)** configurations.

---

## 🧩 Core Components

### 1. Application Server
| Environment | Technology | Port(s) | Key Features |
|--------------|-------------|----------|---------------|
| **Production** | Node.js + Express | 8080 | Horizontal auto-scaling, SSL/TLS, zero-downtime rolling updates |
| **Development** | Node.js + Express | 3000 | Hot reload, debug mode, instant feedback |
| **Experimental** | Node.js + Express + TensorFlow.js | 9000 (main), 9001 (metrics), 9002 (AI API) | AI-powered predictive scaling, ML inference, Kafka event streaming |

---

### 2. Database Layer
| Environment | Type | Configuration | Notes |
|--------------|------|----------------|-------|
| **Production** | PostgreSQL 14 | Master-slave replication, automated backups | High reliability |
| **Development** | Local PostgreSQL | Single instance with seed data | Simplified for local testing |
| **Experimental** | Distributed PostgreSQL cluster (5 nodes) | Multi-master replication, continuous backup, geo-redundancy | AI-driven query optimization, Redis caching |

---

### 3. Monitoring & Observability
| Environment | Tools | Features |
|--------------|--------|-----------|
| **Production** | Prometheus + Grafana | Metrics visualization, email alerts |
| **Development** | Console logging | Verbose output for debugging |
| **Experimental** | Prometheus + Thanos + ELK Stack | AI log analysis, anomaly detection, predictive alerts |

---

### 4. AI/ML Pipeline (Experimental)
- **Frameworks**: TensorFlow, PyTorch, Scikit-learn  
- **Models**:
  - Anomaly detection (LSTM)
  - Load prediction (XGBoost)
  - Auto-scaling optimizer (Reinforcement Learning)
- **Training**: Continuous online learning  
- **Inference**: Real-time (<50ms latency)

---

### 5. Deployment Strategy
| Environment | Method | Highlights |
|--------------|----------|-------------|
| **Production** | Rolling updates | Zero downtime, automated rollback |
| **Development** | Docker Compose | Rapid iteration with hot reload |
| **Experimental** | Kubernetes (multi-cloud) | GeoDNS load balancing, cross-cloud failover |

---

### 6. Security
| Environment | Security Level | Description |
|--------------|----------------|-------------|
| **Production** | High | SSL/TLS encryption, strict access control |
| **Development** | Moderate | Relaxed for debugging convenience |
| **Experimental** | Enhanced | AI-driven anomaly detection, behavioral firewalling |

---

### 🧠 Summary
- **Production & Development**: Stable, well-tested environments.  
- **Experimental Build**: Cutting-edge AI/ML and multi-cloud integrations — use for R&D, not live systems.

---

✅ *Conflict resolved — combines both HEAD and experimental documentation cleanly.*
