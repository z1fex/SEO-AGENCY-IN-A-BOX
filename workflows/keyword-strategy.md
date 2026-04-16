# Keyword Strategy
> **Teams involved:** Keywords, Content | **Steps:** 7 | **Estimated time:** 20–40 minutes

Build a complete keyword strategy from discovery through clustering to content roadmap. This workflow produces the foundational keyword map that drives content, links, and technical optimization.

## What You'll Get
- Comprehensive keyword universe for the client's niche
- SERP landscape analysis for priority keywords
- Intent classification for every keyword (informational, navigational, commercial, transactional)
- Competitor keyword overlap and gap report
- Keyword clusters organized by topic with pillar/supporting page structure
- Content strategy roadmap mapping clusters to page types and priorities

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- Core business topics and seed keywords documented
- Competitor URLs listed in `vault/01-Clients/[client]/competitors.md`

## Steps

### Step 1: Keyword Discovery
**Agent:** `agents/keywords/keyword-discovery.md`
**Action:** Starting from the client's core topics and seed keywords, run broad keyword discovery using Tavily. Expand into long-tail variations, question-based queries, semantic relatives, and emerging terms. Capture estimated search volume, keyword difficulty, and current ranking position where available. Target a minimum of 200 keyword opportunities.
**Save to:** `vault/03-Research/[client]-keyword-universe.md`

### Step 2: SERP Analysis
**Agent:** `agents/keywords/serp-analyzer.md`
**Action:** For the top 20–30 priority keywords from Step 1, analyze the current SERP landscape. Document SERP features present (featured snippets, PAA, image packs, video carousels, AI Overviews, local packs, knowledge panels), identify ranking page types (blog posts, product pages, tools, listicles), and assess ranking difficulty based on competitor domain authority.
**Save to:** `vault/03-Research/[client]-serp-analysis.md`

### Step 3: Intent Classification
**Agent:** `agents/keywords/intent-classifier.md`
**Action:** Classify every keyword from the discovery set by search intent. Use SERP data from Step 2 to validate intent signals. Group keywords into: Informational (how-to, guides, definitions), Navigational (brand/product queries), Commercial Investigation (comparisons, reviews, best-of), Transactional (buy, pricing, signup). Flag keywords with mixed intent.
**Save to:** `vault/03-Research/[client]-intent-map.md`

### Step 4: Competitor Keyword Spy
**Agent:** `agents/keywords/competitor-keyword-spy.md`
**Action:** For each competitor in `vault/01-Clients/[client]/competitors.md`, identify their top-performing keywords. Use Firecrawl to scrape competitor content and Tavily to research their keyword footprint. Map which keywords each competitor ranks for, their estimated traffic share, and content type ranking for each keyword.
**Save to:** `vault/03-Research/[client]-competitor-keywords.md`

### Step 5: Keyword Gap Analysis
**Agent:** `agents/keywords/keyword-gap-analyst.md`
**Action:** Cross-reference the client's current keyword rankings against competitor keyword data from Step 4. Identify three gap categories: (1) Keywords competitors rank for but client does not, (2) Keywords where client ranks but underperforms competitors, (3) Keywords no competitor covers well (blue ocean opportunities). Score each gap by business value and effort to rank.
**Save to:** `vault/03-Research/[client]-keyword-gaps.md`

### Step 6: Keyword Clustering
**Agent:** `agents/keywords/cluster-builder.md`
**Action:** Group the full keyword set into topical clusters based on semantic similarity and intent alignment. Each cluster gets a designated pillar page and supporting pages. Define the hub-and-spoke structure: one pillar keyword per cluster, 5–15 supporting keywords, internal linking relationships between them. Output a visual cluster map.
**Save to:** `vault/03-Research/[client]-keyword-clusters.md`

### Step 7: Content Strategy Roadmap
**Agent:** `agents/content/content-strategist.md`
**Action:** Transform keyword clusters from Step 6 into an actionable content strategy. For each cluster, define: the target page type (pillar post, supporting article, product page, landing page, tool), content format (guide, listicle, comparison, tutorial, case study), priority level (P0–P3), and estimated publishing timeline. Produce a 90-day content roadmap with clear milestones.
**Save to:** `vault/04-Content/[client]-content-strategy.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on all deliverables
2. Verify all keyword data traces back to Tavily or Firecrawl results
3. Save complete keyword strategy package to `output/[client]/[date]/keywords/`
4. Update vault dashboard (`vault/00-Dashboard/`)
5. Update ROI tracker — log keyword strategy completion with estimated agency value ($1,500–$2,500)
