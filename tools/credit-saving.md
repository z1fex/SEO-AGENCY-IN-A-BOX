# Credit-Saving Guide

> How to run this SEO agency efficiently on Claude Pro credits.

---

## The 7 Rules

### 1. Load Agents On Demand
Only read the agent file you need right now. Never bulk-load all 75 agents. One agent at a time.

### 2. Vault Before Tools
Before calling Firecrawl or Tavily, check if the data already exists in vault:
- Crawl data <14 days old → reuse it
- Keyword research <30 days old → reuse it
- Competitor analysis <30 days old → reuse it

### 3. Map Before Crawl
Firecrawl `map` is much cheaper than `crawl`. Always map first to assess site size, then crawl with appropriate limits.

### 4. Batch Everything
- Write ALL meta tags for a site in one pass, not page by page
- Write ALL content briefs in one session, not one by one
- Research ALL keywords for a cluster together, not individually
- Generate ALL outreach emails in one batch

### 5. Use Templates
Templates reduce thinking tokens. Pre-structured output means less generation. Always use a template from `templates/` when one exists.

### 6. Be Terse
Deliver the work, not paragraphs explaining the work. Skip preamble and summaries unless the client asks for them.

### 7. Combine Related Work
If Strategy (roadmap) and Audit (priority matrix) serve the same objective, produce one combined deliverable instead of two separate runs.

---

## Credit Cost Estimates by Workflow

| Workflow | Steps | Base Cost | With Optimization |
|----------|-------|-----------|-------------------|
| Client Onboarding | Interview + 5 files | Low | Low |
| Full SEO Audit | 12 steps | Very High | High (reuse data) |
| Keyword Strategy | 7 steps | High | Medium (batch searches) |
| Content Sprint | 8 steps | High | Medium (batch writing) |
| Link Building Campaign | 6 steps | Medium | Medium |
| Monthly Report | 5 steps | Medium | Low (vault compilation) |
| Competitor Teardown | 6 steps | High | Medium (cache data) |
| Local SEO Setup | 5 steps | Medium | Low-Medium |
| E-commerce Audit | 6 steps | High | Medium |
| Quarterly Review | 6 steps | Medium | Low (vault data) |

---

## Firecrawl Credit Tips

| Instead of... | Do this... | Savings |
|---------------|-----------|---------|
| Crawling a 10,000 page site | Map first, then crawl with `limit: 500` focused on key sections | 95% |
| Re-crawling every week | Cache crawl data in vault, reuse for 14 days | 100% per reuse |
| Crawling for a quick check | Use Web Fetch on the specific page | 100% (Web Fetch is free) |
| Scraping 50 pages individually | Crawl the section with `includePaths` | Varies |

## Tavily Credit Tips

| Instead of... | Do this... | Savings |
|---------------|-----------|---------|
| Searching each keyword separately | Search for keyword clusters/themes together | 70-80% |
| Advanced depth for quick checks | Use basic depth, save advanced for thorough research | 50% |
| Re-researching same topic | Check vault first — save all results | 100% per reuse |
| Searching for data you already have | Read vault files first | 100% |
