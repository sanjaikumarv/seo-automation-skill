---
name: keyword-research
description: Conduct comprehensive SEO keyword research to discover and prioritize primary, secondary, long-tail, and local SEO keywords with search intent classification, using previous website audit data.
---

# Skill: SEO Keyword Research & Intent Mapping

## 1. Role & Objective

Act as a Senior SEO Strategist and Keyword Research Specialist.

Your responsibility is to discover high-value search queries that prospective customers use on Google, classify their search intent, and map these opportunities to the website's service offerings and discovered pages.

---

## 2. Input Parameters & Upstream Prerequisites

1. **User Parameters:**
   - `website_url`: Target website URL.
   - `website_name`: Brand name.
   - `target_country`: Target geographic market.
   - `target_location`: City / region (for local queries).
   - `target_audience`: Target customer persona.
2. **Upstream Prerequisite Data:**
   - **File:** `outputs/seo-audit-report.md`
   - *Requirement:* You must read `outputs/seo-audit-report.md` before starting to extract the *Discovered Pages Catalog* and identified business services.

---

## 3. Research Scope

1. **Primary Keywords:** Core high-intent terms representing primary products or services.
2. **Secondary & Supporting Keywords:** Sub-services, specific tech stacks, platforms, and semantic synonyms.
3. **Long-Tail & Problem-Solving Queries:** Specific multi-word phrases and question queries asked by buyers.
4. **Local SEO Keywords:** Geographically targeted queries (`[Service] in [City]`, `[Service] near me`).
5. **Search Intent Classification:**
   - *Informational:* Seeking knowledge, guides, or answers.
   - *Navigational:* Looking for a specific brand or URL.
   - *Commercial Investigation:* Comparing options, features, pricing, or reviews.
   - *Transactional:* Ready to purchase, request a quote, or contact.
6. **Keyword-to-Page Mapping:** Assign primary and secondary target keywords directly to the discovered pages from `outputs/seo-audit-report.md`.

---

## 4. Output Deliverable

Save the complete keyword strategy report to:
- **File:** `outputs/keyword-research-report.md`
- **Context Variable:** `KEYWORD_RESEARCH_RESULT`

The report must include:
- Executive Strategy Overview.
- Primary Keywords Matrix (Keyword, Intent, Est. Demand, Priority).
- Secondary & Long-Tail Opportunities Table.
- Local SEO Keyword Matrix.
- **Keyword-to-Page Mapping Table** (Discovered URL, Primary Target Keyword, Secondary Keywords, Search Intent).
- Content Gap & New Page Recommendations.

---

## 5. Rules

1. Never fabricate exact search volume numbers. Use estimated demand indicators (High / Medium / Low) when third-party API data is unavailable.
2. Avoid assigning the same primary keyword to multiple pages (prevent cannibalization).
3. The keyword-to-page mapping must directly feed into the downstream `content-generation` skill.
