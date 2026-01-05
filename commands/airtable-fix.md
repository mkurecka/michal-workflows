---
name: airtable-fix
description: Find and process Airtable records with error status. Retry failed operations or fix issues.
arguments:
  - name: table
    description: Table name or ID to check for errors
    required: false
  - name: action
    description: Action to take (list, retry, fix)
    required: false
---

# /airtable-fix - Airtable Error Processing

Find and fix records with error status in Airtable.

## Instructions

### Phase 1: Identify Table
1. If table argument provided, use it
2. If not, check CLAUDE.md for default Airtable config
3. If not found, list available tables and ask user

### Phase 2: Find Errors
1. Query Airtable for records with error status
   - Filter: `{Status} = "Error"` or `{Status} = "Failed"`
2. Display error records:
   - Record ID
   - Error message (if field exists)
   - Last updated
   - Key fields for context

### Phase 3: Process Errors
Based on action parameter:

**list** (default):
- Display all error records
- Show error details
- Suggest fixes

**retry**:
- Re-trigger processing for each error record
- Update status to "Pending" or "Retrying"
- Log retry attempts

**fix**:
- Analyze each error
- Apply automatic fixes where possible
- Update records with fixes
- Mark fixed records as "Fixed" or "Pending"

### Phase 4: Report
- Total errors found
- Errors fixed/retried
- Remaining issues
- Suggested manual actions

## Airtable Config (CLAUDE.md)

```markdown
## Airtable

**Base:** appXXXXXXXX
**Error Tables:**
- ImageRenderers (tblXXXXXX)
- Products (tblYYYYYY)
**Status Field:** Status
**Error Values:** Error, Failed
```

## Example Usage

```
/airtable-fix                          # List errors in default table
/airtable-fix ImageRenderers           # Check specific table
/airtable-fix Products retry           # Retry all product errors
/airtable-fix tblXXXXXX fix            # Auto-fix errors
```

## Common Error Patterns

- **API timeout**: Retry usually works
- **Invalid data**: Needs manual fix
- **Missing field**: Check required fields
- **Rate limit**: Wait and retry
