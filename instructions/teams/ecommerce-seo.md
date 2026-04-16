# E-commerce SEO Team

> Optimize online stores for maximum organic visibility across product pages, category pages, faceted navigation, structured data, and shopping feeds.

## Team Overview

The E-commerce SEO Team is a specialized unit that only activates for clients running online stores. E-commerce SEO is a distinct discipline with challenges that do not exist on content sites: thousands or millions of product pages that need unique optimization, category taxonomy that must align with how customers search, faceted navigation that can explode crawl budget with duplicate or near-duplicate URLs, product structured data that powers rich results in Google Shopping, and shopping feeds that need optimization for Google Merchant Center and other comparison shopping engines.

This team sits in the **Execution Layer** of the agency hierarchy. It runs during Phase 3 (Audit, for e-commerce auditing) and Phase 5 (Execute, for e-commerce optimization). The team only runs when the client has been identified as an e-commerce business during onboarding. For businesses that are primarily content-based with a small shop, the Content SEO and Technical SEO teams typically handle the few product pages; this team activates when the store is a primary revenue channel with a meaningful product catalog.

The team follows a crawl-budget-first approach. The Faceted Navigation Auditor runs first because faceted navigation issues are the most common and most damaging e-commerce SEO problem — they can waste crawl budget by creating thousands of indexable filter combinations that dilute ranking signals. Once crawl budget is protected, the team moves to category strategy (the highest-traffic pages in any store), then product page optimization, then structured data and shopping feeds.

## Agents

| Agent | File | Role |
|-------|------|------|
| Faceted Navigation Auditor | `agents/ecommerce/faceted-nav-auditor.md` | Audits faceted navigation (filters, sorting, pagination) for crawl budget waste, duplicate content, and index bloat — recommends crawl control strategy (noindex, canonical, robots.txt, URL parameter handling) |
| Category Page Strategist | `agents/ecommerce/category-strategist.md` | Optimizes category page taxonomy, content, internal linking, and keyword targeting — ensures category pages rank for high-volume head terms |
| Product Page Optimizer | `agents/ecommerce/product-optimizer.md` | Optimizes individual product pages — unique titles, descriptions, images, reviews integration, cross-selling links, and keyword-rich copy that converts |
| Product Schema Generator | `agents/ecommerce/product-schema.md` | Generates Product structured data (JSON-LD) for product pages including price, availability, reviews, brand, SKU, and all applicable schema.org properties for rich results |
| Shopping Feed Optimizer | `agents/ecommerce/shopping-feed.md` | Optimizes product data feeds for Google Merchant Center, Google Shopping, and other comparison shopping engines — titles, descriptions, categories, GTINs, images |

## When to Run This Team

- **Client is an e-commerce business** — Run during initial audit for any online store
- **New online store launch** — Full e-commerce SEO setup before or immediately after launch
- **Crawl budget issues** — Google is not indexing key pages, crawl stats show waste on filter URLs
- **Index bloat** — Google has indexed far more pages than the store actually has products (faceted nav issue)
- **Product page ranking decline** — Product or category pages losing organic visibility
- **Category restructure** — Client is reorganizing their product taxonomy or adding new categories
- **Platform migration** — Moving from one e-commerce platform to another (Shopify to WooCommerce, etc.)
- **Google Shopping setup** — Client wants to optimize their shopping feed for Google Merchant Center
- **Rich results missing** — Product pages not showing price, rating, or availability in search results
- **Seasonal product optimization** — Before major shopping seasons (Black Friday, holiday, back-to-school)
- **Never run for:** Content-only sites, SaaS companies, service businesses without product catalogs

## Execution Order

```
Step 1: Faceted Navigation Auditor
   │
   │  Uses Firecrawl crawl data (from Technical SEO team) or runs its
   │  own crawl to map all faceted navigation URLs. Identifies filter
   │  combinations creating indexable pages, duplicate content from
   │  sorting/pagination, and crawl budget waste. Recommends a crawl
   │  control strategy (canonical tags, noindex, robots.txt blocks,
   │  URL parameter handling in Search Console).
   │  Saves to vault/10-Technical/[client]/faceted-nav-audit.md
   │
   ▼
Step 2: Category Page Strategist
   │
   │  Analyzes the store's category taxonomy against keyword clusters.
   │  Ensures category pages target the right keywords, have unique
   │  optimized content (not just product grids), include proper
   │  internal linking to subcategories and products, and follow
   │  a logical hierarchy that matches how customers search.
   │  Saves to vault/04-Content/[client]/category-strategy.md
   │
   ▼
Step 3: Product Page Optimizer
   │
   │  Audits product page templates and specific high-priority product
   │  pages. Checks for unique title tags, unique product descriptions
   │  (not manufacturer copy), optimized images with alt text, review
   │  integration, cross-sell/upsell internal links, and proper
   │  keyword targeting. Produces optimization templates and specific
   │  page-level recommendations.
   │  Saves to output/[client]/[date]/ecommerce/product-optimization.md
   │
   ▼
Step 4: Product Schema Generator
   │
   │  Generates Product structured data (JSON-LD) for product page
   │  templates. Includes all applicable properties: name, description,
   │  image, price, priceCurrency, availability, brand, SKU, GTIN,
   │  aggregateRating, review, offers. Validates against schema.org
   │  specifications and Google's rich result requirements.
   │  Saves to output/[client]/[date]/ecommerce/product-schema.md
   │
   ▼
Step 5: Shopping Feed Optimizer
   │
   │  Audits and optimizes the product data feed for Google Merchant
   │  Center. Optimizes product titles (keyword-rich, front-loaded),
   │  descriptions, Google product categories, images, GTINs/MPNs,
   │  and custom labels. Provides feed optimization guidelines and
   │  specific product-level fixes.
   │  Saves to output/[client]/[date]/ecommerce/shopping-feed.md
```

**Data flow:** Faceted Navigation Auditor protects crawl budget first (if filters are creating thousands of junk pages, nothing else matters). Category Strategist builds the taxonomy foundation. Product Page Optimizer refines individual pages. Schema Generator adds structured data. Shopping Feed Optimizer extends into Google Shopping.

## Tools Used

| Tool | Operation | Purpose |
|------|-----------|---------|
| Firecrawl | `crawl` | Crawl the store to discover all URLs including faceted navigation combinations, category structures, and product pages |
| Firecrawl | `map` | Quick URL inventory to assess store size and identify URL patterns (filter parameters, pagination) before full crawl |
| Firecrawl | `scrape` | Scrape individual product and category pages for deep analysis — title tags, schema, content, internal links |
| Web Fetch | Page validation | Check specific pages for schema markup, canonical tags, noindex directives, and redirect behavior |
| Tavily | `search` | Research competitor e-commerce strategies, find category keyword targets, check Google Shopping best practices |
| Web Search | General research | Look up current Google Merchant Center requirements, structured data specifications, and e-commerce SEO updates |

### Tool Usage Protocol

1. **Reuse Technical SEO crawl data** — if the Technical SEO team has already crawled the site, use their data from `vault/10-Technical/[client]/crawl-data/` rather than re-crawling
2. **Use `firecrawl_map` first** to assess store size — e-commerce sites can have hundreds of thousands of URLs from faceted navigation; map before crawling
3. **Set URL filters on crawls** — use `includePaths` and `excludePaths` to focus crawls on specific sections (e.g., crawl `/category/` separately from `/product/`)
4. **Scrape product pages by template type** — most e-commerce sites use templates; scrape 3-5 representative pages per template rather than every product
5. **Cache all crawl data** — e-commerce crawl data is expensive; save everything to vault for reuse

## Input Requirements

| Requirement | Source | Required? |
|-------------|--------|-----------|
| Client profile | `vault/01-Clients/[client]/profile.md` | Yes |
| Client site URL | `vault/01-Clients/[client]/site-info.md` | Yes |
| E-commerce platform | `vault/01-Clients/[client]/site-info.md` | Yes — platform determines what is technically possible |
| Product catalog scope | `vault/01-Clients/[client]/profile.md` | Yes — number of products, categories, and product types |
| Technical crawl data | `vault/10-Technical/[client]/crawl-data/` | Strongly recommended — avoids duplicate crawling |
| Keyword clusters | `vault/03-Research/[client]/keyword-clusters.md` | Recommended — informs category and product keyword targeting |
| Competitor analysis | `vault/06-Competitors/[client]/` | Recommended — reveals competitor category structures and product optimization |
| Google Merchant Center access | Client-provided | Optional — enables shopping feed audit |

## Output

### What This Team Produces

| Deliverable | Saved To | Description |
|-------------|----------|-------------|
| Faceted Navigation Audit | `vault/10-Technical/[client]/faceted-nav-audit.md` | Complete analysis of filter/sort/pagination URLs with crawl control recommendations |
| Category Strategy | `vault/04-Content/[client]/category-strategy.md` | Category taxonomy recommendations, keyword mapping, content guidelines, internal linking plan |
| Product Page Optimization Guide | `output/[client]/[date]/ecommerce/product-optimization.md` | Template-level and page-level product page recommendations |
| Product Schema (JSON-LD) | `output/[client]/[date]/ecommerce/product-schema.md` | Ready-to-implement Product structured data templates with all applicable properties |
| Shopping Feed Optimization | `output/[client]/[date]/ecommerce/shopping-feed.md` | Feed audit findings and optimization guidelines for Google Merchant Center |
| E-commerce SEO Summary | `output/[client]/[date]/ecommerce/ecommerce-summary.md` | Combined e-commerce SEO strategy document with all recommendations and priorities |

### Output Frontmatter

```yaml
---
client: "client-slug"
agent: "agent-name"
team: "ecommerce-seo"
date: YYYY-MM-DD
type: ecommerce
status: complete
platform: "shopify|woocommerce|magento|custom|other"
product-count: approximate
quality-score: 4
---
```

## Dependencies

- **Depends on:**
  - Client profile confirming e-commerce business with online store (must exist in vault)
  - **Technical SEO Team** (strongly recommended) — crawl data is the foundation; running Technical SEO first avoids duplicate crawling and provides the URL inventory, redirect map, and site structure data this team needs
  - **Keyword Research Team** (recommended) — keyword clusters inform category keyword targeting and product page optimization
  - **Competitor Analysis Team** (recommended) — competitor store structures and product strategies provide benchmarks

- **Feeds into:**
  - **Audit & Recommendations Team** — All e-commerce findings and recommendations feed into the master report
  - **Content SEO Team** — Category content needs may trigger content briefs for category page copy
  - **Technical SEO Team** — Faceted navigation fixes often require technical implementation (robots.txt, canonical tags, URL parameters)
  - **Analytics & Reporting Team** — Product page rankings, category traffic, and shopping feed performance become tracking metrics

## Quality Checks

### E-commerce SEO-Specific Quality Criteria

1. **Crawl budget awareness** — Every recommendation must consider its impact on crawl budget. Recommending that Google index every filter combination is never acceptable. The Faceted Navigation Auditor must provide a clear, implementable crawl control strategy that distinguishes between indexable and non-indexable URLs.

2. **Platform-specific recommendations** — All technical recommendations must be feasible on the client's e-commerce platform. Recommending .htaccess rules for a Shopify store (which does not support .htaccess) is a quality failure. Know the platform's capabilities and limitations.

3. **Scale-appropriate strategies** — Recommendations must be feasible at the client's scale. A store with 50 products can have hand-written unique descriptions. A store with 50,000 products needs a template-based approach with optimization focused on top revenue-generating products. Never recommend manual work at an impossible scale.

4. **Valid structured data** — All generated Product schema must be valid JSON-LD that passes Google's Rich Results Test. Include all required properties (name, image, price, availability) and all applicable recommended properties. Invalid schema is worse than no schema.

5. **Unique product content** — Product page optimization must address duplicate content from manufacturer descriptions. Recommendations must include strategies for creating unique product descriptions, at least for top-performing products. Simply stating "write unique descriptions" without a scalable strategy is insufficient.

6. **Category taxonomy logic** — Category structure recommendations must follow both user search behavior (how customers look for products) and keyword data (how people search). Category names should match high-volume keyword targets. Sub-category hierarchy should mirror keyword cluster structure.

7. **Shopping feed completeness** — Feed optimization must cover all required Google Merchant Center fields and address common disapproval reasons (missing GTINs, incorrect availability, image quality issues, category mismatches). Recommendations must be specific enough for the client's team to implement.

8. **Minimum quality score: 3/5. Target: 4/5+.**
