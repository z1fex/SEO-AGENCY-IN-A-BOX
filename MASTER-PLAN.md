# SEO Agency in a Box — Master Plan

> A complete AI-powered SEO agency running inside Claude Code. 75 specialized agents across 12 teams, powered by Firecrawl, Tavily, and Claude's native tools. Self-orchestrating — say "go" and the entire agency runs.
>
> **Note:** This was the original planning document. The built system may have evolved beyond this plan. For the current source of truth, see `CLAUDE.md` (the brain), `instructions/` (the rules), and `agents/` (the team files).

---

## Table of Contents

1. [Vision & Core Concept](#1-vision--core-concept)
2. [Architecture Overview](#2-architecture-overview)
3. [The 8 Teams — Full Hierarchy](#3-the-8-teams--full-hierarchy)
4. [The Pipeline — End-to-End SEO Workflow](#4-the-pipeline--end-to-end-seo-workflow)
5. [Tool Infrastructure — Firecrawl, Tavily, Native](#5-tool-infrastructure--firecrawl-tavily-native)
6. [Directory Structure](#6-directory-structure)
7. [Vault (Memory System)](#7-vault-memory-system)
8. [Workflow System — 11 Workflow Chains](#8-workflow-system--11-workflow-chains)
9. [Command Interface](#9-command-interface)
10. [Agent File Format](#10-agent-file-format)
11. [Quality Gate System](#11-quality-gate-system)
12. [Templates](#12-templates)
13. [Onboarding Flow](#13-onboarding-flow)
14. [Credit Efficiency](#14-credit-efficiency)
15. [Implementation Roadmap](#15-implementation-roadmap)

---

## 1. Vision & Core Concept

### What This Is
A self-contained SEO agency that operates entirely inside Claude Code. You are the agency. Every team, every specialist, every workflow is a prompt file that Claude reads and becomes.

### What Makes It Different From the Original Agency in a Box
| Original (General Agency) | SEO Agency in a Box |
|---------------------------|---------------------|
| 100+ agents across marketing, sales, strategy | 51 agents laser-focused on SEO |
| Uses web search + web fetch only | **Firecrawl** for crawling, **Tavily** for AI search, plus native tools |
| Broad marketing deliverables | Technical audits, keyword clusters, content briefs, backlink analysis, SERP data |
| Generic quality gate | SEO-specific scoring (E-E-A-T, search intent alignment, technical accuracy) |
| General workflows | SEO pipelines (Audit → Research → Strategy → Execute → Monitor → Report) |

### Core Principles
1. **Data-first** — Every recommendation backed by real crawl data, real SERP analysis, real competitor scraping
2. **Tool-powered** — Firecrawl crawls sites, Tavily researches keywords, web fetch validates live pages
3. **Specialist agents** — Each agent has deep SEO expertise in one narrow domain
4. **Pipeline-driven** — Work flows through defined stages: Audit → Research → Strategy → Execute → Monitor → Report
5. **Memory-centric** — Obsidian vault stores all client data, audits, keyword research, and historical performance
6. **Quality-gated** — Every deliverable passes SEO-specific quality checks before delivery

---

## 2. Architecture Overview

```
                        ┌─────────────────────────────┐
                        │      CLAUDE.md (Playbook)    │
                        │   Commands • Rules • Routing │
                        └──────────────┬──────────────┘
                                       │
                 ┌─────────────────────┼─────────────────────┐
                 │                     │                     │
        ┌────────┴────────┐   ┌───────┴───────┐   ┌────────┴────────┐
        │   PLANNING &    │   │   EXECUTION   │   │   MEASUREMENT   │
        │   RESEARCH      │   │   TEAMS       │   │   & REPORTING   │
        └────────┬────────┘   └───────┬───────┘   └────────┬────────┘
                 │                    │                     │
        ┌────────┴────────┐   ┌──────┼──────┐     ┌───────┴────────┐
        │ Strategy Team   │   │      │      │     │ Analytics Team │
        │ Keywords Team   │   │      │      │     └────────────────┘
        └─────────────────┘   │      │      │
                         Technical Content Links
                           Team    Team   Team
                                │
                           ┌────┴────┐
                           │ Local   │
                           │ E-comm  │
                           └─────────┘
```

### Decision Flow
1. **Strategy team** audits, prioritizes, and sets direction
2. **Keywords team** provides the research foundation for all content and optimization
3. **Execution teams** (Technical, Content, Links, Local, E-commerce) do the work
4. **Analytics team** measures results and feeds back to Strategy for iteration

### Data Flow
```
Firecrawl (crawl data) ──→ Technical Team ──→ Audit Findings
Tavily (search data)   ──→ Keywords Team  ──→ Keyword Strategy
Web Fetch (live pages) ──→ Content Team   ──→ Optimized Content
                           Links Team     ──→ Link Prospects
                           Analytics Team ──→ Performance Reports
                                     ↓
                              Strategy Team ──→ Roadmap & Priorities
                                     ↓
                              Client Deliverables
```

---

## 3. The 8 Teams — Full Hierarchy

### Team 1: Technical SEO Team (8 agents)
**Lead:** `agents/technical/_lead.md`
**Purpose:** Crawl, audit, and fix the technical foundation of client sites.
**Primary Tools:** Firecrawl (crawl, map), Web Fetch (validate)

| Agent | File | Role | Tools Used |
|-------|------|------|------------|
| Site Crawler | `site-crawler.md` | Crawl entire sites using Firecrawl, map URL structure, identify broken pages, redirect chains, 404s, orphan pages | Firecrawl `crawl`, `map` |
| Core Web Vitals Analyst | `core-web-vitals-analyst.md` | Analyze page speed, LCP, INP, CLS; identify performance bottlenecks; prioritize fixes | Web Fetch, PageSpeed API |
| Schema Markup Specialist | `schema-specialist.md` | Audit existing structured data, generate JSON-LD schema (Article, FAQ, Product, LocalBusiness, Organization, etc.) | Web Fetch (validate) |
| Indexation Manager | `indexation-manager.md` | Check robots.txt, XML sitemaps, canonical tags, noindex directives, index coverage issues | Firecrawl `crawl`, Web Fetch |
| Internal Linking Architect | `internal-linking-architect.md` | Map internal link structure, identify orphan pages, suggest hub-spoke models, optimize link equity distribution | Firecrawl `map` |
| Mobile SEO Auditor | `mobile-seo-auditor.md` | Mobile-first indexing compliance, responsive design checks, mobile usability issues | Web Fetch |
| Site Migration Specialist | `site-migration-specialist.md` | Pre/post migration audits, URL redirect mapping, 301 planning, traffic monitoring post-launch | Firecrawl `crawl` |
| Log Analyzer | `log-analyzer.md` | Parse server access logs (if provided) for crawl patterns, bot frequency, crawl budget waste | File processing |

---

### Team 2: Keyword Research Team (6 agents)
**Lead:** `agents/keywords/_lead.md`
**Purpose:** Discover, classify, cluster, and prioritize keywords that drive traffic and revenue.
**Primary Tools:** Tavily (search, discover), Firecrawl (competitor scraping)

| Agent | File | Role | Tools Used |
|-------|------|------|------------|
| Keyword Discovery Agent | `keyword-discovery.md` | Find seed keywords, long-tail variations, question keywords, related topics using AI-powered search | Tavily `search` |
| Search Intent Classifier | `intent-classifier.md` | Classify every keyword by search intent: Informational, Commercial Investigation, Transactional, Navigational | Tavily, SERP analysis |
| Keyword Cluster Builder | `cluster-builder.md` | Group keywords into topical clusters, map parent topics to subtopics, identify pillar pages | Analysis + Tavily |
| Competitor Keyword Spy | `competitor-keyword-spy.md` | Scrape competitor pages to extract title tags, H1s, keyword targets, content topics | Firecrawl `scrape` |
| Keyword Gap Analyst | `keyword-gap-analyst.md` | Compare client keyword coverage vs. competitors; identify high-opportunity gaps | Tavily + Firecrawl |
| SERP Analyzer | `serp-analyzer.md` | Analyze SERP features for target keywords: featured snippets, PAA, local packs, image carousels, video results | Tavily, Web Fetch |

---

### Team 3: Content SEO Team (10 agents)
**Lead:** `agents/content/_lead.md`
**Purpose:** Plan, create, and optimize content that ranks and converts.
**Primary Tools:** Tavily (research), Firecrawl (competitor content analysis), Web Fetch

| Agent | File | Role | Tools Used |
|-------|------|------|------------|
| Content Strategist | `content-strategist.md` | Plan topical authority strategy, content pillars, hub & spoke models, content moats | Tavily |
| Content Brief Writer | `brief-writer.md` | Create detailed briefs: target keywords, intent, outline, word count, competitor analysis, SERP features to target | Tavily, Firecrawl |
| SEO Blog Writer | `seo-blog-writer.md` | Write fully optimized long-form blog posts with proper heading hierarchy, keyword placement, internal links, meta tags | Research from vault |
| Landing Page Copywriter | `landing-page-copywriter.md` | Write conversion-optimized landing pages with SEO: hero copy, benefits, CTAs, schema markup suggestions | Research from vault |
| Content Optimizer | `content-optimizer.md` | Audit and rewrite existing content for better rankings: keyword density, readability, freshness, E-E-A-T signals | Firecrawl `scrape`, Tavily |
| Meta Tag Writer | `meta-tag-writer.md` | Write title tags (≤60 chars), meta descriptions (≤155 chars), OG tags at scale for dozens/hundreds of pages | Firecrawl (current tags) |
| Content Gap Analyst | `content-gap-analyst.md` | Find topics competitors cover that the client doesn't; identify content opportunities by topic cluster | Firecrawl, Tavily |
| FAQ & PAA Writer | `faq-paa-writer.md` | Create FAQ sections targeting People Also Ask; write answers optimized for featured snippet extraction | Tavily (PAA scraping) |
| Content Calendar Planner | `content-calendar-planner.md` | Plan monthly/quarterly content schedules factoring seasonality, trends, keyword priority, and publishing capacity | Tavily (trends) |
| Content Performance Analyst | `content-performance-analyst.md` | Analyze which content is performing, declining, or underperforming; recommend updates, consolidation, or pruning | Analytics data |

---

### Team 4: Link Building Team (6 agents)
**Lead:** `agents/links/_lead.md`
**Purpose:** Build high-quality backlinks through outreach, digital PR, and opportunity identification.
**Primary Tools:** Firecrawl (prospect scraping), Tavily (research), Web Fetch

| Agent | File | Role | Tools Used |
|-------|------|------|------------|
| Backlink Auditor | `backlink-auditor.md` | Analyze existing backlink profile quality, identify toxic/spammy links, recommend disavow candidates | Web Fetch, data analysis |
| Link Prospector | `link-prospector.md` | Find link building opportunities: resource pages, guest post targets, broken link replacements, niche directories | Firecrawl, Tavily |
| Outreach Email Writer | `outreach-writer.md` | Write personalized outreach emails for link acquisition: guest posts, resource links, broken link replacements, skyscraper | Templates + personalization |
| Digital PR Strategist | `digital-pr-strategist.md` | Plan newsworthy content (data studies, surveys, infographics) and PR campaigns to earn editorial links at scale | Tavily (journalist research) |
| Broken Link Finder | `broken-link-finder.md` | Find broken outbound links on target sites that can be replaced with client content | Firecrawl `crawl` |
| Competitor Backlink Analyzer | `competitor-backlink-analyzer.md` | Analyze competitor backlink profiles to find replicable link sources, patterns, and strategies | Firecrawl, Tavily |

---

### Team 5: Local SEO Team (5 agents)
**Lead:** `agents/local/_lead.md`
**Purpose:** Optimize local search presence — Google Business Profile, citations, local content, reviews.
**Primary Tools:** Web Fetch, Tavily

| Agent | File | Role | Tools Used |
|-------|------|------|------------|
| GBP Optimizer | `gbp-optimizer.md` | Audit and optimize Google Business Profile: categories, attributes, photos, posts, Q&A, products/services | Web Fetch |
| Local Citation Builder | `citation-builder.md` | Identify NAP citation opportunities across directories, data aggregators, and niche sites; check consistency | Tavily, Web Fetch |
| Local Content Writer | `local-content-writer.md` | Create location-specific content: city pages, service-area pages, local guides, neighborhood content | Tavily (local research) |
| Review Strategist | `review-strategist.md` | Plan review acquisition strategies, draft review response templates, monitor review sentiment | Analysis |
| Local Competitor Analyst | `local-competitor-analyst.md` | Map local competitive landscape: GBP rankings, local pack positions, competitor citations and reviews | Tavily, Web Fetch |

---

### Team 6: Analytics & Reporting Team (6 agents)
**Lead:** `agents/analytics/_lead.md`
**Purpose:** Measure, track, report, and prove ROI on all SEO work.
**Primary Tools:** Data analysis, vault data, Web Fetch

| Agent | File | Role | Tools Used |
|-------|------|------|------------|
| Performance Dashboard Builder | `dashboard-builder.md` | Create comprehensive SEO dashboards with KPIs: organic traffic, rankings, conversions, visibility score | Vault data |
| Ranking Tracker | `ranking-tracker.md` | Monitor keyword ranking positions, track movements, identify wins and losses | Tavily (SERP checks) |
| Traffic Analyst | `traffic-analyst.md` | Analyze organic traffic patterns, segment by landing page, identify seasonality and trends | Client data + analysis |
| Conversion Analyst | `conversion-analyst.md` | Map organic traffic to conversions and revenue; calculate SEO contribution to business goals | Client data |
| Monthly Report Writer | `monthly-report-writer.md` | Generate professional monthly SEO reports with executive summary, KPIs, work completed, next steps | Vault data compilation |
| ROI Calculator | `roi-calculator.md` | Calculate SEO ROI, project growth trajectories, compare against paid channels, forecast organic revenue | Financial modeling |

---

### Team 7: Strategy & Direction Team (5 agents)
**Lead:** `agents/strategy/_lead.md`
**Purpose:** Set direction, compile audits, prioritize work, and build roadmaps.
**Primary Tools:** All team outputs (vault), Tavily

| Agent | File | Role | Tools Used |
|-------|------|------|------------|
| SEO Audit Compiler | `audit-compiler.md` | Compile findings from Technical, Content, Keywords, Links teams into one master audit document | Vault (all audit data) |
| Priority Matrix Builder | `priority-matrix-builder.md` | Score all issues/opportunities by Impact (traffic potential) × Effort (time/resources) → prioritized action list | Analysis |
| SEO Roadmap Planner | `roadmap-planner.md` | Build 3-month, 6-month, and 12-month SEO roadmaps with milestones, dependencies, and expected outcomes | Strategy + vault |
| Competitive Strategy Analyst | `competitive-strategy-analyst.md` | Develop competitive SEO strategies: where to attack, where to defend, where to differentiate | Firecrawl, Tavily |
| Client Communication Manager | `client-communication-manager.md` | Translate technical SEO into business language; write client-facing summaries, presentations, recommendations | Vault deliverables |

---

### Team 8: E-commerce SEO Team (5 agents)
**Lead:** `agents/ecommerce/_lead.md`
**Purpose:** Specialized SEO for online stores — product pages, categories, facets, structured data, feeds.
**Primary Tools:** Firecrawl (product page scraping), Web Fetch, Tavily

| Agent | File | Role | Tools Used |
|-------|------|------|------------|
| Product Page Optimizer | `product-page-optimizer.md` | Optimize product titles, descriptions, images, schema; handle variants and out-of-stock pages | Firecrawl `scrape` |
| Category Page Strategist | `category-strategist.md` | Plan category taxonomy, optimize category pages for keywords, manage thin category content | Firecrawl, analysis |
| Faceted Navigation Auditor | `faceted-navigation-auditor.md` | Identify crawl budget waste from filters/facets, recommend canonical/noindex/parameter handling strategies | Firecrawl `crawl` |
| Product Schema Generator | `product-schema-generator.md` | Generate JSON-LD for Product, AggregateRating, Offer, Review; validate against Google's requirements | Web Fetch (validate) |
| Shopping Feed Optimizer | `shopping-feed-optimizer.md` | Optimize product data feeds for Google Shopping: titles, descriptions, GTINs, categories, custom labels | Data processing |

---

### Agent Count Summary

| Team | Agents | Primary Tools |
|------|--------|---------------|
| Technical SEO | 8 | Firecrawl, Web Fetch |
| Keyword Research | 6 | Tavily, Firecrawl |
| Content SEO | 10 | Tavily, Firecrawl, Web Fetch |
| Link Building | 6 | Firecrawl, Tavily |
| Local SEO | 5 | Web Fetch, Tavily |
| Analytics & Reporting | 6 | Vault data, analysis |
| Strategy & Direction | 5 | All team outputs |
| E-commerce SEO | 5 | Firecrawl, Web Fetch |
| **TOTAL** | **51** | |

---

## 4. The Pipeline — End-to-End SEO Workflow

Every client engagement follows this six-phase pipeline:

```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│   PHASE 1    │───→│   PHASE 2    │───→│   PHASE 3    │
│  DISCOVERY   │    │    AUDIT     │    │   STRATEGY   │
│  & ONBOARD   │    │              │    │              │
└──────────────┘    └──────────────┘    └──────────────┘
                                               │
┌──────────────┐    ┌──────────────┐    ┌──────┴───────┐
│   PHASE 6    │←───│   PHASE 5    │←───│   PHASE 4    │
│  REPORTING   │    │  MONITORING  │    │  EXECUTION   │
│  & ROI       │    │              │    │              │
└──────────────┘    └──────────────┘    └──────────────┘
       │                                       ↑
       └──────── feedback loop ────────────────┘
```

### Phase 1: Discovery & Onboarding
**Teams:** Strategy
**Duration:** Initial session

| Step | Action | Output |
|------|--------|--------|
| 1.1 | Client interview (onboarding flow) | Client profile, site info, goals |
| 1.2 | Site access collection (URLs, analytics access, Search Console) | Access credentials doc |
| 1.3 | Baseline data collection (current traffic, rankings, domain authority) | Baseline metrics doc |

### Phase 2: Comprehensive Audit
**Teams:** Technical, Keywords, Content, Links
**Duration:** First major deliverable

| Step | Action | Agent(s) | Output |
|------|--------|----------|--------|
| 2.1 | Full site crawl | Site Crawler | Crawl data, URL inventory |
| 2.2 | Technical audit | Core Web Vitals, Indexation, Schema, Mobile, Internal Links | Technical findings |
| 2.3 | Keyword research | Discovery, Intent, Clusters, Gap | Keyword strategy |
| 2.4 | Content audit | Content Gap, Content Performance, Content Optimizer | Content findings |
| 2.5 | Competitor analysis | Competitor Keyword Spy, Competitor Backlink Analyzer | Competitor intel |
| 2.6 | Backlink audit | Backlink Auditor | Link profile analysis |
| 2.7 | Compile master audit | Audit Compiler | **Master SEO Audit Report** |

### Phase 3: Strategy Development
**Teams:** Strategy, Keywords
**Duration:** Following audit

| Step | Action | Agent(s) | Output |
|------|--------|----------|--------|
| 3.1 | Build priority matrix | Priority Matrix Builder | Impact × Effort scoring |
| 3.2 | Develop content strategy | Content Strategist | Pillar/cluster content plan |
| 3.3 | Plan link strategy | Digital PR Strategist, Link Prospector | Link building plan |
| 3.4 | Create roadmap | Roadmap Planner | 3/6/12 month SEO roadmap |
| 3.5 | Client presentation | Client Communication Manager | Executive strategy deck |

### Phase 4: Execution
**Teams:** Technical, Content, Links, Local, E-commerce
**Duration:** Ongoing (monthly sprints)

| Track | Actions | Output |
|-------|---------|--------|
| **Technical** | Fix crawl errors, implement schema, optimize page speed, fix canonicals | Technical fix log |
| **Content** | Write briefs → Write content → Optimize existing → Write meta tags | Published content |
| **Links** | Prospect → Outreach → Follow-up → Secure placements | New backlinks |
| **Local** | GBP optimization, citation building, local content, review strategy | Local visibility |
| **E-commerce** | Product optimization, category pages, schema, feeds | E-commerce improvements |

### Phase 5: Monitoring & Optimization
**Teams:** Analytics, Keywords, Technical
**Duration:** Ongoing (weekly)

| Action | Agent | Frequency |
|--------|-------|-----------|
| Track keyword rankings | Ranking Tracker | Weekly |
| Monitor organic traffic | Traffic Analyst | Weekly |
| Check content performance | Content Performance Analyst | Bi-weekly |
| Monitor competitor changes | Competitive Strategy Analyst | Monthly |
| Re-crawl for new issues | Site Crawler | Monthly |

### Phase 6: Reporting & ROI
**Teams:** Analytics, Strategy
**Duration:** Monthly + Quarterly

| Deliverable | Agent | Frequency |
|-------------|-------|-----------|
| Monthly SEO report | Monthly Report Writer | Monthly |
| Performance dashboard | Dashboard Builder | Monthly |
| ROI analysis | ROI Calculator | Monthly |
| Quarterly strategy review | Roadmap Planner + Audit Compiler | Quarterly |
| Client-facing summary | Client Communication Manager | Monthly |

---

## 5. Tool Infrastructure — Firecrawl, Tavily, Native

### MCP Server Configuration

The agency uses MCP (Model Context Protocol) servers for external tool access:

```json
{
  "mcpServers": {
    "firecrawl": {
      "command": "npx",
      "args": ["-y", "firecrawl-mcp"],
      "env": {
        "FIRECRAWL_API_KEY": "fc-your-key-here"
      }
    },
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

### Tool Capabilities Matrix

#### Firecrawl
| Operation | What It Does | SEO Use Case |
|-----------|-------------|--------------|
| `firecrawl_crawl` | Crawl entire websites, follow links, collect all pages | Full site audit, URL inventory, broken link detection |
| `firecrawl_scrape` | Extract content from a single page (markdown, HTML, metadata) | Competitor page analysis, content extraction, schema checking |
| `firecrawl_map` | Get all URLs from a site without full crawl | Quick site structure mapping, sitemap comparison |
| `firecrawl_search` | Search the web and extract content from results | Competitive research, link prospecting |
| `firecrawl_extract` | Extract structured data from pages using LLM | Product data extraction, competitor pricing, feature comparison |

#### Tavily
| Operation | What It Does | SEO Use Case |
|-----------|-------------|--------------|
| `tavily_search` | AI-powered web search with source extraction | Keyword research, topic discovery, SERP analysis, trend spotting |
| `tavily_extract` | Extract and summarize content from URLs | Competitor content analysis, research compilation |

#### Native Claude Code Tools
| Tool | SEO Use Case |
|------|-------------|
| Web Fetch | Validate live pages, check schema, test redirects, fetch sitemaps/robots.txt |
| Web Search | General research, news, industry trends, algorithm update monitoring |
| File Read/Write | Generate reports, process data, manage vault |
| Bash/Scripts | Run data processing scripts, CSV analysis, bulk operations |

### Tool-to-Team Mapping

```
┌─────────────────────────────────────────────────────────────────┐
│                        TOOL LAYER                               │
├──────────────┬───────────────┬──────────────┬──────────────────┤
│  Firecrawl   │    Tavily     │  Web Fetch   │  Web Search      │
│  (Crawl/Map/ │  (AI Search/  │  (Validate/  │  (General        │
│   Scrape/    │   Extract)    │   Check/     │   Research)      │
│   Extract)   │               │   Fetch)     │                  │
├──────────────┼───────────────┼──────────────┼──────────────────┤
│ Technical ●  │ Keywords ●    │ Technical ●  │ All Teams ●      │
│ Keywords ●   │ Content ●     │ Content ●    │                  │
│ Links ●      │ Links ●       │ Links ●      │                  │
│ E-commerce ● │ Strategy ●    │ Local ●      │                  │
│ Content ●    │ Local ●       │ E-commerce ● │                  │
└──────────────┴───────────────┴──────────────┴──────────────────┘
```

### API Key Requirements

| Service | Free Tier | Recommended Plan | Purpose |
|---------|-----------|------------------|---------|
| **Firecrawl** | 500 credits/month | Hobby ($16/mo, 3K credits) or Standard ($83/mo, 250K) | Site crawling, competitor scraping |
| **Tavily** | 1,000 searches/month | Basic (free) or Pro for higher volume | AI-powered search, keyword research |

---

## 6. Directory Structure

```
Agency In a Box/
│
├── CLAUDE.md                          → Master playbook (commands, rules, routing)
├── README.md                          → Setup guide (API keys, MCP config, quick start)
├── MASTER-PLAN.md                     → This document
│
├── agents/                            → All 51 agent prompt files
│   ├── _base/
│   │   ├── quality-gate.md            → SEO-specific quality checks
│   │   └── seo-fundamentals.md        → Core SEO principles all agents share
│   │
│   ├── technical/                     → Technical SEO Team (8 agents)
│   │   ├── _lead.md
│   │   ├── site-crawler.md
│   │   ├── core-web-vitals-analyst.md
│   │   ├── schema-specialist.md
│   │   ├── indexation-manager.md
│   │   ├── internal-linking-architect.md
│   │   ├── mobile-seo-auditor.md
│   │   ├── site-migration-specialist.md
│   │   └── log-analyzer.md
│   │
│   ├── keywords/                      → Keyword Research Team (6 agents)
│   │   ├── _lead.md
│   │   ├── keyword-discovery.md
│   │   ├── intent-classifier.md
│   │   ├── cluster-builder.md
│   │   ├── competitor-keyword-spy.md
│   │   ├── keyword-gap-analyst.md
│   │   └── serp-analyzer.md
│   │
│   ├── content/                       → Content SEO Team (10 agents)
│   │   ├── _lead.md
│   │   ├── content-strategist.md
│   │   ├── brief-writer.md
│   │   ├── seo-blog-writer.md
│   │   ├── landing-page-copywriter.md
│   │   ├── content-optimizer.md
│   │   ├── meta-tag-writer.md
│   │   ├── content-gap-analyst.md
│   │   ├── faq-paa-writer.md
│   │   ├── content-calendar-planner.md
│   │   └── content-performance-analyst.md
│   │
│   ├── links/                         → Link Building Team (6 agents)
│   │   ├── _lead.md
│   │   ├── backlink-auditor.md
│   │   ├── link-prospector.md
│   │   ├── outreach-writer.md
│   │   ├── digital-pr-strategist.md
│   │   ├── broken-link-finder.md
│   │   └── competitor-backlink-analyzer.md
│   │
│   ├── local/                         → Local SEO Team (5 agents)
│   │   ├── _lead.md
│   │   ├── gbp-optimizer.md
│   │   ├── citation-builder.md
│   │   ├── local-content-writer.md
│   │   ├── review-strategist.md
│   │   └── local-competitor-analyst.md
│   │
│   ├── analytics/                     → Analytics & Reporting Team (6 agents)
│   │   ├── _lead.md
│   │   ├── dashboard-builder.md
│   │   ├── ranking-tracker.md
│   │   ├── traffic-analyst.md
│   │   ├── conversion-analyst.md
│   │   ├── monthly-report-writer.md
│   │   └── roi-calculator.md
│   │
│   ├── strategy/                      → Strategy & Direction Team (5 agents)
│   │   ├── _lead.md
│   │   ├── audit-compiler.md
│   │   ├── priority-matrix-builder.md
│   │   ├── roadmap-planner.md
│   │   ├── competitive-strategy-analyst.md
│   │   └── client-communication-manager.md
│   │
│   └── ecommerce/                     → E-commerce SEO Team (5 agents)
│       ├── _lead.md
│       ├── product-page-optimizer.md
│       ├── category-strategist.md
│       ├── faceted-navigation-auditor.md
│       ├── product-schema-generator.md
│       └── shopping-feed-optimizer.md
│
├── workflows/                         → 11 workflow chains
│   ├── full-seo-audit.md
│   ├── keyword-strategy.md
│   ├── content-sprint.md
│   ├── link-building-campaign.md
│   ├── local-seo-setup.md
│   ├── monthly-reporting.md
│   ├── competitor-teardown.md
│   ├── ecommerce-audit.md
│   ├── new-site-launch.md
│   ├── site-migration.md
│   └── quarterly-review.md
│
├── vault/                             → Obsidian-compatible persistent memory
│   ├── 00-Dashboard/
│   │   ├── Agency Dashboard.md
│   │   └── ROI Tracker.md
│   ├── 01-Clients/
│   ├── 02-Audits/
│   ├── 03-Research/
│   ├── 04-Content/
│   ├── 05-Links/
│   ├── 06-Competitors/
│   ├── 07-Reports/
│   ├── 08-Strategy/
│   ├── 09-Local/
│   └── 10-Technical/
│
├── templates/                         → Deliverable templates
│   ├── seo-audit-report.md
│   ├── keyword-research-report.md
│   ├── content-brief.md
│   ├── monthly-seo-report.md
│   ├── backlink-audit-report.md
│   ├── competitor-analysis.md
│   ├── technical-audit.md
│   ├── local-seo-report.md
│   ├── seo-roadmap.md
│   ├── priority-matrix.md
│   └── client-proposal.md
│
├── quality/                           → Quality gate system
│   └── qa-checklist.md
│
├── onboarding/                        → Client onboarding flow
│   └── onboard.md
│
├── tools/                             → Tool guides and helper scripts
│   ├── firecrawl-guide.md
│   ├── tavily-guide.md
│   ├── serp-scraping.md
│   ├── schema-validator.md
│   ├── credit-saving.md
│   └── scripts/
│       ├── crawl-analyzer.py
│       └── keyword-processor.py
│
└── output/                            → Client deliverables
    └── [client-name]/
        └── [YYYY-MM-DD]/
            └── [deliverable]/
```

---

## 7. Vault (Memory System)

### Structure & Purpose

The vault is an Obsidian-compatible knowledge base. Every piece of SEO data, research, and deliverable lives here.

```
vault/
├── 00-Dashboard/                → Agency-level status
│   ├── Agency Dashboard.md      → Active clients, current work, team utilization
│   └── ROI Tracker.md           → Hours saved, deliverables produced, value delivered
│
├── 01-Clients/                  → One folder per client
│   └── [Client Name]/
│       ├── profile.md           → Business overview, site URL, industry, goals
│       ├── site-info.md         → CMS, hosting, analytics IDs, Search Console access
│       ├── competitors.md       → Top 5 SEO competitors with URLs and positioning
│       ├── icp.md               → Ideal customer profile, search behavior, pain points
│       ├── goals.md             → SEO KPIs, target keywords, traffic goals, timeline
│       └── brand-voice.md       → Tone for content creation
│
├── 02-Audits/                   → All audit data
│   └── [Client]/
│       ├── technical-audit-[date].md
│       ├── content-audit-[date].md
│       ├── backlink-audit-[date].md
│       ├── master-audit-[date].md
│       └── crawl-data/          → Raw crawl exports
│
├── 03-Research/                 → All keyword research
│   └── [Client]/
│       ├── seed-keywords-[date].md
│       ├── keyword-clusters-[date].md
│       ├── keyword-gaps-[date].md
│       ├── serp-analysis-[date].md
│       └── intent-mapping-[date].md
│
├── 04-Content/                  → Content library
│   └── [Client]/
│       ├── content-strategy.md
│       ├── content-calendar.md
│       ├── briefs/
│       ├── drafts/
│       ├── published/
│       └── meta-tags/
│
├── 05-Links/                    → Link building data
│   └── [Client]/
│       ├── backlink-profile.md
│       ├── prospects/
│       ├── outreach/
│       ├── placements/
│       └── disavow-list.md
│
├── 06-Competitors/              → Competitor intelligence
│   └── [Client]/
│       ├── [competitor-name]/
│       │   ├── profile.md
│       │   ├── keywords.md
│       │   ├── backlinks.md
│       │   └── content.md
│       └── comparison-matrix.md
│
├── 07-Reports/                  → All reports
│   └── [Client]/
│       ├── monthly/
│       │   ├── [YYYY-MM]-report.md
│       ├── quarterly/
│       └── dashboards/
│
├── 08-Strategy/                 → Strategic documents
│   └── [Client]/
│       ├── priority-matrix.md
│       ├── roadmap.md
│       ├── growth-plan.md
│       └── competitive-strategy.md
│
├── 09-Local/                    → Local SEO data
│   └── [Client]/
│       ├── gbp-audit.md
│       ├── citations.md
│       ├── local-keywords.md
│       └── reviews.md
│
└── 10-Technical/                → Technical SEO data
    └── [Client]/
        ├── crawl-reports/
        ├── schema-markup/
        ├── core-web-vitals/
        ├── redirect-maps/
        └── sitemap-analysis.md
```

### Vault Rules
1. **Before work:** Always read client profile + relevant existing data
2. **After work:** Save results to appropriate vault folder
3. **Link everything:** Use `[[wikilinks]]` — e.g., `[[Acme Corp]]`, `[[Q2 Keyword Strategy]]`
4. **Tag everything:** `#audit`, `#keywords`, `#content`, `#links`, `#local`, `#technical`, `#report`, `#competitor`
5. **No duplication:** Check vault before researching — if data exists and is <30 days old, reuse it
6. **Frontmatter on all files:**
```yaml
---
client: "client-slug"
agent: "agent-name"
date: YYYY-MM-DD
type: audit|keywords|content|links|report|strategy
status: complete|draft|in-progress
tags: [relevant-tags]
---
```

---

## 8. Workflow System — 11 Workflow Chains

### Workflow 1: Full SEO Audit (12 steps)
**File:** `workflows/full-seo-audit.md`
**Teams:** Technical → Keywords → Content → Links → Strategy
**Output:** Master SEO Audit Report with Priority Matrix and Roadmap

```
Step 1:  Site Crawler         → Full site crawl, URL inventory
Step 2:  Indexation Manager   → Robots.txt, sitemaps, canonicals, index coverage
Step 3:  Core Web Vitals      → Page speed, LCP, INP, CLS analysis
Step 4:  Schema Specialist    → Structured data audit
Step 5:  Internal Links       → Link structure mapping and optimization
Step 6:  Mobile SEO Auditor   → Mobile-first indexing compliance
Step 7:  Keyword Discovery    → Seed keywords + competitor keyword analysis
Step 8:  Keyword Gap Analyst  → Gap analysis vs. competitors
Step 9:  Content Gap Analyst  → Content opportunities analysis
Step 10: Backlink Auditor     → Link profile quality assessment
Step 11: Audit Compiler       → Compile all findings into master report
Step 12: Priority Matrix      → Score all issues by Impact × Effort
```

### Workflow 2: Keyword Strategy (7 steps)
**File:** `workflows/keyword-strategy.md`
**Teams:** Keywords → Content
**Output:** Complete keyword strategy with clusters, intent mapping, and content plan

```
Step 1: Keyword Discovery     → Seed keywords, long-tail, questions
Step 2: SERP Analyzer         → Analyze SERP features for top targets
Step 3: Intent Classifier     → Map all keywords to search intent
Step 4: Competitor Keyword Spy→ Extract competitor keyword targets
Step 5: Keyword Gap Analyst   → Identify gaps and opportunities
Step 6: Cluster Builder       → Group into topical clusters
Step 7: Content Strategist    → Map clusters to content plan
```

### Workflow 3: Content Sprint (8 steps)
**File:** `workflows/content-sprint.md`
**Teams:** Keywords → Content
**Output:** Batch of fully optimized content pieces (briefs + articles + meta tags)

```
Step 1: Content Calendar      → Select topics for this sprint
Step 2: SERP Analyzer         → Analyze competition for each topic
Step 3: Brief Writer          → Create detailed content briefs
Step 4: SEO Blog Writer       → Write full articles from briefs
Step 5: Meta Tag Writer       → Write title tags + meta descriptions
Step 6: FAQ & PAA Writer      → Add FAQ sections to each piece
Step 7: Content Optimizer     → Final optimization pass
Step 8: Quality Gate          → SEO quality checks on all content
```

### Workflow 4: Link Building Campaign (6 steps)
**File:** `workflows/link-building-campaign.md`
**Teams:** Links → Content
**Output:** Outreach-ready link building campaign with prospects, emails, and tracking

```
Step 1: Backlink Auditor      → Assess current link profile
Step 2: Competitor Backlinks  → Analyze competitor link sources
Step 3: Link Prospector       → Find new link opportunities
Step 4: Digital PR Strategist → Plan linkable content assets
Step 5: Outreach Writer       → Write personalized outreach emails
Step 6: Broken Link Finder    → Find broken link replacement opportunities
```

### Workflow 5: Local SEO Setup (5 steps)
**File:** `workflows/local-seo-setup.md`
**Teams:** Local → Content → Keywords
**Output:** Complete local SEO optimization plan and initial content

```
Step 1: GBP Optimizer         → Audit and optimize Google Business Profile
Step 2: Citation Builder      → Identify citation opportunities
Step 3: Local Competitor      → Map local competitive landscape
Step 4: Local Content Writer  → Create location-specific pages
Step 5: Review Strategist     → Plan review acquisition strategy
```

### Workflow 6: Monthly Reporting (5 steps)
**File:** `workflows/monthly-reporting.md`
**Teams:** Analytics → Strategy
**Output:** Professional monthly SEO report

```
Step 1: Ranking Tracker       → Keyword position changes
Step 2: Traffic Analyst       → Organic traffic analysis
Step 3: Content Performance   → Content metrics review
Step 4: ROI Calculator        → Calculate month's SEO ROI
Step 5: Monthly Report Writer → Compile into formatted report
```

### Workflow 7: Competitor Teardown (6 steps)
**File:** `workflows/competitor-teardown.md`
**Teams:** Keywords → Links → Technical → Strategy
**Output:** Deep competitor analysis with actionable opportunities

```
Step 1: Site Crawler          → Crawl competitor site (Firecrawl)
Step 2: Competitor Keyword Spy→ Extract all keyword targets
Step 3: Competitor Backlinks  → Analyze their link profile
Step 4: Content Gap Analyst   → Content they have that you don't
Step 5: SERP Analyzer         → Head-to-head SERP comparison
Step 6: Competitive Strategy  → Attack, defend, differentiate plan
```

### Workflow 8: E-commerce Audit (6 steps)
**File:** `workflows/ecommerce-audit.md`
**Teams:** E-commerce → Technical → Keywords
**Output:** Complete e-commerce SEO audit and optimization plan

```
Step 1: Product Page Optimizer→ Audit product pages at scale
Step 2: Category Strategist   → Review category taxonomy and optimization
Step 3: Faceted Nav Auditor   → Check crawl budget waste from filters
Step 4: Product Schema        → Audit and generate product structured data
Step 5: Shopping Feed         → Review product feed optimization
Step 6: Priority Matrix       → Prioritize all e-commerce fixes
```

### Workflow 9: New Site Launch (8 steps)
**File:** `workflows/new-site-launch.md`
**Teams:** Strategy → Keywords → Technical → Content
**Output:** Complete SEO foundation for a new website

```
Step 1: Keyword Discovery     → Build keyword foundation
Step 2: Cluster Builder       → Map site architecture to clusters
Step 3: Content Strategist    → Plan initial content
Step 4: Schema Specialist     → Plan structured data implementation
Step 5: Indexation Manager    → Configure robots.txt, sitemaps, canonicals
Step 6: SEO Blog Writer       → Write foundational content pieces
Step 7: Meta Tag Writer       → Write all initial meta tags
Step 8: Roadmap Planner       → Create 6-month launch roadmap
```

### Workflow 10: Site Migration (7 steps)
**File:** `workflows/site-migration.md`
**Teams:** Technical → Content → Analytics
**Output:** Migration plan, redirect map, and monitoring setup

```
Step 1: Site Crawler          → Pre-migration crawl (complete URL inventory)
Step 2: Migration Specialist  → Create URL mapping and redirect plan
Step 3: Indexation Manager    → Plan sitemap and canonical updates
Step 4: Meta Tag Writer       → Update meta tags for new URLs
Step 5: Internal Links        → Plan internal link updates
Step 6: Dashboard Builder     → Set up post-migration monitoring
Step 7: Migration Specialist  → Post-migration audit checklist
```

### Workflow 11: Quarterly Review (6 steps)
**File:** `workflows/quarterly-review.md`
**Teams:** Analytics → Strategy
**Output:** Quarterly performance review and next-quarter roadmap

```
Step 1: Traffic Analyst       → Quarter-over-quarter traffic analysis
Step 2: Ranking Tracker       → Keyword ranking progress report
Step 3: ROI Calculator        → Quarter ROI and growth projections
Step 4: Competitive Strategy  → Updated competitive landscape
Step 5: Roadmap Planner       → Next quarter roadmap and milestones
Step 6: Client Communication  → Executive quarterly summary
```

---

## 9. Command Interface

### Core Commands

| Command | Action |
|---------|--------|
| `onboard` | Run SEO client onboarding interview |
| `switch client [name]` | Load client profile from vault |
| `dashboard` | Show agency dashboard |
| `status` | Current client, active work, recent deliverables |
| `roi` | Show ROI tracker |
| `list teams` | Show all 8 teams and their agents |
| `list workflows` | Show all 11 workflows |
| `save credits` | Show credit-saving tips |

### Audit Commands

| Command | Action |
|---------|--------|
| `audit` | Run full SEO audit workflow (12 steps) |
| `audit technical` | Run technical audit only |
| `audit content` | Run content audit only |
| `audit backlinks` | Run backlink audit only |
| `audit ecommerce` | Run e-commerce audit |
| `audit local` | Run local SEO audit |

### Research Commands

| Command | Action |
|---------|--------|
| `keywords [topic]` | Run keyword research workflow |
| `competitor teardown [url]` | Deep competitor analysis |
| `serp [keyword]` | Analyze SERP for a specific keyword |
| `gaps` | Run keyword + content gap analysis |

### Execution Commands

| Command | Action |
|---------|--------|
| `content sprint` | Run content sprint workflow |
| `write brief [topic]` | Create a single content brief |
| `write blog [topic]` | Write a single SEO blog post |
| `write meta [url/page]` | Write meta tags for specific pages |
| `links campaign` | Run link building campaign workflow |
| `local seo` | Run local SEO setup workflow |

### Team Commands

| Command | Action |
|---------|--------|
| `run [team]` | Run team lead (orchestrates the full team) |
| `run [team] [agent]` | Run a specific agent |

### Reporting Commands

| Command | Action |
|---------|--------|
| `report monthly` | Generate monthly SEO report |
| `report quarterly` | Generate quarterly review |
| `report roadmap` | Show/update SEO roadmap |

### Workflow Commands

| Command | Action |
|---------|--------|
| `workflow [name]` | Run any named workflow from `workflows/` |
| `crawl [url]` | Quick Firecrawl crawl of a URL |
| `research [topic]` | Quick Tavily research on a topic |
| `qa [file]` | Run quality gate on a deliverable |

---

## 10. Agent File Format

Every agent follows this standardized structure:

```markdown
# [Agent Name]
> **Team:** [Team Name] | **Role:** [One-line description]

## Identity

You are the [Agent Name], a specialist in [specific domain].
Your expertise: [2-3 sentences on deep knowledge areas].
You [specific behavioral trait — e.g., "never make claims without data"].

## Tools

- **Firecrawl:** [specific operations this agent uses, or "Not used"]
- **Tavily:** [specific operations, or "Not used"]
- **Web Fetch:** [specific operations, or "Not used"]
- **Vault:** [what to read/write]

## When to Use

- [Specific trigger 1]
- [Specific trigger 2]
- [Specific trigger 3]

## Instructions

### Pre-Work
1. Read client profile: `vault/01-Clients/[client]/profile.md`
2. Read [relevant existing data from vault]
3. [Check for existing work to avoid duplication]

### Process
1. [Step-by-step numbered instructions]
2. [Each step is concrete and actionable]
3. [Include which tool to use at each step]
4. [Include what data to extract/analyze]

### Post-Work
1. Run quality gate (`agents/_base/quality-gate.md`)
2. Save to vault: `vault/[section]/[client]/[filename]-[date].md`
3. Save to output: `output/[client]/[date]/[filename].md`

## Output Format

```
[Exact markdown template for this agent's deliverable]
[With {{placeholders}} for dynamic content]
[Including frontmatter, sections, tables, etc.]
```

## Quality Criteria

- [ ] [Specific quality check 1 for this agent]
- [ ] [Specific quality check 2]
- [ ] [Specific quality check 3]
- [ ] All data sourced from real tools (no hallucination)
- [ ] Saved to vault and output folders
```

---

## 11. Quality Gate System

### SEO-Specific Quality Checklist

Every deliverable must pass these checks:

#### Accuracy (Non-negotiable)
- [ ] All data sourced from Firecrawl crawls, Tavily searches, or Web Fetch — never hallucinated
- [ ] All keyword data based on real SERP analysis, not guesswork
- [ ] Competitor claims verified by scraping their actual sites
- [ ] Technical recommendations based on actual crawl findings
- [ ] No outdated SEO advice (e.g., keyword density targets, exact match anchor text ratios)

#### SEO Best Practices
- [ ] Recommendations follow current Google guidelines (not black hat)
- [ ] E-E-A-T signals considered (Experience, Expertise, Authoritativeness, Trustworthiness)
- [ ] Search intent alignment verified for all keyword-to-content mappings
- [ ] No keyword stuffing in content deliverables
- [ ] Schema markup validates against Google's structured data requirements

#### Completeness
- [ ] No placeholder text, no TODOs, no "insert here" sections
- [ ] All recommendations are specific and actionable (not generic advice)
- [ ] Priority/impact scores assigned where applicable
- [ ] Next steps clearly defined
- [ ] Client-specific (not templated boilerplate)

#### Client Alignment
- [ ] Matches client's brand voice (for content deliverables)
- [ ] Addresses client's stated SEO goals and KPIs
- [ ] Recommendations feasible given client's resources/CMS/budget
- [ ] Competitor analysis uses the client's actual competitors

#### Vault Integration
- [ ] Saved to correct vault location with proper frontmatter
- [ ] Tagged appropriately
- [ ] Linked with `[[wikilinks]]` to related documents
- [ ] Dashboard updated if significant deliverable
- [ ] ROI tracker updated

### Quality Scoring
- **5/5** — Exceptional: Agency-grade, ready for client presentation
- **4/5** — Strong: Professional quality, minor polish possible
- **3/5** — Acceptable: Meets standards, can deliver (minimum threshold)
- **2/5** — Below standard: Needs revision before delivery
- **1/5** — Unacceptable: Major issues, redo required

**Minimum to deliver: 3/5**

---

## 12. Templates

### Template Files to Create

| Template | Purpose | Key Sections |
|----------|---------|--------------|
| `seo-audit-report.md` | Master SEO audit | Executive summary, technical findings, keyword analysis, content gaps, backlink profile, priority matrix, roadmap |
| `keyword-research-report.md` | Keyword strategy | Keyword list, intent mapping, clusters, gaps, SERP features, content recommendations |
| `content-brief.md` | Content creation brief | Target keyword, intent, outline, word count, competitor analysis, SERP targets, internal links, schema suggestions |
| `monthly-seo-report.md` | Monthly report | Executive summary, ranking changes, traffic analysis, content performance, link growth, work completed, next month plan |
| `backlink-audit-report.md` | Link profile analysis | Profile overview, quality distribution, toxic links, competitor comparison, recommendations |
| `competitor-analysis.md` | Competitor deep dive | Profile, keyword overlap, content comparison, link profile, technical comparison, opportunities |
| `technical-audit.md` | Technical SEO audit | Crawl summary, indexation, Core Web Vitals, schema, internal links, mobile, security |
| `local-seo-report.md` | Local SEO status | GBP audit, citations, local rankings, reviews, local competitors, recommendations |
| `seo-roadmap.md` | Strategic roadmap | 3/6/12 month phases, milestones, KPI targets, dependencies, resource requirements |
| `priority-matrix.md` | Issue prioritization | Impact × Effort matrix, scored issue list, quick wins, strategic investments |
| `client-proposal.md` | New client proposal | Business case for SEO, competitive landscape, proposed strategy, timeline, pricing |

---

## 13. Onboarding Flow

### Phase 1 — Business Basics (5 questions)
1. Company name, industry, website URL
2. What do you sell/offer? Who buys it?
3. How long have you been in business? Team size?
4. Current monthly organic traffic (estimate)?
5. CMS platform (WordPress, Shopify, custom, etc.)?

### Phase 2 — SEO History (4 questions)
1. Have you done SEO before? Agency, in-house, or DIY?
2. What's worked? What hasn't?
3. Do you have Google Search Console and Analytics access?
4. Any technical constraints (can't change code, limited CMS, etc.)?

### Phase 3 — Competition (3 questions)
1. Who are your top 3-5 SEO competitors? (URLs)
2. Who's winning in organic search in your space?
3. What keywords would you love to rank for?

### Phase 4 — Goals & Priorities (4 questions)
1. Top 3 SEO goals (traffic, leads, revenue, local visibility)?
2. Target keywords or topics (if any)?
3. 90-day success = what exactly?
4. Budget context (content budget, tool budget)?

### Phase 5 — Content & Brand (3 questions)
1. Brand voice: formal or casual? Technical or simple?
2. Do you have existing content? How much?
3. Who creates content today?

### After Interview — Create 5 Files:
1. **profile.md** — Business overview, site info, industry context
2. **site-info.md** — CMS, hosting, analytics IDs, Search Console access, technical constraints
3. **competitors.md** — SEO competitors with URLs, strengths, weaknesses
4. **goals.md** — SEO KPIs, target keywords, traffic targets, timeline, budget
5. **brand-voice.md** — Tone, style, content examples

---

## 14. Credit Efficiency

### Rules for SEO Agency
1. **Load agents on demand** — Only read the agent file for the current task
2. **Reuse vault data** — Before crawling or researching, check if data <30 days old exists in vault
3. **Batch operations** — Write all meta tags in one pass, all content briefs in one pass
4. **Firecrawl smart** — Use `map` before `crawl` (map is cheaper); cache crawl results in vault
5. **Tavily smart** — Combine related searches; save results to vault for reuse
6. **Template-driven** — Pre-structured output = fewer thinking tokens
7. **Be terse** — Deliver the work, not paragraphs explaining the work

### Estimated Credit Usage by Workflow

| Workflow | Base Cost | Optimized Cost |
|----------|-----------|----------------|
| Client Onboarding | Low | Low |
| Full SEO Audit (12 steps) | Very High | High (reuse existing data) |
| Keyword Strategy (7 steps) | High | Medium (batch searches) |
| Content Sprint (8 steps) | High | Medium (batch writing) |
| Link Building Campaign (6 steps) | Medium | Medium |
| Monthly Report (5 steps) | Medium | Low (vault data compilation) |
| Competitor Teardown (6 steps) | High | Medium (cache competitor data) |
| Local SEO Setup (5 steps) | Medium | Low-Medium |
| E-commerce Audit (6 steps) | High | Medium |

---

## 15. Implementation Roadmap

### Phase 1: Foundation (Build First)
- [ ] `CLAUDE.md` — Master playbook with all commands and rules
- [ ] `README.md` — Setup guide for API keys and MCP configuration
- [ ] `onboarding/onboard.md` — Client onboarding flow
- [ ] `agents/_base/quality-gate.md` — SEO quality gate
- [ ] `agents/_base/seo-fundamentals.md` — Core SEO knowledge base
- [ ] Vault folder structure (all 00-10 folders)
- [ ] `tools/firecrawl-guide.md` — How agents use Firecrawl
- [ ] `tools/tavily-guide.md` — How agents use Tavily
- [ ] `tools/credit-saving.md` — Credit optimization guide

### Phase 2: Core Teams (Build Second)
- [ ] Technical SEO Team (8 agents) — The backbone of every audit
- [ ] Keyword Research Team (6 agents) — The foundation of every strategy
- [ ] Content SEO Team (10 agents) — The highest-volume deliverables

### Phase 3: Supporting Teams (Build Third)
- [ ] Link Building Team (6 agents)
- [ ] Analytics & Reporting Team (6 agents)
- [ ] Strategy & Direction Team (5 agents)

### Phase 4: Specialist Teams (Build Fourth)
- [ ] Local SEO Team (5 agents)
- [ ] E-commerce SEO Team (5 agents)

### Phase 5: Workflows & Templates
- [ ] All 11 workflow files
- [ ] All 11 template files

### Phase 6: Polish & Test
- [ ] Test each workflow end-to-end with a real client
- [ ] Refine agent prompts based on output quality
- [ ] Optimize credit usage
- [ ] Update vault structure as needed

---

## Summary

| Dimension | Spec |
|-----------|------|
| **Teams** | 8 specialized SEO teams |
| **Agents** | 51 specialist agents |
| **Workflows** | 11 end-to-end workflow chains |
| **Templates** | 11 deliverable templates |
| **Tools** | Firecrawl + Tavily + Web Fetch + Web Search |
| **Vault Sections** | 11 (00-Dashboard through 10-Technical) |
| **Commands** | 25+ quick commands |
| **Pipeline Phases** | 6 (Discovery → Audit → Strategy → Execute → Monitor → Report) |
| **Quality Gate** | SEO-specific with E-E-A-T, search intent, data accuracy checks |

This is a production-ready SEO agency. Every agent knows its tools, every workflow has clear handoffs, and every deliverable passes quality checks before delivery.
