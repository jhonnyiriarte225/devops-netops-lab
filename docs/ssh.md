# SSH Access Notes (Sanitized)

## Goal
Use SSH key-based authentication for secure, auditable, and repeatable remote access to Linux servers.

## Authentication method
Public/private key authentication (no passwords).

## Basic usage
```bash
ssh -i ~/.ssh/id_ed25519 user@SERVER_IP
```

## Security best practices
- Disable password authentication
- Use modern key types (ed25519)
- Restrict SSH access using firewall rules / security groups
- Rotate keys periodically

## Common issues & troubleshooting
- **Permission denied (publickey)**
  - Check key permissions (`chmod 600 ~/.ssh/id_ed25519`)
  - Verify correct user and IP
- **Connection timeout**
  - Verify firewall / security group rules
  - Confirm SSH service is running
