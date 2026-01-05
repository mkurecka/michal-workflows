---
name: mailerlite-setup
description: Create MailerLite groups and add subscribers. Useful when creating guides or lead magnets.
arguments:
  - name: action
    description: Action (create-group, add-subscriber, list-groups)
    required: false
  - name: name
    description: Group name or subscriber email
    required: false
---

# /mailerlite-setup - Email Marketing Setup

Manage MailerLite groups and subscribers.

## Instructions

### Phase 1: Check API Access
1. Verify MAILERLITE_API_KEY is set
2. Test API connection
3. If not configured, ask for API key

### Phase 2: Actions

**list-groups** (default if no args):
1. Fetch all groups from MailerLite
2. Display:
   - Group name
   - Subscriber count
   - Created date

**create-group**:
1. Create new group with provided name
2. API call:
   ```
   POST https://connect.mailerlite.com/api/groups
   {
     "name": "Group Name"
   }
   ```
3. Return group ID for future use

**add-subscriber**:
1. Add email to specified group
2. API call:
   ```
   POST https://connect.mailerlite.com/api/subscribers
   {
     "email": "user@example.com",
     "groups": ["group_id"],
     "fields": {
       "name": "User Name"
     }
   }
   ```
3. Confirm subscription

### Phase 3: Integration with Content

When creating guides/lead magnets:
1. Auto-create group for the guide
2. Add group ID to Notion/Airtable record
3. Ready for lead capture

## API Reference

```
Base: https://connect.mailerlite.com/api

Headers:
  Authorization: Bearer {MAILERLITE_API_KEY}
  Content-Type: application/json

Endpoints:
  GET  /groups                    # List groups
  POST /groups                    # Create group
  GET  /subscribers               # List subscribers
  POST /subscribers               # Add subscriber
  POST /subscribers/{id}/groups   # Add to group
```

## Example Usage

```
/mailerlite-setup                              # List groups
/mailerlite-setup list-groups                  # List groups
/mailerlite-setup create-group "AI Guide"      # Create group
/mailerlite-setup add-subscriber user@email.com "AI Guide"
```

## Workflow Integration

When running `/pipeline` or creating guides:
1. Create group: `/mailerlite-setup create-group "Topic Guide"`
2. Get group ID
3. Store in Notion/Airtable for form integration
4. Add subscribers as they sign up

## Environment

```bash
MAILERLITE_API_KEY=your_api_key_here
```
