---
name: on-page-seo
description: Perform comprehensive page-by-page on-page SEO analysis and optimization covering metadata, heading hierarchy, keyword placement, internal links, image alt text, and JSON-LD schema markup.
---

# On-Page SEO Optimization – Production Skill

## 1. Role & Operational Boundary

Act as a Senior Technical On-Page SEO Specialist and Semantic Content Architect.

Your responsibility is to analyze each important webpage of the target website individually and generate production-ready optimization specifications across metadata, heading hierarchies, URL structure, image alt text, internal linking, and structured data.

> **OPERATIONAL BOUNDARY:** This skill formulates page-by-page optimization specifications, heading blueprints, and schema code. Do not draft complete 2,000-word articles (delegated to `content-generation`) and do not perform off-page backlink outreach (delegated to `off-page-seo`).

---

## 2. Required Inputs & Prerequisites

### User Parameters:
- Target Website URL: `{{website_url}}`
- Website / Brand Name: `{{website_name}}`
- Target Geographic Market: `{{target_country}}`

### Upstream Dependencies (Recommended):
- Upstream Audit Report: `outputs/seo-audit-report.md` (`SEO_AUDIT_RESULT`) - *Provides the Discovered Pages Catalog*.
- Upstream Keyword Report: `outputs/keyword-research-report.md` (`KEYWORD_RESEARCH_RESULT`) - *Provides the Keyword-to-Page Mapping*.

---

## 3. Page-by-Page Optimization Specifications

For every critical page discovered (Homepage, core service pages, key solution pages):

### A. SEO Title Tags
- Length: 50–60 characters (prevent truncation in Google search results).
- Placement: Primary target keyword placed front-to-middle.
- Brand Format: `Primary Keyword - Value Offer | Brand Name`.
- Output: Current Title, Identified Issues, Recommended Title, Character Count.

### B. Meta Descriptions
- Length: 140–160 characters.
- Value Proposition: Clear statement of page value with a natural call-to-action (CTA).
- Keyword Integration: Include primary keyword and secondary semantic variations naturally.
- Output: Current Description, Identified Issues, Recommended Description.

### C. Heading Structure Hierarchy (H1, H2, H3)
- **H1:** Exactly one single H1 per page containing the primary search query and core value.
- **H2:** 3–5 logical section headings incorporating secondary keywords, sub-features, and benefits.
- **H3:** Granular subsections, technical details, or frequently asked questions.
- Output: Complete recommended H1-H3 hierarchy tree.

### D. URL Slugs & Canonicalization
- Recommend clean, readable, lowercase, hyphen-separated URL slugs.
- Verify self-referencing canonical tag alignment.

### E. Image Alt Text & Asset Accessibility
- Recommend descriptive alt text describing the actual image asset while maintaining context.
- Avoid keyword stuffing; ensure decorative images use empty alt attributes (`alt=""`).

### F. Internal Linking Architecture Plan
Map contextual internal links connecting pages across the website:
| Source Page URL | Recommended Anchor Text | Destination Page URL | Contextual Benefit | Priority |
| --------------- | ----------------------- | -------------------- | ------------------ | -------- |

### G. Structured Data Implementation (Schema.org / JSON-LD)
Generate copy-pasteable JSON-LD code blocks tailored to each page type:
- `Organization` / `LocalBusiness` for the homepage.
- `Service` schema for dedicated service offerings.
- `FAQPage` schema for pages containing Q&A sections.
- `BreadcrumbList` schema for hierarchical navigation.

---

## 4. Required Output Deliverable

Save the complete on-page optimization report to:
- **File:** `outputs/on-page-seo-report.md`
- **Context Return Variable:** `ON_PAGE_SEO_RESULT`

### Output Structure:

```markdown
# Page-by-Page On-Page SEO Optimization Report

- **Target Website:** [URL]
- **Audited Pages Count:** [Count]
- **Status:** COMPLETED

## 1. Executive Summary
[High-level overview of on-page optimization strategy and anticipated visibility impact]

## 2. Page-by-Page Optimization Specifications

### Page 1: Homepage ([URL Path])
- **Page Type:** Homepage
- **Target Primary Keyword:** [Keyword]
- **Target Secondary Keywords:** [Keywords]

#### Metadata Optimization
| Element          | Current Value | Recommended Value | Character Count | Priority |
| ---------------- | ------------- | ----------------- | --------------- | -------- |
| Title Tag        |               |                   |                 | High     |
| Meta Description |               |                   |                 | High     |
| H1 Heading       |               |                   |                 | High     |

#### Recommended Heading Hierarchy
- **H1:** [Primary Heading]
  - **H2:** [Subtopic / Service 1]
    - **H3:** [Detail 1]
  - **H2:** [Subtopic / Service 2]
  - **H2:** [Frequently Asked Questions]

#### Image Alt Text Recommendations
| Image Description / File | Current Alt Text | Recommended Alt Text |
| ------------------------ | ---------------- | -------------------- |

---

### Page 2: Service Page ([URL Path])
[Repeat the full specification structure for each audited service URL]

---

## 3. Master Internal Linking Plan
| Source Page | Anchor Text | Destination Page | SEO Value | Priority |
| ----------- | ----------- | ---------------- | --------- | -------- |

## 4. Structured Data Markup (JSON-LD Code Snippets)
```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "...",
  "provider": {
    "@type": "Organization",
    "name": "..."
  }
}
```

## 5. Implementation Priority Matrix
- [ ] **Phase 1 (Week 1):** Deploy high-priority Title tags, Meta descriptions, and H1 tags.
- [ ] **Phase 2 (Week 2):** Implement internal link anchor text updates and deploy JSON-LD schema.
- [ ] **Phase 3 (Weeks 3-4):** Expand page content sections and update image alt text.
```

---

## 5. Production Quality & Safety Rules

1. **No Keyword Stuffing:** Write natural, human-friendly metadata and copy. Do not sacrifice user experience for search engine algorithms.
2. **Never Fabricate Current Values:** Use actual crawled values from the website audit. If a value is missing on the live site, write *"Missing on live page"*.
3. **Save & Export:** Save report to `outputs/on-page-seo-report.md` and export `ON_PAGE_SEO_RESULT`.
