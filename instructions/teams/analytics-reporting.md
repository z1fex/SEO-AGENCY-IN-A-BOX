# Analytics & Reporting Team

> Measure, track, report, and prove ROI by building performance dashboards, tracking keyword rankings over time, analyzing organic traffic patterns, mapping traffic to conversions, and delivering professional monthly and quarterly reports.

## Team Overview

The Analytics & Reporting Team closes the feedback loop. Every other team in the agency does work — research, auditing, optimizing, building links, creating content. This team answers the question: is it working? Without measurement, the agency operates on faith. With measurement, the agency operates on evidence. This team tracks keyword rankings over time, analyzes organic traffic patterns and trends, maps organic traffic to business conversions, calculates the ROI of SEO investment, and packages all of this into professional reports that clients can use to make decisions and justify continued investment.

This team sits in the **Output Layer** of the agency hierarchy. It runs during Phase 6 (Report) for monthly and quarterly reporting cycles, and it also provides baseline metrics during Phase 3 (Audit) that are used as benchmarks for future comparison. The team does not optimize or fix anything — it measures and reports. Its output feeds back into the Strategy & Direction Team, which uses performance data to adjust priorities, double down on what works, and pivot away from what does not.

The team follows a data-first pipeline. Three agents run in parallel to collect different data streams: the Ranking Tracker checks current keyword positions, the Traffic Analyst processes organic traffic data, and the Conversion Analyst maps traffic to business outcomes. The Performance Dashboard Builder then synthesizes all three data streams into a visual dashboard. The ROI Calculator translates performance metrics into financial impact. The Monthly Report Writer packages everything into a polished client report. This sequence ensures that the report is built on complete data, not partial snapshots.

## Agents

| Agent | File | Role |
|-------|------|------|
| Ranking Tracker | `agents/analytics/ranking-tracker.md` | Checks current keyword rankings for the client's target keywords using Tavily SERP checks, compares against previous period rankings, and identifies ranking movements (gains, losses, new entries, exits) |
| Traffic Analyst | `agents/analytics/traffic-analyst.md` | Analyzes organic traffic data (from client-provided analytics or estimated from ranking data), identifies traffic trends, seasonal patterns, page-level performance, and traffic distribution across content types |
| Conversion Analyst | `agents/analytics/conversion-analyst.md` | Maps organic traffic to business conversions — lead submissions, purchases, signups, phone calls — to connect SEO work to revenue outcomes. Works with whatever conversion data the client provides |
| Performance Dashboard Builder | `agents/analytics/dashboard-builder.md` | Creates a structured performance dashboard synthesizing rankings, traffic, and conversion data into a single view with period-over-period comparisons, trend indicators, and key metric highlights |
| ROI Calculator | `agents/analytics/roi-calculator.md` | Calculates the return on SEO investment — compares the cost of the agency engagement against the estimated value of organic traffic, conversions, and brand visibility gains |
| Monthly Report Writer | `agents/analytics/monthly-report-writer.md` | Writes the professional client-facing monthly or quarterly report — narrative analysis of performance, key wins, areas of concern, next period recommendations, and strategic adjustments |

## When to Run This Team

- **Monthly reporting** — Standard monthly cadence: run the full team at the end of each month to produce the monthly SEO performance report
- **Quarterly review** — At the end of each quarter, run with expanded scope for quarter-over-quarter analysis and strategic review
- **Initial audit baseline** — During the first engagement, run the Ranking Tracker and Traffic Analyst to establish baseline metrics before optimization work begins
- **Post-implementation check** — After a round of fixes or optimizations, run the Ranking Tracker to check for early ranking movements
- **Client meeting preparation** — Before any client strategy meeting, run the dashboard to have current data ready
- **ROI justification** — When the client or their management needs ROI data to justify SEO investment
- **Strategy adjustment** — When the Strategy team needs current performance data to adjust the roadmap
- **Traffic anomaly investigation** — When organic traffic shows an unexpected spike or drop, run the Traffic Analyst to investigate
- **Annual review** — At year-end, produce a comprehensive annual performance summary

## Execution Order

```
Step 1a: Ranking Tracker (parallel)
   │
   │  Uses Tavily search to check current SERP positions for all of
   │  the client's target keywords (from vault/03-Research/). Compares
   │  current positions against previous period data stored in vault.
   │  Records: keyword, current position, previous position, change
   │  (up/down/new/lost), URL ranking, and SERP features present.
   │  Saves to vault/07-Reports/[client]/ranking-data/[date].md
   │
Step 1b: Traffic Analyst (parallel)
   │
   │  Processes organic traffic data. If client provides analytics data
   │  (CSV export, screenshots, or access), analyzes actual traffic.
   │  If not, estimates traffic impact from ranking data using CTR
   │  models. Identifies: total organic traffic trend, top-performing
   │  pages, traffic by content type, new vs. returning visitors,
   │  geographic distribution, and seasonal patterns.
   │  Saves to vault/07-Reports/[client]/traffic-data/[date].md
   │
Step 1c: Conversion Analyst (parallel)
   │
   │  Maps organic traffic to conversions using client-provided data.
   │  If conversion data is available: calculates conversion rate by
   │  page, by keyword cluster, and by content type. If not available:
   │  provides conversion tracking setup recommendations and estimates
   │  based on industry benchmarks. Connects SEO work to business
   │  outcomes.
   │  Saves to vault/07-Reports/[client]/conversion-data/[date].md
   │
   ▼
Step 2: Performance Dashboard Builder
   │
   │  Takes ranking, traffic, and conversion data from Steps 1a-1c
   │  and synthesizes into a structured performance dashboard.
   │  Includes: key metric summary (with period-over-period change),
   │  ranking movement chart, traffic trend visualization (text-based),
   │  top gaining keywords, top losing keywords, top pages by traffic,
   │  conversion funnel metrics, and competitive position snapshot.
   │  Saves to vault/07-Reports/[client]/dashboard/[date].md
   │
   ▼
Step 3: ROI Calculator
   │
   │  Calculates SEO ROI using available data:
   │  - Estimated value of organic traffic (traffic x industry CPC)
   │  - Value of conversions attributed to organic search
   │  - Comparison: equivalent paid search cost vs. SEO investment
   │  - Month-over-month ROI trend
   │  - Cumulative ROI since engagement start
   │  If financial data is limited, provides a range estimate with
   │  clear assumptions labeled.
   │  Saves to vault/07-Reports/[client]/roi/[date].md
   │
   ▼
Step 4: Monthly Report Writer
   │
   │  Takes the dashboard, ROI data, and all supporting data to write
   │  the professional client report. Structure:
   │  1. Executive Summary (key wins, key concerns, top metrics)
   │  2. Performance Dashboard (from Step 2)
   │  3. Ranking Performance (detailed keyword movement analysis)
   │  4. Traffic Analysis (trends, patterns, page-level insights)
   │  5. Conversion Analysis (if data available)
   │  6. ROI Summary
   │  7. Work Completed This Period (link to audit/execution work)
   │  8. Next Period Priorities (informed by data trends)
   │  9. Strategic Recommendations
   │  
   │  Writes in business language. Explains the "so what" behind
   │  every data point. Connects metrics to business outcomes.
   │  Saves to output/[client]/[date]/reports/monthly-report.md
```

**Data flow:** Three parallel data collection agents (rankings, traffic, conversions) feed into the Dashboard Builder, which creates the unified performance view. The ROI Calculator adds financial context. The Monthly Report Writer synthesizes everything into a narrative report with analysis, insights, and recommendations. Each stage adds a layer of interpretation — raw data becomes metrics becomes insights becomes recommendations.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Tavily | `search` | SERP position checks for target keywords — the primary method for tracking keyword rankings |
| Tavily | `search` (advanced depth) | Deep SERP analysis for high-priority keywords — checks featured snippets, AI Overviews, and other features alongside ranking position |
| Web Fetch | Page validation | Check specific ranking URLs, verify landing page content, and validate reported metrics |
| Vault | Read (all folders) | Read historical ranking data, previous reports, audit findings, and keyword targets |
| Web Search | General research | Check for algorithm updates that may explain traffic changes, verify industry benchmarks |
| Client data | CSV/provided | Process client-provided analytics, Search Console, and conversion data |

### Tool Usage Protocol

1. **Use Tavily for all ranking checks** — search for each target keyword and record the client's position in the results. Use `search_depth: "advanced"` for priority keywords
2. **Compare against historical data** — always read previous period's ranking data from vault before running new checks, so you can calculate movement
3. **Save all ranking data chronologically** — use `[YYYY-MM-DD].md` date-stamped files so ranking history accumulates over time
4. **Label estimates clearly** — when working without client analytics data, all traffic and conversion numbers are estimates. Label them explicitly: "Estimated based on ranking position and industry CTR curves" — never present estimates as actual data
5. **Check for algorithm updates** — when traffic data shows anomalies, use Web Search to check if a Google algorithm update coincided with the change

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Target keyword list | `vault/03-Research/[client]/keyword-clusters.md` | Yes — must have keywords to track |
| Previous period ranking data | `vault/07-Reports/[client]/ranking-data/` | Recommended — enables period-over-period comparison (not available on first run) |
| Client analytics data | Client-provided (Google Analytics CSV, screenshots) | Recommended — enables actual traffic analysis |
| Client conversion data | Client-provided | Recommended — enables conversion and ROI analysis |
| Audit findings | `vault/02-Audits/[client]/` | Recommended — provides context for what work was done |
| Competitor SERP data | `vault/06-Competitors/[client]/serp-positions.md` | Recommended — enables competitive ranking comparison |
| Previous reports | `vault/07-Reports/[client]/` | Recommended — enables trend analysis across reporting periods |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Ranking Data | `vault/07-Reports/[client]/ranking-data/[date].md` | Current keyword positions with period-over-period changes — accumulated over time for trend analysis |
| Traffic Data | `vault/07-Reports/[client]/traffic-data/[date].md` | Organic traffic analysis with trends, page-level performance, and distribution patterns |
| Conversion Data | `vault/07-Reports/[client]/conversion-data/[date].md` | Traffic-to-conversion mapping with rates by page, keyword cluster, and content type |
| Performance Dashboard | `vault/07-Reports/[client]/dashboard/[date].md` | Synthesized dashboard with all key metrics, trends, and period-over-period comparisons |
| ROI Analysis | `vault/07-Reports/[client]/roi/[date].md` | SEO ROI calculation with traffic value, conversion value, and investment comparison |
| Monthly/Quarterly Report | `output/[client]/[date]/reports/monthly-report.md` | Professional client-facing report with narrative analysis, insights, and recommendations |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "analytics-reporting"
date: YYYY-MM-DD
type: report
status: complete
reporting-period: "YYYY-MM to YYYY-MM"
keywords-tracked: 0
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - **Keyword Research Team** (required) — must have a target keyword list to track rankings
  - Client profile (must exist in vault)
  - Previous period data (recommended — required for period-over-period comparison, but first-period reporting can establish baselines)
  - **All execution teams** (recommended) — understanding what work was done helps explain performance changes
  - Client-provided analytics and conversion data (recommended — significantly improves report depth)

- **Feeds into:**
  - **Client** — the monthly/quarterly report is a client deliverable
  - **Strategy & Direction Team** — performance data drives strategy adjustments, roadmap updates, and priority re-calibration
  - **Research Team** — ranking volatility may trigger algorithm update investigation
  - **All execution teams** (on re-engagement) — performance data reveals which areas need more work and which are performing well
  - **Audit & Recommendations Team** — baseline metrics from the first period become the benchmarks for the audit report

## Quality Checks

### Analytics & Reporting-Specific Quality Criteria

1. **Data accuracy over completeness** — It is better to report fewer verified metrics than to fill the report with estimates presented as facts. Every number in the report must be either: (a) sourced from a tool (Tavily SERP check, client analytics), or (b) clearly labeled as an estimate with the estimation method explained.

2. **Period-over-period comparison** — Every metric must show the current period value AND the previous period value (or baseline). A ranking position means nothing without context. "Position 7" is data. "Position 7 (up from Position 14 last month, +7 positions)" is insight.

3. **Explanation, not just numbers** — The Monthly Report Writer must explain what the numbers mean. "Organic traffic increased 12% month-over-month" is reporting. "Organic traffic increased 12% month-over-month, driven primarily by the 3 new blog posts published in Week 2 — the cold brew guide alone accounts for 40% of the traffic gain, now ranking Position 4 for 'how to make cold brew'" is analysis.

4. **Estimates clearly labeled** — When working without client analytics data, all traffic numbers are estimates based on ranking positions and CTR models. These must be explicitly labeled: "Estimated monthly organic traffic: ~2,400 visits (based on current rankings and industry-average CTR curves — actual traffic may vary)." Never present CTR-modeled estimates as measured traffic.

5. **ROI methodology transparent** — The ROI Calculator must show its math. What CPC values were used? What conversion rates were assumed? What was the total estimated value? What was the engagement cost? Clients and their management will scrutinize ROI claims — the methodology must be defensible.

6. **Actionable recommendations** — Every report must end with specific next-period recommendations informed by the data. If rankings are flat despite content improvements, recommend a link building focus. If traffic is up but conversions are down, recommend CRO work. The recommendations must connect to the data presented in the report.

7. **Professional formatting** — Reports must be polished enough for client presentation. Consistent heading hierarchy, properly formatted tables, clear metric highlights, and no raw data dumps. The report represents the agency's professionalism.

8. **Historical data preservation** — All ranking, traffic, and conversion data must be saved chronologically in the vault using date-stamped files. This data accumulates over months and becomes increasingly valuable for trend analysis. Never overwrite previous period data.

9. **Competitive context** — When available, ranking data should include competitor positions for the same keywords. A client ranking Position 5 in a SERP where their main competitor holds Position 1 tells a different story than Position 5 in a SERP where no direct competitor ranks in the top 10.

10. **Minimum quality score: 4/5. Target: 5/5.** (Higher bar — this is a client-facing deliverable.)
