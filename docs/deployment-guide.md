# Deployment Guide

## Prerequisites

- AWS Account
- Amazon EC2 access
- SSH key pair
- GitHub repository

---

## Deployment Steps

### Step 1

Launch an EC2 instance using:

- Amazon Linux 2023
- t2.micro (or t3.micro)
- 8 GiB gp3 storage

---

### Step 2

Configure Security Group.

Inbound rules:

- SSH (22) → My IP
- HTTP (80) → Anywhere

---

### Step 3

Connect using SSH.

```bash
ssh -i ec2-aws-key.pem ec2-user@<Public-IP>
```

---

### Step 4

Update Linux.

```bash
sudo dnf update -y
```

---

### Step 5

Install Apache.

```bash
sudo dnf install -y httpd
```

---

### Step 6

Start Apache.

```bash
sudo systemctl start httpd
```

---

### Step 7

Enable Apache at boot.

```bash
sudo systemctl enable httpd
```

---

### Step 8

Verify service.

```bash
sudo systemctl status httpd
```

---

### Step 9

Navigate to:

```
/var/www/html
```

Replace the default webpage with a custom landing page.

---

### Step 10

Verify website accessibility.

```
http://<Public-IP>
```

---

## Outcome

A production-ready Apache web server was successfully deployed on Amazon EC2.