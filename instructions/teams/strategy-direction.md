# Strategy & Direction Team

> Set the strategic direction for every engagement by building priority matrices, creating SEO roadmaps, developing competitive strategies, and translating technical SEO into business language that drives client decisions.

## Team Overview

The Strategy & Direction Team is the brain that operates across all layers of the agency. While other teams are specialists — deep in technical audits, keyword data, or content creation — this team sees the full picture and makes the decisions that determine what gets done, in what order, and why. It translates the mountain of data produced by intelligence and execution teams into a clear strategic direction: what matters most, what to do first, what to defer, and what to ignore. Without this team, the agency produces a pile of findings with no coherent plan. With this team, the agency produces a prioritized roadmap that clients can execute with confidence.

This team does not sit in a single layer — it operates across all three. Before the intelligence layer runs, the SEO Strategist defines what to research and why. After the intelligence and execution teams produce findings, the Priority Matrix Builder scores every issue and the Competitive Strategy Analyst positions the client against competitors. The SEO Roadmap Planner sequences everything into a time-bound implementation plan. The Client Communication Manager translates the entire strategy into language that non-technical stakeholders understand and approve. This team sets the goals, checks the results, and adjusts the course.

The team follows a strategic cascade. The SEO Strategist sets the high-level strategic direction based on client goals, market position, and available data. The Priority Matrix Builder applies the Impact x Effort framework to every recommendation, creating the decision matrix that drives resource allocation. The Competitive Strategy Analyst layers in competitive positioning to ensure the strategy accounts for what competitors are doing. The Roadmap Planner translates priorities into a phased implementation timeline. The Client Communication Manager packages everything in business terms for stakeholder buy-in.

## Agents

| Agent | File | Role |
|-------|------|------|
| SEO Strategist | `agents/strategy/seo-strategist.md` | Defines the overarching SEO strategy based on client goals, market position, competitive landscape, and available data — sets the vision that all other decisions cascade from |
| Priority Matrix Builder | `agents/strategy/priority-matrix-builder.md` | Scores every recommendation and opportunity using the Impact (1-5) x Effort (1-5) framework, categorizes them into Quick Wins, High-Priority, Medium-Priority, and Long-Term, and creates the decision matrix |
| Competitive Strategy Analyst | `agents/strategy/competitive-strategy-analyst.md` | Develops the competitive SEO strategy — identifies where the client can win, where they should defend, where to flank competitors, and where to concede — based on competitive intelligence data |
| SEO Roadmap Planner | `agents/strategy/roadmap-planner.md` | Creates phased 3-month, 6-month, and 12-month SEO roadmaps with specific milestones, deliverables, resource requirements, and success metrics for each phase |
| Client Communication Manager | `agents/strategy/client-communication-manager.md` | Translates technical SEO strategy, findings, and recommendations into clear business language for client stakeholders — creates presentation-ready strategy decks, meeting agendas, and talking points |

## When to Run This Team

- **New client onboarding** — Run the SEO Strategist after the intelligence layer to set the initial strategic direction
- **After full audit completion** — Run the complete team after the Audit & Recommendations team compiles the master report, to build the priority matrix and roadmap
- **Quarterly strategy review** — Re-run quarterly to adjust strategy based on performance data from the Analytics team
- **Major ranking shift** — When significant ranking gains or losses require a strategy adjustment
- **Client goal change** — When the client's business goals shift (new market, new product line, pivot)
- **Competitive landscape shift** — When a new competitor enters the market or an existing competitor makes a major move
- **Budget change** — When the client's SEO budget increases or decreases, the roadmap must be re-prioritized
- **Before client meetings** — Run the Client Communication Manager before any strategy presentation or quarterly business review
- **Annual planning** — At year-end, develop the next year's SEO roadmap with 4 quarterly phases
- **Post-execution review** — After a month of execution work, review results against strategy and adjust

## Execution Order

```
Step 1: SEO Strategist
   │
   │  Reads all available data: client profile, goals, intelligence
   │  team outputs (research, competitor analysis, keyword data),
   │  execution team findings (technical, content, links, AEO), and
   │  performance data (if available). Defines the overarching SEO
   │  strategy: what the client's SEO strengths and weaknesses are,
   │  where the biggest opportunities lie, what the competitive
   │  advantages and disadvantages are, and what the strategic
   │  priorities should be.
   │  Saves to vault/08-Strategy/[client]/seo-strategy.md
   │
   ▼
Step 2: Priority Matrix Builder
   │
   │  Takes all recommendations from the Audit & Recommendations team
   │  and all opportunities identified across teams. Scores each using:
   │  - Impact (1-5): How much will this move the needle?
   │  - Effort (1-5): How much time/resource does this require?
   │  - Priority = Impact x Effort score (with high impact + low
   │    effort = highest priority)
   │
   │  Categorizes into four quadrants:
   │  - Quick Wins (High Impact, Low Effort) — do first
   │  - High Priority (High Impact, High Effort) — plan and execute
   │  - Medium Priority (Lower Impact, Low Effort) — batch and do
   │  - Long-Term (High Impact, Very High Effort) — plan strategically
   │  - Deprioritized (Low Impact, High Effort) — defer or eliminate
   │  
   │  Saves to vault/08-Strategy/[client]/priority-matrix.md
   │
   ▼
Step 3: Competitive Strategy Analyst
   │
   │  Reads competitive intelligence from vault/06-Competitors/ and
   │  the SEO strategy from Step 1. Develops the competitive SEO
   │  positioning:
   │  - Domains to ATTACK (client can outrank competitors with effort)
   │  - Domains to DEFEND (client leads but competitors are gaining)
   │  - Domains to FLANK (find uncontested keyword spaces)
   │  - Domains to CONCEDE (competitor is too strong; invest elsewhere)
   │
   │  Maps competitive strategy to specific keyword clusters and
   │  content areas. Identifies the competitive moats to build.
   │  Saves to vault/08-Strategy/[client]/competitive-strategy.md
   │
   ▼
Step 4: SEO Roadmap Planner
   │
   │  Takes the strategy, priority matrix, and competitive positioning
   │  to build phased implementation roadmaps:
   │
   │  Month 1-3 (Foundation):
   │  - Quick Wins from priority matrix
   │  - Critical technical fixes
   │  - Baseline content and AEO optimization
   │
   │  Month 4-6 (Growth):
   │  - High-priority content creation
   │  - Link building campaigns
   │  - Advanced AEO optimization
   │
   │  Month 7-12 (Scale):
   │  - Topical authority building
   │  - Long-term competitive positioning
   │  - Advanced optimization and expansion
   │
   │  Each phase includes: specific tasks, responsible teams, success
   │  metrics, resource requirements, and dependencies.
   │  Saves to vault/08-Strategy/[client]/seo-roadmap.md
   │
   ▼
Step 5: Client Communication Manager
   │
   │  Takes the strategy, priority matrix, competitive positioning,
   │  and roadmap and translates them into client-ready materials:
   │  - Strategy summary in plain business language (no jargon)
   │  - Priority matrix visualization (text-based quadrant grid)
   │  - Roadmap timeline with milestones and expected outcomes
   │  - Talking points for the strategy presentation
   │  - FAQ responses for anticipated client questions
   │  - ROI projections tied to roadmap phases
   │
   │  This agent ensures the client understands and approves the
   │  strategy before execution begins.
   │  Saves to output/[client]/[date]/strategy/strategy-presentation.md
```

**Data flow:** The SEO Strategist sets the direction. The Priority Matrix Builder quantifies the order. The Competitive Strategy Analyst ensures the strategy accounts for the competitive landscape. The Roadmap Planner sequences everything in time. The Client Communication Manager makes it presentable and actionable for the client. Each agent builds on the previous one, and the final output is both internally actionable (the roadmap guides execution teams) and externally presentable (the strategy presentation earns client buy-in).

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Vault | Read (all folders) | Primary input — reads client profile, all team outputs, performance data, competitive intelligence, audit findings |
| Tavily | `search` | Occasional research — verify market sizing data, check current competitive landscape, research industry benchmarks for goal-setting |
| Web Search | General research | Look up industry benchmarks, SEO budget norms, competitive landscape context |
| File processing | Read + Write | Process vault data, build priority matrices, create roadmap documents |

### Tool Usage Protocol

1. **Read comprehensively before strategizing** — The SEO Strategist must read the client profile, goals, all available intelligence data, and all available audit findings before forming the strategy. Strategy built on partial data is partial strategy
2. **Do not re-research** — This team synthesizes and strategizes based on existing data. If new research is needed, send it to the Research or Competitor Analysis team. The Strategy team reads vault; it does not crawl or discover
3. **Use Tavily sparingly** — Only for verifying specific data points needed for strategy (e.g., industry benchmark metrics, market sizing validation). The heavy research lifting is done by other teams
4. **Save all strategy documents to vault/08-Strategy/** — strategy is living documentation that evolves with each quarterly review
5. **Version strategy documents** — when updating a strategy, save the new version alongside the old one (date-stamped) so the evolution of strategy is traceable

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Client goals | `vault/01-Clients/[client]/goals.md` | Yes — strategy must align with business goals |
| Audit findings / recommendations | `vault/02-Audits/[client]/` | Strongly recommended — the priority matrix is built from audit findings |
| Keyword research data | `vault/03-Research/[client]/` | Strongly recommended — keyword opportunities drive strategy |
| Competitor analysis | `vault/06-Competitors/[client]/` | Strongly recommended — competitive positioning requires competitive data |
| Research intelligence | `vault/03-Research/[client]/` | Recommended — market context informs strategic direction |
| Performance data | `vault/07-Reports/[client]/` | Recommended (not available on first engagement — available for quarterly reviews) |
| Previous strategy documents | `vault/08-Strategy/[client]/` | Recommended — build on existing strategy rather than starting fresh |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| SEO Strategy | `vault/08-Strategy/[client]/seo-strategy.md` | Overarching strategic direction — strengths, weaknesses, opportunities, priorities, and strategic vision |
| Priority Matrix | `vault/08-Strategy/[client]/priority-matrix.md` | Impact x Effort scoring for all recommendations with quadrant categorization |
| Competitive Strategy | `vault/08-Strategy/[client]/competitive-strategy.md` | Competitive positioning — attack, defend, flank, and concede decisions mapped to keyword clusters |
| SEO Roadmap | `vault/08-Strategy/[client]/seo-roadmap.md` | Phased 3/6/12 month implementation plan with milestones, tasks, teams, and success metrics |
| Strategy Presentation | `output/[client]/[date]/strategy/strategy-presentation.md` | Client-ready strategy deck with business language summary, visual priority matrix, roadmap timeline, and talking points |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "strategy-direction"
date: YYYY-MM-DD
type: strategy
status: complete
roadmap-horizon: "3-month|6-month|12-month"
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile with clear business goals (must exist in vault)
  - **Audit & Recommendations Team** (strongly recommended) — the compiled findings and recommendations are the raw material for the priority matrix
  - **Keyword Research Team** (strongly recommended) — keyword opportunity data drives strategic decisions about where to invest
  - **Competitor Analysis Team** (strongly recommended) — competitive intelligence is the foundation of competitive strategy
  - **Research Team** (recommended) — market context and algorithm awareness inform strategic direction
  - **Analytics & Reporting Team** (recommended for ongoing strategy) — performance data drives strategy adjustments at quarterly reviews

- **Feeds into:**
  - **All execution teams** — the roadmap and priority matrix tell execution teams what to work on and in what order
  - **Client** — the strategy presentation is a client deliverable that earns buy-in for the execution plan
  - **Audit & Recommendations Team** — the priority matrix is included in the master audit report
  - **Analytics & Reporting Team** — roadmap milestones become the benchmarks tracked in monthly reports

## Quality Checks

### Strategy & Direction-Specific Quality Criteria

1. **Data-driven strategy** — Every strategic decision must trace back to data from the intelligence or execution teams. "We should focus on content because content is important" is opinion. "We should focus on content because: (a) keyword gap analysis shows 47 keyword clusters where competitors rank and we do not, (b) competitor content analysis shows the average top-ranking competitor publishes 3x more content monthly, and (c) the client's existing content scores 35% lower on topical completeness than the top 3 competitors" is data-driven strategy.

2. **Specific priority scores** — The Priority Matrix Builder must score every recommendation with specific Impact (1-5) and Effort (1-5) numbers, not vague "high/medium/low" labels alone. The numeric scores must be consistent: if fixing a broken homepage redirect is Impact 5 / Effort 1, fixing a broken link on a low-traffic archive page cannot also be Impact 5 / Effort 1. Calibrate across the full recommendation set.

3. **Competitive realism** — The Competitive Strategy Analyst must make honest assessments. If a competitor has 10x the domain authority and 100x the content, the strategy cannot be "outrank them for their top keywords." It must identify realistic paths: long-tail flanking, underserved niches, different content formats, local or specialized targeting. Unrealistic competitive strategies waste client resources.

4. **Time-bound roadmap** — The roadmap must include specific month-by-month or quarter-by-quarter milestones with expected deliverables, not vague phase descriptions. "Q2: Content focus" is not a roadmap. "Month 4: Publish 4 blog posts targeting Cluster 3 keywords (list them), optimize 6 existing pages flagged in the content audit, begin link outreach campaign for the cold brew guide — target: 5 placements" is a roadmap.

5. **Resource-aware planning** — The roadmap must account for the client's actual resources. A strategy that requires a full-time content team, a developer, and a PR agency is useless for a solo founder. Scale the roadmap to what the client can actually implement. Include effort estimates per task.

6. **Business language in client materials** — The Client Communication Manager must eliminate all jargon from the strategy presentation. No unexplained acronyms (CWV, LCP, SERP, E-E-A-T). No technical implementation details. Business language only: "Your website is slower than competitors, which costs you customers" not "Your LCP is 4.2s exceeding the 2.5s threshold."

7. **Strategy-execution alignment** — The strategy must directly translate to executable tasks. Every strategic priority must map to specific teams and agents that will execute it. A strategic priority with no execution path is aspirational, not actionable.

8. **Quarterly updateability** — Strategy documents must be structured for easy updating. At each quarterly review, the team should be able to: update performance data, adjust priorities based on results, add new findings from re-audits, and extend the roadmap — without rewriting the entire strategy from scratch.

9. **Minimum quality score: 4/5. Target: 5/5.** (Higher bar — strategy guides all agency work.)
