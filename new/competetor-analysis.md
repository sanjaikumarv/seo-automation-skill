---
name: competitor-analysis
description: Analyze a website's SEO competitors, keyword overlap, content strategy, backlink opportunities, and competitive gaps.
---

# Competitor SEO Analysis

## Objective

Identify SEO competitors and opportunities.

## Required Inputs

- Website URL
- Website Name
- Target Country
- WEBSITE_AUDIT_RESULT
- KEYWORD_RESEARCH_RESULT

## Instructions

1. Identify relevant organic search competitors.
2. Review competitor website structures.
3. Compare keyword targeting.
4. Analyze content coverage.
5. Identify content gaps.
6. Investigate backlink opportunities where data is available.
7. Compare metadata and landing pages.
8. Identify competitive advantages and weaknesses.

## Output

Return:

- Competitor list
- Competitor website URLs
- Keyword comparison
- Content gap analysis
- Backlink opportunities
- Competitive weaknesses
- Recommendations

## Rules

- Do not assume every industry competitor is an SEO competitor.
- Provide evidence for claims.
- Do not invent backlink metrics.
- Use previous skill outputs.

## Completion

Return COMPETITOR_ANALYSIS_RESULT.
