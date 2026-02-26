<<<<<<< HEAD
# 🔴 Modern SOC Lab
=======
# 🔴Modern-SOC-LAB
This is a Project Designed for Security Analysts and all SOC audiences who wants to play with implementation and explore the Modern SOC architecture. All of the componenets are used based on Open Source Projects(Availabe at the time of first commit). 
>>>>>>> af1939888279898ae7e8eae99c618b2d9ee66d57

![Status](https://img.shields.io/badge/status-Ongoing-orange)
![License](https://img.shields.io/badge/license-Open%20Source-brightgreen)
![Cloud](https://img.shields.io/badge/Cloud-Vultr-007BFC)
![SIEM](https://img.shields.io/badge/SIEM-Elastic%20Stack-005571?logo=elastic)

A fully open-source Security Operations Center (SOC) lab designed for security analysts and SOC practitioners who want to explore, implement, and experiment with a modern SOC architecture — from log collection and normalization all the way through automated threat response.

<<<<<<< HEAD
> ⚠️ **This is an ongoing project. The repository will be updated as new components and phases are added.**
=======
# 📑Index:
 - [Architecture Diagram](#Architecture-Diagram)
 - [Components used in this Project](#Components)
 - [Installation Requirements](#Installation-Requirements)
 - [Installation Guide First Phase](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/install1.md)
 - [Installation Guide Second Phase](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/install2.md)
 - [Installation Guide Beats Agent](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/beats.md)
 - [Shuffle Automation Install Guide](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/Shuffle-install.md)
 - [Integration Guide First Phase](https://github.com/Darvin697/Modern-SOC-Project/blob/main/integration/integration.md)
 - [Shuffle Workflow Implementation](#Shuffle-Workflow-Implementation)
 - [Elastic EDR Implementation](#EDR-Implementation)
 
 
>>>>>>> af1939888279898ae7e8eae99c618b2d9ee66d57

---

## 🎯 What This Lab Covers

- **Collect** logs and security data into a single centralized platform
- **Normalize and parse** data for consistent analysis
- **Visualize** data and build meaningful security analytics dashboards
- **Create incidents and cases** from security alerts automatically
- **Automate** threat hunting, playbook execution, and SOC data analytics
- **Analyze observables** (IPs, hashes, domains) at scale from a single interface
- **Actively respond** to threats and coordinate with other teams
- **Enrich** alerts with open-source threat intelligence

---

## 📑 Index

- [Architecture Diagram](#architecture-diagram)
- [Components](#components)
- [Installation Requirements](#installation-requirements)
- [Installation Guide — Phase 1](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/install1.md)
- [Installation Guide — Phase 2](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/install2.md)
- [Installation Guide — Beats Agent](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/beats.md)
- [Shuffle Automation Install Guide](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/Shuffle-install.md)
- [Integration Guide — Phase 1](https://github.com/Darvin697/Modern-SOC-Project/blob/main/integration/integration.md)
- [Shuffle Workflow Implementation](#shuffle-workflow-implementation)
- [Elastic EDR Implementation](#edr-implementation)

---

## 🏗️ Architecture Diagram

<p align="center"><img src="images/simpler-soc.png" alt="SOC Architecture Diagram"></p>

---

## ⚙️ Components

### Phase 1 — Core SOC Stack

All components used in this project are open source.

| Component | Description |
|---|---|
| **Elastic SIEM** | Core SIEM platform powered by Elasticsearch, Logstash, and Kibana |
| **TheHive** | Scalable, open-source Security Incident Response Platform for SOCs, CSIRTs, and CERTs — [GitHub](https://github.com/TheHive-Project/TheHive) |
| **Cortex** | Observable analysis engine — analyze IPs, URLs, hashes, domains one-by-one or in bulk via API — [GitHub](https://github.com/TheHive-Project/Cortex) |
| **MISP** | Open-source threat intelligence platform for collecting, storing, and sharing cybersecurity indicators — [GitHub](https://github.com/MISP/MISP) |

### Phase 2 — Extended Detection & Deception

| Component | Description |
|---|---|
| **Snort** | Leading open-source Intrusion Prevention System (IPS) — [snort.org](https://www.snort.org/) |
| **Wazuh** | Open-source host security monitoring and log analysis — [wazuh.com](https://wazuh.com/) |
| **Dionaea** | Honeypot designed to trap malware exploiting exposed services — [docs](https://dionaea.readthedocs.io/en/latest/) |
| **Jupyter Notebook** | Interactive computing platform for security analytics and data exploration — [jupyter.org](https://jupyter.org/) |
| **IntelOwl** | OSINT platform to retrieve threat intelligence data on files, IPs, and domains from a single API — [intelowlproject.github.io](https://intelowlproject.github.io/) |
| **Atomic Red Team** | Library of adversary simulation tests mapped to MITRE ATT&CK — [GitHub](https://github.com/redcanaryco/atomic-red-team) |
| **Shuffle** | Open-source SOAR platform for orchestrating security tool workflows — [shuffler.io](https://shuffler.io/) |
| **Twitter TI Bot** | Custom bot to collect threat intelligence from Twitter/X — [Watch Episode](https://youtu.be/onklNNJcfDU) |

### Phase 3 — Endpoint Detection & Response

| Component | Description |
|---|---|
| **Elastic EDR** | Free and open endpoint security — prevents ransomware, detects advanced threats, and arms responders with context — [elastic.co](https://www.elastic.co/endpoint-security/) |

---

## 🔀 Shuffle SOAR Workflow

<p align="center"><img src="images/shuffle-workflow.PNG" alt="Shuffle Workflow Diagram"></p>

To use the Shuffle workflow:
1. Follow the [Shuffle installation guide](https://github.com/Darvin697/Modern-SOC-Project/blob/main/installation/Shuffle-install.md)
2. Once your Shuffle instance is running, watch the full walkthrough video [HERE](https://youtu.be/Nb9_ahZMC5U)

---

## 🛡️ EDR Implementation

<p align="center"><img src="images/Part3.png" alt="EDR Architecture"></p>

To deploy Elastic EDR:
1. Follow the installation guide from the [Index](#index)
2. Once your Elastic instance is running, watch the full walkthrough video [HERE](https://youtu.be/fXLsY_eZoeE)

---

## 🔽 Installation Requirements

The lab environment was built on **Vultr Cloud**. You can follow along on Vultr or use any alternative cloud provider. EKS can also be used to deploy the full setup.

### VM Specifications

| VM | OS | Instance Type | Notes |
|---|---|---|---|
| Elastic SIEM | Ubuntu 20.04 | t2.medium | t2.large recommended for best performance |
| TheHive | Ubuntu 20.04 | t2.medium | |
| Cortex | Ubuntu 20.04 | t3a.medium | t2.medium also works |
| MISP | Ubuntu 20.04 | t3.micro | |

### Network / Firewall Rules

| Port | Source | Purpose |
|---|---|---|
| 22 | Your IP | SSH access to VMs |
| 443 | Your IP | MISP web UI |
| 9200 | Your IP | Elasticsearch API |
| 5601 | Your IP | Kibana web UI |
| 9001 | Your IP | Cortex web UI |
| 9000 | Your IP | TheHive web UI |
| All TCP | Cortex VM IP | Inbound API access |
| All TCP | MISP VM IP | Inbound API access |
| All TCP | TheHive VM IP | Inbound API access |

---

## 📚 Key Skills Demonstrated

- Open-source SIEM deployment and configuration
- Security incident case management with TheHive
- Observable enrichment and analysis with Cortex
- Threat intelligence management with MISP
- SOAR workflow automation with Shuffle
- Intrusion detection with Snort and Wazuh
- Endpoint detection and response with Elastic EDR
- Adversary simulation using Atomic Red Team (MITRE ATT&CK)
