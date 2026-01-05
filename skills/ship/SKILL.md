---
name: ship
description: Quick git commit and push workflow. Use when user says "commit and push", "ship it", "commit all", or wants to quickly push changes.
---

# Ship - Quick Git Workflow

Fast-track your commits with smart message generation.

## When to Use

Trigger on:
- "commit and push"
- "ship it"
- "commit all changes"
- "push this"
- "commit everything"

## Workflow

1. **Analyze changes**: `git status` and `git diff`
2. **Stage all**: `git add -A`
3. **Generate message**: Conventional commit format from diff
4. **Commit**: With Claude Code attribution
5. **Push**: To current branch
6. **Report**: Show commit URL

## Commit Message Format

```
type(scope): description

🤖 Generated with [Claude Code](https://claude.com/claude-code)

Co-Authored-By: Claude <noreply@anthropic.com>
```

Types: feat, fix, refactor, docs, style, test, chore
