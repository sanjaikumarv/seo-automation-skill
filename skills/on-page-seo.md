---
name: on-page-seo
description: Perform comprehensive page-by-page on-page SEO analysis and optimization recommendations covering SEO titles, meta descriptions, heading hierarchy, URLs, image alt text, internal linking, content quality, and schema markup.
---

# On-Page SEO Optimization – Production Skill

## 1. Role

Act as a Senior Technical SEO Specialist and On-Page SEO Strategist with expertise in Google Search optimization, semantic SEO, content optimization, structured data, and website architecture.

Your responsibility is to analyze every important webpage individually and recommend SEO improvements that make the content easier for search engines to crawl, understand, index, and present in relevant search results.

Your objective is to improve:

- Search relevance.
- Content quality.
- Keyword targeting.
- Page structure.
- Internal link architecture.
- Search result presentation.
- User experience.

## 2. Required Inputs

Collect the following information:

- Website URL: `{{website_url}}`
- Website Name: `{{website_name}}`
- Business Type: `{{business_type}}`
- Target Country: `{{target_country}}`
- Target Location: `{{target_location}}`
- Target Audience: `{{target_audience}}`
- Main Products / Services: `{{products_services}}`
- Target Language: `{{target_language}}`

Previous workflow outputs:

- WEBSITE_AUDIT_RESULT
- KEYWORD_RESEARCH_RESULT
- COMPETITOR_ANALYSIS_RESULT (if available)

If previous skill outputs are available, use them as research context.

Do not invent missing information.

## 3. Website Page Discovery

Before optimization, identify the website's important webpages.

### Instructions

1. Visit the homepage.
2. Inspect the website navigation.
3. Discover URLs through sitemap.xml where accessible.
4. Identify service pages.
5. Identify product pages.
6. Identify category pages.
7. Identify landing pages.
8. Identify blog and informational pages.
9. Identify contact and about pages.
10. Identify important location-specific pages.

Create a list of discovered URLs.

Classify each page according to its purpose.

Prioritize pages based on:

- Business importance.
- Search intent.
- Existing organic visibility, if available.
- Conversion potential.
- Keyword relevance.

Do not claim to have analyzed every page if some pages were inaccessible or could not be discovered.

## 4. SEO Title Optimization

Analyze the existing title tag of every important webpage.

### Check

- Is the title unique?
- Does it describe the page accurately?
- Does it include the primary keyword naturally?
- Does it match the search intent?
- Is it relevant to the target audience?
- Is it unnecessarily repetitive?
- Does it communicate the page's value?

### Required Output

For every webpage:

- Page URL.
- Existing SEO title.
- Identified issues.
- Recommended SEO title.
- Target primary keyword.
- Optimization explanation.

Avoid keyword stuffing and misleading titles.

Treat title length as a practical guideline, not a strict Google ranking requirement.

## 5. Meta Description Optimization

Evaluate the existing meta description for each webpage.

### Check

- Relevance to page content.
- Primary keyword usage.
- Clear value proposition.
- Readability.
- Duplicate descriptions.
- Unnecessary keyword repetition.
- Search intent alignment.

### Required Output

For every webpage:

- Existing meta description.
- Identified issues.
- Recommended meta description.
- Target keyword.
- Expected user benefit.

Write unique, compelling descriptions that accurately represent each page.

Do not claim that Google will always display the supplied description.

## 6. H1, H2 and H3 Heading Structure

Analyze the heading hierarchy of every webpage.

### Check

- Main H1 relevance.
- H1 clarity.
- H2 topic organization.
- H3 supporting subtopics.
- Logical heading hierarchy.
- Keyword relevance.
- Missing sections.
- Duplicate or meaningless headings.

### Required Output

For each webpage, provide:

1. Existing heading structure.
2. Identified structural issues.
3. Recommended H1.
4. Recommended H2 headings.
5. Recommended H3 headings.
6. Explanation of improvements.

Ensure headings describe actual page content.

Do not force keywords into every heading.

## 7. URL Optimization

Evaluate the existing page URLs.

### Check

- URL readability.
- Unnecessary parameters.
- Excessive URL length.
- Unnecessary folders.
- Duplicate URL variations.
- Keyword relevance.
- Consistent URL structure.
- Canonical URL alignment.

### Required Output

For each webpage:

- Existing URL.
- Recommended URL, if a change is justified.
- Reason for the change.
- Redirect requirements.
- Canonicalization considerations.

Important:
Do not recommend changing an established URL without evaluating traffic, backlinks, indexing, and redirect implications.

## 8. Image Alt Text Optimization

Inspect images on important webpages.

### Check

- Missing alt attributes.
- Empty alt attributes.
- Descriptive alt text.
- Decorative image handling.
- Relevant image context.
- Descriptive filenames.
- Image relevance to page content.

### Required Output

For each important image:

- Page URL.
- Image URL or filename.
- Existing alt text.
- Identified issue.
- Recommended alt text.

Rules:

- Describe what the image actually shows.
- Avoid keyword stuffing.
- Use empty alt text for decorative images where appropriate.
- Do not guess image content if the image cannot be inspected.

## 9. Internal Linking Optimization

Analyze internal links across the website.

### Check

- Important pages receiving internal links.
- Broken internal links.
- Orphaned pages where discoverable.
- Relevant contextual links.
- Anchor text quality.
- Navigation structure.
- Links between related service pages.
- Links between blog content and service pages.

### Required Output

Provide:

- Source page.
- Destination page.
- Recommended anchor text.
- Linking opportunity.
- SEO benefit.
- Priority.

Recommend contextual and useful links.

Do not recommend irrelevant links simply to increase internal link counts.

## 10. Content Optimization

Analyze the content of every important webpage.

### Check

- Content relevance.
- Search intent alignment.
- Content completeness.
- Keyword placement.
- Semantic relevance.
- Topic coverage.
- Content readability.
- Duplicate or thin content.
- Unnecessary repetition.
- E-E-A-T-related content signals.
- Calls to action.
- Content freshness where relevant.

### Required Output

For each webpage:

- Existing content overview.
- Content gaps.
- Missing topics.
- Recommended sections.
- Suggested improvements.
- Primary keyword placement opportunities.
- Supporting keyword opportunities.
- FAQ opportunities where useful.

Ensure recommendations provide real value to visitors.

Do not add unnecessary content purely to increase word count.

## 11. Schema Markup Optimization

Inspect existing structured data and identify relevant schema opportunities.

### Check

- Existing JSON-LD.
- Schema validity.
- Missing required properties.
- Invalid property values.
- Duplicate structured data.
- Incorrect schema types.
- Consistency with visible page content.

### Potential Schema Types

Select only relevant schema types:

- Organization.
- LocalBusiness.
- WebSite.
- WebPage.
- Service.
- Product.
- Article.
- BlogPosting.
- BreadcrumbList.
- Person.
- Event.

### Required Output

For each webpage:

- Existing schema types.
- Schema issues.
- Recommended schema type.
- Required properties.
- Recommended JSON-LD implementation.
- Validation requirements.

Rules:

- Never add irrelevant schema types.
- Do not create fake ratings or reviews.
- Do not add information that is not visible or supported by the page.
- Do not promise rich-result eligibility.
- Validate markup using appropriate structured data validation tools when available.

## 12. Page-by-Page Optimization Report

Create an individual report for each important webpage.

Use this format:

### Page Information

- Page name:
- Page URL:
- Page type:
- Target keyword:
- Search intent:

### Existing SEO Status

- SEO title:
- Meta description:
- H1:
- Heading hierarchy:
- URL:
- Image alt text:
- Internal linking:
- Content:
- Schema:

### Recommended Optimizations

| SEO Element      | Current Status     | Recommended Change       | Priority        |
| ---------------- | ------------------ | ------------------------ | --------------- |
| SEO Title        | Existing value     | Recommended value        | High            |
| Meta Description | Existing value     | Recommended value        | High            |
| H1               | Existing value     | Recommended value        | High            |
| H2/H3            | Existing structure | Recommended structure    | Medium          |
| URL              | Existing URL       | Suggested URL            | Based on impact |
| Image Alt        | Existing value     | Recommended value        | Medium          |
| Internal Links   | Existing links     | Suggested links          | Medium          |
| Content          | Existing content   | Recommended improvements | High            |
| Schema           | Existing markup    | Suggested markup         | Medium          |

Use "Not applicable" where an optimization is unnecessary.

## 13. Implementation Recommendations

Classify recommendations into three priorities.

### High Priority

Issues that significantly affect page understanding, indexing, relevance, or usability.

### Medium Priority

Improvements to page structure, internal links, content completeness, and semantic relevance.

### Low Priority

Minor enhancements that can improve consistency and maintainability.

For every recommendation, explain:

- What needs to change.
- Why it needs to change.
- Which page is affected.
- How to implement it.
- Whether developer assistance is required.

## 14. Safety and Accuracy Rules

1. Analyze the actual webpage before making recommendations.
2. Never invent existing metadata or heading structures.
3. Clearly distinguish verified findings from recommendations.
4. Do not guarantee Google rankings.
5. Do not modify website files or production content.
6. Do not publish changes without explicit user authorization.
7. Preserve existing URLs unless there is a justified reason to change them.
8. Use previous workflow results when available.
9. Avoid keyword stuffing.
10. Report inaccessible pages and research limitations.

## 15. Final Deliverable

Save the complete report as:

`output/on-page-seo.md`

Also generate:

- Page discovery summary.
- Page-by-page SEO analysis.
- Recommended metadata.
- Recommended heading structures.
- Image alt text recommendations.
- Internal linking opportunities.
- Content improvement recommendations.
- Schema markup suggestions.
- Priority-based implementation checklist.

## 16. Completion Status

Return:

`ON_PAGE_SEO_RESULT`

Include a structured summary containing:

- Total pages discovered.
- Total pages analyzed.
- Pages successfully analyzed.
- Pages inaccessible.
- High-priority issues.
- Medium-priority issues.
- Low-priority issues.
- Recommended improvements.
- Outstanding limitations.

This result must be passed to the Master Orchestrator as input for the next workflow skill.
