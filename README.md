# michal-workflows

Claude Code plugin for workflow automation - git shipping, deployments, Linear issues, content creation, and more.

## Installation

```bash
claude plugins install github:mkurecka/michal-workflows
```

## Commands (12 total)

### Git & Deployment
| Command | Usage | Description |
|---------|-------|-------------|
| `/ship` | `/ship` or `/ship "message"` | Quick commit & push with smart message |
| `/cf-deploy` | `/cf-deploy [env]` | Deploy to Cloudflare Workers/Pages |
| `/vps-deploy` | `/vps-deploy [server]` | Deploy to VPS via SSH |
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

### SEO
| Command | Usage | Description |
|---------|-------|-------------|
| `/seo-optimize` | `/seo-optimize [scope]` | Improve project SEO |

## Examples

```bash
# Git & Deployment
/ship                           # Auto-commit and push
/ship "fix login bug"           # Custom message
/cf-deploy production           # Deploy to Cloudflare
/vps-deploy aicko               # Deploy to VPS

# Linear workflow
/linear-next                    # Get next issue
/linear-next MKU                # From specific project

# Content creation - full pipeline
/pipeline "AI productivity"     # All platforms at once

# Content creation - individual steps
/research "AI tools" deep       # Deep research
/article "remote work" long     # Long-form article
/instagram "tips" carousel      # Instagram carousel
/twitter "lessons" thread       # Twitter thread
/youtube "tutorial" both        # Long + shorts
/shorts "hacks" 5 all           # 5 scripts for all platforms

# SEO
/seo-optimize full              # Full SEO audit
/seo-optimize meta              # Just meta tags
```

## Requirements

| Command | Requires |
|---------|----------|
| `/linear-next` | `LINEAR_API_KEY` env variable |
| `/cf-deploy` | `wrangler` CLI installed |
| `/vps-deploy` | SSH access configured |
| Content commands | Notion + Airtable MCP servers |

## License

MIT
