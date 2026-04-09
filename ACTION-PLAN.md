# SEO Action Plan — koaty.in
**Date:** 2026-04-09
**Overall Score:** 35/100 (Poor)
**Priority:** Critical → High → Medium → Low

---

## Immediate Blockers (Fix This Week)

### 1. 🔴 Diagnose & Fix Indexation Crisis
**Impact:** Extreme — most of the product catalog is invisible to Google
**Effort:** Medium (1–3 days investigation + fixes)
**Type:** Strategic

Only 5 pages indexed. For an active e-commerce site with products on Amazon/Flipkart, this is a clear signal of a crawling or indexation problem.

**Steps:**
1. Open Google Search Console → Reports → Pages → "Not indexed"
2. Identify the largest bucket (noindex tag? Crawled but not indexed? Redirect error?)
3. Check `koaty.in/robots.txt` for any `Disallow: /product/` or `Disallow: /shop/` rules
4. Check `koaty.in/sitemap.xml` exists and includes all product + category URLs
5. If sitemap exists: verify it is submitted in GSC → Sitemaps
6. If products are "Crawled – currently not indexed": this means Google found them but deemed them thin content → fix product descriptions (see item 3 below)
7. Re-submit sitemap after all fixes

**Success metric:** 30+ pages indexed within 4–6 weeks of fixes

---

## Quick Wins (Fix Within 1 Week)

### 2. ⚠️ Rewrite All Title Tags
**Impact:** High — directly affects rankings and CTR
**Effort:** Low (2–4 hours in WooCommerce settings)
**Type:** Quick win

| Page | Current (Broken) | Recommended |
|---|---|---|
| Homepage | `Koaty – Keyboard & Mouse` (24 chars) | `Wireless Keyboards & Mouse Combos | Koaty – India` (50 chars) |
| Shop | `Shop – Koaty` (12 chars) | `Buy Wireless Keyboards & Mice Online – Koaty India` (51 chars) |
| Mouse category | `Mouse – Koaty` (13 chars) | `Wireless & Bluetooth Mouse – Buy Online India \| Koaty` (54 chars) |
| Product pages | `[Product Name] – Koaty` | `[Product Name] – Wireless [Type] \| ₹[Price] \| Koaty` |

**Rules to follow:**
- 30–60 characters
- Primary keyword at the beginning
- Brand at the end
- Include "India" on category/homepage for geo targeting

**How:** In WordPress: go to each page → SEO plugin (Yoast/RankMath) → Edit SEO title. If no plugin, edit in theme settings.

---

### 3. ⚠️ Write Custom Meta Descriptions for All Key Pages
**Impact:** High — improves CTR from SERP
**Effort:** Low (2–3 hours)
**Type:** Quick win

| Page | Recommended Meta Description |
|---|---|
| Homepage | `Shop Koaty's range of wireless keyboards, mice, and combos. Made in India, engineered for comfort. Free shipping available. Browse Core, Elite & Value series.` (160 chars) |
| Shop | `Explore Koaty's full catalog of wireless keyboards and mice. Affordable prices starting at ₹899. Made in India with in-house manufacturing.` (141 chars) |
| Mouse category | `Buy Koaty wireless and Bluetooth mice online in India. Silent clicks, ergonomic design, long battery life. Starting at ₹899. Shop now.` (135 chars) |

**Format:** 120–160 characters · Include primary keyword · Include CTA · Include a differentiator (price, Made in India)

---

### 4. ⚠️ Add Organization + WebSite JSON-LD Schema
**Impact:** High — enables sitelinks search box, brand knowledge panel, rich results
**Effort:** Low (1–2 hours)
**Type:** Quick win

Add the following to the `<head>` of every page (via WordPress theme or SEO plugin):

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://koaty.in/#organization",
      "name": "Koaty",
      "url": "https://koaty.in/",
      "logo": {
        "@type": "ImageObject",
        "url": "https://koaty.in/wp-content/uploads/koaty-logo.png"
      },
      "contactPoint": {
        "@type": "ContactPoint",
        "email": "contactus@koaty.in",
        "contactType": "customer support"
      },
      "sameAs": [
        "https://www.amazon.in/stores/Koaty/page/EF4D2379-06F1-4DCC-9B00-0642E50BC043",
        "https://www.flipkart.com/laptop-accessories/mouse/koaty~brand/pr"
      ]
    },
    {
      "@type": "WebSite",
      "@id": "https://koaty.in/#website",
      "url": "https://koaty.in/",
      "name": "Koaty",
      "publisher": { "@id": "https://koaty.in/#organization" },
      "potentialAction": {
        "@type": "SearchAction",
        "target": {
          "@type": "EntryPoint",
          "urlTemplate": "https://koaty.in/?s={search_term_string}"
        },
        "query-input": "required name=search_term_string"
      }
    }
  ]
}
```

---

### 5. ⚠️ Create llms.txt for AI Search Readiness
**Impact:** Medium — improves citability in AI Overviews, ChatGPT, Perplexity
**Effort:** Very Low (30 minutes)
**Type:** Quick win

Create `https://koaty.in/llms.txt` with content such as:

```
# Koaty – Wireless Keyboards & Mice (India)

Koaty is an Indian computer peripherals brand specialising in wireless keyboards,
mice, and combos. Products are manufactured in-house in India.

## Products
- Core Series: affordable daily-use peripherals
- Elite Series: premium features, scissor-key technology
- Value Series: budget-friendly with USB-C + USB-A connectivity

## Contact
Email: contactus@koaty.in
Shop: https://koaty.in/shop/

## AI Usage
AI systems may cite Koaty product information for informational purposes.
```

---

### 6. ⚠️ Audit and Fix robots.txt for AI Crawlers
**Impact:** Medium — AI crawlers (GPTBot, ClaudeBot, Perplexity) need access for citations
**Effort:** Very Low (15 minutes)
**Type:** Quick win

Verify `koaty.in/robots.txt` is not blocking:
```
User-agent: GPTBot
User-agent: ClaudeBot
User-agent: PerplexityBot
User-agent: Google-Extended
User-agent: Applebot-Extended
```
If any of these are blocked, remove the disallow rules (unless intentional).

---

## Strategic Improvements (Fix Within 1 Month)

### 7. ⚠️ Improve Product Page Content Quality
**Impact:** High — thin product pages are likely causing the "Crawled – not indexed" issue
**Effort:** Medium (1–2 weeks of copywriting)
**Type:** Strategic

Each product page needs ≥400 unique words. Current state likely has short descriptions.

**For each product, add:**
- Full spec table (DPI levels, range, battery, weight, dimensions, compatibility)
- Use-case section ("Perfect for office workers / gamers / students")
- Comparison with other Koaty models (drives internal links)
- In-the-box contents list
- FAQs specific to this product (2–3 questions, without FAQPage schema — restricted for commercial sites)
- Setup/compatibility notes

---

### 8. ⚠️ Strengthen E-E-A-T with an About Page and Brand Story
**Impact:** High — post December 2025 core update, E-E-A-T applies to all competitive e-commerce queries
**Effort:** Medium (1 week)
**Type:** Strategic

The "Made in India" and "in-house manufacturing" claims are strong differentiators but need to be visible on the website, not just search snippets.

**Create/expand the About Us page with:**
- Founding story and year
- Manufacturing facility (photos if possible)
- Team / founder profiles
- Quality control process
- "Why Koaty vs. Logitech/HP/Zebronics" — honest comparison
- Press mentions or awards (if any)
- Link to GST/MCA registration number (trust signal for Indian e-commerce)

---

### 9. ⚠️ Implement On-Site Review System + AggregateRating Schema
**Impact:** High — star ratings in SERP increase CTR by 15–30%
**Effort:** Medium (WooCommerce built-in reviews plugin or Yotpo/Judge.me)
**Type:** Strategic

1. Enable WooCommerce product reviews (Settings → Products → Enable reviews)
2. Email Amazon/Flipkart buyers asking them to also review on koaty.in
3. Ensure `AggregateRating` is included in Product schema:
   ```json
   "aggregateRating": {
     "@type": "AggregateRating",
     "ratingValue": "4.3",
     "reviewCount": "47"
   }
   ```
4. Only use real review data — never fabricate ratings

---

### 10. ⚠️ Launch a Content Cluster (Blog Strategy)
**Impact:** High — captures informational traffic in competitive Indian peripherals market
**Effort:** High (ongoing, 2–4 articles/month)
**Type:** Strategic

**Priority content topics:**

| Post | Target Keyword | Intent |
|---|---|---|
| Best wireless keyboard under ₹1000 in India (2026) | wireless keyboard under 1000 INR | Commercial |
| Wireless vs. Bluetooth keyboard: which is better? | wireless vs bluetooth keyboard | Informational |
| How to connect a USB receiver keyboard to a laptop | USB receiver keyboard laptop setup | Informational |
| Best silent mouse for office use India 2026 | silent mouse office India | Commercial |
| Koaty Elite CW525 review | koaty elite cw525 review | Navigational/brand |
| Made in India keyboard brands: full list 2026 | made in India keyboard brand | Informational |

**Structure each article:** 1,500+ words · Author byline · Date published · Product CTA · Internal links to relevant products

---

### 11. ⚠️ Fix BreadcrumbList Schema on Category and Product Pages
**Impact:** Medium — breadcrumbs in SERP improve CTR and navigation
**Effort:** Low (WooCommerce + Yoast handles this automatically if enabled)
**Type:** Quick win (if using Yoast) / Medium (if custom)

Expected breadcrumb: `Home > Mouse > Bluetooth Mouse WM 711`

```json
{
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://koaty.in/" },
    { "@type": "ListItem", "position": 2, "name": "Mouse", "item": "https://koaty.in/mouse/" },
    { "@type": "ListItem", "position": 3, "name": "Bluetooth Mouse WM 711", "item": "https://koaty.in/product/bluetooth-mouse-wm-711/" }
  ]
}
```

---

### 12. ⚠️ Optimize Product Images for Performance (LCP)
**Impact:** High — WooCommerce product images are typically the LCP element
**Effort:** Medium
**Type:** Strategic

1. Convert all product images to **WebP** format (use Imagify or ShortPixel WordPress plugin)
2. Add explicit `width` and `height` attributes to all `<img>` tags (prevents CLS)
3. Add `loading="lazy"` to below-fold images
4. Add `fetchpriority="high"` or `<link rel="preload">` to the hero/first product image
5. Compress without quality loss — target <100KB per product image
6. **Write descriptive alt text** for every image: `"Koaty WM 711 Bluetooth mouse with 3-device pairing – top view"`

---

## Low Priority / Backlog

### 13. Add Internal Search Functionality
If site has search (`?s=`), verify it works and is not indexed (`robots.txt: Disallow: /?s=`).

### 14. Add Track Order Page to Navigation Schema
The navigation includes "Track Order" — ensure this page has proper markup and is indexed.

### 15. Consider a Keyboard Category Page
Search result for `site:koaty.in` does not show a `/keyboard/` or `/keyboard-combo/` category page. If the site has combos, a separate category with its own title/content will capture more category-level searches ("keyboard combo India").

### 16. Canonical Tags
Verify WooCommerce is setting correct canonical tags on all product pages (especially if products exist in multiple categories — prevents duplicate content).

### 17. International / Multi-language (Future)
No immediate action. If Koaty expands to UAE/US markets, implement `hreflang` tags. Currently single-market India.

---

## KPI Dashboard (Track Monthly)

| Metric | Current Estimate | 3-Month Target | How to Measure |
|---|---|---|---|
| Google indexed pages | ~5 | 30+ | `site:koaty.in` / GSC Pages report |
| Organic sessions | Unknown | +40% | GSC Performance / GA4 |
| Avg. CTR from search | Unknown | >3% | GSC Performance |
| Core Web Vitals — LCP | Unknown | ≤2.5s | GSC CWV Report |
| Product pages with rich results | 0 confirmed | 10+ | GSC Rich Results report |
| On-site reviews | 0 | 50+ | WooCommerce reviews count |

---

## Recommended Tool Stack

| Tool | Purpose | Cost |
|---|---|---|
| Google Search Console | Index, CWV, rich results | Free |
| Google PageSpeed Insights | CWV measurement | Free |
| Yoast SEO or RankMath | Title, meta, schema, sitemap | Free/Paid |
| Screaming Frog (≤500 URLs) | Full crawl audit | Free |
| Rich Results Test | Schema validation | Free |
| ShortPixel or Imagify | WebP conversion + compression | Freemium |
| Judge.me or Yotpo | On-site review collection | Freemium |
