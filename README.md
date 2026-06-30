# Data Center Monitoring System

A production-grade distributed monitoring platform built for Oracle RAC environments, providing real-time infrastructure health monitoring, Oracle cluster monitoring, KPI tracking, log analysis, and automated alerting.

## Scale

- 9 Data Centers
- 300+ Oracle RAC Clusters
- 1200+ RAC Nodes
- Minimum 4 nodes per cluster
- Node health monitoring every 30 seconds
- KPI collection every 20 minutes
- Lightweight agent-based architecture with minimal system overhead

---

## Tech Stack

### Agent — Golang
Deployed on every Oracle RAC node.

**Responsibilities:**
- Node health monitoring
- CPU utilization monitoring
- Memory monitoring
- Disk space monitoring
- Node availability checks
- Oracle RAC component status collection
- Log collection and analysis

---

### Backend - Node.js
**Handles:**
- High-frequency agent communication
- Real-time health ingestion
- Monitoring APIs
- Alert processing
- Data processing workflows

---

### Frontend - React.js
**Provides:**
- Centralized monitoring dashboard
- Data center overview
- RAC cluster health view
- Node status visualization
- KPI dashboards
- Alert history
- Log analysis view

---

### Database - MySQL
**Stores:**
- Data center inventory
- Cluster configuration
- Node information
- Monitoring configuration
- Alert history
- System events

---

### Cache/Sessions - Redis
**Used for:**
- Real-time node heartbeat tracking
- Latest health status caching
- Fast dashboard response
- Reducing database load

---


## Key Features
### Cluster Health Monitoring
**Monitors:**
- Oracle High Availability Services (OHAS)
- Cluster Ready Services (CRS)
- RAC node status
- Database instance status
- Listener status
- ASM status
- Cluster resources

---

### Infrastructure Monitoring
**Tracks:**
- CPU utilization
- Memory usage
- Disk space utilization
- Node availability
- System health

**Alerts generated when:**
- CPU exceeds threshold
- Disk usage exceeds 80%
- Node becomes unavailable
- Critical service goes down

---

### KPI Monitoring
**Collects Oracle performance indicators:**
- Database status
- Instance availability
- RAC health metrics
- System performance metrics
- Resource utilization
- Wait events

---

### Log Monitoring & Analysis
**Monitors Oracle logs:**
- Database Alert Logs
- ASM Logs
- CRS Logs
- Clusterware Logs

**Detects:**
- Database failures
- Cluster issues
- ASM problems
- Listener failures
- Oracle critical errors

---

### Alerting System
Automatically sends alerts to Oracle DBA teams through email.
**Alert scenarios:**
- RAC node down
- Database instance unavailable
- CRS/OHAS failure
- Listener failure
- ASM issue
- Disk space threshold breach
- Critical Oracle errors detected in logs

---
## Key Features
- Multi data center monitoring  
- 1200+ node real-time visibility  
- Oracle RAC cluster monitoring  
- Automated log analysis  
- KPI monitoring  
- Disk and infrastructure monitoring  
- Agent-based scalable architecture  
- Centralized dashboard  
- Automated DBA alert notification

## Business Impact
- Reduced manual RAC health checks
- Faster incident detection
- Proactive Oracle issue identification
- Centralized visibility across multiple data centers

## Problem I solved
Distributed monitoring across 1,200+ nodes created high-frequency data ingestion challenges. Implemented Redis in-memory store to handle 1,200+ heartbeats every 30 seconds without Disk I/O bottleneck, ensuring zero data loss and real-time alerting.
