---
name: vps-deploy
description: Deploy to VPS via SSH. Pulls latest code, runs deploy commands, verifies deployment.
arguments:
  - name: server
    description: Server alias or SSH address (e.g., aicko, production, user@ip)
    required: false
---

# /vps-deploy - VPS SSH Deployment

Deploy your project to a VPS server via SSH.

## Instructions

### Phase 1: Identify Server
1. Check if server argument provided
2. If not, check CLAUDE.md for default server config
3. Look for deployment config in project:
   - `.deploy.json`
   - `deploy.sh`
   - CLAUDE.md deployment section
4. If no config found, ask user for SSH details

### Phase 2: Pre-Deploy Checks
1. Verify SSH access: `ssh user@host "echo connected"`
2. Check current git status locally
3. Ensure all changes are committed and pushed

### Phase 3: Deploy
1. SSH to server
2. Navigate to project directory
3. Pull latest changes: `git pull origin main`
4. Install dependencies if needed:
   - Node: `npm install` or `pnpm install`
   - Python: `pip install -r requirements.txt`
   - PHP: `composer install`
5. Run build if needed: `npm run build`
6. Restart services if needed:
   - PM2: `pm2 restart all`
   - Systemd: `sudo systemctl restart app`
   - Docker: `docker-compose up -d`

### Phase 4: Verify
1. Check service status
2. Verify app is responding
3. Report success or errors

## Server Config Format (CLAUDE.md)

```markdown
## Deployment

**Server:** aicko
**SSH:** aicko_cz@49.12.32.38
**Path:** /var/www/app
**Deploy:** git pull && npm install && pm2 restart all
```

## Example Usage

```
/vps-deploy                    # Use default from CLAUDE.md
/vps-deploy aicko              # Use saved alias
/vps-deploy user@1.2.3.4       # Direct SSH address
```

## Common Servers (from your history)

- `aicko_cz@49.12.32.38` - aicko.cz
- `claude@46.62.166.240` - projects VPS
