---
template: monthly-seo-report
version: 1.0
type: report
description: Monthly SEO performance report with KPIs, rankings, traffic, content, and link building progress
agents: seo-analyst, reporting-agent
---

# Monthly SEO Report

| Field | Details |
|-------|---------|
| **Client** | {{client_name}} |
| **Website** | {{website_url}} |
| **Reporting Period** | {{reporting_month}} {{reporting_year}} |
| **Prepared By** | {{prepared_by}} |
| **Report Date** | {{report_date}} |

---

## Executive Summary

- {{highlight_1}}
- {{highlight_2}}
- {{highlight_3}}
- {{highlight_4}}
- {{highlight_5}}

**Overall Assessment:** {{overall_assessment}}

---

## KPI Scorecard

| Metric | Last Month | This Month | Change | Target | On Track |
|--------|-----------|-----------|--------|--------|----------|
| Organic Sessions | {{sessions_last}} | {{sessions_current}} | {{sessions_change}} | {{sessions_target}} | {{sessions_on_track}} |
| Organic Revenue/Leads | {{revenue_last}} | {{revenue_current}} | {{revenue_change}} | {{revenue_target}} | {{revenue_on_track}} |
| Keywords in Top 10 | {{top10_last}} | {{top10_current}} | {{top10_change}} | {{top10_target}} | {{top10_on_track}} |
| Keywords in Top 3 | {{top3_last}} | {{top3_current}} | {{top3_change}} | {{top3_target}} | {{top3_on_track}} |
| Avg. Position | {{position_last}} | {{position_current}} | {{position_change}} | {{position_target}} | {{position_on_track}} |
| Referring Domains | {{rd_last}} | {{rd_current}} | {{rd_change}} | {{rd_target}} | {{rd_on_track}} |
| Domain Authority | {{da_last}} | {{da_current}} | {{da_change}} | {{da_target}} | {{da_on_track}} |
| Organic CTR | {{ctr_last}} | {{ctr_current}} | {{ctr_change}} | {{ctr_target}} | {{ctr_on_track}} |
| Bounce Rate (Organic) | {{bounce_last}} | {{bounce_current}} | {{bounce_change}} | {{bounce_target}} | {{bounce_on_track}} |
| Pages Indexed | {{indexed_last}} | {{indexed_current}} | {{indexed_change}} | {{indexed_target}} | {{indexed_on_track}} |

---

## Ranking Progress

### Biggest Movers (Up)

| Keyword | Volume | Previous Rank | Current Rank | Change | Target Page |
|---------|--------|--------------|-------------|--------|------------|
{{ranking_up_rows}}

### Biggest Movers (Down)

| Keyword | Volume | Previous Rank | Current Rank | Change | Target Page | Likely Cause |
|---------|--------|--------------|-------------|--------|------------|-------------|
{{ranking_down_rows}}

### Priority Keyword Tracker

| Keyword | Volume | Start Rank | Last Month | This Month | Trend | Target |
|---------|--------|-----------|-----------|-----------|-------|--------|
{{priority_keyword_rows}}

---

## Traffic Analysis

### Organic Sessions

| Metric | Value |
|--------|-------|
| Total Organic Sessions | {{total_organic_sessions}} |
| MoM Change | {{mom_session_change}} |
| YoY Change | {{yoy_session_change}} |
| New Users (Organic) | {{new_users}} |
| Returning Users (Organic) | {{returning_users}} |

### Top Pages by Organic Traffic

| # | Page | Sessions | MoM Change | Top Keyword |
|---|------|----------|-----------|------------|
{{top_pages_rows}}

### Device Split

| Device | Sessions | % of Total | MoM Change |
|--------|----------|-----------|-----------|
| Desktop | {{desktop_sessions}} | {{desktop_pct}} | {{desktop_change}} |
| Mobile | {{mobile_sessions}} | {{mobile_pct}} | {{mobile_change}} |
| Tablet | {{tablet_sessions}} | {{tablet_pct}} | {{tablet_change}} |

---

## Content Performance

### Published This Month

| # | Title | Target Keyword | Publish Date | Sessions | Avg. Position |
|---|-------|---------------|-------------|----------|--------------|
{{published_content_rows}}

### Top Performing Content (All Time)

| # | Page | Sessions This Month | MoM Change | Conversions |
|---|------|--------------------|-----------|-----------  |
{{top_content_rows}}

---

## Link Building Progress

| Metric | Value |
|--------|-------|
| New Backlinks Acquired | {{new_backlinks}} |
| New Referring Domains | {{new_referring_domains}} |
| Links Lost | {{links_lost}} |
| Net Link Growth | {{net_link_growth}} |

### Links Acquired This Month

| # | Referring Domain | DA | Link Type | Anchor Text | Target Page |
|---|-----------------|-----|----------|-------------|------------|
{{acquired_links_rows}}

### Profile Health

| Metric | Last Month | This Month |
|--------|-----------|-----------|
| Domain Authority | {{da_last_month}} | {{da_this_month}} |
| Dofollow Ratio | {{dofollow_last}} | {{dofollow_current}} |
| Toxic Links | {{toxic_last}} | {{toxic_current}} |

---

## Work Completed This Month

### Technical SEO
{{technical_work_completed}}

### Content
{{content_work_completed}}

### Link Building
{{linkbuilding_work_completed}}

### On-Page Optimization
{{onpage_work_completed}}

---

## Priorities for Next Month

| Priority | Task | Category | Expected Impact | Owner |
|----------|------|----------|----------------|-------|
| 1 | {{priority_1_task}} | {{priority_1_cat}} | {{priority_1_impact}} | {{priority_1_owner}} |
| 2 | {{priority_2_task}} | {{priority_2_cat}} | {{priority_2_impact}} | {{priority_2_owner}} |
| 3 | {{priority_3_task}} | {{priority_3_cat}} | {{priority_3_impact}} | {{priority_3_owner}} |
| 4 | {{priority_4_task}} | {{priority_4_cat}} | {{priority_4_impact}} | {{priority_4_owner}} |
| 5 | {{priority_5_task}} | {{priority_5_cat}} | {{priority_5_impact}} | {{priority_5_owner}} |

---

## Appendix

### A. Full Keyword Ranking Table
{{full_ranking_table}}

### B. Google Search Console Data
{{gsc_data}}

### C. Analytics Screenshots
{{analytics_screenshots}}

### D. Notes & Caveats
{{notes_caveats}}
