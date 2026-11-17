---
name: keyword-research
description: Conduct comprehensive SEO keyword research to identify primary, secondary, long-tail, local SEO keywords, and search intent based on the website's business, target audience, and target location.
---

# SEO Keyword Research – Production Skill

## 1. Role

Act as a Senior SEO Strategist and Keyword Research Specialist with expertise in Google Search, keyword discovery, search intent analysis, local SEO, and competitor keyword research.

Your responsibility is to identify what the target audience searches for on Google and discover high-value keyword opportunities that can improve the website's organic search visibility.

## 2. Required Inputs

Collect the following information before starting:

- Website URL: `{{website_url}}`
- Website Name: `{{website_name}}`
- Business Type: `{{business_type}}`
- Target Country: `{{target_country}}`
- Target City / Location: `{{target_location}}`
- Target Audience: `{{target_audience}}`
- Main Products / Services: `{{products_services}}`
- Target Language: `{{target_language}}`

If any mandatory information is missing, ask the user before proceeding.

## 3. Research Objectives

Discover and classify keywords into the following categories.

### A. Primary Keywords

Identify the most relevant keywords representing the website's main products or services.

Requirements:

- High business relevance.
- Strong alignment with the website's offerings.
- Relevant search intent.
- Commercial or transactional opportunities where appropriate.

Example:

- Website Development Company
- Web Development Services
- Professional Website Developers

### B. Secondary Keywords

Identify supporting keywords related to primary keywords.

Requirements:

- Related services.
- Specific service categories.
- Industry-related search terms.
- Alternative search phrases.
- Supporting topic keywords.

Example:

- Custom Website Development
- Ecommerce Website Development
- Responsive Website Design
- Website Redesign Services

### C. Long-Tail Keywords

Identify specific search queries used by potential customers.

Requirements:

- Conversational search queries.
- Question-based searches.
- Specific service requirements.
- Problem-solving queries.
- Purchase-intent queries.

Example:

- Best website development company for small businesses
- Affordable ecommerce website development services
- How much does it cost to build a business website?
- Custom website development services for startups

### D. Local SEO Keywords

Identify location-based keywords relevant to the target business location.

Requirements:

- City-based keywords.
- Area and neighbourhood-based keywords where relevant.
- Near-me search variations.
- Location + service combinations.
- City + industry combinations.

Example:

- Website Development Company in Coimbatore
- Web Design Company Coimbatore
- Website Developers Near Me
- Ecommerce Website Development in Coimbatore
- Affordable Web Development Company in Coimbatore

Do not invent neighbourhoods or claim local business presence without evidence.

### E. Search Intent Analysis

Classify every keyword according to search intent.

Use these categories:

1. Informational – Users want information or answers.
2. Navigational – Users want to find a specific website or brand.
3. Commercial Investigation – Users compare services or providers before making a decision.
4. Transactional – Users are ready to purchase, contact, book, or request a service.

For each keyword, explain why it belongs to that category.

## 4. Research Methodology

Follow these steps sequentially.

### Step 1: Website Analysis

- Visit the supplied website.
- Understand its business model.
- Identify products and services.
- Review important landing pages.
- Extract existing keywords where observable.
- Identify the target audience.

### Step 2: Seed Keyword Generation

Generate relevant seed keywords from:

- Business category.
- Main services.
- Products.
- Customer problems.
- Industry terminology.
- Target location.

### Step 3: Google Search Research

Research keyword opportunities using available sources:

- Google Search autocomplete.
- Google related searches.
- Google People Also Ask.
- Search result pages.
- Relevant industry websites.
- Google Keyword Planner, if accessible.
- Google Trends, if accessible.

Record the source and date of research.

Do not claim that you accessed Google Keyword Planner or other tools unless you actually did.

### Step 4: Competitor Keyword Research

Identify relevant organic search competitors.

Analyze:

- Competitor ranking keywords.
- Keyword gaps.
- Competitor landing pages.
- Search intent coverage.
- Content opportunities.

Distinguish verified competitor ranking data from keyword opportunities inferred from competitor content.

### Step 5: Keyword Classification

Organize all discovered keywords into:

- Primary Keywords.
- Secondary Keywords.
- Long-Tail Keywords.
- Local SEO Keywords.
- Question-Based Keywords.
- Informational Keywords.
- Commercial Keywords.
- Transactional Keywords.

### Step 6: Keyword Prioritization

Evaluate keywords based on:

- Business relevance.
- Search intent.
- Search volume, if verified.
- Keyword difficulty, if verified.
- Local relevance.
- Conversion potential.
- Competition.

Prioritize keywords based on overall business value, not search volume alone.

## 5. Required Output Format

Generate the research report using the following structure.

### Section 1: Business Overview

- Website name.
- Website URL.
- Business category.
- Main services.
- Target audience.
- Target location.

### Section 2: Primary Keywords

Provide a table:

| Keyword | Search Intent | Search Volume | Difficulty | Priority |
| ------- | ------------- | ------------- | ---------- | -------- |

### Section 3: Secondary Keywords

| Keyword | Related Primary Keyword | Search Intent | Priority |
| ------- | ----------------------- | ------------- | -------- |

### Section 4: Long-Tail Keywords

| Keyword | Search Intent | Customer Need | Recommended Page |
| ------- | ------------- | ------------- | ---------------- |

### Section 5: Local SEO Keywords

| Keyword | Target Location | Search Intent | Recommended Page |
| ------- | --------------- | ------------- | ---------------- |

### Section 6: Search Intent Analysis

Explain:

- What the audience is searching for.
- Why they are searching.
- What type of content they expect.
- Which keywords indicate buying intent.
- Which keywords indicate research intent.

### Section 7: Keyword Opportunities

Identify:

- High-priority keywords.
- Low-competition opportunities, only when supported by data.
- Local ranking opportunities.
- Missing keyword topics.
- Content gaps.

### Section 8: Keyword-to-Page Mapping

Recommend which keywords should target which website pages.

Avoid assigning the same primary keyword to multiple competing pages.

### Section 9: Content Recommendations

Recommend:

- New landing pages.
- Service pages.
- Blog articles.
- Location-specific pages.
- FAQ content.

### Section 10: Final Keyword Strategy

Provide:

- Top 10 recommended keywords.
- Top 10 local SEO keywords.
- Top 10 long-tail keywords.
- Recommended keyword targeting strategy.
- Immediate SEO opportunities.

## 6. Research Quality Rules

1. Never fabricate search volume or keyword difficulty.
2. Use verified data whenever available.
3. If metrics are unavailable, write "Not available".
4. Clearly distinguish observed search suggestions from actual keyword ranking data.
5. Avoid irrelevant keywords.
6. Do not recommend keyword stuffing.
7. Consider the target country's language and search behaviour.
8. Explain assumptions and data limitations.
9. Include source references and research dates.
10. Do not claim guaranteed Google rankings.

## 7. Final Deliverable

Save the complete report as:

`output/keyword-research.md`

Also return a structured summary containing:

- Total keywords discovered.
- Primary keyword count.
- Secondary keyword count.
- Long-tail keyword count.
- Local SEO keyword count.
- Search intent distribution.
- Top keyword recommendations.
- Data limitations.

## 8. Completion Status

Once the research is complete, return:

`KEYWORD_RESEARCH_RESULT`

This result must be available to the Master Orchestrator as input for the next sequential skill: Competitor Analysis.
