# Local SEO Setup
> **Teams involved:** Local, Content, Keywords | **Steps:** 5 | **Estimated time:** 20–35 minutes

Complete local SEO foundation buildout for businesses serving specific geographic areas. Covers competitor benchmarking, Google Business Profile optimization, citation building, localized content creation, and review strategy.

## What You'll Get
- Local competitor landscape analysis with ranking comparison
- Fully optimized Google Business Profile (GBP) recommendations
- Citation building plan with NAP consistency audit and directory targets
- Locally-optimized content pieces (location pages, local blog posts, service area content)
- Review generation and reputation management strategy

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- Business address, service areas, and phone number documented
- Business category and primary local keywords identified
- Google Business Profile access (or plan to create one)

## Steps

### Step 1: Local Competitor Analysis
**Agent:** `agents/local/local-competitor-analyst.md`
**Action:** Research the local competitive landscape for the client's primary service area and business category. Using Tavily and Web Search, identify: the top 5 local competitors for each target keyword, their GBP ranking positions in the local pack, their review counts and average ratings, their citation presence across major directories, and their local content strategy (location pages, local blog posts, local schema). Benchmark the client's current local SEO standing against each competitor. Identify gaps and advantages.
**Save to:** `vault/09-Local/[client]-local-competitors.md`

### Step 2: Google Business Profile Optimization
**Agent:** `agents/local/gbp-optimizer.md`
**Action:** Audit and optimize the client's Google Business Profile. Generate recommendations for: business name, category selection (primary + secondary), business description (keyword-optimized, 750 characters), attributes selection, service/product catalog setup, photo optimization strategy (types, naming, geotagging), Q&A seeding with target keywords, posting strategy (frequency, content types, CTAs), and GBP features utilization (booking, messaging, products). Provide the complete optimized GBP content ready for implementation.
**Save to:** `vault/09-Local/[client]-gbp-optimization.md`

### Step 3: Citation Building Plan
**Agent:** `agents/local/citation-builder.md`
**Action:** Audit existing citations for NAP (Name, Address, Phone) consistency across the web. Identify discrepancies in business name spelling, address format, phone number, and website URL. Build a prioritized citation submission plan targeting: top general directories (Google, Bing, Apple Maps, Yelp, Facebook), industry-specific directories relevant to the client's niche, local directories for the client's city/region, and data aggregators (Foursquare, Data Axle). For each directory, note submission URL, expected approval time, and dofollow/nofollow status.
**Save to:** `vault/09-Local/[client]-citations.md`

### Step 4: Local Content Creation
**Agent:** `agents/local/local-content-writer.md`
**Action:** Create locally-optimized content tailored to the client's service areas. Write: a primary location page for the main service area (1,000–1,500 words), service area pages for secondary locations (500–800 words each), 2–3 locally-focused blog post drafts (local events, community involvement, area-specific tips), and locally-optimized meta tags for all pages. All content must incorporate local keywords naturally, mention local landmarks, neighborhoods, and geographic identifiers, and include LocalBusiness schema markup recommendations.
**Save to:** `vault/09-Local/[client]-local-content/` (one file per page)

### Step 5: Review Generation Strategy
**Agent:** `agents/local/review-strategist.md`
**Action:** Develop a review generation and reputation management plan. Include: review acquisition tactics (email sequences, in-store signage, receipt QR codes, SMS follow-ups), timing recommendations for review requests (when customers are most likely to respond), review response templates for positive reviews (thanking, reinforcing keywords), review response templates for negative reviews (professional, solution-oriented, offline resolution), a monitoring plan for new reviews across platforms, and a strategy for earning reviews on industry-specific platforms beyond Google. Set monthly review targets based on competitor benchmarks from Step 1.
**Save to:** `vault/09-Local/[client]-review-strategy.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on all deliverables
2. Verify all directory URLs are real and currently accepting submissions
3. Save complete local SEO package to `output/[client]/[date]/local/`
4. Update vault dashboard (`vault/00-Dashboard/`)
5. Update ROI tracker — log local SEO setup with estimated agency value ($1,500–$2,500)
