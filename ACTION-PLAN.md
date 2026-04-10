# SEO Action Plan — cargosimplify.com
**Date:** 2026-04-10
**Overall Score:** 16/100 (Critical — foundational SEO is broken)
**Priority:** Fix technical foundation first, then build content

---

## PHASE 1 — Emergency Technical Fixes (Week 1)
**Goal:** Stop Google from seeing a blank/broken site

---

### Action 1 — Fix All `<title>` Tags (URGENT — Do This First)
**Priority:** Critical | **Effort:** 2–4 hours | **Impact:** Very High

Every page on cargosimplify.com currently shows "Document" as its `<title>` in Google search results. This is a fatal SEO error.

**Root cause:** HTML pages were likely built from a template that left `<title>Document</title>` unfilled. Fix every `.html` file.

**Title tag formulas:**

| Page | Title Tag (max 60 chars) |
|---|---|
| Homepage | `Cargo Simplify — Lorry Broker & Transport Software India` |
| booking.html | `Lorry Booking Software India — Cargo Simplify` |
| lorry_broker.html | `Lorry Broker Software India — Cargo Simplify` |
| pricing (create new) | `Pricing — Cargo Simplify Transport Software` |
| about (create new) | `About Cargo Simplify — Transport Software Vapi India` |
| contact (create new) | `Contact Cargo Simplify — Demo & Support` |
| blog/what-is-bilty | `What is Bilty (Lorry Receipt)? Complete Guide 2026` |

**Implementation (for static HTML files):**
```html
<!-- BEFORE (broken) -->
<title>Document</title>

<!-- AFTER (homepage) -->
<title>Cargo Simplify — Lorry Broker &amp; Transport Software India</title>
```

---

### Action 2 — Add Meta Descriptions to All Pages
**Priority:** Critical | **Effort:** 2 hours | **Impact:** High

No meta descriptions detected on any page. Without them, Google auto-generates snippets from body text (often nonsensical).

**Meta descriptions per page:**

| Page | Meta Description (150–160 chars) |
|---|---|
| Homepage | `Cargo Simplify is India's lorry broker and transport management software. Manage bilty, bookings, fleet, and accounts in one platform. Desktop + Web + Mobile.` (157 chars) |
| booking.html | `Book lorries and manage cargo transport bookings with Cargo Simplify. Automate bilty generation, track shipments, and manage freight from a single dashboard.` (157 chars) |
| lorry_broker.html | `Lorry broker software for Indian transporters. Manage broker commissions, shipment coordination, billing, and fleet utilization with Cargo Simplify.` (150 chars) |

```html
<meta name="description" content="Cargo Simplify is India's lorry broker and transport management software. Manage bilty, bookings, fleet, and accounts in one platform. Desktop + Web + Mobile.">
```

---

### Action 3 — Create and Submit XML Sitemap
**Priority:** Critical | **Effort:** 2 hours | **Impact:** High

**Step 1:** Create `sitemap.xml` at `https://cargosimplify.com/sitemap.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://cargosimplify.com/</loc>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
    <lastmod>2026-04-10</lastmod>
  </url>
  <url>
    <loc>https://cargosimplify.com/booking.html</loc>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://cargosimplify.com/lorry_broker.html</loc>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
</urlset>
```

**Step 2:** Add to robots.txt:
```
User-agent: *
Allow: /
Sitemap: https://cargosimplify.com/sitemap.xml
```

**Step 3:** Submit sitemap URL in Google Search Console → Sitemaps.

---

### Action 4 — Add Canonical Tags and Open Graph to All Pages
**Priority:** Critical | **Effort:** 2 hours | **Impact:** Medium

Add to every page's `<head>`:

```html
<!-- Canonical (prevents duplicate content issues) -->
<link rel="canonical" href="https://cargosimplify.com/">

<!-- Open Graph (for WhatsApp/LinkedIn link previews) -->
<meta property="og:type" content="website">
<meta property="og:title" content="Cargo Simplify — Lorry Broker &amp; Transport Software India">
<meta property="og:description" content="India's lorry broker and transport management software. Manage bilty, bookings, fleet, and accounts in one platform.">
<meta property="og:url" content="https://cargosimplify.com/">
<meta property="og:image" content="https://cargosimplify.com/images/og-banner.jpg">
<meta property="og:site_name" content="Cargo Simplify">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Cargo Simplify — Lorry Broker &amp; Transport Software India">
<meta name="twitter:description" content="India's lorry broker and transport management software.">
```

---

## PHASE 2 — Content Foundation (Weeks 2–3)
**Goal:** Give Google crawlable, keyword-targeted pages to index

---

### Action 5 — Create Missing Core Pages
**Priority:** Critical | **Effort:** 3–5 days | **Impact:** Very High

The following pages are missing entirely from the indexed site:

#### 5A — About / Company Page
**URL:** `/about.html` or `/about/`
**Target keyword:** `cargo simplify software India`, branded searches

**Content structure:**
```
H1: About Cargo Simplify — Transport Software Built for India

Section 1: Our Story (100 words)
  - Founded in Vapi, Gujarat
  - Built for lorry brokers, fleet owners, and cargo handlers
  - Desktop + web + mobile platform

Section 2: What We Do (100 words)
  - Cargo booking and bilty management
  - Lorry broker coordination
  - Fleet tracking
  - Tally accounting integration

Section 3: Who Uses Cargo Simplify (100 words)
  - Fleet owners
  - Lorry brokers / commission agents
  - Warehouse managers
  - Cargo handlers

CTA: [Request a Demo] | [WhatsApp Us]
```

#### 5B — Pricing Page
**URL:** `/pricing.html`
**Target keyword:** `cargo simplify pricing`, `lorry broker software price India`

**Content structure:**
```
H1: Cargo Simplify Pricing — Transparent Plans for Every Business

Pricing Table:
| Plan | Features | Price |
| Desktop | Single-user desktop app, LR/bilty, basic accounting | ₹[X]/year |
| Web | Multi-user cloud access, all desktop features + mobile | ₹[X]/user/month |
| Enterprise | Unlimited users, custom integration, priority support | Contact |

FAQs section (important for conversions):
- Is there a free trial?
- Can I migrate from another software?
- Does it integrate with Tally?
- How is data backed up?

CTA: [Start Free Trial / Get Demo] | [WhatsApp: +91-XXXXXXXXXX]
```

#### 5C — Contact Page
**URL:** `/contact.html`
**Target keyword:** `cargo simplify contact`, `lorry software demo India`

```
H1: Contact Cargo Simplify

Details to include:
- Phone / WhatsApp number
- Email address
- Address: Vapi, Gujarat, India
- Google Maps embed
- Contact form (Name, Company, Phone, Query type)
- WhatsApp direct link
```

---

### Action 6 — Add JSON-LD Schema Markup
**Priority:** High | **Effort:** 1 day | **Impact:** High

Add the following schemas to the site. All via `<script type="application/ld+json">` in `<head>`.

#### 6A — Organization + WebSite Schema (Homepage)
```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://cargosimplify.com/#organization",
      "name": "Cargo Simplify",
      "url": "https://cargosimplify.com/",
      "logo": {
        "@type": "ImageObject",
        "url": "https://cargosimplify.com/images/logo.png"
      },
      "description": "India's lorry broker and transport management software for fleet owners, brokers, and cargo handlers.",
      "address": {
        "@type": "PostalAddress",
        "addressLocality": "Vapi",
        "addressRegion": "Gujarat",
        "addressCountry": "IN"
      },
      "contactPoint": {
        "@type": "ContactPoint",
        "contactType": "customer support",
        "availableLanguage": ["English", "Hindi", "Gujarati"]
      },
      "sameAs": [
        "https://www.facebook.com/BestLogisticsSoftware/"
      ]
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
    }
  ]
}
```

#### 6B — SoftwareApplication Schema (Homepage + Product Pages)
```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "Cargo Simplify",
  "alternateName": "GTA FUSION",
  "applicationCategory": "BusinessApplication",
  "applicationSubCategory": "Transport Management Software",
  "operatingSystem": "Windows, Web, Android, iOS",
  "url": "https://cargosimplify.com/",
  "description": "Lorry broker and transport management software for Indian fleet owners, brokers, and cargo handlers. Includes bilty/LR management, booking, fleet tracking, and Tally integration.",
  "offers": {
    "@type": "Offer",
    "priceCurrency": "INR",
    "price": "Contact for pricing",
    "seller": {
      "@type": "Organization",
      "name": "Cargo Simplify"
    }
  },
  "featureList": [
    "Lorry broker management",
    "Transport booking",
    "Bilty / Lorry Receipt (LR) generation",
    "Fleet tracking",
    "Tally accounting integration",
    "E-way bill compliance",
    "Mobile app (Android and iOS)"
  ],
  "softwareVersion": "Current",
  "inLanguage": ["en", "hi"],
  "availableOnDevice": ["Desktop", "Mobile", "Tablet"],
  "publisher": {
    "@type": "Organization",
    "name": "Cargo Simplify",
    "url": "https://cargosimplify.com/"
  }
}
```

#### 6C — LocalBusiness Schema (About / Contact Page)
```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Cargo Simplify",
  "description": "Lorry broker and transport management software — Vapi, Gujarat.",
  "url": "https://cargosimplify.com/",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Vapi",
    "addressRegion": "Gujarat",
    "addressCountry": "IN"
  },
  "areaServed": ["Gujarat", "Maharashtra", "Rajasthan", "India"],
  "serviceType": "Transport Management Software"
}
```

---

## PHASE 3 — Content Marketing & Keyword Capture (Weeks 3–6)
**Goal:** Rank for target keywords; build topical authority

---

### Action 7 — Create "Lorry Broker Software" Core Landing Page
**URL:** `/lorry-broker-software/` (or convert lorry_broker.html with proper content)
**Target keyword:** `lorry broker software India` · `freight broker software India`
**Word count:** 1,500+
**Priority:** Critical — this is the #1 product keyword

#### Full Page Blueprint

**Title:** `Lorry Broker Software India — Cargo Simplify`
**Meta description:** `Manage lorry bookings, broker commissions, bilty/LR generation, and fleet coordination from one platform. Cargo Simplify is India's lorry broker software. Free demo available.` (176 chars — trim to 160)

**H1:** Lorry Broker Software for Indian Transporters

**Introduction (100 words):**
> Managing lorry brokerage manually — phone calls, paper registers, WhatsApp threads — leads to missed trips, calculation errors, and delayed payments. Cargo Simplify digitizes your entire lorry broker operation: from receiving cargo bookings to assigning lorries, generating bilty/LR documents, calculating broker commissions, and final settlement with fleet owners.

---

**Feature Sections:**

**H2: Cargo Booking Management**
- Accept bookings from shippers by phone, WhatsApp, or web form
- Auto-assign appropriate lorry based on route and capacity
- Generate confirmation slips instantly

**H2: Bilty / LR Generation**
- Digital bilty (Lorry Receipt) with all compliance fields
- GST-compliant format
- Print or share via WhatsApp/email
- Auto-number series management

**H2: Broker Commission Tracking**
- Automatically calculate commission per trip
- Track pending payments from shippers
- Track payments owed to fleet owners
- Monthly/quarterly commission reports

**H2: E-Way Bill Integration**
- Generate e-way bills directly from booking
- One-click upload to GST portal
- Avoid compliance penalties

**H2: Tally Accounting Integration**
- Transfer all transport transactions to Tally
- No duplicate data entry
- GST ledgers auto-populated
- Works with Tally Prime and TallyERP 9

**H2: Fleet Owner Coordination**
- Maintain lorry/truck database
- Track vehicle availability
- Driver assignment per trip
- Vehicle maintenance reminders

---

**Comparison Table:**

| Feature | Cargo Simplify | Manual Register | Basic Excel |
|---|---|---|---|
| Bilty/LR generation | ✅ Digital, GST-compliant | ❌ Paper | ⚠️ Manual |
| Commission calculation | ✅ Automated | ❌ Manual | ⚠️ Formula errors |
| E-way bill | ✅ One-click | ❌ Separate login | ❌ |
| Tally transfer | ✅ Direct | ❌ Manual entry | ❌ |
| Multi-user (web) | ✅ | N/A | ❌ |
| Mobile access | ✅ Android/iOS | N/A | ❌ |

---

**CTA:**
> "See how Cargo Simplify replaces your register, WhatsApp threads, and Excel sheets with one platform. [Request a Free Demo →](/contact.html)"

**Schema for this page:**
```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "Cargo Simplify — Lorry Broker Software",
  "applicationCategory": "BusinessApplication",
  "description": "Digital lorry broker software for Indian transporters. Manage bilty, commissions, e-way bills, and Tally integration.",
  "url": "https://cargosimplify.com/lorry-broker-software/",
  "offers": {
    "@type": "Offer",
    "priceCurrency": "INR",
    "seller": { "@type": "Organization", "name": "Cargo Simplify" }
  }
}
```

---

### Action 8 — Blog Post: "What is Bilty (Lorry Receipt)? Complete Guide 2026"
**URL:** `/blog/what-is-bilty-lorry-receipt/`
**Target keyword:** `what is bilty` · `bilty software` · `lorry receipt software India`
**Word count:** 1,200+
**Priority:** High — Fleetable ranks for this; cargosimplify.com can compete

#### Blueprint

**Title:** `What is Bilty (Lorry Receipt)? Complete Guide for Indian Transporters 2026`
**Meta description:** `Bilty (Lorry Receipt / LR) is the key transport document in India. Learn what a bilty contains, how to generate it digitally, and how software automates the process.` (170 chars — trim)

**H1:** What is Bilty (Lorry Receipt) — Guide for Indian Transporters

**Sections:**
```
H2: What is a Bilty?
  - Definition: Bilty = Lorry Receipt (LR) = consignment note
  - Legal document issued by transporter to shipper
  - Proves transporter has accepted goods for delivery
  - Required for GST e-way bill compliance

H2: What Information Does a Bilty Contain?
  - Consignor name and address
  - Consignee name and address
  - Description of goods
  - Weight / number of packages
  - Freight amount and payment terms (to-pay / paid / to-be-billed)
  - Lorry number and driver details
  - Date and LR number
  - Transporter signature

H2: Types of Bilty in India
  - Single-copy vs carbon copy bilty
  - GST-compliant bilty format
  - E-way bill linked bilty

H2: Why Transporters Are Moving to Digital Bilty
  - Paper bilty lost = legal disputes
  - Manual numbering = errors
  - WhatsApp/email sharing
  - GST portal integration

H2: How to Generate Bilty Using Software
  - Enter booking details once
  - Auto-generate GST-compliant LR
  - Share via WhatsApp or print
  - Link to e-way bill generation

H2: Bilty vs Lorry Receipt vs Consignment Note
  - All the same document; regional name variations

CTA: "Cargo Simplify generates GST-compliant bilties in seconds. [See Demo →](/contact.html)"
```

**Internal links:** → /lorry-broker-software/ → /booking.html → /contact.html

---

### Action 9 — Blog Post: "Transport Management Software vs Excel: Why Indian Transporters Are Switching"
**URL:** `/blog/transport-software-vs-excel-india/`
**Target keyword:** `transport management software India` · `lorry booking software`
**Word count:** 1,000+

#### Blueprint

**Title:** `Transport Management Software vs Excel: Why Indian Transporters Are Switching (2026)`
**Meta description:** `Still tracking lorry bookings in Excel? See why 1,000s of Indian transporters are switching to dedicated transport management software for bilty, e-way bill, and GST compliance.`

**Sections:**
```
H2: The Problem with Excel for Transport Management
  - No automatic bilty number series
  - No GST/e-way bill integration
  - Data scattered across multiple files
  - Can't share with drivers/clients in real time
  - No audit trail

H2: What Transport Management Software Does Differently
  - Feature-by-feature comparison table
  - [Comparison table: Excel vs TMS vs Cargo Simplify]

H2: Real Scenarios Where Software Wins
  - Example 1: Missed e-way bill = ₹10,000 penalty avoided
  - Example 2: Commission dispute resolved with digital record
  - Example 3: Shipper requests copy of bilty from 6 months ago — found in 10 seconds

H2: How to Switch from Excel to Cargo Simplify
  - Data migration support
  - Training
  - Desktop + web + mobile access

CTA: [Book a Free Demo] | [WhatsApp Us]
```

---

### Action 10 — "Transport Booking Software India" Landing Page
**URL:** `/transport-booking-software/` (or improve booking.html)
**Target keyword:** `transport booking software India` · `lorry booking system`
**Word count:** 1,000+

#### Blueprint

**H1:** Transport Booking Software for Indian Fleet Owners & Brokers

**Sections:**
```
H2: One Platform to Manage All Your Lorry Bookings
  - Accept booking from shippers
  - Assign lorry and driver
  - Track trip in real time
  - Generate bilty + e-way bill on booking

H2: Who Uses Cargo Simplify Booking?
  - Lorry brokers / commission agents
  - Fleet owners with 5–50 trucks
  - Logistics companies

H2: Key Booking Features
  - Multi-party booking (shipper → broker → carrier)
  - Rate management
  - Auto-bilty generation
  - WhatsApp sharing of booking confirmation

CTA: [Start Free Trial] or [Book a Demo]
```

---

## PHASE 4 — Off-Page & Local SEO (Weeks 4–8)
**Goal:** Build domain authority and trust signals

---

### Action 11 — List on Indian Software Directories
**Priority:** High | **Effort:** 3–5 days | **Impact:** High (backlinks + review acquisition)

| Platform | URL to Submit | Priority |
|---|---|---|
| SoftwareSuggest | softwaresuggest.com | 🔴 First |
| Capterra India | capterra.in | 🔴 First |
| TechJockey | techjockey.com | 🔴 First |
| GetApp India | getapp.in | ⚠️ Second |
| G2 | g2.com | ⚠️ Second |
| SoftwareWorld | softwareworld.co | 🟢 Third |
| Compare Camp | comparecamp.com | 🟢 Third |

**Listing profile checklist:**
- [ ] Company name: Cargo Simplify
- [ ] Category: Transport Management Software / Freight Broker Software
- [ ] Description: 300+ words covering bilty, lorry broker, fleet, Tally integration
- [ ] Screenshots: 3–5 screenshots of the UI
- [ ] Pricing: indicate pricing model (subscription/one-time)
- [ ] Website: https://cargosimplify.com
- [ ] Contact email and phone
- [ ] Encourage existing customers to leave reviews

---

### Action 12 — Google Business Profile
**Priority:** High | **Effort:** 1 day | **Impact:** High (local SEO)

Create/claim Google Business Profile for "Cargo Simplify" in Vapi, Gujarat.

**Profile details:**
- Business name: Cargo Simplify
- Category: Software Company / Transportation Software
- Address: Vapi, Gujarat, India
- Phone: [Add number]
- Website: https://cargosimplify.com
- Description: "India's lorry broker and transport management software. Manage bilty, freight bookings, fleet coordination, and Tally accounting from one platform."
- Photos: Office, product screenshots, logo

---

### Action 13 — GTA FUSION Brand Alignment Page
**URL:** `/gta-fusion/`
**Priority:** Medium | **Effort:** 1 day

**Purpose:** Users who search "GTA FUSION software India" need to find cargosimplify.com. Create a bridge page explaining the relationship.

**Content:**
```
H1: GTA FUSION — Powered by Cargo Simplify

GTA FUSION is the web and mobile application platform behind Cargo Simplify. 
If you're accessing your transport management system at app.cargosimplify.com,
you're using GTA FUSION.

[Sections: GTA FUSION features / Login / Support / Contact]
```

---

## KPI Targets (Track Monthly via GSC)

| Page / Target | Primary Keyword | 3-Month Goal |
|---|---|---|
| Homepage | "cargo simplify" (branded) | Top 1 |
| /lorry-broker-software/ | "lorry broker software India" | Top 10 |
| /blog/what-is-bilty-lorry-receipt/ | "what is bilty" | Top 5 |
| /transport-booking-software/ | "lorry booking software" | Top 10 |
| /blog/transport-software-vs-excel-india/ | "transport management software India" | Top 20 |

---

## Estimated Ranking Timelines

| Page Type | Timeline to First Ranking | Notes |
|---|---|---|
| Fix title tags → Google re-crawl | 1–2 weeks | Near-instant after GSC resubmit |
| "what is bilty" guide | 3–5 weeks | Low competition; educational intent |
| "lorry broker software India" | 4–8 weeks | Low-medium competition |
| "transport management software India" | 3–6 months | High competition |

---

## Technical Debt Backlog (Lower Priority)

| Task | Priority |
|---|---|
| Migrate from static HTML to CMS (WordPress or similar) for blog support | Medium |
| Implement HTTPS across all pages (verify) | High |
| Add `<html lang="en">` to all pages | Low |
| Add `width` and `height` attributes to all `<img>` tags | Low |
| Add `loading="lazy"` to below-fold images | Low |
| Set up Google Search Console | Critical (if not already) |
| Set up Google Analytics 4 | High |
| Set up hreflang if Hindi content is added | Low |
