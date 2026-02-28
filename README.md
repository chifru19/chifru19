# 👋 Hi, I'm Frank | Security & DevSecOps Engineer

I specialize in building **Hardened Infrastructure** and **Automated Security Pipelines**. I bridge the gap between development and operations by "Shifting Security Left"—integrating automated audits into the heart of the CI/CD cycle.

---

## 🛡️ Featured Security Labs

### 1. [Project-Fortress](https://github.com/chifru19/Project-Fortress) 
**Automated IaC Security & CI/CD Hardening**
* **The Goal**: Build a "Security Gate" that prevents vulnerable infrastructure from being deployed.
* **The Tech**: GitHub Actions, Checkov, Docker, Kubernetes.
* **Key Achievement**: Successfully engineered a pipeline that scans every commit for 50+ security policies, automatically blocking builds that violate "Least Privilege" standards.

### 2. [Network-Guard-Forensics](https://github.com/chifru19/Network-Guard-Forensics)
**Active Defense & Zero-Trust Networking**
* **The Goal**: Create a decoy environment to log attacker behavior while isolating sensitive data.
* **The Tech**: Cowrie Honeypot, Docker Internal Networks, Linux Forensics.
* **Key Achievement**: Implemented a Zero-Trust network architecture where the public-facing honeypot has zero connectivity to the private database subnet.

---

## 🧠 Lessons Learned (The "Hardening" Journey)

Building these labs wasn't just about writing code; it was about overcoming real-world security configuration challenges. Here are my key takeaways:

### 1. Shifting Security Left is a Process
Initially, my pipeline failed frequently due to **CKV_DOCKER_3** (Root user) and **CKV_DOCKER_2** (Healthcheck) violations. 
* **The Fix**: I learned to rewrite Dockerfiles to create non-privileged users and implement granular resource limits.
* **The Lesson**: Security isn't a "final step"—it must be baked into the initial configuration to avoid massive rework later.

### 2. The Power of "Stop-the-Line" Automation
I intentionally triggered pipeline failures to test my "Security Gate." 
* **The Result**: I witnessed how **Checkov** caught a hardcoded secret before it could be pushed to the repository.
* **The Lesson**: Automated enforcement is the only way to maintain a consistent security posture at scale.

### 3. Architecture over Obscurity
While working on network isolation, I realized that hidden ports aren't enough. 
* **The Fix**: I moved to a **Zero-Trust model**, using Docker's `internal: true` flag to ensure the database layer is physically unreachable from the outside world.
* **The Lesson**: Robust architecture (segmentation) is superior to simple perimeter defense.

---

## 🛠️ Technical Toolkit
* **Security Tools**: Checkov, SAST, Honeypots (Cowrie)
* **Orchestration**: Docker, Kubernetes (K8s)
* **Automation**: GitHub Actions (CI/CD)
* **Infrastructure**: Terraform, YAML, Linux Shell
