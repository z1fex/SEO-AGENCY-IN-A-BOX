<div align="center">

# 🔍 SEO Agency in a Box

### Your full-service AI-powered SEO agency. 12 teams. 75 agents. Self-orchestrating.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Agents](https://img.shields.io/badge/🤖_Agents-75-brightgreen)](#the-12-teams)
[![Teams](https://img.shields.io/badge/👥_Teams-12-red)](#the-12-teams)
[![Workflows](https://img.shields.io/badge/⚡_Workflows-11-orange)](#workflows)
[![Templates](https://img.shields.io/badge/📄_Templates-11-purple)](#templates)
[![Battle Tested](https://img.shields.io/badge/🧪_Battle--Tested-3%20Simulations-yellow)](#battle-tested)
[![Firecrawl](https://img.shields.io/badge/🔥_Firecrawl-Powered-FF6B35)](#quick-start)
[![Tavily](https://img.shields.io/badge/🔎_Tavily-Powered-4A90D9)](#quick-start)

<br>

> **Clone this repo. Add your API keys. Open in Claude Code. Say `go`.**
> The entire SEO agency runs automatically — research, audit, strategy, content, links, AEO — and delivers one master report.

**Powered by [🔥 Firecrawl](https://firecrawl.dev) + [🔎 Tavily](https://tavily.com) + [🤖 Claude Code](https://claude.ai/code)**

<br>

[🚀 Quick Start](#-quick-start) · [👥 All Teams](#-the-12-teams) · [⚡ Workflows](#-workflows) · [🧠 How It Works](#-how-it-works) · [💬 Commands](#-commands) · [📦 Obsidian Setup](#-obsidian-setup) · [💰 Save Credits](#-credit-saving-guide)

</div>

---

## 📑 Table of Contents

- [💡 What Is This?](#-what-is-this)
- [🚀 Quick Start](#-quick-start)
- [👥 The 12 Teams](#-the-12-teams)
- [💬 Commands](#-commands)
- [⚡ Workflows](#-workflows)
- [🧠 How It Works](#-how-it-works)
- [🤖 The Auto-Pilot (`go` Command)](#-the-auto-pilot-go-command)
- [📦 Obsidian Setup](#-obsidian-setup)
- [📁 Project Structure](#-project-structure)
- [📄 Templates](#-templates)
- [✅ Quality Gate](#-quality-gate)
- [💰 Credit-Saving Guide](#-credit-saving-guide)
- [🧪 Battle-Tested](#-battle-tested)
- [📖 Step-by-Step Walkthrough](#-step-by-step-walkthrough)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)

---

## 💡 What Is This?

Most businesses either can't afford an SEO agency ($3,000–$10,000/month) or get stuck with generic audits that say "improve your page speed" with zero specifics.

**SEO Agency in a Box fixes that.**

It's a complete SEO agency — 12 specialized teams with 75 AI agents — running entirely inside [Claude Code](https://docs.anthropic.com/en/docs/claude-code). It uses [Firecrawl](https://firecrawl.dev) to crawl real websites and [Tavily](https://tavily.com) for AI-powered research. Every recommendation is backed by actual data from your actual site.

Here's what makes it different:

- **It crawls your real site.** Firecrawl scrapes your pages, finds broken links, checks schema, maps your internal links — real crawl data, not guesswork.
- **It researches with AI search.** Tavily finds keywords, analyzes SERPs, spots trends, and discovers what your competitors are doing — with sources.
- **It self-orchestrates.** Say `go` and the entire agency runs: intelligence gathering, technical audit, content analysis, competitor research, AEO optimization — then compiles everything into one prioritized report.
- **It covers AEO (Answer Engine Optimization).** Not just Google — it optimizes for AI Overviews, Perplexity, ChatGPT Search, featured snippets, and knowledge panels.
- **It remembers everything.** An [Obsidian](https://obsidian.md)-compatible vault stores all research, audits, keyword data, and deliverables. Every session builds on the last.
- **It checks its own work.** Every deliverable passes through a quality gate that verifies data accuracy, specificity, E-E-A-T alignment, and client relevance.
- **Every fix is copy-paste ready.** No generic "improve your SEO." Every recommendation includes what to change, where, how, why, and the expected impact.

---

## 🚀 Quick Start

### Step 1: Clone the repo

```bash
git clone https://github.com/z1fex/SEO-AGENCY-IN-A-BOX.git
cd SEO-AGENCY-IN-A-BOX
```

### Step 2: Get your API keys (2 minutes)

| Service | Get Key | Free Tier |
|---------|---------|-----------|
| [Firecrawl](https://firecrawl.dev) | Sign up → Dashboard → API Keys | 500 credits/month |
| [Tavily](https://tavily.com) | Sign up → API Keys | 1,000 searches/month |

### Step 3: Configure MCP servers

Add this to your Claude Code settings (`.claude/settings.json` or VS Code extension settings):

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

> **Requires Node.js** for the `npx` commands. [Download Node.js](https://nodejs.org) if you don't have it.

### Step 4: Open in Claude Code

Open the folder in Claude Code — works with CLI, VS Code extension, or desktop app. Claude reads `CLAUDE.md` automatically and becomes your SEO agency.

### Step 5: Onboard your business

```
You: onboard
```

The agency interviews you about your business, SEO history, competitors, goals, and brand voice. After the interview, it creates your complete client profile in the vault.

**Or — Quick Onboard:** Just give it your URL.

```
You: Here's my website: example.com
```

The agency scrapes your site with Firecrawl, auto-fills what it can, asks only 5 critical questions, and you're ready to go.

### Step 6: Run the agency

```
You: go
```

The entire SEO agency runs automatically. Research, audit, analysis, compilation, delivery. One command.

---

## 👥 The 12 Teams

<table>
<tr>
<td width="50" align="center"><strong>#</strong></td>
<td width="60" align="center"><strong>Layer</strong></td>
<td width="180"><strong>Team</strong></td>
<td width="60" align="center"><strong>Agents</strong></td>
<td><strong>What They Do</strong></td>
</tr>
<tr>
<td align="center">1</td>
<td align="center">Intel</td>
<td>🔬 <strong>Research</strong></td>
<td align="center">6</td>
<td>Market intelligence, algorithm update monitoring, SERP feature research, industry trends, AI search landscape analysis</td>
</tr>
<tr>
<td align="center">2</td>
<td align="center">Intel</td>
<td>🕵️ <strong>Competitor Analysis</strong></td>
<td align="center">6</td>
<td>Full competitor site crawling with Firecrawl, keyword extraction, content analysis, backlink profiling, technical benchmarking, SERP position tracking</td>
</tr>
<tr>
<td align="center">3</td>
<td align="center">Intel</td>
<td>🔑 <strong>Keyword Research</strong></td>
<td align="center">6</td>
<td>Keyword discovery via Tavily, search intent classification, topical cluster building, competitor keyword spying, keyword gap analysis, SERP feature analysis</td>
</tr>
<tr>
<td align="center">4</td>
<td align="center">Execute</td>
<td>⚙️ <strong>Technical SEO</strong></td>
<td align="center">8</td>
<td>Full site crawling, Core Web Vitals analysis, schema markup auditing and generation (JSON-LD), indexation checks, internal link mapping, mobile audits, site migration planning, log analysis</td>
</tr>
<tr>
<td align="center">5</td>
<td align="center">Execute</td>
<td>✍️ <strong>Content SEO</strong></td>
<td align="center">10</td>
<td>Topical authority strategy, content briefs, SEO blog writing, landing page copy, content optimization, meta tags at scale, FAQ/PAA sections, content calendars, performance analysis</td>
</tr>
<tr>
<td align="center">6</td>
<td align="center">Execute</td>
<td>🔗 <strong>Link Building</strong></td>
<td align="center">6</td>
<td>Backlink profile auditing, link prospecting with Firecrawl, personalized outreach emails, digital PR strategy, broken link finding, competitor backlink analysis</td>
</tr>
<tr>
<td align="center">7</td>
<td align="center">Execute</td>
<td>🤖 <strong>AEO</strong></td>
<td align="center">7</td>
<td>AI Overview optimization (Google), Perplexity optimization, conversational query research, entity optimization for knowledge graphs, featured snippet strategy, Knowledge Panel management, AI citation tracking</td>
</tr>
<tr>
<td align="center">8</td>
<td align="center">Execute</td>
<td>📍 <strong>Local SEO</strong></td>
<td align="center">5</td>
<td>Google Business Profile optimization, local citation building (NAP consistency), location-specific content, review acquisition strategy, local competitor mapping</td>
</tr>
<tr>
<td align="center">9</td>
<td align="center">Execute</td>
<td>🛒 <strong>E-commerce SEO</strong></td>
<td align="center">5</td>
<td>Product page optimization, category taxonomy strategy, faceted navigation auditing, product schema generation (JSON-LD), shopping feed optimization</td>
</tr>
<tr>
<td align="center">10</td>
<td align="center">Output</td>
<td>📋 <strong>Audit & Recommendations</strong></td>
<td align="center">5</td>
<td>Compiles ALL team findings into one master report with prioritized recommendations, copy-paste-ready fixes, and an executive summary in business language</td>
</tr>
<tr>
<td align="center">11</td>
<td align="center">Output</td>
<td>📊 <strong>Analytics & Reporting</strong></td>
<td align="center">6</td>
<td>SEO dashboards, keyword ranking tracking, organic traffic analysis, conversion attribution, professional monthly reports, ROI calculation and forecasting</td>
</tr>
<tr>
<td align="center">12</td>
<td align="center">Strategy</td>
<td>🧭 <strong>Strategy & Direction</strong></td>
<td align="center">5</td>
<td>SEO strategy development, Impact x Effort priority matrices, 3/6/12 month roadmaps, competitive strategy (attack/defend/differentiate), client-facing communication</td>
</tr>
</table>

---

## 💬 Commands

### 🎯 Core

| Command | What Happens |
|---------|-------------|
| `go` | **Auto-pilot** — runs the entire agency: research → audit → compile → deliver |
| `onboard` | Interactive client interview — builds your complete profile |
| `switch client [name]` | Switch between multiple client profiles |
| `dashboard` | View agency status, active clients, deliverables |
| `status` | Current client, recent work, what's next |
| `catch up` | Check what's done, what's missing, recommend next steps |
| `roi` | See deliverables produced and estimated cost savings |

### 🔍 Audit

| Command | What Happens |
|---------|-------------|
| `audit` | Full SEO audit — all teams contribute, Audit team compiles one master report |
| `audit technical` | Technical audit only (crawl, speed, schema, indexation, mobile) |
| `audit content` | Content audit only (gaps, quality, optimization opportunities) |
| `audit backlinks` | Backlink profile audit only |
| `audit aeo` | AEO audit (AI Overviews, snippets, entities, citations) |
| `audit ecommerce` | E-commerce SEO audit (products, categories, facets, feeds) |
| `audit local` | Local SEO audit (GBP, citations, reviews) |
| `audit competitor [url]` | Deep competitor analysis with Firecrawl |

### 🔬 Research

| Command | What Happens |
|---------|-------------|
| `keywords [topic]` | Full keyword research workflow with clusters and gaps |
| `competitor teardown [url]` | Crawl a competitor site and analyze everything |
| `serp [keyword]` | Analyze SERP features for a specific keyword |
| `gaps` | Run keyword + content gap analysis |
| `research [topic]` | Quick Tavily research on any topic |
| `trends` | Current SEO and AI search trends |

### ⚙️ Execution

| Command | What Happens |
|---------|-------------|
| `content sprint` | Batch content creation — calendar → briefs → articles → meta tags |
| `write brief [topic]` | Create one detailed content brief |
| `write blog [topic]` | Write one SEO-optimized blog post |
| `write meta [pages]` | Write title tags + meta descriptions at scale |
| `links campaign` | Full link building campaign with prospects and outreach emails |
| `local seo` | Local SEO setup (GBP, citations, local content, reviews) |
| `aeo optimize` | AEO optimization workflow |

### 📊 Reporting

| Command | What Happens |
|---------|-------------|
| `report` | Master audit report with all findings and prioritized fixes |
| `report monthly` | Professional monthly SEO performance report |
| `report quarterly` | Quarterly review with next-quarter roadmap |
| `report roadmap` | Show or update the SEO roadmap |

### 🏗️ Team Commands

| Command | What Happens |
|---------|-------------|
| `run [team]` | Run a specific team's full workflow |
| `run [team] [agent]` | Run one specific agent |
| `workflow [name]` | Run a named workflow from `workflows/` |
| `crawl [url]` | Quick Firecrawl crawl of any URL |
| `qa [file]` | Run quality gate on a deliverable |
| `list teams` | Show all 12 teams and their agents |
| `list workflows` | Show all 11 workflows |
| `save credits` | Show credit-saving tips |

---

## ⚡ Workflows

Each workflow chains multiple agents together. One command delivers a complete package.

<table>
<tr>
<td width="200"><strong>Workflow</strong></td>
<td width="50" align="center"><strong>Steps</strong></td>
<td><strong>What You Get</strong></td>
</tr>
<tr>
<td>🔍 <strong>Full SEO Audit</strong></td>
<td align="center">12</td>
<td>Complete site crawl, technical audit, keyword analysis, content gaps, backlink profile, AEO assessment, competitor comparison, priority matrix, roadmap — compiled into one master report</td>
</tr>
<tr>
<td>🔑 <strong>Keyword Strategy</strong></td>
<td align="center">7</td>
<td>Keyword discovery, SERP analysis, intent classification, competitor keyword spying, gap analysis, topical clusters, content plan</td>
</tr>
<tr>
<td>✍️ <strong>Content Sprint</strong></td>
<td align="center">8</td>
<td>Content calendar, SERP research, detailed briefs, fully written blog posts, meta tags, FAQ sections with schema, optimization pass</td>
</tr>
<tr>
<td>🔗 <strong>Link Building Campaign</strong></td>
<td align="center">6</td>
<td>Backlink audit, competitor link analysis, prospect discovery, broken link opportunities, digital PR plan, personalized outreach emails</td>
</tr>
<tr>
<td>📍 <strong>Local SEO Setup</strong></td>
<td align="center">5</td>
<td>Local competitor mapping, GBP optimization, citation audit, location-specific content, review strategy</td>
</tr>
<tr>
<td>📊 <strong>Monthly Reporting</strong></td>
<td align="center">5</td>
<td>Ranking tracking, traffic analysis, conversion data, ROI calculation, professional monthly report</td>
</tr>
<tr>
<td>🕵️ <strong>Competitor Teardown</strong></td>
<td align="center">6</td>
<td>Full competitor crawl, keyword extraction, content analysis, backlink profiling, SERP comparison, competitive strategy</td>
</tr>
<tr>
<td>🛒 <strong>E-commerce Audit</strong></td>
<td align="center">6</td>
<td>Faceted navigation audit, category strategy, product page optimization, product schema, shopping feed review, prioritized fixes</td>
</tr>
<tr>
<td>🚀 <strong>New Site Launch</strong></td>
<td align="center">8</td>
<td>Keyword foundation, site architecture, content strategy, schema plan, indexation setup, initial content, meta tags, 6-month roadmap</td>
</tr>
<tr>
<td>🔄 <strong>Site Migration</strong></td>
<td align="center">7</td>
<td>Pre-migration crawl, URL redirect mapping, sitemap/canonical plan, meta tag updates, internal link updates, monitoring setup, post-migration audit</td>
</tr>
<tr>
<td>📈 <strong>Quarterly Review</strong></td>
<td align="center">6</td>
<td>Quarter-over-quarter analysis, ranking progress, ROI report, competitive landscape update, next-quarter roadmap, executive summary</td>
</tr>
</table>

---

## 🧠 How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                   YOU: "Here's my website" or "go"              │
└────────────────────────────┬────────────────────────────────────┘
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│  CLAUDE.md (The Brain)                                          │
│  Routes your request → right teams → right order                │
└────────────────────────────┬────────────────────────────────────┘
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│  INTELLIGENCE LAYER (runs first)                                │
│  Research Team: market context, algorithm updates, trends       │
│  Competitor Team: crawl competitor sites with Firecrawl          │
│  Keywords Team: discover and cluster keywords via Tavily         │
│  ────── all data saved to vault ──────                          │
└────────────────────────────┬────────────────────────────────────┘
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│  EXECUTION LAYER (runs second, reads intelligence from vault)   │
│  Technical: crawl your site, audit speed/schema/indexation      │
│  Content: audit existing content, find gaps                     │
│  Links: audit backlink profile                                  │
│  AEO: check AI search presence                                  │
│  ────── all findings saved to vault ──────                      │
└────────────────────────────┬────────────────────────────────────┘
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│  OUTPUT LAYER (runs last, reads everything from vault)           │
│  Audit Team: compiles ALL data → ONE master report              │
│  Every issue gets: what / where / how to fix / priority / impact│
│  Executive summary in business language (not jargon)            │
│  ────── quality gate checks everything ──────                   │
└────────────────────────────┬────────────────────────────────────┘
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│  DELIVERED                                                      │
│  Saved to: vault/ (memory) + output/ (deliverables)             │
│  Dashboard and ROI tracker updated automatically                │
└─────────────────────────────────────────────────────────────────┘
```

### 🏛️ The Three-Layer Hierarchy

| Layer | Teams | Role | Rule |
|-------|-------|------|------|
| **Intelligence** | Research, Competitor Analysis, Keywords | Gather data first | Never execute without intelligence |
| **Execution** | Technical, Content, Links, AEO, Local, E-commerce | Do the work | Every action backed by data |
| **Output** | Audit & Recommendations, Analytics & Reporting | Compile and deliver | Never deliver without quality gate |

**Strategy & Direction** operates across all layers — setting goals, prioritizing work, and adjusting strategy based on results.

---

## 🤖 The Auto-Pilot (`go` Command)

The `go` command runs the entire agency end-to-end. Here's what happens:

```
Step 1: Verify client profile exists (if not → quick onboard)
Step 2: Research Team → market intel, trends, algorithms
Step 3: Competitor Team → crawl competitor sites, extract strategies
Step 4: Keywords Team → discover, classify, cluster keywords
Step 5: Technical Team → crawl your site, full technical audit
Step 6: Content Gap Analysis → what's missing
Step 7: Backlink Audit → link profile health
Step 8: AEO Team → AI search optimization assessment
Step 9: Audit Team → compile ALL findings into one report
Step 10: Priority Matrix → rank every issue by Impact x Effort
Step 11: Deliver → executive summary, prioritized fixes, roadmap
```

All data flows through the vault. Each team saves its output, and the next team reads it as input. The Audit & Recommendations team at the end reads **everything** and produces the final report.

---

## 📦 Obsidian Setup

The `vault/` folder is an [Obsidian](https://obsidian.md)-compatible knowledge base — the agency's persistent memory.

### 🤔 Why Obsidian?

| Feature | Why It Matters |
|---------|---------------|
| **Visual knowledge graph** | See how clients, keywords, audits, and competitors connect |
| **Bidirectional links** | `[[Client Name]]` creates automatic cross-references |
| **Free and local** | Just markdown files — no cloud dependency, no vendor lock-in |
| **You can edit too** | Add notes, correct data — the agency picks it up next session |

### ⚙️ Setup

1. Download [Obsidian](https://obsidian.md) (free)
2. Click **"Open folder as vault"**
3. Select the `SEO Agency In a Box/` folder (the `.obsidian/` config is included)
4. Open **Graph View** to see the knowledge web

### 📂 Vault Structure

```
vault/
├── 00-Dashboard/        → Agency dashboard + ROI tracker
├── 01-Clients/          → Client profiles, site info, brand voice, goals
├── 02-Audits/           → Master audit reports, compiled findings
├── 03-Research/         → Keywords, market research, trends, algorithms, SERP data
├── 04-Content/          → Content strategy, briefs, drafts, published, meta-tags
├── 05-Links/            → Backlink profiles, prospects, outreach, placements
├── 06-Competitors/      → Competitor profiles, comparisons, monitoring
├── 07-Reports/          → Monthly reports, quarterly reviews, dashboards
├── 08-Strategy/         → Roadmaps, priority matrices, growth plans
├── 09-Local/            → GBP data, citations, local rankings, reviews
├── 10-Technical/        → Crawl data, Core Web Vitals, schema, redirects
└── 11-AEO/              → AI Overview data, entity maps, citation tracking
```

> **Don't have Obsidian?** No problem. The files are just markdown — browse them in VS Code, any text editor, or let the AI manage everything.

---

## 📁 Project Structure

```
SEO Agency In a Box/
│
├── CLAUDE.md                    # The brain — routes commands, enforces rules
├── README.md                    # You are here
├── .gitignore                   # Protects API keys and output/
│
├── agents/                      # 75 agent prompt files across 12 teams
│   ├── _base/                   #   Quality gate + SEO fundamentals
│   ├── technical/               #   8 agents — crawl, speed, schema, mobile
│   ├── keywords/                #   6 agents — discovery, intent, clusters
│   ├── content/                 #   10 agents — strategy, briefs, writing
│   ├── links/                   #   6 agents — backlinks, outreach, PR
│   ├── aeo/                     #   7 agents — AI Overviews, snippets, entities
│   ├── competitor/              #   6 agents — crawl, analyze, benchmark
│   ├── research/                #   6 agents — market, algorithms, trends
│   ├── local/                   #   5 agents — GBP, citations, reviews
│   ├── ecommerce/               #   5 agents — products, categories, feeds
│   ├── audit/                   #   5 agents — compile, recommend, report
│   ├── analytics/               #   6 agents — track, measure, report
│   └── strategy/                #   5 agents — roadmap, priorities, comms
│
├── instructions/                # How the agency operates
│   ├── hierarchy.md             #   Chain of command
│   ├── flow.md                  #   6-phase pipeline
│   ├── data-flow.md             #   Who reads/writes where (the wiring)
│   ├── quality-standards.md     #   What good output looks like
│   ├── tool-usage.md            #   Firecrawl, Tavily, Web Fetch guide
│   └── teams/                   #   12 team instruction files
│
├── workflows/                   # 11 multi-step workflow chains
├── templates/                   # 11 professional deliverable templates
├── quality/                     # Quality gate checklist
├── onboarding/                  # Client interview and profile builder
├── tools/                       # Firecrawl, Tavily, and credit-saving guides
│
├── vault/                       # Obsidian vault — persistent memory (12 sections)
└── output/                      # Final deliverables organized by client/date
```

---

## 📄 Templates

11 professional templates that agents use to produce polished deliverables:

| Template | What It Produces |
|----------|-----------------|
| `seo-audit-report.md` | Master SEO audit — technical, keywords, content, backlinks, AEO, competitors, priority matrix, roadmap |
| `technical-audit.md` | Technical audit — crawl summary, indexation, Core Web Vitals, schema, internal links, mobile, redirects |
| `keyword-research-report.md` | Keyword strategy — clusters, intent distribution, competitor comparison, gaps, SERP features |
| `content-brief.md` | Content brief — target keyword, SERP analysis, outline, SEO requirements, internal links, schema |
| `monthly-seo-report.md` | Monthly report — KPI scorecard, ranking movement, traffic analysis, content performance, next month plan |
| `backlink-audit-report.md` | Backlink audit — quality distribution, toxic links, anchor text, competitor comparison, disavow list |
| `competitor-analysis.md` | Competitor report — per-competitor profiles, side-by-side metrics, attack/defend/differentiate matrix |
| `local-seo-report.md` | Local SEO — GBP audit, local pack rankings, citation audit, review analysis, local competitor comparison |
| `seo-roadmap.md` | Roadmap — 3/6/12 month phases, monthly sprints, milestones, KPI targets, traffic projections |
| `priority-matrix.md` | Priority matrix — Impact x Effort scoring, Quick Wins / Strategic Investments / Deprioritize |
| `client-proposal.md` | Client proposal — assessment, strategy pillars, deliverables, pricing tiers, ROI estimate |

---

## ✅ Quality Gate

Every deliverable passes through `quality/qa-checklist.md` before delivery.

### 🚫 Non-Negotiable Rules

1. **No hallucinated data** — every metric comes from Firecrawl, Tavily, or Web Fetch. If it can't be verified, it says "data not available"
2. **No generic advice** — every recommendation is specific to the client's site, industry, CMS, and situation
3. **No outdated SEO** — no keyword density targets, no PBN links, no exact-match anchor manipulation
4. **Every fix is actionable** — includes what to change, where, how (with code if applicable), why, and expected impact

### 📊 Scoring

| Score | Meaning | Action |
|-------|---------|--------|
| 5/5 | Agency-grade, client-ready | Ship it |
| 4/5 | Professional, minor polish | Ship it |
| 3/5 | Meets standards (minimum) | Ship it |
| 2/5 | Below standard | Revise before delivery |
| 1/5 | Unacceptable | Start over |

---

## 💰 Credit-Saving Guide

Built-in efficiency for Claude Pro users:

| Rule | How It Saves Credits |
|------|---------------------|
| **Vault before tools** | Check if data exists before crawling or searching |
| **Map before crawl** | Firecrawl `map` is 95% cheaper than `crawl` — always map first |
| **Batch everything** | Write all meta tags in one pass, all briefs in one session |
| **Load agents on demand** | Only read the agent file for the current task |
| **Use templates** | Pre-structured output = fewer tokens |

### 📉 Estimated Cost per Workflow

| Workflow | Base Cost | Optimized Cost |
|----------|-----------|----------------|
| Full SEO Audit (12 steps) | Very High | High (reuse data) |
| Keyword Strategy (7 steps) | High | Medium (batch searches) |
| Content Sprint (8 steps) | High | Medium (batch writing) |
| Monthly Report (5 steps) | Medium | Low (vault compilation) |
| Competitor Teardown (6 steps) | High | Medium (cache data) |

---

## 🧪 Battle-Tested

This system was validated through 3 comprehensive simulations that traced every file, every vault path, and every cross-reference:

| Simulation | What Was Tested | Bugs Found | Bugs Fixed |
|------------|----------------|------------|------------|
| **Full Pipeline** | URL → onboard → research → audit → compile → deliver (entire auto-pilot) | 11 | 11 |
| **Content Sprint** | Calendar → SERP → briefs → articles → meta → FAQ → optimize (workflow chain) | 18 | 18 |
| **Cross-Team Data Flow** | All 12 teams reading/writing vault correctly (every cross-reference) | 13 | 13 |

**Final state:** 0 bad vault paths. 0 broken file references. 0 missing dependencies. 143 files verified.

---

## 📖 Step-by-Step Walkthrough

### Example: Full SEO Audit for a Coffee Brand

```
You: Here's my website: freshbrew.coffee — go
```

**What happens behind the scenes:**

1. **Quick Onboard** — Firecrawl scrapes the homepage, extracts business info, asks 5 questions, creates client profile
2. **Research Team** — Tavily researches the coffee/DTC market, checks for Google algorithm updates, scans AI search trends
3. **Competitor Team** — Firecrawl crawls the top 3 competitors, extracts their keywords, content, and link strategies
4. **Keywords Team** — Tavily discovers 200+ keywords, classifies intent, builds topical clusters, finds gaps
5. **Technical Team** — Firecrawl crawls freshbrew.coffee (every page), checks speed, schema, indexation, internal links, mobile
6. **AEO Team** — Checks if freshbrew appears in AI Overviews, Perplexity, featured snippets; maps entities
7. **Audit Team** — Reads ALL findings from vault, compiles into one master report with prioritized fixes
8. **Strategy Team** — Builds Impact x Effort priority matrix, creates 3-month roadmap

**What you receive:**
- Master SEO Audit Report (executive summary + full details)
- Priority Matrix (Quick Wins first)
- 3-month SEO Roadmap
- All data saved to vault for future sessions

---

## 🤝 Contributing

Contributions welcome! Areas that could use help:

- New agent specializations (e.g., video SEO, international SEO, programmatic SEO)
- Additional workflow chains
- Template improvements
- Better Obsidian integration (dataview queries, canvas views)
- Testing with real client sites

---

## 📜 License

MIT License. See [LICENSE](LICENSE) for details.

---

<div align="center">

**Built with [Claude Code](https://claude.ai/code) + [Firecrawl](https://firecrawl.dev) + [Tavily](https://tavily.com)**

*Star this repo if you find it useful.*

</div>
