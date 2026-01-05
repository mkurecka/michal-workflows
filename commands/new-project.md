---
name: new-project
description: Create a new project with GitHub repo, folder structure, and CLAUDE.md.
arguments:
  - name: name
    description: Project name (will be used for repo and folder)
    required: true
  - name: template
    description: Project template (node, python, cloudflare, nextjs, empty)
    required: false
  - name: visibility
    description: Repo visibility (public, private)
    required: false
---

# /new-project - Project Scaffolding

Create a new project with GitHub repo and essential setup.

## Instructions

### Phase 1: Create Repository
1. Create GitHub repo via `gh repo create`
   - Name: provided name
   - Visibility: private by default (or as specified)
   - Description: Ask user or generate
2. Clone to current directory or specified path

### Phase 2: Initialize Structure
Based on template:

**empty** (default):
```
project/
├── .gitignore
├── README.md
└── CLAUDE.md
```

**node**:
```
project/
├── src/
│   └── index.ts
├── package.json
├── tsconfig.json
├── .gitignore
├── README.md
└── CLAUDE.md
```

**python**:
```
project/
├── src/
│   └── main.py
├── requirements.txt
├── .gitignore
├── README.md
└── CLAUDE.md
```

**cloudflare**:
```
project/
├── src/
│   └── index.ts
├── wrangler.toml
├── package.json
├── tsconfig.json
├── .gitignore
├── README.md
└── CLAUDE.md
```

**nextjs**:
- Run `npx create-next-app@latest`
- Add CLAUDE.md

### Phase 3: Create CLAUDE.md
Generate project-specific CLAUDE.md with:
- Project name and description
- Tech stack
- Development commands
- Deployment info (if applicable)
- Linear project link (if applicable)

### Phase 4: Initial Commit
1. Stage all files
2. Commit: "feat: initial project setup"
3. Push to GitHub

### Phase 5: Report
- GitHub repo URL
- Local path
- Next steps

## Example Usage

```
/new-project my-app                     # Empty private repo
/new-project api-service node           # Node.js project
/new-project ml-model python public     # Public Python project
/new-project worker cloudflare          # Cloudflare Worker
/new-project frontend nextjs            # Next.js app
```

## CLAUDE.md Template

```markdown
# [Project Name]

[Description]

## Tech Stack
- [Stack items]

## Development

\`\`\`bash
# Install dependencies
npm install

# Run locally
npm run dev
\`\`\`

## Deployment
[Deployment instructions]

## Links
- GitHub: [url]
- Linear: [project link]
```
