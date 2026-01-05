---
name: snap-render
description: SnapTemplate rendering. Use when user wants to render templates, generate carousels, create PDFs, or work with SnapTemplate.
---

# Snap Render - Template Rendering

Render SnapTemplate images, carousels, and PDFs.

## When to Use

Trigger on:
- "render template"
- "generate carousel"
- "snaptemplate"
- "create pdf from template"
- "bulk render"

## Workflow

1. **Template**: Identify by ID or name
2. **Variables**: Prepare content data
3. **Render**: Call SnapTemplate API
4. **Output**: Image URL or PDF

## Actions

- render: Single image
- bulk: Multiple renders
- pdf: Generate PDF
- preview: Open in browser
