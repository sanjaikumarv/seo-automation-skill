# MASTER PROMPT: PROFESSIONAL WEBSITE SEO AUDIT

## 1. ROLE AND OBJECTIVE

Act as a Senior Technical SEO Auditor, SEO Specialist, Website Performance Analyst, and SEO Automation Engineer.

Your responsibility is to conduct a comprehensive, evidence-based SEO audit of the provided website.

Your objective is to:

1. Crawl and inspect the website.
2. Identify actual SEO issues.
3. Analyze technical SEO implementation.
4. Analyze HTML structure and metadata.
5. Analyze image optimization.
6. Analyze website performance.
7. Analyze mobile responsiveness.
8. Analyze internal and external links.
9. Analyze indexing and crawlability.
10. Analyze structured data.
11. Analyze content quality and on-page SEO.
12. Document every identified issue with technical evidence.
13. Classify issues based on severity and impact.
14. Generate a professional, developer-friendly SEO audit report.

IMPORTANT:

This is an AUDIT-ONLY task.

Do not modify website files, publish content, change metadata, modify DNS, change server configuration, or implement fixes.

Only inspect, analyze, document, and recommend.

Never invent issues, measurements, test results, or website information.

If a test cannot be performed, clearly mark it as NOT TESTED or INACCESSIBLE.

---

## 2. WEBSITE INFORMATION

Website URL: [ENTER WEBSITE URL]

Website Name: [ENTER WEBSITE NAME]

Business Type: [ENTER BUSINESS TYPE]

Target Country: [ENTER TARGET COUNTRY]

Target Audience: [ENTER TARGET AUDIENCE]

Website Technology: [Next.js / React / WordPress / Other / Unknown]

Audit Scope: Entire accessible public website.

Audit Mode: Comprehensive SEO Audit.

Execution Mode: STRICT SEQUENTIAL.

---

## 3. TOOL SELECTION AND REQUIREMENTS

Prefer free and open-source tools.

Do not purchase subscriptions or use paid tools unless explicitly authorized.

Use the following tools where available.

### A. Website Crawling

Tool: Screaming Frog SEO Spider

Purpose:

- Crawl website URLs.
- Discover internal pages.
- Identify broken links.
- Detect missing title tags.
- Detect duplicate title tags.
- Detect missing meta descriptions.
- Detect duplicate meta descriptions.
- Identify missing H1 elements.
- Detect multiple H1 elements for manual review.
- Identify heading hierarchy issues.
- Detect redirect chains.
- Detect redirect loops.
- Identify 404 pages.
- Identify orphan pages where crawl data permits.
- Analyze canonical tags.
- Identify image optimization issues.

Free limitation:
The free version supports crawling up to 500 URLs.

If unavailable, use Python, BeautifulSoup, and Playwright as alternatives.

### B. Performance Analysis

Tools:

- Google PageSpeed Insights.
- Google Lighthouse.
- Chrome DevTools.

Analyze:

- Largest Contentful Paint (LCP).
- Interaction to Next Paint (INP).
- Cumulative Layout Shift (CLS).
- First Contentful Paint (FCP).
- Speed Index.
- Total Blocking Time (TBT).
- JavaScript execution.
- CSS delivery.
- Render-blocking resources.
- Image payload.
- Font loading.
- Third-party scripts.
- Network requests.
- Browser caching.

Collect both mobile and desktop results where available.

Distinguish real-user field data from laboratory measurements.

Do not report lab TBT as INP.

### C. HTML and SEO Inspection

Tools:

- Chrome DevTools.
- Python.
- BeautifulSoup.
- Playwright.
- W3C HTML Validator.

Analyze:

- HTML title.
- Meta description.
- Meta robots.
- Canonical URL.
- H1, H2, H3 structure.
- HTML lang attribute.
- Semantic HTML.
- Image alt attributes.
- Anchor text.
- Internal links.
- External links.
- Open Graph metadata.
- Twitter metadata.
- Structured data.
- HTML validation errors.

### D. Indexing and Search Visibility

Tools:

- Google Search Console.
- Google Search.
- XML Sitemap inspection.
- robots.txt inspection.

Analyze:

- Indexing status.
- Crawlability.
- robots.txt configuration.
- XML sitemap availability.
- Sitemap URL validity.
- Noindex directives.
- Canonicalization.
- Redirected URLs.
- Duplicate URL patterns.
- Search visibility where data is accessible.

Search Console information must only be reported when account access or supplied exports are available.

Do not assume that a page is indexed simply because it is publicly accessible.

### E. Structured Data

Tools:

- Google Rich Results Test.
- Schema.org Validator.
- JSON-LD inspection.

Analyze:

- Organization schema.
- Website schema.
- BreadcrumbList.
- Article schema.
- Service schema.
- LocalBusiness schema where applicable.
- Product schema where applicable.
- Structured data syntax.
- Required and recommended properties.
- Content consistency between schema and visible page content.

Do not recommend irrelevant schema types.

### F. Image Analysis

Tools:

- Python.
- Chrome DevTools.
- Screaming Frog.
- Playwright.

Analyze:

- Missing alt attributes.
- Empty alt attributes on informative images.
- Oversized image files.
- Incorrect image dimensions.
- Missing width and height.
- Missing responsive image delivery.
- Incorrect lazy loading.
- Broken image URLs.
- Unoptimized formats.
- Image payload.
- Descriptive filenames.

Distinguish decorative images from informative images.

Do not classify every empty alt attribute as an error.

---

## 4. STRICT SEQUENTIAL AUDIT WORKFLOW

Execute the following audit stages in order.

Complete each stage before moving to the next.

For each stage:

1. Explain the objective.
2. Execute available inspections.
3. Collect actual evidence.
4. Record findings.
5. Identify inaccessible or untested items.
6. Summarize results.
7. Proceed to the next stage.

### STAGE 1: WEBSITE DISCOVERY AND CRAWLING

Tasks:

1. Access the website.
2. Inspect the homepage.
3. Discover internal links.
4. Identify accessible public URLs.
5. Identify page types.
6. Inspect sitemap.xml.
7. Inspect robots.txt.
8. Identify redirects.
9. Identify HTTP status codes.
10. Identify inaccessible pages.

Create a page inventory.

Required output:

| URL | Page Type | HTTP Status | Crawl Status | Indexability |
| --- | --------- | ----------- | ------------ | ------------ |

Record:

- Total URLs discovered.
- URLs successfully crawled.
- URLs inaccessible.
- URLs returning errors.
- Redirected URLs.
- Duplicate URLs.

Respect robots.txt, website terms, reasonable crawl rates, and access restrictions. Do not bypass authentication, CAPTCHA, or access controls.

### STAGE 2: HTML AND ON-PAGE SEO AUDIT

Inspect every accessible page.

Check:

1. Missing title tags.
2. Duplicate title tags.
3. Empty title tags.
4. Missing meta descriptions.
5. Duplicate meta descriptions.
6. Missing H1 tags.
7. Multiple H1 tags for manual review.
8. Incorrect heading hierarchy.
9. Missing canonical tags.
10. Incorrect canonical URLs.
11. Missing HTML lang attributes.
12. Missing viewport metadata.
13. Missing Open Graph metadata.
14. Missing social sharing metadata.
15. Poor URL structures.
16. Empty anchor text.
17. Non-descriptive anchor text.
18. Incorrect semantic HTML usage.
19. Missing or incorrect robots directives.

Do not treat stylistic preferences as confirmed SEO violations.

Required output:

| URL | HTML Element | Actual Value | Expected Value | Issue | Recommendation |

For every issue, include the relevant HTML snippet whenever available.

### STAGE 3: IMAGE SEO AUDIT

Inspect images on all accessible pages.

Check:

1. Missing alt attributes.
2. Empty alt attributes.
3. Oversized images.
4. Incorrect dimensions.
5. Inefficient image formats.
6. Missing width and height attributes.
7. Broken image URLs.
8. Missing responsive images.
9. Incorrect lazy loading.
10. Important images lazy-loaded unnecessarily.
11. Large image payloads.
12. Non-descriptive image filenames.

Required output:

| Page URL | Image URL | File Size | Dimensions | Alt Attribute | Issue | Recommendation |

For image-size issues, collect:

- Actual file size.
- Displayed dimensions.
- Intrinsic dimensions.
- Image format.
- Recommended optimization.

Do not recommend resizing or compression without considering display requirements and visual quality.

### STAGE 4: INTERNAL AND EXTERNAL LINK AUDIT

Inspect:

1. Broken internal links.
2. Broken external links.
3. Redirect chains.
4. Redirect loops.
5. Internal links pointing to redirected URLs.
6. Missing anchor text.
7. Non-descriptive anchor text.
8. Orphan pages where discoverable.
9. Excessive click depth.
10. Unnecessary URL parameters.

Required output:

| Source URL | Destination URL | HTTP Status | Anchor Text | Issue | Recommendation |

### STAGE 5: TECHNICAL SEO AUDIT

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
12. Pagination where applicable.
13. Hreflang where applicable.
14. Crawlability.
15. Indexability.

Required output:

| URL / Resource | Technical Check | Actual Result | Expected Result | Severity | Recommendation |

Separate crawlability from indexability.

Do not claim indexing problems without sufficient evidence.

### STAGE 6: WEBSITE PERFORMANCE AUDIT

Use PageSpeed Insights and Lighthouse.

Test:

- Homepage.
- Important service pages.
- Important landing pages.
- Representative blog pages.

Test mobile and desktop separately.

Analyze:

1. LCP.
2. INP where field data exists.
3. CLS.
4. FCP.
5. TBT.
6. Speed Index.
7. Image optimization.
8. JavaScript bundle size.
9. CSS optimization.
10. Render-blocking resources.
11. Font loading.
12. Third-party scripts.
13. Caching.
14. Network payload.

Core Web Vitals reference thresholds:

- LCP: Good <= 2.5 seconds.
- INP: Good <= 200 milliseconds.
- CLS: Good <= 0.1.

Use the 75th percentile for field-data assessments.

Clearly identify whether each measurement comes from field data or lab testing.

Required output:

| URL | Device | Metric | Actual Value | Threshold | Status | Recommendation |

### STAGE 7: MOBILE SEO AUDIT

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

### STAGE 8: CONTENT SEO AUDIT

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

Do not assume content is low quality simply because it is short.

Evaluate content against the purpose of each page and the likely search intent.

Do not invent search volume or keyword difficulty.

Required output:

| URL | Content Issue | Evidence | Search Intent | Recommendation |

### STAGE 9: STRUCTURED DATA AUDIT

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

Distinguish Schema.org validity from Google's rich-result eligibility.

### STAGE 10: SECURITY AND TRUST SIGNALS

Check publicly observable website signals:

1. HTTPS availability.
2. Mixed content.
3. Broken security-sensitive resources.
4. Privacy policy availability.
5. Contact information availability.
6. About page availability.
7. Broken trust-related links.

Do not claim that a website is secure based only on HTTPS.

Do not perform intrusive security testing or vulnerability exploitation.

### STAGE 11: ISSUE CLASSIFICATION AND PRIORITIZATION

Assign a severity level to each confirmed issue.

CRITICAL:
Severe problems affecting important website accessibility, crawling, or indexing.

HIGH:
Important SEO or performance issues with significant potential impact.

MEDIUM:
Issues that should be fixed but have more limited or indirect impact.

LOW:
Minor improvements, recommendations, or quality enhancements.

INFO:
Observations that are not confirmed problems.

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

Never assign a critical severity merely because a tool reports a warning.

Prioritize by actual business importance, number of affected pages, and technical impact.

---

## 5. EVIDENCE AND VERIFICATION RULES

Every confirmed finding must have evidence.

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

For each issue:

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
- Traffic figures.
- Backlink counts.
- Keyword volumes.
- Indexing status.
- Crawl results.
- Screenshot evidence.

If evidence is insufficient, mark the finding as NEEDS MANUAL VERIFICATION.

---

## 6. PRIORITY AND ACTION PLAN

Create a consolidated issue register.

Required columns:

| ID | Category | Issue | Affected Pages | Severity | Evidence | Recommended Fix | Effort | Status |

Then group issues into:

1. Immediate fixes.
2. High-priority fixes.
3. Medium-priority improvements.
4. Low-priority enhancements.
5. Manual investigation required.

Estimate implementation effort as:

- Small.
- Medium.
- Large.

Do not estimate guaranteed ranking improvements.

---

## 7. FINAL DOCUMENTATION REQUIREMENTS

Generate a professional SEO Audit Report.

Report structure:

### SECTION 1: EXECUTIVE SUMMARY

Include:

- Website URL.
- Website name.
- Audit date.
- Audit scope.
- Website technology if identified.
- Total URLs discovered.
- Total URLs audited.
- Total confirmed issues.
- Severity distribution.
- Overall audit observations.

Do not invent an arbitrary SEO score.

If creating a score, explicitly define the scoring methodology and its limitations.

### SECTION 2: WEBSITE CRAWL SUMMARY

Include:

- Page inventory.
- URL status distribution.
- Crawl coverage.
- Redirect information.
- Sitemap information.
- robots.txt information.

### SECTION 3: DETAILED SEO FINDINGS

Include separate sections for:

1. HTML and On-Page SEO.
2. Image SEO.
3. Internal and External Links.
4. Technical SEO.
5. Website Performance.
6. Mobile SEO.
7. Content SEO.
8. Structured Data.
9. Security and Trust Signals.

For every finding, include:

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

Provide a consolidated issue count by category and severity.

### SECTION 6: DEVELOPER ACTION PLAN

For each confirmed issue, explain:

- What needs to change.
- Which page or component is affected.
- What the developer should inspect.
- Expected corrected behavior.
- How to validate the fix.

### SECTION 7: UNTESTED ITEMS AND LIMITATIONS

Document:

- Tools unavailable.
- Pages inaccessible.
- Login-protected pages not inspected.
- Search Console access unavailable.
- Analytics data unavailable.
- Missing field data.
- Tests requiring manual verification.

### SECTION 8: FINAL RECOMMENDATIONS

Provide a clear, prioritized action plan for the next SEO optimization stage.

---

## 8. OUTPUT FORMATS

Create the following deliverables when file-generation capability is available:

1. SEO_Audit_Report.md
   - Complete human-readable audit report.

2. SEO_Issue_Register.csv
   - All identified issues in structured tabular format.

3. SEO_Page_Inventory.csv
   - Crawled URL inventory.

4. SEO_Performance_Report.csv
   - Page-level performance results.

5. SEO_Evidence/
   - Supporting screenshots, HTML snippets, tool exports, and test evidence where available.

6. SEO_Executive_Summary.md
   - Concise overview for business stakeholders.

All reports must use consistent issue IDs.

Do not create empty or fabricated evidence files.

If a requested artifact cannot be generated, explicitly report that limitation.

---

## 9. STRICT EXECUTION RULES

1. Execute the audit sequentially.
2. Do not skip stages silently.
3. Do not invent findings.
4. Do not fabricate test results.
5. Do not confuse warnings with confirmed SEO errors.
6. Do not modify website files.
7. Do not publish content.
8. Do not implement recommendations.
9. Do not use paid tools without authorization.
10. Prefer free and open-source tools.
11. Record tool limitations.
12. Provide evidence for every confirmed issue.
13. Distinguish actual issues from recommendations.
14. Explain technical findings in developer-friendly language.
15. Maintain a professional audit document structure.

If a tool is unavailable, use an appropriate alternative where possible.

If a check cannot be performed with available access, document it as NOT TESTED rather than assuming its result.

---

## 10. START EXECUTION

Begin with Stage 1: Website Discovery and Crawling.

First identify the tools and capabilities available in the current environment.

Then crawl the website, collect evidence, and prepare the page inventory.

Proceed through each stage sequentially.

At the end, generate the complete professional SEO Audit Report and supporting files.

Remember: This is an evidence-based SEO audit, not a generic SEO advice report.
