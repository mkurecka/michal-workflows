---
name: mailerlite-setup
description: MailerLite email marketing. Use when user wants to create email groups, add subscribers, or set up email marketing.
---

# MailerLite Setup - Email Marketing

Manage MailerLite groups and subscribers.

## When to Use

Trigger on:
- "create mailerlite group"
- "add subscriber"
- "email marketing setup"
- "mailerlite"
- "create email group"

## Workflow

1. **Verify**: API key configured
2. **Action**: List, create group, or add subscriber
3. **Integrate**: Store group ID for forms

## Actions

- list-groups: Show all groups
- create-group: New subscriber group
- add-subscriber: Add email to group

## Requirements

- MAILERLITE_API_KEY environment variable
