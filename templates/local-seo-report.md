---
template: local-seo-report
version: 1.0
type: report
description: Local SEO report covering GBP audit, local rankings, citations, reviews, and local competitor comparison
agents: local-seo-specialist
---

# Local SEO Report

| Field | Details |
|-------|---------|
| **Client** | {{client_name}} |
| **Business Name** | {{business_name}} |
| **Website** | {{website_url}} |
| **Primary Location** | {{primary_location}} |
| **Report Date** | {{report_date}} |
| **Prepared By** | {{prepared_by}} |
| **Local SEO Score** | {{local_seo_score}}/100 |

---

## 1. Google Business Profile Audit

### Current State

| Field | Current Value | Optimized | Recommendation |
|-------|-------------|-----------|----------------|
| Business Name | {{gbp_name}} | {{gbp_name_optimized}} | {{gbp_name_rec}} |
| Primary Category | {{gbp_primary_cat}} | {{gbp_primary_cat_optimized}} | {{gbp_primary_cat_rec}} |
| Secondary Categories | {{gbp_secondary_cats}} | {{gbp_secondary_cats_optimized}} | {{gbp_secondary_cats_rec}} |
| Address | {{gbp_address}} | {{gbp_address_optimized}} | {{gbp_address_rec}} |
| Phone Number | {{gbp_phone}} | {{gbp_phone_optimized}} | {{gbp_phone_rec}} |
| Website URL | {{gbp_website}} | {{gbp_website_optimized}} | {{gbp_website_rec}} |
| Business Hours | {{gbp_hours}} | {{gbp_hours_optimized}} | {{gbp_hours_rec}} |
| Description | {{gbp_description_status}} | {{gbp_description_optimized}} | {{gbp_description_rec}} |
| Photos | {{gbp_photos_count}} | {{gbp_photos_optimized}} | {{gbp_photos_rec}} |
| Posts (last 30d) | {{gbp_posts_count}} | {{gbp_posts_optimized}} | {{gbp_posts_rec}} |
| Q&A | {{gbp_qa_count}} | {{gbp_qa_optimized}} | {{gbp_qa_rec}} |
| Products/Services | {{gbp_products}} | {{gbp_products_optimized}} | {{gbp_products_rec}} |
| Attributes | {{gbp_attributes}} | {{gbp_attributes_optimized}} | {{gbp_attributes_rec}} |

### GBP Optimization Recommendations

{{gbp_optimization_recommendations}}

---

## 2. Local Rankings

### Local Pack Rankings

| # | Target Keyword | Volume | Pack Position | Organic Position | Trend |
|---|---------------|--------|-------------|-----------------|-------|
{{local_ranking_rows}}

### Map Rankings by Location

| Keyword | Grid Center | Avg. Rank | Best Rank | Worst Rank | Visibility % |
|---------|-----------|-----------|-----------|-----------|-------------|
{{map_ranking_rows}}

---

## 3. Citation Audit

### NAP Consistency

| Field | Correct Value | Consistent Across Citations |
|-------|-------------|---------------------------|
| Name | {{nap_name}} | {{name_consistency}} |
| Address | {{nap_address}} | {{address_consistency}} |
| Phone | {{nap_phone}} | {{phone_consistency}} |

**NAP Consistency Score:** {{nap_consistency_score}}/100

### Current Citations

| # | Directory | Listed | NAP Correct | Profile Complete | Action Needed |
|---|----------|--------|-------------|-----------------|--------------|
{{citation_rows}}

### Missing Citations (Priority Directories)

| # | Directory | Domain Authority | Industry Relevance | Priority |
|---|----------|-----------------|-------------------|----------|
{{missing_citation_rows}}

### Inconsistent Citations (Fix Required)

| # | Directory | Current Name | Current Address | Current Phone | Issue |
|---|----------|-------------|----------------|--------------|-------|
{{inconsistent_citation_rows}}

---

## 4. Review Analysis

### Overview

| Metric | Value | Industry Avg. | Status |
|--------|-------|-------------|--------|
| Total Reviews (Google) | {{total_reviews}} | {{avg_reviews}} | {{reviews_status}} |
| Average Rating | {{avg_rating}} | {{industry_avg_rating}} | {{rating_status}} |
| Reviews (Last 30d) | {{recent_reviews}} | — | {{recent_reviews_status}} |
| Response Rate | {{response_rate}} | — | {{response_rate_status}} |
| Avg. Response Time | {{avg_response_time}} | — | {{response_time_status}} |

### Rating Distribution

| Stars | Count | % of Total |
|-------|-------|-----------|
| 5 Stars | {{five_star}} | {{five_star_pct}} |
| 4 Stars | {{four_star}} | {{four_star_pct}} |
| 3 Stars | {{three_star}} | {{three_star_pct}} |
| 2 Stars | {{two_star}} | {{two_star_pct}} |
| 1 Star | {{one_star}} | {{one_star_pct}} |

### Sentiment Analysis

| Theme | Positive Mentions | Negative Mentions | Net Sentiment |
|-------|------------------|------------------|--------------|
{{sentiment_rows}}

### Review Response Strategy

{{review_response_strategy}}

### Review Generation Recommendations

{{review_generation_recommendations}}

---

## 5. Local Competitor Comparison

| Metric | {{client_name}} | {{local_comp_1}} | {{local_comp_2}} | {{local_comp_3}} |
|--------|-----------------|-------------------|-------------------|-------------------|
| Google Reviews | {{client_reviews}} | {{lcomp1_reviews}} | {{lcomp2_reviews}} | {{lcomp3_reviews}} |
| Avg. Rating | {{client_rating}} | {{lcomp1_rating}} | {{lcomp2_rating}} | {{lcomp3_rating}} |
| GBP Categories | {{client_cats}} | {{lcomp1_cats}} | {{lcomp2_cats}} | {{lcomp3_cats}} |
| GBP Photos | {{client_photos}} | {{lcomp1_photos}} | {{lcomp2_photos}} | {{lcomp3_photos}} |
| GBP Posts (30d) | {{client_posts}} | {{lcomp1_posts}} | {{lcomp2_posts}} | {{lcomp3_posts}} |
| Citation Count | {{client_citations}} | {{lcomp1_citations}} | {{lcomp2_citations}} | {{lcomp3_citations}} |
| Local Pack Visibility | {{client_visibility}} | {{lcomp1_visibility}} | {{lcomp2_visibility}} | {{lcomp3_visibility}} |

---

## 6. Local Content Assessment

| Content Element | Present | Optimized | Recommendation |
|----------------|---------|-----------|----------------|
| Location Page(s) | {{location_pages_present}} | {{location_pages_optimized}} | {{location_pages_rec}} |
| Local Schema Markup | {{local_schema_present}} | {{local_schema_optimized}} | {{local_schema_rec}} |
| Embedded Map | {{map_present}} | {{map_optimized}} | {{map_rec}} |
| Local Keywords in Title Tags | {{local_titles_present}} | {{local_titles_optimized}} | {{local_titles_rec}} |
| Local Keywords in Meta Descriptions | {{local_metas_present}} | {{local_metas_optimized}} | {{local_metas_rec}} |
| Local Keywords in H1s | {{local_h1s_present}} | {{local_h1s_optimized}} | {{local_h1s_rec}} |
| Local Content/Blog | {{local_content_present}} | {{local_content_optimized}} | {{local_content_rec}} |
| Service Area Pages | {{service_area_present}} | {{service_area_optimized}} | {{service_area_rec}} |

---

## 7. Recommendations

### Immediate (Week 1-2)

| # | Action | Category | Expected Impact |
|---|--------|----------|----------------|
{{immediate_action_rows}}

### Short-Term (Month 1)

| # | Action | Category | Expected Impact |
|---|--------|----------|----------------|
{{short_term_action_rows}}

### Ongoing

| # | Action | Frequency | Category |
|---|--------|----------|----------|
{{ongoing_action_rows}}

---

## 8. Next Steps

1. {{next_step_1}}
2. {{next_step_2}}
3. {{next_step_3}}
4. {{next_step_4}}
5. {{next_step_5}}
