# 🛡️ Frank | DevSecOps & Security Infrastructure Engineer

![Security Scan](https://github.com/chifru19/chifru19/actions/workflows/codeql.yml/badge.svg)
![Dependabot Status](https://img.shields.io/badge/Dependabot-Active-brightgreen)

I specialize in engineering **Hardened Infrastructure** and **Automated Security Pipelines**. I bridge the gap between development and operations by "Shifting Security Left"—integrating automated audits into the heart of the CI/CD cycle.

---

## 🏗️ Featured Security Labs & Project Links

### 📂 [1. Project-Fortress (Automated IaC Security)](https://github.com/chifru19/chifru19/tree/main/.github/workflows)
* **Objective**: Engineering a "Security Gate" that scans every commit for 50+ security policies.
* **Verification**: Successfully implemented a hardened `deployment.yaml` that passed all **Checkov** gates for Kubernetes orchestration.

### 📂 [2. Network-Guard-Forensics (Zero-Trust Architecture)](https://github.com/chifru19/chifru19/blob/main/deployment.yaml)
* **Objective**: Active defense using **Cowrie Honeypots** physically isolated from private database subnets.
* **Result**: Used Docker's `internal: true` flag to eliminate lateral movement risks from the public internet.

---

## 🛡️ Automated Security Posture
This repository is a live demonstration of a hardened environment using:
* **SAST (Static Analysis)**: Infrastructure-as-code scanning via **Checkov**.
* **SCA (Supply Chain)**: Dependency monitoring via **Dependabot**.
* **Secret Protection**: Native **Secret Scanning** with Push Protection enabled.


---

## 🧠 Lessons Learned (The "Hardening" Journey)

### 1. Remediation over Detection
* **Finding**: My scanner flagged a "write-all" permission risk in the workflow.
* **The Fix**: Restricted GitHub Token scopes to `contents: read` and `security-events: write`.

### 2. Infrastructure Sandboxing
* **The Fix**: Rewrote Dockerfiles and K8s manifests to enforce **Non-Root** execution and established 128MB RAM limits to prevent DoS attacks.

---

## 🛠️ Technical Toolkit
* **Security**: CodeQL, Checkov, SAST, SCA, Cowrie Honeypots.
* **Orchestration**: Docker, Kubernetes (K8s).
* **Automation**: GitHub Actions (CI/CD), YAML, Linux Shell.
