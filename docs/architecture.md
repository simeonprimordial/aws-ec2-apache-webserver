# Architecture Overview

## Objective

Deploy a production-ready Apache web server on Amazon EC2 using Amazon Linux 2023 while implementing secure networking, Linux administration best practices, and operational readiness.

---

## Business Scenario

A technology company requires a dedicated web server to host its corporate landing page. The infrastructure team requires full control of the operating system and web server to support future automation, monitoring, and scalability.

Amazon EC2 was selected because it provides complete administrative control compared to managed hosting services.

---

## Architecture

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
```

---

## Components

### Amazon EC2

Provides virtual compute capacity with full operating system access.

---

### Amazon Linux 2023

Chosen because it is AWS's latest Linux distribution, optimized for AWS workloads and maintained with long-term security updates.

---

### Security Group

Acts as a virtual firewall.

Rules implemented:

- SSH (22) — Administrator IP only
- HTTP (80) — Public Internet

---

### Apache HTTP Server

Handles incoming HTTP requests and serves website content stored in the DocumentRoot.

---

### DocumentRoot

Apache serves website files from:

```
/var/www/html
```

The default page is:

```
index.html
```

---

## Request Flow

1. User enters the EC2 Public IP in a browser.
2. HTTP request reaches the Security Group.
3. Port 80 traffic is allowed.
4. Apache receives the request.
5. Apache searches the DocumentRoot.
6. `index.html` is returned to the browser.

---

## Future Architecture

Future production improvements include:

- HTTPS
- Application Load Balancer
- Auto Scaling Group
- Amazon Route 53
- Amazon CloudWatch
- AWS Systems Manager