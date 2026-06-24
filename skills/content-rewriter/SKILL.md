---
name: content-rewriter
description: Restructure existing content to make it citable by AI and more useful to human readers. Use this whenever someone has a piece of content that isn't getting traffic or citations and wants to know why, or when they ask to "improve," "fix," or "optimize" an existing article or blog post. Also trigger when content is well-written but poorly structured — good ideas buried in walls of text or vague headings.
---

# Content Rewriter

You're not here to rewrite for style — you're here to restructure for citability and clarity. The ideas stay. The structure changes.

A well-written piece that's buried in a wall of text with vague headings and no FAQ gets cited less often than a mediocre piece with a clear TLDR, specific H2s, and direct FAQ answers. Structure is the leverage point.

## What you need from the user

- The existing content (paste it)
- The primary keyword the piece is targeting (if they know it)
- Who the audience is

## What to change

Work through these in order. Apply each change to the content.

### 1. Add a TLDR at the top

Before the first paragraph, add a 2–3 sentence TLDR that:
- States the core answer or takeaway directly
- Is specific enough to be useful as a standalone extract
- Doesn't start with "In this article" or "We'll explore"

This is what AI tools cite. If the opening 200 words don't answer anything, the piece doesn't get cited.

### 2. Rewrite vague H2s

Read every H2 in the piece. Flag any that are:
- Too short to be meaningful ("Overview", "Details", "More information")
- Marketing-speak ("Unlock the power of X")
- Phrased as topics rather than answers ("Backlinks" instead of "How to get backlinks from real sites")

Rewrite them to be specific and descriptive. A good H2 can stand alone as an answer to a question.

Before: `## Why This Matters`
After: `## Why poorly structured content gets ignored by AI search tools`

### 3. Break dense paragraphs into one claim per sentence

Find any paragraph longer than 3–4 sentences that contains multiple separate claims. Break it up.

Before:
```
Backlinks are an important ranking factor in Google's algorithm, and while many
people focus on getting as many backlinks as possible, the relevance and authority
of the linking site matters much more than the raw number, which is why ten
high-quality backlinks from industry sites will outperform a thousand low-quality
directory listings, as Google has become increasingly good at detecting link spam
and will penalise sites that use it.
```

After:
```
Backlinks are one of Google's most important ranking signals.
Relevance matters more than quantity — ten links from real industry sites outperform
a thousand directory listings.
Google detects link spam and penalises sites that use it.
```

### 4. Add or improve the FAQ section

If the piece has no FAQ section, add one at the end with 4–5 direct Q&A pairs.
If it has one, check that each answer starts with a direct response in the first sentence. Fix any that don't.

See `skills/faq-builder/` for guidance on generating questions and writing direct answers.

### 5. Fix the title (if it's vague)

If the H1 is vague, generic, or doesn't contain the primary keyword in the first three words, rewrite it. Offer two options.

## What NOT to change

- Voice and tone — if the piece sounds like the person who wrote it, keep that
- The substance and arguments — you're restructuring, not ghostwriting
- Specific examples, stories, or data points — these are E-E-A-T signals, leave them in
- Length — don't add filler, don't cut substance just to make it shorter

## Output format

Return the restructured content in full, with a brief note before it explaining what you changed and why. Keep the note to 5 bullets maximum.

```
### What changed
- Added TLDR (the first answer is now in sentence 3, not paragraph 8)
- Rewrote 4 H2s to be specific instead of generic
- Split the third paragraph into 5 single-claim sentences
- Added a 5-question FAQ section at the bottom
- Rewrote the H1 from "My SEO Journey" to "What I Learned Running SEO for 12 SaaS Startups"

---

[Full restructured content below]
```
