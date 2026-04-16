# Tavily Tool Guide

> How agents in this agency use Tavily for AI-powered search and research.

---

## Setup

Tavily runs as an MCP server. Add this to your Claude Code MCP settings:

```json
{
  "mcpServers": {
    "tavily": {
      "command": "npx",
      "args": ["-y", "tavily-mcp@latest"],
      "env": {
        "TAVILY_API_KEY": "tvly-your-key-here"
      }
    }
  }
}
```

Get your API key at [tavily.com](https://tavily.com)

### Plans
| Plan | Searches/Month | Best For |
|------|---------------|----------|
| Free | 1,000 | Testing, light research |
| Basic | 1,000 | Light usage |
| Pro | Higher volume | Full agency operations |

---

## Operations

### 1. `tavily_search` — AI-Powered Search

**What it does:** Searches the web using AI to return the most relevant results with clean content extraction. Better than traditional search for research tasks.

**Parameters:**
- `query` — The search query
- `search_depth` — `"basic"` (fast) or `"advanced"` (thorough, uses more credits)
- `topic` — `"general"` or `"news"` (optimized for recent news)
- `include_domains` — Limit to specific sites (e.g., `["searchengineland.com", "moz.com"]`)
- `exclude_domains` — Block specific sites
- `max_results` — Number of results (default 5, max 20)

**When to use:**
- Keyword research and topic discovery
- SERP analysis for target keywords
- Algorithm update monitoring
- Industry trend research
- Competitor strategy research
- Finding PAA (People Also Ask) questions
- Checking AI Overview triggers

**Credit cost:** 1 credit per basic search, 2 per advanced

**Example use cases by team:**

| Team | Use Case | Query Example |
|------|----------|---------------|
| Keywords | Seed keyword discovery | `"best [product] for [audience] 2026"` |
| Keywords | Question research | `"what is [topic] how to [action]"` |
| Keywords | SERP analysis | `"[target keyword]"` with advanced depth |
| Content | Topic research | `"[topic] trends statistics data 2026"` |
| Content | Competitor content | `"[topic] guide comprehensive"` |
| Research | Algorithm updates | `"google algorithm update [month] 2026"` with topic: news |
| Research | Industry trends | `"[industry] trends 2026 2027"` |
| AEO | AI Overview research | `"[query] AI overview featured snippet"` |
| AEO | Perplexity research | `"[brand] site:perplexity.ai"` |
| Links | Prospect finding | `"[topic] resources links roundup"` |
| Links | PR opportunities | `"[industry] journalist reporter"` with topic: news |
| Local | Local research | `"[service] [city] guide local"` |

---

### 2. `tavily_extract` — Extract Content from URLs

**What it does:** Reads and extracts content from one or more URLs, returning clean text and summaries.

**When to use:**
- Deep-reading competitor articles
- Extracting data from research sources
- Compiling information from multiple pages
- Reading long-form content for analysis

**Credit cost:** Medium (varies by page count)

**Example use cases:**
- "Summarize the top 5 articles about [topic]" → extract all 5 URLs
- "What does this competitor's pricing page say?" → extract the URL
- "Compile data from these 3 research reports" → extract all 3

---

## Team-to-Tool Mapping

| Team | Primary Use | Frequency |
|------|------------|-----------|
| Keyword Research | Keyword discovery, SERP analysis, intent verification | Heavy |
| Content SEO | Topic research, competitor content, trends | Heavy |
| Research | Algorithm updates, trends, AI landscape | Heavy |
| AEO | AI Overview checks, entity research, Perplexity analysis | Heavy |
| Competitor Analysis | Strategy research, SERP tracking | Medium |
| Link Building | Prospect finding, PR research | Medium |
| Local SEO | Local market research, citation discovery | Medium |
| Analytics | SERP position checks | Light |
| Strategy | Market research, competitive strategy | Light |

---

## Best Practices

### Search Query Optimization
- **Be specific** — `"best CRM software for small business 2026"` beats `"CRM software"`
- **Use modifiers** — Add "guide", "statistics", "trends", "vs", "review" for different intent
- **Use advanced depth** — For keyword research and competitive analysis, always use `search_depth: "advanced"`
- **Filter domains** — Use `include_domains` for authoritative sources, `exclude_domains` to skip noise

### Credit Conservation
1. **Check vault first** — If research exists from <30 days ago, reuse it
2. **Combine queries** — Research related keywords in one contextual search instead of separate searches
3. **Use basic depth** — For quick checks, basic is fine. Save advanced for thorough research
4. **Save everything** — Every Tavily result should be saved to vault for future reuse
5. **Batch research** — Do all keyword research for a cluster in one session, not keyword by keyword

### Data Quality
- Tavily returns AI-curated results — they're generally high quality
- Always cross-reference critical data with a second source
- For keyword volumes: Tavily doesn't provide exact volumes — use it for topic discovery and SERP analysis, not volume estimates
- For rankings: Tavily shows current SERP results, not historical — save snapshots to vault for trend tracking
