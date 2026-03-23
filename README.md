# 🚀 Centralized CI/CD Platform with Shared Jenkins Library

## 📌 Overview

This project demonstrates the implementation of a **centralized CI/CD system** using Jenkins, designed to support multiple applications through a **shared pipeline library**.

Instead of managing separate Jenkins setups for each application, a single Jenkins instance is used to enforce **standardized CI/CD workflows**, improving efficiency and maintainability.



<img width="1536" height="1024" alt="CI_CD pipeline architecture overview" src="https://github.com/user-attachments/assets/0b17e441-030a-4cfe-873c-2c0d0374da17" />


---

## 🎯 Objectives

* Build a centralized CI/CD infrastructure
* Standardize pipeline stages across applications
* Reduce duplication and manual effort
* Improve security and consistency

---

## 🛠️ Tech Stack

* Jenkins
* GitHub
* AWS EC2
* Jenkins Shared Library

---

## 🏗️ Architecture Summary

The system follows a centralized pipeline execution model:

```id="mrxkxm"
Developers
   ↓
GitHub Repositories
   ↓
Jenkins Server (AWS EC2)
   ↓
Shared Pipeline Library
   ↓
Jenkins Agent (Docker-based)
   ↓
Build → Test → Scan → Deploy
  
```


## 📁 Repository Structure

### 🔹 Shared Library

```id="5dy81i"
jenkins-shared-library/
└── vars/
    └── cicdPipeline.groovy
```

---

### 🔹 NodeJS Application

```id="ahc8ww"
app-nodejs/
├── app.js
├── package.json
├── Dockerfile
└── Jenkinsfile
```


![WhatsApp Image 2026-03-23 at 2 12 52 PM](https://github.com/user-attachments/assets/0262eab1-157b-4ade-91f0-68dd3a7d1769)



---

### 🔹 Python Application

```id="gfl1e7"
app-python/
├── app.py
├── Dockerfile
└── Jenkinsfile
```


![WhatsApp Image 2026-03-23 at 2 13 44 PM](https://github.com/user-attachments/assets/5e0cc322-802b-4b0b-9ec3-707e868fd6fa)



---

## ⚙️ Jenkins Setup (AWS EC2)

Jenkins is deployed on an EC2 instance and configured for centralized pipeline execution.

### Setup Steps

1. Launch EC2 instance
2. Install Java & Jenkins
3. Install required plugins
4. Configure Docker
5. Add Jenkins agent
6. Configure credentials
7. Connect shared library


![WhatsApp Image 2026-03-23 at 2 26 58 PM](https://github.com/user-attachments/assets/ab63fd9d-4505-4b48-bd14-dba14b69e62f)



---

## 🤖 Build Agent Configuration

A dedicated Jenkins agent is used to execute builds:

```id="yoyxts"
Name: docker-agent
Executors: 1
Label: docker
Connection: SSH
```


![WhatsApp Image 2026-03-23 at 2 31 51 PM](https://github.com/user-attachments/assets/a87858b1-2018-4ed9-8fa6-3379d132f5b7)



---

## 📚 Shared Library Integration

Configured under:

```id="ci3ueh"
Manage Jenkins → System → Global Pipeline Libraries
```

```id="1v4cr4"
Library Name: shared-library-config
```


![WhatsApp Image 2026-03-23 at 2 26 12 PM](https://github.com/user-attachments/assets/b135d4a6-4128-44d4-aa8b-1f04f22900bb)


---

## 🔄 Pipeline Setup

Separate pipelines are created for each application:

**app-nodejs-pipeline**



<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/83255afc-be6d-44e9-8f30-2c617ca3ad4a" />




**app-python-pipeline**



<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/0cb243f6-ca7c-4540-b2b9-0c177d09d799" />



---

## ⚙️ Pipeline Workflow

Each pipeline executes standardized stages:

* Checkout source code
* Build application
* Run basic tests
* Perform security scan
* Deploy or build Docker image


  
<img width="1920" height="1008" alt="Centralized-CI-CD-Platform-using-Shared-Jenkins-Infrastructure_README md at main · mrbacchu2020_Centralized-CI-CD-Platform-using-Shared-Jenkins-Infrastructure — Mozilla Firefox 3_19_2026 10_28_12 PM" src="https://github.com/user-attachments/assets/fe45bc7a-21a7-4704-87c0-ab6610873cb9" />



![WhatsApp Image 2026-03-23 at 2 32 40 PM](https://github.com/user-attachments/assets/00c0a340-fe53-4e1f-a97c-1f31551da781)


---

## 📦 Deliverables

* Centralized Jenkins CI/CD system
* Shared pipeline library
* Multi-application pipeline setup
* Automated Docker image builds

---

## 🎓 Learning Outcomes

* CI/CD automation using Jenkins
* Shared library implementation
* AWS-based infrastructure setup
* Multi-project pipeline management

---

## 📌 Conclusion

The centralized CI/CD platform ensures consistent and reusable pipelines across multiple applications. This approach significantly improves scalability and simplifies CI/CD management.

---
---

## 👩‍💻 Author

**Monika Gaikwad**
Cloud & DevOps Enthusiast ☁️🚀
