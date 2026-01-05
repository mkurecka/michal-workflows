---
name: shorts
description: Create short-form video scripts for TikTok, YouTube Shorts, and Instagram Reels.
arguments:
  - name: topic
    description: The topic for short-form content
    required: true
  - name: count
    description: Number of scripts to generate (default 5)
    required: false
  - name: platform
    description: Platform focus (tiktok, youtube, reels, all)
    required: false
---

# /shorts - Short-Form Video Scripts

Create viral short-form video scripts for all platforms.

## Instructions

### Phase 1: Research Trends
1. Check current trending formats
2. Identify hooks that work
3. Note popular audio trends (if known)

### Phase 2: Generate Scripts
Create specified number of scripts (default 5):

**For Each Script Include:**

1. **Hook** (0-3 seconds):
   - Stop the scroll immediately
   - Pattern interrupt
   - Bold statement or question

2. **Setup** (3-10 seconds):
   - Context
   - The problem/situation

3. **Content** (10-45 seconds):
   - Main value/entertainment
   - Keep it punchy
   - Visual transitions

4. **Payoff** (45-55 seconds):
   - Resolution
   - Key takeaway

5. **CTA** (55-60 seconds):
   - Follow
   - Comment
   - Share

**Script Metadata:**
- Duration target
- Platform optimization notes
- Audio suggestion
- Text overlay notes
- Hashtag suggestions

### Phase 3: Platform Optimization

**TikTok:**
- Trending sounds
- Duet/stitch potential
- TikTok-specific hashtags

**YouTube Shorts:**
- SEO title
- Description
- Subscribe CTA

**Instagram Reels:**
- Caption
- Hashtags
- Stories tie-in

### Phase 4: Save to Notion
- Create page with all scripts
- Tag with topic + platform
- Include production notes

## Example Usage

```
/shorts "coding tips"
/shorts "AI tools" 3 tiktok
/shorts "productivity hacks" 5 all
/shorts "startup advice" 10
```

## Output Format

```markdown
# Shorts: [Topic]

## Script 1: [Hook Title]
**Duration:** 45s
**Platform:** All
**Audio:** [Suggestion]

### Hook (0-3s)
[Text/Action]

### Setup (3-10s)
[Text/Action]

### Content (10-45s)
[Detailed script with visuals]

### CTA (45-60s)
[Text/Action]

**Text Overlays:**
- 0:03 - "[Text]"
- 0:15 - "[Text]"
...

**Hashtags:** #tag1 #tag2 ...

---

## Script 2: [Hook Title]
...
```
