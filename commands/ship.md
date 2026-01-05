---
name: ship
description: Quick commit and push. Auto-stages all changes, generates smart commit message, and pushes.
arguments:
  - name: message
    description: Optional custom commit message (otherwise auto-generated)
    required: false
---

# /ship - Quick Git Commit & Push

Ship your changes with one command. Stages everything, generates a smart commit message, and pushes.

## Instructions

1. First, run `git status` to see all changes (staged and unstaged)
2. Run `git diff` to understand what changed
3. Run `git log --oneline -5` to see recent commit style
4. Stage all changes with `git add -A`
5. If user provided a message, use it. Otherwise, generate a conventional commit message based on the diff:
   - Use format: `type(scope): description`
   - Types: feat, fix, refactor, docs, style, test, chore
   - Keep message under 72 chars
6. Commit with the message + attribution footer
7. Push to the current branch
8. Display the commit URL (if remote is GitHub/GitLab)

## Commit Message Format

```
type(scope): short description

Optional longer description if changes are complex.

🤖 Generated with [Claude Code](https://claude.com/claude-code)

Co-Authored-By: Claude <noreply@anthropic.com>
```

## Example Usage

```
/ship                    # Auto-generate commit message
/ship "fix login bug"    # Use custom message
```
