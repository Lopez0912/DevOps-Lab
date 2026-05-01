# DevOps Project 

End-to-end DevOps pipeline project using:

- Git
- GitHub
- Jenkins
- Docker
- Docker Hub
- Kubernetes
- Minikube

---

## Project Overview

This project demonstrates a complete CI/CD workflow:

1. Source code is pushed to GitHub
2. Jenkins pulls the repository using SCM
3. Docker image is built automatically
4. Image is pushed to Docker Hub
5. Kubernetes deployment is updated automatically

---

## CI/CD Workflow

```text
Developer
   ↓
GitHub Repository
   ↓
Jenkins Pipeline
   ↓
Docker Build
   ↓
Docker Hub
   ↓
Kubernetes Deployment
```

---

## Jenkins Pipeline Stages

- Clone Repository
- Build Docker Image
- Push Docker Image
- Deploy to Kubernetes

---

## Kubernetes Deployment

The application is deployed locally using Minikube and Kubernetes manifests.

Resources used:
- Deployment
- Service

---

## Troubleshooting & Challenges

During this project I worked through several DevOps-related issues including:

- Jenkins SCM configuration
- Docker permissions inside Jenkins container
- Installing Docker and kubectl in Jenkins
- Kubernetes kubeconfig configuration
- TLS and Minikube networking issues
- Git branch mismatch (main/master)

---

## Status

CI/CD pipeline successfully working
