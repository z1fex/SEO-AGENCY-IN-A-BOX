# SEO Quality Assurance Checklist

> Run this checklist on EVERY deliverable before saving to output or presenting to client.

---

## How to Use

1. Go through each section below
2. Check every item that passes
3. Score the deliverable (see scoring at bottom)
4. If score < 3/5, revise and re-check
5. Record the score in the deliverable's frontmatter: `quality-score: X/5`

---

## 1. Data Accuracy (Non-Negotiable)

- [ ] All metrics come from tool results (Firecrawl, Tavily, Web Fetch, Web Search)
- [ ] No made-up search volumes, traffic numbers, or rankings
- [ ] Competitor data verified by actually scraping their sites
- [ ] Technical findings based on actual crawl data, not assumptions
- [ ] Statistics and claims include their source
- [ ] If data was unavailable, it says "data not available" — never fabricated
- [ ] Estimates are clearly labeled as estimates with methodology explained

**If ANY data accuracy check fails → score cannot exceed 2/5**

---

## 2. SEO Best Practices

- [ ] Recommendations follow current Google Search guidelines
- [ ] No black-hat techniques (keyword stuffing, PBNs, link schemes, cloaking)
- [ ] E-E-A-T signals considered (Experience, Expertise, Authoritativeness, Trustworthiness)
- [ ] Search intent alignment verified for keyword-to-content mappings
- [ ] Schema markup recommendations validate against Google's structured data requirements
- [ ] AEO (Answer Engine Optimization) considered where relevant
- [ ] Mobile-first approach applied to all technical recommendations
- [ ] Core Web Vitals thresholds used correctly (LCP <2.5s, INP <200ms, CLS <0.1)

---

## 3. Specificity & Actionability

- [ ] Every recommendation includes WHAT to change
- [ ] Every recommendation includes WHERE to change it (specific URL/page/element)
- [ ] Every recommendation includes HOW to implement (step-by-step)
- [ ] Every recommendation includes WHY it matters (expected impact)
- [ ] Every recommendation has a priority level (Critical / High / Medium / Low)
- [ ] No generic advice ("improve your SEO" — this is worthless)
- [ ] Code examples provided where applicable (schema, meta tags, redirects)
- [ ] Fixes are implementable on the client's CMS/platform

---

## 4. Completeness

- [ ] No placeholder text ("[insert here]", "TBD", "TODO")
- [ ] All sections of the template filled in
- [ ] Table of contents matches actual sections (if applicable)
- [ ] All tables have data in every cell (no empty rows)
- [ ] Next steps clearly defined
- [ ] Timeline or priority order provided
- [ ] Appendix includes raw data or supporting details (where relevant)

---

## 5. Client Relevance

- [ ] Client name and site URL correctly referenced
- [ ] Recommendations match client's industry/vertical
- [ ] CMS/platform constraints considered (don't recommend what they can't do)
- [ ] Budget reality considered
- [ ] Competitors are the client's ACTUAL competitors (verified)
- [ ] Brand voice followed (for content deliverables)
- [ ] Goals align with client's stated objectives from `vault/01-Clients/[client]/goals.md`

---

## 6. Content Quality (for content deliverables only)

- [ ] Natural keyword integration (no stuffing)
- [ ] Proper heading hierarchy (one H1, logical H2/H3 nesting)
- [ ] Short paragraphs (3-4 sentences max)
- [ ] Bullet/numbered lists where appropriate
- [ ] Internal link suggestions included
- [ ] External links to authoritative sources included
- [ ] Meta title ≤60 characters with primary keyword
- [ ] Meta description ≤155 characters with CTA
- [ ] Image alt text suggestions included
- [ ] FAQ section with schema markup (where applicable)

---

## 7. Vault Integration

- [ ] Frontmatter present and complete:
  ```yaml
  ---
  client: "client-slug"
  agent: "agent-name"
  team: "team-name"
  date: YYYY-MM-DD
  type: [audit|keywords|content|links|report|strategy|aeo|competitor]
  status: complete
  quality-score: X/5
  ---
  ```
- [ ] Saved to correct vault location
- [ ] Saved to output folder: `output/[client]/[date]/`
- [ ] Tagged appropriately (#audit, #keywords, #content, etc.)
- [ ] Linked with `[[wikilinks]]` to related documents
- [ ] Dashboard updated (if significant deliverable)
- [ ] ROI tracker updated (if applicable)

---

## Scoring Guide

### 5/5 — Exceptional
All checks pass. Agency-grade. Ready for client presentation without edits. Includes unexpected insights.

### 4/5 — Strong
Nearly all checks pass. Professional quality. May need minor formatting polish. Strong client value.

### 3/5 — Acceptable (Minimum to deliver)
Most checks pass. Core value is there. Some areas could be more specific or detailed. Adequate for delivery.

### 2/5 — Below Standard
Multiple checks fail. Generic advice, missing specifics, or incomplete sections. Must revise before delivery.

### 1/5 — Unacceptable
Fundamental failures. Hallucinated data, entirely generic, or missing critical sections. Start over.

---

## Decision

| Score | Action |
|-------|--------|
| 5/5 | Save and deliver |
| 4/5 | Save and deliver |
| 3/5 | Save and deliver (note areas for improvement) |
| 2/5 | **Revise** weakest areas, then re-score |
| 1/5 | **Redo** the deliverable from scratch |
