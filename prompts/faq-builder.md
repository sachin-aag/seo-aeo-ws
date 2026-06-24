# FAQ Builder Prompt

Copy everything below the line and paste it into any LLM. Fill in the bracketed sections.

---

I need a FAQ section for a piece of content. FAQ sections are the highest-leverage structural change for AI visibility — LLMs are trained to pull Q&A pairs as citations.

**Option A — I have existing content:**
Paste your content below and I'll extract the right questions from it.

[PASTE CONTENT HERE]

**Option B — I have a topic and audience:**
- Topic: [what the page or post is about]
- Audience: [who reads this]
- Questions I already know they ask (optional): [list any you have]

---

Please produce a FAQ section with 5–7 questions following these rules:

**For the questions:**
- Phrase them exactly how someone would type them into Google (lowercase, natural language)
- Cover: how it works, common objections, comparisons, time/cost questions, "what if" scenarios
- Make them specific enough to have a specific answer
- Don't repeat what the main content already covers comprehensively

**For the answers:**
- The first sentence must answer the question directly — no preamble, no "Great question"
- Follow with 1–2 sentences of supporting detail if needed
- Keep answers under 100 words each

**Output format — give me both:**

1. **Markdown version** (for pasting into my content management system):
```
## Frequently Asked Questions

**[Question]?**

[Direct answer. Supporting detail.]

**[Question]?**

[Direct answer.]
```

2. **JSON-LD version** (for adding FAQPage structured data):
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [...]
}
```
