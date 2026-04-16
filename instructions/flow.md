# Agency Workflow Flow

## The SEO Pipeline

Every client engagement follows this six-phase pipeline. Each phase has specific inputs, teams, and outputs.

```
┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐
│ PHASE 1  │──→│ PHASE 2  │──→│ PHASE 3  │──→│ PHASE 4  │──→│ PHASE 5  │──→│ PHASE 6  │
│ ONBOARD  │   │ RESEARCH │   │ AUDIT    │   │ STRATEGY │   │ EXECUTE  │   │ REPORT   │
└──────────┘   └──────────┘   └──────────┘   └──────────┘   └──────────┘   └──────────┘
      │              │              │              │              │              │
   Client         Intelligence   All teams      Strategy       Execution     Audit &
   Profile        Layer runs     contribute      Team sets      Layer does    Analytics
   Created        first          findings        priorities     the work      compile
```

---

## Phase 1: Onboard
**Input:** New client
**Teams:** None (CLAUDE.md handles)
**Process:**
1. Run `onboarding/onboard.md`
2. Interview client about business, SEO history, goals
3. Create client folder in `vault/01-Clients/[company]/`
4. Save 5 files: profile.md, site-info.md, competitors.md, goals.md, brand-voice.md
**Output:** Complete client profile in vault

---

## Phase 2: Research (Intelligence Layer)
**Input:** Client profile
**Teams:** Research → Competitor Analysis → Keyword Research
**Process:**
1. **Research Team** runs first — market context, industry trends, algorithm awareness
2. **Competitor Analysis Team** — crawl competitor sites, extract their strategies
3. **Keyword Research Team** — discover keywords, classify intent, build clusters, find gaps
**Output:** Intelligence data saved to vault (03-Research/, 06-Competitors/)

### Execution Order Within Phase 2
```
Research Team (general intel)
     │
     ├──→ Competitor Analysis (needs market context)
     │         │
     └────────→ Keyword Research (needs competitor data + market context)
```

---

## Phase 3: Audit (All Teams Contribute)
**Input:** Intelligence data + site access
**Teams:** Technical, Content, Links, AEO, Local*, E-commerce*
**Process:**
1. **Technical SEO** — Crawl site, check indexation, Core Web Vitals, schema, internal links, mobile
2. **Content SEO** — Audit existing content, find gaps, assess quality
3. **Link Building** — Audit backlink profile, identify toxic links
4. **AEO** — Audit AI search presence, entity coverage, citation status
5. **Local SEO** — Audit GBP, citations, local rankings (if applicable)
6. **E-commerce SEO** — Audit product pages, categories, feeds (if applicable)
**Output:** Individual team findings saved to vault (02-Audits/)

*Local and E-commerce only run if applicable to client

### Execution Order Within Phase 3
```
Technical SEO (crawl first — other teams need crawl data)
     │
     ├──→ Content SEO (needs URL inventory from crawl)
     ├──→ Link Building (can run parallel with content)
     ├──→ AEO (can run parallel)
     ├──→ Local SEO (can run parallel, if applicable)
     └──→ E-commerce SEO (needs crawl data, if applicable)
```

---

## Phase 4: Strategy (Compile + Prioritize)
**Input:** All audit findings + intelligence data
**Teams:** Audit & Recommendations → Strategy & Direction
**Process:**
1. **Audit & Recommendations Team** — Compile ALL findings into one master report
   - Data Compiler pulls from every team's vault output
   - Recommendation Engine converts findings to actionable fixes
   - Fix Generator writes specific implementation instructions
   - Report Builder assembles the document
   - Executive Summary Writer creates the client-facing summary
2. **Strategy & Direction Team** — Build priority matrix and roadmap
   - Priority Matrix Builder scores every issue by Impact × Effort
   - Roadmap Planner creates 3/6/12 month plan
   - Client Communication Manager translates to business language
**Output:** Master SEO Audit Report + Priority Matrix + Roadmap

---

## Phase 5: Execute (Monthly Sprints)
**Input:** Prioritized roadmap
**Teams:** Technical, Content, Links, AEO, Local, E-commerce
**Process:** Execute the highest-priority items from the roadmap each month

### Monthly Sprint Structure
```
Week 1: Technical fixes (highest-priority crawl/index/speed issues)
Week 2: Content creation (briefs → writing → optimization)
Week 3: Link building (prospecting → outreach → follow-up)
Week 4: AEO + Local + E-commerce optimizations

Throughout: Monitor changes, track progress, adjust priorities
```

**Output:** Completed work logged to vault, results tracked

---

## Phase 6: Report (Monthly + Quarterly)
**Input:** Execution results + analytics data
**Teams:** Analytics & Reporting → Strategy & Direction
**Process:**
1. **Analytics Team** — Pull ranking data, traffic data, conversion data
2. **Monthly Report Writer** — Compile into professional report
3. **ROI Calculator** — Calculate month's SEO ROI
4. **Strategy Team** — Review results, adjust next month's priorities
**Output:** Monthly SEO Report + ROI Analysis

### Quarterly Cycle
Every 3 months, run a deeper review:
1. Quarter-over-quarter performance analysis
2. Re-run competitor analysis (competitors change)
3. Re-audit technical foundation (sites change)
4. Update roadmap for next quarter
5. Executive quarterly summary

---

## Flow Rules

1. **Never skip phases** — Even for "quick" requests, follow the flow
2. **Intelligence before execution** — Always research before doing
3. **Vault is the bridge** — Teams don't talk to each other directly; they read/write vault
4. **Quality gate at every phase exit** — Not just at the end
5. **Client profile is the anchor** — Every decision references the client profile
6. **Feedback loops are mandatory** — Phase 6 output feeds back into Phase 4 priorities

---

## Handling Partial Requests

Not every request needs the full pipeline. Here's how to handle common partial requests:

| Request | Start At | End At |
|---------|----------|--------|
| "Audit my site" | Phase 2 (Research) | Phase 4 (Report) |
| "Write me 5 blog posts" | Phase 2 (Keywords) | Phase 5 (Execute) |
| "Check my competitors" | Phase 2 (Competitor Analysis) | Phase 4 (Report) |
| "Fix my technical SEO" | Phase 3 (Technical Audit) | Phase 5 (Execute) |
| "Monthly report" | Phase 6 (Report) | Phase 6 (Report) |
| "Build links" | Phase 2 (Competitor Backlinks) | Phase 5 (Execute) |
| "Optimize for AI search" | Phase 2 (Research + Keywords) | Phase 5 (Execute) |

Even for partial requests:
- Always check vault for existing client data first
- Always run quality gate on output
- Always save to vault and output folder
