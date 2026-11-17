---
name: keyword-research
description: Research relevant SEO keywords, search intent, keyword opportunities, and content gaps for a supplied website and target market.
---

# Keyword Research

## Objective

Identify valuable keywords for the website.

## Required Inputs

- Website URL
- Website Name
- Target Country
- WEBSITE_AUDIT_RESULT

## Instructions

1. Understand the website's products and services.
2. Identify primary keyword opportunities.
3. Identify secondary keywords.
4. Identify long-tail keywords.
5. Classify search intent:
   - Informational
   - Navigational
   - Commercial
   - Transactional
6. Research keyword difficulty and search volume
   when reliable data is available.
7. Identify content gaps.
8. Group keywords by topic.

## Output

Return:

- Primary keywords
- Secondary keywords
- Long-tail keywords
- Search intent
- Search volume (if verified)
- Keyword difficulty (if verified)
- Content opportunities
- Recommended keyword mapping

## Rules

- Never fabricate search volume.
- Cite data sources.
- Separate estimated metrics from verified metrics.
- Use WEBSITE_AUDIT_RESULT as context.

## Completion

Return KEYWORD_RESEARCH_RESULT.
