# my-app-code


# 🚀 Automated DevOps GitOps Pipeline


![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?logo=github)
![Jenkins](https://img.shields.io/badge/Jenkins-CI-D24939?logo=jenkins)
![Docker](https://img.shields.io/badge/Docker-Image-2496ED?logo=docker)
![ArgoCD](https://img.shields.io/badge/ArgoCD-GitOps-EF7B4D?logo=argo)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Deployment-326CE5?logo=kubernetes)
![Automation](https://img.shields.io/badge/Automation-Fully%20Automated-success)


---

# 📌 Pipeline Overview

Developer
    │
    ▼
GitHub Repository
    │
    ▼
Jenkins CI
    │
    ▼
Version Increment
    │
    ▼
Docker Build
    │
    ▼
Docker Hub
    │
    ▼
Deployment Repository
    │
    ▼
Argo CD
    │
    ▼
Kubernetes Cluster

---

# 🏗 Architecture

flowchart LR

[👨‍💻 Developer] -->[GitHub<br/>Application Repository] -->[Jenkins Pipeline] -->[Read version.txt] -->[Increment Version] -->[Docker Build] -->[Docker Push] -->[Deployment Repository] -->[Argo CD] -->[Kubernetes Cluster]


---

# ⚙️ Automation Workflow

| Step | Action                                            |
| ---- | ------------------------------------------------- |
| ✅ 1  | Developer modifies **index.html**                 |
| ✅ 2  | Commit changes                                    |
| ✅ 3  | Push code to GitHub                               |
| ✅ 4  | Jenkins webhook triggers automatically            |
| ✅ 5  | Jenkins pulls latest source                       |
| ✅ 6  | Reads `version.txt`                               |
| ✅ 7  | Increments Docker image version                   |
| ✅ 8  | Updates `version.txt`                             |
| ✅ 9  | Builds Docker image                               |
| ✅ 10 | Pushes image to Docker Hub                        |
| ✅ 11 | Updates Kubernetes deployment manifest            |
| ✅ 12 | Commits deployment changes                        |
| ✅ 13 | Pushes to Deployment Repository                   |
| ✅ 14 | Argo CD detects Git changes                       |
| ✅ 15 | Kubernetes deploys the latest image automatically |

---

# 📂 Repository Structure

my-app-code

│
├── index.html
├── Dockerfile
├── version.txt
├── Jenkinsfile
└── README.md

Deployment Repository

my-app-deployment

│
├── deployment.yaml
└── service.yaml

---

# 🔄 End-to-End Flow

Developer
     │
     ▼
Git Push
     │
     ▼
Jenkins Trigger
     │
     ▼
Pull Latest Code
     │
     ▼
Read version.txt
     │
     ▼
Increment Version
     │
     ▼
Update version.txt
     │
     ▼
Docker Build
     │
     ▼
Docker Push
     │
     ▼
Update deployment.yaml
     │
     ▼
Git Commit
     │
     ▼
Push Deployment Repository
     │
     ▼
Argo CD Auto Sync
     │
     ▼
Kubernetes Deployment

---

# 🐳 Jenkins Responsibilities

* Pull latest application code
* Read current version
* Increment image version automatically
* Update `version.txt`
* Build Docker image
* Push image to Docker Hub
* Update Kubernetes manifest
* Commit deployment changes
* Push Deployment Repository
* Trigger GitOps deployment

---

# 📦 Technologies Used

| Tool       | Purpose                    |
| ---------- | -------------------------- |
| GitHub     | Source Code                |
| Jenkins    | Continuous Integration     |
| Docker     | Containerization           |
| Docker Hub | Image Registry             |
| Kubernetes | Container Orchestration    |
| Argo CD    | GitOps Continuous Delivery |

---

# ✨ Features

* Fully Automated CI/CD
* GitOps Deployment
* Automatic Image Versioning
* Docker Build & Push
* Kubernetes Deployment
* Zero Manual Deployment
* Automatic Manifest Update
* Version Tracking
* Easy Rollback Using Git History

---

# 📈 Deployment Lifecycle

sequenceDiagram

participant Dev as Developer
participant Git as GitHub
participant Jen as Jenkins
participant DH as Docker Hub
participant Repo as Deployment Repo
participant Argo as Argo CD
participant K8s as Kubernetes

Dev->>Git: Push Code

Git->>Jen: Trigger Pipeline

Jen->>Jen: Increment Version

Jen->>DH: Push Docker Image

Jen->>Repo: Update deployment.yaml

Repo->>Argo: New Commit

Argo->>K8s: Sync Application

K8s-->>Dev: Latest Version Running

---

# 🎯 Outcome

✅ No manual Docker build

✅ No manual Docker tagging

✅ No manual Kubernetes deployment

✅ No manual image updates

✅ Fully automated GitOps workflow

---


## 🚀 Continuous Integration + GitOps + Kubernetes

**Push Code → Build Image → Update Manifest → Argo CD Sync → Kubernetes Deploy**


