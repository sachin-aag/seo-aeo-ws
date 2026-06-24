# Pre-Publish Checklist

Run this before every piece of content goes live. Takes 5 minutes. Saves you from publishing things that won't rank or get cited.

---

## Content structure

- [ ] **TLDR at the top** — 2–3 sentences that answer the main question directly. No preamble.
- [ ] **One H1** — contains the primary keyword, makes a specific promise
- [ ] **H2s are specific** — each one answers a question on its own, no vague headings ("Overview", "More details")
- [ ] **One claim per sentence** — no paragraph-long run-ons that contain multiple ideas
- [ ] **FAQ section at the bottom** — at least 4 questions with direct first-sentence answers
- [ ] **No banned words** — check against the list in `skills/humanise/references/writing-rules.md`
- [ ] **Active voice** — "We did X" not "X was done by us"
- [ ] **No LLM tells** — no em-dashes, no "let's dive in," no essay closers

---

## Technical

- [ ] **Title tag** — 50–60 characters, primary keyword in first 3 words
- [ ] **Meta description** — 150–160 characters, includes keyword, ends with a hook
- [ ] **H1 is in static HTML** — not injected by JavaScript (check with View Source)
- [ ] **Canonical tag** — set correctly (usually self-referencing)
- [ ] **URL slug** — short, contains keyword, no stop words if possible
  - Good: `/fix-404-errors`
  - Bad: `/blog/2025/03/15/how-to-deal-with-and-fix-404-errors-on-your-website`
- [ ] **Internal links** — at least one link from an existing page on your site to this new page

---

## Structured data

- [ ] **JSON-LD added** — correct type for this page (Article, FAQPage, etc.)
- [ ] **Validated** — no errors in Google's Rich Results Test
- [ ] **FAQPage schema** — if the page has a FAQ section, FAQPage JSON-LD matches the actual questions on the page

---

## Images (if any)

- [ ] **Alt text on every image** — descriptive, not keyword-stuffed
- [ ] **Images compressed** — no image over 500KB without a reason
- [ ] **Featured image** — 1200×630px, used in the Article JSON-LD `image` field

---

## Final check

- [ ] **Would you stop and read this?** If you'd scroll past it yourself, fix it.
- [ ] **Does it say something the internet doesn't already have 50 versions of?** If not, add your specific experience, data, or angle.
- [ ] **Request indexing** — after publishing, go to Google Search Console → URL Inspection → Request Indexing
