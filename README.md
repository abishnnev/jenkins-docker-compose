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



