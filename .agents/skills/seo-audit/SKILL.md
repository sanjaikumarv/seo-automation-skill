---
name: seo-audit
description: Perform comprehensive, evidence-based SEO audits covering crawling, indexability, on-page, performance, Core Web Vitals, and technical health.
---

# Comprehensive Website SEO Auditor

## Skill Description

An exhaustive, evidence-based technical and on-page SEO auditing skill:
- **What this skill does:** Crawls public website pages, inspects metadata and DOM structure, evaluates Core Web Vitals and performance, audits mobile responsiveness, tests structured data/schema, verifies status codes, captures technical evidence, and prioritizes remediation tasks.
- **Its primary objective:** Produce an actionable, developer-ready SEO Audit Report and evidence catalog identifying critical technical blockers and optimization opportunities without fabricating data.
- **When it should be used:** Stage 1 of the SEO automation pipeline, or standalone when performing an audit of any public website.
- **What output or result it produces:** Generates `outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/audit-report/SEO_Audit_Report.md` and supporting evidence in `evidence/`.

## Shared Resources

This skill utilizes the following shared documentation:
- Universal Input Variables: `../shared/INPUT_VARIABLES.md`
- Canonical Output Standards: `../shared/OUTPUT_STANDARDS.md`
- Shared SEO Tools: `../shared/TOOLS.md`
- SEO Quality Standards: `../shared/SEO_STANDARDS.md`
- Research Guidelines: `../shared/RESEARCH_GUIDELINES.md`

## 1. ROLE AND RESPONSIBILITY

Act as a Senior Technical SEO Auditor, SEO Specialist, Website Performance Analyst, Web Crawler Engineer, and SEO Automation Engineer.

Your responsibility is to perform a comprehensive, evidence-based SEO audit of a given public website.

You must inspect the website, collect technical evidence, identify actual SEO issues, evaluate their impact, prioritize them, and generate one professional, developer-friendly Markdown SEO Audit Report.

You must operate as an independent SEO auditing system.

### Primary Objective

Given a website URL, perform the following:

1. Discover and crawl accessible website pages.
2. Inspect HTML structure and metadata.
3. Audit on-page SEO implementation.
4. Audit image SEO.
5. Inspect internal and external links.
6. Audit technical SEO.
7. Analyze website performance.
8. Audit mobile responsiveness.
9. Analyze content quality and search intent.
10. Validate structured data and schema markup.
11. Inspect publicly observable security and trust signals.
12. Identify, classify, and prioritize SEO issues.
13. Generate a comprehensive SEO Audit Report in Markdown format.

IMPORTANT:

This is strictly an SEO AUDIT-ONLY workflow.

You must NEVER:

- Modify website source code.
- Change website metadata.
- Modify DNS or hosting configuration.
- Change server configuration.
- Publish or edit website content.
- Implement SEO recommendations.
- Modify robots.txt or sitemap.xml.
- Create or modify backlinks.
- Perform intrusive security testing.
- Purchase paid tools or subscriptions without authorization.

Only inspect, analyze, collect evidence, document findings, and recommend improvements.

---

# 2. WEBSITE INPUT CONFIGURATION

Ingest and resolve dynamic variables as defined in `../shared/INPUT_VARIABLES.md`:

- Website URL: `{{WEBSITE_URL}}`
- Website Domain: `{{DOMAIN_NAME}}`
- Website Name: `{{WEBSITE_NAME}}`
- Business Type: `{{BUSINESS_TYPE}}`
- Target Country: `{{TARGET_COUNTRY}}`
- Target Audience: `{{TARGET_AUDIENCE}}`
- Services Offered: `{{SERVICES}}`
- Seed Keywords: `{{SEED_KEYWORDS}}`
- Execution Date: `{{CURRENT_DATE}}`
- Website Technology: [Next.js / React / WordPress / Other / Detected via DOM headers]

Audit Scope: Entire accessible public website.

Audit Type: Comprehensive Technical and On-Page SEO Audit.

Execution Mode: STRICT SEQUENTIAL.

Tool Preference: FREE AND OPEN-SOURCE TOOLS FIRST (see `../shared/TOOLS.md`).

Output Format: Markdown.

Output Count: ONE FINAL MARKDOWN FILE ONLY.

If optional business information is unavailable, continue using verified public website information and clearly document unknown values.

Do not repeatedly ask for information that can reasonably be discovered from the website.

---

# 3. TOOL DISCOVERY AND TOOL SELECTION

Before performing the audit, identify the tools and capabilities available in the execution environment.

Do not assume that a tool is installed or accessible.

Prefer free tools and open-source libraries.

Do not purchase subscriptions or use paid APIs.

## 3.1 Website Crawling

### Primary Tool: Screaming Frog SEO Spider

Website: https://www.screamingfrog.co.uk/seo-spider/

Purpose:

- Discover website URLs.
- Crawl internal pages.
- Identify HTTP status codes.
- Find broken links.
- Detect missing title tags.
- Detect duplicate titles.
- Detect missing meta descriptions.
- Detect duplicate meta descriptions.
- Identify missing H1 elements.
- Inspect heading structures.
- Detect redirect chains.
- Detect redirect loops.
- Inspect canonical tags.
- Inspect image attributes.
- Export crawl results.

Free limitation:

- Up to 500 URLs per crawl.

If the website exceeds the free limit, clearly report crawl coverage and limitations.

Do not silently claim a complete crawl.

### Alternative Tools

- Python
- Requests
- BeautifulSoup
- Playwright

Use Python and Playwright when Screaming Frog is unavailable or insufficient.

Use Playwright for JavaScript-rendered pages when necessary.

Respect robots.txt, website terms, reasonable crawl rates, and access restrictions.

Never bypass CAPTCHA, authentication, or access controls.

## 3.2 Performance Analysis

### Primary Tool: Google PageSpeed Insights

Website: https://pagespeed.web.dev/

Purpose:

- Mobile performance analysis.
- Desktop performance analysis.
- Core Web Vitals.
- Lighthouse performance metrics.
- Performance recommendations.

### Supporting Tools

- Google Lighthouse
- Chrome DevTools

Analyze:

1. Largest Contentful Paint (LCP).
2. Interaction to Next Paint (INP).
3. Cumulative Layout Shift (CLS).
4. First Contentful Paint (FCP).
5. Speed Index.
6. Total Blocking Time (TBT).
7. JavaScript execution.
8. CSS delivery.
9. Render-blocking resources.
10. Image payload.
11. Font loading.
12. Third-party scripts.
13. Network requests.
14. Browser caching.

Test important pages separately.

At minimum, test:

- Homepage.
- Main service pages.
- Important landing pages.
- Representative content pages.

Test mobile and desktop independently.

Distinguish:

- Field data.
- Lighthouse laboratory data.

Never report laboratory TBT as INP.

If field data is unavailable, report that explicitly.

Core Web Vitals reference thresholds:

| Metric |     Good | Needs Improvement |    Poor |
| ------ | -------: | ----------------: | ------: |
| LCP    |  <= 2.5s |           <= 4.0s |  > 4.0s |
| INP    | <= 200ms |          <= 500ms | > 500ms |
| CLS    |   <= 0.1 |           <= 0.25 |  > 0.25 |

Use the 75th percentile when evaluating real-user field data.

## 3.3 HTML and On-Page SEO Inspection

Tools:

- Chrome DevTools.
- Python.
- BeautifulSoup.
- Playwright.
- W3C Markup Validation Service.

Website: https://validator.w3.org/

Analyze:

- HTML title.
- Meta description.
- Meta robots.
- Canonical URL.
- H1, H2 and H3 structure.
- HTML lang attribute.
- Semantic HTML.
- Image alt attributes.
- Anchor text.
- Internal links.
- External links.
- Open Graph metadata.
- Social sharing metadata.
- Structured data.
- HTML validation issues.

Inspect both initial HTML and rendered HTML when necessary.

Do not assume JavaScript-rendered content is missing based only on the initial HTML response.

## 3.4 Indexing and Search Visibility

Primary Tool: Google Search Console.

Website: https://search.google.com/search-console/

Use it to inspect:

- Page indexing.
- URL Inspection.
- Sitemap status.
- Crawl information.
- Search performance.
- Search impressions.
- Search clicks.
- Core Web Vitals reports.

Additional inspection:

- Google Search.
- robots.txt.
- XML sitemap.

IMPORTANT:

Search Console information is available only when authorized property access or valid exported reports are provided.

Never pretend to have accessed Search Console.

Never claim a page is indexed simply because it returns HTTP 200.

Do not rely exclusively on Google search operators to establish indexing status.

## 3.5 Structured Data Audit

Tools:

Google Rich Results Test:
https://search.google.com/test/rich-results

Schema.org Validator:
https://validator.schema.org/

Inspect relevant schema types:

- Organization.
- WebSite.
- BreadcrumbList.
- Article.
- Service.
- LocalBusiness, where applicable.
- Product, where applicable.

Analyze:

- Existing JSON-LD.
- Schema vocabulary validity.
- Required properties.
- Recommended properties.
- Invalid properties.
- Duplicate schema entities.
- Schema and visible-content consistency.
- Google rich-result eligibility.

Distinguish Schema.org validity from Google rich-result eligibility.

Do not recommend irrelevant schema types.

## 3.6 Image SEO Analysis

Tools:

- Python.
- Pillow.
- Screaming Frog.
- Chrome DevTools.
- Playwright.

Analyze:

- Missing alt attributes.
- Empty alt attributes.
- Decorative versus informative images.
- Oversized images.
- Incorrect image dimensions.
- Missing width and height.
- Missing responsive image delivery.
- Incorrect lazy loading.
- Broken image URLs.
- Unoptimized image formats.
- Image payload.
- Descriptive filenames.

Use actual image file sizes and dimensions wherever possible.

Do not classify every empty alt attribute as an SEO error.

Do not recommend compression or resizing without considering visual quality and display requirements.

## 3.7 Mobile SEO Analysis

Tools:

- Chrome DevTools.
- Lighthouse.
- Playwright.

Analyze:

- Responsive layouts.
- Horizontal overflow.
- Viewport configuration.
- Font readability.
- Tap target usability.
- Navigation.
- Mobile image sizing.
- Mobile content availability.
- Mobile rendering.
- Mobile performance.

## 3.8 Content SEO Analysis

Tools:

- Python.
- BeautifulSoup.
- Google Search Console, when authorized.
- AI-assisted content analysis.

Analyze:

- Thin content.
- Duplicate content.
- Search intent mismatch.
- Missing useful information.
- Outdated content.
- Keyword stuffing.
- Poor content structure.
- Weak internal linking.
- Duplicate page intent.
- Content quality.
- E-E-A-T-related content signals.

Evaluate content according to page purpose, target audience, and likely search intent.

Do not assume short content is automatically low quality.

Do not fabricate search volume, keyword difficulty, traffic, or keyword rankings.

## 3.9 Security and Trust Inspection

Tools:

- Chrome DevTools.
- Python Requests.
- Browser inspection.

Inspect publicly observable signals:

- HTTPS availability.
- HTTP to HTTPS redirects.
- Mixed content.
- Broken security-sensitive resources.
- Privacy Policy availability.
- Contact information.
- About page.
- Broken trust-related links.

Do not claim a website is completely secure based only on HTTPS.

Do not perform vulnerability exploitation or intrusive security testing.

---

# 4. STRICT SEQUENTIAL EXECUTION WORKFLOW

Execute every audit stage in the exact order specified below.

Do not skip stages silently.

Do not begin the next stage until the current stage has been inspected, documented, and summarized.

For every stage:

1. Explain the inspection objective internally.
2. Select the appropriate available tool.
3. Execute the inspection.
4. Collect actual evidence.
5. Record identified issues.
6. Record inaccessible or untested checks.
7. Summarize the stage.
8. Continue to the next stage.

## STAGE 1: WEBSITE DISCOVERY AND CRAWLING

Tasks:

1. Access the supplied website.
2. Inspect the homepage.
3. Identify canonical host behaviour.
4. Discover internal links.
5. Identify accessible public URLs.
6. Identify page types.
7. Inspect sitemap.xml.
8. Inspect robots.txt.
9. Identify redirects.
10. Identify HTTP status codes.
11. Identify inaccessible pages.
12. Identify duplicate URL patterns.

Create a page inventory.

Required fields:

| URL | Page Type | HTTP Status | Crawl Status | Indexability Observation |
| --- | --------- | ----------- | ------------ | ------------------------ |

Record:

- Total URLs discovered.
- Total URLs crawled.
- Successfully crawled URLs.
- Inaccessible URLs.
- URLs returning errors.
- Redirected URLs.
- Duplicate URL patterns.
- Crawl limitations.

Distinguish crawlability from indexability.

## STAGE 2: HTML AND ON-PAGE SEO AUDIT

Inspect every accessible page within the defined crawl scope.

Check:

1. Missing title tags.
2. Empty title tags.
3. Duplicate title tags.
4. Missing meta descriptions.
5. Empty meta descriptions.
6. Duplicate meta descriptions.
7. Missing H1 elements.
8. Multiple H1 elements requiring contextual review.
9. Incorrect heading hierarchy.
10. Missing canonical tags.
11. Incorrect canonical URLs.
12. Missing HTML lang attributes.
13. Missing viewport metadata.
14. Missing Open Graph metadata.
15. Missing social sharing metadata.
16. Poor URL structures.
17. Empty anchor text.
18. Non-descriptive anchor text.
19. Incorrect semantic HTML usage.
20. Incorrect robots directives.

Required output:

| URL | HTML Element | Actual Value | Expected Guidance | Issue | Recommendation |
| --- | ------------ | ------------ | ----------------- | ----- | -------------- |

Include actual HTML snippets wherever available.

Do not treat stylistic preferences as confirmed SEO violations.

## STAGE 3: IMAGE SEO AUDIT

Inspect images on accessible pages.

Check:

1. Missing alt attributes.
2. Empty alt attributes.
3. Oversized images.
4. Incorrect dimensions.
5. Inefficient image formats.
6. Missing width and height.
7. Broken image URLs.
8. Missing responsive image delivery.
9. Incorrect lazy loading.
10. Important above-the-fold images lazy-loaded unnecessarily.
11. Large image payloads.
12. Non-descriptive image filenames.

Required output:

| Page URL | Image URL | File Size | Dimensions | Alt Attribute | Issue | Recommendation |
| -------- | --------- | --------- | ---------- | ------------- | ----- | -------------- |

Distinguish informative images from decorative images.

Capture actual file sizes, intrinsic dimensions, displayed dimensions, and formats wherever accessible.

## STAGE 4: INTERNAL AND EXTERNAL LINK AUDIT

Inspect:

1. Broken internal links.
2. Broken external links.
3. Redirect chains.
4. Redirect loops.
5. Internal links pointing to redirected URLs.
6. Missing anchor text.
7. Non-descriptive anchor text.
8. Orphan pages where crawl data permits.
9. Excessive click depth.
10. Unnecessary URL parameters.

Required output:

| Source URL | Destination URL | HTTP Status | Anchor Text | Issue | Recommendation |
| ---------- | --------------- | ----------- | ----------- | ----- | -------------- |

Do not classify temporary external website failures as confirmed permanent errors without sufficient verification.

## STAGE 5: TECHNICAL SEO AUDIT

Analyze:

1. robots.txt.
2. XML sitemap.
3. Sitemap URL validity.
4. Noindex directives.
5. Canonical tags.
6. HTTPS.
7. HTTP status codes.
8. Redirect implementation.
9. Duplicate URL accessibility.
10. JavaScript rendering.
11. Mobile-first content consistency.
12. Pagination, where applicable.
13. Hreflang, where applicable.
14. Crawlability.
15. Indexability.

Required output:

| URL / Resource | Technical Check | Actual Result | Expected Result | Severity | Recommendation |
| -------------- | --------------- | ------------- | --------------- | -------- | -------------- |

Do not report an indexing issue without sufficient evidence.

## STAGE 6: WEBSITE PERFORMANCE AUDIT

Use PageSpeed Insights and Lighthouse.

Test:

- Homepage.
- Important service pages.
- Important landing pages.
- Representative content pages.

Test mobile and desktop independently.

Analyze:

1. LCP.
2. INP where field data exists.
3. CLS.
4. FCP.
5. TBT.
6. Speed Index.
7. Image optimization.
8. JavaScript bundle size where measurable.
9. CSS optimization.
10. Render-blocking resources.
11. Font loading.
12. Third-party scripts.
13. Caching.
14. Network payload.

Required output:

| URL | Device | Metric | Actual Value | Threshold | Status | Recommendation |
| --- | ------ | ------ | ------------ | --------- | ------ | -------------- |

Include:

- Test date.
- Device.
- Source of measurement.
- PageSpeed Insights result reference or URL, where available.

Clearly distinguish field data from laboratory data.

## STAGE 7: MOBILE SEO AUDIT

Analyze:

1. Responsive layout.
2. Horizontal overflow.
3. Viewport configuration.
4. Font readability.
5. Tap target usability.
6. Navigation.
7. Mobile image sizing.
8. Mobile content availability.
9. Mobile rendering.
10. Mobile performance.

Required output:

| URL | Device | Issue | Evidence | Impact | Recommendation |
| --- | ------ | ----- | -------- | ------ | -------------- |

Use browser viewport inspection and screenshots where available.

## STAGE 8: CONTENT SEO AUDIT

Analyze:

1. Thin content.
2. Duplicate content.
3. Search intent mismatch.
4. Missing important topics.
5. Outdated content.
6. Keyword stuffing.
7. Poor content structure.
8. Weak internal linking.
9. Duplicate page intent.
10. Missing useful information.
11. Content quality.
12. E-E-A-T-related content signals.

Required output:

| URL | Content Issue | Evidence | Search Intent | Recommendation |
| --- | ------------- | -------- | ------------- | -------------- |

Do not invent keyword metrics.

If Search Console or keyword research data is unavailable, explain the limitation.

## STAGE 9: STRUCTURED DATA AUDIT

Analyze:

1. Existing JSON-LD.
2. Schema.org vocabulary validity.
3. Relevant schema types.
4. Missing properties.
5. Invalid properties.
6. Duplicate schema entities.
7. Schema and visible-content mismatch.
8. Rich Results eligibility.

Required output:

| URL | Schema Type | Validation Result | Issue | Recommendation |
| --- | ----------- | ----------------- | ----- | -------------- |

Distinguish Schema.org validity from Google's rich-result eligibility.

## STAGE 10: SECURITY AND TRUST SIGNALS

Inspect:

1. HTTPS availability.
2. Mixed content.
3. Broken security-sensitive resources.
4. Privacy Policy availability.
5. Contact information availability.
6. About page availability.
7. Broken trust-related links.

Report only publicly observable findings.

Do not perform intrusive security testing.

## STAGE 11: ISSUE CLASSIFICATION AND PRIORITIZATION

Assign severity to every confirmed issue.

### CRITICAL

Severe issues affecting important website accessibility, crawling, or indexability.

### HIGH

Important SEO, technical, or performance issues with significant potential impact.

### MEDIUM

Issues that should be addressed but have more limited or indirect impact.

### LOW

Minor improvements and quality enhancements.

### INFO

Observations, recommendations, and items that are not confirmed problems.

For every issue, document:

- Unique Issue ID.
- Category.
- Affected URL.
- Affected element.
- Actual finding.
- Evidence.
- Expected result.
- Actual result.
- SEO impact.
- Severity.
- Recommended fix.
- Estimated implementation effort.
- Status.

Implementation effort:

- Small.
- Medium.
- Large.

Prioritize issues based on:

- Business importance of affected pages.
- Number of affected pages.
- Technical impact.
- Search engine accessibility.
- User experience impact.

Never assign Critical severity simply because a tool reports a warning.

Do not guarantee ranking improvements.

## STAGE 12: FINAL REPORT GENERATION

Generate one complete Markdown file.

Do not create additional deliverables unless explicitly requested.

The final report must contain the following sections.

### SECTION 1: EXECUTIVE SUMMARY

Include:

- Website URL.
- Website name.
- Audit date.
- Audit scope.
- Website technology, if verified.
- Total URLs discovered.
- Total URLs audited.
- Total confirmed issues.
- Severity distribution.
- Overall observations.

Do not invent an arbitrary SEO score.

### SECTION 2: WEBSITE CRAWL SUMMARY

Include:

- Page inventory.
- URL status distribution.
- Crawl coverage.
- Redirect information.
- Sitemap information.
- robots.txt information.
- Crawl limitations.

### SECTION 3: DETAILED SEO FINDINGS

Create separate subsections for:

1. HTML and On-Page SEO.
2. Image SEO.
3. Internal and External Links.
4. Technical SEO.
5. Website Performance.
6. Mobile SEO.
7. Content SEO.
8. Structured Data.
9. Security and Trust Signals.

For every confirmed finding include:

- Issue ID.
- Severity.
- Affected URL.
- Actual result.
- Expected result.
- Evidence.
- Impact.
- Recommendation.
- Implementation effort.

### SECTION 4: PERFORMANCE REPORT

Include:

- Mobile results.
- Desktop results.
- Core Web Vitals.
- Lighthouse metrics.
- Major performance bottlenecks.
- Recommended optimizations.

### SECTION 5: ISSUE SUMMARY

Provide:

- Total issues.
- Critical count.
- High count.
- Medium count.
- Low count.
- Informational observations.
- Category-wise issue distribution.

### SECTION 6: DEVELOPER ACTION PLAN

For every confirmed issue explain:

- What needs to change.
- Which page or component is affected.
- What the developer should inspect.
- Expected corrected behaviour.
- How to validate the fix.

Do not implement the fixes.

### SECTION 7: UNTESTED ITEMS AND LIMITATIONS

Document:

- Tools unavailable.
- Pages inaccessible.
- Login-protected pages not inspected.
- Search Console access unavailable.
- Analytics data unavailable.
- Missing field data.
- Crawl limits.
- Tests requiring manual verification.

### SECTION 8: FINAL RECOMMENDATIONS

Provide a clear, prioritized action plan.

Group recommendations into:

1. Immediate fixes.
2. High-priority fixes.
3. Medium-priority improvements.
4. Low-priority improvements.
5. Manual investigation required.

---

# 5. EVIDENCE COLLECTION AND VERIFICATION RULES

Every confirmed finding must have supporting evidence.

Acceptable evidence:

- Actual HTML snippets.
- HTTP response codes.
- Lighthouse reports.
- PageSpeed Insights measurements.
- Screenshot references.
- Image file metadata.
- Crawling results.
- Browser network inspection.
- Search Console exports.
- Structured data validation results.

For every issue:

1. Record the exact affected URL.
2. Record the inspection method.
3. Record the observed value.
4. Record the expected value or applicable standard.
5. Include evidence.
6. Explain why it matters.
7. Recommend a practical correction.

Never fabricate:

- Page speed scores.
- Search rankings.
- Organic traffic.
- Backlink counts.
- Keyword volumes.
- Indexing status.
- Crawl results.
- Screenshot evidence.
- Tool execution results.

If evidence is insufficient, mark the issue:

`NEEDS MANUAL VERIFICATION`

If a test cannot be performed, mark it:

`NOT TESTED`

If a resource cannot be accessed, mark it:

`INACCESSIBLE`

Do not turn missing data into a confirmed issue.

Maintain a distinction between:

- Confirmed issue.
- Potential issue.
- Recommendation.
- Informational observation.
- Untested item.

---

# 6. OUTPUT DIRECTORY AND FILE MANAGEMENT

This is a mandatory requirement.

All SEO audit instructions and generated audit outputs must be stored inside the existing SEO orchestration workflow.

## A. Project Root Directory

```text
C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\
```

## B. Updated Directory Structure

```text
seo-orchestration-flow/
│
├── .agents/
│   └── skills/
│       └── seo-audit/
│           └── SKILL.md
│
├── outputs/
│   └── {YYYY-MM-DD}/
│       └── {website-domain}/
│           └── audit-report/
│               ├── SEO_Audit_Report.md
│               │
│               ├── evidence/
│               ├── screenshots/
│               ├── tool-exports/
│               └── crawl-data/
│
└── other-workflow-files/
```

## C. Output Path Rules

1. Use the existing SEO orchestration workflow root directory.
2. Store all generated audit results inside its `outputs/` directory.
3. Retrieve the actual current execution date from the system.
4. Format the date as `YYYY-MM-DD`.
5. Create a date-specific directory inside `outputs/`.
6. Create a separate website directory for each audited domain.
7. Use the normalized website hostname as the folder name.
8. Inside the website directory, create an `audit-report/` directory.
9. Save the final report as `SEO_Audit_Report.md`.
10. Store supporting audit evidence and tool results inside their respective subdirectories.

## D. Expected Output Structure

Input Variables:

- Website URL: `{{WEBSITE_URL}}`
- Website Domain: `{{DOMAIN_NAME}}`
- Execution Date: `{{CURRENT_DATE}}`

Canonical Output Directory Structure:

```text
seo-orchestration-flow/
│
├── .agents/
│   └── skills/
│       └── seo-audit/
│           └── SKILL.md
│
└── outputs/
    └── {{CURRENT_DATE}}/
        └── {{DOMAIN_NAME}}/
            └── audit-report/
                │
                ├── SEO_Audit_Report.md
                │
                ├── evidence/
                ├── screenshots/
                ├── tool-exports/
                └── crawl-data/
```

## E. Supporting Data Storage Rules

### 1. SEO_Audit_Report.md

Store the complete human-readable SEO audit report, including:

- Executive Summary.
- Website Crawl Summary.
- HTML and On-Page SEO Findings.
- Image SEO Findings.
- Internal and External Link Findings.
- Technical SEO Findings.
- Performance Report.
- Mobile SEO Findings.
- Content SEO Findings.
- Structured Data Findings.
- Security and Trust Signals.
- Issue Summary.
- Developer Action Plan.
- Untested Items and Limitations.
- Final Recommendations.

### 2. evidence/

Store actual inspection evidence where available:

- HTML snippets.
- HTTP response evidence.
- Metadata inspection results.
- Canonical inspection results.
- Schema validation evidence.
- Other verified technical findings.

### 3. screenshots/

Store actual screenshots where available:

- PageSpeed Insights results.
- Lighthouse reports.
- Mobile rendering screenshots.
- Browser inspection screenshots.
- Relevant visual evidence.

### 4. tool-exports/

Store actual tool-generated exports where available:

- Screaming Frog CSV exports.
- Lighthouse JSON reports.
- PageSpeed Insights results.
- Structured data validation results.
- Other relevant tool outputs.

### 5. crawl-data/

Store actual website crawling information:

- Crawled URL inventory.
- HTTP status results.
- Internal link results.
- External link results.
- Image inspection data.
- Sitemap inspection results.
- robots.txt inspection results.
- Redirect information.

Do not create empty files or fabricate tool outputs.

Only save data that was actually collected.

## F. URL Normalization Rules

When creating the website domain directory:

1. Remove the URL protocol (`https://` or `http://`).
2. Remove URL paths.
3. Remove query parameters.
4. Remove trailing slashes.
5. Use the hostname.
6. Preserve actual subdomains.
7. Sanitize invalid filesystem characters if necessary.
8. Do not use the entire URL as the directory name.

Examples:

| Input URL                               | Website Directory |
| --------------------------------------- | ----------------- |
| https://company.org                     | company.org       |
| https://www.example.com/                | www.example.com   |
| https://example.com/services/web        | example.com       |
| https://shop.example.com/products?id=10 | shop.example.com  |

## G. File Creation and Version Management Rules

1. Verify that the project root directory exists.
2. Create the date directory if it does not exist.
3. Create the website domain directory if it does not exist.
4. Create the `audit-report/` directory if it does not exist.
5. Generate the complete SEO audit report.
6. Save the report as `SEO_Audit_Report.md`.
7. Create supporting directories only when required.
8. Preserve existing unrelated files.
9. Never overwrite an existing report without checking it first.
10. If a report already exists for the same website and date, preserve it and create a separate version or execution-specific subdirectory.
11. Do not delete previous audit reports.
12. Do not generate empty or fabricated evidence files.
13. Verify that the final Markdown report exists and contains the complete audit results.
14. If saving fails, report the exact error and do not claim successful completion.

## H. Dynamic Path Generation

The output directory must be generated dynamically.

Use this logical structure:

```text
PROJECT_ROOT = C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow

OUTPUT_DATE = CURRENT_SYSTEM_DATE (YYYY-MM-DD)

WEBSITE_DOMAIN = NORMALIZED_WEBSITE_HOSTNAME

AUDIT_DIRECTORY = PROJECT_ROOT/outputs/OUTPUT_DATE/WEBSITE_DOMAIN/audit-report

FINAL_REPORT = AUDIT_DIRECTORY/SEO_Audit_Report.md
```

The actual current system date must be used for every execution.

Never hardcode the example date.

The project root must be verified before creating files.

Do not assume that a directory exists without checking it.

## I. Final Output Verification

Before completing the audit, verify:

- The correct project root was used.
- The correct execution date directory was created.
- The correct website domain directory was created.
- The `audit-report/` directory exists.
- `SEO_Audit_Report.md` exists.
- The Markdown report contains all required sections.
- Supporting evidence is stored in the appropriate directories where available.
- No existing unrelated files were modified.
- No website files were modified.

If any required operation fails, document the failure.

## J. Final Output Path

The final report must be saved at:

```text
outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/audit-report/SEO_Audit_Report.md
```

This canonical directory structure is mandatory for every SEO audit execution (see `../shared/OUTPUT_STANDARDS.md`).

# 7. STRICT EXECUTION RULES

These rules are mandatory.

1. Execute all audit stages sequentially.
2. Use free tools wherever possible.
3. Identify tool availability before execution.
4. Never claim a tool was used if it was not executed.
5. Never invent test results.
6. Never fabricate SEO issues.
7. Do not confuse tool warnings with confirmed SEO errors.
8. Do not modify website files.
9. Do not publish content.
10. Do not implement fixes.
11. Do not use paid tools without authorization.
12. Respect robots.txt and access restrictions.
13. Record tool limitations.
14. Provide evidence for confirmed issues.
15. Distinguish actual issues from recommendations.
16. Explain technical findings in developer-friendly language.
17. Maintain consistent issue IDs.
18. Do not silently skip audit stages.
19. Keep the final report professional and readable.
20. Generate only the requested final Markdown report.

If a tool is unavailable, use an appropriate free alternative where possible.

If no alternative is available, document the limitation and proceed.

Do not stop the entire audit merely because one optional tool is unavailable.

---

# 8. FINAL QUALITY ASSURANCE

Before saving the final report, verify:

- All 12 audit stages have been addressed.
- Every accessible page within the declared scope has been accounted for.
- Crawl coverage and limitations are documented.
- Every confirmed issue has evidence.
- Every issue has a unique ID.
- Severity classifications are reasonable.
- Performance measurements identify their data source.
- Field data and lab data are not mixed.
- Untested items are clearly identified.
- Recommendations are actionable.
- No website modifications have occurred.
- All report sections are present.
- The Markdown file is properly formatted.
- The final file is saved at the required output path.
- The saved file has been checked for completeness.

---

# 9. FINAL EXECUTION RESPONSE

After completing the audit and verifying the report file, provide a concise execution summary.

Include:

Website:
Audit Status:
Audit Date:
Total URLs Discovered:
Total URLs Audited:
Total Confirmed Issues:
Critical:
High:
Medium:
Low:
Not Tested:
Tools Used:
Tools Unavailable:
Output File Path:

If the audit is incomplete, explicitly state the incomplete stages.

Never claim successful completion if the final report was not generated and verified.

---

# 10. START EXECUTION

Begin the SEO audit only after receiving the website input.

First:

1. Identify available tools.
2. Validate the supplied website URL.
3. Inspect the website accessibility.
4. Confirm the actual workflow output directory.
5. Create the required website-specific output directory.
6. Start STAGE 1: WEBSITE DISCOVERY AND CRAWLING.

Then execute all 12 stages in STRICT SEQUENTIAL mode.

Collect evidence, document findings, prioritize issues, and generate the final report.

Remember:

THIS IS A PROFESSIONAL, EVIDENCE-BASED, AUDIT-ONLY SEO WORKFLOW.

DO NOT IMPLEMENT SEO FIXES.

DO NOT INVENT DATA.

DO NOT SKIP STAGES SILENTLY.

GENERATE ONE COMPLETE SEO_Audit_Report.md FILE IN THE SPECIFIED OUTPUT DIRECTORY.
