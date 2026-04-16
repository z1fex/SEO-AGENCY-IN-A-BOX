# SEO Client Onboarding

> Interview the client, understand their business and SEO needs, create their complete profile in vault.

---

## How This Works

Ask questions in phases. Don't dump all questions at once — have a conversation. After the interview, create 5 files in the client's vault folder.

---

## Phase 1 — Business Basics (5 questions)

Ask these one at a time, conversationally:

1. **What's your company name and website URL?**
2. **What do you sell or offer? Who buys it?**
   - Products, services, SaaS, e-commerce, local business, etc.
3. **How long have you been in business? Team size?**
4. **What's your current estimated monthly organic traffic?**
   - Even a rough estimate helps. "No idea" is fine — we'll find out.
5. **What CMS/platform is your site built on?**
   - WordPress, Shopify, Webflow, Wix, custom, etc.
   - This determines what technical changes are possible.

---

## Phase 2 — SEO History (4 questions)

1. **Have you done SEO before?**
   - Agency, in-house, freelancer, DIY, or never?
2. **What's worked in the past? What hasn't?**
   - Previous wins, failures, wasted investments
3. **Do you have access to Google Search Console and Google Analytics?**
   - If yes, we can pull real data. If no, we work with what we have.
4. **Any technical constraints we should know about?**
   - Can't change code, limited CMS, shared hosting, IT approval needed, etc.

---

## Phase 3 — Competition (3 questions)

1. **Who are your top 3-5 SEO competitors?** (provide URLs if possible)
   - These may differ from business competitors — we want sites ranking for your target keywords
2. **Who's currently winning in organic search in your space?**
   - Who shows up when you search for your main keywords?
3. **What keywords would you love to rank for?**
   - Dream keywords, even if competitive. Also practical ones.

---

## Phase 4 — Goals & Priorities (4 questions)

1. **What are your top 3 SEO goals?**
   - More organic traffic? More leads? More sales? Local visibility? Brand awareness?
2. **What specific keywords or topics matter most?**
   - High-priority keywords, product categories, service pages
3. **What does success look like in 90 days?**
   - Specific, measurable outcomes. "More traffic" isn't enough — how much more?
4. **Budget context?**
   - Content budget (can you pay writers?), tool budget, time investment
   - This helps us recommend realistic strategies

---

## Phase 5 — Content & Brand (3 questions)

1. **What's your brand voice?**
   - Formal or casual? Technical or simple? Authoritative or friendly?
   - Any words/phrases you love or hate?
2. **Do you have existing content? How much?**
   - Blog posts, guides, landing pages, videos, etc.
   - Rough count helps us plan content audits
3. **Who creates content today?**
   - In-house team, freelancers, agency, nobody yet?

---

## After the Interview — Create 5 Files

Create a folder at `vault/01-Clients/[company-name]/` (lowercase, hyphens for spaces).

### File 1: `profile.md`
```markdown
---
client: "{{company-slug}}"
type: profile
created: {{date}}
status: active
tags: [#client, #profile]
---

# {{Company Name}} — Client Profile

## Business Overview
- **Company:** {{name}}
- **Website:** {{url}}
- **Industry:** {{industry}}
- **Founded:** {{year}}
- **Team Size:** {{size}}
- **Business Model:** {{B2B/B2C/Both}}
- **Products/Services:** {{what they sell}}

## Current State
- **Estimated Monthly Organic Traffic:** {{traffic}}
- **CMS/Platform:** {{platform}}
- **SEO History:** {{previous SEO work}}
- **Technical Constraints:** {{limitations}}
- **Analytics Access:** {{GSC/GA status}}

## Key Notes
{{anything important from the conversation}}
```

### File 2: `site-info.md`
```markdown
---
client: "{{company-slug}}"
type: site-info
created: {{date}}
tags: [#client, #technical]
---

# {{Company Name}} — Site Information

## Technical Details
- **URL:** {{url}}
- **CMS:** {{platform}}
- **Hosting:** {{if known}}
- **SSL:** {{yes/no}}
- **CDN:** {{if known}}

## Access
- **Google Search Console:** {{yes/no/pending}}
- **Google Analytics:** {{yes/no/pending — GA4 or UA}}
- **CMS Admin:** {{yes/no/pending}}
- **Server Access:** {{yes/no/pending}}

## Technical Constraints
{{list any limitations — can't edit code, limited plugins, etc.}}

## Known Technical Issues
{{any issues mentioned during onboarding}}
```

### File 3: `competitors.md`
```markdown
---
client: "{{company-slug}}"
type: competitors
created: {{date}}
tags: [#client, #competitor]
---

# {{Company Name}} — SEO Competitors

## Identified Competitors

| # | Competitor | URL | Notes |
|---|-----------|-----|-------|
| 1 | {{name}} | {{url}} | {{why they're a competitor}} |
| 2 | {{name}} | {{url}} | {{notes}} |
| 3 | {{name}} | {{url}} | {{notes}} |
| 4 | {{name}} | {{url}} | {{notes}} |
| 5 | {{name}} | {{url}} | {{notes}} |

## Who's Winning
{{who currently dominates organic search in this space}}

## Competitive Notes
{{any insights from the client about competitors}}

*Full competitor analysis to be done by Competitor Analysis team*
```

### File 4: `goals.md`
```markdown
---
client: "{{company-slug}}"
type: goals
created: {{date}}
tags: [#client, #strategy]
---

# {{Company Name}} — SEO Goals

## Top 3 Goals
1. {{goal 1 — specific and measurable}}
2. {{goal 2}}
3. {{goal 3}}

## Target Keywords
{{list of dream/priority keywords from the client}}

## 90-Day Success Criteria
{{what success looks like in 90 days — specific metrics}}

## Budget Context
- **Content Budget:** {{what they can invest in content}}
- **Tool Budget:** {{what they can invest in tools}}
- **Time Investment:** {{hours/week they can dedicate}}

## Priorities
{{what they want to work on first}}

## What Has NOT Worked
{{previous failures to avoid repeating}}
```

### File 5: `brand-voice.md`
```markdown
---
client: "{{company-slug}}"
type: brand-voice
created: {{date}}
tags: [#client, #content]
---

# {{Company Name}} — Brand Voice Guide

## Tone
- **Formality:** {{formal / professional / conversational / casual}}
- **Technical Level:** {{expert / intermediate / beginner-friendly}}
- **Personality:** {{3-5 adjectives — e.g., authoritative, friendly, data-driven}}

## Writing Style
- **Sentence Length:** {{short and punchy / medium / long and detailed}}
- **Vocabulary:** {{simple / industry-standard / technical}}
- **POV:** {{first person "we" / third person / second person "you"}}

## Do's
- {{word/phrase/style to use}}
- {{another}}

## Don'ts
- {{word/phrase/style to avoid}}
- {{another}}

## Content Examples
{{links to content they like, or descriptions of style they want}}

## Existing Content Volume
- **Blog Posts:** {{count or estimate}}
- **Landing Pages:** {{count}}
- **Other:** {{videos, guides, etc.}}

## Who Creates Content
{{in-house, freelancers, agency, nobody}}
```

---

## After Creating Client Files — Initialize Vault

Create ALL client subfolders so every team can write without errors:

```
vault/02-Audits/[client]/
vault/03-Research/[client]/
vault/04-Content/[client]/
vault/04-Content/[client]/briefs/
vault/04-Content/[client]/drafts/
vault/04-Content/[client]/published/
vault/04-Content/[client]/meta-tags/
vault/05-Links/[client]/
vault/05-Links/[client]/prospects/
vault/05-Links/[client]/outreach/
vault/05-Links/[client]/placements/
vault/06-Competitors/[client]/
vault/07-Reports/[client]/
vault/07-Reports/[client]/monthly/
vault/07-Reports/[client]/quarterly/
vault/08-Strategy/[client]/
vault/09-Local/[client]/           (if local business)
vault/10-Technical/[client]/
vault/10-Technical/[client]/crawl-data/
vault/11-AEO/[client]/
```

Also create the output folder:
```
output/[client]/
```

---

## After Vault Initialization

1. Confirm the profile with the client: "Here's what I have — anything to correct?"
2. Update the agency dashboard: `vault/00-Dashboard/Agency Dashboard.md` — add the new client
3. Ask the client: **"Want me to run a full audit now?"**
   - If yes → Run `go` (the auto-pilot command — full audit + report)
   - If they want something specific:
     - New to SEO → `audit` (full SEO audit)
     - Have content but no rankings → `keywords` + `content sprint`
     - Technical issues suspected → `run technical`
     - Want to outrank competitors → `competitor teardown [url]`
     - Local business → `local seo`
     - E-commerce → `audit ecommerce`
4. If the client just wants to explore first, show them available commands from CLAUDE.md

---

## Quick Onboard Mode

If the user just provides a URL without wanting the full interview:

1. Accept the URL
2. Use Firecrawl `map` to get site overview
3. Use Web Fetch to read the homepage, about page, and a few key pages
4. Auto-fill what you can: company name, industry, products/services, CMS (from HTML)
5. Ask only the 5 most critical questions:
   - What are your top 3 SEO goals?
   - Who are your top 3 competitors?
   - What keywords matter most to you?
   - Brand voice: formal or casual?
   - Any technical constraints?
6. Create the 5 client files with auto-filled + answered data
7. Initialize all vault folders
8. Recommend next step (or auto-run `go`)

---

## Rules

- **Never leave placeholders** — Every field gets a real answer or "To be determined — will research"
- **Ask follow-up questions** if answers are vague — specificity matters
- **Don't overwhelm** — Conversational pace, not interrogation
- **Validate competitors** — If client isn't sure about competitors, offer to research them
- **Set expectations** — Be honest about what SEO can and can't do in 90 days
- **Always initialize vault folders** — Teams will fail if their folders don't exist
- **Always update dashboard** — New client = dashboard updated immediately
