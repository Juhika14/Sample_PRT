# 🚀 Jenkins-Triggered Ansible Deployment

## 📌 Overview
This repository contains the **Terraform, Ansible, and Jenkins pipeline scripts** for automating the provisioning and configuration of instances. The setup includes:
- **Terraform** for provisioning AWS infrastructure.
- **Ansible** for configuring server dependencies.
- **Jenkins** for automated deployment using a **GitHub webhook**.

## 🎯 Project Objectives
✅ **Infrastructure Setup (Terraform)**:
- Creates a **VPC & Subnet**.
- Defines a **Security Group** with appropriate rules.
- Launches **3 Instances** with Elastic IPs.

✅ **Configuration Management (Ansible)**:
- Installs **Nginx** on `Slave1`.
- Installs **Apache2** on `Slave2`.

✅ **Continuous Deployment (Jenkins)**:
- **Pulls Ansible playbook** from this repository.
- Runs **syntax check** before execution.
- Executes the playbook automatically upon every push (via **GitHub webhook**).

## 🏗️ Technologies Used
- **Terraform** (Infrastructure as Code)
- **Ansible** (Configuration Management)
- **Jenkins** (CI/CD Automation)
- **GitHub** (Version Control)

## 🔗 Repository Link
📌 **GitHub Repository:** [Sample_PRT](https://github.com/Juhika14/Sample_PRT.git)

## 🛠️ Usage
### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/Juhika14/Sample_PRT.git
cd Sample_PRT
2️⃣ Run Terraform Script
terraform init
terraform apply
4️⃣ Set Up Jenkins Pipeline
Add the Jenkinsfile to the repository.

Configure GitHub webhook for auto-triggering.

👨‍💻 Author
Juhika Azmeen
Email: juhikaazmeen123@gmail.com
giithub url: www.github.com/juhika14
