# Security Review

## Objective

Implement security best practices while maintaining accessibility for legitimate users.

---

## Security Controls Implemented

### Security Groups

Inbound Rules

| Service | Port | Source |
|----------|------|--------|
| SSH | 22 | My Public IP |
| HTTP | 80 | Anywhere |

---

### Least Privilege

SSH access is restricted to the administrator's IP address.

This significantly reduces the attack surface.

---

### Linux Ownership

Website files are owned by:

```
root
```

This prevents unauthorized modification.

---

### File Permissions

Default permissions:

```
rw-r--r--
```

Apache only requires read permission to serve web pages.

---

### Why Not chmod 777?

Granting full permissions to every user introduces serious security risks.

Instead, permissions should follow the Principle of Least Privilege.

---

## Future Security Enhancements

- HTTPS
- AWS WAF
- AWS Systems Manager Session Manager
- CloudWatch monitoring
- Fail2Ban
- SSH key rotation