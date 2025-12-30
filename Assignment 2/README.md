
# Assignment 2 — Terraform Multi-Tier Architecture with NGINX

## Architecture
This project deploys a highly available multi-tier web architecture on AWS using Terraform.

Components:
- VPC with public and private subnets
- EC2 instances acting as backend web servers
- NGINX reverse proxy / load balancer
- Security Groups for controlled access
- HTTPS enabled using self-signed SSL certificate
- Backup server for high availability

NGINX distributes traffic across multiple backend servers and redirects HTTP traffic to HTTPS.

---

## Deployment
Steps used to deploy the infrastructure:

1. Initialize Terraform
   terraform init

2. Review execution plan
   terraform plan

3. Deploy infrastructure
   terraform apply

4. Verify EC2 instances and NGINX service

---

## Testing
The following tests were performed:

- Load Balancing Test:
  Refreshing NGINX public IP alternates responses between backend servers

- High Availability Test:
  Stopping backend servers redirects traffic to available instances and backup server

- Security Test:
  - SSL certificate verified using openssl
  - HTTP to HTTPS redirection tested
  - Security headers verified using curl

---

## Troubleshooting
Common issues and solutions:

- SSH connection issues:
  Ensure correct security group rules and private key permissions

- NGINX not responding:
  Restart service using systemctl restart nginx

- Backend not reachable:
  Verify private IP connectivity and security group rules

---

## Cleanup
All AWS resources were removed using:
terraform destroy
