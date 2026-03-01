# 👋 Hi, I'm Frank | Security & DevSecOps Engineer

I specialize in building **Hardened Infrastructure** and **Automated Security Pipelines**. I bridge the gap between development and operations by "Shifting Security Left"—integrating automated audits into the heart of the CI/CD cycle to ensure only production-ready, secure code is deployed.

---

## 🛡️ Automated Security Posture
This repository is hardened using GitHub’s Advanced Security suite and industry-standard IaC auditing tools:
* **SAST (Static Analysis)**: Continuous code auditing via **CodeQL** and **Checkov** to catch vulnerabilities and misconfigurations in real-time.
* **SCA (Supply Chain)**: Dependency monitoring via **Dependabot** to proactively mitigate CVE risks in third-party libraries.
* **Secret Protection**: Native **Secret Scanning** with Push Protection enabled to prevent credential leakage.
* **Vulnerability Disclosure**: Professional **Security Policy** implemented for responsible disclosure and private reporting.

---

## 🏗️ Featured Security Labs

### 1. [Project-Fortress](https://github.com/chifru19/Project-Fortress) 
**Automated IaC Security & CI/CD Hardening**
* **Goal**: Build an automated "Security Gate" to prevent insecure deployment.
* **Tech**: GitHub Actions, Checkov, Docker, Kubernetes.
* **Success**: Successfully engineered a pipeline that scans every commit for 50+ security policies, automatically blocking builds that violate "Least Privilege" or resource sandboxing standards.

### 2. [Network-Guard-Forensics](https://github.com/chifru19/Network-Guard-Forensics)
**Active Defense & Zero-Trust Networking**
* **Goal**: Create a decoy environment to log attacker behavior while isolating sensitive data subnets.
* **Tech**: Cowrie Honeypot, Docker Internal Networks, Linux Forensics.
* **Success**: Implemented a Zero-Trust network architecture where public-facing honeypots are physically isolated from private database subnets via internal network flags.

---

## 🧠 Lessons Learned (The "Hardening" Journey)

### 1. The Reality of DevSecOps Integration
Initially, my security workflows encountered failures (Red X) due to strict policy enforcement, such as **CKV_DOCKER_3** (Root user violations). 
* **The Fix**: I learned to rewrite Dockerfiles to enforce non-root execution and established granular memory limits (128MB) to prevent DoS attacks.
* **The Lesson**: Security is an iterative process; a "Failed" build is actually a success for the security gate.

### 2. Architecture over Obscurity
While working on network isolation, I moved beyond simple firewalls to a **Zero-Trust model**.
* **The Fix**: Used Docker's `internal: true` network flag to ensure the database layer is physically unreachable from the public internet.
* **The Lesson**: Robust network segmentation is the most effective way to prevent lateral movement after a breach.

---

## 🛠️ Technical Toolkit
* **Security Tools**: CodeQL, Checkov, SAST, Honeypots (Cowrie)
* **Orchestration**: Docker, Kubernetes (K8s)
* **Automation**: GitHub Actions (CI/CD)
* **Infrastructure**: Terraform, YAML, Linux Shell
