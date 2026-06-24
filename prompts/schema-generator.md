# Schema Generator Prompt

Copy everything below the line and paste it into any LLM. Fill in the bracketed sections.

---

I need JSON-LD structured data for a web page. Please generate the right schema markup based on my page details.

**Page type:** [blog post / article / page with FAQ / local business homepage / product page / how-to guide / other]

**Page URL:** [full URL including https://]

**Page title:** [the title of this page]

**Page description:** [1–2 sentence summary of what the page covers]

Fill in whichever fields below apply to your page type:

---

**For a blog post or article:**
- Date published: [YYYY-MM-DD]
- Date last modified: [YYYY-MM-DD]
- Author name: [full name]
- Author profile URL: [URL, or leave blank]
- Publisher / brand name: [your company or site name]
- Publisher logo URL: [URL to your logo image, ideally 60x60px PNG]
- Featured image URL: [URL to the main image for this article]

**For a FAQ page or a page with a FAQ section:**
- List your Q&A pairs below (add as many as you have, minimum 3):
  - Q: [question]?
    A: [answer — direct first sentence, then supporting detail]
  - Q: [question]?
    A: [answer]
  - Q: [question]?
    A: [answer]

**For a local business:**
- Business name: [exact legal name]
- Business type: [most specific type, e.g. Restaurant, LegalService, MedicalClinic, MarketingAgency]
- Street address: [street and number]
- City: [city]
- Postal code: [postal code]
- Country code: [2-letter country code, e.g. DE, US, GB]
- Phone: [in international format, e.g. +491234567890]
- Opening hours: [e.g. Mon–Fri 9:00–18:00]
- Social media URLs: [LinkedIn, Instagram, etc.]

---

Please:
1. Generate the complete JSON-LD ready to paste into a `<script type="application/ld+json">` tag
2. Tell me exactly where in my HTML to place it (it goes in the `<head>` section)
3. Tell me how to validate it (Google Rich Results Test)
4. Note if I should add multiple schema types (e.g., Article + FAQPage)
