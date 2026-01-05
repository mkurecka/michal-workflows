---
name: research
description: Research a topic using web search, analyze trends, and compile findings. Saves to Notion.
arguments:
  - name: topic
    description: The topic to research
    required: true
  - name: depth
    description: Research depth (quick, medium, deep)
    required: false
---

# /research - Topic Research

Deep research on any topic with web search and trend analysis.

## Instructions

1. **Web Search**: Search for current information about the topic
   - Recent articles and news
   - Statistics and data
   - Expert opinions
   - Trending angles

2. **Competitor Analysis**: Find existing content on the topic
   - Top-ranking articles
   - Content gaps
   - Unique angles not covered

3. **Trend Analysis**: Check what's trending
   - Google Trends (if accessible)
   - Social media discussions
   - Recent developments

4. **Compile Research**:
   - Key findings (5-10 bullet points)
   - Statistics and data points
   - Quotes from experts
   - Content angles to explore
   - Sources list

5. **Save to Notion**:
   - Create page in research database
   - Title: "[Topic] - Research"
   - Include all findings
   - Tag with topic keywords

## Depth Levels

- **quick**: 5 min, basic overview, 3-5 sources
- **medium**: 15 min, thorough analysis, 8-10 sources (default)
- **deep**: 30 min, comprehensive research, 15+ sources

## Example Usage

```
/research "AI productivity tools"
/research "remote work trends" deep
/research "SaaS pricing strategies" quick
```

## Output Format

```markdown
# Research: [Topic]

## Key Findings
- Finding 1
- Finding 2
...

## Statistics & Data
- Stat 1
- Stat 2
...

## Expert Quotes
> "Quote" - Source

## Content Angles
1. Angle 1
2. Angle 2
...

## Sources
- [Source 1](url)
- [Source 2](url)
```
