# 👋 Hi, I'm Frank | Security & DevSecOps Engineer

I specialize in building **Hardened Infrastructure** and **Automated Security Pipelines**. I bridge the gap between development and operations by "Shifting Security Left"—integrating automated audits into the heart of the CI/CD cycle.

---

## 🛡️ Automated Security Posture
This repository is actively monitored and hardened using GitHub’s Advanced Security suite:
* **SAST (Static Analysis)**: Automated code auditing via **CodeQL** and **Checkov** to catch vulnerabilities before deployment.
* **SCA (Supply Chain)**: Continuous dependency monitoring via **Dependabot** to mitigate CVE risks in third-party libraries.
* **Secret Protection**: Native **Secret Scanning** with Push Protection enabled to prevent credential leakage.
* **Vulnerability Disclosure**: Professional **Security Policy** enabled for responsible disclosure and private reporting.

---

## 🏗️ Featured Security Labs

### 1. [Project-Fortress](https://github.com/chifru19/Project-Fortress) 
**Automated IaC Security & CI/CD Hardening**
* **The Goal**: Build a "Security Gate" that prevents vulnerable infrastructure from being deployed.
* **The Tech**: GitHub Actions, Checkov, Docker, Kubernetes.
* **Key Achievement**: Engineered a pipeline that scans every commit for 50+ security policies, automatically blocking builds that violate "Least Privilege" standards.

### 2. [Network-Guard-Forensics](https://github.com/chifru19/Network-Guard-Forensics)
**Active Defense & Zero-Trust Networking**
* **The Goal**: Create a decoy environment to log attacker behavior while isolating sensitive data.
* **The Tech**: Cowrie Honeypot, Docker Internal Networks, Linux Forensics.
* **Key Achievement**: Implemented a Zero-Trust network architecture where the public-facing honeypot has zero connectivity to the private database subnet.

---

## 🧠 Lessons Learned (The "Hardening" Journey)

Building these labs required overcoming real-world configuration challenges. Here are my key takeaways:

### 1. Shifting Security Left
Initially, my pipeline failed due to **CKV_DOCKER_3** (Root user) violations. 
* **The Fix**: I learned to rewrite Dockerfiles to create non-privileged users and implement granular resource limits.
* **The Lesson**: Security isn't a "final step"—it must be baked into the initial configuration.

### 2. Architecture over Obscurity
While working on network isolation, I moved to a **Zero-Trust model**.
* **The Fix**: Used Docker's `internal: true` flag to ensure the database layer is physically unreachable from the outside world.
* **The Lesson**: Robust network segmentation is superior to simple perimeter defense.

---

## 🛠️ Technical Toolkit
* **Security Tools**: CodeQL, Checkov, SAST, Honeypots (Cowrie)
* **Orchestration**: Docker, Kubernetes (K8s)
* **Automation**: GitHub Actions (CI/CD)
* **Infrastructure**: Terraform, YAML, Linux Shell
