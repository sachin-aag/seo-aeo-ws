# Best Practices: Get Found by Humans and AI

Two sections. Work through Part 1 first — no amount of great content fixes a broken technical foundation.

---

## Part 1 — Technical Checklist

Use this as a pre-launch audit and a quarterly health check. Each item is either passing or it isn't.

---

### 1. Indexing

**Are your pages actually in Google?**

```
site:yourdomain.com
```

Type that into Google. If your pages show up, you're indexed. If nothing appears, stop here and fix this before anything else.

- [ ] `site:yourdomain.com` returns your key pages
- [ ] Google Search Console is set up and verified
- [ ] No pages show "URL not on Google" in Search Console that should be indexed
- [ ] XML sitemap exists at `yourdomain.com/sitemap.xml`
- [ ] Sitemap is submitted in Google Search Console with no errors

**How to request indexing manually:**
Search Console → URL Inspection → enter URL → Request Indexing. Takes 1–14 days. New sites index slowly — that's normal.

---

### 2. Metadata

Title tags and meta descriptions are the first thing both Google and LLMs read. Get these right before writing a single word of body content.

**Title tag rules:**
- [ ] 50–60 characters (Google truncates at ~60)
- [ ] Primary keyword appears within the first three words
- [ ] Each page has a unique title — no duplicates
- [ ] Reads like a human wrote it, not a robot

**Meta description rules:**
- [ ] 150–160 characters
- [ ] Contains the primary keyword naturally
- [ ] Ends with a clear action or value statement
- [ ] Each page has a unique meta description

**How to check:**
```bash
curl -s https://yourdomain.com/your-page | grep -i "<title\|meta name=\"description\""
```

---

### 3. The LLM Rendering Gap

This is the most overlooked technical issue for AI visibility. Google executes JavaScript during crawls. LLMs don't — they fetch raw HTML only.

If your title, meta description, or body content is injected by JavaScript after the page loads, LLMs can't read it.

**Check if your metadata is static:**
```bash
curl -s https://yourdomain.com/your-page | grep "<title>"
```

If that returns your actual title → you're fine.
If it returns nothing or a placeholder → your metadata is JS-injected and invisible to LLMs.

- [ ] Title tag is present in raw HTML (not injected by JS)
- [ ] Meta description is present in raw HTML
- [ ] Key body content (first 200 words) is server-rendered
- [ ] OG tags (`og:title`, `og:description`) are in static HTML

**Fix:** Use server-side rendering or static generation for any page you want AI to read. In Next.js, use the `metadata` export (App Router) or `getServerSideProps`/`getStaticProps` (Pages Router) — never rely on `useEffect` to set metadata.

---

### 4. Page Structure

One H1. Clear H2s. No orphan pages.

- [ ] Every page has exactly one H1
- [ ] The H1 contains your primary keyword
- [ ] H2s are descriptive and specific — not "More information" or "Details"
- [ ] Heading levels don't skip (H1 → H2 → H3, not H1 → H4)
- [ ] Every key page is linked from at least one other page on your site (no orphans)
- [ ] Internal links use descriptive anchor text, not "click here"

---

### 5. JSON-LD Structured Data

Structured data tells both Google and LLMs exactly what your content is. It doesn't guarantee a rich result, but it makes your content easier to parse and cite.

**Which schema type to use:**

| Page type | Schema to add |
|-----------|--------------|
| Blog post / article | `Article` |
| Page with Q&A | `FAQPage` |
| Local business homepage | `LocalBusiness` |
| Any inner page | `BreadcrumbList` |
| Product or service | `Product` or `Service` |

- [ ] Blog posts have `Article` JSON-LD
- [ ] Any page with Q&A has `FAQPage` JSON-LD
- [ ] Local business has `LocalBusiness` JSON-LD on homepage
- [ ] Inner pages have `BreadcrumbList`
- [ ] Structured data validates with no errors in Google's Rich Results Test

**How to validate:**
Paste your URL into [Google's Rich Results Test](https://search.google.com/test/rich-results). Fix any errors before fixing warnings.

See [`skills/schema-generator/`](skills/schema-generator/) to generate the right JSON-LD for your page.

---

### 6. Crawlability

- [ ] `robots.txt` doesn't block pages you want indexed
- [ ] Canonical tags point to the correct URL (self-referencing canonicals are fine; cross-page canonicals should be intentional)
- [ ] No redirect chains longer than one hop (A → B is fine; A → B → C is not)
- [ ] HTTPS is active and HTTP redirects to HTTPS
- [ ] Page load time is under 3 seconds on mobile (check with PageSpeed Insights)

---

## Part 2 — Content: Do This, Not This

The structural changes that move content from invisible to citable. Each example is short on purpose — the pattern matters more than the length.

---

### Put the answer first

LLMs and Google both reward content that answers the question immediately. Readers don't scroll to find your point.

**Do this:**
```
## What is a canonical tag?

A canonical tag tells Google which version of a URL is the "real" one.
Use it when the same content appears at multiple URLs.
```

**Not this:**
```
## What is a canonical tag?

Search engine optimization involves many different technical elements.
One of the things that confuses people most is the concept of canonical tags.
In this post, we'll explore what they are and why they matter.
A canonical tag is...
```

Why it matters: AI tools extract the first sentence of each section to form their answers. If your first sentence is filler, you don't get cited.

---

### Write specific H2s

Vague headings fail both humans and search engines. Specific headings get picked up as standalone answers.

**Do this:**
```
## How to submit your sitemap to Google Search Console
## Why your title tag is getting cut off in search results
## The difference between a 301 and 302 redirect
```

**Not this:**
```
## More about sitemaps
## Title tags
## Redirects — what you need to know
```

Why it matters: LLMs scan headings to decide what a page is about. Vague headings make your content hard to parse.

---

### One claim per sentence

Dense sentences force the reader (and the model) to do extra work. One idea per sentence makes content easier to extract and cite.

**Do this:**
```
Backlinks from relevant sites outrank backlinks from high-traffic sites.
A link from a niche industry blog carries more weight than one from a general news site.
Google measures topical relevance, not just domain authority.
```

**Not this:**
```
Backlinks are important for SEO, and while many people focus on getting links from
high-authority sites with lots of traffic, the relevance of the site to your topic
actually matters more than the raw domain authority score, which is something
Google has increasingly prioritised in recent algorithm updates.
```

Why it matters: AI tools pull individual sentences as citations. A sentence that contains three ideas produces a confusing citation.

---

### Start with a TLDR

Readers scan before they read. AI tools read the first 200 words of your page before deciding whether to go deeper.

**Do this:**
```
**TL;DR:** Google indexes your page even if it's JS-rendered.
LLMs don't — they only read raw HTML. If your metadata is injected
by JavaScript, you're invisible to AI tools.
```

**Not this:**
```
In today's digital landscape, many businesses are starting to think
about how artificial intelligence might impact their online presence.
This is an important consideration...
```

Why it matters: The TLDR is what gets cited. Everything below it is evidence.

---

### Write direct FAQ answers

FAQ sections are the single highest-leverage structural change for AI visibility. LLMs are trained to pull Q&A pairs. But only if the answer starts in the first sentence.

**Do this:**
```
**Can I rank for AI overviews without ranking in regular search?**

No. 97% of AI Overview citations already rank in the top 20 organic results.
Fix your organic rankings first — AI visibility follows.
```

**Not this:**
```
**Can I rank for AI overviews without ranking in regular search?**

That's a great question that a lot of people ask. There are many factors
that go into AI overviews, and the relationship between organic rankings
and AI citations is complex...
```

Why it matters: AI tools extract the first sentence of FAQ answers. If that sentence doesn't answer the question, the section is useless.

---

### Write like a person, not a press release

Passive voice, corporate hedging, and marketing fluff make your content harder to trust and harder to read.

**Do this:**
```
We got burned by this last year. Our blog posts ranked well but our homepage
wasn't indexed at all — we'd accidentally blocked it in robots.txt.
Check yours now before you do anything else.
```

**Not this:**
```
It is recommended that website owners ensure their robots.txt configuration
does not inadvertently restrict search engine access to key pages.
Organisations may wish to consider reviewing this setting periodically.
```

Why it matters: E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness) is a Google signal. Content that sounds like it was written by a committee scores lower.

---

### Target topic clusters, not individual keywords

One strong page that covers a topic thoroughly outranks ten thin pages each targeting one keyword.

**Do this:**
```
One page: "Vegan Burgers — How to Find, Make, and Order Them"
Covers: best vegan burgers, vegan burger recipes, vegan burger near me,
        are vegan burgers healthy, vegan burger protein content
```

**Not this:**
```
Page 1: "Best Vegan Burgers"
Page 2: "Vegan Burger Recipes"
Page 3: "Vegan Burger Near Me"
Page 4: "Are Vegan Burgers Healthy"
(each page: 300 words, no depth)
```

Why it matters: Thin pages split your authority and compete against each other. One comprehensive page builds topical depth that both Google and LLMs reward.

---

### Match content format to search intent

The format of your content needs to match what the searcher actually wants — not just the topic.

| Intent | What they want | Right format |
|--------|---------------|-------------|
| "what is GEO" | A definition | Short explainer, definition in sentence 1 |
| "best SEO tools" | A comparison | List with clear criteria |
| "how to submit sitemap" | Steps to follow | Numbered how-to guide |
| "SEO agency Stuttgart" | A service to hire | Service page with proof, contact |

**Do this:** Check the top 3 results for your target keyword and match the format they use — Google has already validated what format works for that intent.

**Not this:** Write a 2,000-word essay for a query where everyone ranking is a step-by-step list.

Why it matters: Mismatched intent is the most common reason a technically good piece fails to rank.
