
# 🔥 FireOps — SIEM & Intrusion Detection Lab

**Team B | Cybersecurity Internship Project**  
**Focus Area:** Network Security Monitoring & Attack Detection  
**Date:** February 21, 2026

---

## Abstract

This project presents the deployment and configuration of a Security Information and Event Management (SIEM) system using **Wazuh** integrated with **Suricata IDS**. The objective was to build a functional security monitoring lab capable of:

- Detecting brute force attacks
- Monitoring file integrity changes
- Analyzing security events in real time

The lab environment was implemented using virtual machines in a controlled setting.

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Project Objectives](#2-project-objectives)
3. [Lab Architecture & Environment Setup](#3-lab-architecture--environment-setup)
4. [Tools and Technologies Used](#4-tools-and-technologies-used)
5. [Installation and Configuration](#5-installation-and-configuration)
6. [Azure Activity — VM Deallocation](#6-azure-activity--vm-deallocation)
7. [Suricata Integration with Wazuh](#7-suricata-integration-with-wazuh)
8. [Brute Force Attack Simulation](#8-brute-force-attack-simulation)
9. [Alert Monitoring and Log Analysis](#9-alert-monitoring-and-log-analysis)
10. [Security Findings](#10-security-findings)
11. [Challenges Encountered](#11-challenges-encountered)
12. [Lessons Learned](#12-lessons-learned)
13. [Conclusion](#13-conclusion)

---

## 1. Introduction

This project demonstrates the practical implementation of a SIEM system for detecting and analyzing cyber threats within a virtual lab environment. The focus was on real-time log monitoring, intrusion detection, and attack simulation.

---

## 2. Project Objectives

- Deploy and configure **Wazuh SIEM**
- Install and integrate **Suricata IDS**
- Enable **File Integrity Monitoring (FIM)**
- Simulate brute force attacks using **Kali Linux**
- Analyze generated alerts in the **Wazuh dashboard**

---

## 3. Lab Architecture & Environment Setup

The lab environment consisted of multiple virtual machines:

| Role | OS |
|------|----|
| Wazuh Manager | Ubuntu Server |
| Ubuntu Agent | Ubuntu |
| Target Machine | Windows 10 |
| Attacker Machine | Kali Linux |

---

## 4. Tools and Technologies Used

| Tool | Purpose |
|------|---------|
| VirtualBox | Virtualization platform |
| Wazuh SIEM | Log management & alerting |
| Suricata IDS | Network intrusion detection |
| Kali Linux | Attack simulation |
| Ubuntu Server | Agent & manager hosting |
| Windows 10 | Target endpoint |

---

## 5. Installation and Configuration

### Install Wazuh

```bash
curl -sO https://packages.wazuh.com && sudo bash ./wazuh-install.sh -a
```

### Install Suricata (Ubuntu/Debian)

```bash
sudo add-apt-repository ppa:oisf/suricata-stable
sudo apt update && sudo apt install suricata -y
```

### Install Wazuh Agent

```bash
WAZUH_MANAGER="10.0.2.5" apt-get install wazuh-agent

sudo systemctl daemon-reload
sudo systemctl enable wazuh-agent
sudo systemctl start wazuh-agent
```

---

## 6. Azure Activity — VM Deallocation

Azure Activity Logs were reviewed to monitor VM deallocation events. These logs provided insight into infrastructure-level changes that could correlate with security incidents.

---

## 7. Suricata Integration with Wazuh

Suricata was configured to generate logs in **JSON format (`eve.json`)**, which were integrated into Wazuh for centralized monitoring and alert generation.

Key configuration steps:
- Set Suricata output to `eve.json`
- Point Wazuh to read the Suricata log file
- Verify alert forwarding in the Wazuh dashboard

---

## 8. Brute Force Attack Simulation

A brute force attack was simulated from **Kali Linux** targeting the victim machine. The objective was to trigger authentication failure alerts in Wazuh and verify end-to-end detection.

---

## 9. Alert Monitoring and Log Analysis

Security alerts were analyzed based on severity levels:

| Level | Description |
|-------|-------------|
| 🔴 Critical | Immediate threat requiring action |
| 🟠 High | Significant suspicious activity |
| 🟡 Medium | Moderate risk indicators |
| 🟢 Low | Informational events |

Logs were reviewed to identify attack patterns and suspicious behavior across all monitored endpoints.

---

## 10. Security Findings

The SIEM system successfully detected:

- ✅ Brute force login attempts
- ✅ File integrity violations
- ✅ Suspicious network traffic patterns (via Suricata)

---

## 11. Challenges Encountered

- Suricata logs not appearing in the dashboard (resolved via JSON config fix)
- Agent disconnection troubleshooting
- JSON log configuration errors

---

## 12. Lessons Learned

This project enhanced practical knowledge in:

- SIEM deployment and configuration
- IDS (Suricata) setup and integration
- Log analysis and correlation
- Incident detection techniques
- Virtual lab environment management

---

## 13. Conclusion

The successful deployment of **Wazuh** and **Suricata** demonstrates the effectiveness of SIEM solutions in monitoring, detecting, and analyzing cybersecurity threats in real time. This lab serves as a foundation for building more advanced security operations capabilities.

---

## Team

**Team B** — Cybersecurity Internship, 2026
