# Quarterly Review
> **Teams involved:** Analytics, Competitor, Strategy | **Steps:** 6 | **Estimated time:** 30–50 minutes

Comprehensive quarterly SEO performance review and strategic planning session. Analyzes 3 months of progress, benchmarks against competitors, recalculates ROI, and produces the next quarter's strategic roadmap. Designed for client stakeholder presentations.

## What You'll Get
- Quarter-over-quarter traffic and ranking analysis
- Keyword ranking progress report across the full quarter
- Quarterly ROI calculation with cumulative value tracking
- Updated competitive landscape assessment
- Next quarter's SEO roadmap with prioritized initiatives
- Executive summary presentation for stakeholders

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- At least one quarter of SEO work completed and tracked in vault
- Monthly reports from the quarter available in `vault/07-Reports/`
- Competitor data exists in `vault/06-Competitors/` (will be refreshed in this workflow)
- Current quarter's goals/OKRs documented in `vault/08-Strategy/`

## Steps

### Step 1: Quarter-over-Quarter Traffic Analysis
**Agent:** `agents/analytics/traffic-analyst.md`
**Action:** Analyze organic traffic performance across the full quarter (3 months). Compare against the previous quarter and year-over-year if data exists. Document: total organic sessions QoQ with growth percentage, monthly trend within the quarter (accelerating, decelerating, flat), top 20 landing pages by organic traffic and their QoQ change, new pages published this quarter and their traffic contribution, pages with significant traffic decline (investigate causes), organic traffic split by device, geographic, and channel, and branded vs. non-branded organic traffic split. Identify the key drivers behind traffic changes: algorithm updates, content published, technical fixes implemented, seasonal factors, or competitive shifts.
**Save to:** `vault/07-Reports/[client]-Q[quarter]-traffic-analysis.md`

### Step 2: Quarterly Ranking Progress
**Agent:** `agents/analytics/ranking-tracker.md`
**Action:** Compile ranking performance across the full quarter. Using Tavily and Web Search, check current positions for all target keywords and compare against the quarter-start baseline. Deliver: total keywords tracked and ranking distribution (page 1, page 2, page 3+), keywords that entered page 1 this quarter, keywords that improved position (with magnitude of change), keywords that declined (with potential causes), new keyword rankings acquired from content published this quarter, featured snippet and SERP feature wins/losses, and AI Overview appearances gained or lost. Calculate the overall keyword visibility trend and its correlation to traffic changes.
**Save to:** `vault/07-Reports/[client]-Q[quarter]-ranking-progress.md`

### Step 3: Quarterly ROI Calculation
**Agent:** `agents/analytics/roi-calculator.md`
**Action:** Calculate comprehensive ROI for the quarter. Inputs: total SEO investment this quarter (agency fees, tool costs, content costs, link building spend), organic revenue or lead value generated, estimated organic traffic value (sum of ranking keyword CPCs multiplied by estimated click-through rates), link equity value gained (new referring domains multiplied by industry average link cost), and content asset value created (word count multiplied by industry content rate). Compare: quarter ROI vs. previous quarter, cumulative ROI since engagement start, and progress toward annual ROI targets. Present in both percentage terms and absolute dollar values.
**Save to:** `vault/07-Reports/[client]-Q[quarter]-roi.md`

### Step 4: Updated Competitive Landscape
**Agent:** `agents/strategy/competitive-strategy-analyst.md`
**Action:** Refresh the competitive landscape assessment using current data. For each tracked competitor, research: significant changes in their SEO strategy this quarter (new content, site changes, link building activity), ranking position changes for shared keywords, new competitors that have emerged in the SERP, and competitors that have weakened or exited key positions. Identify: competitive threats that have intensified, new opportunities created by competitor weaknesses, and market shifts affecting the competitive dynamic (algorithm updates, industry changes, new search features). Compare the client's progress against the competitive field.
**Save to:** `vault/06-Competitors/[client]-Q[quarter]-competitive-landscape.md`

### Step 5: Next Quarter Roadmap
**Agent:** `agents/strategy/roadmap-planner.md`
**Action:** Build the strategic roadmap for the next quarter based on all Q-review data. Structure into: **Goals** (3–5 measurable quarterly objectives tied to business outcomes), **Technical SEO Priorities** (fixes and improvements from audit findings still open), **Content Plan** (topics, formats, volume targets based on keyword gaps and content performance), **Link Building Targets** (referring domain goals, target publications, campaign types), **AEO Initiatives** (AI search optimization actions for next quarter), and **Competitive Countermoves** (specific responses to competitor activity identified in Step 4). Each initiative includes: owner, timeline (month 1/2/3), success metric, and estimated impact. The roadmap must be achievable within the quarter's resource constraints.
**Save to:** `vault/08-Strategy/[client]-Q[next-quarter]-roadmap.md`

### Step 6: Executive Summary & Stakeholder Communication
**Agent:** `agents/strategy/client-communication-manager.md`
**Action:** Write the executive quarterly review document for client stakeholders. This is a presentation-ready deliverable, not an internal report. Structure: **Quarter Highlights** (3–5 headline wins with numbers), **Performance Dashboard** (key metrics at a glance: traffic, rankings, conversions, ROI — QoQ and YoY), **What We Did** (summary of work completed this quarter with outcomes), **What Worked** (strategies that drove results, with data), **What We Learned** (insights that inform future strategy), **Challenges & How We're Addressing Them** (honest assessment of underperformance with action plan), **Next Quarter Preview** (roadmap highlights and expected outcomes), and **Investment Recommendation** (maintain, increase, or reallocate budget with justification). Tone: confident, data-driven, strategic, and honest about both wins and challenges.
**Save to:** `vault/07-Reports/[client]-Q[quarter]-executive-summary.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on all quarterly review deliverables
2. Verify all metrics trace to real data sources (no hallucinated percentages or growth figures)
3. Save executive summary to `output/[client]/[date]/reports/quarterly-review.md`
4. Save roadmap to `output/[client]/[date]/strategy/Q[next-quarter]-roadmap.md`
5. Save supporting data to `output/[client]/[date]/reports/quarterly-data/`
6. Update vault dashboard (`vault/00-Dashboard/`)
7. Update ROI tracker — log quarterly review with estimated agency value ($1,000–$2,000)
