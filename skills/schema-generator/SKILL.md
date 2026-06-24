---
name: schema-generator
description: Generate JSON-LD structured data for any web page. Use this whenever someone asks about structured data, schema markup, rich results, or JSON-LD. Also trigger when someone wants their page to appear in AI answers or get rich snippets in Google — structured data is one of the highest-leverage technical changes for both. Even if they don't know the term "JSON-LD," if they want their content to be understood by machines, this is the skill to use.
---

# Schema Generator

Structured data is how you tell Google and LLMs exactly what your content is — not just what it looks like. A page with well-formed JSON-LD gets parsed more accurately, has a higher chance of rich results, and is easier for AI tools to cite.

Your job is to produce ready-to-paste JSON-LD for the right schema type based on what the user tells you about their page.

## Step 1: Choose the right schema type

Ask the user what type of page they're working on, or infer it from context.

| Page type | Primary schema | Often also add |
|-----------|---------------|----------------|
| Blog post or article | `Article` | `BreadcrumbList` |
| Page with Q&A or FAQ | `FAQPage` | — |
| Local business homepage | `LocalBusiness` | `BreadcrumbList` |
| Product page | `Product` | `BreadcrumbList` |
| How-to guide | `HowTo` | `BreadcrumbList` |
| Event listing | `Event` | — |
| Person / author bio | `Person` | — |
| Inner page (any type) | `BreadcrumbList` | depends on content |

A page can have multiple JSON-LD blocks. Adding both `Article` and `FAQPage` to a blog post that ends with a FAQ section is correct — not redundant.

## Step 2: Collect the required fields

### For Article:
- Headline (title of the post)
- URL of the page
- Date published (ISO 8601: YYYY-MM-DD)
- Date modified
- Author name
- Author URL or profile page (optional but recommended)
- Publisher name
- Publisher logo URL (should be a square PNG, 60x60px recommended)
- Description (1–2 sentences)
- Featured image URL

### For FAQPage:
- List of questions and answers (at least 3 pairs)
- Note: answers must match what's on the page — Google validates this

### For LocalBusiness:
- Business name
- Business type (use the most specific Schema.org type: `Restaurant`, `MedicalClinic`, `LegalService`, etc.)
- Street address, city, postal code, country
- Phone number
- Website URL
- Opening hours
- Description

### For BreadcrumbList:
- The full breadcrumb path (e.g. Home → Blog → Article Title)
- URL for each step

## Step 3: Generate the JSON-LD

Produce clean, valid JSON-LD ready to paste into a `<script type="application/ld+json">` tag in the HTML `<head>`.

Use the templates in the `references/` folder as your base. Always:
- Fill every field the user provided
- Leave optional fields out rather than putting in placeholder values — empty string values fail validation
- Use ISO 8601 format for dates
- Use fully qualified URLs (https://...), not relative paths

## Step 4: Tell them where to put it

The JSON-LD block goes inside the `<head>` tag of the HTML. If they're on a CMS:
- WordPress: use the Yoast SEO or Rank Math plugin, or paste into a Custom HTML block in the page head
- Webflow: site settings → Custom Code → Head Code
- Squarespace: Settings → Advanced → Code Injection → Header
- Shopify: edit theme.liquid, paste before `</head>`
- Next.js: use the `<Script>` component with `strategy="beforeInteractive"` or put it directly in the `<Head>` component

## Step 5: Tell them how to validate

After adding the schema, validate it at **Google's Rich Results Test**: https://search.google.com/test/rich-results

A valid result means no errors (warnings are fine). An error means the schema won't be used for rich results — fix it before moving on.

## Example output

**Input:** Blog post about fixing 404 errors, published 2025-03-15, author Jane Smith, site is example.com

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "How to Fix 404 Errors: A Complete Guide",
  "description": "A step-by-step guide to finding, fixing, and preventing 404 errors on your website.",
  "url": "https://example.com/blog/fix-404-errors",
  "datePublished": "2025-03-15",
  "dateModified": "2025-03-15",
  "author": {
    "@type": "Person",
    "name": "Jane Smith",
    "url": "https://example.com/about"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Example",
    "logo": {
      "@type": "ImageObject",
      "url": "https://example.com/logo.png"
    }
  },
  "image": "https://example.com/images/404-guide-cover.jpg"
}
</script>
```

See `references/` for templates for `Article`, `FAQPage`, and `LocalBusiness`.
