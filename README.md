# Jenkins Docker Pipeline 

## Overview

 It demonstrates how to set up Jenkins inside a Docker container and create a Jenkins Pipeline that builds and deploys a simple Hello World application using Docker Desktop.

The project provides a basic Continuous Integration (CI) workflow where Jenkins automatically builds and runs a Docker container from the application source code.

---

## Objectives

- Install and run Jenkins using Docker Desktop
- Create a custom Jenkins Docker image
- Configure Jenkins Pipeline
- Build a Docker image automatically
- Deploy a Hello World application inside a Docker container
- Understand the basics of Continuous Integration (CI)

---

## Work Architecture

```
Developer
    │
    ▼
GitHub Repository
    │
    ▼
Jenkins Pipeline
    │
    ▼
Docker Build
    │
    ▼
Docker Container
    │
    ▼
Hello World Application
```

---

## Repository Structure

```
jenkins-docker-pipeline/
│
├── hello-world-demo/
│   ├── Dockerfile
│   ├── Jenkinsfile
│   ├── index.html
│   └── README.md
│
└── jenkins-docker/
    ├── Dockerfile
    └── docker-compose.yml
```

---

## Workflow

1. Create a custom Jenkins Docker image.
2. Run Jenkins using Docker Compose.
3. Configure Jenkins.
4. Connect Jenkins with GitHub.
5. Build the Hello World Docker image.
6. Deploy the application inside a Docker container.
7. Access the application through a web browser.

---
## Commands Used

### 1. Verify Docker Installation

```bash
docker --version
docker ps
```

---

### 2. Build the Custom Jenkins Docker Image

```bash
cd jenkins-docker
docker compose build
```

---

### 3. Start Jenkins Container

```bash
docker compose up -d
```

---

### 4. Verify Running Containers

```bash
docker ps
```

---

### 5. Retrieve Jenkins Initial Admin Password

```bash
docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

---

### 6. Access Jenkins

Open a browser and navigate to:

```
http://localhost:8080
```

---

### 7. Build the Hello World Docker Image

```bash
docker build -t hello-world .
```

---

### 8. Run the Hello World Container

```bash
docker run -d --name hello -p 8081:80 hello-world
```

---

### 9. View Running Containers

```bash
docker ps
```

---

### 10. View Container Logs

```bash
docker logs hello
```

---

### 11. Stop and Remove the Container

```bash
docker stop hello
docker rm hello
```

---

### 12. Stop Jenkins

```bash
docker compose down
```

---

### 13. Git Commands

Initialize Git Repository

```bash
git init
```

Add Files

```bash
git add .
```

Commit Changes

```bash
git commit -m "Initial commit"
```

Rename Branch

```bash
git branch -M main
```

Add Remote Repository

```bash
git remote add origin https://github.com/<your-username>/jenkins-docker-pipeline-lab.git
```

Push to GitHub

```bash
git push -u origin main
```

---

* The application is accessible at:

```
http://localhost:8081
```



DevOps | AWS | Docker | Jenkins
