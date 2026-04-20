# SEO Action Plan — cargosimplify.com
**Date:** 2026-04-20
**Audit Score:** 24/100 (Critical)
**Priority Framework:** P0 = Fix today | P1 = This week | P2 = This month | P3 = Next month
**Market:** Transport Management Software / Lorry Broker SaaS — India

---

## Phase 0 — Emergency Fixes (Fix Today)

### FIX-01: Replace All Placeholder Title Tags

The homepage and booking page have `<title>Document</title>` and `<title>Booking - Document</title>`. These must be replaced immediately.

**Copy-paste replacements for every page:**

```html
<!-- index.html / homepage -->
<title>Lorry Broker & Transport Management Software India | Cargo Simplify</title>
<meta name="description" content="Cargo Simplify is India's lorry broker and transport management software. Generate bilty, e-way bills, Tally integration. Desktop, Web & Mobile App. Free demo.">

<!-- lorry-broker-software.html -->
<title>Lorry Broker Software India — Bilty, LR & Commission Tracking | Cargo Simplify</title>
<meta name="description" content="Cargo Simplify's lorry broker module manages bookings, bilty/LR generation, commission tracking, and fleet assignment. Built for India's GTA transport businesses.">

<!-- booking.html -->
<title>Transport Booking Management Software | Cargo Simplify</title>
<meta name="description" content="Create, assign, and track cargo bookings digitally. Automated bilty generation, WhatsApp sharing, and multi-party shipper-broker-carrier workflows.">

<!-- pricing.html -->
<title>Cargo Simplify Pricing — Desktop, Web & Mobile Plans | Lorry Broker Software</title>
<meta name="description" content="Cargo Simplify pricing: Desktop, Web, and Enterprise plans for lorry brokers and fleet owners. Transparent pricing with Tally integration and mobile app included.">

<!-- about.html -->
<title>About Cargo Simplify — Vapi, Gujarat Transport Software Company</title>
<meta name="description" content="Cargo Simplify is a transport management software company based in Vapi, Gujarat. We build bilty, LR, and fleet management tools for India's lorry brokers.">

<!-- contact.html -->
<title>Contact Cargo Simplify — Free Demo & Support | Vapi, Gujarat</title>
<meta name="description" content="Contact Cargo Simplify for a free software demo, pricing, or support. Based in Vapi, Gujarat. WhatsApp, phone, and email support available.">

<!-- gta-fusion.html -->
<title>GTA FUSION — The Cargo Simplify Transport Management App</title>
<meta name="description" content="GTA FUSION is the web and mobile application powering Cargo Simplify's transport management system. Access your lorry broker dashboard at app.cargosimplify.com.">

<!-- blog-what-is-bilty.html -->
<title>What is Bilty in Transport? Complete Guide for Indian Transporters</title>
<meta name="description" content="Learn what a bilty (lorry receipt/LR) is, its legal importance under GST, required fields, and how to generate digital bilty using transport software. 2026 guide.">

<!-- blog-tms-vs-excel.html -->
<title>Transport Management Software vs Excel — Which is Better for Indian Transporters?</title>
<meta name="description" content="Compare TMS software with Excel for managing Indian transport operations. See when Excel fails and how Cargo Simplify eliminates manual errors and billing delays.">
```

---

### FIX-02: Submit Sitemap to Google Search Console

1. Confirm `https://cargosimplify.com/sitemap.xml` is accessible (check browser)
2. Log in to Google Search Console (https://search.google.com/search-console)
3. Go to **Sitemaps** → Add `sitemap.xml`
4. Use **URL Inspection** tool → request indexing for each of these URLs:
   - `https://cargosimplify.com/`
   - `https://cargosimplify.com/lorry-broker-software/` (after URL rename)
   - `https://cargosimplify.com/pricing/`
   - `https://cargosimplify.com/about/`
   - `https://cargosimplify.com/contact/`
   - `https://cargosimplify.com/gta-fusion/`

**Updated sitemap.xml (replace current):**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://cargosimplify.com/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/lorry-broker-software/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/transport-booking/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/gta-fusion/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/pricing/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/about/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>yearly</changefreq>
    <priority>0.6</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/contact/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>yearly</changefreq>
    <priority>0.6</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/blog/what-is-bilty/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>yearly</changefreq>
    <priority>0.7</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/blog/transport-management-software-vs-excel/</loc>
    <lastmod>2026-04-20</lastmod>
    <changefreq>yearly</changefreq>
    <priority>0.7</priority>
  </url>
</urlset>
```

---

## Phase 1 — Core SEO Implementation (This Week)

### FIX-03: URL Restructuring with 301 Redirects

Rename all URLs from underscored `.html` to clean hyphenated slugs.

**URL mapping (add to server config / .htaccess):**
```apache
# .htaccess redirects — add to Apache root or equivalent Nginx config
RewriteEngine On

# Lorry broker page
Redirect 301 /lorry_broker.html https://cargosimplify.com/lorry-broker-software/
Redirect 301 /lorry-broker.html https://cargosimplify.com/lorry-broker-software/

# Booking page
Redirect 301 /booking.html https://cargosimplify.com/transport-booking/

# Other pages
Redirect 301 /pricing.html https://cargosimplify.com/pricing/
Redirect 301 /about.html https://cargosimplify.com/about/
Redirect 301 /contact.html https://cargosimplify.com/contact/
Redirect 301 /gta-fusion.html https://cargosimplify.com/gta-fusion/
```

---

### FIX-04: Add Schema Markup to Every Page

#### Homepage — Organization + WebSite + SoftwareApplication
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://cargosimplify.com/#organization",
      "name": "Cargo Simplify",
      "alternateName": "CargoSimplify",
      "url": "https://cargosimplify.com/",
      "logo": {
        "@type": "ImageObject",
        "url": "https://cargosimplify.com/images/logo.png",
        "width": 280,
        "height": 60
      },
      "description": "India's lorry broker and transport management software. Bilty generation, e-way bills, Tally integration, and fleet management.",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "[Your Street Address]",
        "addressLocality": "Vapi",
        "addressRegion": "Gujarat",
        "postalCode": "396195",
        "addressCountry": "IN"
      },
      "contactPoint": {
        "@type": "ContactPoint",
        "telephone": "+91-XXXXXXXXXX",
        "contactType": "sales",
        "availableLanguage": ["English", "Hindi", "Gujarati"]
      },
      "sameAs": [
        "https://www.facebook.com/BestLogisticsSoftware/",
        "https://www.youtube.com/@CARGOSIMPLIFY"
      ],
      "foundingDate": "2023",
      "areaServed": "IN"
    },
    {
      "@type": "WebSite",
      "@id": "https://cargosimplify.com/#website",
      "url": "https://cargosimplify.com/",
      "name": "Cargo Simplify",
      "publisher": { "@id": "https://cargosimplify.com/#organization" },
      "potentialAction": {
        "@type": "SearchAction",
        "target": {
          "@type": "EntryPoint",
          "urlTemplate": "https://cargosimplify.com/?s={search_term_string}"
        },
        "query-input": "required name=search_term_string"
      }
    },
    {
      "@type": "SoftwareApplication",
      "@id": "https://cargosimplify.com/#software",
      "name": "Cargo Simplify",
      "alternateName": "GTA FUSION",
      "applicationCategory": "BusinessApplication",
      "operatingSystem": "Windows, Web Browser, Android, iOS",
      "url": "https://cargosimplify.com/",
      "description": "Lorry broker and transport management software for Indian GTA businesses. Includes bilty generation, LR management, e-way bill, commission tracking, and Tally integration.",
      "featureList": [
        "Bilty / LR generation",
        "E-way bill integration",
        "Commission tracking for lorry brokers",
        "Tally Prime integration",
        "WhatsApp LR sharing",
        "Multi-branch support",
        "Android & iOS mobile app",
        "Fleet management",
        "GST-compliant invoicing"
      ],
      "offers": {
        "@type": "AggregateOffer",
        "priceCurrency": "INR",
        "lowPrice": "0",
        "highPrice": "99999",
        "offerCount": "3",
        "offers": [
          {
            "@type": "Offer",
            "name": "Desktop Plan",
            "description": "Single-user desktop software for small lorry brokers"
          },
          {
            "@type": "Offer",
            "name": "Web Plan",
            "description": "Cloud-based multi-user transport management"
          },
          {
            "@type": "Offer",
            "name": "Enterprise Plan",
            "description": "Full-featured TMS with mobile app and advanced reporting"
          }
        ]
      },
      "publisher": { "@id": "https://cargosimplify.com/#organization" }
    }
  ]
}
</script>
```

#### Lorry Broker Page — SoftwareApplication + BreadcrumbList
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "Cargo Simplify Lorry Broker Module",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Windows, Web Browser, Android, iOS",
  "description": "Complete lorry broker management: booking creation, bilty generation, commission tracking, fleet assignment, and party ledgers. Built for Indian GTA transport businesses.",
  "url": "https://cargosimplify.com/lorry-broker-software/",
  "publisher": {
    "@type": "Organization",
    "name": "Cargo Simplify",
    "url": "https://cargosimplify.com/"
  },
  "offers": {
    "@type": "Offer",
    "priceCurrency": "INR",
    "price": "0",
    "priceValidUntil": "2027-01-01",
    "availability": "https://schema.org/InStock",
    "seller": {
      "@type": "Organization",
      "name": "Cargo Simplify"
    }
  }
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://cargosimplify.com/" },
    { "@type": "ListItem", "position": 2, "name": "Lorry Broker Software", "item": "https://cargosimplify.com/lorry-broker-software/" }
  ]
}
</script>
```

#### Blog Post — Article Schema (for what-is-bilty page)
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "What is Bilty in Transport? Complete Guide for Indian Transporters",
  "description": "A bilty (also called Lorry Receipt or LR) is the primary transport document used in India's road freight industry. Learn its legal status under GST, required fields, and how to generate digital bilty.",
  "image": {
    "@type": "ImageObject",
    "url": "https://cargosimplify.com/images/blog/what-is-bilty-guide.jpg",
    "width": 1200,
    "height": 630
  },
  "datePublished": "2026-04-20",
  "dateModified": "2026-04-20",
  "author": {
    "@type": "Organization",
    "name": "Cargo Simplify",
    "url": "https://cargosimplify.com/"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Cargo Simplify",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cargosimplify.com/images/logo.png"
    }
  },
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://cargosimplify.com/blog/what-is-bilty/"
  },
  "keywords": ["bilty", "lorry receipt", "LR in transport", "transport document India", "bilty format GST"]
}
</script>
```

#### GTA FUSION Page — SoftwareApplication + BreadcrumbList
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "GTA FUSION",
  "alternateName": "Cargo Simplify Web App",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Web Browser, Android, iOS",
  "url": "https://app.cargosimplify.com/",
  "description": "GTA FUSION is the web and mobile application platform for Cargo Simplify transport management software. Access your lorry broker dashboard, manage bookings, and generate bilty.",
  "publisher": {
    "@type": "Organization",
    "name": "Cargo Simplify",
    "url": "https://cargosimplify.com/"
  }
}
</script>
```

---

### FIX-05: Add Open Graph Tags to All Pages

Add this block to every page `<head>` (customized per page):
```html
<!-- Open Graph / WhatsApp / Facebook sharing -->
<meta property="og:type" content="website">
<meta property="og:site_name" content="Cargo Simplify">
<meta property="og:title" content="Lorry Broker & Transport Management Software India | Cargo Simplify">
<meta property="og:description" content="India's lorry broker and transport management software. Bilty, e-way bills, Tally integration. Desktop, Web & Mobile App.">
<meta property="og:url" content="https://cargosimplify.com/">
<meta property="og:image" content="https://cargosimplify.com/images/og-homepage.jpg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:locale" content="en_IN">

<!-- Canonical -->
<link rel="canonical" href="https://cargosimplify.com/">

<!-- Robots -->
<meta name="robots" content="index, follow">
```

---

### FIX-06: Updated robots.txt with AI Crawler Management

Replace current `robots.txt` with:
```
# robots.txt — cargosimplify.com
# Updated: 2026-04-20

# Marketing site — allow all crawlers
User-agent: *
Allow: /

# Block common non-content paths
Disallow: /wp-admin/
Disallow: /wp-login.php
Disallow: /cgi-bin/

# AI Crawlers — Allow (opt-in to AI search visibility)
User-agent: GPTBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: Google-Extended
Allow: /

User-agent: Applebot-Extended
Allow: /

User-agent: Bytespider
Allow: /

User-agent: CCBot
Allow: /

# Sitemap
Sitemap: https://cargosimplify.com/sitemap.xml
```

**Also create `robots.txt` at `app.cargosimplify.com`:**
```
# robots.txt — app.cargosimplify.com
# Block all crawlers from the app (login/dashboard pages have no SEO value)
User-agent: *
Disallow: /
```

---

### FIX-07: Create llms.txt for AI Search Discoverability

Create file at `https://cargosimplify.com/llms.txt`:
```
# Cargo Simplify
> India's lorry broker and transport management software. Bilty generation, e-way bill, Tally integration, fleet management. Based in Vapi, Gujarat.

## About
Cargo Simplify (app: GTA FUSION) is a SaaS product built for India's Goods Transport Agency (GTA) businesses. It helps lorry brokers, fleet owners, and transporters manage bookings, generate digital bilty/LR, create e-way bills, track commissions, integrate with Tally Prime, and share documents via WhatsApp.

## Key Features
- Bilty / LR generation (GST-compliant)
- E-way bill creation and submission
- Lorry broker commission tracking
- Tally Prime / TallyERP 9 integration
- WhatsApp-based document sharing
- Multi-branch, multi-user access
- Android + iOS mobile app

## Products
- Desktop Plan: Single-user Windows software
- Web Plan: Cloud-based multi-user TMS
- Enterprise Plan: Full TMS + mobile app + advanced reporting

## Company
- Name: Cargo Simplify
- Location: Vapi, Gujarat, India
- App URL: https://app.cargosimplify.com

## Pages
- /lorry-broker-software/ — Lorry broker module details
- /transport-booking/ — Booking management feature
- /gta-fusion/ — About the GTA FUSION application
- /pricing/ — Pricing plans
- /blog/what-is-bilty/ — Educational guide: what is bilty
- /blog/transport-management-software-vs-excel/ — TMS vs Excel comparison
```

---

## Phase 2 — Off-Page & Trust Building (This Month)

### FIX-08: Software Review Platform Submissions

Submit Cargo Simplify to these directories (ranked by SEO value for India B2B SaaS):

| Platform | URL | Expected DA | Action |
|---|---|---|---|
| SoftwareSuggest | softwaresuggest.com/vendor | 60+ | Submit free listing |
| Capterra | capterra.com/vendors | 80+ | Submit free listing |
| G2 | g2.com/sell | 80+ | Submit free listing |
| GetApp | getapp.com | 75+ | Submit free listing |
| IndiaMART (Software) | indiamart.com | 70+ | Create seller profile |
| Tracxn | tracxn.com | 55+ | Register startup |
| Justdial (Software) | justdial.com | 65+ | Add business listing |
| Sulekha Business | sulekha.com/business | 55+ | Add business listing |

---

### FIX-09: Google Business Profile Setup

1. Go to `business.google.com`
2. Create new profile for "Cargo Simplify"
3. Category: **Software Company**
4. Address: [Full address], Vapi, Gujarat 396195
5. Phone: +91-XXXXXXXXXX
6. Website: https://cargosimplify.com/
7. Upload minimum 5 photos: office exterior, team, screenshots of software
8. Add description (750 chars max):
   > "Cargo Simplify is India's lorry broker and transport management software, based in Vapi, Gujarat. Our GTA FUSION platform helps lorry brokers, fleet owners, and transporters manage bookings, generate digital bilty/LR, create e-way bills, and integrate with Tally. Available as Desktop, Web, and Mobile App. Free demo available."

---

### FIX-10: GTA FUSION Bridge Page

Create `/gta-fusion/` page to capture users who search for the app name. This page should:
- Explain that GTA FUSION = Cargo Simplify's web/mobile app
- Include direct login CTA → `app.cargosimplify.com`
- Include forgot password link
- Explain what GTA stands for (Goods Transport Agency)
- List key app features

**Target keywords:** "GTA FUSION login", "GTA FUSION transport software", "GTA FUSION Cargo Simplify"

---

### FIX-11: Backlink Acquisition Strategy

**Tier 1 — Free directories (do immediately):**
- IndiaMART company profile
- JustDial business listing
- Sulekha business listing
- Vapi local business directories (myvapi.com)
- India Logistics & Transport forums

**Tier 2 — Content outreach (within 30 days):**
- Reach out to logistics blogs for guest posts: "How Indian Lorry Brokers Can Digitize Operations in 2026"
- Submit a PR release to ET Logistics, Supply Chain India, CW (Cargo Week India)
- Ask existing customers to link their website to cargosimplify.com as "powered by" or "built with"

**Tier 3 — YouTube backlinks:**
- Every YouTube video description should link to `https://cargosimplify.com/`
- Create pinned comment with website URL on all videos

---

## Phase 3 — Content Marketing (Next 30–90 Days)

### Blog Content Blueprint

#### Article 1 — "What is Bilty in Transport? Complete Guide for Indian Transporters"
**Target keyword:** "what is bilty in transport" (Informational)
**URL:** `/blog/what-is-bilty/`
**Word count:** 1,500+ words
**Structure:**
1. Introduction — what is bilty, why it matters (150 words)
2. Bilty vs LR vs Consignment Note — are they the same? (200 words)
3. Legal status of bilty under GST (200 words)
4. What a bilty must contain — 10 required fields (250 words, table format)
5. Paper bilty vs digital bilty — pros/cons (200 words)
6. How to generate digital bilty with software (150 words + CTA to Cargo Simplify)
7. Bilty FAQ — 5 common questions (300 words)
8. Conclusion with internal links

**Schema:** Article (BlogPosting)
**Internal links:** → Lorry Broker Software page, → GTA FUSION page

---

#### Article 2 — "TMS vs Excel: Why Indian Transporters Are Switching in 2026"
**Target keyword:** "transport management software vs excel India"
**URL:** `/blog/transport-management-software-vs-excel/`
**Word count:** 1,800+ words
**Structure:**
1. Introduction — why Excel feels "good enough" (150 words)
2. What transport businesses actually need to manage (200 words)
3. Excel limitations for Indian transport (300 words, 8-point list)
4. What TMS software solves — feature-by-feature (300 words)
5. Real scenario: A day in the life with Excel vs TMS (300 words)
6. Hidden cost of Excel (error rates, time, compliance failures) (200 words)
7. How to migrate from Excel to Cargo Simplify in 3 steps (150 words + CTA)
8. Conclusion

**Schema:** Article (BlogPosting)
**Internal links:** → Pricing page, → Lorry Broker Software page

---

#### Article 3 — "E-Way Bill Guide for Lorry Brokers India 2026"
**Target keyword:** "e-way bill lorry broker India" / "e-way bill transport software"
**URL:** `/blog/e-way-bill-guide-lorry-brokers-india/`
**Word count:** 1,500+ words
**Structure:**
1. What is e-way bill? (150 words)
2. When is e-way bill required? Distance and value thresholds (200 words)
3. Who generates the e-way bill? Broker vs shipper vs carrier (200 words)
4. Step-by-step: How to generate e-way bill on GST portal (250 words)
5. Common e-way bill errors and how to fix them (300 words)
6. How Cargo Simplify automates e-way bill generation (150 words + CTA)

**Schema:** Article (BlogPosting)

---

#### Article 4 — "Best Lorry Broker Software India 2026 — Compared"
**Target keyword:** "lorry broker software India" / "best transport management software India"
**URL:** `/blog/best-lorry-broker-software-india/`
**Word count:** 2,000+ words
**Structure:**
1. What to look for in lorry broker software (200 words)
2. Comparison table: Cargo Simplify vs Fleetable vs TransportBook vs BharatSoftware (table format)
3. Deep dive: Cargo Simplify — features, pricing, pros/cons
4. Deep dive: Fleetable
5. Deep dive: TransportBook
6. Which software is right for your business? (use-case matrix)
7. Conclusion + CTA

**Comparison Table:**
| Feature | Cargo Simplify | Fleetable | TransportBook |
|---|---|---|---|
| Bilty/LR Generation | ✅ | ✅ | ✅ |
| E-Way Bill | ✅ | ✅ | ✅ |
| Tally Integration | ✅ | ⚠️ | ❌ |
| WhatsApp LR Sharing | ✅ | ⚠️ | ✅ |
| Desktop App | ✅ | ❌ | ❌ |
| Mobile App | ✅ | ✅ | ✅ |
| Commission Tracking | ✅ | ✅ | ⚠️ |
| Free Trial | ✅ | ✅ | ✅ |
| Vapi/Gujarat Support | ✅ Local | ❌ | ❌ |
| Pricing (from) | Contact | Contact | Contact |

**Schema:** Article + ItemList for the comparison section

---

#### Article 5 — "Tally Integration for Transport Companies India — Complete Guide"
**Target keyword:** "tally transport software integration India"
**URL:** `/blog/tally-transport-software-integration/`
**Word count:** 1,200+ words
**Structure:**
1. Why Indian transporters use Tally
2. The manual sync problem
3. How TMS-Tally integration works
4. What data syncs automatically
5. How Cargo Simplify's Tally integration works (CTA)

---

## E-E-A-T Improvement Checklist

| Action | Priority | Impact |
|---|---|---|
| Add "Customers" / "Trusted by" counter on homepage | P1 | High |
| Create Case Study page (1 real customer story) | P2 | High |
| Add team bio page with photos | P2 | Medium |
| Get featured in any logistics/transport industry blog | P2 | High |
| Add Trustpilot or Google Reviews widget | P2 | High |
| Create Privacy Policy and Terms & Conditions pages | P1 | Medium |
| Add client logos section to homepage | P2 | Medium |
| Link YouTube channel from footer and about page | P1 | Low |

---

## 90-Day SEO Milestone Targets

| Week | Target | How to Verify |
|---|---|---|
| Week 1 | Fix all title tags; submit sitemap to GSC | GSC Coverage report |
| Week 2 | All schema deployed; OG tags live; robots.txt updated | GSC Rich Results Test |
| Week 3 | URLs renamed to hyphenated slugs with 301 redirects | GSC > Pages > Coverage |
| Week 4 | 5+ directory listings submitted | Manual check |
| Month 2 | First 2 blog posts published | GSC Search Analytics |
| Month 2 | Google Business Profile verified | Google Search "Cargo Simplify Vapi" |
| Month 2 | 10+ new backlinks | Google Search Console Links report |
| Month 3 | 10+ pages indexed | `site:cargosimplify.com` in Google |
| Month 3 | Ranking for "GTA FUSION login" brand query | Google Search |
| Month 3 | Ranking for "what is bilty in transport" informational query | Google Search Console |
