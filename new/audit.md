---
name: website-audit
description: Perform a comprehensive technical SEO audit of a website, including crawlability, indexability, broken links, performance, mobile usability, metadata, and technical SEO issues.
---

# Website Technical SEO Audit

## Objective

Perform a comprehensive technical SEO audit.

## Required Inputs

- Website URL
- Website Name
- Target Country

## Instructions

1. Inspect the supplied website.
2. Review robots.txt and sitemap.xml where accessible.
3. Inspect page titles and meta descriptions.
4. Check canonical URLs.
5. Identify broken internal and external links where verifiable.
6. Review heading structure.
7. Check mobile usability.
8. Investigate page speed and Core Web Vitals using available tools.
9. Review indexing and crawlability.
10. Identify duplicate content and technical issues.

## Output

Return:

- Website overview
- Technical SEO issues
- Broken links
- Indexability issues
- Performance issues
- Mobile usability findings
- Priority of each issue
- Recommended fixes

## Rules

- Never invent audit results.
- Distinguish verified findings from potential issues.
- Include evidence and URLs.
- Mention limitations if a page cannot be accessed.

## Completion

Return a structured report named WEBSITE_AUDIT_RESULT.
