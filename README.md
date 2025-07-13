# 🚀 Medusa Backend Deployment on AWS ECS with Fargate

This repository contains Infrastructure as Code (IaC) written in **Terraform** to deploy the [Medusa](https://medusajs.com/) open-source headless commerce backend on **Amazon ECS using Fargate**, along with a **CI/CD pipeline using GitHub Actions**.

---

## 📦 What’s Included

- **Medusa backend** container deployed on AWS ECS (Fargate)
- **Terraform code** to provision:
  - VPC, subnets, and security groups
  - ECS cluster and service
- **GitHub Actions** for automated deployment on push to `main`
- Optional Dockerfile to build a custom Medusa image

---

## 🧱 Architecture Overview

- **AWS ECS Cluster** using Fargate
- **Dockerized Medusa backend** from `medusajs/medusa:latest`
- **Public VPC** with two subnets
- **Security group** allowing HTTP traffic on port 80
- **No database or Redis included** (you can add RDS or ElastiCache as needed)

---



## 🗂 Project Structure

medusa-aws-ecs-fargate/
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf (optional)
├── .github/
│   └── workflows/
│       └── deploy.yml
├── docker/
│   └── Dockerfile
├── README.md
└── .gitignore


