# 🚀 Jenkins on AWS with Terraform

![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

A complete infrastructure-as-code solution to deploy a production-ready Jenkins server on AWS with automated backups, secure networking, and persistent storage.

## 📋 Table of Contents

- [Overview](#-overview)
- [Architecture](#-architecture)
- [Features](#-features)
- [Quick Start](#-quick-start)
- [Infrastructure](#-infrastructure)
- [Usage](#-usage)
- [Monitoring](#-monitoring)
- [Cost Estimation](#-cost-estimation)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)

## 🏗️ Overview

This Terraform project automates the deployment of a fully functional Jenkins CI/CD environment on AWS. It follows best practices for security, reliability, and maintainability.

```bash
jenkins-docker-compose/
├── main.tf                 # Main infrastructure configuration
├── outputs.tf              # Output variables
├── variables.tf            # Input variables
├── user-data.sh           # EC2 instance bootstrap script
├── .terraform.lock.hcl    # Terraform dependency lock
└── README.md              # Project documentation
