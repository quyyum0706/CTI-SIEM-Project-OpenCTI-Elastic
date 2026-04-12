# CTI-SIEM-Project-OpenCTI-Elastic
Cyber Threat Intelligence Platform using OpenCTI, MISP, Elastic Stack and SOAR automation
# 🔐 CTI-SIEM Platform (OpenCTI + Elastic Stack)

## 📖 Overview
This project implements a **Cyber Threat Intelligence (CTI) Platform** designed for a fintech environment.

The system integrates:
- OpenCTI (Threat Intelligence Platform)
- MISP (Threat Sharing)
- Elastic Stack (SIEM)
- Cortex XSOAR (SOAR Automation)

It enables **real-time threat detection, intelligence enrichment, and automated incident response**.

---

## 🧱 Architecture

![Architecture](screenshots/architecture.png)

### 🔄 Intelligence Flow
Threat Feeds → OpenCTI → IOC Enrichment → Logstash → Elasticsearch → Detection Rules → Alerts → SOAR → Automated Response

---

## ⚙️ Technologies Used

- OpenCTI
- MISP
- Elastic Stack (Elasticsearch, Logstash, Kibana)
- Cortex XSOAR
- Kali Linux (Attack Simulation)
- Docker

---

## 🎯 Key Features

- ✅ Aggregation of threat intelligence from multiple sources
- ✅ MITRE ATT&CK mapping for all detected threats
- ✅ Real-time detection using Elastic SIEM
- ✅ Automated response using SOAR playbooks
- ✅ Centralized dashboard for monitoring threats

---

## 🧪 Attack Simulation

The following attacks were simulated using Kali Linux:

- 🔹 Brute Force Attack (Hydra)
- 🔹 Malicious IP Communication
- 🔹 Phishing Domain Detection

All attacks were successfully detected in **Elastic SIEM dashboards**.

---

## 🔍 Detection Engineering

Custom detection rules were created in Elastic SIEM:

| Scenario                  | MITRE Technique | Severity |
|--------------------------|---------------|----------|
| Malicious IP Connection  | T1071         | Critical |
| Phishing Domain          | T1566         | High     |
| Brute Force Attack       | T1110         | High     |
| Ransomware Pattern       | T1486         | Critical |

---

## 📊 Results

- 🚀 Reduced detection time to **< 5 minutes**
- 🤖 Automated response for **80% of incidents**
- 🌐 Integrated **8+ threat intelligence feeds**
- 📈 Improved SOC visibility and alert correlation

---

## 📂 Project Structure

