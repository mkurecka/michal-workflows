---
name: linear-next
description: Linear issue workflow management. Use when user says "next issue", "linear issue", "work on next task", "update linear", or wants to manage Linear issues.
---

# Linear Next - Issue Workflow

Fetch and manage Linear issues efficiently.

## When to Use

Trigger on:
- "next issue"
- "linear issue"
- "work on next task"
- "update linear"
- "solve next issue"
- "what's next in linear"

## Workflow

1. **Identify project**: From argument, CLAUDE.md, or ask user
2. **Fetch issue**: Query Linear API for next prioritized issue
3. **Display details**: Title, description, priority, labels
4. **Work**: User works on the issue
5. **Update**: Change status, add comment
6. **Continue**: Offer next issue

## API Requirements

Requires `LINEAR_API_KEY` environment variable.

## GraphQL Query

```graphql
query NextIssue($teamKey: String!) {
  issues(
    filter: {
      team: { key: { eq: $teamKey } }
      state: { type: { nin: ["completed", "canceled"] } }
    }
    orderBy: [priority, createdAt]
    first: 1
  ) {
    nodes { id identifier title description priority }
  }
}
```

## Status Flow

- Todo → In Progress → In Review → Done
