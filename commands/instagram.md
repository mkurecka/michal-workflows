---
name: instagram
description: Create Instagram content - carousel posts, single posts, or reels scripts.
arguments:
  - name: topic
    description: The topic for Instagram content
    required: true
  - name: type
    description: Content type (carousel, post, reel, all)
    required: false
---

# /instagram - Instagram Content Creation

Create engaging Instagram content ready to post.

## Instructions

### Phase 1: Check Existing Content
1. Search Notion for existing research/article on topic
2. Use as foundation if available
3. Otherwise, extract key points for Instagram format

### Phase 2: Carousel Post (if type=carousel or all)
Create 8-10 slide carousel:

1. **Slide 1 - Cover**:
   - Bold headline that stops scroll
   - Eye-catching design concept
   - Brand colors/style

2. **Slides 2-8 - Content**:
   - One key point per slide
   - Short, punchy text (max 30 words)
   - Visual suggestion for each

3. **Slide 9 - Summary**:
   - Recap key points
   - Reinforce main message

4. **Slide 10 - CTA**:
   - Clear call to action
   - "Save this post"
   - "Follow for more"
   - "Comment your thoughts"

5. **Caption**:
   - Hook in first line
   - Expand on content
   - Engagement question
   - 20-30 relevant hashtags

### Phase 3: Single Post (if type=post or all)
- Visual concept description
- Engaging caption (2200 char max)
- Hashtag set

### Phase 4: Reels Scripts (if type=reel or all)
Create 3 reel scripts:
- 15-30 seconds each
- Hook in first 2 seconds
- Trending audio suggestions
- Text overlay notes
- CTA at end

### Phase 5: Save to Notion
- Create page with all content
- Tag with topic + "instagram"
- Include visual notes for designer

## Example Usage

```
/instagram "productivity tips"
/instagram "AI tools" carousel
/instagram "quick tip" reel
/instagram "product launch" all
```

## Output Format

```markdown
# Instagram: [Topic]

## Carousel
### Slide 1 (Cover)
**Text:** [Headline]
**Visual:** [Design concept]

### Slide 2
**Text:** [Point 1]
**Visual:** [Concept]
...

### Caption
[Full caption with hashtags]

---

## Reels
### Reel 1: [Hook]
**Duration:** 20s
**Audio:** [Suggestion]
**Script:**
[Second by second script]

### Reel 2: [Hook]
...
```
