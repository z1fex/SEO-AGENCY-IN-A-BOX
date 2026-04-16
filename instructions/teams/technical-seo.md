# Technical SEO Team

> Crawl, audit, and fix the technical foundation so search engines can efficiently discover, crawl, index, and render every page on the client's site.

## Team Overview

The Technical SEO Team is the structural engineering department of the agency. Before any content can rank or any link can pass value, the site itself must work flawlessly for search engines. This team finds and fixes the invisible problems that silently kill organic performance: broken pages, redirect chains, crawl budget waste, missing schema, orphan pages, slow Core Web Vitals, mobile rendering failures, and indexation gaps.

This team sits in the **Execution Layer** of the agency hierarchy. It runs after the Intelligence Layer (Research, Competitor Analysis, Keyword Research) has provided data, and its findings feed into the Audit & Recommendations team for compilation into the master report. Technical SEO is almost always the first execution team to run because its crawl data serves as the foundation for Content SEO, Link Building, and E-commerce SEO teams.

In the agency pipeline, Technical SEO owns Phase 3 (Audit) for all site infrastructure concerns and Phase 5 (Execute) for implementing technical fixes. The Site Crawler agent always runs first because every other agent on this team depends on crawl data to do its work.

## Agents

| Agent | File | Role |
|-------|------|------|
| Site Crawler | `agents/technical/site-crawler.md` | Crawls the entire site using Firecrawl, builds the URL inventory, discovers broken pages, redirect chains, status codes, and orphan pages |
| Core Web Vitals Analyst | `agents/technical/core-web-vitals.md` | Analyzes LCP, INP, and CLS for key pages, identifies performance bottlenecks, recommends specific fixes |
| Schema Specialist | `agents/technical/schema-specialist.md` | Audits existing structured data, identifies missing schema opportunities, generates JSON-LD markup for all applicable page types |
| Indexation Manager | `agents/technical/indexation-manager.md` | Checks robots.txt, XML sitemaps, meta robots tags, canonical tags, and Search Console indexation status to ensure the right pages are indexed |
| Internal Linking Architect | `agents/technical/internal-linking.md` | Maps the internal link graph, finds orphan pages, identifies link equity distribution issues, recommends internal linking improvements |
| Mobile SEO Auditor | `agents/technical/mobile-seo.md` | Tests mobile rendering, checks mobile-first indexing readiness, audits tap targets, viewport settings, and mobile UX signals |
| Site Migration Specialist | `agents/technical/site-migration.md` | Plans and audits site migrations (domain changes, CMS switches, URL restructures), builds redirect maps, monitors post-migration health |
| Log Analyzer | `agents/technical/log-analyzer.md` | Analyzes server log data (when provided) to understand Googlebot crawl patterns, crawl budget allocation, and crawl anomalies |

## When to Run This Team

- **Full site audit** — Always runs as the first execution team in any comprehensive audit
- **New client onboarding** — Run immediately after intelligence phase to establish a technical baseline
- **Site speed complaints** — Client reports slow pages or poor Core Web Vitals scores
- **Indexation problems** — Pages not appearing in Google, unexpected drops in indexed page count
- **Site migration** — Before, during, and after any domain change, CMS switch, or URL restructure
- **Ranking drops** — Sudden ranking declines often have technical root causes (crawl errors, accidental noindex, canonical issues)
- **New site sections** — When the client launches a new section, subdomain, or subfolder
- **Post-redesign** — After any significant design or template change
- **Quarterly re-audit** — Technical health degrades over time; re-crawl quarterly

## Execution Order

```
Step 1: Site Crawler (MANDATORY FIRST)
   │
   │  Crawls the full site via Firecrawl. Produces the URL inventory,
   │  status code report, redirect map, and raw crawl data.
   │  Saves to vault/10-Technical/[client]/crawl-data/
   │
   ├──→ Step 2a: Core Web Vitals Analyst (parallel)
   │    Uses crawl data to identify key pages, then checks performance
   │    metrics. Produces page-speed report with specific fix instructions.
   │
   ├──→ Step 2b: Schema Specialist (parallel)
   │    Uses crawl data to audit structured data on every page type.
   │    Identifies missing schema, generates JSON-LD templates.
   │
   ├──→ Step 2c: Indexation Manager (parallel)
   │    Uses crawl data + Web Fetch (robots.txt, sitemaps) to audit
   │    indexation. Cross-references crawled URLs against sitemap URLs.
   │
   ├──→ Step 2d: Internal Linking Architect (parallel)
   │    Uses crawl data to build the internal link graph. Finds orphan
   │    pages, thin link equity nodes, and hub page opportunities.
   │
   ├──→ Step 2e: Mobile SEO Auditor (parallel)
   │    Uses crawl data to identify template types, then spot-checks
   │    mobile rendering via Web Fetch on representative pages.
   │
   ├──→ Step 2f: Log Analyzer (parallel, if log data available)
   │    Analyzes server logs to map Googlebot crawl behavior.
   │    Only runs if the client provides log files.
   │
   └──→ Step 2g: Site Migration Specialist (conditional)
        Only runs if a migration is planned or recently completed.
        Uses crawl data to build redirect maps and verify migration health.
```

**Data flow:** Site Crawler output is the single source of truth for all subsequent agents. Every agent reads from `vault/10-Technical/[client]/crawl-data/` rather than re-crawling.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Firecrawl | `crawl` | Full site crawl — URL discovery, status codes, content extraction, link mapping |
| Firecrawl | `map` | Quick URL inventory before committing to a full crawl (assess site size first) |
| Firecrawl | `scrape` | Deep analysis of individual pages (schema inspection, content structure) |
| Web Fetch | Page validation | Check robots.txt, XML sitemaps, individual page rendering, redirect behavior |
| Web Search | Research | Look up current Core Web Vitals thresholds, schema documentation, algorithm updates |

### Tool Usage Protocol

1. **Always run `firecrawl_map` first** to assess site size before committing to a full crawl
2. **Set `maxDepth` and `maxPages`** on crawls to control scope and credit usage
3. **Cache all crawl data** in `vault/10-Technical/[client]/crawl-data/` — never re-crawl if data is less than 14 days old
4. **Use Web Fetch for spot checks** — do not re-crawl just to check one page
5. **Use `includePaths` filters** on Firecrawl when you only need specific site sections

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Client site URL | `vault/01-Clients/[client]/site-info.md` | Yes |
| Keyword research data | `vault/03-Research/[client]/` | Recommended (helps prioritize pages) |
| Competitor crawl data | `vault/06-Competitors/[client]/` | Recommended (for benchmarking) |
| Server log files | Client-provided | Optional (enables Log Analyzer) |
| Search Console access/data | Client-provided | Optional (enhances Indexation Manager) |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| URL Inventory | `vault/10-Technical/[client]/url-inventory.md` | Complete list of all discovered URLs with status codes, titles, word counts |
| Crawl Data (raw) | `vault/10-Technical/[client]/crawl-data/` | Raw Firecrawl output, cached for reuse by other teams |
| Technical Audit Findings | `vault/02-Audits/[client]/technical-findings.md` | All issues found, categorized and prioritized |
| Core Web Vitals Report | `vault/10-Technical/[client]/cwv-report.md` | Page-by-page performance analysis with specific fixes |
| Schema Audit | `vault/10-Technical/[client]/schema-audit.md` | Current schema status + generated JSON-LD for missing types |
| Indexation Report | `vault/10-Technical/[client]/indexation-report.md` | Robots.txt analysis, sitemap audit, canonical review, index/noindex mapping |
| Internal Link Map | `vault/10-Technical/[client]/internal-link-map.md` | Link graph analysis, orphan pages, hub pages, link equity distribution |
| Mobile Audit | `vault/10-Technical/[client]/mobile-audit.md` | Mobile rendering issues, tap target problems, viewport analysis |
| Redirect Map | `vault/10-Technical/[client]/redirect-map.md` | All redirects found, redirect chains, redirect loops |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "technical-seo"
date: YYYY-MM-DD
type: audit
status: complete
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile (must exist in vault before this team runs)
  - Intelligence Layer output (recommended but not blocking — Technical SEO can run with just a site URL)
  - Keyword Research data (recommended — helps prioritize which pages matter most)

- **Feeds into:**
  - **Content SEO Team** — URL inventory tells Content which pages exist; crawl data reveals thin content pages
  - **Link Building Team** — Internal link map reveals pages that need more authority
  - **E-commerce SEO Team** — Crawl data reveals faceted navigation issues, product page structure
  - **AEO Team** — Schema audit informs entity optimization work
  - **Audit & Recommendations Team** — All technical findings feed into the master report
  - **Analytics & Reporting Team** — Technical baselines become tracking benchmarks

## Quality Checks

### Technical SEO-Specific Quality Criteria

1. **Crawl completeness** — Did the Site Crawler discover all expected URLs? Compare crawled count against sitemap count and Firecrawl map count. If there is a significant discrepancy (more than 15%), investigate before proceeding.

2. **Data sourced from tools, not assumptions** — Every status code, page speed metric, and schema finding must come from Firecrawl, Web Fetch, or client-provided data. No "this page is probably slow" without measurement.

3. **Specific fix instructions** — Every issue must include the exact URL, what is wrong, and how to fix it. "Fix your redirect chains" is unacceptable. "Redirect chain: /old-page → /middle-page → /final-page (3 hops, should be 1). Fix: Update /old-page to redirect directly to /final-page" is acceptable.

4. **Priority scoring** — Every finding must be scored by Impact (High/Medium/Low) and Effort (Easy/Medium/Hard). Critical issues (broken pages on high-traffic URLs, noindex on important pages) must be flagged as Critical priority.

5. **No outdated metrics** — Use current Core Web Vitals thresholds (LCP < 2.5s, INP < 200ms, CLS < 0.1). Do not reference deprecated metrics (FID) without noting they are deprecated.

6. **Schema validation** — All generated JSON-LD must be valid according to schema.org specifications. Include the full markup, not just a description of what to add.

7. **Mobile-first perspective** — All audits must evaluate from a mobile-first perspective, since Google uses mobile-first indexing.

8. **Minimum quality score: 3/5. Target: 4/5+.**
