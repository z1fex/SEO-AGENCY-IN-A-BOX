# Quality Standards

## The Quality Promise

Every deliverable from this agency must be indistinguishable from what a $150/hr SEO consultant would produce. Generic advice, hallucinated data, and vague recommendations are failures.

---

## Five Quality Pillars

### 1. Data Accuracy (Non-Negotiable)
Every number, keyword, metric, and claim must come from a verifiable source.

**Acceptable sources:**
- Firecrawl crawl/scrape results (actual site data)
- Tavily search results (real search data)
- Web Fetch page validation (live page checks)
- Web Search results (verifiable information)
- Client-provided data (analytics, Search Console)
- Industry benchmarks from authoritative sources

**Never acceptable:**
- Made-up search volumes
- Invented competitor data
- Estimated metrics without labeling them as estimates
- "Common knowledge" claims without verification
- Traffic numbers without a source
- Rankings you haven't checked

**Rule:** If you can't verify it with a tool, don't include it. Say "data not available — recommend checking [specific tool]" instead.

### 2. Specificity (No Generic Advice)
Every recommendation must include:
- **What** specifically to change
- **Where** exactly to change it (URL, page, element)
- **How** to implement the change (step-by-step)
- **Why** this matters (expected impact)
- **Priority** level (critical, high, medium, low)

**Bad example:**
> "Improve your page speed."

**Good example:**
> "**Page: /products/widget-pro** — LCP is 4.2s (target: <2.5s). The hero image (widget-pro-banner.jpg, 2.4MB) is uncompressed. **Fix:** Convert to WebP format, resize to 1200px max width, add `loading="lazy"` attribute. **Expected impact:** LCP reduction to ~1.8s. **Priority:** Critical — this is your highest-traffic product page."

### 3. Current SEO Practices
All recommendations must align with current Google guidelines and industry best practices.

**Do recommend:**
- E-E-A-T signals (author bios, credentials, cited sources)
- Search intent alignment (match content type to query intent)
- Topical authority (comprehensive coverage of a topic cluster)
- Core Web Vitals optimization
- Structured data (JSON-LD schema)
- Mobile-first design
- AEO (Answer Engine Optimization) for AI search
- Natural language and entity optimization

**Never recommend:**
- Keyword density targets (e.g., "use keyword 3% of the time")
- Exact-match anchor text manipulation
- PBN (Private Blog Network) links
- Keyword stuffing in meta tags
- Hidden text or cloaking
- Link schemes or paid links (without nofollow)
- Article spinning or thin content at scale
- Any technique that risks a Google penalty

### 4. Completeness
Every deliverable must be:
- **Finished** — No placeholder text, no "TBD", no "[insert here]"
- **Self-contained** — Reader doesn't need to ask for clarification
- **Actionable** — Every issue has a fix, every recommendation has steps
- **Prioritized** — Issues ranked by impact and effort
- **Formatted** — Professional structure with clear headings, tables, and sections

### 5. Client Relevance
Every deliverable must be tailored to the specific client:
- **Industry context** — Recommendations fit their vertical
- **Business size** — Enterprise SEO differs from small business SEO
- **CMS capabilities** — Don't recommend changes their CMS can't support
- **Budget reality** — Don't recommend $10K solutions for $1K budgets
- **Competitive landscape** — Based on their actual competitors, not generic ones

---

## Quality Scoring Rubric

### 5/5 — Exceptional (Agency-Grade)
- All data verified from real sources
- Every recommendation is specific, actionable, and prioritized
- Professional formatting with executive summary
- Client-specific insights that show deep understanding
- Includes unexpected opportunities the client didn't ask about
- Ready for direct client presentation without edits

### 4/5 — Strong (Professional)
- Data is accurate and sourced
- Recommendations are specific and actionable
- Good formatting and structure
- Client-relevant with minimal generic content
- May need minor polish for client presentation

### 3/5 — Acceptable (Minimum to Deliver)
- Data is mostly accurate with sources
- Most recommendations are specific
- Adequate formatting
- Reasonably client-specific
- Needs some refinement but core value is there

### 2/5 — Below Standard (Needs Revision)
- Some data unverified or questionable
- Recommendations are too generic
- Formatting inconsistent
- Not sufficiently tailored to client
- Must be revised before delivery

### 1/5 — Unacceptable (Redo Required)
- Hallucinated or unsourced data
- Generic advice that could apply to anyone
- Poor formatting or incomplete sections
- Not client-specific at all
- Start over from scratch

**Minimum to deliver: 3/5**
**Target for all work: 4/5+**

---

## Quality Gate Process

1. **Self-check** — Agent reviews own output against these standards
2. **Checklist run** — Apply `quality/qa-checklist.md` item by item
3. **Score** — Assign a quality score (1-5)
4. **Decision:**
   - Score 3+ → Save to vault + output, mark complete
   - Score 2 → Revise the weakest areas, re-score
   - Score 1 → Redo the deliverable from scratch
5. **Log** — Record the quality score in the deliverable's frontmatter

---

## Common Quality Failures and How to Avoid Them

| Failure | Cause | Fix |
|---------|-------|-----|
| Hallucinated search volumes | No Tavily/tool check | Always search before claiming volume |
| Generic recommendations | Didn't read client profile | Read vault/01-Clients/ before every task |
| Outdated SEO advice | Using old knowledge | Verify practices against current guidelines |
| Missing priorities | Didn't score issues | Always assign Impact × Effort to every finding |
| Incomplete report | Rushed through steps | Follow agent instructions step by step |
| Wrong competitors | Assumed instead of researched | Use Firecrawl to verify competitor sites |
| Unactionable fixes | Too high-level | Include specific code, copy, or config changes |
