# SEO & AI Discoverability Recommendations - Advanced Arborist LLC

These are recommendations only. No changes have been made. Review and let me know which ones to implement.

---

## HIGH PRIORITY

### 1. Expand Meta Description
Current meta description is decent but could include more local keywords:
- Current: "Professional and dedicated arborist services in Midland, MI. Plant health care, ISA certified consultations, pruning and stump grinding."
- Better: "ISA certified arborist services in Midland, MI. Plant health care, integrated pest management, tree consultations, pruning, and stump grinding. Free estimates. Call 1-989-486-1924."

### 2. Add Structured Data (Schema.org JSON-LD)
This is how Google and AI tools understand your business. Critical for local search.

- **LocalBusiness** + **ProfessionalService** schema:
```json
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "name": "Advanced Arborist LLC",
  "description": "ISA certified arborist services",
  "url": "https://wearetreepeople.com",
  "telephone": "1-989-486-1924",
  "email": "hello@wearetreepeople.com",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "1543 East Ednor Court",
    "addressLocality": "Midland",
    "addressRegion": "MI",
    "addressCountry": "US"
  },
  "sameAs": [
    "https://www.facebook.com/advancedarborist/",
    "https://www.instagram.com/advancedarborist/"
  ],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Arborist Services",
    "itemListElement": [
      {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Plant Health Care / IPM"}},
      {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "ISA Arborist Consultations"}},
      {"@type": "Offer", "itemOffered": {"@type": "Service", "name": "Pruning and Stump Grinding"}}
    ]
  }
}
```

### 3. Add Open Graph and Twitter Card Tags
```html
<meta property="og:title" content="Advanced Arborist LLC - Healthy Trees Start Here!">
<meta property="og:description" content="ISA certified arborist services in Midland, MI. Plant health care, consultations, pruning and stump grinding.">
<meta property="og:image" content="https://wearetreepeople.com/images/logo.jpg">
<meta property="og:url" content="https://wearetreepeople.com">
<meta property="og:type" content="website">
<meta name="twitter:card" content="summary_large_image">
```

### 4. Add sitemap.xml and robots.txt
Even for a single-page site, these are expected by search engines:

sitemap.xml listing index.html
robots.txt:
```
User-agent: *
Allow: /
Sitemap: https://wearetreepeople.com/sitemap.xml
```

---

## MEDIUM PRIORITY

### 5. Page Title Optimization
Current: "Advanced Arborist LLC - Healthy Trees Start Here!"
Better: "Advanced Arborist LLC | ISA Certified Tree Services in Midland, MI"

The title should include location and primary service keyword for local search.

### 6. Add a Favicon
Missing. Use a tree icon or small version of the logo.

### 7. Add Canonical URL
```html
<link rel="canonical" href="https://wearetreepeople.com/">
```

### 8. Expand Service Area Information
The site mentions "Midland, MI" but doesn't list surrounding cities served. For local SEO, mention the full service area:
- "Serving Midland, Bay City, Saginaw, Mt. Pleasant, and surrounding areas"
- This helps capture searches from neighboring cities

### 9. Add More Content
Single-page sites have limited SEO potential. Consider adding:
- **A dedicated Services page** with more detail on each service
- **An About/Our Story page** — who you are, your ISA credentials, experience
- **A Gallery page** — before/after photos of tree work
- **A FAQ page** — common tree care questions (great for AI discovery)

These additional pages would dramatically improve search visibility.

### 10. Image Optimization
- Current images are small (300px wide originals from the WordPress site). Consider uploading higher-resolution versions.
- Add more descriptive alt text:
  - service-ipm.jpg → "Plant health care and integrated pest management for trees in Midland MI"
  - service-consultation.jpg → "ISA certified arborist consulting on tree health"
  - service-pruning.jpg → "Professional tree pruning and stump grinding services"
- Add `width` and `height` attributes to prevent layout shift
- Add `loading="lazy"` to below-the-fold images

---

## LOWER PRIORITY (but valuable)

### 11. Add a 404 Page
Custom page for broken links with a clear path back to the main site.

### 12. Google Business Profile
Not a site change, but critical: make sure there's a Google Business Profile listing for Advanced Arborist LLC at the Midland, MI address. This is the #1 factor for appearing in Google Maps and local search results.

### 13. Add Reviews/Testimonials Section
If there are customer reviews (Google, Facebook, etc.), featuring them on the site with ReviewSchema markup would significantly boost trust and search visibility.

### 14. Improve Internal Anchor Links
Add `id` attributes to each section for smooth-scroll navigation and potential direct linking from search results (section anchors).

---

## AI DISCOVERABILITY SPECIFIC

### 15. llms.txt File
```
# Advanced Arborist LLC
> ISA certified arborist services in Midland, Michigan

## Services
- Plant Health Care / Integrated Pest Management (IPM)
- ISA Arborist Consultations
- Pruning and Stump Grinding
- Free estimates available

## Contact
- Phone: 1-989-486-1924
- Email: hello@wearetreepeople.com
- Address: 1543 East Ednor Court, Midland, MI
- By appointment

## Social
- Facebook: https://www.facebook.com/advancedarborist/
- Instagram: https://www.instagram.com/advancedarborist/

## Related
- Travis Kelly Memorial Forest Preserve: https://www.tkmfp.org
```

### 16. Add "Frequently Asked Questions" Content
AI assistants love FAQ-style content. Questions like:
- "Do I need an arborist or a tree service?"
- "What is integrated pest management?"
- "How much does tree pruning cost?"
- "What does an ISA certified arborist do?"

These map directly to questions people ask AI assistants about tree care.
