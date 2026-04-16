# Content SEO Team

> Plan, create, and optimize content that ranks in search engines AND converts visitors into customers, with every piece built on keyword research and competitive intelligence.

## Team Overview

The Content SEO Team is the production engine of the agency. While other teams gather intelligence and fix infrastructure, this team produces the assets that directly compete in search results: blog posts, landing pages, meta tags, FAQ content, and content strategies. Every piece of content this team creates is built on a foundation of keyword research, competitor analysis, and search intent data. No content is ever written on instinct alone.

This team sits in the **Execution Layer** of the agency hierarchy. It runs during Phase 3 (Audit, for content auditing) and Phase 5 (Execute, for content creation and optimization). It is the largest team in the agency because content is the primary vehicle for SEO growth — technical fixes and links support content, but content is what ranks.

The team follows a structured pipeline: strategy first, then planning, then briefs, then writing, then optimization, then performance analysis. The Content Strategist sets the direction, the Brief Writer creates detailed specifications, and the writers execute. No writer ever starts without a brief. No brief is ever written without keyword data. This discipline is what separates agency-grade content from generic AI output.

## Agents

| Agent | File | Role |
|-------|------|------|
| Content Strategist | `agents/content/content-strategist.md` | Analyzes keyword clusters, competitor content, and client goals to build the overall content strategy — what to create, in what order, and why |
| Content Calendar Planner | `agents/content/content-calendar-planner.md` | Translates the content strategy into a time-bound publishing calendar with deadlines, assignments, and content types |
| Content Brief Writer | `agents/content/brief-writer.md` | Creates detailed content briefs for each piece — target keywords, search intent, outline, competitor analysis, word count target, internal links, CTA |
| SEO Blog Writer | `agents/content/seo-blog-writer.md` | Writes full-length SEO blog posts from briefs, following E-E-A-T guidelines, proper heading hierarchy, and natural keyword integration |
| Landing Page Copywriter | `agents/content/landing-page-copywriter.md` | Writes conversion-focused landing page copy optimized for both search engines and user conversion, with clear CTAs and benefit-driven structure |
| Meta Tag Writer | `agents/content/meta-tag-writer.md` | Writes optimized title tags and meta descriptions at scale for existing and new pages, following character limits and click-through-rate best practices |
| FAQ & PAA Writer | `agents/content/faq-paa-writer.md` | Creates FAQ content targeting People Also Ask boxes and AI Overview citations, using question-and-answer format with schema markup |
| Content Gap Analyst | `agents/content/content-gap-analyst.md` | Audits existing site content against keyword clusters and competitor coverage to find topics the client should cover but does not |
| Content Optimizer | `agents/content/content-optimizer.md` | Rewrites and improves existing underperforming content — updates outdated information, improves keyword targeting, strengthens E-E-A-T signals, adds internal links |
| Content Performance Analyst | `agents/content/content-performance-analyst.md` | Analyzes which content is performing, which is underperforming, and why — provides data-driven recommendations for content iteration |

## When to Run This Team

- **Content sprint** — When executing the content portion of the SEO roadmap (monthly or quarterly)
- **New client content strategy** — After keyword research to build the initial content plan
- **Content gap found** — When the Keyword Research or Competitor Analysis teams identify content opportunities
- **Content audit** — When evaluating existing site content for optimization opportunities
- **Existing content decline** — When previously ranking content starts losing positions
- **New product or service launch** — New offerings need supporting content (landing pages, blogs, FAQs)
- **Seasonal content planning** — Preparing content for seasonal search demand spikes
- **Meta tag cleanup** — When the Technical SEO audit reveals missing or duplicate title tags and meta descriptions
- **AEO content needs** — When the AEO team identifies questions and topics that need FAQ or authoritative content

## Execution Order

```
Step 1: Content Strategist
   │
   │  Reads keyword clusters from vault/03-Research/, competitor content
   │  from vault/06-Competitors/, and client goals from vault/01-Clients/.
   │  Produces the content strategy: what topics to cover, content types,
   │  priority order, and strategic rationale.
   │  Saves to vault/04-Content/[client]/content-strategy.md
   │
   ▼
Step 2: Content Calendar Planner
   │
   │  Translates strategy into a time-bound calendar. Maps content pieces
   │  to weeks/months, assigns content types, and sets publishing cadence.
   │  Saves to vault/04-Content/[client]/content-calendar.md
   │
   ▼
Step 3: Content Brief Writer
   │
   │  Creates a detailed brief for each content piece. Each brief includes:
   │  target keywords, search intent, competitor analysis, suggested outline,
   │  word count target, internal linking targets, CTA strategy, E-E-A-T hooks.
   │  Saves to vault/04-Content/[client]/briefs/
   │
   ▼
Step 4a: SEO Blog Writer (parallel with 4b)
   │
   │  Writes full blog posts from briefs. Follows the outline, integrates
   │  keywords naturally, uses proper heading hierarchy (H1 → H2 → H3),
   │  includes internal links, and structures for featured snippets.
   │  Saves to output/[client]/[date]/content/blogs/
   │
   ▼
Step 4b: Landing Page Copywriter (parallel with 4a)
   │
   │  Writes conversion-focused landing page copy from briefs. Balances
   │  SEO keyword targeting with persuasive copywriting and clear CTAs.
   │  Saves to output/[client]/[date]/content/landing-pages/
   │
   ▼
Step 5: Meta Tag Writer
   │
   │  Writes optimized title tags and meta descriptions for all new and
   │  existing pages. Follows character limits (title: 50-60 chars,
   │  description: 150-160 chars). Includes target keyword and CTA.
   │  Saves to output/[client]/[date]/content/meta-tags.md
   │
   ▼
Step 6: FAQ & PAA Writer
   │
   │  Creates FAQ content targeting People Also Ask queries and AI Overview
   │  citations. Generates FAQ schema (JSON-LD) for each FAQ section.
   │  Saves to output/[client]/[date]/content/faqs/
   │
   ▼
Step 7: Content Optimizer (for existing content)
   │
   │  Audits and rewrites underperforming existing content. Updates facts,
   │  improves keyword targeting, strengthens headings, adds internal links,
   │  enhances E-E-A-T signals. Produces before/after comparison.
   │  Saves to output/[client]/[date]/content/optimized/
   │
   ▼
Step 8: Content Performance Analyst
   │
   │  Reviews all content (new and existing) against performance data if
   │  available. Flags what is working, what is not, and recommends next
   │  actions (promote, update, consolidate, or retire).
   │  Saves to vault/04-Content/[client]/performance-analysis.md
```

**Note:** Steps 4a and 4b can run in parallel. The Content Gap Analyst can run at any point after Step 1 — it is often run as part of Step 1 (Content Strategist pulls it in) or independently when investigating content opportunities.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Tavily | `search` | Research topics for content briefs, find current information to include in articles, check what is ranking |
| Tavily | `extract` | Deep-read top-ranking competitor content to understand structure, depth, and angle |
| Firecrawl | `scrape` | Scrape competitor content pages to analyze their structure, word count, headings, and keyword usage |
| Firecrawl | `map` | Map competitor blog/content sections to understand their content architecture |
| Web Fetch | Page validation | Check live pages for existing meta tags, headings, content structure before optimizing |
| Web Search | General research | Find current statistics, quotes, and facts to include in content for E-E-A-T |
| Vault | Read | Pull keyword clusters, competitor analysis, client brand voice, and existing content data |

### Tool Usage Protocol

1. **Always read keyword data from vault first** — never write content without keyword targets
2. **Read client brand voice** from `vault/01-Clients/[client]/brand-voice.md` before any writing
3. **Use Tavily to research every topic** — content must include current, accurate information
4. **Scrape top 3-5 competitor articles** for each brief to understand what Google rewards for that topic
5. **Batch meta tag writing** — write all meta tags in a single pass, not one page at a time

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Keyword clusters | `vault/03-Research/[client]/keyword-clusters.md` | Yes — no content without keyword data |
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Brand voice guide | `vault/01-Clients/[client]/brand-voice.md` | Yes — all writing must match brand voice |
| Client goals | `vault/01-Clients/[client]/goals.md` | Yes — content strategy must align with business goals |
| Competitor content analysis | `vault/06-Competitors/[client]/` | Recommended |
| SERP analysis | `vault/03-Research/[client]/serp-analysis.md` | Recommended — informs content format and angle |
| Technical crawl data | `vault/10-Technical/[client]/crawl-data/` | Recommended — reveals existing pages and content gaps |
| Existing content inventory | `vault/04-Content/[client]/` | Recommended — avoid duplicating existing content |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Content Strategy | `vault/04-Content/[client]/content-strategy.md` | What to create, why, and in what order |
| Content Calendar | `vault/04-Content/[client]/content-calendar.md` | Time-bound publishing schedule |
| Content Briefs | `vault/04-Content/[client]/briefs/[topic-slug].md` | Detailed brief per content piece |
| Blog Posts | `output/[client]/[date]/content/blogs/[topic-slug].md` | Full SEO blog articles |
| Landing Pages | `output/[client]/[date]/content/landing-pages/[page-name].md` | Conversion-optimized landing page copy |
| Meta Tags | `output/[client]/[date]/content/meta-tags.md` | Title tags and meta descriptions for all pages |
| FAQ Content | `output/[client]/[date]/content/faqs/[topic-slug].md` | FAQ sections with JSON-LD schema |
| Content Optimization Report | `output/[client]/[date]/content/optimized/[page-name].md` | Before/after content rewrites with change rationale |
| Performance Analysis | `vault/04-Content/[client]/performance-analysis.md` | Content performance review with recommendations |
| Content Gap Report | `vault/04-Content/[client]/content-gaps.md` | Topics the client should cover but does not |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "content-seo"
date: YYYY-MM-DD
type: content
status: complete
target-keyword: "primary keyword"
intent: informational|commercial|transactional|navigational
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - **Keyword Research Team** (required) — Keyword clusters are the foundation of all content work
  - **Competitor Analysis Team** (recommended) — Competitor content analysis informs strategy and briefs
  - **Technical SEO Team** (recommended) — Crawl data reveals existing pages, thin content, and URL structure
  - **Research Team** (recommended) — Market context and trend data enrich content strategy

- **Feeds into:**
  - **Link Building Team** — New content creates linkable assets for outreach campaigns
  - **AEO Team** — FAQ content and authoritative articles support AI search optimization
  - **Audit & Recommendations Team** — Content findings and strategy feed into the master report
  - **Analytics & Reporting Team** — Content pieces become tracking targets for performance reports

## Quality Checks

### Content SEO-Specific Quality Criteria

1. **Keyword integration** — Every content piece must naturally include the target keyword in the title tag, H1, first 100 words, at least one H2, and meta description. Keyword usage must be natural — no stuffing, no forced repetition. If a keyword reads awkwardly, use a close semantic variant.

2. **Search intent match** — The content type and angle must match the search intent identified in the keyword research. Informational intent gets educational content. Commercial intent gets comparison or review content. Transactional intent gets product or service pages with clear CTAs.

3. **E-E-A-T signals** — Every piece must include: author attribution recommendations, cited sources for claims, first-person experience hooks where appropriate, and clear expertise indicators. No anonymous, unsourced content.

4. **Competitive depth** — Content must be at least as comprehensive as the top 3 ranking competitors for the target keyword. If competitors have 2,000-word guides, a 500-word post will not compete. Depth is measured by topical completeness, not word count alone.

5. **Internal linking** — Every content piece must include at least 3 internal links to relevant existing pages on the client's site. Links must use descriptive anchor text (not "click here").

6. **Meta tag quality** — Title tags must be 50-60 characters, include the target keyword, and have a compelling click hook. Meta descriptions must be 150-160 characters, include the keyword, and have a clear call to action or value proposition.

7. **Brief before writing** — No blog post or landing page is ever written without a content brief. The brief must be saved to vault before writing begins. If a writer agent is invoked without a brief, create the brief first.

8. **Brand voice compliance** — All writing must match the client's brand voice as defined in `vault/01-Clients/[client]/brand-voice.md`. Tone, vocabulary, and style must be consistent.

9. **No placeholder content** — Every deliverable must be complete. No "[insert statistic]", no "TBD", no "coming soon" sections. If data is unavailable, note it explicitly and provide a recommendation for how to obtain it.

10. **Minimum quality score: 3/5. Target: 4/5+.**
