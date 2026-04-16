# SEO Fundamentals — Shared Knowledge Base

> Core SEO principles that every agent in this agency must understand and follow.

---

## Current SEO Landscape (2025-2026)

### What Matters Now
1. **E-E-A-T** — Experience, Expertise, Authoritativeness, Trustworthiness. Google's quality framework for evaluating content.
2. **Search Intent** — Content MUST match what the searcher actually wants. Informational queries need guides, not product pages.
3. **Topical Authority** — Comprehensive coverage of a topic cluster ranks better than isolated pages.
4. **Core Web Vitals** — LCP <2.5s, INP <200ms, CLS <0.1. Page experience matters.
5. **Mobile-First** — Google crawls and indexes the mobile version of your site first.
6. **AI Search (AEO)** — Google AI Overviews, Perplexity, ChatGPT Search are changing how people find information. Optimize for both traditional and AI search.
7. **Entity SEO** — Search engines understand entities (people, places, things), not just keywords. Build entity relationships.
8. **Structured Data** — JSON-LD schema helps search engines understand your content. Required for rich results.

### What No Longer Works
- Keyword density targets (there is no magic percentage)
- Exact-match anchor text manipulation
- Private Blog Networks (PBNs)
- Article spinning or thin content at scale
- Keyword stuffing in meta tags or content
- Buying links without nofollow/sponsored attributes
- Cloaking or hidden text
- Doorway pages
- Comment spam or forum spam for links

---

## Core Ranking Factors

### On-Page
- **Title tag** — Primary keyword near the front, ≤60 characters, compelling for clicks
- **Meta description** — Not a ranking factor, but affects CTR. ≤155 chars, include CTA
- **H1 tag** — One per page, includes primary keyword naturally
- **Heading hierarchy** — H1 → H2 → H3, logical nesting, no skipping levels
- **Content quality** — Comprehensive, original, well-researched, answers the query
- **Internal links** — Connect related pages, distribute link equity, help crawlability
- **URL structure** — Short, descriptive, includes keywords, uses hyphens
- **Image optimization** — Descriptive file names, alt text, compressed, WebP format
- **Schema markup** — JSON-LD structured data for rich results

### Technical
- **Crawlability** — No blocked important pages, clean robots.txt, valid sitemaps
- **Indexability** — Proper canonical tags, no unintended noindex, index coverage clean
- **Page speed** — Core Web Vitals passing, optimized images, minimal render-blocking
- **Mobile-friendly** — Responsive design, proper viewport, readable without zoom
- **HTTPS** — SSL certificate, no mixed content
- **Site architecture** — Flat hierarchy (important pages within 3 clicks of homepage)

### Off-Page
- **Backlinks** — Quality over quantity. Editorial links from relevant, authoritative sites
- **Brand signals** — Brand searches, mentions, social presence
- **E-E-A-T signals** — Author credentials, cited sources, real-world expertise

### AEO (Answer Engine Optimization)
- **Concise answers** — Clear, direct answers that AI can cite (40-60 words for snippets)
- **Entity optimization** — Consistent entity naming, schema markup, knowledge graph presence
- **Source authority** — Being THE primary source on a topic
- **Structured content** — Well-organized content with clear sections, lists, tables
- **Freshness** — Up-to-date information that AI models can trust

---

## Search Intent Framework

| Intent | User Goal | Content Type | Keywords Signals |
|--------|-----------|-------------|-----------------|
| **Informational** | Learn something | Blog posts, guides, tutorials, wiki pages | "how to", "what is", "guide", "tutorial", "why" |
| **Commercial Investigation** | Compare options | Comparison pages, reviews, listicles | "best", "vs", "review", "top", "comparison" |
| **Transactional** | Buy/act | Product pages, landing pages, pricing pages | "buy", "price", "discount", "order", "near me" |
| **Navigational** | Find a specific site | Homepage, brand pages | Brand names, product names, "[brand] login" |

**Golden rule:** Match content type to intent. Don't serve a blog post to someone searching "buy [product]".

---

## Content Quality Standards

### E-E-A-T Checklist
- [ ] **Experience** — Content demonstrates first-hand experience with the topic
- [ ] **Expertise** — Author has demonstrable knowledge (credentials, bio, body of work)
- [ ] **Authoritativeness** — Site is recognized as an authority in this space
- [ ] **Trustworthiness** — Accurate information, cited sources, transparent authorship

### Content Formatting
- Short paragraphs (3-4 sentences max)
- Bullet and numbered lists for scanability
- Tables for comparisons
- Headers every 200-300 words
- Images/visuals to break up text
- Internal links to related content
- External links to authoritative sources

---

## Schema Markup Reference

### Most Common Types
| Schema Type | Use On | Rich Result |
|-------------|--------|-------------|
| `Article` | Blog posts, news | Article rich result |
| `FAQPage` | FAQ sections | FAQ dropdown in SERP |
| `HowTo` | Step-by-step guides | How-to rich result |
| `Product` | Product pages | Product rich result (price, availability, rating) |
| `LocalBusiness` | Local business pages | Local business panel |
| `Organization` | About/homepage | Knowledge panel |
| `BreadcrumbList` | All pages | Breadcrumb trail in SERP |
| `WebSite` | Homepage | Sitelinks search box |
| `Review`/`AggregateRating` | Review pages | Star ratings in SERP |
| `Event` | Event pages | Event rich result |
| `VideoObject` | Video pages | Video rich result |

### Implementation
- Always use JSON-LD format (Google's preference)
- Place in `<head>` or `<body>` of the HTML
- Validate with Google's Rich Results Test
- Only mark up content visible on the page (no hidden schema)

---

## Technical SEO Benchmarks

| Metric | Good | Needs Work | Poor |
|--------|------|------------|------|
| LCP | <2.5s | 2.5-4.0s | >4.0s |
| INP | <200ms | 200-500ms | >500ms |
| CLS | <0.1 | 0.1-0.25 | >0.25 |
| Time to First Byte | <200ms | 200-600ms | >600ms |
| Crawl Depth | ≤3 clicks | 4-5 clicks | 6+ clicks |
| 404 Error Rate | <1% | 1-5% | >5% |
| Redirect Chains | 0 | 1-2 hops | 3+ hops |
| Mobile Score | 90+ | 50-89 | <50 |
