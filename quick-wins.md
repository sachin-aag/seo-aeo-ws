# Quick Wins

Five things you can do today, under 30 minutes each, with no paid tools.

These won't replace a full SEO strategy. But they fix the most common silent killers — issues that cost you traffic you've already earned.

---

## 1. Check if you're actually indexed (5 minutes)

Type this into Google:
```
site:yourdomain.com
```

**If your pages appear:** you're indexed. Move on.

**If nothing appears:** stop. You're invisible to Google and this is your entire problem. Go to Google Search Console → URL Inspection → enter your homepage URL → Request Indexing.

Common reasons pages aren't indexed:
- `noindex` tag accidentally left in the HTML
- robots.txt blocking the wrong pages
- The site is so new Google hasn't discovered it yet (submit your sitemap)

This takes 5 minutes to check and can unblock weeks of invisible work.

---

## 2. Fix your homepage title tag (10 minutes)

Open your homepage. View Source (Ctrl+U / Cmd+U). Find `<title>`.

Check three things:
1. Is it under 60 characters? (Count them — Google cuts off at ~60)
2. Does your primary keyword appear in the first three words?
3. Is it different from every other page on your site?

If it fails any of these, rewrite it now. Use the `meta-optimizer` skill or prompt to get three alternatives in 2 minutes.

Most business homepages have titles like "Welcome to [Brand Name] | Home" — which is a wasted 40 characters.

---

## 3. Add a TLDR to your most-visited page (10 minutes)

Open your analytics. Find the page that gets the most traffic or the most impressions in Search Console.

Read the first 200 words. Does it answer anything in those 200 words?

If not: add a TLDR block right after the H1. 2–3 sentences. The core answer, stated directly.

Before:
```
Search engine optimization has become increasingly important in recent years.
As more businesses move online, the competition for visibility has intensified...
```

After:
```
**TL;DR:** Your page needs to answer the question in the first paragraph.
If it takes more than 200 words to get to your point, AI tools won't cite you
and human readers won't scroll.
```

This is the single highest-leverage change for AI visibility. AI tools extract the first 200 words of a page when deciding what to cite.

---

## 4. Check your AI visibility baseline (10 minutes)

Open ChatGPT or Perplexity. Turn on web search mode. Type:
```
best [your category] in [your city]
```

What do you see?

- **You appear:** Note which page is cited. That page is your strongest content — model more content after it.
- **A competitor you've never heard of appears:** Look at their page. It's almost certainly well-structured with a clear TLDR, specific H2s, and a FAQ section. That's what you're competing against.
- **No one appears and AI says it doesn't know:** That's an opportunity to own the answer. Write a piece that directly answers the query with a clear structure.

This costs nothing and takes 10 minutes. It tells you exactly where you stand before spending any time on content.

---

## 5. Request indexing for your three best pages (5 minutes)

Go to Google Search Console.

For each of your top three pages (homepage, best blog post, key service page):
1. Click URL Inspection
2. Enter the page URL
3. If it shows "URL is not on Google" — click Request Indexing
4. If it shows a last crawl date older than 3 months — click Request Indexing anyway

Google doesn't always re-crawl updated content quickly. Requesting indexing after any change (new content, title tag update, restructured FAQ) speeds up the process.

This takes 5 minutes and ensures changes you've already made actually get picked up.

---

## What's next

Once you've done these five things, you have a baseline:
- You know if you're indexed
- Your homepage title is fixed
- Your best page has a TLDR
- You know your AI visibility baseline
- Your top pages are queued for re-crawl

That's a clean starting point. From here, work through the 90-day plan (`worksheets/90-day-tracker.md`).
