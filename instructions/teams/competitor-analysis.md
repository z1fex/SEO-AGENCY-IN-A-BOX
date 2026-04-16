# Competitor Analysis Team

> Crawl, dissect, and benchmark competitor websites to extract their keyword strategies, content depth, backlink sources, technical health, and SERP positioning — feeding actionable competitive intelligence to every other team.

## Team Overview

The Competitor Analysis Team is the intelligence-gathering unit that every other team depends on. No SEO strategy should be built in a vacuum. Before the agency writes a single blog post, builds a single link, or optimizes a single page, it must know exactly what the competition is doing, where they are strong, where they are weak, and where the gaps are. This team provides that intelligence by crawling competitor sites with Firecrawl, extracting their keyword targets, analyzing their content depth and quality, profiling their backlink strategies, benchmarking their technical SEO health, and tracking head-to-head SERP positions.

This team sits in the **Intelligence Layer** of the agency hierarchy. It runs during Phase 2 (Research), typically after the Research team has provided market context and before or alongside the Keyword Research team. Competitor Analysis output feeds into EVERY execution team: Technical SEO uses it for benchmarking, Content SEO uses it for content gap analysis, Link Building uses it for backlink opportunity identification, AEO uses it for understanding who AI search engines cite, and Strategy uses it for competitive positioning. Running execution teams without competitor data is running blind.

The team follows a crawl-first approach. The Competitor Site Crawler must run first because it produces the raw data that every other agent on the team consumes. Once the crawl is complete, four specialist agents work in parallel to extract keyword intelligence, content analysis, backlink profiles, and technical benchmarks from the crawl data. The Competitor SERP Tracker then runs last to map head-to-head ranking positions across the client's target keywords, synthesizing the full competitive picture.

## Agents

| Agent | File | Role |
|-------|------|------|
| Competitor Site Crawler | `agents/competitor/site-crawler.md` | Crawls each competitor's website using Firecrawl to extract URL structures, page content, meta data, internal linking patterns, site architecture, and technical implementation details |
| Competitor Keyword Analyst | `agents/competitor/keyword-analyst.md` | Extracts keyword targets from competitor crawl data — analyzes title tags, H1s, URL structures, content themes, and meta descriptions to map the keywords each competitor is actively targeting |
| Competitor Content Analyzer | `agents/competitor/content-analyzer.md` | Evaluates competitor content depth, quality, format, freshness, topical coverage, and content strategy — identifies what content types they invest in and where their content is strong or weak |
| Competitor Backlink Profiler | `agents/competitor/backlink-profiler.md` | Profiles competitor backlink strategies — identifies their top referring domains, link building patterns (guest posts, PR, directories, resource pages), anchor text distribution, and replicable link sources |
| Competitor Technical Benchmarker | `agents/competitor/technical-benchmarker.md` | Benchmarks competitor technical SEO implementation — Core Web Vitals, schema markup, mobile optimization, site speed, indexation strategy, and crawl efficiency compared to the client |
| Competitor SERP Tracker | `agents/competitor/serp-tracker.md` | Tracks head-to-head SERP positions for the client's target keywords — maps who ranks where, identifies keyword overlaps and gaps, and tracks competitive movement over time |

## When to Run This Team

- **New client onboarding** — Always run during the initial intelligence phase to establish the competitive baseline
- **Full SEO audit** — Required as part of any comprehensive audit; competitor data contextualizes every finding
- **Content planning** — Before any content sprint, know what competitors have published and how deep their coverage is
- **Link building campaign** — Before prospecting, understand where competitors get their links
- **Ranking changes** — When the client gains or loses rankings, check what competitors changed
- **New competitor enters market** — When a new competitor appears in the client's SERP landscape
- **Competitor site redesign** — When a competitor launches a new site or major redesign, crawl immediately to understand changes
- **Quarterly refresh** — Competitors evolve; re-crawl quarterly to catch strategy shifts, new content, and link acquisitions
- **Strategy review** — Before updating the SEO roadmap, refresh competitive intelligence
- **AEO optimization** — Before AEO work, understand which competitors are being cited by AI search engines

## Execution Order

```
Step 1: Competitor Site Crawler (MANDATORY FIRST)
   │
   │  Crawls each competitor site using Firecrawl. Always runs firecrawl_map
   │  first to assess site size, then sets appropriate crawl limits. Extracts
   │  all URLs, page content, meta data, internal links, and site structure.
   │  Caches all raw crawl data for the parallel agents to consume.
   │  Saves to vault/06-Competitors/[client]/[competitor-slug]/crawl-data/
   │
   ├──→ Step 2a: Competitor Keyword Analyst (parallel)
   │    │
   │    │  Reads competitor crawl data and extracts keyword targets from
   │    │  title tags, H1s, URL slugs, meta descriptions, and content
   │    │  themes. Maps each competitor's keyword universe and identifies
   │    │  the topics they prioritize. Cross-references with the client's
   │    │  keyword data to find overlaps and exclusive competitor keywords.
   │    │  Saves to vault/06-Competitors/[client]/competitor-keywords.md
   │    │
   ├──→ Step 2b: Competitor Content Analyzer (parallel)
   │    │
   │    │  Reads competitor crawl data and evaluates content strategy:
   │    │  content types (blogs, guides, tools, videos), publishing
   │    │  frequency, average content depth, topical coverage breadth,
   │    │  content freshness, and quality assessment. Identifies content
   │    │  gaps where the client can outperform.
   │    │  Saves to vault/06-Competitors/[client]/competitor-content.md
   │    │
   ├──→ Step 2c: Competitor Backlink Profiler (parallel)
   │    │
   │    │  Uses Tavily and Firecrawl to research competitor backlink
   │    │  patterns. Identifies top referring domains, link building
   │    │  tactics (guest posts, PR mentions, resource pages, directories),
   │    │  anchor text patterns, and replicable link opportunities.
   │    │  Saves to vault/06-Competitors/[client]/competitor-backlinks.md
   │    │
   ├──→ Step 2d: Competitor Technical Benchmarker (parallel)
   │    │
   │    │  Uses crawl data plus Web Fetch spot checks to benchmark
   │    │  competitor technical SEO: page speed, Core Web Vitals,
   │    │  schema implementation, mobile optimization, HTTPS, site
   │    │  architecture depth, and indexation strategy. Compares
   │    │  against the client's technical baseline.
   │    │  Saves to vault/06-Competitors/[client]/competitor-technical.md
   │
   ▼
Step 3: Competitor SERP Tracker
   │
   │  Uses Tavily search to check actual SERP positions for the client's
   │  priority keywords. Maps which competitor ranks where for each keyword.
   │  Identifies: keywords where the client leads, keywords where competitors
   │  lead, keywords where neither ranks (opportunity gaps), and keyword
   │  clusters dominated by specific competitors. Produces the head-to-head
   │  competitive ranking matrix.
   │  Saves to vault/06-Competitors/[client]/serp-positions.md
```

**Data flow:** The Competitor Site Crawler provides the raw data foundation. Four specialist agents work in parallel to extract keyword, content, backlink, and technical intelligence from that data. The SERP Tracker runs last because it synthesizes the full competitive picture — knowing who ranks where is most valuable when you already understand why they rank there (content depth, link profile, technical health).

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Firecrawl | `map` | Quick URL inventory of competitor sites — always run before crawl to assess site size and plan crawl scope |
| Firecrawl | `crawl` | Full competitor site crawl — extracts all URLs, content, metadata, internal links, and site architecture |
| Firecrawl | `scrape` | Deep analysis of specific competitor pages — product pages, top blog posts, landing pages |
| Firecrawl | `extract` | Extract structured data from competitor pages — pricing, features, product details |
| Tavily | `search` | Research competitor backlinks, discover competitor mentions, check SERP positions, find competitor PR coverage |
| Tavily | `search` (advanced depth) | Deep SERP analysis — check actual ranking positions for target keywords across competitors |
| Tavily | `extract` | Deep-read competitor content pages to analyze structure, depth, and quality |
| Web Fetch | Page validation | Spot-check competitor pages for schema markup, redirect behavior, mobile rendering, page speed indicators |
| Web Search | General research | Find competitor news, press releases, recent launches, strategy changes |

### Tool Usage Protocol

1. **Always run `firecrawl_map` before `firecrawl_crawl`** — map the competitor site first to assess size, then set appropriate `maxPages` and `maxDepth` limits to control cost
2. **Set crawl limits per competitor** — use `maxPages: 500` as a default ceiling for most competitor sites; adjust up or down based on site size from the map
3. **Cache ALL competitor crawl data** in `vault/06-Competitors/[client]/[competitor-slug]/crawl-data/` — never re-crawl a competitor site if data is less than 30 days old
4. **Use `includePaths` filters** — if you only need competitor blog content, filter to `/blog/*` rather than crawling the entire site
5. **Scrape selectively** — for content depth analysis, scrape the top 10-20 pages per competitor rather than analyzing every page
6. **Batch SERP checks** — when checking ranking positions, research multiple related keywords in contextual Tavily queries rather than one keyword per query

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Client site URL | `vault/01-Clients/[client]/site-info.md` | Yes |
| Competitor list | `vault/01-Clients/[client]/competitors.md` | Yes — must have at least 3 competitors identified |
| Client goals | `vault/01-Clients/[client]/goals.md` | Yes — determines what competitive dimensions matter most |
| Research team output | `vault/03-Research/[client]/` | Recommended — market context helps interpret competitive data |
| Client keyword data | `vault/03-Research/[client]/` | Recommended — enables keyword overlap and gap analysis |
| Client technical crawl data | `vault/10-Technical/[client]/crawl-data/` | Recommended — enables direct technical benchmarking |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Competitor Crawl Data (raw) | `vault/06-Competitors/[client]/[competitor-slug]/crawl-data/` | Raw Firecrawl output cached for reuse by all agents and other teams |
| Competitor Site Structure | `vault/06-Competitors/[client]/site-structures.md` | URL architecture, navigation patterns, and content organization for each competitor |
| Competitor Keyword Analysis | `vault/06-Competitors/[client]/competitor-keywords.md` | Keywords each competitor targets, overlaps with client, and exclusive competitor keywords |
| Competitor Content Analysis | `vault/06-Competitors/[client]/competitor-content.md` | Content strategy, depth, format, freshness, and quality assessment per competitor |
| Competitor Backlink Profile | `vault/06-Competitors/[client]/competitor-backlinks.md` | Link building patterns, top referring domains, replicable link opportunities |
| Competitor Technical Benchmark | `vault/06-Competitors/[client]/competitor-technical.md` | Technical SEO comparison — page speed, schema, mobile, indexation, CWV benchmarks |
| SERP Position Matrix | `vault/06-Competitors/[client]/serp-positions.md` | Head-to-head ranking positions for all target keywords with competitive gap analysis |
| Competitive Intelligence Summary | `vault/06-Competitors/[client]/competitive-summary.md` | Executive summary of all competitive findings with strengths, weaknesses, and opportunities |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "competitor-analysis"
date: YYYY-MM-DD
type: competitor
status: complete
competitors-analyzed: ["competitor-1", "competitor-2", "competitor-3"]
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile with competitor list of at least 3 competitors (must exist in vault)
  - **Research Team** (recommended) — market context helps interpret competitive data and identify which competitive dimensions matter
  - Client site crawl data from Technical SEO (optional but helpful — enables direct client-vs-competitor benchmarking)

- **Feeds into:**
  - **Keyword Research Team** — competitor keyword data feeds directly into keyword gap analysis and discovery
  - **Content SEO Team** — competitor content analysis reveals content gaps and benchmarks for content depth
  - **Link Building Team** — competitor backlink profiles reveal replicable link opportunities and authority gaps
  - **AEO Team** — competitor analysis reveals which competitors get cited in AI search results
  - **Technical SEO Team** — technical benchmarks reveal where the client lags behind competitors technically
  - **E-commerce SEO Team** — competitor product and category structures inform e-commerce optimization
  - **Strategy & Direction Team** — competitive intelligence is the foundation of strategic positioning
  - **Audit & Recommendations Team** — all competitive findings feed into the master report for competitive context

## Quality Checks

### Competitor Analysis-Specific Quality Criteria

1. **Real crawl data** — Every competitor finding must come from actual Firecrawl crawl/scrape data, Tavily search results, or Web Fetch validation. Never describe a competitor's strategy based on assumptions or general industry knowledge. If you cannot crawl a competitor (robots.txt blocks, dynamic rendering issues), document the limitation and use alternative methods (Tavily search, Web Fetch spot checks).

2. **Minimum three competitors** — Every competitive analysis must cover at least three competitors. Two is too few for meaningful patterns; one is useless. If the client identified fewer than three, use Tavily to discover additional competitors ranking for the same keywords.

3. **Apples-to-apples benchmarking** — Technical benchmarks must compare equivalent page types. Compare the client's homepage to competitor homepages, the client's product pages to competitor product pages. Comparing a lightweight landing page to a heavy e-commerce category page is misleading.

4. **Replicable opportunities** — Backlink analysis must distinguish between replicable and non-replicable link sources. A competitor getting press coverage in the New York Times is informational. A competitor getting links from an industry resource page that accepts submissions is actionable. Prioritize actionable opportunities.

5. **Content depth measurements** — Content analysis must include specific depth metrics, not just qualitative assessments. Word counts, topic coverage breadth (number of subtopics), content freshness (publication/update dates), and content format mix (text, video, tools, interactive) must all be quantified where possible.

6. **Keyword overlap precision** — Competitor keyword analysis must distinguish between: keywords both the client and competitor target (direct competition), keywords only the competitor targets (gaps), and keywords only the client targets (advantages). Each category must be quantified.

7. **SERP verification** — SERP positions must come from actual Tavily search results, not from assumptions based on content quality or domain authority. Rankings must be checked, not estimated.

8. **Timestamped data** — All competitive data must be timestamped in the frontmatter. Competitor strategies change; data older than 30 days should be flagged for refresh on re-audit.

9. **Minimum quality score: 3/5. Target: 4/5+.**
