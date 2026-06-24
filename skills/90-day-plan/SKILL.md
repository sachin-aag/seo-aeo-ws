---
name: 90-day-plan
description: Generate a personalized 90-day SEO and GEO action plan. Use this whenever someone wants a roadmap, asks "where do I start," or has done an audit and doesn't know what to prioritize next. Also trigger when someone feels overwhelmed by SEO — a concrete 90-day plan with specific weekly actions is the antidote to paralysis. SEO is a mortgage, not a lottery ticket: the plan only works if it gets executed monthly.
---

# 90-Day SEO + GEO Plan

The 90-day plan takes someone from wherever they are now to a stable, working SEO foundation with content in motion and AI visibility improving. It's not a wish list — it's a weekly action schedule with specific deliverables.

## What you need from the user

- Their business type and target audience
- Their current situation (pick what applies):
  - Approximate number of pages indexed (they can check with `site:domain.com`)
  - Number of blog posts or content pieces live
  - Domain age (brand new / 1–2 years / older)
  - Whether Google Search Console is set up
  - Whether they've done any keyword research before
- Any known blockers (no time for writing, no CMS access, no budget for tools)

## The plan structure

### Month 1 — Fix the foundation, pick your targets, publish piece 1

Week 1: Technical audit
- Run `site:domain.com` — check what's indexed
- Check title tags and meta descriptions on the top 5 pages
- Run the LLM rendering gap check (`curl -s domain.com | grep "<title>"`)
- Set up Google Search Console if it's not already active
- Submit sitemap

Week 2: Fix technical issues found in Week 1
- Fix any missing or duplicate title tags
- Fix any JS-rendered metadata (move to static HTML)
- Request indexing for any key pages that aren't indexed
- Verify sitemap has no errors in Search Console

Week 3: Keyword and topic strategy
- Use the `keyword-cluster` skill to build a topic cluster for their niche
- Identify the top 3 pieces to write first:
  1. A bottom-of-funnel piece (comparison, review, "best X for Y")
  2. An FAQ-structured informational piece
  3. An off-page post (LinkedIn, Reddit, or Quora — written for the platform)
- Build a topic map using the worksheet in `worksheets/topic-map.md`

Week 4: Write and publish piece 1 (bottom-of-funnel)
- Use `content-brief` to plan it
- Write it with the structure checklist: TLDR up top, clear H2s, FAQ at bottom
- Add JSON-LD using `schema-generator`
- Publish and request indexing

**Month 1 deliverable:** Clean technical foundation, topic map complete, first piece live.

---

### Month 2 — Publish, restructure, start outreach

Week 5: Write and publish piece 2 (FAQ/informational)
- Informational intent, targeting a question your audience asks
- Use `faq-builder` to build the FAQ section
- Add FAQPage JSON-LD

Week 6: Restructure top existing pages
- Identify the 3 most important existing pages that don't have a TLDR or FAQ
- Use `content-rewriter` on each one
- Re-publish and re-request indexing

Week 7: Write and publish piece 3 (off-page post)
- Write natively for the platform (LinkedIn article, Reddit answer, Quora post)
- Don't repurpose body content — write it for that audience
- Link back to one relevant page on your site

Week 8: First outreach batch
- Use `backlink-gap` to identify 5 gap opportunities
- Send 5 outreach emails (one per opportunity)
- Submit to 3 relevant directories

**Month 2 deliverable:** 3 pieces live, top pages restructured, outreach pipeline started.

---

### Month 3 — Double down on what's working, check AI visibility, set cadence

Week 9: Check Search Console data
- Which pages are getting impressions? Which are getting clicks?
- Which queries are you appearing for that you didn't target?
- Use this data to identify 2–3 quick wins (pages ranking in positions 8–20 that need a push)

Week 10: Optimise the quick wins
- Run `meta-optimizer` on any page ranking in positions 8–20 — a better title can move it up
- Add internal links from newer content to these pages
- Check and fix any structured data issues

Week 11: AI visibility check
- Run the `geo-check` skill — check ChatGPT and Perplexity for your top 4 queries
- Note who shows up, who doesn't, what content is being cited
- Identify 1–2 pieces to write that would directly fill an AI citation gap

Week 12: Set the ongoing cadence
- Commit to a monthly rhythm: 2 new pieces + 1 restructure + 3 outreach emails
- Fill in `worksheets/90-day-tracker.md` as a tracker going forward
- Run the `monthly-seo.md` checklist once a month

**Month 3 deliverable:** Data-informed decisions on what to prioritise next, AI visibility baseline established, monthly cadence set.

---

## Output format

Produce the plan as a month-by-month breakdown with specific weekly actions. Adjust the pacing based on how much time the user has available (full-time vs. side project). Make the actions concrete: not "work on content" but "write the FAQ-structured piece on [specific topic], publish by [specific day]."

Flag any Month 1 blockers immediately — if their site has a serious technical issue (JS-rendered metadata, not indexed at all, no Search Console), everything else waits until that's fixed.

```
## Your 90-Day Plan

**Starting point:** [brief summary of their current state]
**Primary goal:** [what success looks like at day 90]

### Month 1 — Fix the foundation
Week 1: [specific actions]
Week 2: [specific actions]
Week 3: [specific actions]
Week 4: [specific actions]
End of month checkpoint: [deliverables]

### Month 2 — Publish and outreach
[same format]

### Month 3 — Optimise and set cadence
[same format]

**Monthly cadence going forward:**
[what they should do every month after the 90 days]
```
