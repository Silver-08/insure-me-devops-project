# Insure Me DevOps Project

## Overview

This project demonstrates a simple CI/CD pipeline for the _Insure Me_ Spring Boot application using:

- Git (version control)
- Jenkins (CI/CD automation)
- Docker (containerization)
- Ansible (configuration management)
- AWS EC2 (hosting Jenkins, Docker, and app)

## Architecture

- Single AWS EC2 instance runs Jenkins, Docker, and the deployed application.
- No Kubernetes or Terraform used.
- No separate monitoring instance needed.

## How It Works

1. Developer pushes code to GitHub (main branch).
2. GitHub webhook triggers Jenkins pipeline.
3. Jenkins pulls code, builds with Maven, and runs tests.
4. Jenkins builds Docker image and deploys container.
5. Application runs on EC2 instance accessible at `http://<EC2-IP>:8080`.

## Project Structure

- `app/` — Cloned Spring Boot app code
- `ansible/` — Playbook and inventory for instance setup
- `docker/` — Dockerfile for app container
- `jenkins/` — Jenkinsfile defining pipeline
- `LICENSE` — License file

## Setup Instructions

1. Launch one AWS EC2 instance (Amazon Linux 2 recommended).
2. Run Ansible playbook from your local machine to install Jenkins, Docker, Java, and Git on EC2.
3. Set up Jenkins pipeline job using the `jenkins/Jenkinsfile`.
4. Configure GitHub webhook to trigger Jenkins build on push.
5. Jenkins will build, test, containerize, and deploy the app automatically.

## Accessing the App

Open a browser and go to `http://<EC2-public-ip>:8080`.

## About the App Code

The main application source code is **not included** in this repository.

During the Jenkins CI/CD pipeline, the app code is cloned directly from its original public GitHub repository.

This keeps the project repository clean and focused on DevOps configurations.

Make sure your Jenkinsfile contains the appropriate commands to clone the app repository during the build stage.

---

_For any questions, reach out to Silver-08._
