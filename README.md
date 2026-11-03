# Terraform + Docker + Nginx Website Hosting on AWS

## Project Overview

This project demonstrates website hosting on AWS using Terraform, Docker, and Nginx.

Terraform is used to provision AWS infrastructure, while Docker is used to build and run an Nginx container to host a static website created using HTML and CSS.

## Technologies Used

- AWS EC2
- Terraform
- Docker
- Nginx
- Amazon Linux 2023
- HTML & CSS
- Git & GitHub

## Architecture Diagram

The following diagram represents the project architecture and deployment workflow.

<img width="1536" height="1024" alt="ar" src="https://github.com/user-attachments/assets/21ee3552-e46b-452c-afa8-327e34f34c64" />


## Implementation

- Provisioned an EC2 instance on AWS using Terraform.
- Configured Security Groups for SSH and website access.
- Set up Docker on the EC2 instance.
- Created a custom Docker image using Nginx.
- Added HTML and CSS files to the Docker image.
- Deployed the Nginx container on EC2.
- Configured port mapping 8080:80.
- Accessed the hosted website using the EC2 public IP.

## Project Structure

    terraform-nginx-docker-website-project/
    |
    |-- Docker/
    |   |-- Dockerfile
    |   |-- index.html
    |   |-- style.css
    |
    |-- terraform/
    |   |-- main.tf
    |   |-- provider.tf
    |   |-- variables.tf
    |   |-- outputs.tf
    |
    |-- .gitignore

## Deployment Steps

### 1. Clone Repository

    git clone https://github.com/pooja-daingade/terraform-nginx-docker-website-project.git

### 2. Initialize Terraform

    cd terraform-nginx-docker-website-project/terraform
    terraform init

### 3. Validate Terraform Configuration

    terraform validate

### 4. Review Execution Plan

    terraform plan

### 5. Provision AWS Infrastructure

    terraform apply --auto-approve

### 6. Build Docker Image

    cd ../Docker
    sudo docker build -t nginx-website .

### 7. Run Docker Container

    docker run -d nginx-custom -p 8080:80 nginx-pooja:new

## Website Access

    http://<EC2-Public-IP>:8080

Replace EC2-Public-IP with your EC2 instance's public IP address.

## Key Learnings

- AWS infrastructure provisioning using Terraform.
- EC2 and Security Group configuration.
- Docker image creation and container management.
- Nginx web server deployment.
- Website hosting using Docker port mapping.
- Git and GitHub version control.

## Author

Pooja Daingade
