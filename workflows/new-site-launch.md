# New Site Launch
> **Teams involved:** Strategy, Keywords, Technical, Content | **Steps:** 8 | **Estimated time:** 40–70 minutes

SEO foundation buildout for a brand new website or major site redesign. Establishes the keyword strategy, content architecture, technical SEO foundation, and initial content before launch to ensure the site is indexed and ranking as fast as possible.

## What You'll Get
- Complete keyword universe with clusters and intent mapping
- Content architecture plan (pillar pages, supporting content, hub structure)
- Content strategy with 90-day publishing roadmap
- Schema markup plan and templates for all page types
- Indexation strategy (sitemaps, robots.txt, canonical plan)
- Initial batch of SEO-optimized blog posts
- Meta tags for all launch pages
- Pre-launch SEO checklist and post-launch monitoring plan

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- Business model, target audience, and core offerings documented
- Site structure or wireframes available (or being designed concurrently)
- Brand voice guide at `vault/01-Clients/[client]/brand-voice.md`

## Steps

### Step 1: Keyword Discovery
**Agent:** `agents/keywords/keyword-discovery.md`
**Action:** Conduct comprehensive keyword research for the new site's niche. Since there's no existing keyword baseline, start from the client's core offerings, target audience pain points, and competitor analysis. Use Tavily for broad discovery. Identify: primary commercial keywords (products/services), informational keywords (education and top-of-funnel), long-tail opportunities with lower competition (important for a new domain with low authority), question-based queries for content, and branded keyword variations. Target 300+ keyword opportunities across all intent types.
**Save to:** `vault/03-Research/[client]-keyword-universe.md`

### Step 2: Keyword Clustering
**Agent:** `agents/keywords/cluster-builder.md`
**Action:** Organize the keyword universe into topical clusters. Each cluster becomes a content hub on the site. Define: pillar topics (5–10 core themes the site will own), supporting subtopics within each pillar (10–20 per cluster), the hub-and-spoke internal linking model, primary keyword assignment per page, and secondary/tertiary keyword mapping. The cluster map directly informs the site's information architecture and navigation structure.
**Save to:** `vault/03-Research/[client]-keyword-clusters.md`

### Step 3: Content Strategy & Architecture
**Agent:** `agents/content/content-strategist.md`
**Action:** Transform keyword clusters into a complete content architecture and publishing strategy. Define: page types needed (pillar pages, category pages, service pages, blog posts, resource pages, landing pages), content format for each page (guide, listicle, comparison, case study, tool), word count and depth targets per page type, the site's content hierarchy and navigation structure, a 90-day content calendar prioritizing pages that target low-competition/high-intent keywords first (a new site can't compete for head terms immediately), and internal linking blueprint connecting all content pieces.
**Save to:** `vault/04-Content/[client]-content-architecture.md`

### Step 4: Schema Markup Plan
**Agent:** `agents/technical/schema-specialist.md`
**Action:** Design the structured data strategy for the new site. Create schema templates for every page type: Organization schema (homepage), WebSite schema with SearchAction (sitelinks search box), BreadcrumbList (all pages), Article/BlogPosting (blog posts), FAQPage (FAQ sections), HowTo (tutorial content), Product (if e-commerce), LocalBusiness (if local), Service (service pages), and Person (author pages for E-E-A-T). Provide implementable JSON-LD code blocks for each template. Document where each schema type should be deployed.
**Save to:** `vault/10-Technical/[client]-schema-plan.md`

### Step 5: Indexation Strategy
**Agent:** `agents/technical/indexation-manager.md`
**Action:** Set up the technical indexation foundation for the new site. Create: XML sitemap structure (which pages to include, priority and changefreq values), robots.txt configuration (crawl directives, sitemap reference, blocked paths for staging/admin/duplicate content), canonical URL strategy (trailing slashes, www vs. non-www, HTTP vs. HTTPS), Search Console setup checklist, and initial index request plan (which pages to submit first). Include a noindex strategy for thin pages, tag pages, author archives, and other low-value URLs that shouldn't consume crawl budget.
**Save to:** `vault/10-Technical/[client]-indexation-plan.md`

### Step 6: Initial Blog Posts
**Agent:** `agents/content/seo-blog-writer.md`
**Action:** Write the first batch of 4–6 SEO blog posts targeting long-tail, lower-competition keywords from the content strategy. For a new domain, these initial posts should: target informational intent keywords with manageable difficulty, establish topical authority in the site's core pillars, be comprehensive (1,500–2,500 words), follow E-E-A-T best practices (demonstrate expertise), include internal links to pillar pages and service pages, and serve as the foundation for the site's content hub structure. Apply the client's brand voice throughout.
**Save to:** `vault/04-Content/[client]-launch-posts/` (one file per post)

### Step 7: Meta Tag Writing
**Agent:** `agents/content/meta-tag-writer.md`
**Action:** Write optimized meta titles and descriptions for all launch pages: homepage, service/product pages, pillar pages, blog posts from Step 6, about page, contact page, and any category pages. Each meta title targets the assigned primary keyword, stays under 60 characters, and differentiates the brand. Each meta description includes the primary keyword, stays under 155 characters, and includes a clear value proposition. Provide 2 variants per page for future A/B testing.
**Save to:** `vault/04-Content/[client]-launch-meta-tags.md`

### Step 8: Launch Roadmap
**Agent:** `agents/strategy/roadmap-planner.md`
**Action:** Compile all pre-launch and post-launch SEO activities into a single roadmap. **Pre-Launch Checklist:** technical SEO setup, schema implementation, meta tags, sitemap submission, robots.txt deployment, analytics/Search Console setup, initial content publishing. **Launch Week:** index submission plan, social signals, initial link building, performance monitoring setup. **30-Day Post-Launch:** content publishing cadence, link building activation, ranking monitoring, technical issue resolution. **60–90 Day Plan:** content velocity targets, link building targets, ranking milestones, first monthly report. Include specific KPIs and success metrics for each phase.
**Save to:** `vault/08-Strategy/[client]-launch-roadmap.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on all deliverables
2. Verify keyword data from Tavily, technical recommendations are implementation-ready
3. Save complete launch package to `output/[client]/[date]/strategy/new-site-launch/`
4. Update vault dashboard (`vault/00-Dashboard/`)
5. Update ROI tracker — log new site launch SEO package with estimated agency value ($4,000–$7,000)
