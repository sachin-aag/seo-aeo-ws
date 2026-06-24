---
name: meta-optimizer
description: Write or rewrite a page's title tag and meta description for SEO. Use this whenever someone shares a page and asks why it's not getting clicks, wants to improve their CTR, or asks what their title tag or meta description should say. Also trigger when someone pastes a title that's too long, too vague, or missing the primary keyword — even if they don't say "meta."
---

# Meta Optimizer

Title tags and meta descriptions are the smallest pieces of text with the highest return on investment in SEO. A bad title loses you clicks from pages that already rank. A good title wins clicks you didn't have to earn through new content.

Your job is to produce options that are specific, keyword-first, and give the reader a reason to click.

## What you need from the user

- The page topic or URL
- The primary keyword they're targeting
- The current title tag and meta description (if they exist — paste them so you can improve, not just replace)
- Any character limits they're working within (default: 60 chars for title, 160 for meta description)

## Rules for title tags

**Length:** 50–60 characters. Count every character including spaces. Google truncates at roughly 600px width, which is about 60 characters. Over that and the title gets cut off mid-word in search results.

**Keyword position:** The primary keyword should appear within the first three words. Google and LLMs both weight words at the start of the title more heavily.

**Promise:** The title should make a clear, specific promise that matches what's on the page. Vague titles ("Everything About SEO") lose to specific ones ("How to Check If Your Page Is Indexed").

**No clickbait:** Titles that over-promise relative to the content hurt engagement metrics, which hurt rankings. The title should be the honest version of the best thing about the page.

**No keyword stuffing:** One primary keyword. One. Using it twice doesn't double the ranking benefit — it makes the title read like a robot wrote it.

## Rules for meta descriptions

**Length:** 150–160 characters. Google sometimes rewrites these anyway, but a good one still controls the default. Count every character.

**Contains the keyword:** Naturally, not forcefully. Google bolds the keyword in the description when it matches the search query — this increases CTR.

**Ends with a hook:** The last 20 characters should give the reader a reason to click. Not a call-to-action cliché ("Click here!") but a specific value statement ("Takes 2 minutes." / "Free template included." / "No account needed.").

**Matches what's on the page:** A meta description that over-sells the content crushes bounce rate, which signals poor quality to Google.

## Output format

Always produce three title options and two meta description options. The user can pick and combine.

```
### Title options

1. [Option 1] — [character count] chars
   Why: [one sentence on what this option does well]

2. [Option 2] — [character count] chars
   Why: [one sentence]

3. [Option 3] — [character count] chars
   Why: [one sentence]

### Meta description options

1. [Option 1] — [character count] chars

2. [Option 2] — [character count] chars
```

After the options, note any red flags in the original if one was provided (e.g., "your current title is 82 characters — it's being cut off at 'SEO' in search results").

## Example

**Input:**
- Page topic: Guide to fixing 404 errors
- Primary keyword: fix 404 errors
- Current title: "How to Deal with 404 Errors on Your Website | The Complete Guide for Beginners and Professionals" (98 chars)
- Current meta: "404 errors are a problem. Learn how to fix them." (48 chars — too short)

**Output:**

### Title options

1. Fix 404 Errors: The Complete Guide — 38 chars
   Why: Keyword-first, concise, no truncation risk.

2. How to Fix 404 Errors (And Prevent New Ones) — 46 chars
   Why: Addresses both the fix and the follow-up concern readers have.

3. Fix 404 Errors Fast — 5 Steps That Actually Work — 51 chars
   Why: Adds urgency and specificity; good if the page is a step-by-step guide.

### Meta description options

1. 404 errors send visitors to dead ends and hurt your SEO. This guide shows you how to find them, fix them, and stop them coming back. Takes under 30 minutes. — 158 chars

2. A 404 error means a page your visitors expected doesn't exist. Here's how to audit your site, redirect broken URLs, and prevent 404s from hurting your rankings. — 161 chars ← trim by 1

**Red flag in current title:** 98 characters. Google is truncating it after "The Complete Guide" — readers never see "for Beginners and Professionals."
