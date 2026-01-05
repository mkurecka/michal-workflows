---
name: linear-next
description: Fetch next Linear issue, display details, and update status when done.
arguments:
  - name: project
    description: Linear project identifier or team key (e.g., MKU, SNAP)
    required: false
---

# /linear-next - Linear Issue Workflow

Fetch your next prioritized Linear issue and work through your backlog efficiently.

## Instructions

1. Check for Linear project identifier:
   - If provided as argument, use it
   - If in CLAUDE.md, use that
   - Otherwise, ask user which project to use
2. Query Linear API for issues:
   - Filter: `state.type != "completed" AND state.type != "canceled"`
   - Sort by: priority (urgent first), then created date
   - Limit: 1
3. Display issue details:
   - Title, identifier, priority, labels
   - Description (full markdown)
   - Assignee, due date if set
4. Ask user: "Ready to work on this? (yes/skip/list more)"
5. When user completes work:
   - Ask for status update (In Progress, Done, etc.)
   - Add comment summarizing what was done
   - Update issue state via API
6. Offer to fetch next issue

## Linear API Usage

Use GraphQL API with LINEAR_API_KEY environment variable:

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
    nodes {
      id
      identifier
      title
      description
      priority
      state { name }
      labels { nodes { name } }
      assignee { name }
      dueDate
    }
  }
}
```

## Example Usage

```
/linear-next           # Use project from CLAUDE.md or ask
/linear-next MKU       # Fetch from MKU project
/linear-next SNAP      # Fetch from SNAP project
```

## Status Updates

After completing work, update the issue:
- "In Progress" → working on it
- "In Review" → ready for review
- "Done" → completed
