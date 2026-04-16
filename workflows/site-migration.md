# Site Migration
> **Teams involved:** Technical, Content, Analytics | **Steps:** 7 | **Estimated time:** 35–60 minutes

SEO-safe site migration planning and execution. Covers pre-migration crawl baselining, URL mapping, redirect strategy, indexation reconfiguration, content preservation, monitoring setup, and post-migration validation. Designed to preserve organic traffic and rankings during domain moves, platform changes, URL restructures, or HTTP/HTTPS migrations.

## What You'll Get
- Pre-migration crawl baseline with full URL inventory and ranking data
- Complete URL mapping document (old URL → new URL) with redirect rules
- Sitemap and canonical reconfiguration plan
- Updated meta tags for restructured pages
- Internal link audit and update plan
- Real-time monitoring dashboard specification
- Post-migration audit checklist with validation steps

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- Current site URL and new site URL (or new URL structure) documented
- Migration type identified (domain change, platform change, URL restructure, HTTP→HTTPS, subdomain consolidation)
- Timeline for migration established
- Access to current site for crawling (pre-migration snapshot critical)

## Steps

### Step 1: Pre-Migration Crawl Baseline
**Agent:** `agents/technical/site-crawler.md`
**Action:** Crawl the current site to establish the pre-migration baseline. This is the most critical step — everything in the migration depends on accurate current-state data. Capture: complete URL inventory with status codes, page titles, meta descriptions, H1 tags, and word counts; internal link graph (which pages link to which); external backlink landing pages (pages receiving inbound links — these MUST redirect correctly); current XML sitemap contents; robots.txt directives; canonical tag assignments; pages with highest organic traffic (from analytics or estimated via keyword rankings); and current indexation status. Store this baseline as the source of truth for the entire migration.
**Save to:** `vault/10-Technical/[client]-pre-migration-crawl.md`

### Step 2: URL Mapping & Redirect Strategy
**Agent:** `agents/technical/site-migration-specialist.md`
**Action:** Build the complete URL mapping document using the pre-migration crawl data. For every URL on the current site, define: the corresponding new URL, the redirect type (301 permanent for all ranking/linked pages), and redirect chain prevention rules. Prioritize: pages receiving external backlinks (highest priority — link equity preservation), pages ranking for target keywords, pages with highest traffic, and all remaining indexed pages. Handle edge cases: deleted pages (redirect to most relevant alternative), merged pages (consolidate with 301), split pages (redirect to primary and cross-link), and parameterized URLs. Generate implementation-ready redirect rules in the appropriate format (Apache .htaccess, Nginx conf, or platform-specific).
**Save to:** `vault/10-Technical/[client]-url-mapping.md`

### Step 3: Indexation Reconfiguration
**Agent:** `agents/technical/indexation-manager.md`
**Action:** Plan the indexation transition for the new site structure. Create: new XML sitemap reflecting the post-migration URL structure (remove old URLs, add new URLs, set appropriate priorities), updated robots.txt for the new domain/structure, canonical tag migration plan (all canonicals must point to new URLs), Search Console property setup for the new domain (if domain change), Change of Address tool submission plan (if domain change), and a timeline for sitemap submission and old sitemap removal. Define the indexation monitoring checklist for the first 30 days post-migration.
**Save to:** `vault/10-Technical/[client]-migration-indexation-plan.md`

### Step 4: Meta Tag Update
**Agent:** `agents/content/meta-tag-writer.md`
**Action:** Review and update meta tags for pages affected by the migration. If URLs are changing, ensure meta tags still reference the correct keywords and don't contain outdated URL references. If the migration includes a rebrand or content restructuring, write new meta titles and descriptions that align with the new site structure and brand positioning. Verify no meta tag content was lost or corrupted in the migration process. Provide a complete meta tag inventory for the post-migration site.
**Save to:** `vault/04-Content/[client]-migration-meta-tags.md`

### Step 5: Internal Link Architecture Update
**Agent:** `agents/technical/internal-linking-architect.md`
**Action:** Audit all internal links against the URL mapping from Step 2. Identify every internal link that points to an old URL and must be updated to point directly to the new URL (not through a redirect — internal links should never rely on redirects). Generate a page-by-page internal link update manifest. Check for: links in navigation menus, footer links, in-content links, sidebar links, breadcrumbs, and XML sitemap references. Verify the internal link structure maintains proper hierarchy and PageRank flow in the new architecture.
**Save to:** `vault/10-Technical/[client]-migration-internal-links.md`

### Step 6: Monitoring Dashboard Setup
**Agent:** `agents/analytics/dashboard-builder.md`
**Action:** Define the post-migration monitoring dashboard. Specify metrics to track during the critical 30-day post-migration window: crawl rate changes (Search Console), indexation count (old URLs dropping, new URLs being indexed), 404 error rate, redirect chain/loop errors, organic traffic daily trend vs. pre-migration baseline, ranking position changes for top 50 keywords, Core Web Vitals on the new site, and referral traffic from backlinks (are redirects passing traffic?). Set alert thresholds: what percentage drop in traffic triggers investigation, what 404 spike rate is acceptable, and when to escalate. Provide a daily, weekly, and monthly monitoring checklist.
**Save to:** `vault/07-Reports/[client]-migration-monitoring-plan.md`

### Step 7: Post-Migration Validation Audit
**Agent:** `agents/technical/site-migration-specialist.md`
**Action:** Define the post-migration validation protocol to run once the migration is live. Create a comprehensive checklist: crawl the new site and compare URL count against pre-migration baseline, verify every redirect works (spot-check critical pages, bulk-test via script), confirm no redirect chains or loops exist, validate XML sitemap is submitted and being crawled, check robots.txt is not accidentally blocking critical pages, verify canonical tags point to correct new URLs, confirm Search Console shows new pages being indexed, test structured data on new URLs (Rich Results Test), verify analytics tracking is firing on all pages, and check for mixed content warnings (HTTP resources on HTTPS pages). Include a timeline: what to check on Day 1, Day 7, Day 14, and Day 30.
**Save to:** `vault/10-Technical/[client]-post-migration-checklist.md`

### Final Delivery
1. Run quality gate (`quality/qa-checklist.md`) on all migration documents
2. Verify all URL mappings reference real URLs from the crawl data
3. Save complete migration package to `output/[client]/[date]/technical/site-migration/`
4. Include redirect rules file in implementation-ready format
5. Update vault dashboard (`vault/00-Dashboard/`)
6. Update ROI tracker — log site migration SEO package with estimated agency value ($3,000–$6,000)
