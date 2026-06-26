# Jenkins Docker Pipeline Lab

## Project Overview

This project demonstrates how to set up Jenkins inside a Docker container and create a Jenkins Pipeline that builds and deploys a simple Hello World application using Docker Desktop.

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

## Project Architecture

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

## Project Structure

```
jenkins-docker-pipeline/
│
├── hello-world/
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



DevOps | AWS | Docker | Jenkins
