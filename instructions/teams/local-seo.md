# Local SEO Team

> Optimize the client's local search presence so they dominate the map pack, local organic results, and location-based queries in their service areas.

## Team Overview

The Local SEO Team is a specialized unit that only activates for businesses with physical locations or defined service areas. Local search is a distinct discipline from traditional SEO — it operates on a different algorithm (proximity, relevance, prominence), has its own ranking surfaces (Google Map Pack, Local Finder, Google Business Profile), and requires unique optimization tactics (NAP consistency, local citations, review management, location-specific content). A business that ranks well nationally may be invisible locally, and vice versa.

This team sits in the **Execution Layer** of the agency hierarchy. It runs during Phase 3 (Audit, for local SEO auditing) and Phase 5 (Execute, for local optimization work). The team only runs when the client has been identified as a local business during onboarding — there is no reason to run it for purely online businesses, SaaS companies without local presence, or national e-commerce brands without physical stores.

The team follows a sequence that starts with competitive analysis (understand what local competitors are doing), moves through Google Business Profile optimization (the most impactful local ranking factor), then builds citation consistency, creates location-specific content, and finally develops a review management strategy. Each agent builds on the previous one's findings to create a cohesive local SEO plan.

## Agents

| Agent | File | Role |
|-------|------|------|
| Local Competitor Analyst | `agents/local/local-competitor.md` | Analyzes local competitors' Google Business Profiles, local rankings, citation profiles, review volumes, and local content strategies |
| GBP Optimizer | `agents/local/gbp-optimizer.md` | Audits and optimizes the client's Google Business Profile — categories, attributes, description, photos, posts, Q&A, products/services, and all available fields |
| Local Citation Builder | `agents/local/citation-builder.md` | Audits existing citations for NAP (Name, Address, Phone) consistency, identifies missing citation sources, and builds a citation cleanup and creation plan |
| Local Content Writer | `agents/local/local-content-writer.md` | Creates location-specific content — city/neighborhood landing pages, local blog posts, area guides, and locally relevant FAQ content |
| Review Strategist | `agents/local/review-strategist.md` | Develops a review acquisition strategy, creates review response templates, and plans for improving the client's review profile across platforms |

## When to Run This Team

- **Client has a physical location** — Run during initial audit and setup for any brick-and-mortar business
- **Client has a service area** — Run for service-area businesses (plumbers, electricians, lawyers, etc.) even without a storefront
- **Client has multiple locations** — Run for multi-location businesses that need location-specific optimization
- **Map Pack absence** — Client does not appear in the Google Map Pack for their primary keywords
- **Local ranking decline** — Client losing local rankings or map pack positions
- **New location launch** — Client opening a new physical location or expanding to a new service area
- **Competitor overtaking locally** — A local competitor is outranking the client in map results
- **Low review volume or rating** — Client's review profile is weaker than local competitors
- **NAP inconsistencies found** — Technical SEO or Research teams discover inconsistent business information across the web
- **Never run for:** Pure e-commerce without physical stores, SaaS companies, businesses with no geographic targeting

## Execution Order

```
Step 1: Local Competitor Analyst
   │
   │  Researches local competitors using Tavily and Web Fetch.
   │  Analyzes their GBP listings, review volumes and ratings,
   │  local content strategies, citation profiles, and local
   │  keyword targeting. Establishes the competitive baseline.
   │  Saves to vault/09-Local/[client]/local-competitor-analysis.md
   │
   ▼
Step 2: GBP Optimizer
   │
   │  Audits the client's Google Business Profile against best
   │  practices and competitor benchmarks. Checks every field:
   │  primary and secondary categories, business description,
   │  attributes, photos, posts, Q&A, products/services, hours,
   │  and special features. Produces optimization recommendations.
   │  Saves to vault/09-Local/[client]/gbp-optimization.md
   │
   ▼
Step 3: Local Citation Builder
   │
   │  Searches for existing citations using Tavily and Web Search.
   │  Audits NAP consistency across all found citations. Identifies
   │  missing citation sources (industry directories, local directories,
   │  data aggregators). Produces a citation cleanup list and a
   │  citation building list with submission details.
   │  Saves to vault/09-Local/[client]/citation-audit.md
   │
   ▼
Step 4: Local Content Writer
   │
   │  Creates location-specific content based on keyword data and
   │  competitive analysis. Writes city/neighborhood landing pages,
   │  local blog posts, area guides, and locally-focused FAQs.
   │  Each piece targets local keywords and includes local entities
   │  (landmarks, neighborhoods, local references).
   │  Saves to output/[client]/[date]/local/content/
   │
   ▼
Step 5: Review Strategist
   │
   │  Analyzes current review profile (volume, rating, recency,
   │  platforms) against competitors. Develops review acquisition
   │  strategy with specific tactics (review request emails, QR codes,
   │  follow-up timing). Creates review response templates for
   │  positive, negative, and neutral reviews.
   │  Saves to output/[client]/[date]/local/review-strategy.md
```

**Data flow:** The Local Competitor Analyst establishes what "good" looks like in the local market. Every subsequent agent benchmarks against competitor standards and fills the gaps.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Web Fetch | Page fetch | Check the client's GBP listing, verify citation pages, read local directory listings |
| Tavily | `search` | Research local competitors, find citation sources, discover local keywords, find industry directories |
| Tavily | `extract` | Deep-read competitor GBP listings and local directory pages |
| Web Search | General research | Find local directories, check NAP consistency across the web, research local market context |
| Firecrawl | `scrape` | Scrape competitor local pages and directory listings for detailed analysis |

### Tool Usage Protocol

1. **Use Tavily for local competitor research** — search for "[business type] + [city]" to find local competitors and their presence
2. **Use Web Fetch to check GBP listings** — fetch the client's and competitors' Google Business Profile pages directly
3. **Use Web Search for citation discovery** — search for the business name and phone number to find existing citations
4. **Batch citation checks** — search for NAP across multiple directories in related queries
5. **Save all local data to vault/09-Local/** — local SEO is ongoing and data should persist between sessions

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Business name, address, phone (NAP) | `vault/01-Clients/[client]/site-info.md` | Yes — exact NAP is critical for citation work |
| Business type confirmation | `vault/01-Clients/[client]/profile.md` | Yes — must confirm this is a local business |
| Service areas / locations | `vault/01-Clients/[client]/profile.md` | Yes — must know geographic targets |
| Competitor list | `vault/01-Clients/[client]/competitors.md` | Yes — must include local competitors |
| Keyword research data | `vault/03-Research/[client]/` | Recommended — local keyword variations inform content |
| GBP access/URL | Client-provided | Recommended — enables direct GBP audit |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Local Competitor Analysis | `vault/09-Local/[client]/local-competitor-analysis.md` | Detailed analysis of local competitors' GBP, reviews, citations, and local content |
| GBP Optimization Plan | `vault/09-Local/[client]/gbp-optimization.md` | Field-by-field GBP audit with specific optimization recommendations |
| Citation Audit & Plan | `vault/09-Local/[client]/citation-audit.md` | NAP consistency audit, citation cleanup list, new citation targets with submission details |
| Local Content | `output/[client]/[date]/local/content/` | City/neighborhood landing pages, local blog posts, area guides |
| Review Strategy | `output/[client]/[date]/local/review-strategy.md` | Review acquisition plan, response templates, platform-specific tactics |
| Local SEO Summary | `output/[client]/[date]/local/local-seo-summary.md` | Combined local SEO strategy document with all recommendations |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "local-seo"
date: YYYY-MM-DD
type: local
status: complete
locations: ["city-1", "city-2"]
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile confirming local business status with NAP details (must exist in vault)
  - **Keyword Research Team** (recommended) — local keyword variations and intent data improve local content targeting
  - **Research Team** (recommended) — market context helps understand the local competitive landscape
  - **Technical SEO Team** (optional) — crawl data can reveal existing local landing pages and URL structure

- **Feeds into:**
  - **Audit & Recommendations Team** — Local SEO findings and recommendations feed into the master report
  - **Content SEO Team** — Local content needs may trigger additional content briefs and writing
  - **Analytics & Reporting Team** — Local rankings, GBP metrics, and review data become tracking targets
  - **Strategy & Direction Team** — Local SEO opportunities inform the overall SEO roadmap

## Quality Checks

### Local SEO-Specific Quality Criteria

1. **NAP accuracy** — The client's Name, Address, and Phone number must be verified as 100% consistent across all recommendations. Every citation recommendation must use the exact same NAP format. Even minor inconsistencies (St. vs Street, Suite 100 vs Ste 100) degrade local SEO.

2. **Verified competitor data** — Local competitor analysis must be based on actual data from GBP listings, review platforms, and citation sources — not assumed based on general knowledge. Include URLs and screenshots or scraped data as evidence.

3. **GBP completeness** — The GBP optimization plan must cover every available field, not just the basics. Categories, attributes, business description, photos, posts, Q&A, products/services, special hours, and all applicable features must be addressed.

4. **Relevant citation sources** — Citation recommendations must include sources relevant to the client's industry and location, not just generic directories. A dentist needs dental directories and health directories; a restaurant needs food and dining directories. Generic-only lists are insufficient.

5. **Local content authenticity** — Location-specific content must include genuine local references (neighborhoods, landmarks, local events, area-specific information). Generic content with a city name inserted is not local content. Each city/area page must be meaningfully different from others.

6. **Review strategy ethics** — Review strategies must never recommend fake reviews, review gating (only asking happy customers), or incentivized reviews (offering discounts for reviews). These practices violate platform policies and can result in penalties. Recommend ethical tactics only: asking all customers, making the process easy, responding to all reviews.

7. **Multi-location handling** — For multi-location businesses, each location must have its own GBP optimization plan, citation audit, and local content. One-size-fits-all local SEO across locations is unacceptable.

8. **Minimum quality score: 3/5. Target: 4/5+.**
