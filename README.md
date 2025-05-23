## Insure Me DevOps Project

This project demonstrates a complete CI/CD pipeline using Git, Docker, Jenkins, Ansible, and AWS.

## Key Points

- The Jenkins pipeline clones the public app repo.
- It builds the Spring Boot app using Maven.
- Builds a Docker image and pushes it to Docker Hub (Docker ID: silvy08).
- Uses Ansible to deploy the Docker container on an AWS EC2 instance.

## Prerequisites

- Jenkins set up with Docker and Ansible plugins.
- Jenkins credentials for Docker Hub and AWS SSH key.
- AWS EC2 instance with Docker installed or install via Ansible.
- Properly configured Ansible inventory file.

## Usage

1. Commit your changes.
2. Run the Jenkins pipeline.
3. Access the app on `http://<EC2_PUBLIC_IP>:8081`.
