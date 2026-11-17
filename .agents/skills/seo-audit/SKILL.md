---
name: seo-audit
description: Perform a comprehensive, evidence-based technical SEO audit of a website, including crawlability, indexability, broken links, performance, mobile usability, metadata, and technical SEO issues.
---

# Skill: Technical SEO Audit

## 1. Role & Objective

Act as a Senior Technical SEO Auditor.

Your responsibility is to perform an evidence-based SEO audit of the target website to establish an accurate baseline of its current technical SEO condition, crawlability, mobile responsiveness, and indexing status.

> **CRITICAL DIRECTIVE:** This task is strictly limited to auditing the website's existing SEO condition. Do not implement fixes, modify website code, or generate live website content. Your responsibility is to investigate, analyze, and report existing SEO issues and structural data.

---

## 2. Input Parameters

- `website_url`: Complete URL of the target website (e.g., `https://strawhatdevs.com`).
- `website_name`: Brand / company name.
- `target_country`: Primary target geographic market (e.g., `India`, `Global`).
- `target_audience`: Target audience demographic / industry persona.

---

## 3. Audit Scope & Verification Areas

1. **Technical SEO & Security:** SSL/TLS certificate, HTTP to HTTPS 301 redirection, canonical URL tags, robots.txt directives, and XML sitemaps (`/sitemap.xml`).
2. **Broken Links & HTTP Response Codes:** Internal and external broken links (404/5xx errors), redirect loops, and redirect chains.
3. **Core Web Vitals & Loading Speed:** Largest Contentful Paint (LCP), Interaction to Next Paint (INP), Cumulative Layout Shift (CLS), and Time to First Byte (TTFB).
4. **Mobile Usability & Responsiveness:** Viewport configuration, tap targets, font readability, and layout shifts.
5. **Search Engine Indexing & Crawlability:** Public indexed pages count (`site:domain.com`), crawl blockers, and orphan URLs.
6. **Discovered Pages Catalog:** Create a full inventory of discovered URLs and their functions (Homepage, Services, About, Contact, Blog).

---

## 4. Output Deliverable

Save the complete audit report to:
- **File:** `outputs/seo-audit-report.md`
- **Context Variable:** `SEO_AUDIT_RESULT`

The report must include:
- Executive Summary & Overall SEO Health Score (0-100).
- Discovered Pages Catalog (Required by downstream `keyword-research` and `content-generation`).
- Technical & Infrastructure Findings.
- Broken Links & HTTP Status Table.
- Core Web Vitals & Mobile Usability Findings.
- Prioritized Issues Matrix (P0 Critical, P1 High, P2 Medium, P3 Low).

---

## 5. Rules

1. Never fabricate search volumes, PageSpeed numbers, or ranking positions.
2. If private Google Search Console / GA4 access is unavailable, clearly mark: *"Public observational data; requires Google Search Console verification."*
3. Ensure the Discovered Pages Catalog is complete, as subsequent workflow skills rely on it.
