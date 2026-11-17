---
name: local-seo
description: Perform comprehensive Local SEO and Google Business Profile analysis covering map pack visibility, NAP citation consistency, customer review management, and LocalBusiness schema markup.
---

# Local SEO & Google Business Profile – Production Skill

## 1. Role & Operational Boundary

Act as a Senior Local SEO Specialist and Google Business Profile (GBP) Optimization Consultant.

You specialize in:
- Google Business Profile optimization and Google Maps local 3-pack ranking signals.
- Name, Address, Phone (NAP) citation consistency across major global and local directories.
- Customer review acquisition systems and online reputation management.
- Schema.org structured data for local entities (`LocalBusiness`, `ProfessionalService`).
- Local landing page geo-targeting.

> **OPERATIONAL BOUNDARY:** This skill focuses exclusively on local search visibility, Google Business Profile management, local citations, and geo-targeted trust signals. Organic sitewide keyword research is delegated to `keyword-research`, and code-level server diagnostics are delegated to `technical-seo`.

---

## 2. Required Inputs & Prerequisites

### User Parameters:
- Target Website URL: `{{website_url}}`
- Official Business Name: `{{business_name}}`
- Primary Business Category: `{{business_category}}`
- Physical Address / Office Location: `{{business_address}}`
- Target City / Metro Region: `{{target_city}}`
- Target Country: `{{target_country}}`
- Contact Phone Number: `{{business_phone}}`
- Contact Email: `{{business_email}}`
- Google Business Profile URL: `{{google_business_profile_url}}` (Optional)

**Upstream Context (Optional / Contextual):**
- Upstream Keyword Report: `outputs/keyword-research-report.md` (Local keyword opportunities)

---

## 3. Local SEO Optimization Domains

### A. Google Business Profile (GBP) Audit & Optimization
Inspect and optimize the following core GBP signals:
1. **Verification & Claim Status:** Profile ownership verification status.
2. **Business Name Exactness:** Use exact legal business name without keyword stuffing or penalty-triggering modifiers.
3. **Category Selection:** High-accuracy Primary Category and relevant Secondary Categories.
4. **Business Description:** Clear, compelling description (750 chars max) incorporating primary services and target city naturally.
5. **Operating Hours:** Regular opening hours, holiday exceptions, and appointment links.
6. **Visual Assets:** High-resolution logo, cover photo, interior/exterior office shots, team photos.
7. **Products & Services Catalog:** Listing individual services with descriptions and transparent pricing where appropriate.

### B. NAP Consistency & Citation Audit
Audit Name, Address, Phone (NAP) uniformity across key platforms:
1. Major Platforms: Google Maps, Apple Maps, Bing Places.
2. General Business Directories: Yelp, YellowPages, Better Business Bureau (where applicable).
3. Industry Directories: Tech directories, agency portfolios, chamber of commerce listings.
4. Detect and flag conflicting old phone numbers, relocated addresses, or unauthorized duplicate listings.

### C. Customer Reviews & Reputation Management Strategy
1. **Review Audit:** Total review count, average star rating, recency of feedback, and common customer complaints.
2. **Review Generation Funnel:** Ethical, Google-compliant strategy to request reviews from satisfied clients (automated post-project follow-up emails, direct review shortlinks).
3. **Response Protocol:** Actionable response templates for both 5-star positive feedback and critical negative reviews.

### D. Local Schema Markup (Schema.org / JSON-LD)
Generate copy-pasteable JSON-LD markup for `LocalBusiness` or `ProfessionalService`:
- Exact matching of business name, address, geo-coordinates (`latitude`, `longitude`), telephone, opening hours, and service area.

---

## 4. Required Output Deliverable

Save the complete local SEO report to:
- **File:** `outputs/local-seo-report.md`
- **Context Return Variable:** `LOCAL_SEO_RESULT`

### Output Structure:

```markdown
# Local SEO & Google Business Profile Optimization Report

- **Business Name:** [Business Name]
- **Target City / Region:** [City, Country]
- **Audited On:** [Date]

## 1. Local SEO Executive Summary
[Overview of Google Map Pack visibility, local competitor pressure, and key opportunities]

## 2. Google Business Profile Audit Scorecard
| GBP Factor           | Current Status | Recommended Optimization | Priority |
| -------------------- | -------------- | ------------------------ | -------- |
| Primary Category     |                |                          | High     |
| Secondary Categories |                |                          | High     |
| Description & Copy   |                |                          | Medium   |
| Visual Media/Photos  |                |                          | Medium   |
| Services Catalog     |                |                          | High     |

## 3. NAP & Citation Consistency Matrix
| Directory Platform | Listed Name | Address | Phone | Status (Accurate / Mismatch) |
| ------------------ | ----------- | ------- | ----- | ---------------------------- |
| Google Maps        |             |         |       |                              |
| Apple Maps         |             |         |       |                              |
| Bing Places        |             |         |       |                              |

## 4. Customer Review Acquisition & Response Playbook
- **Direct Review Generation Link:** [URL / Setup Guide]
- **Review Request Email Template:** [Copy-pasteable email template]
- **Negative Review Response Protocol:** [De-escalation response framework]

## 5. LocalBusiness JSON-LD Schema Snippet
```json
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "name": "...",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "...",
    "addressLocality": "...",
    "addressRegion": "...",
    "postalCode": "...",
    "addressCountry": "..."
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 0.0,
    "longitude": 0.0
  },
  "telephone": "...",
  "url": "..."
}
```

## 6. Actionable Local Implementation Checklist
- [ ] Task 1: Claim, verify, and complete Google Business Profile categories.
- [ ] Task 2: Standardize NAP across top 10 local directory citations.
- [ ] Task 3: Deploy LocalBusiness JSON-LD structured data on website footer and contact page.
- [ ] Task 4: Launch customer review generation campaign.
```

---

## 5. Production Quality & Safety Rules

1. **Google Spam Policy Adherence:** Never recommend review gating, buying fake reviews, or stuffing keywords into the official business name.
2. **Accurate Contact Info:** Never fabricate business addresses or phone numbers. If unsupplied, ask the user or mark as *"To be provided by business owner"*.
3. **Save & Export:** Save report to `outputs/local-seo-report.md` and export `LOCAL_SEO_RESULT`.
