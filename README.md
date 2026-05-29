# Assessment

## Project Overview

This project demonstrates cloud infrastructure deployment using Terraform, Docker, and AWS services. The application was containerized using Docker and deployed on AWS infrastructure provisioned using Terraform.

---

## Technologies Used

* AWS EC2
* AWS VPC
* Terraform
* Docker
* GitHub Actions
* Nginx
* Auto Scaling Group
* CloudWatch Monitoring

---

## Infrastructure Components

* VPC
* Public Subnet
* Internet Gateway
* Route Tables
* Security Groups
* EC2 Instances
* Auto Scaling Group
* Application Load Balancer

---

## Design Decisions

* Used Terraform for Infrastructure as Code
* Dockerized application for portability and simplified deployment
* Implemented Auto Scaling Group for scalability
* Used Load Balancer architecture for high availability
* Used GitHub Actions for CI/CD automation

---

## Trade-offs Considered

* Used EC2 instead of ECS/EKS for simplicity and lower infrastructure cost
* Focused on lightweight architecture suitable for assessment requirements
* Implemented basic infrastructure instead of production-grade Kubernetes orchestration

---

## Cost Optimization

* Used lightweight t3.micro instances
* Used minimal AWS resources
* Used Auto Scaling configuration to prevent over provisioning
* Avoided unnecessary managed services to reduce costs

---

## Deployment Steps

### Docker

```bash
docker build -t siddhan-app .
docker run -d -p 8080:80 siddhan-app
```

### Terraform

```bash
terraform init
terraform plan
terraform apply
```

### GitHub Actions CI/CD

GitHub Actions workflow automatically builds Docker image whenever code is pushed to the main branch.

---

## Auto Scaling & Monitoring

Implemented Auto Scaling Group with:

* Minimum Capacity: 2
* Desired Capacity: 2
* Maximum Capacity: 4

Monitoring implemented using AWS CloudWatch:

* CPU Utilization
* Network In/Out
* EC2 Status Checks

---

## Architecture

Refer to architecture-diagram.png for infrastructure architecture overview.
