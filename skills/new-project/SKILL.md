---
name: new-project
description: Project scaffolding. Use when user wants to create a new project, repo, or start something new.
---

# New Project - Scaffolding

Create new projects with GitHub repo and setup.

## When to Use

Trigger on:
- "create new project"
- "new repo"
- "start new project"
- "scaffold project"
- "init project"

## Workflow

1. **Create**: GitHub repo via gh cli
2. **Structure**: Based on template (node, python, etc.)
3. **CLAUDE.md**: Generate project config
4. **Commit**: Initial commit and push

## Templates

- empty: Just .gitignore, README, CLAUDE.md
- node: TypeScript Node.js project
- python: Python project
- cloudflare: Cloudflare Worker
- nextjs: Next.js app
