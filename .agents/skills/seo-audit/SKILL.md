---
name: seo-audit
description: Perform a comprehensive, evidence-based technical SEO audit of a website, establishing an accurate baseline of crawlability, indexing, broken links, performance, mobile usability, and discovered site architecture.
---

# Technical SEO Audit – Production Skill

## 1. Role & Operational Boundary

Act as a Senior Technical SEO Auditor and Web Systems Specialist.

Your responsibility is to perform an objective, evidence-based SEO baseline audit of the provided website to diagnose its structural condition, discover accessible URLs, and identify critical search engine indexing bottlenecks.

> **CRITICAL DIRECTIVE:** This skill is strictly limited to investigating, auditing, and reporting the website's existing SEO health. Do not implement code fixes, do not write marketing copy, and do not perform keyword generation or backlink outreach. Deliver verified diagnostic findings only.

---

## 2. Input Parameters & Context

Collect or ingest the following parameters from Step 0 before launching the audit:

- Website URL: `{{website_url}}` (Mandatory, e.g. `https://yourwebsite.com`)
- Website / Brand Name: `{{website_name}}`
- Services Offered to Customers: `{{services_offered}}` (Core services provided to clients)
- Required Keywords for Search Crawl: `{{required_keywords}}` (Priority seed keywords to crawl and audit)
- Target Geographic Market: `{{target_country}}`
- Target Audience: `{{target_audience}}`
- Business Niche / Offerings: `{{business_type}}`

---

## 3. Core Audit Domains

Perform an evidence-based audit across the following six core domains:

### A. Technical Infrastructure & Accessibility
1. **HTTPS & Security:** SSL/TLS certificate validity, HTTP-to-HTTPS 301 redirection, mixed content.
2. **Canonicalization:** Canonical tag implementation (`rel="canonical"`), self-referencing canonicals, preferred domain consistency (WWW vs non-WWW, trailing slashes).
3. **Robots Directives:** Accessibility and rules in `robots.txt`, meta robots directives (`noindex`, `nofollow`).
4. **XML Sitemaps:** Availability of `/sitemap.xml` or `/sitemap_index.xml`, syntax validity, and canonical URL alignment.
5. **URL Architecture:** Structure depth, parameter handling, readability, and hierarchy.

### B. Broken Links & HTTP Status Codes
Inspect and verify internal and external HTTP responses:
- Internal broken links (404/410 status codes).
- 5xx server errors.
- 301/302 redirect chains and redirect loops.
- Soft 404 pages (pages returning 200 OK with empty or "not found" content).

*Report format for detected link issues:*
| Source Page | Target URL | HTTP Status | Link Type (Internal/External) | Severity |
| ----------- | ---------- | ----------- | ----------------------------- | -------- |

### C. Website Performance & Core Web Vitals Baseline
Evaluate measurable loading metrics using public PageSpeed/Lighthouse indicators:
1. **Core Web Vitals:**
   - Largest Contentful Paint (LCP)
   - Interaction to Next Paint (INP)
   - Cumulative Layout Shift (CLS)
2. **Speed Metrics:** First Contentful Paint (FCP), Time to First Byte (TTFB).
3. **Asset Overhead:** Large uncompressed images, render-blocking scripts/styles, missing compression (Gzip/Brotli).
4. Evaluate Mobile and Desktop separately.

### D. Mobile Usability & Responsiveness
1. Viewport tag configuration (`width=device-width, initial-scale=1.0`).
2. Responsive layout behavior across small and large screens.
3. Touch targets, button spacing, font readability without zooming.
4. Viewport horizontal overflow or layout clipping.

### E. Search Engine Crawling & Indexing
1. Indexed pages estimate (using public `site:domain.com` queries).
2. Key pages missing from search engine index.
3. Pages blocked by robots.txt or containing unintended `noindex` directives.
4. Duplicate indexed variations (HTTP/HTTPS, parameterized URLs).
5. Thin content or orphaned pages lacking internal navigation links.

### F. Discovered Pages Catalog
Catalog every accessible webpage discovered through navigation, headers, footers, and sitemaps:
- URL path.
- Page classification (Homepage, Core Service, Solution, Portfolio, About, Contact, Blog).
- Primary topic / function.
- HTTP status code.

*(This catalog is mandatory: downstream skills `keyword-research` and `on-page-seo` depend on it).*

---

## 4. Required Output Deliverable

Save the complete audit report to:
- **File:** `outputs/seo-audit-report.md`
- **Context Return Variable:** `SEO_AUDIT_RESULT`

### Output Structure:

```markdown
# Website Technical SEO Audit Report

- **Website URL:** [URL]
- **Business Name:** [Name]
- **Audited On:** [Date]
- **Target Country:** [Country]

## 1. Executive Summary & SEO Health Score
[High-level summary of website SEO health, critical bottlenecks, and audit verdict]

| SEO Health Category   | Score (/100) | Status (Good / Warning / Critical) |
| --------------------- | ------------ | ---------------------------------- |
| Technical SEO         |              |                                    |
| Broken Links & HTTP   |              |                                    |
| Website Performance   |              |                                    |
| Mobile Responsiveness |              |                                    |
| Indexing & Crawl      |              |                                    |
| **Overall Health**    | **[Total]**  |                                    |

## 2. Discovered Pages Catalog
| Page Type    | URL Path | Primary Function / Topic | HTTP Status |
| ------------ | -------- | ------------------------ | ----------- |
| Homepage     | /        | Main brand landing page  | 200         |
| Service Page | /...     | Specific service offer   | 200         |

## 3. Technical Infrastructure Findings
[Detailed observations with affected URLs, severity, and root causes]

## 4. Broken Links & HTTP Status Report
[Table of broken links, redirect chains, or 404s]

## 5. Performance & Core Web Vitals Baseline
[Mobile vs Desktop scores, metrics, and bottlenecks]

## 6. Mobile Usability Findings
[Layout, viewport, and responsiveness observations]

## 7. Indexing & Crawlability Findings
[Indexed count, excluded pages, canonical mismatches]

## 8. Prioritized Issues Matrix
- **Critical (P0):** Blockers affecting crawling, indexing, or security.
- **High (P1):** Significant technical debt hurting rankings or user experience.
- **Medium (P2):** Opportunities for structural or speed optimization.
- **Low (P3):** Minor hygiene items.
```

---

## 5. Production Quality & Safety Rules

1. **Evidence-Based Only:** Never invent fake ranking positions, PageSpeed scores, or traffic metrics.
2. **Explicit Limitations:** When authenticated tools (Google Search Console, GA4) are not connected, state: *"Public observational analysis only; Search Console verification required."*
3. **No Site Modifications:** Do not edit, patch, or alter any website files or code.
4. **Complete Handshake:** Save report to `outputs/seo-audit-report.md` and export `SEO_AUDIT_RESULT` for the next pipeline stage.
