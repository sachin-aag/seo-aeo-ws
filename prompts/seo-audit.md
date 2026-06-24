# SEO Audit Prompt

Copy everything below the line and paste it into any LLM (Claude, ChatGPT, Perplexity, etc.). Fill in the bracketed sections with your details.

---

I need a technical SEO audit for a web page. Here are the details:

**Page URL:** [paste URL here]

**Page title (current):** [paste title tag here, or "unknown"]

**Meta description (current):** [paste meta description here, or "none"]

**Raw HTML or page content:** [paste the HTML source or main body text here — use View Source in your browser with Ctrl+U / Cmd+U and paste the full content, OR paste just the readable text]

**Primary keyword I'm targeting:** [what you want this page to rank for]

**Additional context:** [anything relevant — is this a new site? Recently relaunched? Specific traffic issues?]

---

Please audit this page against the following checklist and give me a clear report:

1. **Indexing** — is there anything in the HTML that would prevent indexing (noindex tags, etc.)? Tell me how to verify with `site:domain.com` in Google.

2. **Title tag** — is it 50–60 characters? Does the primary keyword appear in the first three words? Is it specific and compelling?

3. **Meta description** — is it 150–160 characters? Does it contain the keyword naturally and end with a reason to click?

4. **LLM rendering gap** — is the title and key content visible in the raw HTML, or is it likely JS-injected? (Check if the title appears in the source I pasted.)

5. **H1 and heading structure** — one H1 containing the keyword, specific H2s, no skipped heading levels?

6. **Structured data** — any JSON-LD present? Is the right schema type being used for this page type?

7. **Content structure** — does the content open with a clear TLDR? Is there a FAQ section? Are there walls of text that need breaking up?

Format your response as:
- A summary (2–3 sentences on the biggest issues)
- A table with each check marked pass / fail / can't check
- The top 3 fixes to do first (specific, not vague)
- Rewritten title tag and meta description if they failed
