---
name: cf-deploy
description: Deploy to Cloudflare Workers or Pages. Runs wrangler deploy and reports status.
arguments:
  - name: environment
    description: Optional environment (production, staging, preview)
    required: false
---

# /cf-deploy - Cloudflare Deployment

Deploy your project to Cloudflare Workers or Pages with status reporting.

## Instructions

1. Check if `wrangler.toml` or `wrangler.jsonc` exists in the project
2. If not found, inform user and ask if they want to initialize
3. Run `wrangler deploy` (or `wrangler pages deploy` for Pages projects)
4. If environment specified, use `--env <environment>`
5. Monitor the output for deployment URL
6. Report success with the live URL, or show errors if failed
7. Optionally run `wrangler tail` to show recent logs if user wants

## Pre-flight Checks

- Verify wrangler is installed: `which wrangler`
- Check for wrangler config file
- Ensure user is logged in: `wrangler whoami`

## Example Usage

```
/cf-deploy                 # Deploy to default environment
/cf-deploy production      # Deploy to production
/cf-deploy staging         # Deploy to staging
```

## Common Issues

- If "not logged in": Run `wrangler login`
- If "missing account_id": Add to wrangler.toml
- If "compatibility_date": Update wrangler.toml
