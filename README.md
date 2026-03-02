# 🛡️ Frank | DevSecOps & Security Infrastructure Engineer

![Security Scan](https://github.com/chifru19/chifru19/actions/workflows/codeql.yml/badge.svg)
![Dependabot Status](https://img.shields.io/badge/Dependabot-Active-brightgreen)

I specialize in engineering **Hardened Infrastructure** and **Automated Security Pipelines**. I bridge the gap between development and operations by "Shifting Security Left"—integrating automated audits into the heart of the CI/CD cycle to ensure only production-ready, secure code is deployed.

---

## 🛡️ Automated Security Posture
This repository is a live demonstration of a hardened environment using GitHub’s Advanced Security suite and industry-standard **IaC** auditing tools:

* **SAST (Static Analysis)**: Continuous application auditing via **CodeQL** and infrastructure-as-code scanning via **Checkov**.
* **SCA (Supply Chain)**: Proactive dependency monitoring via **Dependabot** to mitigate CVE risks in Python and YAML libraries.
* **Secret Protection**: Native **Secret Scanning** with Push Protection enabled to prevent credential leakage.
* **K8s Orchestration**: Verified secure **Kubernetes** manifests featuring resource sandboxing and non-root execution.



---

## 🏗️ Featured Security Labs

### 1. Project-Fortress: Automated IaC Security & CI/CD Hardening
* **Success**: Engineered a pipeline that scans every commit for 50+ security policies, automatically blocking builds that violate "Least Privilege" or resource limits.
* **Verification**: Successfully implemented a hardened `deployment.yaml` that passed all **Checkov** security gates for Kubernetes orchestration.

### 2. Network-Guard-Forensics: Active Defense & Zero-Trust Networking
* **Success**: Implemented a **Zero-Trust** network architecture where public-facing **Cowrie Honeypots** are physically isolated from private database subnets.
* **Network Isolation**: Used Docker's `internal: true` network flag to ensure the database layer is unreachable from the public internet, preventing lateral movement.



---

## 🧠 Lessons Learned (The "Hardening" Journey)

### 1. Remediation over Detection
* **The Challenge**: My automated scanner flagged a high-severity risk: "Ensure top-level permissions are not set to write-all".
* **The Fix**: Applied the **Principle of Least Privilege** by restricting GitHub Token scopes to `contents: read` and `security-events: write`.
* **The Lesson**: Identifying a risk is only half the battle; real security lies in the engineering required to remediate it.

### 2. Infrastructure Sandboxing
* **The Challenge**: Initial Docker builds failed policy `CKV_DOCKER_3` (Root user violations).
* **The Fix**: Rewrote Dockerfiles to enforce non-root execution and established 128MB RAM limits to prevent DoS attacks.

---

## 🛠️ Technical Toolkit
* **Security Tools**: CodeQL, Checkov, SAST, SCA, Honeypots (Cowrie).
* **Orchestration**: Docker, Kubernetes (K8s).
* **Automation**: GitHub Actions (CI/CD), YAML, Linux Shell.
