# Django Notes App — CI/CD with Docker, Nginx & Kubernetes on AWS EC2



![Docker](https://img.shields.io/badge/Docker-Container-blue)




![Kubernetes](https://img.shields.io/badge/Kubernetes-Orchestration-blue)




![AWS](https://img.shields.io/badge/AWS-EC2-orange)




![Nginx](https://img.shields.io/badge/Nginx-ReverseProxy-green)




![Django](https://img.shields.io/badge/Django-Backend-darkgreen)




![Python](https://img.shields.io/badge/Python-3.x-yellow)



A DevOps practice project — React + Django Notes App 
containerized with Docker, served via Nginx reverse proxy, 
and deployed to Kubernetes on AWS EC2.

---

## 👩‍💻 My Contributions

> Original app credit: LondheShubham153
> My DevOps work on top of this project:

- Containerized the full app using Docker
- Configured Nginx as reverse proxy
- Deployed to AWS EC2 instance
- Created Kubernetes deployment & service manifests
- Successfully ran pods on Kubernetes cluster
- App accessible via public IP on port 8000

---

## 🔍 Project Overview

This project demonstrates DevOps skills by taking an 
existing React + Django application and deploying it 
using industry-standard containerization and 
orchestration tools on AWS cloud.

---

## ✅ Prerequisites

| Tool | Version | Purpose |
|------|---------|---------|
| Python | 3.x | Run Django backend |
| Docker | Latest | Containerization |
| Nginx | Latest | Reverse proxy server |
| kubectl | Latest | Kubernetes CLI |
| AWS EC2 | - | Cloud hosting |
| GitHub | - | Source code |

---

## 🛠️ Tech Stack

| Layer | Tool |
|-------|------|
| Frontend | React (JavaScript) |
| Backend | Django (Python) |
| Container | Docker |
| Server | Nginx (Reverse Proxy) |
| Orchestration | Kubernetes (k8s) |
| Cloud | AWS EC2 |
| Version Control | GitHub |

---

## 📁 Project Structure

- `api/` — Django REST API
- `mynotes/` — Django app
- `nginx/` — Nginx configuration
- `notesapp/` — React frontend
- `staticfiles/` — Static assets
- `Dockerfile` — Docker image definition
- `deployment.yaml` — Kubernetes deployment
- `service.yaml` — Kubernetes service
- `requirements.txt` — Python dependencies

---

## ⚙️ Pipeline Stages

1. **Clone code** → Pull from GitHub
2. **Docker Build** → `docker build -t notes-app .`
3. **Nginx Config** → Reverse proxy on port 8000
4. **K8s Deploy** → `kubectl apply -f deployment.yaml`
5. **Verify** → `kubectl get pods` — all Running ✅

---

## 🚧 Challenges Faced

| Challenge | How I Solved It |
|-----------|----------------|
| Nginx not routing correctly | Fixed proxy_pass config in nginx.conf |
| Docker container not starting | Debugged using docker logs command |
| Kubernetes pod CrashLoopBackOff | Fixed using kubectl describe pod |
| EC2 app not accessible | Opened port 8000 in EC2 Security Group |
| Static files not loading | Ran python manage.py collectstatic |

---

## 🚀 Run with Docker

```bash
docker build -t notes-app .
docker run -p 8000:8000 notes-app

## Deploy to Kubernetes
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl get pods
kubectl get svc

## 📸 Screenshots

### Kubectl Deployment


![Kubectl Deployment](kubectl%20deployments.jpeg)



### Pipeline


![Pipeline](pipeline.jpeg)



