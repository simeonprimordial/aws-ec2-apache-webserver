# Lessons Learned

## Technical Lessons

This project introduced practical Linux administration on AWS.

Key concepts learned include:

- Amazon EC2 deployment
- Amazon Linux 2023
- SSH authentication
- Apache installation
- Linux package management using DNF
- Service management using systemctl
- Linux users and groups
- File ownership
- File permissions
- Apache DocumentRoot

---

## Security Lessons

Important security concepts included:

- Principle of Least Privilege
- Restricting SSH access
- Root ownership
- Proper file permissions
- Why chmod 777 should be avoided

---

## Operational Lessons

I learned the importance of:

- Starting services
- Enabling services at boot
- Validating deployments
- Troubleshooting connectivity issues
- Understanding Linux administration instead of simply following commands

---

## Business Lessons

Amazon EC2 provides significantly more flexibility than AWS Lightsail by giving administrators full control over the operating system, applications, networking, and security configuration.

This additional flexibility comes with increased operational responsibility, making EC2 suitable for production workloads requiring customization and scalability.

---

## Future Improvements

- Configure HTTPS
- Deploy an Application Load Balancer
- Implement Auto Scaling
- Configure Amazon Route 53
- Enable CloudWatch monitoring
- Automate infrastructure using Terraform
- Implement CI/CD with GitHub Actions