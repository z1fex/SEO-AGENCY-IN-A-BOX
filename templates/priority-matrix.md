---
template: priority-matrix
version: 1.0
type: strategy
description: Impact x Effort priority matrix for SEO issues with scoring methodology and implementation order
agents: seo-strategist, project-manager
---

# Priority Matrix

| Field | Details |
|-------|---------|
| **Client** | {{client_name}} |
| **Website** | {{website_url}} |
| **Date** | {{matrix_date}} |
| **Prepared By** | {{prepared_by}} |
| **Total Issues Evaluated** | {{total_issues}} |
| **Source Audit** | {{source_audit_reference}} |

---

## Methodology

### Impact Score (1-5)

| Score | Label | Definition |
|-------|-------|-----------|
| 5 | Critical | Directly blocking organic growth or causing ranking loss |
| 4 | High | Strong positive effect on traffic, rankings, or conversions |
| 3 | Medium | Noticeable improvement across multiple pages or keywords |
| 2 | Low | Minor improvement, limited to a few pages |
| 1 | Minimal | Marginal or theoretical benefit |

### Effort Score (1-5)

| Score | Label | Definition |
|-------|-------|-----------|
| 1 | Trivial | < 1 hour, no dev resources needed |
| 2 | Low | 1-4 hours, minimal coordination |
| 3 | Medium | 1-2 days, may require dev or content resources |
| 4 | High | 3-5 days, multiple stakeholders |
| 5 | Major | 1+ weeks, significant dev work or content production |

### Priority Score Formula

`Priority Score = Impact - (Effort * 0.5)`

Higher score = higher priority. Ties broken by Impact (higher Impact wins).

---

## Quick Wins (High Impact / Low Effort)

*Do these first. Maximum ROI for minimum investment.*

| # | Issue | Category | Impact | Effort | Score | Est. Completion |
|---|-------|----------|--------|--------|-------|----------------|
{{quick_win_rows}}

**Estimated total time for Quick Wins:** {{quick_wins_total_time}}

**Expected combined impact:** {{quick_wins_expected_impact}}

---

## Strategic Investments (High Impact / High Effort)

*Plan these carefully. Significant results but require resources and time.*

| # | Issue | Category | Impact | Effort | Score | Est. Completion | Dependencies |
|---|-------|----------|--------|--------|-------|----------------|-------------|
{{strategic_investment_rows}}

**Estimated total time for Strategic Investments:** {{strategic_total_time}}

**Expected combined impact:** {{strategic_expected_impact}}

---

## Low-Hanging Fruit (Low Impact / Low Effort)

*Batch these together. Small wins that add up when done in bulk.*

| # | Issue | Category | Impact | Effort | Score | Batch Group |
|---|-------|----------|--------|--------|-------|------------|
{{low_hanging_fruit_rows}}

**Recommended approach:** {{low_hanging_fruit_approach}}

---

## Deprioritize (Low Impact / High Effort)

*Skip these for now. Not worth the investment at this stage.*

| # | Issue | Category | Impact | Effort | Score | Revisit When |
|---|-------|----------|--------|--------|-------|-------------|
{{deprioritize_rows}}

---

## Full Issue List

| # | Issue | Category | Impact | Effort | Score | Quadrant | Phase | Status |
|---|-------|----------|--------|--------|-------|----------|-------|--------|
{{full_issue_rows}}

**Category Key:** TECH = Technical, CONT = Content, LINK = Link Building, ONPG = On-Page, LOCL = Local, SCHM = Schema, CWV = Core Web Vitals

**Quadrant Key:** QW = Quick Win, SI = Strategic Investment, LHF = Low-Hanging Fruit, DP = Deprioritize

**Phase Key:** P1 = Month 1, P2 = Month 2-3, P3 = Month 4-6, P4 = Month 7+

**Status Key:** NOT STARTED, IN PROGRESS, DONE, BLOCKED

---

## Implementation Order

### Sprint 1 (Week 1-2): Quick Wins

| Order | Issue | Owner | Due Date | Status |
|-------|-------|-------|---------|--------|
{{sprint_1_rows}}

### Sprint 2 (Week 3-4): Quick Wins + Strategic Investment Kickoff

| Order | Issue | Owner | Due Date | Status |
|-------|-------|-------|---------|--------|
{{sprint_2_rows}}

### Sprint 3 (Month 2): Strategic Investments + Batched Low-Hanging Fruit

| Order | Issue | Owner | Due Date | Status |
|-------|-------|-------|---------|--------|
{{sprint_3_rows}}

### Sprint 4 (Month 3): Strategic Investments Continued

| Order | Issue | Owner | Due Date | Status |
|-------|-------|-------|---------|--------|
{{sprint_4_rows}}

---

## Summary

| Quadrant | Issue Count | Est. Total Hours | Expected Traffic Impact |
|----------|-----------|-----------------|----------------------|
| Quick Wins | {{qw_count}} | {{qw_hours}} | {{qw_traffic_impact}} |
| Strategic Investments | {{si_count}} | {{si_hours}} | {{si_traffic_impact}} |
| Low-Hanging Fruit | {{lhf_count}} | {{lhf_hours}} | {{lhf_traffic_impact}} |
| Deprioritize | {{dp_count}} | {{dp_hours}} | {{dp_traffic_impact}} |
| **Total** | {{total_count}} | {{total_hours}} | {{total_traffic_impact}} |
