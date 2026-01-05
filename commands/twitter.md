---
name: twitter
description: Create Twitter/X content - threads, single tweets, or tweet series.
arguments:
  - name: topic
    description: The topic for Twitter content
    required: true
  - name: type
    description: Content type (thread, tweet, series)
    required: false
---

# /twitter - Twitter/X Content Creation

Create engaging Twitter/X content optimized for engagement.

## Instructions

### Phase 1: Check Existing Content
1. Search Notion for existing research/article on topic
2. Use as foundation if available
3. Extract tweetable insights

### Phase 2: Thread (if type=thread or default)
Create 8-12 tweet thread:

1. **Tweet 1 - Hook**:
   - Stop the scroll
   - Promise value
   - Use numbers or bold claim
   - End with "🧵" or "Thread:"

2. **Tweets 2-10 - Value**:
   - One key point per tweet
   - Max 280 chars each
   - Use line breaks for readability
   - Include relevant emojis sparingly

3. **Tweet 11 - Summary**:
   - Recap main points
   - Reinforce key message

4. **Tweet 12 - CTA**:
   - Ask for retweet
   - Engagement question
   - Follow CTA
   - Link to full content (if applicable)

### Phase 3: Single Tweets (if type=tweet)
Create 5 standalone tweets:
- Each can be posted independently
- Different angles on the topic
- Mix of formats (tips, questions, statements)

### Phase 4: Tweet Series (if type=series)
Create themed series for posting over days:
- Day 1: Problem statement
- Day 2: Solution overview
- Day 3: Deep dive
- Day 4: Case study/example
- Day 5: CTA/conclusion

### Phase 5: Save to Notion
- Create page with all content
- Tag with topic + "twitter"
- Include posting schedule suggestion

## Example Usage

```
/twitter "AI productivity tips"
/twitter "startup lessons" thread
/twitter "quick tips" tweet
/twitter "product launch" series
```

## Output Format

```markdown
# Twitter: [Topic]

## Thread
### Tweet 1 (Hook)
[Tweet text]

### Tweet 2
[Tweet text]
...

### Tweet 12 (CTA)
[Tweet text]

---

## Standalone Tweets
### Tweet A
[Text]

### Tweet B
[Text]
...

---

## Posting Schedule
- Best times to post
- Thread: [Day/Time]
- Follow-up tweets: [Schedule]
```
