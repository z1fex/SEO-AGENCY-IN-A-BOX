# E-commerce SEO Audit
> **Teams involved:** E-commerce, Technical, Keywords | **Steps:** 6 | **Estimated time:** 25–40 minutes

Specialized audit for e-commerce sites covering the unique SEO challenges of online stores: faceted navigation, category architecture, product page optimization, structured data, and shopping feeds. Produces a prioritized action plan for improving organic product visibility.

## What You'll Get
- Faceted navigation audit with crawl budget and duplicate content recommendations
- Category page architecture strategy with keyword targeting
- Product page SEO optimization checklist with page-level recommendations
- Product schema markup templates and validation results
- Shopping feed optimization report (Google Merchant Center, free listings)
- Prioritized e-commerce SEO action plan with effort/impact scoring

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- E-commerce site URL with product catalog accessible
- Product category structure documented (or discoverable via crawl)
- Competitor e-commerce sites identified in `vault/01-Clients/[client]/competitors.md`

## Steps

### Step 1: Faceted Navigation Audit
**Agent:** `agents/ecommerce/faceted-navigation-auditor.md`
**Action:** Audit the site's faceted navigation for SEO impact using Firecrawl crawl data. Analyze: how filters generate URLs (query parameters, subdirectories, JavaScript-only), crawl budget waste from faceted URLs, duplicate and near-duplicate content created by filter combinations, canonicalization strategy for filtered pages, robots.txt and meta robots treatment of faceted URLs, internal link equity dilution from faceted pages, and indexation status of faceted URLs. Recommend a faceted navigation strategy: which filter combinations to allow indexing (high search volume, unique content), which to block (low value, duplicate), and the optimal technical implementation (canonical tags, robots.txt, noindex, URL parameter handling in Search Console).
**Save to:** `vault/10-Technical/[client]-faceted-nav-audit.md`

### Step 2: Category Strategy
**Agent:** `agents/ecommerce/category-strategist.md`
**Action:** Audit and optimize the category page architecture. Using keyword data from vault (or run keyword discovery if missing), analyze: current category hierarchy and depth, keyword targeting per category page, category page content quality (thin vs. rich), subcategory structure alignment with search demand, category URL structure and breadcrumbs, cross-category linking opportunities, and gap categories where search demand exists but no category page serves it. Deliver a recommended category taxonomy optimized for both search and user navigation, with target keywords, content requirements, and internal linking plans for each category level.
**Save to:** `vault/04-Content/[client]-category-strategy.md`

### Step 3: Product Page Optimization
**Agent:** `agents/ecommerce/product-page-optimizer.md`
**Action:** Audit a representative sample of product pages (10–20 across categories) using Firecrawl scraping. Evaluate: title tag optimization (brand + product + key attribute + category), meta description quality, H1 tag usage, product description uniqueness and depth, image optimization (alt text, file names, compression, lazy loading), user-generated content (reviews, Q&A), related/cross-sell product linking, out-of-stock page handling, product variant/color/size URL strategy, and page load performance. Produce a product page SEO template with optimized element specifications that can be applied site-wide.
**Save to:** `vault/04-Content/[client]-product-page-audit.md`

### Step 4: Product Schema Generation
**Agent:** `agents/ecommerce/product-schema-generator.md`
**Action:** Audit existing product structured data and generate optimized schema markup. Validate current Product schema against Google's requirements for rich results (price, availability, reviews, images). Identify missing schema properties that could enhance SERP appearance (aggregateRating, offers, brand, sku, gtin, color, size). Generate Product schema templates for each product type in the catalog. Include supplementary schema types: BreadcrumbList for navigation, Organization for the store, FAQPage for product FAQs, and Review schema. Test all schema against Google's Rich Results Test specifications.
**Save to:** `vault/10-Technical/[client]-product-schema.md`

### Step 5: Shopping Feed Optimization
**Agent:** `agents/ecommerce/shopping-feed-optimizer.md`
**Action:** Audit and optimize the product data feed for Google Merchant Center and free product listings. Review: product title optimization (keyword-rich, attribute-inclusive format), product description quality, product category mapping to Google's taxonomy, image quality and compliance, price and availability accuracy, GTIN/MPN/brand data completeness, custom label strategy for campaign segmentation, and feed error/warning resolution. Provide feed optimization recommendations that maximize free listing visibility and improve Shopping ad quality scores.
**Save to:** `vault/04-Content/[client]-shopping-feed-audit.md`

### Step 6: Priority Action Plan
**Agent:** `agents/strategy/priority-matrix-builder.md`
**Action:** Synthesize all e-commerce audit findings from Steps 1–5 into a prioritized action plan. Score each recommendation on two axes: SEO impact (estimated traffic/revenue uplift) and implementation effort (development hours, content creation time). Organize into four quadrants: Quick Wins (high impact, low effort — do first), Strategic Projects (high impact, high effort — plan and resource), Low-Hanging Fruit (low impact, low effort — batch together), and Deprioritize (low impact, high effort — skip or defer). Deliver a 90-day implementation roadmap with weekly milestones.
**Save to:** `vault/08-Strategy/[client]-ecommerce-priority-matrix.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on all deliverables
2. Verify all product and technical data comes from Firecrawl results (no hallucinated URLs or metrics)
3. Save complete e-commerce audit to `output/[client]/[date]/audit/ecommerce-audit.md`
4. Save schema templates to `output/[client]/[date]/audit/schema-templates/`
5. Update vault dashboard (`vault/00-Dashboard/`)
6. Update ROI tracker — log e-commerce audit with estimated agency value ($2,500–$4,000)
