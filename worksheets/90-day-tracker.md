# 90-Day SEO Tracker

Fill in the start date, then check off each action as you complete it. The goal isn't perfection — it's consistency.

**Start date:** _______________
**Domain:** _______________
**Primary keyword:** _______________

---

## Month 1 — Fix the foundation

### Week 1: Technical audit

- [ ] Run `site:yourdomain.com` in Google — note how many pages appear: _____
- [ ] Set up Google Search Console (if not already active)
- [ ] Submit sitemap to Search Console
- [ ] Check title tags on your top 5 pages — any missing, duplicate, or over 60 chars?
- [ ] Check meta descriptions on your top 5 pages
- [ ] Run the LLM rendering gap check: `curl -s yourdomain.com | grep "<title>"`
- [ ] Check robots.txt for any blocked pages that should be indexed
- [ ] Check Google Search Console for crawl errors

**Notes:**
```
[What you found]
```

---

### Week 2: Fix technical issues

- [ ] Fix missing or duplicate title tags (pages fixed: _____)
- [ ] Fix JS-rendered metadata (move to static HTML)
- [ ] Request indexing for key pages not in Google
- [ ] Fix robots.txt if any pages were wrongly blocked
- [ ] Confirm sitemap has no errors in Search Console
- [ ] Add canonical tags to any pages that needed them

**Notes:**
```
[What you fixed]
```

---

### Week 3: Keyword and topic strategy

- [ ] Complete the `worksheets/topic-map.md` worksheet
- [ ] Primary keyword chosen: _______________
- [ ] Topic cluster of 6–8 supporting keywords built
- [ ] First 3 content pieces planned (titles and keywords noted)
- [ ] Competitor gap identified — what are they missing?

**Notes:**
```
[Your topic cluster summary]
```

---

### Week 4: Publish piece 1

- [ ] Content brief created using `skills/content-brief`
- [ ] Piece written with: TLDR at top, clear H2s, FAQ at bottom
- [ ] Title tag and meta description optimised (use `skills/meta-optimizer`)
- [ ] JSON-LD added (use `skills/schema-generator`)
- [ ] Published and indexing requested in Search Console
- [ ] Piece 1 URL: _______________

**Month 1 checkpoint:**
- Pages indexed: _____
- Technical issues fixed: _____
- Piece 1 live: [ ] Yes / [ ] No

---

## Month 2 — Publish and outreach

### Week 5: Publish piece 2 (FAQ/informational)

- [ ] Topic: _______________
- [ ] FAQ section added (4–5 direct Q&A pairs)
- [ ] FAQPage JSON-LD added
- [ ] Published — URL: _______________
- [ ] Indexing requested

---

### Week 6: Restructure existing pages

- [ ] Top 3 existing pages identified that need TLDR + FAQ
- [ ] Page 1 restructured using `skills/content-rewriter` — URL: _______________
- [ ] Page 2 restructured — URL: _______________
- [ ] Page 3 restructured — URL: _______________
- [ ] All three re-published and indexing re-requested

---

### Week 7: Publish piece 3 (off-page post)

- [ ] Platform chosen: LinkedIn / Reddit / Quora
- [ ] Written natively for that platform (not repurposed from site content)
- [ ] Published with link back to relevant site page
- [ ] Post URL: _______________

---

### Week 8: First outreach batch

- [ ] Backlink gap analysis run using `skills/backlink-gap`
- [ ] 5 gap opportunities identified
- [ ] 5 outreach emails sent
- [ ] 3 relevant directories submitted to

**Outreach log:**

| Target | Status | Date sent | Response |
|--------|--------|-----------|---------|
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |

**Month 2 checkpoint:**
- Pieces live: _____
- Pages restructured: _____
- Outreach emails sent: _____

---

## Month 3 — Optimise and set cadence

### Week 9: Check Search Console data

- [ ] Reviewed impressions and clicks for all pages
- [ ] Identified 2–3 pages ranking in positions 8–20 (quick win candidates)
- [ ] Noted queries appearing that weren't targeted — new content opportunities found?

**Quick win pages (positions 8–20):**
```
1.
2.
3.
```

---

### Week 10: Optimise quick wins

- [ ] Title tags rewritten for pages in positions 8–20 (use `skills/meta-optimizer`)
- [ ] Internal links added from newer content to these pages
- [ ] Structured data checked and any errors fixed

---

### Week 11: AI visibility check

- [ ] GEO check run using `skills/geo-check`
- [ ] Queries tested in ChatGPT: _____ / Perplexity: _____
- [ ] Results recorded:

| Query | Tool | Mentioned? | Who appears instead |
|-------|------|-----------|-------------------|
| | | | |
| | | | |
| | | | |
| | | | |

- [ ] 1–2 new content pieces identified based on AI citation gaps

---

### Week 12: Set ongoing cadence

- [ ] Monthly cadence committed to: 2 pieces + 1 restructure + 3 outreach
- [ ] `checklists/monthly-seo.md` bookmarked as monthly routine
- [ ] Next 90-day topic cluster planned

**Month 3 checkpoint:**
- Organic impressions vs. Month 1: _____ → _____
- Pages indexed: _____
- AI visibility: mentioned in _____ out of _____ queries tested
- Backlinks added: _____

---

## Ongoing monthly cadence

After the 90 days, run this every month:

- [ ] 2 new content pieces published
- [ ] 1 existing page restructured (TLDR, H2s, FAQ)
- [ ] 3 outreach emails sent
- [ ] Monthly SEO checklist completed (`checklists/monthly-seo.md`)
- [ ] Search Console reviewed for new quick wins
- [ ] AI visibility spot-checked (2–3 queries in ChatGPT or Perplexity)
