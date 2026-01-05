---
name: snap-render
description: Render SnapTemplate content - carousels, images, PDFs. Trigger image generation via API.
arguments:
  - name: action
    description: Action (render, bulk, pdf, preview)
    required: false
  - name: template
    description: Template ID or name
    required: false
---

# /snap-render - SnapTemplate Operations

Render images, carousels, and PDFs using SnapTemplate API.

## Instructions

### Phase 1: Identify Template
1. If template argument provided, use it
2. If not, list available templates
3. Check for template in current context

### Phase 2: Actions

**render** (default):
1. Get template by ID or name
2. Prepare variables (from content or ask user)
3. Call render API:
   ```
   POST /api/render
   {
     "templateId": "...",
     "variables": { ... }
   }
   ```
4. Return rendered image URL

**bulk**:
1. Get list of content items to render
2. For each item:
   - Map content to template variables
   - Call render API
   - Track progress
3. Report results (success/failed counts)

**pdf**:
1. Render all slides of a carousel
2. Combine into PDF
3. Call PDF generation endpoint:
   ```
   POST /api/pdf
   {
     "templateId": "...",
     "slides": [...]
   }
   ```
4. Return PDF URL

**preview**:
1. Open template in browser
2. Show preview with sample data

### Phase 3: Error Handling
- Track failed renders
- Retry on timeout
- Log to Airtable if configured

## API Endpoints

```
Base: https://snaptemplate-api.kureckamichal.workers.dev

GET  /templates              # List templates
GET  /templates/:id          # Get template
POST /api/render             # Render single image
POST /api/bulk-render        # Render multiple
POST /api/pdf                # Generate PDF
```

## Example Usage

```
/snap-render                         # Render current template
/snap-render render carousel-1       # Render specific template
/snap-render bulk                    # Bulk render from queue
/snap-render pdf my-carousel         # Generate PDF
/snap-render preview                 # Preview in browser
```

## Template Variables

Templates use Mustache syntax:
```json
{
  "slide_number": 1,
  "title": "Main Title",
  "content": "Body text",
  "image_url": "https://...",
  "cta_text": "Learn More"
}
```

## Integration

- Content from Notion/Airtable
- Images stored in Cloudflare R2
- Status tracked in Airtable
