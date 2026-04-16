---
template: backlink-audit-report
version: 1.0
type: audit
description: Backlink profile audit with quality analysis, toxic link identification, and link building opportunities
agents: backlink-analyst, link-builder
---

# Backlink Audit Report

| Field | Details |
|-------|---------|
| **Client** | {{client_name}} |
| **Website** | {{website_url}} |
| **Audit Date** | {{audit_date}} |
| **Prepared By** | {{prepared_by}} |
| **Data Source** | {{data_source}} |
| **Data Pulled** | {{data_pull_date}} |

---

## Profile Overview

| Metric | Value | Industry Benchmark | Status |
|--------|-------|--------------------|--------|
| Total Backlinks | {{total_backlinks}} | {{benchmark_backlinks}} | {{backlinks_status}} |
| Referring Domains | {{referring_domains}} | {{benchmark_rd}} | {{rd_status}} |
| Domain Authority | {{domain_authority}} | {{benchmark_da}} | {{da_status}} |
| Dofollow Links | {{dofollow_count}} ({{dofollow_pct}}) | — | {{dofollow_status}} |
| Nofollow Links | {{nofollow_count}} ({{nofollow_pct}}) | — | — |
| Link Velocity (30d) | {{link_velocity_30d}} | {{benchmark_velocity}} | {{velocity_status}} |
| Links Lost (30d) | {{links_lost_30d}} | — | {{lost_status}} |

---

## Quality Distribution

| Quality Tier | Referring Domains | % of Total | Description |
|-------------|------------------|-----------|-------------|
| High Quality (DA 50+) | {{high_quality_count}} | {{high_quality_pct}} | Authoritative, relevant, editorial links |
| Medium Quality (DA 20-49) | {{medium_quality_count}} | {{medium_quality_pct}} | Decent authority, generally relevant |
| Low Quality (DA 1-19) | {{low_quality_count}} | {{low_quality_pct}} | Low authority but not harmful |
| Toxic / Spam | {{toxic_count}} | {{toxic_pct}} | Harmful, should be disavowed |

**Health Score:** {{backlink_health_score}}/100

---

## Toxic Link Candidates

| # | Referring URL | Referring Domain DA | Anchor Text | Reason for Concern | Recommendation |
|---|--------------|--------------------|-----------  |--------------------  |----------------|
{{toxic_link_rows}}

**Total Toxic Links Identified:** {{total_toxic_links}}

**Risk Level:** {{toxicity_risk_level}}

---

## Top Referring Domains

| # | Domain | DA | Total Links | Link Type | Anchor Text | First Seen |
|---|--------|----|-----------|-----------|-------------|-----------|
{{top_referring_domain_rows}}

---

## Anchor Text Distribution

| Anchor Text Category | Count | % of Total | Health Status |
|---------------------|-------|-----------|---------------|
| Branded | {{branded_count}} | {{branded_pct}} | {{branded_status}} |
| Exact Match | {{exact_count}} | {{exact_pct}} | {{exact_status}} |
| Partial Match | {{partial_count}} | {{partial_pct}} | {{partial_status}} |
| Generic (click here, etc.) | {{generic_count}} | {{generic_pct}} | {{generic_status}} |
| URL | {{url_count}} | {{url_pct}} | {{url_status}} |
| Image (no alt) | {{image_count}} | {{image_pct}} | {{image_status}} |
| Other | {{other_count}} | {{other_pct}} | — |

**Assessment:** {{anchor_text_assessment}}

---

## Link Type Breakdown

| Link Type | Count | % of Total |
|-----------|-------|-----------|
| Editorial / Contextual | {{editorial_count}} | {{editorial_pct}} |
| Guest Post | {{guest_post_count}} | {{guest_post_pct}} |
| Directory | {{directory_count}} | {{directory_pct}} |
| PR / News | {{pr_count}} | {{pr_pct}} |
| Social Profile | {{social_count}} | {{social_pct}} |
| Forum / Comment | {{forum_count}} | {{forum_pct}} |
| Resource Page | {{resource_count}} | {{resource_pct}} |
| Sidebar / Footer | {{sidebar_count}} | {{sidebar_pct}} |
| Other | {{other_type_count}} | {{other_type_pct}} |

---

## Competitor Comparison

| Metric | {{client_name}} | {{competitor_1}} | {{competitor_2}} | {{competitor_3}} |
|--------|-----------------|-------------------|-------------------|-------------------|
| Referring Domains | {{client_rd}} | {{comp1_rd}} | {{comp2_rd}} | {{comp3_rd}} |
| Domain Authority | {{client_da}} | {{comp1_da}} | {{comp2_da}} | {{comp3_da}} |
| High Quality Links | {{client_hq}} | {{comp1_hq}} | {{comp2_hq}} | {{comp3_hq}} |
| Link Velocity (30d) | {{client_lv}} | {{comp1_lv}} | {{comp2_lv}} | {{comp3_lv}} |
| Branded Anchor % | {{client_branded}} | {{comp1_branded}} | {{comp2_branded}} | {{comp3_branded}} |

### Domains Linking to Competitors But Not Us

| # | Domain | DA | Links to {{competitor_1}} | Links to {{competitor_2}} | Links to {{competitor_3}} | Opportunity |
|---|--------|----|--------------------------|--------------------------|--------------------------|-------------|
{{competitor_gap_rows}}

---

## Disavow Recommendations

**Disavow Action Required:** {{disavow_required}}

**Total Domains to Disavow:** {{disavow_domain_count}}

**Total URLs to Disavow:** {{disavow_url_count}}

### Disavow List

| # | Type | Entry | Reason |
|---|------|-------|--------|
{{disavow_list_rows}}

**Next Steps for Disavow:**
1. {{disavow_step_1}}
2. {{disavow_step_2}}
3. {{disavow_step_3}}

---

## Link Building Opportunities

| # | Opportunity Type | Target Domain/Page | DA | Approach | Difficulty | Priority |
|---|-----------------|-------------------|-----|----------|-----------|----------|
{{link_opportunity_rows}}

---

## Next Steps

1. {{next_step_1}}
2. {{next_step_2}}
3. {{next_step_3}}
4. {{next_step_4}}
5. {{next_step_5}}
