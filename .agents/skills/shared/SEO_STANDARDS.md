# Standardized SEO Technical & On-Page Quality Standards

This document establishes the universal quality standards, technical thresholds, and compliance baselines for all skills in the SEO ecosystem.

---

## 1. Compliance Baseline & White-Hat Policy

- **Google Search Essentials Adherence:** All recommendations must strictly adhere to Google Search Essentials and spam policies.
- **Prohibited Black-Hat Tactics:**
  - No private blog networks (PBNs), automated link schemes, or paid un-attributed links (`rel="sponsored"` mandatory for paid).
  - No doorway pages, hidden text, keyword stuffing, or cloaking.
  - No scraped or unedited low-effort AI regurgitation lacking Information Gain.
- **Zero Fabrication Mandate:** Never fabricate or guess PageSpeed scores, ranking positions, search volumes, or backlink quantities. Any unverified metric must be documented with: `[Public observational search data; requires Google Search Console verification]`.

---

## 2. On-Page & Metadata Quality Baselines

| Element | Specification / Threshold | Best Practice |
|---|---|---|
| **Title Tag** | 50–60 characters (≤ 580px width) | Primary Keyword + Secondary Keyword \| Brand Name. Front-load intent. |
| **Meta Description** | 140–160 characters (≤ 960px width) | Compelling summary with explicit value proposition and Call to Action. |
| **H1 Heading** | Exactly 1 unique H1 per indexable page | Clear match to page search intent; aligned with Title Tag. |
| **Heading Hierarchy** | Logical nesting (`H1` ➔ `H2` ➔ `H3`) | No skipping levels (e.g. `H1` directly to `H3`). Clear topical modularity. |
| **Canonical Tag** | Self-referencing on canonical URL | Fully qualified absolute URL with correct protocol (`https://`) and no trailing slash inconsistency. |
| **Open Graph & Twitter** | Complete social meta tags | `og:title`, `og:description`, `og:image`, `og:url`, `og:type`, `twitter:card`. |

---

## 3. Core Web Vitals (CWV) Standards

| Metric | Good (Passing) | Needs Improvement | Poor |
|---|---|---|---|
| **Largest Contentful Paint (LCP)** | ≤ 2.5 seconds | 2.5s – 4.0s | > 4.0 seconds |
| **Interaction to Next Paint (INP)** | ≤ 200 ms | 200 ms – 500 ms | > 500 ms |
| **Cumulative Layout Shift (CLS)** | ≤ 0.1 | 0.1 – 0.25 | > 0.25 |
| **First Input Delay (FID)** *(Deprecated)* | Replaced by INP in March 2024. |
| **Time to First Byte (TTFB)** | ≤ 800 ms (Server response) | 800 ms – 1800 ms | > 1800 ms |

---

## 4. Crawlability & Indexing Standards

- **Robots.txt:** Clean, valid syntax, clearly pointing to `Sitemap: {{WEBSITE_URL}}/sitemap.xml`. Never disallow critical CSS/JS assets needed for rendering.
- **XML Sitemap:** UTF-8, compliant with sitemaps.org protocol, listing only 200 OK indexable canonical URLs. Zero redirects or 404s in sitemaps.
- **Status Codes:** Target 200 OK for canonical pages; 301 Permanent Redirects for migrated URLs; zero internal 404 loops or redirect chains (> 1 hop).
- **Mobile-First Indexing:** Responsive viewport meta tag mandatory; identical content and metadata served to mobile and desktop user agents.

---

## 5. Structured Data & Schema Standards

- **Format:** Pure JSON-LD embedded within `<script type="application/ld+json">`.
- **Core Schemas:**
  - `Organization` or `LocalBusiness`: Name, URL, Logo, SameAs profiles.
  - `WebSite`: Name, URL, PotentialAction (SearchAction).
  - `Service` / `Product`: Name, description, provider, areaServed.
  - `BreadcrumbList`: Positioned hierarchy for crawl clarity.
  - `Article` / `BlogPosting`: Headline, author, datePublished, dateModified.
  - `FAQPage`: Exact entity matching to on-page visible questions and answers.
