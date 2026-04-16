# Audit & Recommendations Team

> Compile ALL findings from ALL teams into ONE unified master report with prioritized recommendations, specific fix instructions, and an executive summary — this is THE deliverable clients receive.

## Team Overview

The Audit & Recommendations Team is the most important output team in the agency. Every other team generates internal findings — raw audit data, keyword lists, competitor crawls, technical issues, content gaps, link profiles, AEO opportunities. None of those internal outputs go directly to clients. This team is the funnel: all data flows IN from every team, and ONE polished, prioritized, actionable master report flows OUT. This is what the client pays for. This is the deliverable that drives decisions, justifies budgets, and demonstrates the agency's value.

This team sits in the **Output Layer** of the agency hierarchy. It runs during Phase 4 (Strategy), after all intelligence and execution teams have completed their work. The team does not perform any original research, crawling, or auditing — that is the job of the other 11 teams. Instead, this team reads everything those teams produced, identifies the most impactful findings, converts them into prioritized recommendations with specific fix instructions, assembles them into a professional report structure, and writes an executive summary that non-technical stakeholders can understand and act on.

The team follows a strict compilation pipeline. The Data Compiler reads all team outputs from the vault and organizes raw findings by category and impact. The Recommendation Engine converts findings into actionable recommendations with clear priority scores. The Fix Generator writes specific, implementable fix instructions for every recommendation. The Report Builder assembles everything into a structured, professional report with clear sections, tables, and visual hierarchy. The Executive Summary Writer produces the opening section that busy stakeholders read first — and sometimes only.

## Agents

| Agent | File | Role |
|-------|------|------|
| Data Compiler | `agents/audit/data-compiler.md` | Reads ALL team outputs from the vault, deduplicates overlapping findings, categorizes issues by type (technical, content, links, AEO, local, e-commerce), and scores each finding by severity and impact |
| Recommendation Engine | `agents/audit/recommendation-engine.md` | Converts compiled findings into actionable recommendations — each with a clear problem statement, recommended action, expected impact, priority level, and effort estimate |
| Fix Generator | `agents/audit/fix-generator.md` | Writes specific, implementable fix instructions for every recommendation — exact code changes, copy edits, configuration steps, or process changes that the client's team can execute |
| Report Builder | `agents/audit/report-builder.md` | Assembles all recommendations, fixes, and supporting data into a structured, professional report with clear sections, summary tables, priority matrices, and consistent formatting |
| Executive Summary Writer | `agents/audit/executive-summary-writer.md` | Writes the client-facing executive summary — translates technical SEO findings into business language, highlights the top 5-10 highest-impact opportunities, and provides a clear recommended action plan |

## When to Run This Team

- **After a full site audit** — This is the primary trigger. After all audit teams have completed their work, this team compiles the master report
- **After any multi-team engagement** — Whenever more than two teams have produced findings, this team compiles them into a unified deliverable
- **Quarterly report compilation** — At the end of each quarter, compile all quarterly findings into a comprehensive review report
- **Strategy presentation preparation** — When the agency needs to present findings and recommendations to client stakeholders
- **Post-execution review** — After executing a round of fixes, compile a "what was done, what changed, what is next" report
- **Never run for:** Single-agent tasks (one blog post, one keyword check), ongoing monitoring updates, or internal team-to-team data transfers

## Execution Order

```
Step 1: Data Compiler (MANDATORY FIRST)
   │
   │  Reads ALL team outputs from the vault:
   │  - vault/03-Research/[client]/ (Research team findings)
   │  - vault/03-Research/[client]/ (Keyword research data)
   │  - vault/06-Competitors/[client]/ (Competitor analysis)
   │  - vault/10-Technical/[client]/ (Technical SEO audit)
   │  - vault/04-Content/[client]/ (Content SEO findings)
   │  - vault/05-Links/[client]/ (Link building audit)
   │  - vault/11-AEO/[client]/ (AEO audit findings)
   │  - vault/09-Local/[client]/ (Local SEO, if applicable)
   │  - vault/10-Technical/[client]/faceted-nav-audit.md (E-commerce, if applicable)
   │
   │  Deduplicates overlapping findings (e.g., schema issues found
   │  by both Technical SEO and AEO teams). Categorizes all issues.
   │  Scores each finding by severity (Critical/High/Medium/Low) and
   │  estimated effort (Easy/Medium/Hard).
   │  Saves to vault/02-Audits/[client]/compiled-findings.md
   │
   ▼
Step 2: Recommendation Engine
   │
   │  Reads the compiled findings and converts each into a structured
   │  recommendation. Each recommendation includes:
   │  - Problem statement (what is wrong and why it matters)
   │  - Recommended action (what to do about it)
   │  - Expected impact (what will improve and by how much)
   │  - Priority score: Impact (1-5) x Effort (1-5) = Priority
   │  - Category tag (technical, content, links, aeo, local, ecommerce)
   │  - Dependencies (does this fix depend on another fix?)
   │  
   │  Sorts recommendations by priority score (highest impact, lowest
   │  effort first). Groups into Quick Wins, High-Priority, Medium-
   │  Priority, and Long-Term categories.
   │  Saves to vault/02-Audits/[client]/recommendations.md
   │
   ▼
Step 3: Fix Generator
   │
   │  Takes each recommendation and writes specific, implementable
   │  fix instructions. For technical issues: exact code, markup, or
   │  configuration changes. For content issues: specific copy edits,
   │  structural changes, or content outlines. For link issues: specific
   │  outreach targets and approaches. For AEO issues: specific content
   │  restructuring with before/after examples.
   │  
   │  Every fix must be detailed enough that a developer, content writer,
   │  or SEO specialist can implement it without asking follow-up
   │  questions.
   │  Saves to vault/02-Audits/[client]/fix-instructions.md
   │
   ▼
Step 4: Report Builder
   │
   │  Assembles the complete master report from compiled findings,
   │  recommendations, and fix instructions. Structures the report
   │  with clear sections:
   │  1. Executive Summary (placeholder — filled by Step 5)
   │  2. Priority Matrix (Impact x Effort grid)
   │  3. Quick Wins (implement immediately)
   │  4. Technical SEO Findings & Fixes
   │  5. Content SEO Findings & Fixes
   │  6. Link Profile Analysis & Recommendations
   │  7. AEO / AI Search Findings & Fixes
   │  8. Local SEO Findings (if applicable)
   │  9. E-commerce SEO Findings (if applicable)
   │  10. Competitive Landscape Summary
   │  11. Keyword Opportunity Analysis
   │  12. Implementation Roadmap
   │  13. Appendix (raw data, supporting evidence)
   │  
   │  Saves to output/[client]/[date]/audit/master-seo-report.md
   │
   ▼
Step 5: Executive Summary Writer
   │
   │  Reads the complete report and writes the executive summary.
   │  This is the most important section of the entire report — many
   │  stakeholders will only read this section. It must:
   │  - State the overall SEO health score (1-10)
   │  - Highlight the top 5-10 highest-impact findings
   │  - Summarize the competitive position in plain language
   │  - Present estimated traffic and revenue opportunity
   │  - Provide a clear "do this first" action plan (top 3 quick wins)
   │  - Use business language, not technical jargon
   │  
   │  Inserts the executive summary into the master report (Section 1)
   │  and saves a standalone version for presentation use.
   │  Saves to output/[client]/[date]/audit/executive-summary.md
   │  Updates master report at output/[client]/[date]/audit/master-seo-report.md
```

**Data flow:** The Data Compiler is the intake — it reads from every vault location where other teams save their work. Each subsequent agent adds a layer of analysis and polish. The final output is two files: the master report (comprehensive) and the executive summary (concise). The master report is the definitive deliverable; the executive summary is the presentation-ready version.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Vault | Read (all team folders) | Primary input — reads ALL findings from ALL teams across the entire vault |
| File processing | Read + Write | Reads multiple vault files, processes data, writes compiled reports |
| Tavily | `search` | Occasionally used to verify findings or check current SERP status for specific recommendations |
| Web Fetch | Page validation | Occasionally used to verify that a reported issue still exists before including it in the final report |

### Tool Usage Protocol

1. **Read comprehensively** — The Data Compiler must read EVERY relevant vault file for the client, not just the most recent ones. Check all vault folders listed in the execution order
2. **Never skip a team's output** — If a team ran and saved findings, those findings must appear in the compiled report. Missing a team's work is a quality failure
3. **Verify critical findings** — For Critical-priority findings, use Web Fetch or Tavily to verify the issue still exists before publishing in the report. Issues may have been fixed between team execution and report compilation
4. **No original research** — This team compiles and analyzes. If research is needed, send it back to the appropriate team. The Audit team reads, scores, organizes, and writes — it does not crawl, search, or discover
5. **Use templates** — Follow the report structure defined in Step 4 for consistency across all client reports

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| At least one team's audit findings | Any vault team folder | Yes — there must be findings to compile |
| Technical SEO findings | `vault/10-Technical/[client]/` | Strongly recommended — technical issues are the foundation of most audits |
| Keyword research data | `vault/03-Research/[client]/` | Strongly recommended — keyword context makes recommendations more actionable |
| Competitor analysis | `vault/06-Competitors/[client]/` | Strongly recommended — competitive context makes the report more valuable |
| Content SEO findings | `vault/04-Content/[client]/` | Recommended |
| Link building findings | `vault/05-Links/[client]/` | Recommended |
| AEO findings | `vault/11-AEO/[client]/` | Recommended |
| Local SEO findings | `vault/09-Local/[client]/` | If applicable |
| Research intelligence | `vault/03-Research/[client]/` | Recommended — provides market context for the report |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Compiled Findings | `vault/02-Audits/[client]/compiled-findings.md` | All team findings deduplicated, categorized, and severity-scored (internal working document) |
| Recommendations | `vault/02-Audits/[client]/recommendations.md` | Prioritized recommendations with Impact x Effort scoring (internal working document) |
| Fix Instructions | `vault/02-Audits/[client]/fix-instructions.md` | Specific, implementable fixes for every recommendation (internal working document) |
| Master SEO Report | `output/[client]/[date]/audit/master-seo-report.md` | THE client deliverable — complete audit report with all findings, recommendations, fixes, and roadmap |
| Executive Summary | `output/[client]/[date]/audit/executive-summary.md` | Standalone executive summary for presentation to stakeholders |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "report-builder"
team: "audit-recommendations"
date: YYYY-MM-DD
type: audit-report
status: complete
teams-compiled: ["research", "competitor-analysis", "keyword-research", "technical-seo", "content-seo", "link-building", "aeo"]
total-findings: 0
critical-findings: 0
seo-health-score: 0
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - **ALL other teams that have run** — this team compiles their output. At minimum, one team must have produced findings. For a full audit report, the intelligence layer (Research, Competitor Analysis, Keywords) and execution layer (Technical, Content, Links, AEO) should all have completed
  - Client profile (must exist in vault)
  - The more teams that contribute findings, the more comprehensive the report

- **Feeds into:**
  - **Client** — this is the primary client deliverable
  - **Strategy & Direction Team** — the priority matrix and recommendations feed directly into roadmap planning
  - **Analytics & Reporting Team** — the audit baseline becomes the benchmark for future performance tracking
  - **All execution teams** (on re-engagement) — the fix instructions guide the next round of execution work

## Quality Checks

### Audit & Recommendations-Specific Quality Criteria

1. **Completeness of compilation** — Every team that produced findings must be represented in the report. The Data Compiler must confirm it read every relevant vault file. If a team's section is missing, the report is incomplete. Include a "Sources Compiled" section listing every vault file that was read.

2. **No duplicate findings** — When multiple teams identify the same issue (e.g., Technical SEO and AEO both find missing schema), it must appear once in the report with a note that multiple teams flagged it. Duplicates inflate the finding count and confuse clients.

3. **Consistent priority scoring** — Every finding must use the same Impact (1-5) x Effort (1-5) priority framework. Priority scores must be internally consistent: if a broken homepage redirect is scored as Critical, a broken 404 on a low-traffic blog post cannot also be Critical. The Recommendation Engine must calibrate scores across the entire finding set.

4. **Implementable fix instructions** — Every recommendation must have a specific fix. "Fix your page speed" is unacceptable. "Compress hero image on /products/widget-pro from 2.4MB PNG to WebP format (target: <200KB), add width/height attributes to prevent CLS, and defer non-critical JavaScript using the `defer` attribute" is acceptable. The Fix Generator must provide instructions detailed enough for implementation without follow-up questions.

5. **Executive summary independence** — The executive summary must be understandable without reading the full report. A stakeholder who reads only the executive summary must walk away knowing: overall SEO health, top 5 issues, competitive position, estimated opportunity, and what to do first. No jargon. No acronyms without definitions. Business language only.

6. **Evidence for every finding** — Every finding must include the evidence source: which tool produced the data, which URL was checked, what the specific metric or value is. "Your site is slow" has no evidence. "Your homepage LCP is 4.2s (measured via Firecrawl scrape on 2026-04-10, target: <2.5s)" has evidence.

7. **Realistic effort estimates** — Effort estimates must account for the client's technical capabilities and resources. A fix that takes 5 minutes for a developer with server access takes much longer for a client on a managed CMS with no code access. When possible, note effort variations by implementation context.

8. **Professional formatting** — The report must use consistent heading hierarchy, table formatting, and visual structure. Findings must be organized logically (by priority, by category, or by implementation phase). The report must be presentable to a client without reformatting.

9. **Roadmap included** — The report must end with a recommended implementation roadmap that sequences the fixes in logical order (quick wins first, then high-priority items, then medium-term projects, then long-term initiatives). The roadmap must account for dependencies (e.g., fix crawl budget issues before worrying about content optimization for filtered pages).

10. **Minimum quality score: 4/5. Target: 5/5.** (Higher bar than other teams — this is the client-facing deliverable.)
