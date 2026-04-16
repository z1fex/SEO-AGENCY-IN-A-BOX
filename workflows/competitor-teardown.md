# Competitor Teardown
> **Teams involved:** Competitor, Keywords, Links, Strategy | **Steps:** 6 | **Estimated time:** 25–45 minutes

Deep-dive analysis of a specific competitor's entire SEO strategy. Reverse-engineers their technical setup, keyword strategy, content approach, and link profile to uncover exactly how they rank and where they're vulnerable.

## What You'll Get
- Complete competitor site architecture and technical SEO analysis
- Full keyword portfolio with ranking positions and traffic estimates
- Content strategy breakdown (topics, formats, frequency, top performers)
- Backlink profile analysis with link acquisition patterns
- SERP presence tracking across target keywords
- Competitive strategy report with exploitable weaknesses and actionable counter-tactics

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- Target competitor URL provided
- Client's own keyword data exists in vault (run `keyword-strategy` first if missing)

## Steps

### Step 1: Competitor Site Crawl
**Agent:** `agents/competitor/competitor-site-crawler.md`
**Action:** Crawl the target competitor's site using Firecrawl. Map their complete site architecture: total page count, URL structure and hierarchy, site depth and navigation patterns, content categories and subcategories, key landing pages, and technical infrastructure (CMS, CDN, page speed indicators). Identify their SEO-critical pages (those targeting high-value keywords) and content hubs. Document their internal linking strategy by analyzing link distribution across sections.
**Save to:** `vault/06-Competitors/[competitor-name]-crawl.md`

### Step 2a: Competitor Keyword Analysis (parallel track A)
**Agent:** `agents/competitor/competitor-keyword-analyst.md`
**Action:** Identify the competitor's keyword footprint using Tavily research and content analysis from the crawl data. Document: estimated number of ranking keywords, their top 50 keywords by traffic value, keyword distribution by intent type (informational vs. transactional), topic areas they dominate, emerging keywords they're targeting (recently published content), and keywords where they rank #1–3 that overlap with the client's targets. Calculate their estimated organic traffic value.
**Save to:** `vault/06-Competitors/[competitor-name]-keywords.md`

### Step 2b: Competitor Content Analysis (parallel track B)
**Agent:** `agents/competitor/competitor-content-analyzer.md`
**Action:** Analyze the competitor's content strategy using Firecrawl scraping and Tavily. Document: content publishing frequency and consistency, content types and formats used (blogs, guides, tools, videos, case studies), average content length and depth, content freshness (how often they update), their top 10 performing content pieces (by estimated traffic/links), content gaps in their strategy, use of multimedia and interactive elements, E-E-A-T signals (author bios, credentials, citations). Assess their content quality compared to the client.
**Save to:** `vault/06-Competitors/[competitor-name]-content.md`

### Step 2c: Competitor Backlink Profile (parallel track C)
**Agent:** `agents/competitor/competitor-backlink-profiler.md`
**Action:** Analyze the competitor's backlink profile using Tavily and Web Search. Document: estimated domain authority/rating, total referring domains, link acquisition velocity (links gained per month), top linking domains by authority, most-linked-to pages (link magnets), anchor text distribution, link types (editorial, guest posts, directories, resource pages, digital PR), and their link building tactics. Identify their most replicable link sources for the client.
**Save to:** `vault/06-Competitors/[competitor-name]-backlinks.md`

### Step 3: SERP Presence Tracking
**Agent:** `agents/competitor/competitor-serp-tracker.md`
**Action:** Track the competitor's SERP presence across the client's target keyword set. For each overlapping keyword, document: the competitor's current position, the SERP feature they occupy (if any — featured snippet, PAA, AI Overview, local pack, image pack), the page that ranks, and the content format. Identify keywords where the competitor holds SERP features the client could challenge. Map head-to-head rankings for all shared keywords.
**Save to:** `vault/06-Competitors/[competitor-name]-serp-presence.md`

### Step 4: Competitive Strategy Analysis
**Agent:** `agents/strategy/competitive-strategy-analyst.md`
**Action:** Synthesize all competitor data from Steps 1–3 into a strategic analysis. Deliver: **Competitor Strengths** (what they do well that drives their rankings), **Competitor Weaknesses** (technical issues, content gaps, link profile vulnerabilities, ignored keywords), **Threat Assessment** (where they're actively improving and could overtake the client), **Opportunity Map** (specific actions the client can take to outrank this competitor), and a **Priority Action List** with 10 ranked tactical moves the client should execute. Each recommendation must reference specific data from the analysis.
**Save to:** `vault/06-Competitors/[competitor-name]-strategy.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on all deliverables
2. Verify all competitor data comes from Firecrawl, Tavily, or Web Fetch (no hallucinated metrics)
3. Save complete teardown to `output/[client]/[date]/competitor/[competitor-name]-teardown.md`
4. Update vault competitor records in `vault/06-Competitors/`
5. Update vault dashboard (`vault/00-Dashboard/`)
6. Update ROI tracker — log competitor teardown with estimated agency value ($1,500–$2,500)
