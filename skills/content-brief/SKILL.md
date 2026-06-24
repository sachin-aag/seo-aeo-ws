---
name: content-brief
description: Generate a complete SEO content brief for a target keyword or topic. Use this whenever someone wants to write a blog post, article, or landing page and needs a plan before they start writing. Trigger when someone says "I want to write about X", "what should my post on X cover", or shares a keyword and asks how to tackle it. A content brief is the difference between writing that ranks and writing that disappears.
---

# Content Brief Generator

A content brief answers one question before a word of body content is written: "What exactly should this piece contain, and in what order?" Your job is to produce a brief so clear that the writer (or an AI writing assistant) can follow it without asking any clarifying questions.

## What you need from the user

- Target keyword or topic
- Search intent type (informational, transactional, commercial, navigational) — if they don't know, ask one question: "What is someone trying to do when they search this?"
- Their audience (who is this written for?)
- Any existing content on this topic they want to beat or reference (optional)

## What to produce

### 1. Brief summary (3 sentences)

What this piece is about, who it's for, and what makes it worth reading. Write this as a commissioning editor would — it should make the writer want to write the piece.

### 2. Target keyword and intent

```
Primary keyword: [keyword]
Intent: [Informational / Transactional / Commercial / Navigational]
Secondary keywords to include naturally: [3–5 related terms]
```

### 3. TLDR angle (2–3 sentences)

This is the opening TLDR the finished article should start with. Write a draft now. It should:
- State the core claim or answer directly
- Be specific enough to be useful on its own
- Not start with "In this article" or "Today we'll explore"

This matters because LLMs extract the TLDR as the citation. If the TLDR is weak, the piece won't get cited even if the body is excellent.

### 4. Suggested H1

One option. Keyword-first. Specific promise. Under 65 characters.

### 5. H2 outline

The full structure of the piece. Each H2 should:
- Be specific and descriptive (answerable as a standalone question)
- Map to one clear point or section
- Build on the previous section rather than repeat it

Format:
```
## [H2 title]
→ What this section covers (1 sentence)

## [H2 title]
→ What this section covers (1 sentence)
```

Aim for 5–8 H2s. More than 10 is usually a sign the brief is too broad.

### 6. FAQ section (5 questions)

Five questions a real reader would ask about this topic. These become the FAQ block at the bottom of the finished article.

Good FAQ questions:
- Are phrased exactly as someone would type them into Google
- Have a direct, one-sentence answer (include a draft answer for each)
- Cover objections, comparisons, and "how long does this take"-type questions

Bad FAQ questions:
- "What is [topic]?" (too basic if the whole article covers it)
- "Can you tell me more about [topic]?" (not a real search query)

### 7. Content notes

Any specific points the writer should include that aren't obvious from the outline:
- A stat or data point that strengthens the piece
- A common misconception to address
- A personal experience or example that would build E-E-A-T
- What the top-ranking competitors are missing that this piece could own

### 8. Recommended length and format

```
Estimated word count: [X–Y words]
Format: [How-to guide / Comparison / FAQ post / Case study / Explainer]
Tone: [Direct and practical / Conversational / Technical]
```

Base the word count on what intent typically requires, not arbitrary targets. An informational piece explaining a concept can do it in 600 words. A comprehensive comparison guide might need 2,000. More is not better — complete is better.

## Example output (abbreviated)

**Target keyword:** how to check if your website is indexed

**Intent:** Informational

**TLDR draft:**
Type `site:yourdomain.com` into Google. If your pages appear, you're indexed. If nothing shows up, your site is invisible to search engines and needs to be fixed before you do anything else.

**Suggested H1:** How to Check If Your Website Is Indexed (And Fix It If It's Not)

**H2 outline:**
```
## What "indexed" actually means
→ Quick definition, no jargon

## The 30-second check: site: operator
→ Exact steps, what to look for in results

## What to do if your pages aren't showing up
→ Top 4 reasons + fixes for each

## How to use Google Search Console for a deeper check
→ URL Inspection tool walkthrough

## How long indexing takes (and when to worry)
→ Timelines for new sites vs existing pages

## FAQ
→ 5 questions answered directly
```

**FAQ questions:**
1. How long does it take for Google to index a new page? → Usually 3–14 days, but new sites can take weeks.
2. Why is my homepage indexed but not my blog posts? → Blog posts need inbound links to be discovered. Add them to your sitemap.
3. Can I force Google to index my page? → Yes — use URL Inspection in Search Console and click Request Indexing.
4. Does indexing mean I'll rank? → No. Indexing means Google knows your page exists. Ranking depends on relevance and authority.
5. What's the difference between indexed and crawled? → Crawled means Google visited the page. Indexed means it decided to include it in search results.
