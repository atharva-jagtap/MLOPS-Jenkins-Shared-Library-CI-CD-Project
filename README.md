# 🚀 MLOps CI/CD Pipeline with Jenkins Shared Library on GCP

End-to-end MLOps project implementing a reusable Jenkins Shared Library
to standardize CI/CD workflows across ML services. The system builds,
tests, containerizes, and deploys applications to Kubernetes running on
Google Cloud Platform.

------------------------------------------------------------------------

## 📌 Project Overview

This project demonstrates:

-   🔁 Reusable Jenkins Shared Library for CI/CD automation
-   🐳 Dockerized ML application
-   ☁️ Deployment on GCP Virtual Machine
-   ☸️ Kubernetes-based container orchestration
-   📦 Docker image storage via Docker Hub
-   ⚙️ Automated build → test → push → deploy pipeline

------------------------------------------------------------------------

## 🏗️ Architecture Overview

### Flow

1.  Developer pushes code to GitHub\
2.  Jenkins pipeline is triggered\
3.  Shared Library loads reusable pipeline logic\
4.  Application is:
    -   Built & tested
    -   Dockerized
    -   Image pushed to Docker Hub
    -   Deployed to Kubernetes cluster
<img width="1536" height="1024" alt="Architecture" src="https://github.com/user-attachments/assets/681bdfb5-fc14-4040-a361-116ca6a5bb60" />
<img width="2816" height="1536" alt="Jenkins-Shared Library" src="https://github.com/user-attachments/assets/f22b137a-584b-4a40-a2c8-97fca961394f" />

------------------------------------------------------------------------

## 🧱 Architecture Components

  Component                     Description
  ----------------------------- --------------------------------------
  GitHub Repo                   Stores application code + Dockerfile
  Jenkins Shared Library Repo   Centralized reusable Groovy scripts
  GCP VM                        Hosts Jenkins + Docker
  Docker Hub                    Stores container images
  Kubernetes Cluster            Deploys and runs containerized app

------------------------------------------------------------------------

## 📂 Project Structure

    MLOPS-JENKINS-SHARED-LIB/
    │
    ├── artifacts/
    │   ├── models/
    │   ├── processed/
    │   └── raw/
    │
    ├── k8s/
    │   ├── deployment.yaml
    │   └── service.yaml
    │
    ├── notebook/
    │   └── notebook.ipynb
    │
    ├── pipeline/
    ├── src/
    ├── static/
    ├── templates/
    │
    ├── application.py
    ├── Dockerfile
    ├── Jenkinsfile
    ├── requirements.txt
    ├── setup.py
    └── README.md

------------------------------------------------------------------------

## 🔁 Jenkins Shared Library Structure

    (shared-library-repo)
    │
    ├── vars/
    │   └── commonPipeline.groovy
    │
    ├── src/com/company/
    │   └── Deployer.groovy
    │
    └── resources/templates/

------------------------------------------------------------------------

## 🐳 Docker Commands

Build image:

``` bash
docker build -t your-dockerhub-username/mlops-app .
```

Run locally:

``` bash
docker run -p 5000:5000 mlops-app
```

------------------------------------------------------------------------

## ☸️ Kubernetes Deployment

``` bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

------------------------------------------------------------------------

## ⚙️ Jenkins Pipeline Stages

-   Build
-   Test
-   Docker Build & Push
-   Deploy to Kubernetes

Example shared library call:

``` groovy
commonPipeline.deployTo('dev')
```

------------------------------------------------------------------------

## ☁️ GCP Setup

-   Compute Engine VM created
-   Docker installed
-   Jenkins installed & configured
-   Kubernetes cluster configured
-   Firewall rules enabled

------------------------------------------------------------------------

## 🧠 Why This Project Matters

✔ Demonstrates production-level MLOps\
✔ Shows CI/CD automation skills\
✔ Highlights DevOps + Cloud integration\
✔ Aligns with real-world ML deployment pipelines

------------------------------------------------------------------------

## 👨‍💻 Author

Atharva Jagtap\
MLOps \| Data Science \| DevOps Enthusiast
