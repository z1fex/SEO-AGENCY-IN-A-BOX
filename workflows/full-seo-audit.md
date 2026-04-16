# Full SEO Audit
> **Teams involved:** Technical, Keywords, Content, Links, AEO, Competitor, Audit & Recommendations | **Steps:** 12 | **Estimated time:** 45–90 minutes

The flagship workflow. Every SEO team contributes data; the Audit & Recommendations team compiles everything into a single prioritized report with actionable fixes.

## What You'll Get
- Complete technical SEO audit (crawl errors, indexation, Core Web Vitals, schema, internal links, mobile)
- Keyword gap analysis with intent mapping
- Content gap assessment against top competitors
- Backlink profile audit with toxic link identification
- AEO readiness assessment (AI Overview, Perplexity, ChatGPT search visibility)
- Prioritized recommendation matrix (quick wins → long-term projects)
- Executive summary for stakeholder presentation

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- Client site URL is documented in `vault/01-Clients/[client]/site-info.md`
- At least one competitor URL identified in `vault/01-Clients/[client]/competitors.md`

## Steps

### Step 1: Site Crawl
**Agent:** `agents/technical/site-crawler.md`
**Action:** Crawl the client's full site using Firecrawl. Capture URL inventory, status codes, redirect chains, broken links, page depth, orphan pages, and crawl budget issues. Save a structured URL map.
**Save to:** `vault/10-Technical/[client]-crawl-data.md`

### Step 2: Indexation Audit
**Agent:** `agents/technical/indexation-manager.md`
**Action:** Using crawl data from Step 1, audit indexation health. Check robots.txt directives, XML sitemap completeness and accuracy, canonical tag consistency, noindex/nofollow usage, and index bloat. Identify pages that should be indexed but aren't, and pages indexed that shouldn't be.
**Save to:** `vault/10-Technical/[client]-indexation-audit.md`

### Step 3: Core Web Vitals Analysis
**Agent:** `agents/technical/core-web-vitals-analyst.md`
**Action:** Analyze Core Web Vitals performance (LCP, INP, CLS) for key landing pages. Identify pages failing thresholds, diagnose root causes (render-blocking resources, layout shifts, slow server response), and quantify the performance gap.
**Save to:** `vault/10-Technical/[client]-cwv-audit.md`

### Step 4: Schema & Structured Data Review
**Agent:** `agents/technical/schema-specialist.md`
**Action:** Audit existing structured data across the site. Validate schema markup against Google's requirements, identify missing schema opportunities (FAQ, HowTo, Product, Organization, BreadcrumbList, Article), and flag errors or warnings from Rich Results testing.
**Save to:** `vault/10-Technical/[client]-schema-audit.md`

### Step 5: Internal Link Architecture Analysis
**Agent:** `agents/technical/internal-linking-architect.md`
**Action:** Map the internal link graph using crawl data from Step 1. Identify PageRank distribution issues, orphan pages, thin hub pages, over-linked pages, and link equity waste. Recommend an improved internal linking strategy aligned with keyword clusters.
**Save to:** `vault/10-Technical/[client]-internal-links-audit.md`

### Step 6: Mobile SEO Audit
**Agent:** `agents/technical/mobile-seo-auditor.md`
**Action:** Evaluate mobile-first indexing readiness. Check mobile rendering, viewport configuration, touch target sizing, font legibility, content parity between mobile and desktop, and intrusive interstitial usage. Identify mobile-specific UX issues impacting rankings.
**Save to:** `vault/10-Technical/[client]-mobile-audit.md`

### Step 7: Keyword Discovery & Gap Analysis
**Agent:** `agents/keywords/keyword-discovery.md` + `agents/keywords/keyword-gap-analyst.md`
**Action:** Run keyword discovery for the client's core topics using Tavily. Then run gap analysis comparing the client's keyword footprint against top competitors from `vault/01-Clients/[client]/competitors.md`. Classify all keywords by search intent (informational, navigational, commercial, transactional). Identify high-opportunity keywords the client is missing.
**Save to:** `vault/03-Research/[client]-keyword-landscape.md`

### Step 8: Content Gap Assessment
**Agent:** `agents/content/content-gap-analyst.md`
**Action:** Using keyword data from Step 7 and competitor analysis, identify content gaps. Map existing client content to keyword clusters, find topics with no coverage, identify thin content needing expansion, and flag content cannibalization issues. Prioritize gaps by search volume and business value.
**Save to:** `vault/04-Content/[client]-content-gaps.md`

### Step 9: Backlink Profile Audit
**Agent:** `agents/links/backlink-auditor.md`
**Action:** Audit the client's backlink profile. Analyze referring domain quality, anchor text distribution, link velocity trends, toxic/spammy links requiring disavow, and lost high-value links. Compare backlink authority metrics against competitors.
**Save to:** `vault/05-Links/[client]-backlink-audit.md`

### Step 10: AEO Readiness Assessment
**Agent:** `agents/aeo/ai-overview-optimizer.md`
**Action:** Assess the client's visibility in AI-powered search experiences. Check presence in Google AI Overviews for target keywords, evaluate content structure for LLM citation likelihood, audit entity clarity and knowledge panel status, and identify AEO opportunities where competitors are being cited instead.
**Save to:** `vault/11-AEO/[client]-aeo-assessment.md`

### Step 11: Data Compilation
**Agent:** `agents/audit/data-compiler.md`
**Action:** Compile all findings from Steps 1–10 into a unified dataset. Normalize issue severity ratings, deduplicate overlapping findings, categorize all issues (technical, content, links, AEO), and calculate aggregate health scores per category.
**Save to:** `vault/02-Audits/[client]-compiled-data.md`

### Step 12: Report Building & Executive Summary
**Agent:** `agents/audit/report-builder.md` + `agents/audit/executive-summary-writer.md`
**Action:** Build the final audit report from compiled data. Structure findings into sections with severity ratings (Critical / High / Medium / Low). Generate a prioritized fix matrix with estimated effort and impact for each recommendation. Write an executive summary highlighting top 5 critical issues, 5 biggest opportunities, and a 90-day action plan.
**Save to:** `vault/02-Audits/[client]-full-seo-audit.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on the full audit report
2. Verify all data points trace back to tool results (Firecrawl, Tavily, Web Fetch)
3. Save final report to `output/[client]/[date]/audit/full-seo-audit.md`
4. Save executive summary to `output/[client]/[date]/audit/executive-summary.md`
5. Update vault dashboard (`vault/00-Dashboard/`)
6. Update ROI tracker — log full audit completion with estimated agency value ($3,000–$5,000)
