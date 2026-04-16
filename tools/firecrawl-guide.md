# Firecrawl Tool Guide

> How agents in this agency use Firecrawl for web crawling, scraping, and data extraction.

---

## Setup

Firecrawl runs as an MCP server. Add this to your Claude Code MCP settings:

```json
{
  "mcpServers": {
    "firecrawl": {
      "command": "npx",
      "args": ["-y", "firecrawl-mcp"],
      "env": {
        "FIRECRAWL_API_KEY": "fc-your-key-here"
      }
    }
  }
}
```

Get your API key at [firecrawl.dev](https://firecrawl.dev)

### Plans
| Plan | Credits/Month | Best For |
|------|---------------|----------|
| Free | 500 | Testing, small sites |
| Hobby ($16/mo) | 3,000 | Small agency, 1-3 clients |
| Standard ($83/mo) | 250,000 | Full agency operations |

---

## Operations

### 1. `firecrawl_map` — Map Site URLs (Cheapest)

**What it does:** Returns a list of all discoverable URLs on a site without crawling page content.

**When to use:**
- ALWAYS use before `firecrawl_crawl` to assess site size
- Compare against XML sitemap to find discrepancies
- Quick site structure overview
- URL pattern analysis

**Credit cost:** Low (1 credit)

**Example use cases:**
- "How big is this site?" → map it first
- "Does their sitemap match reality?" → map + compare to sitemap.xml
- "What URL patterns do they use?" → map and analyze

**Tips:**
- Use the `search` parameter to filter URLs (e.g., only blog pages)
- Save results to vault — reuse for 14+ days

---

### 2. `firecrawl_scrape` — Scrape a Single Page (Medium)

**What it does:** Extracts content from one page in clean markdown format, plus metadata (title, description, OG tags, links).

**When to use:**
- Analyzing a specific competitor page
- Extracting title tags, H1s, meta descriptions
- Checking page content and structure
- Validating specific pages flagged in audits

**Credit cost:** Medium (1 credit per page)

**Example use cases:**
- "What keywords is this competitor page targeting?" → scrape, extract title/H1/H2s
- "What's the content structure of the top-ranking page?" → scrape, analyze headings
- "Check if this page has schema markup" → scrape, look for JSON-LD

**Tips:**
- Use `formats: ["markdown"]` for clean content extraction
- Use `onlyMainContent: true` to skip headers/footers/sidebars
- Batch multiple scrapes when analyzing competitor pages

---

### 3. `firecrawl_crawl` — Crawl Entire Site (Most Expensive)

**What it does:** Follows links and crawls multiple pages, returning content and metadata for each.

**When to use:**
- Full site technical audit
- Complete URL inventory
- Finding broken links, redirect chains, orphan pages
- Content audit of all pages

**Credit cost:** High (1 credit per page crawled)

**Example use cases:**
- "Audit this client's site" → crawl with appropriate limits
- "Find all broken pages" → crawl, filter for 4xx/5xx
- "Map the internal link structure" → crawl, analyze link data

**Tips:**
- ALWAYS `map` first to know the site size
- Set `limit` to control how many pages to crawl
- Use `includePaths` to focus on specific sections (e.g., `/blog/*`)
- Use `excludePaths` to skip irrelevant sections (e.g., `/wp-admin/*`, `/cart/*`)
- Set `maxDepth` to limit crawl depth
- Save crawl data to `vault/10-Technical/[client]/crawl-data/` — NEVER re-crawl if data is <14 days old

---

### 4. `firecrawl_search` — Search the Web (Medium)

**What it does:** Searches the web and returns results with extracted content.

**When to use:**
- Finding specific types of pages (resource pages for link building)
- Discovering competitor sites
- Researching link building prospects

**Credit cost:** Medium

**Example use cases:**
- "Find resource pages about [topic]" → search with targeted query
- "Find sites that link to [competitor]" → search for link sources

---

### 5. `firecrawl_extract` — Extract Structured Data (Medium)

**What it does:** Uses LLM extraction to pull structured data from pages based on a schema you define.

**When to use:**
- Extracting product data from competitor e-commerce sites
- Pulling pricing information
- Building structured comparison tables

**Credit cost:** Medium (more expensive than scrape due to LLM processing)

**Example use cases:**
- "Compare pricing across competitors" → extract pricing schema
- "Build a feature comparison table" → extract features from each site

---

## Team-to-Tool Mapping

| Team | Primary Operations | Common Use Case |
|------|-------------------|-----------------|
| Technical SEO | crawl, map | Full site audits |
| Keyword Research | scrape | Competitor page keyword extraction |
| Content SEO | scrape | Competitor content analysis |
| Link Building | crawl, search | Prospect discovery, broken link finding |
| Competitor Analysis | crawl, map, scrape | Full competitor intelligence |
| E-commerce SEO | crawl, scrape, extract | Product page audits |
| AEO | scrape | Analyzing AI-cited content |
| Local SEO | scrape | Competitor GBP/local page analysis |

---

## Credit-Saving Rules

1. **Map before crawl** — Always assess site size before committing to a full crawl
2. **Cache everything** — Save results to vault; reuse if <14 days old
3. **Set limits** — Never crawl unlimited; set `limit` based on site size
4. **Use filters** — `includePaths`/`excludePaths` to avoid crawling irrelevant pages
5. **Scrape over crawl** — If you only need 5-10 pages, scrape individually instead of crawling
6. **Batch scrapes** — If you need to scrape 20 competitor pages, do it in one session
