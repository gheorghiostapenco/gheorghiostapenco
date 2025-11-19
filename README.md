# Hi, I'm Gheorghi Ostapenco 

![DevOps Engineer | Moldova](https://img.shields.io/badge/DevOps%20Engineer-Moldova%20%F0%9F%87%B2%F0%9F%87%A9-4A90E2?style=for-the-badge&logo=terraform&logoColor=white)
![15+ years in QA/PM → DevOps](https://img.shields.io/badge/Experience-15%2B%20years%20QA%2FPM%20→%20DevOps-2ECC71?style=for-the-badge)

> **From ensuring software quality to automating the systems that deliver it.**

I am a **DevOps Engineer** with a **15-year background** in **QA, Business Analysis, and Project Management**.  
After a long career dedicated to **ensuring software quality (QA)** and **managing delivery processes (PM)**, I have transitioned my focus to **automating the systems that build and deliver that software**.

I've spent the **last two years** in a **deep, hands-on dive** into **DevOps culture and its core technologies**.  
My unique background allows me to see the **"big picture"** — connecting **business requirements** and **quality gates** directly to the **automated infrastructure** that supports them.

> **I don't just build pipelines — I understand *why* they are critical for business success.**

---

## 🛠 Core Technical Competencies

My practical experience is focused on **building and managing the full DevOps lifecycle**:

| Category | Tools & Technologies |
|---------|----------------------|
| ☁️ **Cloud Platforms** | **AWS** (EC2, S3, VPC, IAM, CloudWatch), **DigitalOcean** |**GCP**
| 🛠 **Infrastructure as Code (IaC)** | **Terraform** (modules, state backends, remote execution, multi-env) |
| ⚙️ **Configuration Management** | **Ansible** (Playbooks, Roles, Inventory, Ansible Tower basics) |
| 📦 **CI/CD & Containers** | **GitHub Actions**, **Docker**, **Docker Compose**, GitOps workflows |
| 📊 **Load & Performance Testing** | **K6** (scripting, thresholds, distributed testing) |
| 🧩 **Processes & Methodologies** | **Agile**, **Scrum** (`PSM I`, `PSPO I`),`ISTQB Certified Tester` |

---

## 🔭 Current Focus: Full-Stack Automation in Action

I am actively **building and automating real-world projects** to apply these skills.

# Automated Infrastructure Migration Suite: VMware to OpenNebula

**Role:** DevOps Engineer / Toolsmith
**Focus:** Infrastructure Automation, Cost Optimization (FinOps), Virtualization
**Repository:** [[Link](https://github.com/gheorghiostapenco/vm-opennebula-migrator)]

### The Challenge: Escaping the "Broadcom Tax"
Following Broadcom's acquisition of VMware, many enterprises faced a sudden shift from perpetual licenses to costly subscription models (3x–10x cost increases). Organizations needed a way to migrate workloads to open-source alternatives like OpenNebula (KVM) to regain control of their infrastructure budgets.

However, migrating virtual machines between hypervisors is technically complex. It involves incompatible disk formats (VMDK vs. QCOW2), different API endpoints, and high risks of data corruption. Manual migration is unscalable and error-prone.

### The Solution
I engineered a **Python-based CLI automation tool** that orchestrates the end-to-end migration pipeline. It serves as a bridge between proprietary and open-source stacks, treating infrastructure migration as a reliable, repeatable software process rather than a manual sysadmin task.

### Technical Architecture
The tool implements a strict **ETL (Extract, Transform, Load)** pipeline designed for reliability:

1.  **Extract (API & Streaming):** Connects to vCenter via `pyvmomi` to inspect VM metadata and streams disk data to a staging environment using `ovftool`.
2.  **Transform (Disk Engineering):** logic automates `qemu-img` to transmute monolithic VMware disks (`.vmdk`) into sparse, KVM-native QCOW2 images, optimizing for storage efficiency.
3.  **Load (Infrastructure as Code):** Interacts with the OpenNebula XML-RPC API (`pyone`) to register the new artifacts, effectively re-templating the VM for the new hypervisor.

### SRE & Engineering Highlights
This project was built with **Site Reliability Engineering (SRE)** principles at its core:

* **Risk Mitigation:** Implemented "Pre-flight Checks" and "Dry Run" modes (`--mode dry-run`) to validate connectivity, storage capacity, and tool availability before touching any production data.
* **Observability:** comprehensive logging architecture (Console + File rotation) ensures that if a 500GB migration fails at 99%, the root cause is immediately traceable.
* **Modular Design:** The codebase follows clean architecture, separating "Connectors" (API wrappers) from "Core Logic" (Conversion engines), making it easy to swap out hypervisors or add new targets in the future.
* **Security:** strict separation of configuration (YAML) and secrets (Environment Variables) following 12-Factor App methodologies.

### Tech Stack
* **Core Language:** Python 3.12
* **Virtualization APIs:** PyVmomi (vSphere), PyOne (OpenNebula/XML-RPC)
* **System Tools:** QEMU/KVM tools (`qemu-img`), VMware OVF Tool
* **CLI Framework:** `argparse` (Standard Library stability)
* **Config Management:** YAML, DotEnv

### Impact
This tool reduces the time-to-migrate for a standard server from hours of manual oversight to a single CLI command, effectively unblocking infrastructure cost-reduction strategies.

---

## 📫 Let's Connect

I am **currently seeking a new role** as:
- **DevOps Engineer**
- **Platform Engineer**
- **Release Engineer**

📍 **Location**: Chișinău, Moldova (open to **remote** or **hybrid** in EU)  
⏰ **Time Zone**: EET (UTC+2) / EEST (UTC+3)  
🔗 **LinkedIn**: [linkedin.com/in/gostapenco](https://linkedin.com/in/gostapenco)
📧 **Email**: [gheorghi.ostapenco@gmail.com](mailto:gheorghi.ostapenco@gmail.com)

---

## 📊 GitHub Stats

![Gheorghi's GitHub Stats](https://github-readme-stats.vercel.app/api?username=gheorghiostapenco&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=gheorghiostapenco&layout=compact&theme=tokyonight&hide_border=true&langs_count=8)

![Streak](https://github-readme-streak-stats.herokuapp.com/?user=gheorghiostapenco&theme=tokyonight&hide_border=true)

---

## 🏆 Certifications

| Badge | Certification |
|-------|---------------|
| ![PSM I](https://img.shields.io/badge/PSM%20I-Scrum.org-4A90E2?style=flat-square) | **Professional Scrum Master I** |
| ![PSPO I](https://img.shields.io/badge/PSPO%20I-Scrum.org-2ECC71?style=flat-square) | **Professional Scrum Product Owner I** |
| ![ISTQB](https://img.shields.io/badge/ISTQB-Certified%20Tester-FF6B6B?style=flat-square) | **ISTQB Foundation Level** |

---

**P.S.** If you're hiring for **DevOps**, **SRE**, or **Platform Engineering** roles — let's talk!  
Drop me a message on [LinkedIn](https://linkedin.com/in/gostapenco) or star my **Budget Tracker** repo to say hi.

---
