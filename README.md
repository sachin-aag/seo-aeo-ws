# Get Found by Humans and AI

The companion repo to the workshop by [Narayanan (Rayn)](https://github.com/narayanan-rayn).

97% of AI citations come from pages already ranking in Google's top 20. That means SEO and GEO (Generative Engine Optimization) are the same skill — pointed at two outputs. This repo gives you the tools to work that skill.

---

## What's in here

| Folder | What it contains |
|--------|-----------------|
| [`skills/`](skills/) | 11 Claude Code skills — install and run in your terminal |
| [`prompts/`](prompts/) | Same 11 prompts as plain text — copy-paste into any LLM |
| [`best-practices.md`](best-practices.md) | Technical checklist + content do/don't guide |
| [`worksheets/`](worksheets/) | Topic map builder, 90-day tracker |
| [`checklists/`](checklists/) | Pre-publish checklist, monthly SEO cadence |
| [`quick-wins.md`](quick-wins.md) | 5 actions you can take in under 30 minutes, no paid tools |
| [`tools.md`](tools.md) | Curated free-first tool list, one pick per job |

---

## The 11 skills

| Skill | What it does |
|-------|-------------|
| [`seo-audit`](skills/seo-audit/) | Audit a page against the core technical checklist |
| [`keyword-cluster`](skills/keyword-cluster/) | Build a topic cluster for your niche |
| [`content-brief`](skills/content-brief/) | Generate a full content brief for a target topic |
| [`meta-optimizer`](skills/meta-optimizer/) | Write or rewrite your title tag and meta description |
| [`schema-generator`](skills/schema-generator/) | Generate JSON-LD structured data for any page type |
| [`faq-builder`](skills/faq-builder/) | Extract and format a citable FAQ block |
| [`content-rewriter`](skills/content-rewriter/) | Restructure existing content for AI citability |
| [`geo-check`](skills/geo-check/) | Check your AI visibility across ChatGPT and Perplexity |
| [`backlink-gap`](skills/backlink-gap/) | Find where competitors are cited and you're not |
| [`90-day-plan`](skills/90-day-plan/) | Generate a personalized 90-day SEO + GEO action plan |
| [`humanise`](skills/humanise/) | Strip AI language and layer in SEO/AEO structure |

---

## Quick start

### Option A — Claude Code skills (recommended)

Install a skill by copying its folder into your Claude Code skills directory, then trigger it by describing what you want in Claude Code.

```bash
# Clone this repo
git clone https://github.com/your-org/get-found-by-humans-and-ai.git

# Copy skills into your Claude Code skills directory
cp -r get-found-by-humans-and-ai/skills/humanise ~/.claude/skills/
cp -r get-found-by-humans-and-ai/skills/seo-audit ~/.claude/skills/
# ... repeat for any skills you want
```

Then in Claude Code, just describe your task — e.g. "humanise this blog post" or "run an SEO audit on this page" — and the skill triggers automatically.

### Option B — Plain prompts (works anywhere)

Open any file in [`prompts/`](prompts/), copy the prompt, fill in your details, and paste it into Claude, ChatGPT, Perplexity, or any other LLM.

---

## Where to start

**If you're brand new:** Read [`quick-wins.md`](quick-wins.md) first — five actions, under 30 minutes each, no paid tools.

**If you have a website:** Run the [`seo-audit`](skills/seo-audit/) skill on your homepage first, then fix what it flags before doing anything else.

**If you have existing content:** Run [`humanise`](skills/humanise/) on your best-performing piece to see what a rewrite looks like before committing to a full content overhaul.

**If you're starting from scratch:** Fill in the [`topic map worksheet`](worksheets/topic-map.md) first, then use [`content-brief`](skills/content-brief/) to plan your first three pieces.

---

## The 90-day view

- **Month 1:** Fix the technical basics, finalize your keyword clusters, publish piece 1
- **Month 2:** Publish pieces 2–3, add TLDR/FAQ to existing pages, start first outreach batch
- **Month 3:** Double down on what's working, re-check AI visibility, set your ongoing cadence

SEO is a mortgage, not a lottery ticket. Pay it monthly, build equity.
