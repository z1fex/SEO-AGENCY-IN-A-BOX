---
template: technical-audit
version: 1.0
type: audit
description: Technical SEO audit covering crawl, indexation, Core Web Vitals, schema, internal linking, mobile, security, and redirects
agents: technical-seo-auditor
---

# Technical SEO Audit

| Field | Details |
|-------|---------|
| **Client** | {{client_name}} |
| **Website** | {{website_url}} |
| **Audit Date** | {{audit_date}} |
| **Prepared By** | {{prepared_by}} |
| **Crawl Tool** | {{crawl_tool}} |
| **Pages Analyzed** | {{pages_analyzed}} |
| **Technical Health Score** | {{tech_health_score}}/100 |

---

## 1. Crawl Summary

| Metric | Value | Status |
|--------|-------|--------|
| Total URLs Discovered | {{total_urls}} | — |
| Crawlable URLs | {{crawlable_urls}} | {{crawlable_status}} |
| Blocked by Robots.txt | {{blocked_urls}} | {{blocked_status}} |
| Avg. Crawl Depth | {{avg_crawl_depth}} | {{crawl_depth_status}} |
| Avg. Page Load Time | {{avg_load_time}} | {{load_time_status}} |
| Avg. Page Size | {{avg_page_size}} | {{page_size_status}} |

### Status Code Distribution

| Status Code | Count | % of Total | Action |
|-------------|-------|-----------|--------|
| 200 OK | {{status_200}} | {{status_200_pct}} | — |
| 301 Redirect | {{status_301}} | {{status_301_pct}} | {{action_301}} |
| 302 Redirect | {{status_302}} | {{status_302_pct}} | {{action_302}} |
| 404 Not Found | {{status_404}} | {{status_404_pct}} | {{action_404}} |
| 410 Gone | {{status_410}} | {{status_410_pct}} | {{action_410}} |
| 500 Server Error | {{status_500}} | {{status_500_pct}} | {{action_500}} |
| Other | {{status_other}} | {{status_other_pct}} | {{action_other}} |

### Crawl Depth Distribution

| Depth (clicks from home) | Pages | % of Total |
|--------------------------|-------|-----------|
| 0 (Homepage) | 1 | {{depth_0_pct}} |
| 1 | {{depth_1}} | {{depth_1_pct}} |
| 2 | {{depth_2}} | {{depth_2_pct}} |
| 3 | {{depth_3}} | {{depth_3_pct}} |
| 4+ | {{depth_4plus}} | {{depth_4plus_pct}} |

---

## 2. Indexation Status

| Metric | Value | Status |
|--------|-------|--------|
| Indexed Pages (GSC) | {{indexed_pages}} | {{indexed_status}} |
| Non-Indexed Pages (GSC) | {{non_indexed_pages}} | {{non_indexed_status}} |
| Index Bloat | {{index_bloat}} | {{bloat_status}} |

### Robots.txt Issues

| # | Issue | Affected URLs | Severity | Recommendation |
|---|-------|--------------|----------|----------------|
{{robots_issue_rows}}

### Sitemap Issues

| # | Issue | Sitemap URL | Severity | Recommendation |
|---|-------|-----------|----------|----------------|
{{sitemap_issue_rows}}

### Canonical Issues

| # | Issue Type | Page URL | Current Canonical | Correct Canonical | Severity |
|---|-----------|---------|-------------------|-------------------|----------|
{{canonical_issue_rows}}

### Noindex Issues

| # | Page URL | Source (tag/header) | Intentional | Recommendation |
|---|---------|-------------------|-------------|----------------|
{{noindex_issue_rows}}

---

## 3. Core Web Vitals

### Origin Summary (CrUX)

| Metric | Mobile | Desktop | Threshold | Status |
|--------|--------|---------|-----------|--------|
| LCP (Largest Contentful Paint) | {{lcp_mobile}} | {{lcp_desktop}} | Good: < 2.5s | {{lcp_status}} |
| INP (Interaction to Next Paint) | {{inp_mobile}} | {{inp_desktop}} | Good: < 200ms | {{inp_status}} |
| CLS (Cumulative Layout Shift) | {{cls_mobile}} | {{cls_desktop}} | Good: < 0.1 | {{cls_status}} |

### Per-Page-Category Breakdown

| Page Category | LCP (Mobile) | INP (Mobile) | CLS (Mobile) | Overall | Sample URL |
|--------------|-------------|-------------|-------------|---------|-----------|
{{cwv_category_rows}}

### LCP Issues

| # | Issue | Affected Pages | Fix | Priority |
|---|-------|---------------|-----|----------|
{{lcp_issue_rows}}

### INP Issues

| # | Issue | Affected Pages | Fix | Priority |
|---|-------|---------------|-----|----------|
{{inp_issue_rows}}

### CLS Issues

| # | Issue | Affected Pages | Fix | Priority |
|---|-------|---------------|-----|----------|
{{cls_issue_rows}}

---

## 4. Schema Markup

### Current Schema

| Schema Type | Pages Using | Validated | Errors | Warnings |
|-------------|-----------|-----------|--------|----------|
{{current_schema_rows}}

### Recommended Schema Additions

| Page Type | Recommended Schema | Benefit | Priority |
|-----------|-------------------|---------|----------|
{{recommended_schema_rows}}

### Schema Errors

| # | Page | Schema Type | Error | Fix |
|---|------|-----------|-------|-----|
{{schema_error_rows}}

---

## 5. Internal Linking

### Overview

| Metric | Value | Status |
|--------|-------|--------|
| Avg. Internal Links per Page | {{avg_internal_links}} | {{internal_links_status}} |
| Orphan Pages (0 internal links) | {{orphan_pages}} | {{orphan_status}} |
| Pages with 1 Internal Link | {{single_link_pages}} | {{single_link_status}} |
| Max Internal Links on a Page | {{max_links_page}} | {{max_links_status}} |

### Orphan Pages

| # | URL | Organic Traffic | Recommended Link From |
|---|-----|----------------|---------------------|
{{orphan_page_rows}}

### Hub Pages (Most Internal Links)

| # | URL | Internal Links Out | Internal Links In | Role |
|---|-----|-------------------|------------------|------|
{{hub_page_rows}}

### Link Distribution Issues

| # | Issue | Affected Pages | Recommendation |
|---|-------|---------------|----------------|
{{link_distribution_issue_rows}}

---

## 6. Mobile Audit

| Check | Result | Status | Fix Required |
|-------|--------|--------|-------------|
| Viewport Meta Tag | {{viewport_result}} | {{viewport_status}} | {{viewport_fix}} |
| Tap Target Size (48px+) | {{tap_target_result}} | {{tap_target_status}} | {{tap_target_fix}} |
| Font Size Legibility | {{font_size_result}} | {{font_size_status}} | {{font_size_fix}} |
| Content Width (no h-scroll) | {{content_width_result}} | {{content_width_status}} | {{content_width_fix}} |
| Content Parity (mobile vs desktop) | {{parity_result}} | {{parity_status}} | {{parity_fix}} |
| Mobile Page Speed | {{mobile_speed_result}} | {{mobile_speed_status}} | {{mobile_speed_fix}} |
| Intrusive Interstitials | {{interstitial_result}} | {{interstitial_status}} | {{interstitial_fix}} |

### Mobile-Specific Issues

| # | Issue | Affected Pages | Severity | Fix |
|---|-------|---------------|----------|-----|
{{mobile_issue_rows}}

---

## 7. Security

| Check | Result | Status |
|-------|--------|--------|
| HTTPS Enabled | {{https_enabled}} | {{https_status}} |
| SSL Certificate Valid | {{ssl_valid}} | {{ssl_status}} |
| SSL Expiry Date | {{ssl_expiry}} | — |
| Mixed Content Issues | {{mixed_content_count}} | {{mixed_content_status}} |
| HTTP to HTTPS Redirect | {{http_redirect}} | {{http_redirect_status}} |
| HSTS Header | {{hsts_header}} | {{hsts_status}} |

### Mixed Content URLs

| # | Page | Resource Type | Insecure URL | Fix |
|---|------|-------------|-------------|-----|
{{mixed_content_rows}}

---

## 8. Redirect Map

### Redirect Chains

| # | Chain | Hops | Final Destination | Fix |
|---|-------|------|-------------------|-----|
{{redirect_chain_rows}}

### Redirect Loops

| # | Loop | Fix |
|---|------|-----|
{{redirect_loop_rows}}

### Temporary Redirects (302) That Should Be 301

| # | Source URL | Destination URL | Reason to Permanentize |
|---|----------|----------------|----------------------|
{{temp_redirect_rows}}

---

## 9. Priority Fixes

| # | Issue | Category | Page(s) | Fix | Priority | Effort | Impact |
|---|-------|----------|---------|-----|----------|--------|--------|
{{priority_fix_rows}}

**Priority Key:** P1 = Critical (fix immediately), P2 = High (fix within 2 weeks), P3 = Medium (fix within 30 days), P4 = Low (backlog)

**Effort Key:** Low = < 1 hour, Medium = 1-4 hours, High = 4+ hours

---

## Appendix

### A. Full Crawl Data
{{crawl_data_reference}}

### B. Tools Used
{{tools_used}}

### C. Testing Methodology
{{testing_methodology}}
