# 🛡️ Sentinel Fortress | Splunk SOC Lab

[![Security Scan](https://img.shields.io/github/actions/workflow/status/chifru19/splunk-soc-lab/codeql.yml?branch=main&label=Security%20Scan&logo=github)](https://github.com/chifru19/splunk-soc-lab/actions)
[![NIST Compliance](https://img.shields.io/badge/Compliance-NIST%20CSF%202.0-blue)](https://www.nist.gov/cyberframework)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📖 Executive Summary
**Sentinel Fortress** is a production-grade SIEM and SOC laboratory engineered for active defensive monitoring. This project bridges the gap between infrastructure deployment and security operations, utilizing a containerized architecture to stream real-time telemetry into a centralized Splunk environment.

Designed for resilience, this lab validates security controls against automated adversarial simulations and provides high-fidelity detection for unauthorized access attempts.

---

## 🏗️ Technical Architecture
The infrastructure is built on a modular, containerized stack:

* **Centralized SIEM:** Splunk Enterprise (Custom field extraction & correlation).
* **Logging Pipeline:** Docker logging drivers streaming container telemetry directly to Splunk HEC.
* **Attack Simulation:** Custom Python-based adversarial scripts (Brute Force/SQLi).
* **Security Scanning:** GitHub Actions CI/CD pipeline integrated with secret scanning.

---

## 🕵️‍♂️ Detection in Action: Threat Hunting
This lab is currently operational and actively monitoring traffic. Below is the validated detection logic for unauthorized access attempts captured in the `web_logs` index.

### Detection Case: Brute Force Attempt
**Scenario:** An adversarial script attempted to bypass authentication via multiple `401 Unauthorized` status codes.

**SPL Detection Logic:**
```splunk
index="web_logs" status="401" user="admin"
| timechart count span=1m as Failed_Login_Attempts
| sort - Failed_Login_Attempts