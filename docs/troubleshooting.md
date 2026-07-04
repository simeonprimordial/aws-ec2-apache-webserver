# Troubleshooting Guide

## Issue 1

### EC2 Instance Connect Failed

Symptoms

Unable to connect using EC2 Instance Connect.

Resolution

Connected successfully using SSH and the downloaded PEM key.

---

## Issue 2

### Apache Not Running

Check:

```bash
sudo systemctl status httpd
```

Start if necessary:

```bash
sudo systemctl start httpd
```

---

## Issue 3

### Website Not Loading

Possible causes:

- Security Group missing HTTP rule
- Apache stopped
- Incorrect DocumentRoot
- Firewall configuration

---

## Issue 4

### Permission Denied

Cause

Attempting to edit files owned by root.

Resolution

Use:

```bash
sudo
```

---

## Issue 5

### SSH Connection Failed

Verify:

- Public IP
- PEM key
- Port 22
- Security Group
- Correct username

Amazon Linux username:

```
ec2-user
```