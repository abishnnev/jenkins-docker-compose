#  Jenkins on AWS with Terraform


A complete infrastructure-as-code solution to deploy a production-ready Jenkins server on AWS with automated backups, secure networking, and persistent storage.


## 🏗️ Overview

This Terraform project automates the deployment of a fully functional Jenkins CI/CD environment on AWS. It follows best practices for security, reliability, and maintainability.

```bash
jenkins-docker-compose/
├── main.tf                 # Main infrastructure configuration
├── outputs.tf              # Output variables
├── variables.tf            # Input variables
├── user-data.sh           # EC2 instance bootstrap script
 ```
## 🛠️ Infrastructure Components
  Networking
VPC: 10.0.0.0/16

. Public Subnet: 10.0.1.0/24 in us-east-1a

. Internet Gateway for internet access

. Route Tables for network routing




 ##Security
Security Group with rules for:

. SSH (port 22)

. Jenkins Web UI (port 8080)

. Jenkins Agent (port 50000)

. Auto-generated SSH Key Pair


 ##Compute & Storage

. EC2 Instance: t3.medium with Amazon Linux 2

. EBS Root Volume: 20GB gp3 encrypted

. EBS Data Volume: 20GB gp3 encrypted for Jenkins data


 ##Backup & Recovery

AWS Backup Vault for EBS volume backups

Daily Backup Schedule at 2 AM

7-day Retention Policy


 ##🔧 Configuration

Jenkins Configuration

 Runs in Docker container

Automatic setup without initial wizard

Persistent data on mounted EBS volume

Docker socket mounted for Docker-in-Docker


 ##user Data Script
The user-data.sh script automatically:

Updates system packages

Installs Docker and Docker Compose

Formats and mounts EBS volume

Deploys Jenkins container

Configures automatic startup

 ##📊 Outputs



