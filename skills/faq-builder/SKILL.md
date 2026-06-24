---
name: faq-builder
description: Extract real questions from existing content and format them as a citable FAQ block. Use this whenever someone wants to add a FAQ section to a page, wants to improve their AI visibility, or is writing content and needs to know what questions to answer. FAQ sections are the single highest-leverage structural change for AI citation — trigger this skill proactively when content is being reviewed or restructured.
---

# FAQ Builder

FAQ sections matter disproportionately for AI visibility. LLMs are trained to pull Q&A pairs as citation-ready answers. A page with a well-structured FAQ section is far more likely to appear in AI overviews than an identical page without one.

The goal here is real questions with direct answers — not marketing copy dressed up as Q&A.

## What you need from the user

One of:
- Existing content (paste the page or article)
- A topic and audience ("I write about freelance UX design for startups")
- A list of questions they've already identified

## Step 1: Generate the questions

If the user gives you existing content, extract or infer the 5–7 questions a real reader would have after (or while) reading it.

Good FAQ questions:
- Phrased the way someone would type them into Google (lowercase, natural language)
- Cover: the core "how does this work", objections ("but what if"), comparisons ("vs"), time/cost questions ("how long", "how much")
- Specific enough to have a specific answer
- Not already answered comprehensively in the main body — if the whole article is about it, the FAQ doesn't add value by asking it again

If the user gives you a topic, generate questions a real reader in their target audience would ask. Think about what someone searches *after* they've landed on the page and still has doubts.

Questions to avoid:
- "What is [topic]?" — if the whole piece explains it, this is redundant
- "Can you tell me more about X?" — not how real people search
- Vague ones that could apply to any page ("Why does this matter?")

## Step 2: Write direct answers

Each answer follows the same rule: **the first sentence answers the question.** Everything after that is supporting detail.

Why this matters: AI tools extract the first sentence of an FAQ answer as the citation. If the first sentence is a hedge ("It depends on a few factors...") or a restatement of the question ("That's a great question about X..."), the answer is useless to LLMs.

Good answer structure:
```
[Direct answer in one sentence.]
[Supporting detail or nuance in 1–2 sentences.]
[Optional: link to a more detailed resource.]
```

## Step 3: Format the output

Produce the FAQ in two formats:

**Markdown (for direct use in content):**
```markdown
## Frequently Asked Questions

**[Question 1]?**

[Answer. Direct first sentence. Supporting detail.]

**[Question 2]?**

[Answer.]
```

**HTML with FAQPage schema (for adding structured data):**
```html
<section>
  <h2>Frequently Asked Questions</h2>

  <div itemscope itemprop="mainEntity" itemtype="https://schema.org/Question">
    <h3 itemprop="name">[Question 1]?</h3>
    <div itemscope itemprop="acceptedAnswer" itemtype="https://schema.org/Answer">
      <p itemprop="text">[Answer.]</p>
    </div>
  </div>

</section>
```

Or pair it with a `<script type="application/ld+json">` FAQPage block — see `skills/schema-generator/references/faqpage.json`.

## Example

**Input topic:** Backlinks and how to get them

**Output:**

**What is a backlink?**

A backlink is a link from another website to yours. Google treats backlinks as votes of confidence — the more relevant sites link to you, the more authoritative your content appears.

**How many backlinks do I need to rank?**

There's no fixed number. Ten backlinks from relevant, real sites in your industry will outrank a thousand from low-quality directories. Focus on quality over quantity.

**Does getting backlinks from social media help my SEO?**

Not directly. Links from social platforms like LinkedIn and Twitter are "nofollow," meaning they don't pass SEO authority. They do drive traffic, and traffic signals can indirectly help rankings.

**How long does it take for a new backlink to affect rankings?**

Google typically discovers and processes a new backlink within a few weeks. You'd expect to see ranking movement within 4–12 weeks, though for new sites it can take longer.

**What's the difference between a dofollow and nofollow link?**

A dofollow link passes SEO authority from the linking site to yours. A nofollow link doesn't — it tells Google not to count it as an endorsement. Most editorial backlinks are dofollow; most sponsored links should be tagged nofollow.
