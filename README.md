# Production-Ready Apache Web Server on Amazon EC2

![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Amazon Linux](https://img.shields.io/badge/OS-Amazon_Linux_2023-232F3E?style=for-the-badge&logo=amazonlinux&logoColor=white)
![Apache](https://img.shields.io/badge/Web_Server-Apache-D22128?style=for-the-badge&logo=apache&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-System_Administration-FCC624?style=for-the-badge&logo=linux&logoColor=black)

![Architecture](https://img.shields.io/badge/Architecture-Production_Ready-success?style=for-the-badge)
![Documentation](https://img.shields.io/badge/Documentation-Complete-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Project](https://img.shields.io/badge/AWS_80_Projects-3%2F80-orange?style=for-the-badge)

![License](https://img.shields.io/github/license/simeonprimordial/aws-ec2-apache-webserver?style=for-the-badge)
![Last Commit](https://img.shields.io/github/last-commit/simeonprimordial/aws-ec2-apache-webserver?style=for-the-badge)
![Repo Size](https://img.shields.io/github/repo-size/simeonprimordial/aws-ec2-apache-webserver?style=for-the-badge)

---

## Project Overview

This project demonstrates the deployment of a production-ready Apache web server on Amazon EC2 using Amazon Linux 2023.

Unlike managed hosting services such as AWS Lightsail, Amazon EC2 provides complete administrative control over the operating system, networking, software installation, and security configuration. This project focuses on foundational Linux administration skills while implementing AWS security best practices and operational procedures.

The deployment includes launching an EC2 instance, configuring secure network access, installing Apache HTTP Server, deploying a custom landing page, validating the web service, and documenting the implementation from an infrastructure engineering perspective.

---

# Business Scenario

A growing technology company requires a dedicated web server to host its corporate landing page.

The infrastructure team requires full control of the operating system to allow future customization, automation, monitoring, and scalability. Rather than using a managed hosting solution, the company has selected Amazon EC2 to support future migration to a highly available architecture using Application Load Balancers and Auto Scaling Groups.

---

# Business Requirements

The solution must:

- Deploy a Linux virtual machine
- Configure secure remote administration
- Install and configure Apache HTTP Server
- Host a custom HTML landing page
- Follow the Principle of Least Privilege
- Allow HTTP access to customers
- Support future scalability
- Be fully documented

---

# Solution Architecture

```
                    Internet
                        │
                        ▼
               EC2 Security Group
          ┌────────────────────────┐
          │ SSH (22) - My IP Only │
          │ HTTP (80) - Internet  │
          └────────────────────────┘
                        │
                        ▼
               Amazon EC2 Instance
              Amazon Linux 2023 AMI
                        │
                        ▼
                Apache HTTP Server
                        │
                        ▼
             /var/www/html/index.html
                        │
                        ▼
                 Website Visitors
```

A detailed architecture diagram is available in the `architecture/` directory.

---

# Why Amazon EC2?

Amazon EC2 was selected because it provides complete control over the compute environment.

Compared to previous projects:

| Service | Best For | Server Management |
|----------|----------|------------------|
| Amazon S3 | Static websites | None |
| AWS Lightsail | Simplified application hosting | Minimal |
| Amazon EC2 | Full infrastructure control | Full |

EC2 enables administrators to manage:

- Operating System
- Web Server
- Linux Users
- File Permissions
- Security Configuration
- Software Installation
- Automation
- Monitoring
- Scaling

This flexibility makes EC2 suitable for enterprise workloads and custom applications.

---

# AWS Services Used

| AWS Service | Purpose |
|-------------|---------|
| Amazon EC2 | Virtual server hosting |
| Amazon VPC | Network isolation |
| Security Groups | Instance firewall |
| Amazon Linux 2023 | Operating system |

---

# Linux Concepts Demonstrated

Throughout this project, the following Linux administration concepts were applied:

- SSH remote administration
- Package management using DNF
- Apache installation
- Service management using systemctl
- File ownership
- File permissions
- Linux groups
- sudo privilege escalation
- DocumentRoot
- Directory structure

---

# Deployment Summary

The deployment consisted of the following stages:

1. Launch an Amazon EC2 instance.
2. Configure least-privilege Security Groups.
3. Connect using SSH.
4. Update the operating system.
5. Install Apache HTTP Server.
6. Start and enable the Apache service.
7. Deploy a custom landing page.
8. Validate website accessibility.
9. Review Linux permissions.
10. Document the deployment.

Detailed implementation instructions are available in:

```
docs/deployment-guide.md
```

---

# Security Implementation

Security controls implemented include:

- SSH restricted to the administrator's public IP
- HTTP exposed only for web traffic
- Root-owned web content
- Linux permission management
- Principle of Least Privilege
- Amazon Linux security updates

Future improvements include:

- HTTPS using Let's Encrypt
- AWS Systems Manager Session Manager
- AWS WAF
- CloudWatch monitoring
- Application Load Balancer
- Auto Scaling Group

---

# Testing & Validation

The deployment was validated through:

- EC2 instance health checks
- SSH connectivity
- Apache service verification
- Browser accessibility
- Landing page deployment
- Linux permission inspection

---

# Troubleshooting

Challenges encountered during implementation included:

- EC2 Instance Connect failure
- SSH authentication using a PEM key
- Apache service verification
- Linux permission analysis

Solutions and troubleshooting procedures are documented in:

```
docs/troubleshooting.md
```

---

# Repository Structure

```
aws-ec2-apache-webserver/
│
├── README.md
├── LICENSE
│
├── architecture/
│   ├── architecture.drawio
│   └── architecture.png
│
├── docs/
│   ├── architecture.md
│   ├── deployment-guide.md
│   ├── security.md
│   ├── troubleshooting.md
│   └── lessons-learned.md
│
├── screenshots/
│
└── scripts/
```

---

# Lessons Learned

This project reinforced practical knowledge in:

- Amazon EC2 deployment
- Linux server administration
- Apache HTTP Server
- Linux file permissions
- Security Groups
- Least Privilege
- SSH authentication
- Service management
- Production troubleshooting

---

# Future Improvements

Future enhancements include:

- Configure HTTPS
- Register a custom domain
- Deploy an Application Load Balancer
- Configure Auto Scaling
- Integrate CloudWatch monitoring
- Use AWS Systems Manager instead of SSH
- Automate provisioning using Terraform
- Implement CI/CD with GitHub Actions

---

# Skills Demonstrated

- Amazon EC2
- Amazon VPC
- Security Groups
- Amazon Linux 2023
- Apache HTTP Server
- Linux Administration
- SSH
- Systemd
- Networking
- Infrastructure Deployment
- Troubleshooting
- Technical Documentation

---

# Documentation

Additional documentation is available in the `docs/` directory.

- Architecture
- Deployment Guide
- Security Review
- Troubleshooting Guide
- Lessons Learned

---

# Author

**simeon siaka**

Aspiring Cloud & DevOps Engineer

Documenting real-world AWS projects while building practical skills in cloud infrastructure, Linux administration, automation, networking, and production-ready system design.