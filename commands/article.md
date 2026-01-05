---
name: article
description: Write a full article/blog post on a topic. Can use existing research or start fresh.
arguments:
  - name: topic
    description: The topic for the article
    required: true
  - name: length
    description: Article length (short ~800, medium ~1500, long ~2500 words)
    required: false
  - name: style
    description: Writing style (professional, casual, educational, persuasive)
    required: false
---

# /article - Article Creation

Write a comprehensive article ready for publishing.

## Instructions

### Phase 1: Check for Existing Research
1. Search Notion for existing research on the topic
2. If found, use as foundation
3. If not, do quick research first

### Phase 2: Outline Creation
1. Generate article outline:
   - Headline (compelling, SEO-friendly)
   - Introduction with hook
   - 4-7 main sections
   - Conclusion with CTA
2. Confirm outline with user or proceed

### Phase 3: Write Article
1. **Headline**: Compelling, includes keyword, 60 chars
2. **Meta Description**: 150-160 chars for SEO
3. **Introduction** (100-150 words):
   - Hook that grabs attention
   - State the problem/opportunity
   - Preview what reader will learn
4. **Main Sections**:
   - Clear subheadings (H2, H3)
   - Practical examples
   - Data and statistics
   - Actionable tips
5. **Conclusion** (100-150 words):
   - Summarize key points
   - Clear CTA
   - Encourage engagement

### Phase 4: SEO Optimization
- Include target keyword in title, intro, headings
- Add internal/external link suggestions
- Suggest featured image concept

### Phase 5: Save to Notion
- Create page with full article
- Include meta description
- Tag with topic keywords
- Set status to "Draft"

## Length Guidelines

- **short**: ~800 words, quick read
- **medium**: ~1500 words, standard blog post (default)
- **long**: ~2500 words, comprehensive guide

## Example Usage

```
/article "AI tools for productivity"
/article "remote work tips" short casual
/article "complete guide to SaaS pricing" long professional
```

## Output Format

```markdown
# [Headline]

**Meta Description:** [150-160 chars]

**Target Keyword:** [keyword]

---

[Full article content with proper formatting]

---

## SEO Notes
- Suggested internal links
- Suggested external links
- Featured image concept
```
