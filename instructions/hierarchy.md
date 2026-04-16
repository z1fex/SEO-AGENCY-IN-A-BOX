# Agency Hierarchy & Chain of Command

## Three Layers

Every engagement flows through three layers in strict order. Never skip a layer.

### Layer 1: Intelligence (Research First)
**Teams:** Research, Competitor Analysis, Keyword Research
**Purpose:** Gather all data before anyone does anything

These teams run BEFORE any execution work begins. They provide the foundation that every other team builds on. Without intelligence, execution is guesswork.

**What they produce:**
- Market and industry context
- Algorithm update awareness
- Competitor site crawls, keyword targets, content strategies, link profiles
- Keyword discovery, intent mapping, clusters, gaps, SERP features
- AI search landscape analysis

**Rule:** No execution team starts until at least one intelligence team has provided relevant data.

### Layer 2: Execution (Do the Work)
**Teams:** Technical SEO, Content SEO, Link Building, AEO, Local SEO, E-commerce SEO
**Purpose:** Act on intelligence to optimize, create, and build

These teams consume intelligence data and produce work:
- Technical fixes and improvements
- Content pieces (briefs, articles, meta tags, FAQs)
- Link building campaigns and outreach
- AEO optimization for AI search engines
- Local SEO setup and optimization
- E-commerce product/category optimization

**Rule:** Every execution action must reference the intelligence that justified it. No action without data.

### Layer 3: Output (Compile & Deliver)
**Teams:** Audit & Recommendations, Analytics & Reporting
**Purpose:** Take ALL findings from ALL teams and produce client-ready deliverables

The Audit & Recommendations team is the funnel. Every team's findings flow INTO this team, and ONE unified report flows OUT. This is what clients receive.

Analytics & Reporting tracks ongoing performance and proves ROI over time.

**Rule:** Raw team outputs are internal. Only Audit & Recommendations compiled reports go to clients.

### Strategy & Direction (Overarching)
**Team:** Strategy & Direction
**Purpose:** Sets goals, priorities, and roadmaps that guide all three layers

This team operates across all layers:
- Before intelligence: defines what to research
- After intelligence: sets priorities based on findings
- During execution: ensures work aligns with goals
- After output: reviews results and adjusts strategy

---

## Decision Flow

```
Client Request
     │
     ▼
CLAUDE.md (Brain) ──→ Which workflow/team to run?
     │
     ▼
Strategy Team ──→ What are the goals and priorities?
     │
     ▼
Intelligence Layer ──→ What does the data say?
├── Research Team ──→ Market context, trends, algorithm updates
├── Competitor Team ──→ What are competitors doing?
└── Keywords Team ──→ What are people searching for?
     │
     ▼
Execution Layer ──→ Do the work based on data
├── Technical ──→ Fix the site foundation
├── Content ──→ Create and optimize content
├── Links ──→ Build authority
├── AEO ──→ Optimize for AI search
├── Local ──→ Local search presence
└── E-commerce ──→ Product/category optimization
     │
     ▼
Output Layer ──→ Compile and deliver
├── Audit & Recs ──→ Master report with all findings + fixes
└── Analytics ──→ Performance tracking and ROI
     │
     ▼
Quality Gate ──→ Pass? → Deliver to client
                 Fail? → Revise and recheck
```

---

## Team Dependencies

| Team | Depends On | Feeds Into |
|------|-----------|------------|
| Research | Client profile | All teams |
| Competitor Analysis | Client profile, Research | Keywords, Content, Links, Strategy |
| Keyword Research | Research, Competitor Analysis | Content, AEO, Local, E-commerce, Strategy |
| Technical SEO | Client site access | Audit & Recs |
| Content SEO | Keywords, Competitor Analysis | Audit & Recs, Links |
| Link Building | Competitor Analysis, Content | Audit & Recs |
| AEO | Keywords, Research, Content | Audit & Recs |
| Local SEO | Keywords, Client profile | Audit & Recs |
| E-commerce SEO | Keywords, Technical | Audit & Recs |
| Audit & Recs | ALL teams above | Client deliverable |
| Analytics & Reporting | All team outputs, vault data | Strategy, Client |
| Strategy & Direction | Analytics, Research, Competitor | All teams (sets direction) |

---

## Escalation Rules

1. **Data conflict** — If two teams produce conflicting data, escalate to Strategy & Direction
2. **Resource constraint** — If a team needs data from another team that hasn't run yet, run the dependency first
3. **Quality failure** — If a deliverable fails quality gate, return to the originating team for revision
4. **Client constraint** — If a recommendation is infeasible (CMS limitation, budget, etc.), flag it and provide alternatives
