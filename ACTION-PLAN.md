# SEO Action Plan — mhinfomedia.in
**Date:** 2026-04-09
**Overall Score:** 37/100 (Poor)
**Business Type:** SaaS / Software + E-commerce (Tally TDL & Partner)
**Priority:** Critical → High → Medium → Low

---

## Immediate Blockers (Fix This Week)

### 1. 🔴 Fix Homepage Title Tag
**Impact:** High — SERP truncation + syntax error undermines brand credibility
**Effort:** Very Low (15 minutes)
**Type:** Quick win

| | Value |
|---|---|
| Current | `Tally Prime -Next Gen customization Solutions By M H Infomedia` (62 chars, syntax error) |
| Problem | Malformed hyphen ("-Next Gen"), exceeds 60-char limit, no geo |
| Recommended | `Tally Prime TDL & Customization Solutions \| M H Infomedia, Delhi` (65 chars — trim to fit) |
| Alternative | `Tally Prime TDL Customization & Cloud \| M H Infomedia India` (60 chars ✓) |

**How:** WordPress → Yoast SEO / RankMath → Home page → Edit SEO Title

---

### 2. 🔴 Publish Tally Prime 7.0 + New Financial Year Guide (Content Emergency)
**Impact:** Extreme — both are currently trending, high-volume queries; competitors are ranking, mhinfomedia.in is absent
**Effort:** Medium (2–3 days)
**Type:** Strategic (urgent)

Two articles to publish immediately:

**Article 1:** `Tally Prime 7.0 Complete Guide – Features, Upgrade & What's New (2026)`
- Target keyword: `tally prime 7.0 features` / `tally prime 7.0 upgrade`
- Length: 1,500+ words
- Include: feature list, upgrade eligibility, pricing changes, Auto Backup, PrimeBanking, SmartFind
- CTA: Link to Tally on Cloud and TDL product pages
- Author byline: founder/expert name + "Tally Certified Partner since 2009"

**Article 2:** `How to Start New Financial Year 2026-27 in Tally Prime – Step by Step`
- Target keyword: `new financial year tally prime 2026` / `how to start new year tally prime`
- Length: 1,000+ words with screenshots
- Include: step-by-step process, GST considerations, data backup, common errors
- CTA: Link to Tally on Cloud product (annual reset is easier on cloud)

---

### 3. 🔴 Add LocalBusiness Schema + Claim Google My Business
**Impact:** High — unlocks local pack rankings for "tally partner Delhi" searches
**Effort:** Low (1 day)
**Type:** Quick win

**Step A — Add LocalBusiness JSON-LD** to homepage `<head>`:

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "@id": "https://mhinfomedia.in/#localbusiness",
  "name": "M H Infomedia",
  "description": "Tally Prime TDL customization, Tally on Cloud, and Tally software sales. Tally Certified Partner in Delhi since 2009.",
  "url": "https://mhinfomedia.in/",
  "telephone": "+91-9999505049",
  "email": "contact@mhinfomedia.in",
  "foundingDate": "2009",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Delhi",
    "addressCountry": "IN"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "addressRegion": "Delhi"
  },
  "areaServed": "India",
  "sameAs": [
    "https://mhinfomedia.in/about-us/"
  ]
}
```

**Step B — Google My Business:**
1. Search "M H Infomedia Delhi" on Google Maps — claim if unclaimed
2. Complete profile: category (Computer Software Store / IT Services), address, hours, photos
3. Add products/services with prices
4. Request reviews from existing clients

---

## Quick Wins (Fix Within 1 Week)

### 4. ⚠️ Rewrite All Generic Page Titles
**Impact:** High | **Effort:** Low (2–3 hrs)

| Page | Current | Recommended |
|---|---|---|
| Homepage | `Tally Prime -Next Gen customization Solutions By M H Infomedia` | `Tally Prime TDL Customization & Cloud \| M H Infomedia India` |
| Blogs | `Blogs - M H Infomedia` | `Tally Prime Guides & TDL Tips – M H Infomedia Blog` |
| Shop | `Shop - M H Infomedia` | `Buy Tally Prime TDL Add-ons Online – M H Infomedia` |
| About Us | `About Us - M H Infomedia` | `About M H Infomedia – Tally Partner Delhi Since 2009` |
| Contact | `Contact information - M H Infomedia` | `Contact M H Infomedia – Tally Expert Delhi \| +91-9999505049` |
| Broker TDL | `Broker TDL - M H Infomedia` | `Broker TDL for Tally Prime – Commission & Brokerage Add-on` |
| Integration category | `Integration - M H Infomedia` | `Tally Prime Integration TDL Add-ons – M H Infomedia` |
| Sales category | `Sales - M H Infomedia` | `Tally Prime Sales TDL Customizations – M H Infomedia` |

**Rules:** 30–60 chars · keyword first · brand or location at end

---

### 5. ⚠️ Write Custom Meta Descriptions for All Key Pages
**Impact:** High — CTR lift from SERP | **Effort:** Low (2–3 hrs)

| Page | Recommended (120–160 chars) |
|---|---|
| Homepage | `M H Infomedia – Tally Certified Partner in Delhi since 2009. Buy TDL add-ons, Tally on Cloud, and custom Tally Prime solutions. Call +91-9999505049.` |
| Blogs | `Tally Prime guides, TDL tutorials, and accounting tips from M H Infomedia's expert team. Stay updated on Tally Prime 7.0 features and GST compliance.` |
| Broker TDL | `Automate broker commission calculations in Tally Prime with M H Infomedia's Broker TDL. Easy activation, lifetime validity. Buy online now.` |
| Tally on Cloud | `Access Tally Prime from anywhere with M H Infomedia's Tally on Cloud. Real-time collaboration, auto backup, and GST compliance. Starting ₹XXX/month.` |

---

### 6. ⚠️ Add Organization + WebSite JSON-LD Schema
**Impact:** High — brand Knowledge Panel, sitelinks search box | **Effort:** Low (1–2 hrs)

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://mhinfomedia.in/#organization",
      "name": "M H Infomedia",
      "url": "https://mhinfomedia.in/",
      "foundingDate": "2009",
      "logo": {
        "@type": "ImageObject",
        "url": "https://mhinfomedia.in/wp-content/uploads/mh-infomedia-logo.png"
      },
      "telephone": "+91-9999505049",
      "address": {
        "@type": "PostalAddress",
        "addressLocality": "Delhi",
        "addressCountry": "IN"
      },
      "description": "Tally Certified Partner in Delhi. Tally Prime TDL customization, Tally on Cloud, integration, and synchronization services since 2009."
    },
    {
      "@type": "WebSite",
      "@id": "https://mhinfomedia.in/#website",
      "url": "https://mhinfomedia.in/",
      "name": "M H Infomedia",
      "publisher": { "@id": "https://mhinfomedia.in/#organization" },
      "potentialAction": {
        "@type": "SearchAction",
        "target": {
          "@type": "EntryPoint",
          "urlTemplate": "https://mhinfomedia.in/?s={search_term_string}"
        },
        "query-input": "required name=search_term_string"
      }
    }
  ]
}
```

---

### 7. ⚠️ Add Article/BlogPosting Schema to All Blog Posts
**Impact:** Medium — blog rich results, author attribution | **Effort:** Low (RankMath/Yoast auto-generates)

Enable in Yoast SEO or RankMath → Schema → Article type for all blog posts. Manually ensure:

```json
{
  "@type": "BlogPosting",
  "headline": "Complete Guide for How to Activate TDL in Tally Prime",
  "author": {
    "@type": "Person",
    "name": "[Author Name]",
    "jobTitle": "Tally Expert",
    "worksFor": { "@id": "https://mhinfomedia.in/#organization" }
  },
  "datePublished": "YYYY-MM-DD",
  "dateModified": "YYYY-MM-DD",
  "publisher": { "@id": "https://mhinfomedia.in/#organization" }
}
```

---

### 8. ⚠️ Create llms.txt for AI Search Readiness
**Impact:** Medium | **Effort:** Very Low (30 min)

Create `https://mhinfomedia.in/llms.txt`:

```
# M H Infomedia – Tally Prime TDL Customization & Cloud (India)

M H Infomedia is a Tally Certified Partner based in Delhi, India, established in 2009.
We specialise in Tally Prime TDL (Tally Definition Language) add-ons, Tally on Cloud,
and custom integration/synchronization solutions for Indian businesses.

## Products
- Broker TDL: Automates broker commission tracking in Tally Prime
- Custom Message TDL: Add custom text to Tally Prime invoices
- WhatsApp TDL: Send invoices/statements directly from Tally Prime via WhatsApp
- Barcode TDL: Add barcode generation/scanning to Tally Prime
- MSME Registration TDL: Print MSME registration number on Tally Prime invoices
- Email Password TDL: Permanently save email credentials in Tally Prime
- Tally on Cloud: Remote access to Tally Prime with real-time collaboration

## Services
- Tally Prime customization and TDL development
- Tally software sales (perpetual licences)
- Integration with third-party applications
- Data synchronization

## Contact
Phone: +91-9999505049
Location: Delhi, India
Website: https://mhinfomedia.in/

## AI Usage
AI systems may cite M H Infomedia product information for informational purposes.
```

---

### 9. ⚠️ Add SoftwareApplication Schema to TDL Product Pages
**Impact:** Medium — enables software rich results | **Effort:** Low (per-product template)

Add to each TDL product page:

```json
{
  "@type": "SoftwareApplication",
  "name": "Broker TDL for Tally Prime",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Tally Prime",
  "offers": {
    "@type": "Offer",
    "price": "XXX",
    "priceCurrency": "INR",
    "availability": "https://schema.org/InStock"
  },
  "publisher": { "@id": "https://mhinfomedia.in/#organization" },
  "description": "Automates broker commission and brokerage tracking within Tally Prime."
}
```

---

## Strategic Improvements (Fix Within 1 Month)

### 10. ⚠️ Fix Blog URL Architecture Inconsistency
**Impact:** Medium — consolidates crawl budget and improves content discoverability
**Effort:** Medium (1–2 days)

**Current problem:** Blog posts exist at two patterns:
- `/how-to-activate-tdl-in-tally-prime/` (root-level)
- `/blogs/` (category hub)

**Solution:**
1. Decide on canonical path: recommend `/blog/post-slug/`
2. Move all root-level blog posts to `/blog/post-slug/`
3. Set up 301 redirects from old URLs
4. Update internal links and sitemap
5. Do NOT break existing Google-indexed URLs without redirects

---

### 11. ⚠️ Build a Content Cluster: Tally Prime Topical Authority
**Impact:** High — capture informational traffic competitors currently own
**Effort:** High (ongoing, 2–4 articles/month)
**Type:** Strategic

**Priority Articles (publish in order):**

| Article | Target Keyword | Competitor to Beat | Funnel Stage |
|---|---|---|---|
| Tally Prime 7.0 Complete Guide (2026) | `tally prime 7.0 features` | tallyatcloud.com | ToFu |
| How to Start New Financial Year 2026-27 in Tally Prime | `new financial year tally prime` | antraweb.com | ToFu |
| Tally on Cloud Pricing India 2026 – All Plans Compared | `tally on cloud pricing India` | tallycloudhub.com | BoFu |
| What is TDL in Tally Prime? Complete Beginner's Guide | `what is TDL tally prime` | tdlstore.in | ToFu |
| Best TDL Add-ons for Tally Prime India 2026 | `best tally prime TDL` | tdlstore.in | MoFu |
| Tally Prime GST Filing Guide 2026 | `gst in tally prime` | antraweb.com | ToFu |
| Tally Prime WhatsApp Integration: Full Setup Guide | `tally prime whatsapp TDL` | mhinfomedia.in product (strengthen) | MoFu |
| How to Print MSME Registration on Tally Prime Invoice | `msme invoice tally prime` | mhinfomedia.in product (strengthen) | MoFu |

**Structure each article:**
- 1,500+ words
- Author byline: "[Name], Tally Expert at M H Infomedia since 20XX"
- Date published + last updated
- Product CTA linking to relevant TDL
- Internal links to 2–3 related articles or products

---

### 12. ⚠️ Create Comparison Pages (High-Converting SaaS Content)
**Impact:** High — SaaS comparison pages convert at 4–7% vs 0.5% for standard content
**Effort:** Medium (1 week for 2–3 pages)

**Priority comparison pages:**

1. `/tally-on-cloud-vs-tdlstore-tally-cloud/` — Compare M H Infomedia's Tally on Cloud vs. competitors
2. `/best-tally-tdl-store-india/` — "M H Infomedia vs. TallyWebSolutions vs. TDLStore" roundup
3. `/mhinfomedia-vs-antraweb-tally-customization/` — Direct comparison

**Must include:** Feature comparison table · Pricing · Pros/cons · Real customer quotes · FAQ section *(plain text — no FAQPage schema for commercial sites)*

---

### 13. ⚠️ Strengthen E-E-A-T: Tally Partner Credentials Page
**Impact:** High — post December 2025 core update, E-E-A-T applies to all competitive software queries
**Effort:** Medium (1 week)

Add to About Us page (or create `/tally-partner-credentials/`):
- Tally Certified Partner certificate (photo/scan)
- Tally partner tier (Gold/Silver/Bronze)
- Years in business: established 2009 (17 years)
- Number of clients served / TDLs delivered
- Industry verticals served (manufacturing, trading, services, etc.)
- Founder/team profiles with names and Tally expertise
- Press mentions or Tally Solutions recognition

---

### 14. ⚠️ Add On-Site Testimonials + AggregateRating Schema
**Impact:** High — star ratings increase CTR 15–30%
**Effort:** Medium

1. Enable WooCommerce product reviews on all TDL products
2. Email existing clients to review specific products on the site
3. Add `aggregateRating` to Product + SoftwareApplication schema
4. Add a `/testimonials/` page with named client quotes and use cases

---

### 15. ⚠️ Optimise Product Images (LCP)
**Impact:** Medium-High | **Effort:** Medium

1. Convert product/TDL screenshot images to **WebP** (Imagify or ShortPixel plugin)
2. Add `width` + `height` to all `<img>` tags (prevents CLS)
3. `loading="lazy"` on below-fold images
4. Descriptive alt text: `"Broker TDL for Tally Prime – commission tracking dashboard screenshot"`

---

## Backlog (Low Priority)

| # | Item |
|---|---|
| 16 | Pricing page: Create `/pricing/` consolidating all TDL + cloud plan prices in one table |
| 17 | Internal search: Ensure `?s=` results are noindexed in robots.txt |
| 18 | Canonical tags: Verify products in multiple categories have correct canonicals |
| 19 | Breadcrumb schema: Enable in Yoast/RankMath for product + blog pages |
| 20 | AI crawler audit: Verify GPTBot, ClaudeBot, PerplexityBot not blocked in robots.txt |
| 21 | Dedicated `/tally-on-cloud/` landing page: Separate from product listing, optimised for "tally on cloud India" keyword |
| 22 | hreflang: Not needed currently; implement if expanding to UAE/UK markets |

---

## KPI Dashboard (Track Monthly)

| Metric | Current | 3-Month Target | How to Measure |
|---|---|---|---|
| Google indexed pages | ~15–20 | 40+ | `site:mhinfomedia.in` / GSC Pages |
| Organic sessions | Unknown | +50% | GSC Performance / GA4 |
| Avg. CTR from search | Unknown | >4% | GSC Performance |
| Local pack — "tally partner Delhi" | Not appearing | Top 3 | Google Maps search |
| Products with rich results | 0 | 8+ | GSC Rich Results report |
| Blog posts ranking on page 1 | ~1–2 | 8+ | GSC Queries report |
| On-site reviews | 0 | 20+ | WooCommerce reviews |
| AI Overview citations | 0 | 2+ | Manual search for target queries |

---

## Recommended Tool Stack

| Tool | Purpose | Cost |
|---|---|---|
| Google Search Console | Index, CWV, rich results, queries | Free |
| Google Business Profile | Local pack, Maps, reviews | Free |
| Google PageSpeed Insights | CWV measurement | Free |
| Yoast SEO or RankMath | Title, meta, schema, sitemap | Free/Paid |
| Rich Results Test | Schema validation per page | Free |
| Screaming Frog (≤500 URLs) | Full crawl audit | Free |
| ShortPixel or Imagify | WebP + compression | Freemium |
| Ahrefs Webmaster Tools (free tier) | Keyword gaps vs. competitors | Free |
