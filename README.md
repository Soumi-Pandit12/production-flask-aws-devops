# Production Flask AWS DevOps Project

## Project Overview

This project demonstrates a production-style DevOps workflow using Flask, Docker, Jenkins, AWS EC2, RDS, and S3.

The application is containerized using Docker and deployed automatically through a Jenkins CI/CD pipeline.

This project simulates a real-world cloud deployment environment.

---

## Architecture

User → EC2 (Flask App in Docker) → RDS (MySQL) → S3 (File Storage)

---

## Tech Stack

- Python Flask
- Docker
- Jenkins
- AWS EC2
- AWS RDS (MySQL)
- AWS S3
- Linux
- Git & GitHub

---

## CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins pulls latest source code
3. Docker image is built automatically
4. Old container is stopped and removed
5. New container is deployed
6. Updated Flask application becomes live

---

## Jenkins Pipeline Stages

- Checkout SCM
- Checkout Code
- Build Docker Image
- Stop Old Container
- Run New Container

---

## Project Structure

```bash
production-flask-aws-devops/
│
├── app/
│   ├── static/
│   │   └── style.css
│   │
│   ├── templates/
│   │   └── index.html
│   │
│   ├── app.py
│   └── requirements.txt
│
├── docker/
│   ├── docker-compose.yml
│   └── Dockerfile
│
├── jenkins/
│   └── Jenkinsfile
│
├── .gitignore
└── README.md
```

---

## Run Locally

```bash
docker build -t flask-devops-app -f docker/Dockerfile .
docker run -d -p 5000:5000 flask-devops-app
```

---

## Features

- Dockerized Flask application
- Automated Jenkins CI/CD pipeline
- AWS EC2 deployment
- RDS MySQL integration
- AWS S3 integration
- Automated container deployment
- Production-style workflow


---

## Author

Soumi Pandit