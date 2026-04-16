# Link Building Team

> Build high-quality backlinks through outreach, digital PR, and opportunity identification to grow the client's domain authority and ranking power.

## Team Overview

The Link Building Team is the authority-building arm of the agency. Search engines use backlinks as one of the strongest ranking signals — a site with high-quality, relevant links from authoritative domains will outrank a site without them, all else being equal. This team does not buy links, use PBNs, or engage in any link scheme that risks a Google penalty. Instead, it builds links through legitimate methods: identifying broken link opportunities, prospecting relevant sites for outreach, writing compelling outreach emails, planning digital PR campaigns, and analyzing competitor link strategies to find replicable opportunities.

This team sits in the **Execution Layer** of the agency hierarchy. It runs during Phase 3 (Audit, for backlink auditing) and Phase 5 (Execute, for active link building campaigns). Link building is a long-term play — the team sets up campaigns, writes outreach templates, and identifies targets, but actual link acquisition happens over weeks and months as outreach is sent and relationships are built.

The team operates in a clear sequence: audit the current backlink profile first, analyze what competitors are doing, then find new opportunities, and finally create outreach materials and PR strategies. The Backlink Auditor establishes the baseline, the Competitor Backlink Analyzer reveals the competitive gap, and the remaining agents fill that gap with actionable link building plans.

## Agents

| Agent | File | Role |
|-------|------|------|
| Backlink Auditor | `agents/links/backlink-auditor.md` | Audits the client's existing backlink profile — catalogs referring domains, identifies toxic or spammy links, assesses anchor text distribution, and evaluates overall link health |
| Competitor Backlink Analyzer | `agents/links/competitor-backlinks.md` | Analyzes competitor backlink profiles to find their link sources, identify patterns (guest posts, resource pages, PR mentions), and surface replicable link opportunities |
| Link Prospector | `agents/links/link-prospector.md` | Finds new link building opportunities — resource pages, guest post targets, industry directories, roundup posts, and relevant sites that accept contributions or mentions |
| Broken Link Finder | `agents/links/broken-link-finder.md` | Discovers broken links on relevant external sites that point to dead pages in the client's niche — creates opportunities to suggest the client's content as a replacement |
| Digital PR Strategist | `agents/links/digital-pr.md` | Plans digital PR campaigns — identifies newsworthy angles, data stories, and unique content assets that attract natural links from journalists and publications |
| Outreach Email Writer | `agents/links/outreach-writer.md` | Writes personalized outreach email templates for each link building tactic — guest post pitches, broken link outreach, resource page suggestions, and PR pitches |

## When to Run This Team

- **Full site audit** — Backlink Auditor runs as part of every comprehensive audit
- **New client onboarding** — Run Backlink Auditor and Competitor Backlink Analyzer to establish the link baseline
- **Link building campaign** — When the SEO roadmap calls for authority building
- **Competitor gained links** — When monitoring reveals competitors acquiring significant new backlinks
- **New linkable content** — After the Content SEO team creates high-value content (guides, research, tools) that can attract links
- **Ranking plateau** — When content and technical SEO are solid but rankings are not improving, links are often the missing factor
- **Toxic link cleanup** — When the Backlink Auditor identifies harmful links that need disavowing
- **Domain authority gap** — When the competitor analysis reveals a significant authority gap between the client and competitors
- **Digital PR opportunity** — When the client has newsworthy data, launches, or stories that can earn media coverage

## Execution Order

```
Step 1: Backlink Auditor
   │
   │  Scrapes and analyzes the client's existing backlink profile.
   │  Uses Firecrawl to check referring pages and Web Search/Tavily
   │  to assess domain quality. Catalogs all linking domains, anchor
   │  text distribution, link types, and flags toxic links.
   │  Saves to vault/05-Links/[client]/backlink-audit.md
   │
   ▼
Step 2: Competitor Backlink Analyzer
   │
   │  Analyzes competitor backlink profiles using Firecrawl scraping
   │  and Tavily research. Identifies their top link sources, link
   │  building patterns, and replicable opportunities.
   │  Saves to vault/05-Links/[client]/competitor-backlinks.md
   │
   ▼
Step 3a: Link Prospector (parallel with 3b)
   │
   │  Uses Tavily search and Firecrawl to find link building targets:
   │  resource pages, guest post opportunities, industry directories,
   │  roundup posts, and relevant blogs that accept contributions.
   │  Produces a prioritized prospect list with contact information.
   │  Saves to vault/05-Links/[client]/link-prospects.md
   │
Step 3b: Broken Link Finder (parallel with 3a)
   │
   │  Uses Firecrawl and Web Fetch to find broken outbound links on
   │  relevant external sites. Matches broken destinations to topics
   │  where the client has (or could create) replacement content.
   │  Saves to vault/05-Links/[client]/broken-link-opportunities.md
   │
   ▼
Step 4: Digital PR Strategist
   │
   │  Reviews the client's business, content assets, and industry context
   │  to identify newsworthy angles for earning links through PR.
   │  Plans campaigns around data stories, original research, expert
   │  commentary, and industry trend pieces.
   │  Saves to vault/05-Links/[client]/digital-pr-plan.md
   │
   ▼
Step 5: Outreach Email Writer
   │
   │  Takes the prospect list, broken link opportunities, and PR plan
   │  and writes personalized outreach email templates for each tactic.
   │  Each template includes subject line, body, follow-up sequence,
   │  and personalization variables.
   │  Saves to output/[client]/[date]/links/outreach-emails.md
```

**Data flow:** The Backlink Auditor establishes the baseline. The Competitor Backlink Analyzer reveals the gap. Steps 3a and 3b find opportunities in parallel. The Digital PR Strategist adds earned-media angles. The Outreach Writer produces the execution materials.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Firecrawl | `scrape` | Scrape competitor pages to find their backlink mentions, check referring page content and context |
| Firecrawl | `crawl` | Crawl sections of referring domains to assess their quality and relevance |
| Firecrawl | `search` | Find resource pages, guest post opportunities, and industry directories |
| Tavily | `search` | Research link prospects, find broken link opportunities, identify PR targets and journalists |
| Tavily | `extract` | Deep-read prospect pages to assess relevance and find contact information |
| Web Fetch | Page validation | Verify broken links, check if prospect pages are still live, validate referring page context |
| Web Search | General research | Find industry publications, journalist contacts, PR distribution channels |

### Tool Usage Protocol

1. **Check vault for existing backlink data** — if a backlink audit exists and is less than 30 days old, reuse it
2. **Use Firecrawl `scrape` for individual link checks** — do not crawl entire referring domains unless assessing domain quality
3. **Use Tavily for prospecting searches** — batch related queries (e.g., search for "[industry] + resource page" and "[industry] + guest post" together)
4. **Verify all prospect links with Web Fetch** — ensure pages are live before adding to the prospect list
5. **Save all raw data to vault** — link building is ongoing; future campaigns build on previous research

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Client site URL | `vault/01-Clients/[client]/site-info.md` | Yes |
| Competitor list | `vault/01-Clients/[client]/competitors.md` | Yes |
| Competitor analysis data | `vault/06-Competitors/[client]/` | Recommended (provides competitor context) |
| Keyword clusters | `vault/03-Research/[client]/keyword-clusters.md` | Recommended (identifies which pages need link support) |
| Content inventory | `vault/04-Content/[client]/` | Recommended (identifies linkable assets) |
| Technical crawl data | `vault/10-Technical/[client]/crawl-data/` | Recommended (reveals internal link structure) |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Backlink Audit | `vault/05-Links/[client]/backlink-audit.md` | Current backlink profile analysis with toxic link flags |
| Competitor Backlink Analysis | `vault/05-Links/[client]/competitor-backlinks.md` | Competitor link sources and replicable patterns |
| Link Prospect List | `vault/05-Links/[client]/link-prospects.md` | Prioritized targets with contact info, domain quality, and outreach approach |
| Broken Link Opportunities | `vault/05-Links/[client]/broken-link-opportunities.md` | External broken links matchable to client content |
| Digital PR Plan | `vault/05-Links/[client]/digital-pr-plan.md` | PR campaign concepts with newsworthy angles and target publications |
| Outreach Email Templates | `output/[client]/[date]/links/outreach-emails.md` | Personalized email templates for each link building tactic |
| Link Building Strategy | `output/[client]/[date]/links/link-building-strategy.md` | Combined strategy document summarizing all tactics and priorities |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "link-building"
date: YYYY-MM-DD
type: links
status: complete
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile with competitor list (must exist in vault)
  - **Competitor Analysis Team** (recommended) — provides deeper competitor intelligence that enriches backlink analysis
  - **Content SEO Team** (recommended) — identifies linkable content assets and content gaps that could become link magnets
  - **Keyword Research Team** (recommended) — high-priority keywords reveal which pages need the most link support

- **Feeds into:**
  - **Audit & Recommendations Team** — Backlink audit findings and link building recommendations feed into the master report
  - **Content SEO Team** — Link building needs may drive content creation (e.g., "we need a comprehensive guide on X to use as a link magnet")
  - **Strategy & Direction Team** — Link gap data informs the SEO roadmap and resource allocation
  - **Analytics & Reporting Team** — New backlinks become tracking metrics in monthly reports

## Quality Checks

### Link Building-Specific Quality Criteria

1. **No black-hat tactics** — Never recommend PBNs, paid links (without nofollow/sponsored attributes), link exchanges, link farms, or any tactic that violates Google's Webmaster Guidelines. Every link building recommendation must be defensible if audited by Google.

2. **Domain quality assessment** — Every link prospect must include an assessment of the referring domain's quality. Consider: Is the site relevant to the client's industry? Does it have real traffic and content? Is it a legitimate publication or a low-quality link farm? Do not include prospects from obviously spammy or irrelevant domains.

3. **Relevance over volume** — 10 relevant, high-quality links from industry sites are worth more than 100 links from unrelated directories. Prioritize topical relevance and domain quality over quantity.

4. **Verified opportunities** — Every broken link must be verified as actually broken (via Web Fetch). Every prospect page must be verified as live and accepting the proposed link type. Do not include dead opportunities.

5. **Personalized outreach** — Outreach email templates must be personalized to each prospect type. Generic "Dear Webmaster" emails are unacceptable. Each template must reference the specific page, content, or context that makes the outreach relevant.

6. **Anchor text diversity** — Recommendations must promote natural anchor text distribution. No strategy should rely on exact-match anchor text for more than a small minority of links. Recommend branded, URL, generic, and partial-match anchors.

7. **Actionable prospect list** — Each prospect must include: target URL, contact method, proposed approach (guest post, resource page, broken link, etc.), and priority level. A list of domain names without context is not actionable.

8. **Toxic link identification** — The Backlink Auditor must flag genuinely toxic links with specific evidence for why they are harmful (spammy domain, irrelevant anchor text, link scheme pattern) and include disavow file recommendations where appropriate.

9. **Minimum quality score: 3/5. Target: 4/5+.**
