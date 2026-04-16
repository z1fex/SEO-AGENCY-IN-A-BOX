# Monthly Reporting
> **Teams involved:** Analytics, Strategy | **Steps:** 5 | **Estimated time:** 15–30 minutes

Generate a comprehensive monthly SEO performance report. Pulls ranking, traffic, and conversion data together, calculates ROI, and produces a client-ready report with insights and next-month recommendations.

## What You'll Get
- Keyword ranking progress report (gains, losses, new rankings)
- Organic traffic analysis with trend identification
- Conversion and goal completion metrics
- SEO ROI calculation with dollar-value attribution
- Client-ready monthly report with executive summary and recommendations

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- At least one month of prior data in vault (previous audit, keyword baseline, or traffic baseline)
- Access to ranking data, traffic data, or client-provided analytics exports
- Previous month's report in `vault/07-Reports/` (if not the first report)

## Steps

### Step 1: Ranking Tracking (parallel track A)
**Agent:** `agents/analytics/ranking-tracker.md`
**Action:** Track keyword ranking changes for all target keywords. Using Tavily and Web Search, check current positions for priority keywords. Compare against the previous month's baseline in vault. Document: keywords that improved position, keywords that declined, new keyword rankings acquired, keywords lost from page 1, featured snippet wins/losses, and AI Overview appearances. Calculate the overall ranking trend direction and velocity.
**Save to:** `vault/07-Reports/[client]-[month]-rankings.md`

### Step 1b: Traffic Analysis (parallel track B)
**Agent:** `agents/analytics/traffic-analyst.md`
**Action:** Analyze organic traffic performance for the reporting period. Using available data (client-provided analytics, Web Fetch of public data, Tavily research), document: total organic sessions month-over-month, top landing pages by organic traffic, new pages gaining traction, pages with significant traffic drops, organic traffic by device (mobile vs. desktop), and geographic traffic distribution if relevant. Identify traffic trends and correlate with known SEO changes.
**Save to:** `vault/07-Reports/[client]-[month]-traffic.md`

### Step 1c: Conversion Analysis (parallel track C)
**Agent:** `agents/analytics/conversion-analyst.md`
**Action:** Analyze organic conversion performance. Document: organic conversion rate month-over-month, top converting landing pages, conversion rate by page type (blog, product, service, landing page), goal completions from organic traffic, and revenue attribution to organic channel if available. Identify high-traffic/low-conversion pages (optimization opportunities) and high-conversion pages to replicate.
**Save to:** `vault/07-Reports/[client]-[month]-conversions.md`

### Step 2: ROI Calculation
**Agent:** `agents/analytics/roi-calculator.md`
**Action:** Calculate the return on SEO investment for the reporting period. Inputs: SEO spend (agency fees, tools, content costs), organic revenue or lead value generated, ranking improvements translated to estimated traffic value (what the equivalent PPC cost would be), and link equity gained. Output a clear ROI percentage and dollar-value summary. Compare against previous months to show ROI trend. If direct revenue data is unavailable, estimate traffic value using average CPC for target keywords.
**Save to:** `vault/07-Reports/[client]-[month]-roi.md`

### Step 3: Monthly Report Compilation
**Agent:** `agents/analytics/monthly-report-writer.md`
**Action:** Compile all data from Steps 1–2 into a polished monthly SEO report. Structure: Executive Summary (3–5 key takeaways), Ranking Performance (table + trend chart description), Traffic Analysis (month-over-month comparison), Conversion Performance (goal tracking), ROI Summary, Work Completed This Month (reference vault entries for deliverables), Key Wins (celebrate progress), Areas of Concern (flag issues early), and Recommendations for Next Month (3–5 prioritized actions). Tone should be professional, data-driven, and action-oriented.
**Save to:** `vault/07-Reports/[client]-[month]-monthly-report.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on the monthly report
2. Verify all metrics are sourced from real data (no hallucinated numbers)
3. Save final report to `output/[client]/[date]/reports/monthly-report.md`
4. Archive supporting data files to `output/[client]/[date]/reports/supporting-data/`
5. Update vault dashboard (`vault/00-Dashboard/`)
6. Update ROI tracker — log monthly report with estimated agency value ($500–$1,000)
