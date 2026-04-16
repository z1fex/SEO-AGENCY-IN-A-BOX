# Link Building Campaign
> **Teams involved:** Links, Content | **Steps:** 6 | **Estimated time:** 25–45 minutes

Plan and launch a strategic link building campaign. Starts with auditing the current backlink profile, analyzes competitor link strategies, identifies high-value prospects, and produces outreach-ready materials.

## What You'll Get
- Current backlink profile audit with toxic link identification
- Competitor backlink comparison showing link gaps
- Curated prospect list of high-authority link targets
- Broken link opportunities for easy wins
- Digital PR strategy with story angles and target publications
- Personalized outreach email templates for each prospect type
- Campaign tracking framework

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- Client site URL documented in `vault/01-Clients/[client]/site-info.md`
- Competitor URLs listed in `vault/01-Clients/[client]/competitors.md`
- At least one piece of linkable content exists (or plan to create during campaign)

## Steps

### Step 1: Backlink Profile Audit
**Agent:** `agents/links/backlink-auditor.md`
**Action:** Audit the client's existing backlink profile. Analyze: total referring domains and link count, domain authority distribution of linking sites, anchor text distribution (branded vs. keyword-rich vs. generic), link velocity trends (gaining/losing links over time), dofollow vs. nofollow ratio, toxic or spammy links requiring disavow consideration, highest-value existing links to protect. Establish the baseline for measuring campaign success.
**Save to:** `vault/05-Links/[client]-backlink-profile.md`

### Step 2: Competitor Backlink Analysis
**Agent:** `agents/links/competitor-backlink-analyzer.md`
**Action:** For each competitor in `vault/01-Clients/[client]/competitors.md`, analyze their backlink profiles using Firecrawl and Tavily. Identify: sites linking to competitors but not the client (link gap), competitor link building tactics (guest posts, resource pages, directories, digital PR, HARO), their most-linked content (what earns links in this niche), and anchor text strategies. Rank opportunities by link quality and acquisition feasibility.
**Save to:** `vault/05-Links/[client]-competitor-backlinks.md`

### Step 3: Link Prospect Discovery
**Agent:** `agents/links/link-prospector.md` + `agents/links/broken-link-finder.md`
**Action:** Build a curated prospect list from two sources. **Link Prospector:** Find resource pages, roundup posts, industry directories, bloggers, journalists, and publications in the client's niche. Evaluate each prospect for: domain authority, relevance to client's niche, likelihood of responding, and link value. **Broken Link Finder:** Scan competitor backlink profiles and niche resource pages for broken outbound links. These represent easy-win replacement link opportunities. Compile a master prospect list of 30–50 targets, categorized by type and priority.
**Save to:** `vault/05-Links/[client]-link-prospects.md`

### Step 4: Digital PR Strategy
**Agent:** `agents/links/digital-pr-strategist.md`
**Action:** Develop a digital PR strategy to earn high-authority editorial links. Create 3–5 PR story angles based on the client's expertise, data, or unique perspective. Identify target publications and journalists for each angle. Recommend linkable asset types to create (original research, data studies, interactive tools, expert roundups, infographics). Build a PR calendar with pitch timing aligned to industry events, seasonal trends, or news cycles.
**Save to:** `vault/05-Links/[client]-digital-pr-strategy.md`

### Step 5: Outreach Email Writing
**Agent:** `agents/links/outreach-writer.md`
**Action:** Write personalized outreach email templates for each prospect type identified in Steps 3 and 4. Create distinct templates for: resource page link requests, broken link replacement pitches, guest post proposals, digital PR pitches to journalists, and expert quote offers. Each template includes: a compelling subject line (personalized, not spammy), a concise value proposition, a specific ask, and a natural follow-up sequence (initial + 2 follow-ups). Personalization tokens marked with `[brackets]` for easy customization per prospect.
**Save to:** `vault/05-Links/[client]-outreach-templates.md`

### Step 6: Campaign Summary & Tracking Setup
**Agent:** `agents/audit/report-builder.md`
**Action:** Compile all link building campaign materials into a unified campaign brief. Include: current baseline metrics (from Step 1), campaign goals (target number of links, target DA range, timeline), prioritized prospect list with outreach status columns, outreach templates mapped to prospect types, digital PR calendar, and KPIs to track (links acquired, DA of linking domains, referral traffic, ranking impact). Create a tracking table for ongoing campaign management.
**Save to:** `vault/05-Links/[client]-link-campaign-plan.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on all deliverables
2. Verify all prospect data is real (no hallucinated domains or contacts)
3. Save campaign package to `output/[client]/[date]/links/`
4. Update vault dashboard (`vault/00-Dashboard/`)
5. Update ROI tracker — log link building campaign with estimated agency value ($2,000–$3,500)
