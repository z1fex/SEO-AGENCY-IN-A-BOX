# Research Team

> Monitor algorithm updates, track AI search developments, analyze SERP feature evolution, and provide the market and industry intelligence that informs every strategic decision across the agency.

## Team Overview

The Research Team is the intelligence backbone of the agency. Every strategy, every audit finding, every content decision, and every recommendation the agency makes is only as good as the intelligence behind it. This team ensures the agency operates with current, accurate information about the search landscape — not outdated assumptions from six months ago. Google changes its algorithm constantly. AI search engines are evolving weekly. SERP features appear and disappear. Industry trends shift. The Research Team monitors all of it and translates raw information into actionable intelligence that every other team consumes.

This team sits in the **Intelligence Layer** of the agency hierarchy. It runs during Phase 2 (Research) and is typically the first team to activate in any engagement. The Research Team provides the contextual foundation: what is happening in search right now, what algorithm changes have occurred, how AI search engines are evolving, what SERP features are appearing for the client's industry, and what industry trends affect the client's SEO strategy. Without this context, execution teams operate blind — optimizing for a search landscape that may have changed since the last engagement.

The team follows a parallel-then-sequential pipeline. The Market Researcher, Algorithm Update Monitor, and AI Search Landscape Analyst all run in parallel because they gather independent data streams. The Industry Trend Analyst then synthesizes these inputs into broader strategic context. The SERP Feature Researcher drills into specific feature opportunities. The Data Analyst processes all raw data and produces the synthesized intelligence reports that other teams consume.

## Agents

| Agent | File | Role |
|-------|------|------|
| Market Researcher | `agents/research/market-researcher.md` | Researches the client's market landscape — market size, growth trends, key players, customer segments, industry dynamics, and macroeconomic factors that affect search demand |
| Algorithm Update Monitor | `agents/research/algorithm-monitor.md` | Monitors Google algorithm updates (core updates, spam updates, helpful content updates, link spam updates), documents confirmed changes, assesses impact on the client's industry, and flags required strategy adjustments |
| SERP Feature Researcher | `agents/research/serp-feature-researcher.md` | Researches which SERP features appear for the client's target queries — featured snippets, People Also Ask, AI Overviews, knowledge panels, local packs, image packs, video carousels, and other features — to identify optimization opportunities |
| Industry Trend Analyst | `agents/research/industry-trend-analyst.md` | Tracks industry-specific trends affecting search behavior — seasonal demand patterns, emerging topics, shifting consumer interests, new product categories, and content format preferences |
| AI Search Landscape Analyst | `agents/research/ai-search-analyst.md` | Monitors the rapidly evolving AI search engine landscape — Google AI Overviews rollout, Perplexity growth, ChatGPT search capabilities, Gemini integration, and how these changes affect organic traffic and SEO strategy |
| Data Analyst | `agents/research/data-analyst.md` | Processes raw research data from all other agents and client-provided data (analytics, Search Console) into structured, actionable intelligence — identifies patterns, correlations, and anomalies that inform strategy |

## When to Run This Team

- **New client onboarding** — Always the first team to run, establishing the intelligence foundation for the entire engagement
- **Full SEO audit** — Required to provide current search landscape context before any audit work begins
- **Quarterly strategy review** — Re-run at least quarterly to catch algorithm changes, AI search developments, and industry shifts
- **After a Google algorithm update** — Run the Algorithm Update Monitor immediately after any confirmed update to assess impact
- **Ranking volatility** — When the client experiences sudden ranking changes, research the cause (algorithm update, SERP feature changes, competitor moves)
- **Before content planning** — Research current SERP features and AI Overview triggers before planning content
- **AI search concern** — When the client asks about AI search impact on their traffic, run the AI Search Landscape Analyst
- **New market entry** — When the client expands into a new industry, geography, or product category
- **Annual planning** — Before setting annual SEO goals, refresh all market and industry intelligence
- **Client-provided data analysis** — When the client provides analytics, Search Console, or other data, the Data Analyst processes it

## Execution Order

```
Step 1a: Market Researcher (parallel)
   │
   │  Uses Tavily and Web Search to research the client's market:
   │  market size, growth trajectory, key segments, major players,
   │  regulatory changes, and macroeconomic factors that affect
   │  search demand in the client's industry.
   │  Saves to vault/03-Research/[client]/market-research.md
   │
Step 1b: Algorithm Update Monitor (parallel)
   │
   │  Uses Tavily (topic: "news") and Web Search to check for recent
   │  Google algorithm updates. Documents: update name, rollout date,
   │  confirmed targets, industry impact assessment, and any required
   │  strategy adjustments. Checks multiple authoritative sources
   │  (Search Engine Journal, Search Engine Land, Google SearchLiaison,
   │  Barry Schwartz, etc.).
   │  Saves to vault/03-Research/[client]/algorithm-updates.md
   │
Step 1c: AI Search Landscape Analyst (parallel)
   │
   │  Uses Tavily and Web Search to research the current state of
   │  AI-powered search: Google AI Overviews coverage and behavior,
   │  Perplexity usage and citation patterns, ChatGPT search
   │  capabilities, Gemini integration, and how AI search affects
   │  organic traffic patterns in the client's industry.
   │  Saves to vault/03-Research/[client]/ai-search-landscape.md
   │
   ▼
Step 2: Industry Trend Analyst
   │
   │  Takes the market research, algorithm updates, and AI search
   │  landscape data and synthesizes industry-specific trends.
   │  Identifies: seasonal search demand patterns, emerging topics
   │  gaining search volume, shifting consumer interests, new content
   │  format preferences, and industry-specific search behavior changes.
   │  Saves to vault/03-Research/[client]/industry-trends.md
   │
   ▼
Step 3: SERP Feature Researcher
   │
   │  Uses Tavily with advanced depth to analyze which SERP features
   │  appear for the client's priority keywords. Maps: featured snippets,
   │  People Also Ask, AI Overviews, knowledge panels, local packs,
   │  image packs, video carousels, shopping results, site links, and
   │  other features. Identifies feature optimization opportunities
   │  and flags queries where AI Overviews may reduce click-through rates.
   │  Saves to vault/03-Research/[client]/serp-features.md
   │
   ▼
Step 4: Data Analyst
   │
   │  Processes all research outputs from Steps 1-3 plus any
   │  client-provided data (analytics, Search Console exports, rank
   │  tracking data). Identifies patterns, correlations, and anomalies.
   │  Produces structured intelligence summaries that are directly
   │  consumable by other teams. Translates raw data into decisions:
   │  what the data means, not just what the data says.
   │  Saves to vault/03-Research/[client]/research-intelligence.md
```

**Data flow:** Three parallel streams (market, algorithm, AI search) converge in the Industry Trend Analyst, who synthesizes broader patterns. The SERP Feature Researcher drills into specific feature-level opportunities. The Data Analyst is the final synthesizer — processing everything into actionable intelligence that other teams can directly consume without re-interpreting raw data.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Tavily | `search` | Primary research tool — market research, algorithm updates, industry trends, SERP feature analysis |
| Tavily | `search` (topic: "news") | Algorithm update monitoring — returns recent news about Google changes, AI search developments |
| Tavily | `search` (advanced depth) | Deep SERP feature analysis — check which features appear for specific queries |
| Tavily | `extract` | Deep-read authoritative articles about algorithm updates, industry reports, and market analyses |
| Web Search | General research | Current news, fact checking, cross-referencing algorithm update sources, industry event monitoring |
| Web Fetch | Source validation | Fetch and read specific articles, reports, and data sources for detailed analysis |

### Tool Usage Protocol

1. **Use Tavily with `topic: "news"` for algorithm updates** — this filters for recent results, which is critical for time-sensitive algorithm change monitoring
2. **Cross-reference algorithm updates from at least 3 sources** — Google SearchLiaison (official), Search Engine Journal, Search Engine Land, Barry Schwartz / Search Engine Roundtable. Do not report an update based on a single source
3. **Use advanced depth for SERP feature analysis** — standard depth may miss feature data
4. **Save all raw research to vault** — research data has a long shelf life and is reused across multiple teams and engagements
5. **Check vault for existing research first** — if market research for this client's industry exists and is less than 30 days old, build on it rather than starting from scratch
6. **Timestamp everything** — research is time-sensitive; every output must include the date the research was conducted and the date of the most recent data point found

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Client industry / vertical | `vault/01-Clients/[client]/profile.md` | Yes — determines research focus |
| Client goals | `vault/01-Clients/[client]/goals.md` | Yes — determines which trends and updates matter most |
| Client site URL | `vault/01-Clients/[client]/site-info.md` | Recommended — enables industry-specific SERP feature research |
| Client competitor list | `vault/01-Clients/[client]/competitors.md` | Recommended — provides context for market research |
| Client analytics data | Client-provided (CSV, screenshots, or access) | Optional — enables the Data Analyst to process real performance data |
| Previous research data | `vault/03-Research/[client]/` | Optional — build on existing research rather than starting fresh |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Market Research Report | `vault/03-Research/[client]/market-research.md` | Market landscape, size, growth, key players, customer segments, and factors affecting search demand |
| Algorithm Update Brief | `vault/03-Research/[client]/algorithm-updates.md` | Recent algorithm changes with impact assessment and strategy implications for the client |
| AI Search Landscape Report | `vault/03-Research/[client]/ai-search-landscape.md` | Current state of AI-powered search engines and their impact on the client's organic visibility |
| Industry Trends Report | `vault/03-Research/[client]/industry-trends.md` | Industry-specific trends, seasonal patterns, emerging topics, and content format preferences |
| SERP Feature Map | `vault/03-Research/[client]/serp-features.md` | Which SERP features appear for target queries, optimization opportunities, and AI Overview impact assessment |
| Research Intelligence Summary | `vault/03-Research/[client]/research-intelligence.md` | Synthesized, actionable intelligence from all research agents — the primary file other teams read |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "research"
date: YYYY-MM-DD
type: research
status: complete
data-freshness: "YYYY-MM-DD"
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile with industry, goals, and competitor list (must exist in vault)
  - No team dependencies — the Research Team is designed to run first with no prior team output required

- **Feeds into:**
  - **Competitor Analysis Team** — market context helps interpret competitive data and identify which competitors matter
  - **Keyword Research Team** — industry trends and SERP feature data inform keyword discovery and intent classification
  - **Technical SEO Team** — algorithm update awareness prevents outdated technical recommendations
  - **Content SEO Team** — industry trends and SERP features inform content strategy and format decisions
  - **AEO Team** — AI search landscape data is the foundation of all AEO optimization work
  - **Link Building Team** — market context helps identify link building opportunities in industry publications and events
  - **Local SEO Team** — local market trends inform local content and strategy
  - **E-commerce SEO Team** — market trends and SERP features (shopping results, product rich results) inform e-commerce strategy
  - **Strategy & Direction Team** — all research intelligence feeds into strategic planning and roadmap creation
  - **Audit & Recommendations Team** — research context is included in the master report to explain why recommendations matter
  - **Analytics & Reporting Team** — algorithm update awareness helps explain traffic fluctuations in performance reports

## Quality Checks

### Research-Specific Quality Criteria

1. **Source authority** — Every research finding must cite its source. Authoritative sources include: Google's official communications (Search Central Blog, SearchLiaison), established industry publications (Search Engine Journal, Search Engine Land, Moz, Ahrefs Blog), financial market reports, government statistics, and recognized industry analysts. Random blog posts and social media speculation are not authoritative sources.

2. **Timeliness** — Algorithm update information must include the exact date of the update (confirmed or estimated rollout period). Industry trends must include the date range of the data. SERP feature analysis must note the date the SERPs were checked. Stale data must be flagged. The Data Analyst must include a "data freshness" field in every output.

3. **Impact assessment** — Raw information is insufficient. Every algorithm update, market trend, and SERP feature change must include an impact assessment specific to the client's industry and situation. "Google released a core update" is information. "Google's March 2025 core update targeted thin affiliate content; the client's review pages may be affected because they use templated product descriptions — recommend auditing the top 20 review pages" is intelligence.

4. **Actionable conclusions** — The Data Analyst's intelligence summary must translate data into decisions. Every section must answer "So what does this mean for the client?" and "What should the agency do differently because of this information?" Data without conclusions is a quality failure.

5. **No speculation presented as fact** — Research must clearly distinguish between confirmed facts (Google confirmed this update targets X), industry analysis (SEOs have observed that Y correlates with the update), and speculation (it is possible that Z is related, but unconfirmed). Mixing these categories misleads other teams.

6. **SERP feature verification** — SERP features must be verified through actual search queries (Tavily or Web Search), not assumed based on keyword type. "Informational keywords usually show featured snippets" is an assumption. "The query 'how to brew cold brew coffee' currently shows a featured snippet (paragraph format, held by example.com) and a People Also Ask box with 4 questions" is verified data.

7. **AI search coverage** — Every research engagement must include at minimum a basic AI search landscape check. The AI Search Landscape Analyst is not optional. Even if the focus is traditional SEO, the client needs to know how AI search is affecting their space.

8. **Cross-referenced algorithm updates** — No algorithm update should be reported based on a single source. Cross-reference at least 3 independent sources before including an update in the brief. Google's own announcements plus at least 2 industry publications.

9. **Minimum quality score: 3/5. Target: 4/5+.**
