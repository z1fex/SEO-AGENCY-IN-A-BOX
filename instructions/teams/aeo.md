# AEO (Answer Engine Optimization) Team

> Optimize the client's content and entity presence so AI-powered search engines cite, reference, and surface their brand in AI Overviews, Perplexity answers, ChatGPT search results, and Gemini responses.

## Team Overview

The AEO Team is the future-proofing arm of the agency. Traditional SEO optimizes for ten blue links. AEO optimizes for the answer layer that sits above those links — Google AI Overviews, Perplexity AI, ChatGPT search, Gemini, and every AI-powered search experience that is replacing click-based discovery with citation-based answers. When a user asks an AI search engine a question and gets a synthesized answer with sources, AEO determines whether the client's site is one of those sources. If the agency ignores AEO, it is optimizing for a search landscape that is shrinking.

This team sits in the **Execution Layer** of the agency hierarchy. It runs during Phase 3 (Audit, for auditing AI search presence) and Phase 5 (Execute, for AEO optimization). AEO is NOT optional — every SEO engagement must include it. Even if the initial audit scope is narrow, the AEO team must at minimum audit the client's visibility in AI search results for their primary keywords. The shift from link-based results to AI-generated answers is accelerating, and clients who are invisible to AI search engines today will lose organic traffic tomorrow.

The team follows a research-first pipeline. The Conversational Query Researcher identifies how users ask AI search engines about the client's topics. The AI Overview Optimizer and Perplexity Optimizer analyze what those AI engines actually return and how the client can get cited. The Featured Snippet Strategist targets the structured answer boxes that AI Overviews often pull from. The Entity Optimizer and Knowledge Panel Manager build the entity authority that AI models use to determine which sources are trustworthy. The Citation Optimizer ensures the client's content is structured, sourced, and formatted in the way AI models prefer to cite.

## Agents

| Agent | File | Role |
|-------|------|------|
| Conversational Query Researcher | `agents/aeo/conversational-query-researcher.md` | Discovers how users phrase questions to AI search engines — natural language queries, follow-up questions, comparison queries, and multi-turn conversational patterns that differ from traditional keyword searches |
| AI Overview Optimizer | `agents/aeo/ai-overview-optimizer.md` | Analyzes which queries trigger Google AI Overviews, identifies which sources Google cites, and optimizes the client's content to be cited in AI Overview responses |
| Perplexity Optimizer | `agents/aeo/perplexity-optimizer.md` | Analyzes how Perplexity AI answers queries in the client's space, identifies which sources Perplexity cites, and optimizes content structure and authority signals to earn Perplexity citations |
| Featured Snippet Strategist | `agents/aeo/featured-snippet-strategist.md` | Identifies featured snippet opportunities for the client's target keywords, analyzes current snippet holders, and creates content structures (tables, lists, definitions, step-by-step formats) that win snippet positions |
| Entity Optimizer | `agents/aeo/entity-optimizer.md` | Builds and strengthens the client's entity presence in knowledge graphs — defines entity relationships, optimizes entity attributes, ensures consistent entity representation across the web, and improves topical authority signals |
| Knowledge Panel Manager | `agents/aeo/knowledge-panel-manager.md` | Audits and manages the client's Google Knowledge Panel — verifies or triggers panel creation, optimizes panel content, manages linked entities, and ensures accurate representation across Google's knowledge graph |
| Citation Optimizer | `agents/aeo/citation-optimizer.md` | Optimizes content formatting, structure, and sourcing so AI models prefer to cite it — clear headings, direct answers, authoritative sourcing, structured data, and the content patterns that AI models extract from |

## When to Run This Team

- **Every SEO engagement** — AEO is not optional; at minimum run the AI Overview Optimizer and Conversational Query Researcher for the client's primary keywords
- **Full site audit** — Run the complete AEO team as part of any comprehensive SEO audit
- **New client onboarding** — Establish the client's AI search visibility baseline immediately
- **AI Overview appeared for key terms** — When Google starts showing AI Overviews for the client's target keywords, optimize immediately before competitors do
- **Client losing traffic but not rankings** — AI Overviews may be consuming clicks from organic results; diagnose and optimize
- **Content strategy planning** — Before creating new content, understand which topics trigger AI answers and how to structure content for citation
- **Competitor cited in AI results** — When competitors appear in AI Overviews or Perplexity answers for the client's target topics
- **Knowledge Panel issues** — Client's Knowledge Panel is inaccurate, incomplete, or nonexistent
- **Entity authority weak** — The client is not recognized as an entity by Google's knowledge graph
- **Post-algorithm update** — After Google updates that change AI Overview behavior or citation patterns
- **Quarterly review** — AI search results change rapidly; re-audit quarterly to catch new opportunities and citation changes

## Execution Order

```
Step 1: Conversational Query Researcher
   │
   │  Uses Tavily and Web Search to discover how users phrase questions
   │  to AI search engines about the client's topics. Maps conversational
   │  queries, follow-up chains, comparison queries, and question patterns
   │  that differ from traditional keyword searches. Identifies which
   │  queries trigger AI Overviews and which trigger traditional results.
   │  Saves to vault/11-AEO/[client]/conversational-queries.md
   │
   ▼
Step 2: AI Overview Optimizer
   │
   │  Takes the conversational queries and checks which ones trigger
   │  Google AI Overviews. For each AI Overview, records: the query,
   │  the AI-generated answer, all cited sources, the content structure
   │  of cited sources, and whether the client is cited. Produces
   │  optimization recommendations for each query where the client
   │  should be cited but is not.
   │  Saves to vault/11-AEO/[client]/ai-overview-audit.md
   │
   ▼
Step 3: Perplexity Optimizer
   │
   │  Takes the same conversational queries and checks Perplexity AI
   │  responses. Records which sources Perplexity cites, what content
   │  patterns it prefers, and whether the client appears. Compares
   │  citation patterns between Google AI Overviews and Perplexity
   │  to identify cross-platform optimization opportunities.
   │  Saves to vault/11-AEO/[client]/perplexity-audit.md
   │
   ▼
Step 4: Featured Snippet Strategist
   │
   │  Analyzes which target keywords currently show featured snippets
   │  in traditional SERP results (these often feed AI Overviews).
   │  Identifies snippet format (paragraph, list, table, video),
   │  analyzes current snippet holders, and creates content structures
   │  optimized to win snippet positions. Prioritizes queries where
   │  the client ranks on page 1 but does not hold the snippet.
   │  Saves to vault/11-AEO/[client]/featured-snippet-strategy.md
   │
   ▼
Step 5: Entity Optimizer
   │
   │  Audits the client's entity presence across the web. Checks if
   │  the brand, products, and key people are recognized as entities
   │  by Google. Maps entity relationships, identifies missing entity
   │  attributes, and recommends actions to strengthen entity authority:
   │  Wikipedia/Wikidata presence, consistent entity references across
   │  authoritative sites, structured data, and topical authority signals.
   │  Saves to vault/11-AEO/[client]/entity-audit.md
   │
   ▼
Step 6: Knowledge Panel Manager
   │
   │  Checks if the client has a Google Knowledge Panel. If yes, audits
   │  it for accuracy and completeness. If no, assesses eligibility and
   │  recommends actions to trigger panel creation. Manages panel
   │  content: linked social profiles, logo, description, key facts,
   │  and related entities. Ensures Knowledge Graph representation
   │  matches the client's desired brand positioning.
   │  Saves to vault/11-AEO/[client]/knowledge-panel-audit.md
   │
   ▼
Step 7: Citation Optimizer
   │
   │  Takes all findings from the previous agents and produces a
   │  unified citation optimization plan. Specifies exactly how to
   │  restructure existing content and create new content so AI models
   │  prefer to cite it: clear H2/H3 question-answer structures,
   │  direct definitive answers in the first sentence after headings,
   │  authoritative sourcing with cited statistics, structured data
   │  enhancements, and content formatting patterns that AI models
   │  extract from. This is the culmination deliverable of the team.
   │  Saves to vault/11-AEO/[client]/citation-optimization-plan.md
```

**Data flow:** The Conversational Query Researcher provides the query foundation. The AI Overview Optimizer and Perplexity Optimizer reveal what AI engines currently cite and where the client is missing. The Featured Snippet Strategist targets the structured answer positions that often feed AI Overviews. The Entity Optimizer and Knowledge Panel Manager build the underlying authority that AI models trust. The Citation Optimizer synthesizes everything into an actionable optimization plan.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Tavily | `search` | Primary research tool — discover conversational queries, check what AI search engines return, research entity presence, find citation patterns |
| Tavily | `search` (advanced depth) | Deep SERP analysis — check which queries trigger AI Overviews, analyze featured snippet content, examine citation sources |
| Tavily | `extract` | Deep-read pages that AI Overviews and Perplexity cite to understand what content structures get cited |
| Web Search | General research | Check Google AI Overviews live, research Knowledge Panel status, verify entity recognition, monitor AI search developments |
| Web Fetch | Page validation | Fetch the client's pages to audit content structure, heading hierarchy, schema markup, and citation-readiness |
| Firecrawl | `scrape` | Scrape competitor pages that are being cited by AI search engines to reverse-engineer their content structure |

### Tool Usage Protocol

1. **Use Tavily with advanced depth for AI Overview checks** — standard depth may miss AI Overview triggers and citation data
2. **Check both Google and Perplexity** for every priority query — citation patterns differ between AI search engines
3. **Scrape cited sources** — when an AI Overview cites a competitor, use Firecrawl to scrape that page and understand why it was cited
4. **Web Fetch for the client's own pages** — check current content structure, heading hierarchy, and schema before recommending changes
5. **Save all AI search results to vault** — AI results change frequently; timestamp everything for comparison on re-audit
6. **Check vault for existing keyword data** — the Keyword Research team's SERP analysis may already identify AI Overview triggers

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Client site URL | `vault/01-Clients/[client]/site-info.md` | Yes |
| Keyword clusters | `vault/03-Research/[client]/keyword-clusters.md` | Yes — AEO optimization must target specific queries |
| SERP analysis | `vault/03-Research/[client]/serp-analysis.md` | Strongly recommended — identifies which keywords already trigger AI Overviews |
| Content inventory | `vault/04-Content/[client]/` | Recommended — know what content exists before recommending changes |
| Competitor analysis | `vault/06-Competitors/[client]/` | Recommended — reveals which competitors are getting cited |
| Technical crawl data | `vault/10-Technical/[client]/crawl-data/` | Recommended — schema audit informs entity and structured data work |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Conversational Query Map | `vault/11-AEO/[client]/conversational-queries.md` | Full map of how users ask AI search engines about the client's topics, with query types and AI trigger status |
| AI Overview Audit | `vault/11-AEO/[client]/ai-overview-audit.md` | Which queries trigger AI Overviews, who gets cited, where the client is missing, and how to get cited |
| Perplexity Audit | `vault/11-AEO/[client]/perplexity-audit.md` | Perplexity citation analysis with source comparison against Google AI Overviews |
| Featured Snippet Strategy | `vault/11-AEO/[client]/featured-snippet-strategy.md` | Snippet opportunities, current holders, content format recommendations to win snippets |
| Entity Audit | `vault/11-AEO/[client]/entity-audit.md` | Entity recognition status, relationship map, authority gaps, and strengthening recommendations |
| Knowledge Panel Audit | `vault/11-AEO/[client]/knowledge-panel-audit.md` | Knowledge Panel status, accuracy review, optimization or creation plan |
| Citation Optimization Plan | `vault/11-AEO/[client]/citation-optimization-plan.md` | Unified plan for restructuring content to earn AI citations — the team's culmination deliverable |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "aeo"
date: YYYY-MM-DD
type: aeo
status: complete
ai-engines-checked: ["google-ai-overview", "perplexity"]
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile with site URL (must exist in vault)
  - **Keyword Research Team** (required) — keyword clusters and SERP analysis are the foundation of AEO work; you cannot optimize for AI search without knowing which queries to target
  - **Research Team** (recommended) — AI search landscape analysis provides context on current AI search engine behavior and algorithm changes
  - **Content SEO Team** (recommended) — existing content inventory reveals what can be optimized vs. what must be created
  - **Technical SEO Team** (recommended) — schema audit and crawl data inform entity and structured data recommendations

- **Feeds into:**
  - **Content SEO Team** — AEO findings drive content restructuring and new content needs (FAQ sections, authoritative guides, entity-building pages)
  - **Audit & Recommendations Team** — All AEO findings and the citation optimization plan feed into the master report
  - **Strategy & Direction Team** — AEO opportunity data informs the SEO roadmap and prioritization of AI search optimization
  - **Analytics & Reporting Team** — AI search visibility metrics become tracking targets in monthly reports

## Quality Checks

### AEO-Specific Quality Criteria

1. **Real AI search data** — Every AI Overview analysis and Perplexity citation must come from actual tool queries (Tavily, Web Search), not assumptions about what AI engines might return. If a query does not trigger an AI Overview, record that fact rather than guessing what it would show.

2. **Multi-engine coverage** — AEO is not just Google AI Overviews. The team must check at minimum Google AI Overviews and Perplexity for priority queries. Recommendations must work across AI search engines, not just one.

3. **Cited source analysis** — When an AI engine cites a source, the team must analyze WHY that source was cited. What content structure does it use? How is it formatted? What authority signals does it have? Vague recommendations like "create better content" are unacceptable. Specific structural patterns must be identified and recommended.

4. **Entity verification** — Entity optimization recommendations must be based on verified entity recognition status. Use Google's Knowledge Graph Search API results (via Tavily/Web Search), check for Wikipedia/Wikidata entries, and verify structured data rather than assuming entity status.

5. **Actionable content structures** — Every citation optimization recommendation must include the specific content structure to use: heading format, answer placement (first sentence after heading), recommended word count for the answer block, supporting evidence structure, and schema markup. Abstract advice like "make content more authoritative" is a quality failure.

6. **Featured snippet specificity** — Featured snippet recommendations must specify the exact format to target (paragraph, list, table, video), the exact query to target, the current snippet holder's approach, and a ready-to-implement content structure that improves on the current holder.

7. **Knowledge Panel accuracy** — Knowledge Panel recommendations must be based on the actual current state of the client's panel (or confirmed absence). Every recommended change must be implementable through legitimate channels (Google Business Profile, structured data, Wikipedia if notable, official website markup).

8. **No conflation of traditional SEO with AEO** — AEO recommendations must be distinct from traditional SEO advice. "Optimize your title tags" is traditional SEO. "Restructure your H2s as direct questions and place a concise 40-60 word answer immediately below each heading so AI models can extract clean answer blocks" is AEO. The team must demonstrate understanding of how AI models extract and cite content differently from how traditional search indexes it.

9. **Minimum quality score: 3/5. Target: 4/5+.**
