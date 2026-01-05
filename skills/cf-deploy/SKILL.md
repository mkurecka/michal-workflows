---
name: cf-deploy
description: Cloudflare Workers/Pages deployment. Use when user says "deploy to cloudflare", "cf deploy", "wrangler deploy", or wants to deploy to Cloudflare.
---

# Cloudflare Deploy

Quick deployment to Cloudflare Workers or Pages.

## When to Use

Trigger on:
- "deploy to cloudflare"
- "cf deploy"
- "wrangler deploy"
- "deploy to production" (if Cloudflare project)
- "push to workers"

## Workflow

1. **Check config**: Look for `wrangler.toml` or `wrangler.jsonc`
2. **Verify auth**: `wrangler whoami`
3. **Deploy**: `wrangler deploy` or `wrangler pages deploy`
4. **Report**: Show deployment URL or errors

## Pre-requisites

- wrangler CLI installed
- Logged in via `wrangler login`
- Valid wrangler config file

## Troubleshooting

- Not logged in → `wrangler login`
- Missing account_id → Add to wrangler.toml
- Build errors → Check wrangler.toml compatibility_date
