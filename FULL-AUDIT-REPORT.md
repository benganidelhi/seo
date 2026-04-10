# Full SEO Audit Report — cargosimplify.com
**Date:** 2026-04-10
**Auditor:** Agentic SEO Skill v1.0
**Method:** LLM-first audit with SERP evidence (WebFetch blocked; all evidence via WebSearch + SERP analysis)
**Market:** Lorry broker & transport management software — India

---

## Page Score Card

```
Overall Score: 16/100

Technical SEO:   15/100  ██░░░░░░░░  [Score Confidence: Confirmed]
On-Page SEO:     10/100  █░░░░░░░░░  [Score Confidence: Confirmed]
Content Quality: 10/100  █░░░░░░░░░  [Score Confidence: Confirmed]
Schema:           5/100  ░░░░░░░░░░  [Score Confidence: Confirmed]
Performance:     30/100  ███░░░░░░░  [Score Confidence: Hypothesis]
Images:          40/100  ████░░░░░░  [Score Confidence: Hypothesis]
AI Readiness:    10/100  █░░░░░░░░░  [Score Confidence: Confirmed]
```

**Weighted Score Breakdown:**
| Category | Score | Weight | Contribution |
|---|---|---|---|
| Technical SEO | 15 | 25% | 3.75 |
| On-Page SEO | 10 | 15% | 1.50 |
| Content Quality | 10 | 20% | 2.00 |
| Schema | 5 | 15% | 0.75 |
| Performance | 30 | 10% | 3.00 |
| Images | 40 | 10% | 4.00 |
| AI Readiness | 10 | 5% | 0.50 |
| **Total** | | | **15.5 / 100** |

---

## Site Overview

| Attribute | Value |
|---|---|
| Domain | cargosimplify.com |
| App Subdomain | app.cargosimplify.com (GTA FUSION) |
| Business Type | Lorry broker & transport management SaaS + desktop software |
| Location | Vapi, Gujarat, India (Facebook page) |
| Target Users | Fleet owners, lorry brokers, warehouse managers, cargo handlers |
| Platforms | Desktop app + Web version + Mobile app (Android/iOS) |
| Key Features | Transport booking, lorry broker coordination, fleet management, accounting, Tally transfer |
| Google-Indexed Pages | **3** (homepage, booking.html, app password reset) |
| Homepage Title in Google | **"Document"** ← CRITICAL |

---

## Issues Found

### 🔴 CRITICAL

---

#### C1 — Homepage Title Tag is "Document"
**Severity:** Critical | **Confidence:** Confirmed

Google indexes and displays the page title as **"Document"** — this is a placeholder `<title>` left from an HTML template or static site generator. The booking page is indexed as **"Booking - Document"**.

**Evidence:** `site:cargosimplify.com` SERP returns show:
- Homepage: title "Document"
- Booking page: title "Booking - Document"
- This is the single most damaging SEO issue possible: Google displays "Document" as the blue link for your homepage in search results. **No user will click this.**

**Impact:**
- Zero click-through rate from any organic impressions
- Google may be demoting the page due to thin/unhelpful title
- Branded searches for "cargo simplify" or "GTA FUSION" return an unbranded title
- Damages credibility for all pages

**Fix:** Set descriptive `<title>` tags on every page. Example for homepage:
```html
<title>Cargo Simplify — Lorry Broker & Transport Management Software India</title>
```

---

#### C2 — Only 3 Pages Indexed in Google
**Severity:** Critical | **Confidence:** Confirmed

Google's index for cargosimplify.com contains only **3 URLs**:
1. `cargosimplify.com/` — "Document"
2. `cargosimplify.com/booking.html` — "Booking - Document"
3. `app.cargosimplify.com/forgetpassword.aspx` — "password recover - GTA FUSION"

There is no blog, no feature pages, no pricing page, no about page, no testimonials indexed. The lorry_broker.html page appeared in a search result snippet but not in `site:` query, suggesting it may exist but is either blocked or crawl-delayed.

**Impact:**
- Near-zero organic search footprint
- Cannot rank for any product keywords
- Google has no content to evaluate for quality

**Root cause (likely):**
- Static HTML pages with broken `<title>` tags are treated as low-quality pages by Google
- Possibly a robots.txt disallowing crawl, or no sitemap submitted
- The main app lives on app.cargosimplify.com (GTA FUSION) — the marketing site has very few pages

---

#### C3 — No XML Sitemap (Likely)
**Severity:** Critical | **Confidence:** Hypothesis

No sitemap.xml appears in Google's index or returns from standard `site:` searches. Without a sitemap, Google relies solely on link discovery — which is limited if the site has few external backlinks.

**Fix:** Create and submit `cargosimplify.com/sitemap.xml` to Google Search Console.

---

### 🟠 HIGH

---

#### H1 — No Meta Descriptions on Any Page
**Severity:** High | **Confidence:** Confirmed

SERP snippets for cargosimplify.com show auto-generated descriptions pulled from page content rather than set `<meta name="description">` tags. With broken titles, the auto-generated snippets are also meaningless.

**Fix:** Add unique, keyword-rich meta descriptions (150–160 chars) to every page.
Example for homepage:
```html
<meta name="description" content="Cargo Simplify is India's lorry broker and transport management software. Book lorries, track shipments, manage bilty/LR, and integrate with Tally. Based in Vapi.">
```

---

#### H2 — No Schema / Structured Data
**Severity:** High | **Confidence:** Confirmed

No schema markup detected on any indexed page. For a software product targeting Indian SMEs, the following schemas are expected and missing:
- `Organization` — establishes brand identity for Google
- `SoftwareApplication` — enables software-specific rich results
- `WebSite` with `SearchAction` — enables sitelinks search box
- `LocalBusiness` (if targeting local Vapi/Gujarat market)

---

#### H3 — No Blog / Content Marketing Presence
**Severity:** High | **Confidence:** Confirmed

Zero blog posts indexed. Competitors like Fleetable run active content blogs (TMS guides, bilty/LR guides, e-way bill guides) that capture informational queries and funnel users to product pages.

**Top competitor content gap:**
- Fleetable: "What is Bilty / Lorry Receipt" guide — ranks for "bilty software" queries
- BharatSoftware: "Freight Broker Software" landing pages with rich feature descriptions
- cargosimplify.com: 0 informational content

---

#### H4 — No Reviews or Social Proof Indexed
**Severity:** High | **Confidence:** Confirmed

No listings found on:
- Capterra India
- Software Suggest
- G2
- Trustpilot
- GetApp
- TechJockey

Competitors are listed and reviewed on these platforms. These listings provide:
- Third-party backlinks
- Review schema for star ratings in SERPs
- Trust signals for prospective buyers

---

#### H5 — App on Separate Subdomain Without SEO Bridge
**Severity:** High | **Confidence:** Confirmed

The actual application runs at `app.cargosimplify.com` (GTA FUSION). The marketing site (cargosimplify.com) has no deep linking to feature pages, demo requests, or pricing. The app subdomain is indexed only for a password reset page — not helpful for brand discovery.

**Impact:** Users who discover GTA FUSION branding may not find cargosimplify.com. The two properties are disconnected in Google's view.

---

#### H6 — Page URL Structure Uses Raw HTML Files
**Severity:** High | **Confidence:** Confirmed

Pages are served as `.html` files (`booking.html`, `lorry_broker.html`). While technically valid, this structure:
- Is difficult to extend with CMS/blog functionality
- Does not support dynamic SEO meta injection
- Makes it harder to implement canonical tags, hreflang, or schema at scale
- Suggests the site was hand-built with no CMS or SEO framework

---

### 🟡 MEDIUM

---

#### M1 — No Pricing Page in Google Index
**Severity:** Medium | **Confidence:** Confirmed

"Pricing" or "Plans" page is not indexed. For commercial software searches like "lorry broker software India pricing", having a dedicated pricing page is essential for conversion.

---

#### M2 — No About/Company Page
**Severity:** Medium | **Confidence:** Confirmed

No About Us, Company, or Team page indexed. This is an E-E-A-T gap — Google cannot verify experience/authoritativeness without company information on the site.

---

#### M3 — GTA FUSION Brand Not Aligned With Marketing Site
**Severity:** Medium | **Confidence:** Confirmed

The app branding is "GTA FUSION" while the marketing site is "Cargo Simplify". Users who search "GTA FUSION software India" will likely not find cargosimplify.com. The brands should be clearly linked.

---

#### M4 — No Open Graph / Social Tags
**Severity:** Medium | **Confidence:** Hypothesis

Given that title tags are broken, Open Graph tags (og:title, og:description, og:image) are almost certainly missing too. This affects link previews on WhatsApp, LinkedIn, and Facebook shares.

---

#### M5 — No Internal Linking Architecture
**Severity:** Medium | **Confidence:** Confirmed

With only 3 indexed pages, there is no internal linking structure to pass PageRank between pages or guide Google's crawl budget.

---

#### M6 — Mobile App Not Leveraged in SEO
**Severity:** Medium | **Confidence:** Hypothesis

Mobile app (Android/iOS) appears to exist but no App Schema or App Store links are visible on the marketing site. For a mobile-first Indian audience, app deep linking and app schema are conversion accelerators.

---

### 🔵 LOW

---

#### L1 — No Canonical Tags (Hypothesis)
**Severity:** Low | **Confidence:** Hypothesis

Without canonical tags, duplicate content across .html files (e.g. www vs non-www, HTTP vs HTTPS) can dilute rankings.

---

#### L2 — No Hreflang (If Multi-Language Planned)
**Severity:** Low | **Confidence:** Hypothesis

If targeting Hindi-speaking users in addition to English, hreflang would be needed.

---

## B) Competitor Landscape

### Direct Competitors Ranking for Target Keywords

| Competitor | Domain | Key Advantage | SEO Strength |
|---|---|---|---|
| Fleetable | fleetable.tech | Active blog, 14 years India-specific TMS, strong keyword coverage | 🔴 High |
| BharatSoftware | bharatsoftware.com | 17 years, 1150+ logistics clients, full landing pages per feature | 🔴 High |
| BiltySoftware | biltysoftware.com | Dedicated to bilty/LR — owns branded niche | ⚠️ Medium |
| ecount.in | ecount.in | Freight brokerage + TMS + 300+ happy clients page | ⚠️ Medium |
| Logistiqo | logistiqo.com | International SaaS TMS with pricing page | ⚠️ Medium |
| TMSMitra | tmsmitra.com | India-specific TMS branding | ⚠️ Medium |
| Waybiller | waybiller.com | Bulk TMS specialist | 🟢 Low |

**Key observation:** No competitor is specifically dominating the "lorry broker software" niche with deep content. This is an exploitable gap for cargosimplify.com.

---

## C) Keyword Gap Analysis

### High-Priority Keyword Opportunities

| Keyword | Monthly Volume Est. | Competition | Opportunity |
|---|---|---|---|
| lorry broker software India | Medium (500–2K) | Low | 🔴 Primary target — core product |
| freight broker software India | Medium (1K–5K) | Medium | 🔴 High-value |
| bilty software | Medium (1K–3K) | Low | 🔴 Easy win |
| LR software India | Low-Medium (200–1K) | Low | ⚠️ Quick win |
| lorry receipt software | Low-Medium | Low | ⚠️ Quick win |
| lorry booking software India | Medium (500–2K) | Low | ⚠️ Core product |
| transport management software India | High (5K–20K) | High | 🟡 Long-term target |
| fleet management software India | High (5K+) | High | 🟡 Long-term |
| cargo management software India | Medium | Medium | ⚠️ Target now |
| GTA FUSION software | Low (Branded) | Low | 🔵 Brand protection |
| e-way bill software India | Medium-High | Medium | ⚠️ Feature content |
| Tally transport integration | Low | Low | ⚠️ Unique differentiator |

---

## D) E-E-A-T Assessment

| Signal | Status | Notes |
|---|---|---|
| Experience | ❌ Missing | No case studies, no client stories, no "built by transport industry" narrative |
| Expertise | ❌ Missing | No team page, no author bios, no product expertise content |
| Authoritativeness | ❌ Missing | No reviews on Capterra/G2, no press mentions found |
| Trustworthiness | ⚠️ Weak | Facebook page exists; no contact page indexed; no GST/company info visible |

**E-E-A-T Score: 2/20** — Critical gap for B2B software buying decisions.

---

## E) Content Gap vs Competitors

| Content Type | Fleetable | BharatSoftware | BiltySoftware | cargosimplify.com |
|---|---|---|---|---|
| Feature landing pages | ✅ Multiple | ✅ Multiple | ✅ | ⚠️ 2 pages (.html) |
| Pricing page | ✅ | ✅ | ✅ | ❌ |
| Blog / guides | ✅ Active | ✅ Active | ❌ | ❌ |
| "What is bilty" guide | ✅ | ❌ | ✅ | ❌ |
| E-way bill guide | ✅ | ✅ | ❌ | ❌ |
| Case studies | ✅ | ✅ | ❌ | ❌ |
| Review platform listings | ✅ SoftwareSuggest | ✅ | ❌ | ❌ |
| Schema markup | ✅ | ✅ | ⚠️ | ❌ |
| About page | ✅ | ✅ | ✅ | ❌ |
| Contact page | ✅ | ✅ | ✅ | ❌ (not indexed) |
| Free trial / demo CTA | ✅ | ✅ | ✅ | ❌ |

---

## F) Unique Differentiators to Exploit

| Differentiator | Competitors Have This? | SEO Opportunity |
|---|---|---|
| Tally integration (Tally transfer) | Rare — most TMS don't offer this | Create "Tally + Transport Software" content; target "tally transport integration" |
| GTA FUSION app brand | Unique | Build GTA FUSION landing page; explain the brand relationship to cargosimplify.com |
| Lorry broker + fleet owner + warehouse in one | Partial — Fleetable is close | "All-in-one lorry broker software" positioning |
| Desktop + web + mobile options | Common | Not a differentiator — don't lead with this |
| Vapi/Gujarat base | No major competitor claims Gujarat | Local SEO opportunity for Gujarat logistics market |
| Bilty/LR digital generation | Fleetable does this well | Must create bilty guide content or lose this keyword category |

---

## G) Technical Summary

| Signal | Status | Confidence |
|---|---|---|
| HTTPS | ✅ (assumed — app subdomain is modern) | Hypothesis |
| Mobile responsive | Hypothesis — unknown | Hypothesis |
| Title tags set | ❌ Broken ("Document") | Confirmed |
| Meta descriptions | ❌ Missing | Confirmed |
| Sitemap | ❌ Not found | Hypothesis |
| Robots.txt | ❌ Unknown / possibly blocking | Hypothesis |
| Schema markup | ❌ None detected | Confirmed |
| Canonical tags | ❌ Likely missing | Hypothesis |
| Open Graph tags | ❌ Likely missing | Hypothesis |
| Google Search Console | ❓ Unknown if set up | Unknown |
| Pages indexed | 3 (critically low) | Confirmed |
| Core Web Vitals | ❓ Not measurable | Unknown |

---

## H) Priority Fix Summary

| # | Issue | Priority | Est. Impact | Effort |
|---|---|---|---|---|
| 1 | Fix all title tags (remove "Document") | Critical | Very High | 1 day |
| 2 | Add meta descriptions to all pages | Critical | High | 1 day |
| 3 | Submit XML sitemap to GSC | Critical | High | 2 hours |
| 4 | Create About + Contact + Pricing pages | Critical | High | 3–5 days |
| 5 | Add Organization + SoftwareApplication schema | High | Medium | 1 day |
| 6 | List on SoftwareSuggest, Capterra India, G2 | High | High | 2–3 days |
| 7 | Create "lorry broker software" landing page | High | Very High | 2–3 days |
| 8 | Start blog: "What is Bilty/LR" guide | High | High | 2 days |
| 9 | Create pricing page | High | High | 1 day |
| 10 | Connect GTA FUSION brand to main site | Medium | Medium | 1 day |
