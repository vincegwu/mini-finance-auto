# 🏗️ Mini-Finance Auto: Terraform + Ansible Deployment Project

A **Cloud DevOps mini-project** demonstrating **Infrastructure as Code (IaC)** and **Configuration Management** for a lightweight static website.  
The project provisions a secure **Azure Virtual Machine** using **Terraform**, then automates **Nginx installation, static site deployment, and service reload** using **Ansible**.

---

## 🚀 Project Overview

**Objective:**  
Provision a secure and repeatable environment to host a public demo of a static finance website.

**Tools Used:**
- 🧱 **Terraform** — Infrastructure provisioning (Azure)
- ⚙️ **Ansible** — Configuration management and deployment
- ☁️ **Azure** — Cloud provider
- 🖥️ **Nginx** — Web server for static content

**Workflow:**
1. Terraform provisions:
   - Resource Group  
   - Virtual Network & Subnet  
   - Network Security Group (SSH + HTTP rules)  
   - Ubuntu VM with Public IP  
   - Passwordless SSH Access  
2. Ansible executes a multi-play flow:
   - Install and configure Nginx  
   - Clone static mini-finance site from GitHub  
   - Deploy the app to Nginx web root  
   - Reload and verify Nginx service

---

## 🗂️ Repository Structure

.
├── README.md
├── ansible
│   ├── inventory.ini
│   └── site.yml
└── terraform
    ├── main.tf
    ├── outputs.tf
    ├── terraform.tfstate
    ├── terraform.tfstate.backup
    ├── terraform.tfvars
    └── variables.tf