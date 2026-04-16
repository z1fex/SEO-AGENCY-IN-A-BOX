# Tool Usage Guide

## Available Tools

This agency uses four categories of tools. Every agent must know which tools to use and when.

---

## 1. Firecrawl (MCP Server)

### What It Does
Firecrawl is a web crawling and scraping API. It can crawl entire websites, scrape individual pages, map site structures, search the web, and extract structured data.

### Operations

#### `firecrawl_crawl` — Crawl an Entire Site
**Use when:** Full site audit, URL inventory, finding broken pages, redirect chains, orphan pages
**Returns:** All pages with their content, metadata, links, status codes
**Cost:** High (uses many credits — cache results in vault)

```
Input: URL + optional filters (include/exclude patterns, max pages)
Output: All discovered pages with content and metadata
```

**Best practices:**
- Set `maxDepth` to limit crawl scope for large sites
- Use `includePaths` to focus on specific sections (e.g., `/blog/*`)
- Save raw crawl data to `vault/10-Technical/[client]/crawl-data/`
- Never re-crawl a site if data is <14 days old — reuse from vault

#### `firecrawl_scrape` — Scrape a Single Page
**Use when:** Analyzing a specific page, extracting competitor content, checking a landing page
**Returns:** Page content in markdown, metadata (title, description, OG tags), links

```
Input: Single URL
Output: Markdown content + metadata
```

**Best practices:**
- Use for competitor page analysis (extract their title tags, H1s, content structure)
- Use for checking specific pages flagged in audits
- Lighter than a full crawl — preferred for spot checks

#### `firecrawl_map` — Map Site URLs
**Use when:** Quick site structure overview, comparing against sitemap, finding URL patterns
**Returns:** List of all URLs on the site (no content)

```
Input: URL
Output: List of discovered URLs
```

**Best practices:**
- Use BEFORE crawl to assess site size and plan crawl scope
- Compare against XML sitemap to find discrepancies
- Much cheaper than full crawl — use as first step

#### `firecrawl_search` — Search the Web
**Use when:** Finding specific types of pages (resource pages for link building, competitor sites)
**Returns:** Search results with extracted content

```
Input: Search query
Output: Relevant pages with content
```

#### `firecrawl_extract` — Extract Structured Data
**Use when:** Pulling specific data from pages (product prices, feature lists, competitor pricing)
**Returns:** Structured data based on your extraction schema

```
Input: URL(s) + extraction schema
Output: Structured JSON data matching your schema
```

---

## 2. Tavily (MCP Server)

### What It Does
Tavily is an AI-powered search engine optimized for research. It returns relevant, clean results with source extraction.

### Operations

#### `tavily_search` — AI-Powered Search
**Use when:** Keyword research, topic discovery, SERP analysis, trend spotting, general research
**Returns:** Search results with titles, URLs, and content snippets

```
Input: Search query + optional parameters (search_depth, include_domains, topic)
Output: Ranked results with extracted content
```

**Best practices:**
- Use `search_depth: "advanced"` for thorough keyword research
- Use `include_domains` to focus on specific sources (e.g., industry publications)
- Use `topic: "news"` for algorithm update monitoring
- Combine related queries to save credits (e.g., research 5 related keywords in context)
- Save all research results to vault for reuse

#### `tavily_extract` — Extract Content from URLs
**Use when:** Deep-reading specific pages, summarizing competitor content, research compilation
**Returns:** Extracted and summarized content from provided URLs

```
Input: List of URLs
Output: Extracted content from each URL
```

---

## 3. Web Fetch (Built-in Claude Code)

### What It Does
Fetches and reads any webpage. Built into Claude Code — no API key needed.

### Use When
- **Validating live pages** — Check if a page loads, check redirects
- **Reading robots.txt** — Fetch and analyze robots.txt files
- **Reading sitemaps** — Fetch and parse XML sitemaps
- **Checking schema** — Fetch a page and inspect structured data
- **Quick page checks** — When you need to see one specific page (lighter than Firecrawl scrape)

### Best Practices
- Preferred for single-page validation tasks
- Use for checking implementation after recommending fixes
- Good for fetching structured data files (robots.txt, sitemap.xml, JSON-LD)

---

## 4. Web Search (Built-in Claude Code)

### What It Does
General web search. Returns search results from the web.

### Use When
- **Algorithm updates** — Search for latest Google algorithm changes
- **Industry news** — Current events in the client's industry
- **General research** — When you need broad information
- **Fact checking** — Verify claims and statistics

### Best Practices
- Use for general research, NOT for structured keyword research (use Tavily for that)
- Good for checking if a piece of news or trend is real
- Use for algorithm update monitoring

---

## Tool Decision Tree

```
Need to analyze a website?
├── Entire site? → Firecrawl crawl (check vault first!)
├── Site structure only? → Firecrawl map
├── One specific page? → Firecrawl scrape OR Web Fetch
└── Structured data from pages? → Firecrawl extract

Need to research something?
├── Keyword research? → Tavily search
├── SERP analysis? → Tavily search
├── Topic/trend research? → Tavily search
├── General news/info? → Web Search
└── Deep-read a specific article? → Tavily extract OR Web Fetch

Need to validate something?
├── Page loads/redirects? → Web Fetch
├── Schema markup present? → Web Fetch
├── Robots.txt/sitemap? → Web Fetch
└── Implementation check? → Web Fetch
```

---

## Tool Priority Order

Always follow this order:

1. **Check vault first** — Does the data already exist? Is it <30 days old? Use it.
2. **Use the lightest tool** — Map before crawl. Web Fetch before Firecrawl scrape.
3. **Cache everything** — Save tool results to vault for future use.
4. **Batch operations** — Combine related searches/scrapes into fewer calls.

---

## Credit Management

| Tool | Credit Cost | Use Sparingly? |
|------|-------------|----------------|
| Firecrawl crawl | High | Yes — cache results, set max pages |
| Firecrawl scrape | Medium | Moderate — batch when possible |
| Firecrawl map | Low | No — use freely as scout |
| Firecrawl search | Medium | Moderate |
| Firecrawl extract | Medium | Moderate |
| Tavily search | Low-Medium | No — but save results to vault |
| Tavily extract | Medium | Moderate |
| Web Fetch | Free | No — use as much as needed |
| Web Search | Free | No — use as much as needed |
