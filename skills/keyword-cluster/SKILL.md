---
name: keyword-cluster
description: Build a topic cluster for a business or niche — primary keyword, supporting terms, intent classification, and content page ideas. Use this whenever someone wants to figure out what to write about, is starting an SEO strategy from scratch, or asks "what keywords should I target." Also trigger when someone shares their business type and wants to know where to focus content-wise.
---

# Keyword Cluster Builder

The goal here is to help the user think in topics, not keywords. A topic is a cluster of related searches with the same underlying intent. One strong page that covers a topic thoroughly outranks ten thin pages each targeting one keyword.

## What you need from the user

- Their business type or niche (e.g. "freelance UX designer in Berlin", "vegan meal prep company")
- Their target audience (who they're trying to reach)
- Location, if relevant
- Any keywords they're already ranking for or have tried (optional — helps avoid suggesting what they already have)

## What to produce

### 1. Primary keyword

The main keyword that defines their core topic. This is what their homepage or most important page should rank for. Criteria:
- Clear commercial or informational intent matching their business
- Realistic to rank for as a smaller site (don't suggest "best SEO agency" to someone who just started)
- Specific enough that it has a real audience, broad enough to anchor a content strategy

### 2. Topic cluster (5–8 supporting keywords)

Each supporting keyword should:
- Be closely related to the primary keyword
- Have its own clear search intent (informational, navigational, transactional, or commercial)
- Map to a single content piece or page — not overlap with others in the cluster

Present them in a table:

```
| Supporting keyword | Intent | Content type |
|-------------------|--------|-------------|
| ... | Informational | Blog post |
| ... | Transactional | Service/landing page |
| ... | Commercial | Comparison page |
| ... | Informational | FAQ / guide |
```

### 3. Intent classification

Remind the user what the four intent types mean, with examples from their specific niche:

- **Informational** — they want to learn something ("how does X work", "what is Y")
- **Navigational** — they're looking for a specific site or brand ("your-brand login", "competitor pricing page")
- **Transactional** — they're ready to act ("hire a UX designer", "buy X", "book a consultation")
- **Commercial** — they're comparing before deciding ("best X for Y", "X vs Y", "top X in Berlin")

Mismatched intent is the most common reason a well-written page fails to rank. A blog post for a transactional query, or a sales page for an informational one, won't perform regardless of how good the content is.

### 4. Content page titles (3 suggestions)

Based on the cluster, suggest three specific content piece titles the user could write first. Prioritize:
1. One bottom-of-funnel piece (comparison, review, "best X for Y") — converts readers most directly
2. One FAQ / informational piece — earns AI citations most reliably
3. One piece the user could realistically write from personal experience — builds E-E-A-T

Each title should make a specific promise. "My Thoughts on SEO" is not a title. "Why Your Pages Aren't Indexed (And How to Fix It in 10 Minutes)" is a title.

## Example output

**Business:** Freelance UX designer in Berlin, targeting startups

**Primary keyword:** UX designer for startups Berlin

**Cluster:**

| Supporting keyword | Intent | Content type |
|-------------------|--------|-------------|
| how much does a UX designer cost | Informational | Blog post |
| UX designer vs UI designer | Informational | Explainer post |
| hire freelance UX designer | Transactional | Service page |
| best UX designers Berlin | Commercial | Profile / comparison |
| UX audit for startups | Transactional | Service page |
| what does a UX designer do | Informational | FAQ guide |

**First three pieces to write:**
1. "UX Design Rates in Berlin: What Startups Actually Pay in 2025" ← bottom-of-funnel, converts
2. "5 Questions Every Startup Should Ask Before Hiring a UX Designer" ← FAQ format, AI-citable
3. "What I Learned Redesigning Onboarding for Three Berlin B2B Startups" ← E-E-A-T, personal

## Tone note

Don't pad this with caveats about keyword research being complex. Give them a clear, usable cluster and move on. They can refine it with real search volume data in Ubersuggest or Google Search Console — but the strategic shape of the cluster is what you're here to provide.
