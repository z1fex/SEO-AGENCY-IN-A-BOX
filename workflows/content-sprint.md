# Content Sprint
> **Teams involved:** Keywords, Content | **Steps:** 8 | **Estimated time:** 30–60 minutes

Rapid content production pipeline. Takes a batch of topics from calendar through SERP research, brief creation, writing, optimization, and quality assurance. Designed to produce 4–8 publish-ready SEO articles in a single session.

## What You'll Get
- Content calendar with prioritized topics and publishing schedule
- SERP-informed content briefs for each piece
- Fully written SEO blog posts (1,500–2,500 words each)
- Optimized meta titles and descriptions for every page
- FAQ sections with People Also Ask coverage
- Content optimization scores with improvement recommendations
- All content passing quality gate

## Prerequisites
- Client profile exists in `vault/01-Clients/[client]/profile.md`
- Brand voice guide at `vault/01-Clients/[client]/brand-voice.md`
- Keyword strategy or clusters at `vault/03-Research/[client]/keyword-clusters.md` (run `keyword-strategy` workflow first if missing)
- Target topic list or content calendar already planned

## Steps

### Step 1: Content Calendar Planning
**Agent:** `agents/content/content-calendar-planner.md`
**Action:** Review existing keyword clusters and content gaps. Select 4–8 topics for this sprint based on priority (quick wins first: high search volume, low difficulty, strong business relevance). Assign each topic a target keyword cluster, content type, word count target, and publish date. Check for seasonal relevance and trending opportunities.
**Save to:** `vault/04-Content/[client]/calendar/sprint-calendar.md`

### Step 2: SERP Research
**Agent:** `agents/keywords/serp-analyzer.md`
**Action:** For each topic in the sprint calendar, analyze the top 10 SERP results. Document: what content format ranks (guide, listicle, comparison, etc.), average word count of ranking pages, common headings and subtopics covered, SERP features present, and content freshness signals. Identify what the top results do well and where they fall short.
**Save to:** `vault/03-Research/[client]/sprint-serp-analysis.md`

### Step 3: Brief Writing
**Agent:** `agents/content/brief-writer.md`
**Action:** Create detailed content briefs for each sprint article using SERP data from Step 2. Each brief includes: target keyword and secondary keywords, search intent, recommended title options, H2/H3 heading outline, key points to cover (sourced from SERP analysis), word count target, internal linking targets, competitor content to beat, unique angle or value-add differentiator.
**Save to:** `vault/04-Content/[client]/briefs/` (one file per brief)

### Step 4: SEO Blog Writing
**Agent:** `agents/content/seo-blog-writer.md`
**Action:** Write each article following its brief from Step 3. Apply the client's brand voice from `vault/01-Clients/[client]/brand-voice.md`. Each article must: hit the target word count, naturally incorporate primary and secondary keywords, follow the approved heading structure, include original insights or analysis (not just rewriting competitors), use short paragraphs and clear formatting, include a compelling introduction and actionable conclusion.
**Save to:** `vault/04-Content/[client]/drafts/` (one file per article)

### Step 5: Meta Tag Writing
**Agent:** `agents/content/meta-tag-writer.md`
**Action:** Write optimized meta titles and descriptions for each article. Meta titles: include primary keyword, stay under 60 characters, be compelling enough to earn the click. Meta descriptions: include primary keyword naturally, stay under 155 characters, include a clear value proposition and call to action. Write 2–3 title and description variants for A/B testing.
**Save to:** `vault/04-Content/[client]/meta-tags/sprint-meta-tags.md`

### Step 6: FAQ & PAA Section Writing
**Agent:** `agents/content/faq-paa-writer.md`
**Action:** For each article, research People Also Ask questions and related queries using Tavily. Write FAQ sections with 4–6 questions per article. Answers must be concise (40–60 words for featured snippet targeting), factually accurate, and naturally incorporate secondary keywords. Structure FAQs with proper FAQ schema markup recommendations.
**Save to:** `vault/04-Content/[client]/faqs/sprint-faqs.md`

### Step 7: Content Optimization
**Agent:** `agents/content/content-optimizer.md`
**Action:** Run each completed article through optimization checks. Verify: keyword placement in title, H1, first 100 words, and throughout; readability score (target Grade 8 or lower); internal linking implemented per brief; image alt text recommendations; NLP entity coverage compared to top SERP results; content uniqueness and value-add over competitors. Score each piece and flag specific improvements.
**Save to:** `vault/04-Content/[client]/optimization/sprint-scores.md`

### Step 8: Quality Gate
**Agent:** `agents/_base/quality-gate.md`
**Action:** Run the full quality checklist on every article. Verify brand voice consistency, factual accuracy (no hallucinated statistics or claims), search intent alignment, completeness (no placeholder text, no TODOs, no generic filler), and E-E-A-T signals. Any article scoring below 3/5 goes back to Step 4 for revision.
**Save to:** `vault/04-Content/[client]/sprint-qa-results.md`

### Final Delivery
1. Compile all passing articles with their meta tags and FAQ sections
2. Save final articles to `output/[client]/[date]/content/sprint/`
3. Save meta tags to `output/[client]/[date]/content/meta-tags.md`
4. Update content calendar status in vault
5. Update vault dashboard (`vault/00-Dashboard/`)
6. Update ROI tracker — log articles produced with estimated agency value ($500–$800 per article)
