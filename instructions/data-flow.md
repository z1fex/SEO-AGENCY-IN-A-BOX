# Data Flow Map — How Teams Talk to Each Other

> This is the wiring diagram. Every agent must know where to READ input from and where to WRITE output to. Data flows through the vault — teams never communicate directly.

---

## The Golden Rule

**Teams don't talk to each other. They talk to the vault.**

```
Agent A writes to vault/[section]/[client]/[file].md
                         ↓
Agent B reads from vault/[section]/[client]/[file].md
```

Every agent's instructions say:
1. **Pre-Work:** Read these specific files from vault
2. **Post-Work:** Save output to this specific vault path

This document maps every connection.

---

## Master Data Flow Diagram

```
┌─────────────┐
│  ONBOARDING │──writes──→ vault/01-Clients/[client]/ (profile, site-info, competitors, goals, brand-voice)
└──────┬──────┘
       │ triggers
       ▼
┌─────────────────────────────────────────────────────────────┐
│                    INTELLIGENCE LAYER                        │
│                                                             │
│  Research Team ──writes──→ vault/03-Research/[client]/      │
│    - market-research-[date].md                              │
│    - algorithm-updates-[date].md                            │
│    - industry-trends-[date].md                              │
│    - ai-search-landscape-[date].md                          │
│    - serp-features-[date].md                                │
│    - research-briefing-[date].md                            │
│                                                             │
│  Competitor Team ──writes──→ vault/06-Competitors/[client]/ │
│    - [competitor-name]/profile.md                           │
│    - [competitor-name]/keywords.md                          │
│    - [competitor-name]/content.md                           │
│    - [competitor-name]/backlinks.md                         │
│    - [competitor-name]/technical.md                         │
│    - competitor-comparison-[date].md                        │
│    - serp-positions-[date].md                               │
│                                                             │
│  Keywords Team ──writes──→ vault/03-Research/[client]/      │
│    - keyword-discovery-[date].md                            │
│    - serp-analysis-[date].md                                │
│    - intent-mapping-[date].md                               │
│    - competitor-keywords-[date].md                          │
│    - keyword-gaps-[date].md                                 │
│    - keyword-clusters-[date].md                             │
│    - keyword-strategy-[date].md (compiled by lead)          │
└─────────────────────────┬───────────────────────────────────┘
                          │ data flows down
                          ▼
┌─────────────────────────────────────────────────────────────┐
│                     EXECUTION LAYER                         │
│                                                             │
│  Technical Team ──writes──→ vault/10-Technical/[client]/    │
│    - crawl-data/site-crawl-[date].md                       │
│    - core-web-vitals-[date].md                              │
│    - schema-audit-[date].md                                 │
│    - indexation-report-[date].md                            │
│    - internal-links-[date].md                               │
│    - mobile-audit-[date].md                                 │
│    - technical-audit-[date].md (compiled by lead)           │
│                                                             │
│  Content Team ──writes──→ vault/04-Content/[client]/        │
│    - content-strategy-[date].md                             │
│    - content-calendar-[date].md                             │
│    - briefs/[topic]-brief.md                                │
│    - drafts/[topic].md                                      │
│    - published/[topic].md                                   │
│    - meta-tags/meta-tags-[date].md                          │
│    - content-gaps-[date].md                                 │
│    - content-performance-[date].md                          │
│                                                             │
│  Links Team ──writes──→ vault/05-Links/[client]/            │
│    - backlink-audit-[date].md                               │
│    - competitor-backlinks-[date].md                         │
│    - prospects/link-prospects-[date].md                     │
│    - outreach/outreach-emails-[date].md                     │
│    - broken-links-[date].md                                 │
│    - link-building-plan-[date].md (compiled by lead)        │
│                                                             │
│  AEO Team ──writes──→ vault/11-AEO/[client]/               │
│    - conversational-queries-[date].md                       │
│    - ai-overview-optimization-[date].md                     │
│    - perplexity-optimization-[date].md                      │
│    - featured-snippets-[date].md                            │
│    - entity-optimization-[date].md                          │
│    - knowledge-panel-[date].md                              │
│    - citation-optimization-[date].md                        │
│    - aeo-strategy-[date].md (compiled by lead)              │
│                                                             │
│  Local Team ──writes──→ vault/09-Local/[client]/            │
│    - local-competitors-[date].md                            │
│    - gbp-audit-[date].md                                    │
│    - citations-[date].md                                    │
│    - local-content-[date].md                                │
│    - review-strategy-[date].md                              │
│                                                             │
│  E-commerce Team ──writes──→ vault/02-Audits/[client]/      │
│    - faceted-nav-audit-[date].md                            │
│    - category-strategy-[date].md                            │
│    - product-optimization-[date].md                         │
│    - product-schema-[date].md                               │
│    - shopping-feed-[date].md                                │
└─────────────────────────┬───────────────────────────────────┘
                          │ all outputs flow down
                          ▼
┌─────────────────────────────────────────────────────────────┐
│                      OUTPUT LAYER                           │
│                                                             │
│  Audit & Recs Team ──reads ALL above──→                     │
│    writes──→ vault/02-Audits/[client]/                      │
│    - master-audit-[date].md                                 │
│    - recommendations-[date].md                              │
│    - fix-instructions-[date].md                             │
│    - executive-summary-[date].md                            │
│    AND──→ output/[client]/[date]/                           │
│                                                             │
│  Analytics Team ──reads ALL above──→                        │
│    writes──→ vault/07-Reports/[client]/                     │
│    - monthly/[YYYY-MM]-report.md                            │
│    - quarterly/[YYYY-QN]-review.md                          │
│    - dashboards/dashboard-[date].md                         │
│    - roi-[date].md                                          │
│                                                             │
│  Strategy Team ──reads ALL above──→                         │
│    writes──→ vault/08-Strategy/[client]/                    │
│    - seo-strategy-[date].md                                 │
│    - priority-matrix-[date].md                              │
│    - competitive-strategy-[date].md                         │
│    - roadmap-[date].md                                      │
│    - client-summary-[date].md                               │
└─────────────────────────────────────────────────────────────┘
```

---

## Cross-Reference Table — Who Reads What

This table shows exactly which vault files each team READS as input.

### Intelligence Layer (reads client data)

| Team | Reads From | Specific Files |
|------|-----------|----------------|
| **Research** | `vault/01-Clients/[client]/` | profile.md, site-info.md, goals.md |
| **Competitor Analysis** | `vault/01-Clients/[client]/` | profile.md, competitors.md |
| | `vault/03-Research/[client]/` | market-research (if Research team ran first) |
| **Keywords** | `vault/01-Clients/[client]/` | profile.md, goals.md, competitors.md |
| | `vault/03-Research/[client]/` | market-research, industry-trends (if available) |
| | `vault/06-Competitors/[client]/` | competitor keyword data (if Competitor team ran first) |

### Execution Layer (reads intelligence + client data)

| Team | Reads From | Specific Files |
|------|-----------|----------------|
| **Technical** | `vault/01-Clients/[client]/` | profile.md, site-info.md |
| **Content** | `vault/01-Clients/[client]/` | profile.md, brand-voice.md, goals.md |
| | `vault/03-Research/[client]/` | keyword-clusters, keyword-gaps, intent-mapping |
| | `vault/06-Competitors/[client]/` | competitor content analysis |
| | `vault/10-Technical/[client]/` | crawl data (for internal linking, URL inventory) |
| **Links** | `vault/01-Clients/[client]/` | profile.md, competitors.md |
| | `vault/06-Competitors/[client]/` | competitor backlinks |
| | `vault/04-Content/[client]/` | content pieces (for outreach material) |
| **AEO** | `vault/01-Clients/[client]/` | profile.md, site-info.md |
| | `vault/03-Research/[client]/` | keyword-clusters, conversational queries |
| | `vault/10-Technical/[client]/` | schema audit data |
| **Local** | `vault/01-Clients/[client]/` | profile.md, site-info.md |
| | `vault/03-Research/[client]/` | keyword data (local keywords) |
| **E-commerce** | `vault/01-Clients/[client]/` | profile.md, site-info.md |
| | `vault/03-Research/[client]/` | keyword data (product keywords) |
| | `vault/10-Technical/[client]/` | crawl data (URL structure, facets) |

### Output Layer (reads EVERYTHING)

| Team | Reads From | Specific Files |
|------|-----------|----------------|
| **Audit & Recs** | `vault/02-Audits/[client]/` | All audit files |
| | `vault/03-Research/[client]/` | All keyword/research files |
| | `vault/04-Content/[client]/` | Content audit, gaps |
| | `vault/05-Links/[client]/` | Backlink audit |
| | `vault/06-Competitors/[client]/` | Competitor analysis |
| | `vault/09-Local/[client]/` | Local audit (if applicable) |
| | `vault/10-Technical/[client]/` | Technical audit |
| | `vault/11-AEO/[client]/` | AEO assessment |
| **Analytics** | `vault/03-Research/[client]/` | Keyword data for ranking tracking |
| | `vault/07-Reports/[client]/` | Previous reports (for comparison) |
| | `vault/10-Technical/[client]/` | Technical metrics |
| **Strategy** | ALL vault sections for the client | Everything — strategy considers all data |

---

## Dependency Chain — What Must Run Before What

```
REQUIRED DEPENDENCIES (must run first):
═══════════════════════════════════════

Site Crawler ──must run before──→ ALL Technical agents (they need crawl data)
                                  Internal Linking Architect
                                  Content Optimizer (needs URL inventory)
                                  E-commerce agents (need URL structure)

Keyword Discovery ──must run before──→ Intent Classifier
                                       Cluster Builder
                                       Content Strategist
                                       Content Brief Writer
                                       SEO Blog Writer

Competitor Site Crawler ──must run before──→ Competitor Keyword Analyst
                                             Competitor Content Analyzer
                                             Competitor Backlink Profiler
                                             Competitor Technical Benchmarker

RECOMMENDED DEPENDENCIES (better output if run first):
══════════════════════════════════════════════════════

Research Team ──improves──→ Keyword Research (market context helps)
Competitor Analysis ──improves──→ Content Strategy (know what they're doing)
Keywords Team ──improves──→ Content Team (know what to write about)
Keywords Team ──improves──→ AEO Team (know what queries to optimize for)
Technical Audit ──improves──→ Content Team (know site structure)
Links Audit ──improves──→ Strategy (know current authority)
```

---

## Data Freshness Rules

| Data Type | Reuse If Younger Than | Reason |
|-----------|-----------------------|--------|
| Site crawl data | 14 days | Sites change slowly; crawls are expensive |
| Keyword research | 30 days | Search landscape evolves monthly |
| Competitor analysis | 30 days | Competitors update their sites monthly |
| Market research | 60 days | Markets shift slowly |
| Algorithm updates | 7 days | Can change any time |
| Content audit | 30 days | Content doesn't change much |
| Backlink data | 30 days | Link profiles evolve slowly |
| SERP analysis | 14 days | SERPs shift frequently |
| AEO data | 14 days | AI search changes rapidly |

**Rule:** Before running a tool (Firecrawl, Tavily), check vault for existing data. If the data is younger than the freshness threshold above, read from vault instead of running the tool again.

---

## Handling Incomplete Data

When an agent needs input from another team that hasn't run yet:

1. **Check vault** — Maybe the data exists from a previous run
2. **If data exists but is stale** — Proceed with it, but flag it: "Note: using [data type] from [date], which is [X] days old. Consider refreshing."
3. **If no data exists** — Two options:
   - **If the dependency is REQUIRED** — Stop and say: "I need [X] before I can proceed. Please run [team/agent] first."
   - **If the dependency is RECOMMENDED** — Proceed without it, but note: "Output would be stronger with [X] data. Consider running [team] and re-running me."
4. **Never hallucinate missing data** — If you don't have keyword volumes, don't make them up. If you don't have competitor data, don't invent competitors.

---

## Wikilink Conventions

When saving to vault, link to related documents:

```markdown
## Related
- Client: [[Acme Corp]]
- Keywords: [[keyword-clusters-2026-04-15]]
- Competitor: [[competitor-comparison-2026-04-15]]
- Technical: [[site-crawl-2026-04-15]]
- Previous: [[keyword-strategy-2026-03-15]]
```

**Naming convention for wikilinks:**
- Client names: `[[Company Name]]` (title case)
- Deliverables: `[[type-date]]` (lowercase-hyphenated)
- Competitors: `[[Competitor Name]]` (title case)

This creates a navigable knowledge graph in Obsidian.
