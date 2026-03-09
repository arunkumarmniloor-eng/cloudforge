# CloudForge – Cloud Native DevOps Automation Platform

CloudForge is a production-style DevOps project that demonstrates how modern cloud-native applications are built, deployed, automated, and monitored using a complete DevOps toolchain.

This project implements an **end-to-end CI/CD pipeline**, containerized application deployment, Kubernetes orchestration, infrastructure automation, and monitoring — all running on **AWS**.

---

## Architecture Overview

Developer → GitHub → Jenkins CI/CD → Docker Build → DockerHub Registry → Kubernetes (K3s) Deployment → Monitoring (Prometheus + Grafana)

---

## Tech Stack

| Category                | Tools Used           |
| ----------------------- | -------------------- |
| Cloud                   | AWS EC2              |
| Infrastructure as Code  | Terraform            |
| CI/CD                   | Jenkins              |
| Containerization        | Docker               |
| Container Orchestration | Kubernetes (K3s)     |
| Container Registry      | DockerHub            |
| Monitoring              | Prometheus + Grafana |
| Version Control         | GitHub               |

---

## Project Features

* Infrastructure provisioning using **Terraform**
* Containerized application deployment using **Docker**
* Kubernetes orchestration using **K3s**
* Automated **CI/CD pipeline with Jenkins**
* Continuous deployment triggered from **GitHub commits**
* Monitoring and visualization using **Prometheus and Grafana**
* Optimized architecture for **AWS**

---

## Project Structure

cloudforge-devops-platform
│
├── terraform
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── app
│   ├── Dockerfile
│   └── index.html
│
├── kubernetes
│   ├── deployment.yaml
│   └── service.yaml
│
├── jenkins
│   └── Jenkinsfile
│
└── README.md

---

## Deployment Guide

### 1. Clone the Repository

git clone https://github.com/arunkumarmniloor-eng/cloudforge.git 

cd cloudforge

---

### 2. Provision Infrastructure using Terraform

cd terraform

terraform init

terraform apply

This will create the EC2 instance required for the CloudForge platform.

---

### 3. Install DevOps Tools on EC2

Install the following tools on the created EC2 instance:

* Docker
* Jenkins
* Kubernetes (K3s)
* kubectl
* Helm

---

### 4. Build Docker Image

cd app

docker build -t cloudforge-app .

---

### 5. Deploy Application to Kubernetes

kubectl apply -f kubernetes/

---

### 6. Access the Application

http://EC2-PUBLIC-IP:30007

---

## Monitoring Setup

CloudForge uses **Prometheus** to collect system and Kubernetes metrics and **Grafana** to visualize the data through dashboards.

Example metrics monitored:

* Pod CPU usage
* Memory usage
* Node health
* Application availability

---

## Future Enhancements

* GitOps deployment using **ArgoCD**
* Container security scanning using **Trivy**
* Centralized logging using **ELK Stack**
* Canary and Blue-Green deployments
* Multi-environment deployment (Dev / Staging / Production)

---

## Author

Arun Kumar
DevOps Engineer | Cloud & Automation Enthusiast

---

## License

This project is for learning and portfolio demonstration purposes.
