---
name: vps-deploy
description: VPS deployment via SSH. Use when user wants to deploy to a VPS, server, or mentions SSH deployment.
---

# VPS Deploy - SSH Deployment

Deploy to VPS servers via SSH.

## When to Use

Trigger on:
- "deploy to vps"
- "deploy via ssh"
- "push to server"
- "deploy to production" (if VPS project)
- "ssh deploy"

## Workflow

1. **Identify**: Server from arg, CLAUDE.md, or ask
2. **Verify**: SSH access and git status
3. **Deploy**: SSH, pull, install, build, restart
4. **Verify**: Check service status

## Server Config

In CLAUDE.md:
```
**SSH:** user@ip
**Path:** /var/www/app
**Deploy:** git pull && npm install && pm2 restart
```
