---
name: pipeline
description: Full content pipeline. Research topic, create article, generate social media content for all platforms, save to Notion + Airtable.
arguments:
  - name: topic
    description: The topic to research and create content about
    required: true
---

# /pipeline - Content Creation Pipeline

Complete content creation workflow: Research → Article → Social Media → Storage.

## Instructions

Execute these phases in order:

### Phase 1: Research
1. Use WebSearch to find current information about the topic
2. Search YouTube for existing content and angles
3. Check Twitter/X for trending discussions
4. Compile research notes with key findings, statistics, and angles

### Phase 2: Article Creation
1. Generate article outline based on research
2. Write comprehensive article (1500-2500 words)
3. Include:
   - Engaging headline
   - Introduction with hook
   - Main sections with subheadings
   - Practical tips/examples
   - Conclusion with CTA
4. Create Notion page with the article

### Phase 3: Social Media Content

**Instagram Carousel (8-10 slides):**
- Slide 1: Hook/Title
- Slides 2-8: Key points with visuals
- Slide 9: Summary/Recap
- Slide 10: CTA + follow prompt
- Include caption with hashtags

**Twitter/X Thread (8-12 tweets):**
- Tweet 1: Hook that stops scroll
- Tweets 2-10: Value points
- Final tweet: CTA + engagement question
- Include relevant hashtags

**YouTube Video:**
- Title (click-worthy, 60 chars max)
- Description (SEO optimized)
- Full script outline with timestamps
- Thumbnail concept

**Short-Form Content (3-5 each):**
- YouTube Shorts scripts
- TikTok scripts
- Instagram Reels scripts
- Each 30-60 seconds, vertical format

### Phase 4: Storage
1. Create Notion page with all content organized:
   - Research section
   - Article section
   - Instagram section
   - Twitter section
   - YouTube section
   - Short-form section
2. Create Airtable record:
   - Topic name
   - Status: "Draft"
   - Created date
   - Link to Notion page
   - Content types generated

## Output Structure in Notion

```markdown
# [Topic] - Content Package

## Research Notes
[Compiled research]

## Article
[Full article]

## Instagram Carousel
[Slide content + caption]

## Twitter Thread
[All tweets]

## YouTube
[Title, description, script]

## Short-Form Scripts
[Shorts, TikToks, Reels]
```

## Example Usage

```
/pipeline "AI productivity tools for 2024"
/pipeline "How to start a SaaS business"
/pipeline "Best practices for remote work"
```

## After Completion

Ask user:
- Review and edit content in Notion?
- Generate images for carousel?
- Schedule posts?
