# 👋 Hi, I'm Frank | Security & DevSecOps Engineer

```mermaid
graph TD
    subgraph "Local Environment"
        A[VS Code / Mac] -->|Git Push| B(GitHub Repository)
    end

    subgraph "CI/CD Security Gate (GitHub Actions)"
        B --> C{Checkov Audit}
        C -->|Fail: Red X| D[Block Deployment]
        C -->|Pass: Green Check| E[Approve Build]
    end

    subgraph "Hardened Infrastructure (Docker/K8s)"
        E --> F[Honeypot: Public-Net]
        E --> G[Secure Database: Private-Net]
        F -.- G{Zero-Trust Gap}
    end
### 1. [Network-Guard-Forensics](https://github.com/chifru19/Network-Guard-Forensics)
**Focus:** Cloud Auditing & Container Hardening
* **Key Achievement**: Successfully remediated `CKV_DOCKER_3` by implementing non-root user execution and established a "Stop-the-Line" CI/CD security gate.
* **Tech Stack**: Python, Docker, Boto3, GitHub Actions, Checkov.
[![Security Scan](https://github.com/chifru19/Network-Guard-Forensics/actions/workflows/main.yml/badge.svg)](https://github.com/chifru19/Network-Guard-Forensics/actions)
### 2. [Project-Fortress](https://github.com/chifru19/Project-Fortress)
**Focus:** Active Defense & Network Isolation
* **Key Achievement**: Engineered a 3-tier secure network with internal database isolation and enforced **Resource Sandboxing** (128MB RAM limits) to mitigate DoS attacks.
* **Tech Stack**: Docker Compose, Kubernetes, Alpine Linux, Shell Scripting.
[![Security Scan](https://github.com/chifru19/Project-Fortress/actions/workflows/security-scan.yml/badge.svg)](https://github.com/chifru19/Project-Fortress/actions)
---

## 🛠️ Technical Toolkit
* **Security Tools**: Checkov (IaC Scanning), Docker Scout, Nmap, Wireshark.
* **Cloud & DevOps**: GitHub Actions (CI/CD), AWS S3, Terraform, Kubernetes.

<!--
**chifru19/chifru19** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
