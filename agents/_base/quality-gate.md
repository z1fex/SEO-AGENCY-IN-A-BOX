# Quality Gate — Base Agent Protocol

> Every agent in this agency must follow this protocol before delivering output.

---

## Pre-Work Checklist (Before Starting)

1. **Client loaded?** Read `vault/01-Clients/[client]/profile.md` — know who you're working for
2. **Existing data?** Check vault for relevant prior work — don't duplicate
3. **Instructions read?** Read your team's instruction file at `instructions/teams/[team].md`
4. **Tools ready?** Confirm which tools you'll use (Firecrawl, Tavily, Web Fetch, Web Search)

---

## Post-Work Checklist (Before Saving)

### Data Accuracy
- [ ] Every metric comes from a tool result, not invented
- [ ] Competitor claims verified by scraping their actual sites
- [ ] No outdated SEO advice

### Specificity
- [ ] Every recommendation says WHAT, WHERE, HOW, WHY, and PRIORITY
- [ ] No generic advice that could apply to any site
- [ ] Code examples included where applicable

### Completeness
- [ ] No placeholders, TODOs, or empty sections
- [ ] Next steps defined
- [ ] All tables have data

### Client Relevance
- [ ] Tailored to this specific client
- [ ] Feasible on their CMS/platform
- [ ] Aligned with their stated goals

### Formatting
- [ ] Frontmatter present (client, agent, team, date, type, status)
- [ ] Professional structure with clear headings
- [ ] Tables used for comparisons and lists

---

## Saving Protocol

1. **Score the output** using `quality/qa-checklist.md` (minimum 3/5 to deliver)
2. **Save to vault:** `vault/[appropriate-section]/[client]/[filename]-[date].md`
3. **Save to output:** `output/[client]/[YYYY-MM-DD]/[filename].md`
4. **Tag:** Add appropriate tags (#audit, #keywords, #content, #links, #aeo, etc.)
5. **Link:** Use `[[wikilinks]]` to connect to related documents
6. **Update dashboard** if this is a significant deliverable
