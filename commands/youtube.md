---
name: youtube
description: Research YouTube for a topic and generate video content (title, description, script, thumbnail ideas).
arguments:
  - name: topic
    description: The topic for YouTube content
    required: true
  - name: type
    description: Content type (long, short, both)
    required: false
---

# /youtube - YouTube Content Creation

Research YouTube and create video content package.

## Instructions

### Phase 1: YouTube Research
1. Search YouTube for existing content on the topic
2. Analyze top-performing videos:
   - Titles that work
   - Thumbnail styles
   - Video length
   - Engagement patterns
3. Identify content gaps and unique angles
4. Note successful hooks and CTAs

### Phase 2: Long-Form Content (if type=long or both)
1. **Title**: Click-worthy, 60 chars max, includes keyword
2. **Description**: SEO optimized, 200+ words
   - Hook in first 2 lines
   - Key points
   - Timestamps
   - Links and CTAs
3. **Script Outline**:
   - Hook (0:00-0:30)
   - Intro (0:30-1:00)
   - Main content with timestamps
   - CTA and outro
4. **Thumbnail Concept**: Visual description, text overlay

### Phase 3: Short-Form Content (if type=short or both)
Generate 3-5 YouTube Shorts scripts:
- 30-60 seconds each
- Vertical format
- Hook in first 3 seconds
- One clear point per short
- Strong CTA at end

### Phase 4: Save to Notion
- Create page with all content
- Include research findings
- Tag with topic + "youtube"

## Example Usage

```
/youtube "how to use AI for productivity"
/youtube "best coding practices" long
/youtube "quick tips" short
/youtube "startup mistakes" both
```

## Output Structure

```markdown
# YouTube: [Topic]

## Research Insights
- Top videos analysis
- What's working
- Content gaps

## Long-Form Video
### Title Options
1. Option 1
2. Option 2

### Description
[Full description]

### Script Outline
[Timestamped outline]

### Thumbnail Concept
[Visual description]

## Shorts (3-5)
### Short 1: [Hook]
[Script]

### Short 2: [Hook]
[Script]
...
```
