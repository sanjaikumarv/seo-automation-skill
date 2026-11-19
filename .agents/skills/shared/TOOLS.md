# Standardized SEO Tools Documentation

This document centralizes tool references, analytical capabilities, usage guidelines, and data reliability constraints across the SEO skills ecosystem.

---

## 1. Web Crawlers & Inspection Utilities

### 1.1 HTTP Client / Curl / Native Fetch

- **Purpose:** Fast raw HTTP header inspection, status code verification, redirect chains, canonical link tags, and robots meta tags.
- **Capabilities:** Follows redirects (`-L`), measures TTFB (`curl -w`), captures raw response headers (`-I`).
- **Limitations:** Does not execute client-side JavaScript (SPA / hydration).
- **Appropriate Use Cases:** `seo-audit`, `technical-seo`.

### 1.2 Chrome Headless / Puppeteer / Browser Subagent

- **Purpose:** Full DOM rendering, client-rendered JavaScript inspection, Core Web Vitals profiling, hydrated schema validation.
- **Capabilities:** Inspects post-hydration DOM, executes scripts, extracts dynamic metadata.
- **Limitations:** Heavier compute footprint; rate-limit respectful crawling required.
- **Appropriate Use Cases:** `seo-audit`, `technical-seo`, `seo-on-page`.

---

## 2. Search Engine & SERP Analysis

### 2.1 Web Search / Search APIs

- **Purpose:** Live search query analysis, competitor identification, SERP feature discovery (snippets, People Also Ask, Knowledge Panels).
- **Capabilities:** Discovers active ranking contenders and live search intent patterns.
- **Data Reliability:** Real-time public observational search data.
- **Appropriate Use Cases:** `seo-keyword-research`, `seo-competitor-analysis`, `seo-content-strategy`.

---

## 3. Performance & Core Web Vitals (CWV)

### 3.1 Google PageSpeed Insights (PSI) & Lighthouse

- **Purpose:** Measure Core Web Vitals (LCP, INP, CLS), Total Blocking Time (TBT), and performance diagnostics.
- **Capabilities:** Produces lab diagnostics and CrUX (Chrome User Experience Report) field data.
- **Limitations:** Lab metrics may vary based on test runner geography and server load.
- **Appropriate Use Cases:** `seo-audit`, `technical-seo`, `seo-monitoring`.

---

## 4. Structured Data & Schema Validators

### 4.1 Schema.org Validator / Google Rich Results Testing

- **Purpose:** Validate JSON-LD microdata syntax, type hierarchies, and eligibility for rich snippets in Google SERPs.
- **Capabilities:** Identifies missing required/recommended properties according to schema.org standards.
- **Appropriate Use Cases:** `technical-seo`, `seo-on-page`.

---

## 5. Webmaster & Search Analytics

### 5.1 Google Search Console (GSC)

- **Purpose:** Ground-truth search performance (impressions, clicks, average CTR, average position), indexing coverage, and crawl stats.
- **Limitations:** Requires verified domain ownership or authenticated API access.
- **Handling When Unavailable:** When authenticated credentials are not provided, mark findings as `[Public observational search data; requires Google Search Console verification]`. **Never invent or fabricate Search Console figures.**
- **Appropriate Use Cases:** `seo-audit`, `seo-keyword-research`, `seo-competitor-analysis`, `seo-monitoring`.

### 5.2 Google Analytics 4 (GA4)

- **Purpose:** User engagement, conversion tracking, bounce/engagement rate, session duration, landing page conversion paths.
- **Limitations:** Requires authenticated property access. Mark unauthenticated metrics with verified disclaimer.
- **Appropriate Use Cases:** `seo-monitoring`, `seo-final-report`.

---

## 6. Free Tools First Command Reference

When executing skills without paid subscriptions, use these free command-line and API patterns:

### 6.1 HTTP & Header Inspection (Curl)
```bash
# Check status code, redirect destination, and response headers
curl -ILs -o /dev/null -w "%{http_code} %{url_effective} %{time_total}\n" "https://example.com"

# Capture robots.txt
curl -s "https://example.com/robots.txt"

# Capture XML sitemap index
curl -s "https://example.com/sitemap.xml"
```

### 6.2 Core Web Vitals & Performance (Public PageSpeed Insights API)
```bash
# Query Google PageSpeed Insights public REST API (no auth required for low volume)
curl -s "https://www.googleapis.com/pagespeedonline/v5/runPagespeed?url=https://example.com&strategy=mobile"
```

### 6.3 Google Search Operators (SERP Analysis)
- `site:example.com`: Indexation estimation and indexed URL discovery.
- `site:example.com inurl:service`: Discover service landing pages.
- `site:example.com "keyword"`: Check existing content coverage for a target query.
- `related:example.com`: Identify algorithmic competitor entities.
- `intitle:"keyword" "keyword"`: Check SERP competitor saturation.

