---
name: geo-check
description: Check how a business or website appears in AI-generated answers across ChatGPT, Perplexity, and Claude. Use this whenever someone asks "am I showing up in AI search," "does ChatGPT know about me," or wants to understand their GEO (Generative Engine Optimization) baseline. Also trigger when someone is about to start an SEO strategy and wants to know where they stand with AI tools before doing anything else.
---

# GEO Check (AI Visibility Audit)

97% of AI Overview citations come from pages already ranking in the top 20 Google results. That means AI visibility largely follows organic visibility — but not always. Some pages get cited that don't rank well, and some that rank well never get cited. This skill helps you figure out which camp you're in.

## What you need from the user

- Business name
- Business category (what they do / sell / offer)
- City or region (if they serve a local or regional market)
- Their website URL (optional — for the direct mention check)

## The queries to run

Give the user a set of exact queries to paste into ChatGPT, Perplexity, and Claude. Tell them to use **web search mode** in each tool — not the default knowledge-only mode — so the tools are actively fetching current web content.

Produce 4–6 queries tailored to their specific business. Cover these categories:

### Category 1: Direct category + location
```
best [category] in [city]
top [category] [city] [year]
```

### Category 2: Problem-first queries (how a real customer searches)
```
[the problem their customer has] [city]
how to find a good [category] in [city]
```

### Category 3: Comparison queries
```
[their category] vs [alternative approach or competitor category]
when should I hire a [their category]
```

### Category 4: Direct brand mention
```
[their business name]
[their business name] reviews
```

## What to look for

Tell the user exactly what to check for and record:

**Presence check:**
- Does your business name appear in the answer?
- Is the information accurate (name, what you do, location)?
- Are you in the top 3 mentions, or buried at the end?

**Citation check:**
- Is your website URL cited as a source?
- Which of your pages is cited (homepage, blog post, service page)?

**Competitor check:**
- Who shows up instead of you?
- What does their content look like? (This tells you what's working)

**Gap check:**
- Are there queries in your category where nobody gets a clear answer? These are opportunities to own a topic.

## The recording template

Have the user fill this in for each query:

```
Query: [paste query here]
Tool: ChatGPT / Perplexity / Claude
Mentioned? Yes / No / Partially
Citation URL: [if cited]
Who shows up instead: [competitors named]
Notes: [anything notable about the answer]
```

## What the results mean

**You're mentioned and cited accurately:**
Your current content is doing its job. Focus on expanding your topic coverage and improving the content that's already getting cited.

**You're mentioned but not cited:**
AI tools know about you from brand mentions (directories, reviews, other sites) but haven't found citable content on your site. Add structured FAQ content and improve on-page structure.

**You're not mentioned at all:**
Two scenarios: (a) you're not ranking for related queries organically — fix technical SEO and content first; (b) your content exists but isn't structured for AI extraction — run `content-rewriter` on your key pages.

**A competitor you've never heard of keeps showing up:**
Look at their content. They've likely published clear, well-structured content that directly answers the queries you're targeting. The `content-brief` skill can help you plan a piece that goes deeper.

## The 30-day follow-up

Tell the user to run the same queries again in 30 days after making changes. AI tools update their citations as content changes — but it's not instant. Four weeks is a reasonable window to see early movement.
