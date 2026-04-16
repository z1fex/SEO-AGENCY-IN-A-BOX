# Keyword Research Team

> Discover, classify, cluster, and prioritize the keywords that drive every content, optimization, and strategy decision across the agency.

## Team Overview

The Keyword Research Team is the foundation of the entire agency's execution work. No content should be written, no page should be optimized, and no strategy should be set without keyword research backing it. This team transforms raw search data into structured, prioritized keyword intelligence that every other team consumes.

This team sits in the **Intelligence Layer** of the agency hierarchy. It runs during Phase 2 (Research) and provides the keyword data that the Execution Layer teams (Content SEO, AEO, Local SEO, E-commerce SEO) depend on. Keyword Research typically runs after the Research team (for market context) and after or alongside Competitor Analysis (for competitive keyword intelligence), but it can run independently if time is constrained.

The team follows a strict sequential pipeline. Keyword Discovery casts a wide net, then each subsequent agent refines, classifies, and organizes the data until the Cluster Builder delivers ready-to-use keyword clusters mapped to content types and priority scores. The output is not a list of keywords — it is an actionable keyword strategy.

## Agents

| Agent | File | Role |
|-------|------|------|
| Keyword Discovery Agent | `agents/keywords/keyword-discovery.md` | Casts a wide net using Tavily to discover seed keywords, long-tail variations, question queries, and related terms for the client's industry |
| SERP Analyzer | `agents/keywords/serp-analyzer.md` | Analyzes actual search results for priority keywords to understand what Google rewards — content types, SERP features, AI Overviews, and ranking patterns |
| Search Intent Classifier | `agents/keywords/intent-classifier.md` | Classifies every keyword by search intent (informational, navigational, commercial, transactional) and maps each to the appropriate content type |
| Competitor Keyword Spy | `agents/keywords/competitor-spy.md` | Uses Firecrawl to scrape competitor sites and extract the keywords they target through title tags, H1s, URLs, content themes, and meta descriptions |
| Keyword Gap Analyst | `agents/keywords/gap-analyst.md` | Compares the client's keyword coverage against competitors to find keywords competitors rank for that the client does not |
| Keyword Cluster Builder | `agents/keywords/cluster-builder.md` | Groups keywords into topical clusters, assigns a pillar page and supporting content structure, and prioritizes clusters by opportunity size |

## When to Run This Team

- **New client onboarding** — Always run after initial research to establish the keyword baseline
- **Content planning** — Before any content sprint, brief creation, or content calendar build
- **Content gap analysis** — When looking for new content opportunities
- **Competitor monitoring** — When a competitor launches new content or enters a new topic area
- **Quarterly refresh** — Keywords shift over time; re-run quarterly to catch new opportunities and intent changes
- **New product or service launch** — When the client adds offerings that need new keyword targets
- **Market expansion** — When the client enters a new geographic market or industry vertical
- **Ranking stagnation** — When existing keyword targets stop improving, look for better opportunities
- **AEO optimization** — Keyword data informs which queries trigger AI Overviews and need AEO treatment

## Execution Order

```
Step 1: Keyword Discovery Agent
   │
   │  Uses Tavily search to discover seed keywords, long-tail variations,
   │  question queries, and related terms. Produces the raw keyword universe.
   │  Saves to vault/03-Research/[client]/raw-discovery.md
   │
   ▼
Step 2: SERP Analyzer
   │
   │  Takes the top priority keywords from Discovery and analyzes actual
   │  SERPs. Records content types ranking, SERP features present,
   │  AI Overview triggers, and ranking difficulty signals.
   │  Saves to vault/03-Research/[client]/serp-analysis.md
   │
   ▼
Step 3: Search Intent Classifier
   │
   │  Takes all discovered keywords and classifies each by search intent.
   │  Maps each intent type to a content format (blog post, product page,
   │  comparison page, guide, etc.). Flags ambiguous intent keywords.
   │  Saves to vault/03-Research/[client]/intent-map.md
   │
   ▼
Step 4: Competitor Keyword Spy
   │
   │  Uses Firecrawl to scrape competitor pages and extract keyword targets
   │  from their title tags, H1s, URL structures, and content themes.
   │  Cross-references with the client's keyword universe.
   │  Saves to vault/03-Research/[client]/competitor-keywords.md
   │
   ▼
Step 5: Keyword Gap Analyst
   │
   │  Compares the client's current keyword coverage (from site crawl
   │  or provided data) against competitor keyword targets. Identifies
   │  keywords that competitors rank for but the client does not.
   │  Saves to vault/03-Research/[client]/keyword-gaps.md
   │
   ▼
Step 6: Keyword Cluster Builder
   │
   │  Takes ALL prior agent outputs and organizes keywords into topical
   │  clusters. Each cluster has: a pillar keyword, supporting keywords,
   │  recommended content type per keyword, intent classification,
   │  priority score, and competitive difficulty assessment.
   │  Saves to vault/03-Research/[client]/keyword-clusters.md
```

**Data flow:** Each agent builds on the previous agent's output. The Cluster Builder is the culmination — it produces the final, actionable keyword strategy that all execution teams consume.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Tavily | `search` | Primary keyword discovery — finds related terms, question queries, long-tail variations, and SERP data |
| Tavily | `search` (advanced depth) | Deep SERP analysis — examines what content ranks, SERP features, AI Overview presence |
| Tavily | `extract` | Deep-reads top-ranking pages to understand content patterns that win for specific keywords |
| Firecrawl | `scrape` | Scrapes competitor pages to extract title tags, H1s, meta descriptions, and content structure for keyword extraction |
| Firecrawl | `map` | Maps competitor site structure to understand their content architecture and topic coverage |
| Web Search | General research | Checks current search trends, verifies keyword context, finds industry terminology |

### Tool Usage Protocol

1. **Use Tavily for all keyword research** — it returns cleaner, more research-oriented results than general web search
2. **Use `search_depth: "advanced"`** for SERP analysis to get thorough results
3. **Batch related queries** — research 3-5 related keywords in a single Tavily search where possible
4. **Scrape competitors selectively** — only scrape the most relevant pages, not entire sites (use `map` first to identify target pages)
5. **Save all raw search results** to vault for reuse by other teams

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Client site URL | `vault/01-Clients/[client]/site-info.md` | Yes |
| Client goals | `vault/01-Clients/[client]/goals.md` | Yes (determines keyword focus areas) |
| Competitor list | `vault/01-Clients/[client]/competitors.md` | Yes (for Competitor Spy and Gap Analyst) |
| Market research data | `vault/03-Research/[client]/` | Recommended (provides industry context) |
| Existing site crawl data | `vault/10-Technical/[client]/crawl-data/` | Recommended (reveals current keyword targets) |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Raw Keyword Discovery | `vault/03-Research/[client]/raw-discovery.md` | Full list of discovered keywords with search context |
| SERP Analysis | `vault/03-Research/[client]/serp-analysis.md` | SERP feature mapping, content type analysis, AI Overview triggers, ranking patterns |
| Intent Map | `vault/03-Research/[client]/intent-map.md` | Every keyword classified by intent with mapped content type |
| Competitor Keywords | `vault/03-Research/[client]/competitor-keywords.md` | Keywords extracted from competitor sites with source URLs |
| Keyword Gaps | `vault/03-Research/[client]/keyword-gaps.md` | Keywords competitors target that the client does not, sorted by opportunity |
| Keyword Clusters | `vault/03-Research/[client]/keyword-clusters.md` | Organized topical clusters with pillar/supporting structure, priorities, and content type mapping |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "keyword-research"
date: YYYY-MM-DD
type: keywords
status: complete
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile with goals and competitor list (must exist in vault)
  - Research Team output (recommended — provides market context and trend awareness)
  - Competitor Analysis Team output (recommended — provides detailed competitor intelligence)
  - Technical SEO crawl data (optional — useful for understanding current keyword targets on the client's site)

- **Feeds into:**
  - **Content SEO Team** — Keyword clusters drive content strategy, briefs, and writing targets
  - **AEO Team** — SERP analysis reveals which keywords trigger AI Overviews, informing AEO optimization
  - **Local SEO Team** — Local keyword variations feed into local content and GBP optimization
  - **E-commerce SEO Team** — Product and category keywords drive product page and taxonomy optimization
  - **Link Building Team** — High-priority keywords inform which pages need backlink support
  - **Strategy & Direction Team** — Keyword opportunity data informs the SEO roadmap and priority matrix
  - **Audit & Recommendations Team** — Keyword gaps and opportunities are included in the master report

## Quality Checks

### Keyword Research-Specific Quality Criteria

1. **Real data, not guesses** — Every keyword must come from a Tavily search, Firecrawl scrape, or verifiable source. Never invent keywords or search volumes. If volume data is unavailable, state "volume data not available" rather than estimating.

2. **Intent accuracy** — Every intent classification must be verified by checking actual SERP results for that keyword. If the SERP shows a mix of content types, flag the keyword as "mixed intent" rather than forcing a single classification.

3. **Cluster coherence** — Each keyword cluster must represent a genuine topical group. Keywords in the same cluster should share semantic relevance and could logically be covered by a pillar page and supporting content. Random groupings by surface-level word overlap are not acceptable.

4. **Competitor verification** — Competitor keywords must be extracted from actual competitor pages via Firecrawl, not assumed based on industry knowledge. Include the source URL for every competitor keyword.

5. **Gap analysis accuracy** — Keyword gaps must be confirmed by checking both the competitor's coverage (via scrape data) and the client's lack of coverage (via site crawl or manual check). A gap is only valid if the competitor demonstrably targets the keyword and the client demonstrably does not.

6. **Actionable prioritization** — Every keyword cluster must have a priority score based on: estimated opportunity (search relevance and competitive landscape), business alignment (does it match client goals?), and competitive difficulty (what is currently ranking?). Do not present a flat list with no prioritization.

7. **Content type mapping** — Every keyword must be mapped to a specific content type (blog post, product page, category page, landing page, FAQ, guide, comparison, etc.). The content type must match the search intent and SERP analysis findings.

8. **Minimum quality score: 3/5. Target: 4/5+.**
