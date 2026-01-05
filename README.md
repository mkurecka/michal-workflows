# michal-workflows

Claude Code plugin for workflow automation - git shipping, deployments, Linear issues, and content creation pipelines.

## Installation

```bash
claude plugins install github:mkurecka/michal-workflows
```

## Commands

### Git & Deployment
| Command | Usage | Description |
|---------|-------|-------------|
| `/ship` | `/ship` or `/ship "message"` | Quick commit & push with smart message |
| `/cf-deploy` | `/cf-deploy [env]` | Deploy to Cloudflare Workers/Pages |
| `/linear-next` | `/linear-next [project]` | Fetch and work on next Linear issue |

### Content Creation
| Command | Usage | Description |
|---------|-------|-------------|
| `/pipeline` | `/pipeline "topic"` | Full content pipeline (all platforms) |
| `/research` | `/research "topic" [depth]` | Deep topic research |
| `/article` | `/article "topic" [length]` | Write article/blog post |
| `/instagram` | `/instagram "topic" [type]` | Instagram carousel, posts, reels |
| `/twitter` | `/twitter "topic" [type]` | Twitter threads and tweets |
| `/youtube` | `/youtube "topic" [type]` | YouTube video content |
| `/shorts` | `/shorts "topic" [count]` | TikTok, Shorts, Reels scripts |

## Examples

```bash
# Quick git workflow
/ship                           # Auto-commit and push
/ship "fix login bug"           # Custom message

# Cloudflare deployment
/cf-deploy                      # Deploy to default env
/cf-deploy production           # Deploy to production

# Linear issues
/linear-next                    # Get next issue
/linear-next MKU                # From specific project

# Content creation
/pipeline "AI productivity"     # Full pipeline
/research "AI tools" deep       # Deep research
/article "remote work" long     # Long-form article
/instagram "tips" carousel      # Instagram carousel
/twitter "lessons" thread       # Twitter thread
/youtube "tutorial" both        # Long + shorts
/shorts "hacks" 5 all           # 5 scripts for all platforms
```

## Requirements

- **Linear**: Set `LINEAR_API_KEY` for `/linear-next`
- **Cloudflare**: `wrangler` CLI installed and logged in
- **Content**: Notion and Airtable MCP servers configured

## License

MIT
