---
name: seo-audit
description: Audit a web page against the core technical SEO and AI-visibility checklist. Use this whenever someone shares a URL, pastes HTML, or asks "why isn't my page ranking / why am I not showing up in AI answers." Even if they don't say "SEO audit" — if they're troubleshooting visibility, indexing, or traffic, trigger this skill.
---

# SEO Audit

Your job is to audit a page against the core technical checklist and return a clear, actionable report — not a vague list of suggestions.

## What you need from the user

You need at least one of these:
- The URL of the page to audit
- The raw HTML of the page (paste or file)
- The rendered text content of the page

If they only give you a URL, tell them how to get the raw HTML for the LLM rendering gap check (see below).

## What to check

Work through each section in order. Mark each item as **pass**, **fail**, or **can't check** (if you don't have enough information).

---

### 1. Indexing

Ask the user to run `site:theirdomain.com/their-page` in Google and report back what they see.

- Is the page appearing in results? → pass
- No results? → fail. Instruct them to check Google Search Console → URL Inspection for the reason.

Common reasons a page isn't indexed:
- `noindex` tag in the HTML head
- Blocked by robots.txt
- Page has no inbound links and hasn't been discovered yet
- The page was recently published (can take days to weeks)

---

### 2. Title tag

Extract the `<title>` tag from the HTML.

Check:
- Length: 50–60 characters. Count them. Flag if over 60.
- Primary keyword: does it appear in the first three words? If the page has an obvious topic, flag if the keyword is buried at the end.
- Unique: ask if this title is used on any other page. Duplicate titles are a common silent killer.

Rewrite the title if it fails any of these checks. Offer two alternatives.

---

### 3. Meta description

Extract `<meta name="description">` from the HTML.

Check:
- Length: 150–160 characters. Count them.
- Does it describe what the page actually delivers?
- Does it end with a reason to click?

Missing meta description → write one. Too long → trim it. Generic filler → rewrite it.

---

### 4. The LLM rendering gap

This is the most important check for AI visibility, and most audits miss it.

**What to check:** Is the title tag and key body content present in the raw HTML — or is it injected by JavaScript after the page loads?

**How to check:**
```bash
curl -s https://their-url.com | grep -i "<title\|meta name=\"description\""
```

If the title appears in the curl output → static HTML, LLMs can read it. ✓
If the curl output returns nothing or a generic placeholder → JS-injected, LLMs are blind to it. ✗

**Why this matters:** Google executes JS during crawls. LLMs don't — they fetch raw HTML only. A page that looks fine in a browser can be completely invisible to ChatGPT, Perplexity, and Claude.

If the user can't run curl, instruct them to: View Source in their browser (Ctrl+U / Cmd+U) and search for their title tag. If it's not there, it's JS-rendered.

---

### 5. H1 and heading structure

Find all heading tags in the HTML.

Check:
- Exactly one H1 per page (not zero, not two)
- H1 contains the primary keyword
- H2s are specific and descriptive — flag any that are vague ("More details", "Overview")
- Heading levels don't skip (H1 → H2 → H3, not H1 → H4)

---

### 6. JSON-LD structured data

Look for `<script type="application/ld+json">` in the HTML.

- Present and valid → note what types are included
- Present but wrong type for the page → flag and suggest the right type
- Missing entirely → tell them which schema to add based on page type:
  - Blog post → `Article`
  - Q&A page → `FAQPage`
  - Business homepage → `LocalBusiness`
  - Inner page → `BreadcrumbList`

---

### 7. Content structure (quick check)

Scan the body content if available.

- Does the page open with a clear TLDR or direct answer? → if not, flag it
- Are there FAQ-style sections? → if not, suggest adding one
- Is the content mostly one long block, or broken into scannable sections? → flag walls of text

---

## Output format

Return a report in this structure:

```
## SEO Audit — [Page Title or URL]

### Summary
[2-3 sentence overview of the biggest issues found]

### Findings

| Check | Status | Notes |
|-------|--------|-------|
| Indexed | ✅ / ❌ / ❓ | ... |
| Title tag | ✅ / ❌ | ... |
| Meta description | ✅ / ❌ | ... |
| LLM rendering gap | ✅ / ❌ / ❓ | ... |
| H1 | ✅ / ❌ | ... |
| Structured data | ✅ / ❌ | ... |
| Content structure | ✅ / ❌ | ... |

### Top 3 fixes (do these first)
1. [Most impactful fix with exact action]
2. [Second fix]
3. [Third fix]

### Rewrites
[Include rewritten title tag, meta description if they failed]
```

Keep the fixes specific. "Add a meta description" is not a fix. "Add a 158-character meta description that starts with your primary keyword and ends with a reason to click" is a fix.
