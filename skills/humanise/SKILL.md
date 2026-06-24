---
name: humanise
description: Rewrite content to sound human and structure it for AI and search visibility. Use this whenever someone pastes content that feels flat, robotic, or AI-generated — even if they don't say "humanise." Also trigger when someone asks to "clean up," "improve," or "polish" a piece of writing, or when content uses passive voice, hedge language, or LLM tells like em-dashes and "let's dive in." After rewriting, layer in SEO/AEO structure so the human voice and search visibility compound.
---

# Humanise

You're doing two things in one pass: stripping the AI out, then making it findable.

A piece that reads like it was written by a committee and a piece that reads like a person both get ignored — but for different reasons. The committee piece gets scrolled past. The person piece gets read, shared, and cited. Your job is to get it to the second state, then make sure search engines and AI tools can find and extract it.

## Read the writing rules first

Before you start, read `references/writing-rules.md`. The rules there are the ground truth for this skill — they cover banned words, banned phrases, LLM patterns to kill, and voice principles to enforce. Don't rely on memory; read the file.

## Step 1 — Strip the AI out

Work through the content systematically.

### Kill the banned words

Scan for every word in the banned list. Replace each one using the alternatives in the rules. Don't just delete — find the word that belongs there.

Common ones to prioritise (they appear most often):
- leverage → use
- utilize → use
- seamless / seamlessly → automatic, or just cut
- robust → strong, or cut
- innovative → cut (always)
- implement → do
- delve → go into
- just → cut
- very / really / quite / pretty → cut
- commence → start
- facilitate → help

### Kill the banned phrases

Look for hedging and corporate filler:
- "I think / I believe / we believe" → state it directly
- "Today, we're excited to" → cut
- Anything that sounds like a press release

### Kill the LLM tells

These patterns flag AI-generated content to any reader who's seen it before:

- **Em-dashes (—):** Replace with a comma, semicolon, or full stop. Never em-dash.
- **"Let's dive in":** Cut it. Start with the first real sentence.
- **"In today's fast-paced / ever-evolving landscape of":** Cut the whole sentence and start with the point.
- **"It's not just X, it's Y":** Rewrite as two separate sentences.
- **Perfectly symmetrical paragraph structure:** ("Firstly... Secondly... Thirdly...") — break the symmetry, vary the rhythm.
- **High-school essay closers:** "In conclusion," "To summarize," "Overall," → cut them. Make the last sentence the actual point.
- **Hedge stacks:** "may potentially," "it's important to note that," "it's worth mentioning" → cut the meta-commentary, state the thing.
- **Title case headings:** Convert to sentence case. "How To Fix Your Title Tags" → "How to fix your title tags."

### Convert passive to active voice

Find every instance of "is/are/was/were + past participle" and flip it.

Before: "The content was restructured by our team."
After: "Our team restructured the content."

Before: "Results can be seen within 4 weeks."
After: "You'll see results within 4 weeks."

### Add contractions

Scan for: "do not / cannot / will not / it is / they are / I am / we are" → "don't / can't / won't / it's / they're / I'm / we're"

Contractions make writing warmer. Use them unless the context is explicitly formal (legal, medical disclaimers).

### Swap "we" for "you" where addressing the reader

If a sentence is aimed at the reader, it should say "you" not "we."

Before: "We've built this for teams who need to move fast."
After: "You can use this if your team needs to move fast."

## Step 2 — Layer in SEO/AEO structure

Once the content sounds human, make sure it's findable.

### Add or improve the TLDR

If there's no TLDR at the top, add one (2–3 sentences):
- First sentence: the core answer or takeaway, stated directly
- Second sentence: the key supporting fact or nuance
- No preamble, no "In this article we will explore"

### Check the H2s

Read every H2. If any are vague, rename them to be specific and descriptive.
- Before: "More on this topic"
- After: "Why your meta description gets rewritten by Google (and what to do)"

### Add or fix the FAQ

If there's no FAQ section, add one at the end with 4–5 questions.
If there is one, check that each answer starts with a direct response in the first sentence.

### Check the title

If a title was provided, evaluate it against the title rules:
- Does it make a specific promise?
- Is the keyword near the front?
- Is it specific enough to be useful on its own?

If it fails, offer two improved versions.

## Step 3 — Output

Return the full rewritten content.

Before it, add a brief change log (max 6 bullets):

```
### What changed
- Cut 12 banned words (leverage ×3, utilize ×2, seamless ×4, robust ×2, innovative ×1)
- Replaced 4 em-dashes with commas or sentence breaks
- Removed "let's dive in," "in today's landscape," and two essay closers
- Converted 7 passive constructions to active voice
- Added TLDR (the main answer was buried in paragraph 5)
- Rewrote 3 H2s to be specific; added 5-question FAQ
```

Then the full rewritten content.

## What not to change

- The facts, arguments, and substance — you're fixing the delivery, not the thinking
- Specific examples, data points, and personal stories — these are E-E-A-T signals, leave them in
- Code blocks, technical terms, or proper nouns
- The overall length — don't pad to fill space, don't cut substance to be shorter
