---
template: seo-audit-report
version: 1.0
type: audit
description: Master SEO audit covering technical, content, keywords, backlinks, AEO, and competitor analysis
agents: seo-auditor, technical-seo-auditor, keyword-researcher, content-auditor, backlink-analyst, aeo-analyst
---

# SEO Audit Report

## Cover Page

| Field | Details |
|-------|---------|
| **Client** | {{client_name}} |
| **Website** | {{website_url}} |
| **Audit Date** | {{audit_date}} |
| **Prepared By** | {{prepared_by}} |
| **Audit Period** | {{audit_start_date}} — {{audit_end_date}} |
| **Overall Health Score** | {{health_score}}/100 |

---

## Executive Summary

**Current State:** {{current_state_summary}}

**Top 3 Critical Issues:**
1. {{critical_issue_1}}
2. {{critical_issue_2}}
3. {{critical_issue_3}}

**Top 3 Opportunities:**
1. {{opportunity_1}}
2. {{opportunity_2}}
3. {{opportunity_3}}

**Estimated Traffic Upside:** {{estimated_traffic_upside}}

---

## 1. Technical SEO Findings

### 1.1 Crawl Statistics

| Metric | Value | Status |
|--------|-------|--------|
| Total Pages Found | {{total_pages}} | {{total_pages_status}} |
| Pages Crawled | {{pages_crawled}} | {{pages_crawled_status}} |
| Avg. Crawl Depth | {{avg_crawl_depth}} | {{crawl_depth_status}} |
| Avg. Response Time | {{avg_response_time}} | {{response_time_status}} |
| Crawl Budget Waste | {{crawl_budget_waste}} | {{crawl_budget_status}} |

### 1.2 Indexation

| Metric | Value | Status |
|--------|-------|--------|
| Indexed Pages | {{indexed_pages}} | {{indexed_status}} |
| Non-Indexed Pages | {{non_indexed_pages}} | {{non_indexed_status}} |
| Robots.txt Issues | {{robots_issues}} | {{robots_status}} |
| Sitemap Issues | {{sitemap_issues}} | {{sitemap_status}} |
| Canonical Issues | {{canonical_issues}} | {{canonical_status}} |

### 1.3 Core Web Vitals

| Metric | Mobile | Desktop | Threshold | Status |
|--------|--------|---------|-----------|--------|
| LCP | {{lcp_mobile}} | {{lcp_desktop}} | < 2.5s | {{lcp_status}} |
| INP | {{inp_mobile}} | {{inp_desktop}} | < 200ms | {{inp_status}} |
| CLS | {{cls_mobile}} | {{cls_desktop}} | < 0.1 | {{cls_status}} |

### 1.4 Schema Markup

| Schema Type | Present | Validated | Recommendation |
|-------------|---------|-----------|----------------|
{{schema_rows}}

### 1.5 Internal Linking

| Metric | Value |
|--------|-------|
| Orphan Pages | {{orphan_pages}} |
| Pages with 1 Internal Link | {{single_link_pages}} |
| Avg. Internal Links per Page | {{avg_internal_links}} |
| Deepest Page (clicks from home) | {{deepest_page}} |

### 1.6 Mobile Audit

| Check | Result | Status |
|-------|--------|--------|
| Viewport Configured | {{viewport_configured}} | {{viewport_status}} |
| Tap Targets Sized | {{tap_targets}} | {{tap_targets_status}} |
| Content Parity | {{content_parity}} | {{content_parity_status}} |
| Mobile Page Speed | {{mobile_speed}} | {{mobile_speed_status}} |

---

## 2. Keyword Analysis

### 2.1 Keyword Landscape

| Metric | Value |
|--------|-------|
| Total Keywords Tracked | {{total_keywords}} |
| Keywords in Top 3 | {{keywords_top_3}} |
| Keywords in Top 10 | {{keywords_top_10}} |
| Keywords in Top 100 | {{keywords_top_100}} |
| Avg. Position | {{avg_position}} |

### 2.2 Keyword Clusters

| Cluster | Primary Keyword | Supporting Keywords | Est. Monthly Volume | Current Best Rank |
|---------|----------------|--------------------|--------------------|-------------------|
{{keyword_cluster_rows}}

### 2.3 Keyword Gaps

| Keyword | Competitor Ranking | Our Ranking | Gap Type | Priority |
|---------|-------------------|-------------|----------|----------|
{{keyword_gap_rows}}

### 2.4 SERP Feature Opportunities

| SERP Feature | Current Presence | Opportunity Keywords | Difficulty |
|--------------|-----------------|---------------------|------------|
| Featured Snippet | {{snippet_current}} | {{snippet_opportunities}} | {{snippet_difficulty}} |
| People Also Ask | {{paa_current}} | {{paa_opportunities}} | {{paa_difficulty}} |
| AI Overview | {{aio_current}} | {{aio_opportunities}} | {{aio_difficulty}} |
| Local Pack | {{local_current}} | {{local_opportunities}} | {{local_difficulty}} |
| Image Pack | {{image_current}} | {{image_opportunities}} | {{image_difficulty}} |

---

## 3. Content Audit

### 3.1 Content Inventory

| Metric | Count |
|--------|-------|
| Total Pages Audited | {{total_content_pages}} |
| Blog Posts | {{blog_count}} |
| Landing Pages | {{landing_count}} |
| Product/Service Pages | {{product_count}} |
| Thin Content (< 300 words) | {{thin_content_count}} |
| Duplicate/Near-Duplicate | {{duplicate_count}} |

### 3.2 Quality Assessment

| Rating | Count | % of Total | Action |
|--------|-------|-----------|--------|
| High Quality | {{high_quality_count}} | {{high_quality_pct}} | Maintain & Optimize |
| Medium Quality | {{medium_quality_count}} | {{medium_quality_pct}} | Improve |
| Low Quality | {{low_quality_count}} | {{low_quality_pct}} | Rewrite or Consolidate |
| Remove/Redirect | {{remove_count}} | {{remove_pct}} | Prune |

### 3.3 Content Gaps

| Topic Gap | Search Volume | Competitor Coverage | Recommended Content Type |
|-----------|--------------|--------------------|-----------------------|
{{content_gap_rows}}

### 3.4 Optimization Opportunities

| Page | Current Keyword | Issue | Recommendation | Est. Impact |
|------|----------------|-------|----------------|-------------|
{{content_optimization_rows}}

---

## 4. Backlink Audit

### 4.1 Profile Overview

| Metric | Value |
|--------|-------|
| Total Backlinks | {{total_backlinks}} |
| Referring Domains | {{referring_domains}} |
| Domain Authority | {{domain_authority}} |
| Dofollow / Nofollow Ratio | {{dofollow_ratio}} |
| Link Velocity (last 30d) | {{link_velocity}} |

### 4.2 Quality Distribution

| Quality Tier | Count | % of Total |
|-------------|-------|-----------|
| High Quality | {{high_quality_links}} | {{high_quality_links_pct}} |
| Medium Quality | {{medium_quality_links}} | {{medium_quality_links_pct}} |
| Low Quality | {{low_quality_links}} | {{low_quality_links_pct}} |
| Toxic | {{toxic_links}} | {{toxic_links_pct}} |

### 4.3 Toxic Link Candidates

| # | Referring URL | Anchor Text | Reason | Recommendation |
|---|--------------|-------------|--------|----------------|
{{toxic_link_rows}}

### 4.4 Competitor Backlink Comparison

| Metric | {{client_name}} | {{competitor_1}} | {{competitor_2}} | {{competitor_3}} |
|--------|-----------------|-------------------|-------------------|-------------------|
| Referring Domains | {{client_rd}} | {{comp1_rd}} | {{comp2_rd}} | {{comp3_rd}} |
| Domain Authority | {{client_da}} | {{comp1_da}} | {{comp2_da}} | {{comp3_da}} |
| Link Velocity | {{client_lv}} | {{comp1_lv}} | {{comp2_lv}} | {{comp3_lv}} |

---

## 5. AEO Assessment

### 5.1 AI Overview Presence

| Query | AI Overview Triggered | Client Cited | Competitor Cited | Action |
|-------|-----------------------|-------------|-----------------|--------|
{{aeo_query_rows}}

### 5.2 Featured Snippet Status

| Query | Snippet Type | Current Owner | Client Eligible | Optimization Needed |
|-------|-------------|--------------|----------------|-------------------|
{{snippet_status_rows}}

### 5.3 Entity Status

| Entity | Knowledge Panel | Wikidata Entry | Schema Markup | Status |
|--------|----------------|---------------|--------------|--------|
{{entity_status_rows}}

### 5.4 Knowledge Panel

| Field | Current State | Recommendation |
|-------|--------------|----------------|
| Knowledge Panel Active | {{kp_active}} | {{kp_recommendation}} |
| Information Accuracy | {{kp_accuracy}} | {{kp_accuracy_rec}} |
| Images | {{kp_images}} | {{kp_images_rec}} |

---

## 6. Competitor Analysis

### 6.1 Top Competitors

| Competitor | Domain | DA | Organic Traffic | Top Keywords |
|-----------|--------|-----|----------------|-------------|
{{competitor_overview_rows}}

### 6.2 Strengths & Weaknesses

**{{competitor_1}}:**
- Strengths: {{comp1_strengths}}
- Weaknesses: {{comp1_weaknesses}}

**{{competitor_2}}:**
- Strengths: {{comp2_strengths}}
- Weaknesses: {{comp2_weaknesses}}

**{{competitor_3}}:**
- Strengths: {{comp3_strengths}}
- Weaknesses: {{comp3_weaknesses}}

### 6.3 Opportunities

{{competitor_opportunities}}

---

## 7. Priority Matrix

### Quick Wins (High Impact / Low Effort)

| # | Issue | Category | Expected Impact | Effort |
|---|-------|----------|----------------|--------|
{{quick_wins_rows}}

### Strategic Investments (High Impact / High Effort)

| # | Issue | Category | Expected Impact | Effort |
|---|-------|----------|----------------|--------|
{{strategic_investment_rows}}

---

## 8. Implementation Roadmap

### Days 1-30: Foundation

{{roadmap_30_day}}

### Days 31-60: Optimization

{{roadmap_60_day}}

### Days 61-90: Growth

{{roadmap_90_day}}

---

## Appendix

### A. Tools Used
{{tools_used}}

### B. Data Sources
{{data_sources}}

### C. Methodology Notes
{{methodology_notes}}

### D. Glossary
{{glossary}}
