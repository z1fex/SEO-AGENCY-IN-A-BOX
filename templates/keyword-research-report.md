---
template: keyword-research-report
version: 1.0
type: research
description: Comprehensive keyword research with clusters, intent mapping, gaps, and content recommendations
agents: keyword-researcher, content-strategist
---

# Keyword Research Report

| Field | Details |
|-------|---------|
| **Client** | {{client_name}} |
| **Website** | {{website_url}} |
| **Date** | {{report_date}} |
| **Prepared By** | {{prepared_by}} |
| **Target Market** | {{target_market}} |
| **Target Location** | {{target_location}} |

---

## Executive Summary

{{executive_summary}}

| Metric | Value |
|--------|-------|
| Total Keywords Identified | {{total_keywords}} |
| Keyword Clusters | {{total_clusters}} |
| Avg. Monthly Search Volume (all) | {{total_search_volume}} |
| Quick-Win Keywords (rank 4-20) | {{quick_win_count}} |
| New Opportunity Keywords | {{new_opportunity_count}} |

---

## Methodology

- **Seed Source:** {{seed_source}}
- **Tools Used:** {{tools_used}}
- **Competitor Domains Analyzed:** {{competitor_domains_analyzed}}
- **Filters Applied:** {{filters_applied}}
- **Location/Language:** {{location_language}}

---

## Seed Keywords

| # | Seed Keyword | Source | Rationale |
|---|-------------|--------|-----------|
{{seed_keyword_rows}}

---

## Full Keyword List

| # | Keyword | Intent | Est. Monthly Volume | KD | Current Rank | SERP Features | Priority |
|---|---------|--------|--------------------|----|-------------|---------------|----------|
{{full_keyword_rows}}

**Intent Key:** I = Informational, N = Navigational, C = Commercial, T = Transactional

**Priority Key:** P1 = Immediate, P2 = Short-term, P3 = Medium-term, P4 = Long-term

---

## Keyword Clusters

### Cluster 1: {{cluster_1_name}}

**Pillar Keyword:** {{cluster_1_pillar}} (Volume: {{cluster_1_pillar_volume}}, KD: {{cluster_1_pillar_kd}})

| Subtopic Keyword | Intent | Volume | KD | Content Type |
|-----------------|--------|--------|----|-------------|
{{cluster_1_subtopic_rows}}

### Cluster 2: {{cluster_2_name}}

**Pillar Keyword:** {{cluster_2_pillar}} (Volume: {{cluster_2_pillar_volume}}, KD: {{cluster_2_pillar_kd}})

| Subtopic Keyword | Intent | Volume | KD | Content Type |
|-----------------|--------|--------|----|-------------|
{{cluster_2_subtopic_rows}}

### Cluster 3: {{cluster_3_name}}

**Pillar Keyword:** {{cluster_3_pillar}} (Volume: {{cluster_3_pillar_volume}}, KD: {{cluster_3_pillar_kd}})

| Subtopic Keyword | Intent | Volume | KD | Content Type |
|-----------------|--------|--------|----|-------------|
{{cluster_3_subtopic_rows}}

{{additional_clusters}}

---

## Intent Distribution

| Intent Type | Keyword Count | % of Total | Avg. Volume |
|-------------|--------------|-----------|-------------|
| Informational | {{info_count}} | {{info_pct}} | {{info_avg_vol}} |
| Navigational | {{nav_count}} | {{nav_pct}} | {{nav_avg_vol}} |
| Commercial | {{comm_count}} | {{comm_pct}} | {{comm_avg_vol}} |
| Transactional | {{trans_count}} | {{trans_pct}} | {{trans_avg_vol}} |

---

## Competitor Keyword Comparison

| Metric | {{client_name}} | {{competitor_1}} | {{competitor_2}} | {{competitor_3}} |
|--------|-----------------|-------------------|-------------------|-------------------|
| Total Organic Keywords | {{client_kw_count}} | {{comp1_kw_count}} | {{comp2_kw_count}} | {{comp3_kw_count}} |
| Keywords in Top 10 | {{client_top10}} | {{comp1_top10}} | {{comp2_top10}} | {{comp3_top10}} |
| Estimated Organic Traffic | {{client_traffic}} | {{comp1_traffic}} | {{comp2_traffic}} | {{comp3_traffic}} |
| Content Pages | {{client_pages}} | {{comp1_pages}} | {{comp2_pages}} | {{comp3_pages}} |

---

## Keyword Gaps

### Keywords Competitors Rank For (We Don't)

| Keyword | Volume | KD | {{competitor_1}} Rank | {{competitor_2}} Rank | {{competitor_3}} Rank | Priority |
|---------|--------|----|----------------------|----------------------|----------------------|----------|
{{keyword_gap_rows}}

### Keywords Only We Rank For

| Keyword | Volume | Our Rank | Opportunity |
|---------|--------|----------|-------------|
{{unique_keyword_rows}}

---

## SERP Feature Opportunities

| SERP Feature | Keyword | Current Owner | Difficulty | Content Needed |
|-------------|---------|--------------|------------|---------------|
{{serp_feature_rows}}

---

## Content Recommendations

| Priority | Target Keyword | Content Type | Cluster | Est. Volume | Recommended Title |
|----------|---------------|-------------|---------|-------------|-------------------|
{{content_recommendation_rows}}

---

## Next Steps

1. {{next_step_1}}
2. {{next_step_2}}
3. {{next_step_3}}
4. {{next_step_4}}
5. {{next_step_5}}
