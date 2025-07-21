
# 🚀 DevOps Project: Go Web Application Deployment on Amazon EKS

This project demonstrates a complete DevOps pipeline for deploying a Go web application using Docker, GitHub Actions, Helm, Argo CD, and Kubernetes on Amazon EKS. The application is containerized, tested, pushed to Docker Hub, and then deployed to a Kubernetes cluster with a GitOps workflow.

---

## ✅ What’s Implemented

- **Terraform** for infrastructure provisioning
- **Containerization** using a multi-stage Dockerfile and Docker Hub
- **Kubernetes deployment** (Deployment, Service, Ingress)
- **NGINX Ingress Controller** for external traffic routing
- **Amazon EKS** for cluster provisioning and management
- **Helm charts** for simplified Kubernetes resource deployment
- **GitHub Actions** for CI: image build, test, and push
- **Argo CD** for CD: GitOps-based automated deployment

---

## Architecture Workflow

![DevOps Workflow]()

This diagram represents the complete DevOps flow — from source code to live deployment in EKS via CI/CD tools and GitOps.

---

## Docker Build & Push

Commands to build the Docker container:

```bash
docker build -t <your-docker-username>/go-web-app .
```

Command to run the Docker container:

```bash
docker run -p 8080:8080 <your-docker-username>/go-web-app
```

Command to push the Docker container to Docker Hub:

```bash
docker push <your-docker-username>/go-web-app
```

## CI/CD Pipeline

- **CI** with GitHub Actions: Automatically builds Docker image, runs tests, and pushes to Docker Hub on every commit.
- **CD** with Argo CD: Monitors GitHub repo and syncs changes to the Amazon EKS cluster using GitOps.

---

## Argo CD Application Sync

Below is the Argo CD dashboard confirming the successful deployment of the application:

![Argo CD Sync]()

---

