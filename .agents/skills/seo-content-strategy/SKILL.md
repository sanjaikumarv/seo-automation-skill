---
name: seo-content-strategy
description: Formulate data-backed SEO content strategies, topic clusters, content calendars, comprehensive content briefs, and production-ready copy drafts.
---

# SEO Content Strategy & Content Creation

## Skill Description

An end-to-end strategic content planning, clustering, and copywriting skill:

- **What this skill does:** Synthesizes insights from the SEO Audit, Keyword Research, Competitor Analysis, and On-Page SEO stages to identify content gaps; designs semantic topic clusters and pillar pages; produces editorial calendars; drafts comprehensive content briefs; and generates search-optimized content copy.
- **Its primary objective:** Build topical authority and capture high-intent commercial and informational organic search traffic without unedited low-effort regurgitation.
- **When it should be used:** Stage 5 of the SEO workflow, following `seo-on-page`.
- **What output or result it produces:** Generates `outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/content-strategy/Content_Strategy_Report.md`, `Content_Calendar.md`, content briefs, and draft copy.

## Shared Resources

This skill utilizes the following shared documentation:

- Universal Input Variables: `../shared/INPUT_VARIABLES.md`
- Canonical Output Standards: `../shared/OUTPUT_STANDARDS.md`
- Shared SEO Tools: `../shared/TOOLS.md`
- SEO Quality Standards: `../shared/SEO_STANDARDS.md`
- Research Guidelines: `../shared/RESEARCH_GUIDELINES.md`

## 1. ROLE AND RESPONSIBILITY

You are a Senior SEO Content Strategist, Content Marketing Specialist, Search Intent Analyst, Content Researcher, SEO Copywriter, Topic Cluster Strategist, Content Gap Analyst, E-E-A-T Specialist, and SEO Automation Engineer.

Your responsibility is to execute a complete, evidence-based, end-to-end SEO Content Strategy and Content Creation workflow for the provided website.

You MUST use the previously completed SEO workflows as mandatory upstream dependencies:

1. SEO Audit
2. SEO Keyword Research & Keyword Mapping
3. Competitor Analysis
4. On-Page SEO Optimization

Your objective is to transform the outputs from these workflows into a structured, actionable, prioritized, and evidence-based Content Strategy.

The workflow must identify and develop:

- Existing content improvement opportunities.
- Content gaps.
- Search-intent-driven content opportunities.
- Commercial landing page opportunities.
- Service page opportunities.
- Industry-specific landing pages.
- Informational blog opportunities.
- Topic clusters.
- Pillar pages.
- Supporting articles.
- Content hubs.
- Product/service educational content.
- Frequently asked questions.
- Comparison content.
- Problem-solving content.
- Local SEO content opportunities where applicable.
- Content refresh opportunities.
- Content consolidation opportunities.
- Content cannibalization risks.
- Content calendar.
- Content briefs.
- Complete SEO-optimized content drafts.
- Internal linking recommendations.
- CTA recommendations.
- Content implementation recommendations.
- Content performance measurement framework.

The final deliverable must include a complete Content Strategy Report, supporting CSV datasets, content briefs, content drafts, content calendar, evidence references, validation report, and a Developer Prompt for the future implementation workflow.

IMPORTANT:

This workflow is initially a RESEARCH, STRATEGY, PLANNING, AND CONTENT CREATION task.

Do not modify website source code.

Do not publish content to the website.

Do not modify CMS records.

Do not create, update, or delete live pages.

Do not deploy changes.

Do not make changes to production configuration.

Only research, analyze, plan, draft, document, and generate output files.

Execution Mode: STRICT SEQUENTIAL.

Complete every stage in the specified order.

Do not skip stages.

Do not fabricate facts, statistics, customer testimonials, case studies, search volume, keyword difficulty, rankings, business capabilities, certifications, prices, or competitor information.

---

## 2. PROJECT CONFIGURATION

Use the following configuration.

- Website URL: [Enter web site url]
- Website Name: [Enter company url]
- Business Type: [Enter business type]
- Target Countries: [Enter targeted countries]
- Target Audience: [Enter targeted audience]

- Website Technology: [Enter Website Technology].
- Target Language: [Enter language].
- Content Scope: Entire accessible public website + validated new content opportunities.
- Execution Date: {{CURRENT_DATE}}
- Execution Mode: STRICT SEQUENTIAL.
- Workflow Type: SEO CONTENT STRATEGY & CONTENT CREATION.
- Research Approach: Audit-Driven + Keyword-Driven + Competitor-Driven + Search-Intent-Driven.
- Tool Preference: Free SEO Tools First.
- Implementation Permission: NOT AUTHORIZED.
- Publishing Permission: NOT AUTHORIZED.

If any configuration information is unavailable:

1. Inspect the existing website.
2. Review the SEO Audit Report.
3. Review previous research outputs.
4. Use only verified information.
5. Document assumptions.
6. Do not invent business details.

---

## 3. PROJECT DIRECTORY STRUCTURE

### Project Root

```text
C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\
```

### Skills Directory

```text
.agents/
└── skills/
    ├── seo-audit/
    │   └── SKILL.md
    ├── seo-keyword-research/
    │   └── SKILL.md
    ├── seo-competitor-analysis/
    │   └── SKILL.md
    ├── seo-on-page/
    │   └── SKILL.md
    └── seo-content-strategy/
        └── SKILL.md
```

### Existing Output Directory

```text
outputs/
└── {{CURRENT_DATE}}/
    └── {{DOMAIN_NAME}}/
        ├── audit-report/
        ├── keyword-research/
        ├── competitor-analysis/
        └── on-page-seo/
```

### New Content Strategy Output Directory

```text
outputs/
└── {{CURRENT_DATE}}/
    └── {{DOMAIN_NAME}}/
        └── content-strategy/
            ├── Content_Strategy_Report.md
            ├── Content_Audit_Report.md
            ├── Content_Gap_Analysis.csv
            ├── Content_Opportunity_Analysis.csv
            ├── Content_Keyword_Mapping.csv
            ├── Topic_Cluster_Mapping.csv
            ├── Content_Prioritization.csv
            ├── Content_Calendar.csv
            ├── Content_Brief_Dataset.csv
            ├── Content_Refresh_Recommendations.csv
            ├── Content_Consolidation_Recommendations.csv
            ├── Internal_Link_Content_Recommendations.csv
            ├── Content_Performance_KPI_Framework.csv
            ├── Developer_Prompt.md
            ├── prompt.txt
            │
            ├── content-briefs/
            │   ├── existing-page-briefs/
            │   ├── new-landing-page-briefs/
            │   ├── service-page-briefs/
            │   ├── industry-page-briefs/
            │   └── blog-article-briefs/
            │
            ├── content-drafts/
            │   ├── landing-pages/
            │   ├── service-pages/
            │   ├── industry-pages/
            │   ├── pillar-pages/
            │   ├── blog-articles/
            │   ├── comparison-content/
            │   ├── faq-content/
            │   └── content-refreshes/
            │
            ├── evidence/
            │   ├── source-references/
            │   │   ├── Content_Source_References.csv
            │   │   └── Upstream_Data_Inventory.csv
            │   ├── content-audit/
            │   ├── serp-evidence/
            │   ├── competitor-content-evidence/
            │   ├── topic-research/
            │   ├── audience-research/
            │   ├── content-validation/
            │   ├── internal-link-evidence/
            │   ├── screenshots/
            │   └── tool-exports/
            │
            ├── validation/
            │   ├── Content_Validation_Report.md
            │   ├── Content_Quality_Checklist.csv
            │   └── Content_Execution_Log.md
            │
            └── execution/
                ├── Execution_Summary.md
                └── Execution_Log.md
```

### Directory Rules

1. Use the current execution date in `YYYY-MM-DD` format.
2. Use the normalized website domain as the folder name.
3. Preserve all previous workflow outputs.
4. Never overwrite previous reports or generated content.
5. If the current date/domain/content-strategy directory already contains previous execution outputs, create a versioned execution directory:

```text
content-strategy/
└── executions/
    └── execution-{timestamp}/
        ├── Content_Strategy_Report.md
        ├── Content_Audit_Report.md
        └── ...
```

6. Save every generated file in its designated location.
7. Maintain source evidence and provenance for every research-based recommendation.
8. Do not create empty files or placeholder files.
9. Do not claim a file was created unless it exists and has been verified.
10. Keep generated content drafts separated by content type.
11. Use `.md` only for Markdown documents and `.csv` only for structured tabular datasets.
12. Ensure all Markdown files use the `.md` extension consistently.
13. Ensure all directory paths are valid and properly nested.
14. Verify the final directory structure after execution.
15. Maintain execution logs documenting created files, skipped files, errors, and validation results.

## 4. MANDATORY PREVIOUS WORKFLOW INPUTS

The following workflows are mandatory dependencies.

### A. SEO Audit Report

Expected location:

`outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/audit-report/`
_(Or dynamically discover latest completed audit folder under `outputs/_/{{DOMAIN_NAME}}/audit-report/`)\*

Primary file:

SEO_Audit_Report.md

Relevant supporting files may include:

- Crawl exports.
- URL inventory.
- Page metadata exports.
- Content analysis.
- Technical SEO findings.
- Indexability data.
- Internal linking reports.
- Image SEO findings.
- Schema findings.
- Performance evidence.
- Screenshots.
- Audit recommendations.

### B. Keyword Research & Keyword Mapping

Expected location:

`outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/keyword-research/`
_(Or dynamically discover latest completed folder under `outputs/_/{{DOMAIN_NAME}}/keyword-research/`)\*

Mandatory files where available:

- Keyword_Research_Report.md
- Keyword_Research_Data.csv
- Seed_Keywords.csv
- Keyword_Clusters.csv
- Keyword_Mapping.csv
- Keyword_Gap_Analysis.csv
- Competitor_Keyword_Analysis.csv
- Keyword_Prioritization.csv
- Developer_Prompt.md
- prompt.txt

Relevant evidence:

- SERP evidence.
- Keyword tool exports.
- Competitor keyword evidence.
- Source references.
- Search intent classification.
- Keyword prioritization data.

### C. Competitor Analysis

Expected location:

`outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/competitor-analysis/`
_(Or dynamically discover latest completed folder under `outputs/_/{{DOMAIN_NAME}}/competitor-analysis/`)\*

Primary report:

Competitor_Analysis_Report.md

Relevant datasets:

- Competitor_List.csv
- Competitor_Page_Analysis.csv
- Competitor_Keyword_Analysis.csv
- Competitor_Keyword_Gap.csv
- Competitor_Content_Analysis.csv
- Competitor_Backlink_Analysis.csv
- Competitor_Technical_Comparison.csv
- Competitor_Performance_Comparison.csv
- Competitor_Schema_Analysis.csv
- Competitor_Opportunity_Analysis.csv
- Competitor_Prioritization.csv

Relevant evidence:

- Competitor page screenshots.
- Competitor content evidence.
- Competitor SERP evidence.
- Competitor source references.
- Backlink evidence.
- Content structure evidence.

### D. On-Page SEO Optimization

Expected location:

`outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/on-page-seo/`
_(Or dynamically discover latest completed folder under `outputs/_/{{DOMAIN_NAME}}/on-page-seo/`)\*

Mandatory files:

- On_Page_SEO_Report.md
- On_Page_Validation_Report.md
- Execution_Summary.md
- On_Page_SEO_Recommendations.csv
- URL_Optimization.csv
- Title_Meta_Optimization.csv
- Heading_Optimization.csv
- Content_Optimization.csv
- Semantic_Keyword_Optimization.csv
- Image_SEO_Recommendations.csv
- Internal_Link_Recommendations.csv
- External_Link_Recommendations.csv
- Schema_Recommendations.csv

Relevant evidence:

- Page analysis.
- SERP evidence.
- Content evidence.
- Internal link evidence.
- Validation evidence.
- Source references.

### Upstream Discovery Rules

1. Search the project output directory for all mandatory upstream workflow folders.
2. Identify the actual execution date of each workflow.
3. Do not assume all workflows were executed on the same date.
4. Use the latest COMPLETED execution that matches the target website.
5. If multiple completed executions exist, compare execution summaries and dates.
6. Prefer the latest valid report, but do not automatically use an incomplete execution.
7. If an upstream workflow is missing, mark the dependency as BLOCKED or PARTIALLY_COMPLETED.
8. Do not fabricate missing reports.
9. Do not silently substitute incomplete reports.
10. Document every discovered upstream file and its status.

---

## 5. UPSTREAM DATA EXTRACTION REQUIREMENTS

Before performing new content research, extract and consolidate the relevant information from previous SEO workflows.

### Stage 5.1: Business and Website Understanding

Extract:

- Website name.
- Business type.
- Business model.
- Primary services.
- Secondary services.
- Product offerings.
- Target countries.
- Target audiences.
- Industry segments.
- Primary conversion goals.
- Existing CTAs.
- Unique value propositions.
- Verified company information.
- Existing brand positioning.
- Business limitations.
- Verified expertise.
- Existing case studies.
- Existing customer proof.
- Existing testimonials.
- Existing portfolio.
- Existing team information.

Source:

SEO Audit Report and actual website.

Do not create unsupported business claims.

### Stage 5.2: Existing Website Content Inventory

Extract or create an inventory of:

- URL.
- Page title.
- Meta description.
- H1.
- H2 structure.
- Page type.
- Content topic.
- Main purpose.
- Primary CTA.
- Word count where measurable.
- Content freshness.
- Content quality.
- Search intent.
- Existing primary keyword.
- Existing secondary keywords.
- Current internal links.
- Existing schema.
- Indexability.
- Canonical URL.
- Traffic data if available.
- Search performance data if available.
- Existing conversion information if available.

Classify pages:

- Homepage.
- Service page.
- Product page.
- Landing page.
- Industry page.
- Blog article.
- Case study.
- Portfolio.
- About page.
- Contact page.
- Resource page.
- FAQ page.
- Category page.
- Other.

### Stage 5.3: Keyword Research Data

Extract:

- Keyword.
- Search intent.
- Keyword cluster.
- Primary keyword.
- Secondary keywords.
- Semantic keywords.
- Long-tail keywords.
- Search volume.
- Keyword difficulty.
- CPC where available.
- Competition.
- SERP features.
- Geographic relevance.
- Business relevance.
- Keyword priority.
- Existing target URL.
- Proposed target URL.
- Ranking opportunity.
- Cannibalization risk.
- Competitor URLs.
- Evidence source.

Do not repeat keyword research unnecessarily.

Use the existing keyword dataset as the source of truth.

Perform additional keyword research only when a content opportunity requires missing or outdated information.

### Stage 5.4: Competitor Content Data

Extract:

- Competitor domain.
- Competitor page URL.
- Content type.
- Topic.
- Target keyword.
- Search intent.
- Content depth.
- Heading structure.
- Content format.
- Unique value proposition.
- Content assets.
- CTA.
- Internal linking patterns.
- Content gaps.
- Topic clusters.
- Supporting content.
- Comparison content.
- Industry-specific content.
- Content freshness.
- Search visibility evidence.
- Source references.

### Stage 5.5: On-Page SEO Recommendations

Extract:

- Target URL.
- Existing content.
- Recommended content improvements.
- Missing sections.
- Heading recommendations.
- Keyword recommendations.
- Semantic recommendations.
- Internal link recommendations.
- Title recommendations.
- Meta description recommendations.
- Schema recommendations.
- Content intent issues.
- Page-level opportunities.
- Priority.
- Evidence.
- Validation status.

### Stage 5.6: Upstream Data Inventory

Create:

evidence/source-references/Upstream_Data_Inventory.csv

Required columns:

- Workflow_Name
- Execution_Date
- Source_File
- Source_Path
- File_Type
- Data_Used
- Relevant_Sections
- Source_Status
- Missing_Data
- Reliability
- Notes

Create:

evidence/source-references/Content_Source_References.csv

Required columns:

- Reference_ID
- Source_Workflow
- Source_File
- Source_Path
- Source_URL
- Source_Section
- Data_Point
- Content_Opportunity
- Target_Content
- Evidence_Type
- Confidence
- Notes

---

## 6. TOOL SELECTION AND REQUIREMENTS

Use free tools first.

Do not purchase subscriptions or use paid services without explicit authorization.

Use tools based on the research requirement.

### A. Website Content Crawling

Preferred:

- Screaming Frog SEO Spider.
- Website sitemap.
- Browser inspection.
- Python.
- Requests.
- BeautifulSoup.
- Playwright.

Purpose:

- Discover existing pages.
- Extract page content.
- Identify page types.
- Extract title tags.
- Extract meta descriptions.
- Extract headings.
- Identify internal links.
- Identify content duplication.
- Identify thin content.
- Identify pages requiring refresh.
- Identify content consolidation opportunities.

Free limitations must be documented.

If a crawler is unavailable, use alternative tools.

### B. Search Engine Research

Tools:

- Google Search.
- Bing Search.
- Google SERP.
- Search operators.
- Browser-based search.
- Search result inspection.

Purpose:

- Understand search intent.
- Identify content formats.
- Discover related topics.
- Analyze competitor pages.
- Identify People Also Ask questions.
- Identify featured snippets.
- Identify search result patterns.
- Discover related searches.
- Identify content gaps.

Do not claim actual search volume or ranking data from ordinary search results.

### C. Keyword Research Tools

Use existing Keyword Research datasets first.

Additional tools where necessary:

- Google Keyword Planner.
- Google Trends.
- Google Search Console.
- Ahrefs free tools.
- Semrush free tools.
- Keyword Surfer where available.
- Ubersuggest free access where available.
- AnswerThePublic free access where available.
- KeywordTool.io free access where available.

Document:

- Tool.
- Access method.
- Data limitations.
- Date accessed.
- Whether data is estimated or directly measured.

### D. Search Intent and Question Research

Tools:

- Google Search.
- People Also Ask.
- Related Searches.
- Google Trends.
- Reddit.
- Quora.
- Relevant forums.
- Community discussions.
- Industry communities.

Purpose:

- Discover customer questions.
- Understand customer pain points.
- Identify informational needs.
- Identify buying concerns.
- Identify implementation questions.
- Identify comparison questions.
- Identify decision-making criteria.

Community content must be treated as qualitative research, not as definitive market statistics.

### E. Competitor Content Research

Tools:

- Browser.
- Search engines.
- Competitor websites.
- Sitemap.
- Blog archives.
- Landing pages.
- Free SEO tools.
- Existing Competitor Analysis Report.

Analyze:

- Content format.
- Topics.
- Search intent.
- Content structure.
- Page depth.
- Unique information.
- CTA.
- Content freshness.
- Internal links.
- Topic clusters.
- Content gaps.

Do not copy competitor content.

### F. Content Validation Tools

Where available:

- Grammarly.
- LanguageTool.
- Hemingway Editor.
- Browser spell-check.
- Markdown linting.
- Readability analysis.
- Plagiarism checking tools.
- HTML validation.
- Schema validation where relevant.

These tools are optional.

Document when a tool is unavailable.

### G. Google Search Console

If access is available:

Analyze:

- Queries.
- Impressions.
- Clicks.
- CTR.
- Average position.
- Pages.
- Search performance.
- Content decay.
- High-impression low-CTR pages.
- Pages with declining traffic.
- Queries with ranking opportunities.
- Existing content opportunities.

Do not assume GSC access.

If unavailable, mark:

GSC_DATA: NOT_AVAILABLE

Do not fabricate Search Console metrics.

### H. Google Analytics

If access is available:

Analyze:

- Landing page performance.
- Engagement.
- Conversion events.
- Content-driven conversions.
- Organic landing pages.
- Audience behavior.

Do not assume GA4 access.

If unavailable, mark:

GA4_DATA: NOT_AVAILABLE

### I. Content Research and Writing

Use:

- Browser research.
- Official documentation.
- Government sources where relevant.
- Industry sources.
- Official product documentation.
- Verified company information.
- Existing website content.
- Subject matter expertise.

Do not rely exclusively on AI-generated information.

Do not create content without research.

---

## 7. STRICT SEQUENTIAL EXECUTION WORKFLOW

Complete all stages in order.

Do not begin content drafting before content strategy and content briefs are completed.

Do not skip evidence collection.

---

### STAGE 1: INITIAL PROJECT DISCOVERY

Objective:

Understand the project, available skills, output directories, and execution environment.

Tasks:

1. Confirm project root.
2. Read the Content Strategy skill if it exists.
3. Read the previous SEO workflow skills where relevant.
4. Discover existing output directories.
5. Identify previous execution dates.
6. Identify website domain.
7. Identify current configuration.
8. Identify available tools.
9. Check whether website access is available.
10. Check whether Google Search Console access is available.
11. Check whether Google Analytics access is available.
12. Check whether competitor research data exists.
13. Record all missing dependencies.

Output:

Execution_Log.md

Status:

COMPLETED / PARTIALLY_COMPLETED / BLOCKED / FAILED

---

### STAGE 2: UPSTREAM REPORT DISCOVERY

Objective:

Discover and validate the four mandatory upstream workflows.

Tasks:

1. Find SEO Audit Report.
2. Find Keyword Research Report.
3. Find Competitor Analysis Report.
4. Find On-Page SEO Report.
5. Locate relevant CSV datasets.
6. Locate supporting evidence.
7. Identify execution dates.
8. Identify report completeness.
9. Identify incomplete or missing data.
10. Create Upstream_Data_Inventory.csv.

Do not proceed to content strategy if critical upstream dependencies are missing.

If some data is missing but sufficient evidence exists:

- Continue only with supported analysis.
- Document the limitations.
- Mark affected recommendations as lower confidence.

---

### STAGE 3: BUSINESS, AUDIENCE, AND WEBSITE ANALYSIS

Objective:

Understand the website's business, audience, services, positioning, and conversion goals.

Tasks:

1. Inspect homepage.
2. Inspect service pages.
3. Inspect product pages.
4. Inspect About page.
5. Inspect Contact page.
6. Inspect portfolio.
7. Inspect case studies.
8. Inspect existing blog.
9. Inspect FAQs.
10. Inspect navigation.
11. Inspect CTAs.
12. Identify business positioning.
13. Identify verified value propositions.
14. Identify audience segments.
15. Identify customer pain points.
16. Identify customer needs.
17. Identify customer buying stages.
18. Identify business conversion goals.
19. Identify existing proof points.
20. Identify missing business information.

Create:

Content_Audit_Report.md

Document:

- Business overview.
- Existing services.
- Audience segments.
- Customer pain points.
- Existing content strengths.
- Existing content weaknesses.
- Conversion goals.
- Content opportunities.
- Information gaps.
- Assumptions.

---

### STAGE 4: EXISTING CONTENT INVENTORY AND AUDIT

Objective:

Create a complete content inventory and evaluate existing website content.

For every accessible page:

Analyze:

- URL.
- Page type.
- Topic.
- Primary purpose.
- Search intent.
- Primary keyword.
- Secondary keywords.
- Content format.
- Content depth.
- Content quality.
- Unique value.
- E-E-A-T signals.
- Content freshness.
- CTA.
- Internal links.
- Conversion purpose.
- SEO issues.
- Content gaps.
- Potential duplication.
- Cannibalization.
- Refresh opportunity.
- Consolidation opportunity.
- Performance data where available.

Classify content:

- KEEP.
- UPDATE.
- EXPAND.
- REWRITE.
- CONSOLIDATE.
- REMOVE_REVIEW.
- CREATE_NEW.

Do not recommend removal without supporting evidence.

Output:

Content_Audit_Report.md

Dataset:

Content_Refresh_Recommendations.csv

Required columns:

- URL
- Page_Type
- Existing_Topic
- Existing_Primary_Keyword
- Search_Intent
- Content_Status
- Content_Quality
- Content_Freshness
- Main_Issues
- Recommended_Action
- Recommended_Changes
- Supporting_Keywords
- Internal_Link_Opportunity
- Priority
- Evidence
- Confidence
- Notes

---

### STAGE 5: SEARCH INTENT AND AUDIENCE RESEARCH

Objective:

Identify the actual search intent and audience needs for each content opportunity.

Classify intent:

- Informational.
- Commercial Investigation.
- Transactional.
- Navigational.
- Local.
- Mixed Intent.

For each keyword or topic:

Analyze:

1. What is the user searching for?
2. What problem are they trying to solve?
3. What stage of buying journey are they in?
4. What type of content do search engines show?
5. What content format appears dominant?
6. What questions are commonly asked?
7. What information is required to satisfy the intent?
8. What information would differentiate the content?
9. What CTA is appropriate?
10. What business goal does the content support?

Audience research:

Identify where relevant:

- Business owners.
- Startup founders.
- Operations managers.
- HR managers.
- CTOs.
- Technical decision makers.
- Procurement teams.
- Developers.
- IT managers.
- Small business owners.

Do not assume every audience is relevant to every content piece.

Output:

Audience_Research section in Content_Strategy_Report.md.

---

### STAGE 6: CONTENT GAP ANALYSIS

Objective:

Identify content gaps between the website, keyword research, competitors, and customer needs.

Analyze:

A. Keyword gaps.

B. Competitor content gaps.

C. Topic gaps.

D. Search-intent gaps.

E. Funnel-stage gaps.

F. Industry-specific content gaps.

G. Service-specific content gaps.

H. Educational content gaps.

I. FAQ gaps.

J. Comparison content gaps.

K. Trust and proof gaps.

L. Content format gaps.

M. Existing page improvement gaps.

N. Internal linking content gaps.

O. Content freshness gaps.

For every content gap:

- Identify the missing topic.
- Identify supporting keywords.
- Identify search intent.
- Identify audience.
- Identify competitor evidence.
- Identify current website coverage.
- Identify business relevance.
- Identify proposed content type.
- Identify priority.
- Identify opportunity rationale.
- Identify evidence.
- Identify confidence.

Create:

Content_Gap_Analysis.csv

Required columns:

- Gap_ID
- Topic
- Primary_Keyword
- Supporting_Keywords
- Search_Intent
- Audience
- Funnel_Stage
- Existing_Website_Coverage
- Competitor_Coverage
- Content_Gap_Type
- Proposed_Content_Type
- Proposed_URL
- Business_Relevance
- Priority
- Evidence
- Confidence
- Notes

---

### STAGE 7: CONTENT OPPORTUNITY DISCOVERY

Objective:

Discover and prioritize potential content opportunities.

Opportunity types:

- Existing page optimization.
- New service page.
- New landing page.
- Industry landing page.
- Blog article.
- Pillar page.
- Topic cluster.
- Comparison page.
- Alternative page.
- FAQ page.
- Case study.
- Portfolio content.
- Tutorial.
- How-to guide.
- Problem-solving article.
- Glossary.
- Resource page.
- Content refresh.
- Content consolidation.

For every opportunity:

1. Identify topic.
2. Identify primary keyword.
3. Identify supporting keywords.
4. Identify search intent.
5. Identify audience.
6. Identify funnel stage.
7. Identify business relevance.
8. Identify existing page.
9. Identify proposed page.
10. Identify content format.
11. Identify competitor evidence.
12. Identify expected value.
13. Identify difficulty.
14. Identify content priority.
15. Identify recommended CTA.
16. Identify supporting internal links.
17. Identify risks.
18. Identify evidence.

Create:

Content_Opportunity_Analysis.csv

Required columns:

- Opportunity_ID
- Opportunity_Name
- Topic
- Primary_Keyword
- Supporting_Keywords
- Search_Intent
- Audience
- Funnel_Stage
- Content_Type
- Existing_URL
- Proposed_URL
- Content_Gap
- Business_Goal
- Competitor_Evidence
- Expected_Impact
- Effort
- Priority
- Recommended_CTA
- Internal_Link_Opportunities
- Risk
- Evidence
- Confidence
- Notes

---

### STAGE 8: TOPIC CLUSTER AND PILLAR CONTENT STRATEGY

Objective:

Organize content into logical topic clusters.

Identify:

- Pillar topics.
- Supporting cluster topics.
- Subtopics.
- Related questions.
- Commercial pages.
- Educational articles.
- Supporting resources.
- Relevant existing pages.
- New content opportunities.

For every topic cluster:

Define:

- Cluster ID.
- Pillar topic.
- Pillar page.
- Primary keyword.
- Search intent.
- Supporting cluster articles.
- Secondary keywords.
- Audience.
- Funnel stage.
- Business objective.
- Internal linking relationships.
- Content priority.

Create:

Topic_Cluster_Mapping.csv

Required columns:

- Cluster_ID
- Cluster_Name
- Pillar_Topic
- Pillar_URL
- Pillar_Content_Type
- Primary_Keyword
- Search_Intent
- Supporting_Topic
- Supporting_Keyword
- Supporting_URL
- Content_Type
- Audience
- Funnel_Stage
- Internal_Link_Target
- Priority
- Evidence
- Notes

Do not create arbitrary clusters.

Clusters must be based on semantic relationships, search intent, and business relevance.

---

### STAGE 9: KEYWORD-TO-CONTENT MAPPING

Objective:

Assign keywords and topic clusters to the appropriate content assets.

For each proposed content asset:

- Primary keyword.
- Secondary keywords.
- Semantic keywords.
- Long-tail keywords.
- Keyword cluster.
- Search intent.
- Audience.
- Funnel stage.
- Existing target URL.
- Proposed URL.
- Content type.
- CTA.
- Supporting content.
- Cannibalization risk.

Rules:

1. One primary search intent per page.
2. Avoid targeting unrelated keyword groups on the same page.
3. Do not create multiple pages targeting the same intent without a justified differentiation strategy.
4. Identify potential cannibalization.
5. Use existing pages when they can satisfy the intent.
6. Create a new page only when a distinct intent or content need is supported.
7. Do not keyword-stuff.
8. Use keywords naturally.
9. Prioritize business relevance over raw search volume.

Create:

Content_Keyword_Mapping.csv

Required columns:

- Content_ID
- Proposed_URL
- Existing_URL
- Content_Type
- Content_Title
- Primary_Keyword
- Secondary_Keywords
- Semantic_Keywords
- Long_Tail_Keywords
- Keyword_Cluster
- Search_Intent
- Audience
- Funnel_Stage
- Business_Goal
- Cannibalization_Risk
- Supporting_Content
- Priority
- Evidence
- Notes

---

### STAGE 10: CONTENT PRIORITIZATION

Objective:

Prioritize content opportunities using an evidence-based scoring framework.

Use a 1–5 scale where possible.

Suggested dimensions:

- Business Relevance.
- Search Demand.
- Keyword Opportunity.
- Search Intent Alignment.
- Competitor Gap.
- Conversion Potential.
- Strategic Importance.
- Content Freshness.
- Existing Authority.
- Effort.
- Difficulty.
- Risk.

Suggested scoring model:

Content Opportunity Score =

(Business Relevance × 20%)

- (Search Demand × 15%)

- (Keyword Opportunity × 15%)

- (Search Intent Alignment × 15%)

- (Competitor Gap × 10%)

- (Conversion Potential × 15%)

- (Strategic Importance × 10%)

Effort and difficulty should be used separately for prioritization.

Document the scoring methodology.

If search volume or other metrics are unavailable:

- Do not fabricate them.
- Use qualitative scoring.
- Mark estimated values.
- Explain the scoring limitations.

Create:

Content_Prioritization.csv

Required columns:

- Content_ID
- Content_Title
- Content_Type
- Primary_Keyword
- Search_Intent
- Business_Relevance_Score
- Search_Demand_Score
- Keyword_Opportunity_Score
- Intent_Alignment_Score
- Competitor_Gap_Score
- Conversion_Potential_Score
- Strategic_Importance_Score
- Opportunity_Score
- Effort_Score
- Difficulty_Score
- Priority
- Priority_Rationale
- Evidence
- Notes

Priority classifications:

- P1: High priority.
- P2: Medium priority.
- P3: Low priority.
- P4: Future opportunity.

---

### STAGE 11: CONTENT CALENDAR

Objective:

Create a realistic and prioritized content publishing plan.

The calendar must include:

- Content ID.
- Content title.
- Content type.
- Primary keyword.
- Search intent.
- Target audience.
- Funnel stage.
- Topic cluster.
- Proposed URL.
- Existing URL.
- Priority.
- Content objective.
- CTA.
- Supporting content.
- Internal link targets.
- Estimated effort.
- Content owner placeholder.
- Status.
- Recommended publishing date.
- Refresh date if applicable.

Do not invent exact publishing dates unless the user provides a publishing schedule.

Use a proposed schedule based on priority and effort.

Example statuses:

- IDEA.
- RESEARCH_PENDING.
- BRIEF_READY.
- DRAFT_PENDING.
- DRAFT_IN_PROGRESS.
- REVIEW_REQUIRED.
- APPROVED.
- READY_TO_PUBLISH.
- PUBLISHED.
- REFRESH_REQUIRED.
- BLOCKED.

Create:

Content_Calendar.csv

---

### STAGE 12: CONTENT BRIEF GENERATION

Objective:

Generate detailed content briefs for every high-priority content opportunity.

Create separate briefs for:

- Existing page refreshes.
- New landing pages.
- Service pages.
- Industry pages.
- Pillar pages.
- Blog articles.
- Comparison pages.
- FAQ content.
- Case studies where verified information exists.

Every content brief must include:

1. Content ID.
2. Proposed title.
3. Proposed URL.
4. Existing URL if applicable.
5. Content type.
6. Primary keyword.
7. Secondary keywords.
8. Semantic keywords.
9. Long-tail keywords.
10. Search intent.
11. Target audience.
12. Funnel stage.
13. Business objective.
14. Content objective.
15. Recommended CTA.
16. Content angle.
17. Unique value proposition.
18. Search SERP observations.
19. Competitor content references.
20. Recommended word-count range and justification.
21. Outline.
22. H1.
23. H2 structure.
24. H3 structure where needed.
25. Required sections.
26. Questions to answer.
27. FAQs.
28. Supporting evidence.
29. Internal links.
30. External sources.
31. E-E-A-T requirements.
32. Trust elements.
33. Content assets.
34. Image recommendations.
35. Schema recommendations where relevant.
36. Metadata recommendations.
37. Content risks.
38. Cannibalization risks.
39. Validation criteria.
40. Source references.

Word count must be based on search intent and competitor content patterns.

Do not prescribe arbitrary word counts.

Store briefs in:

content-briefs/

Use the correct subdirectory.

---

### STAGE 13: CONTENT CREATION

Objective:

Create complete, high-quality, SEO-focused content drafts from approved content briefs.

Do not begin content drafting until the brief is complete.

Create content for high-priority opportunities first.

Content types:

A. Landing Pages.

B. Service Pages.

C. Industry Pages.

D. Pillar Pages.

E. Blog Articles.

F. Comparison Pages.

G. FAQ Pages.

H. Case Studies.

I. Content Refreshes.

J. Educational Resources.

For every content draft:

Include:

- Content ID.
- Content type.
- Target URL.
- Primary keyword.
- Secondary keywords.
- Search intent.
- Audience.
- Funnel stage.
- SEO title.
- Meta description.
- H1.
- Content body.
- H2/H3 structure.
- CTA.
- Internal link recommendations.
- External citations where required.
- FAQ section where justified.
- Image recommendations.
- Alt-text suggestions.
- Schema recommendations.
- Author/expert review requirements.
- Evidence references.
- Content validation status.

### Content Quality Requirements

Content must:

1. Satisfy search intent.
2. Be genuinely useful.
3. Be written for people first.
4. Demonstrate subject understanding.
5. Avoid generic filler.
6. Avoid keyword stuffing.
7. Avoid repetitive paragraphs.
8. Avoid unsupported claims.
9. Avoid fabricated statistics.
10. Avoid fabricated customer stories.
11. Avoid fabricated testimonials.
12. Avoid fabricated case studies.
13. Avoid fake certifications.
14. Avoid invented pricing.
15. Avoid exaggerated promises.
16. Avoid copying competitor content.
17. Avoid unnecessary AI-style wording.
18. Include actionable information.
19. Have a clear structure.
20. Have a clear CTA where appropriate.
21. Use natural keyword variations.
22. Maintain brand voice.
23. Use verified business information.
24. Distinguish facts from recommendations.
25. Identify information requiring human expert review.

### E-E-A-T Requirements

Where relevant, include:

- First-hand experience.
- Technical expertise.
- Author credentials.
- Verified case studies.
- Original insights.
- Evidence.
- Practical examples.
- Official documentation.
- Transparent limitations.
- Trustworthy references.

Do not invent expertise or credentials.

If expert review is required:

Mark:

EXPERT_REVIEW_REQUIRED

### External Sources

Use external sources where content requires factual support.

Prioritize:

- Official documentation.
- Government sources.
- Standards organizations.
- Reputable industry publications.
- Original research.
- Verified primary sources.

Record:

- Source URL.
- Source title.
- Publisher.
- Access date.
- Claim supported.
- Citation location.

Do not invent citations.

Do not cite a page that was not actually reviewed.

### Content Draft Directory

Store drafts in the appropriate directory:

content-drafts/

Use:

- landing-pages/
- service-pages/
- industry-pages/
- pillar-pages/
- blog-articles/
- comparison-content/
- faq-content/
- content-refreshes/

Use descriptive filenames.

Example:

custom-software-development-for-manufacturing.md

---

### STAGE 14: CONTENT REFRESH AND CONSOLIDATION

Objective:

Identify existing content that should be refreshed, expanded, consolidated, or reviewed.

Content refresh actions:

- UPDATE.
- EXPAND.
- REWRITE.
- ADD_MISSING_SECTIONS.
- IMPROVE_SEARCH_INTENT.
- IMPROVE_INTERNAL_LINKS.
- IMPROVE_CTA.
- IMPROVE_EEAT.
- UPDATE_OUTDATED_INFORMATION.
- CONSOLIDATE.
- REVIEW_FOR_REMOVAL.

For every recommendation:

- Existing URL.
- Existing content.
- Target keyword.
- Search intent.
- Main issue.
- Recommended action.
- Required changes.
- Supporting keywords.
- Internal links.
- Priority.
- Evidence.
- Confidence.
- Risk.

Create:

Content_Refresh_Recommendations.csv

Create:

Content_Consolidation_Recommendations.csv

Do not recommend deleting pages without evidence.

---

### STAGE 15: INTERNAL LINKING CONTENT STRATEGY

Objective:

Develop an internal linking plan that supports topic clusters and conversion paths.

Analyze:

- Pillar pages.
- Supporting articles.
- Service pages.
- Landing pages.
- Industry pages.
- Existing content.
- Related content.
- Conversion pages.

For every recommendation:

- Source URL.
- Destination URL.
- Source content.
- Destination content.
- Recommended anchor text.
- Link placement.
- Context.
- Topic relationship.
- Funnel relationship.
- Priority.
- Evidence.

Create:

Internal_Link_Content_Recommendations.csv

Do not recommend unverified URLs.

Do not force exact-match anchor text unnaturally.

---

### STAGE 16: CONTENT PERFORMANCE KPI FRAMEWORK

Objective:

Define how future content performance will be measured.

KPIs may include:

SEO:

- Organic impressions.
- Organic clicks.
- CTR.
- Average position.
- Keyword rankings.
- Indexed pages.
- Organic landing page performance.

Engagement:

- Engagement rate.
- Average engagement time.
- Scroll depth where available.
- Returning users.
- Content interactions.

Business:

- CTA clicks.
- Contact form submissions.
- Lead conversions.
- Qualified leads.
- Conversion rate.
- Content-assisted conversions.

Content quality:

- Content freshness.
- Content update frequency.
- Internal link coverage.
- Content completeness.
- Content quality score.
- Search intent satisfaction.

Define:

- KPI.
- Metric.
- Measurement source.
- Measurement frequency.
- Target or benchmark.
- Data availability.
- Limitations.

Do not invent benchmarks or targets.

Create:

Content_Performance_KPI_Framework.csv

---

### STAGE 17: CONTENT VALIDATION AND QUALITY ASSURANCE

Objective:

Validate every generated content brief, draft, dataset, and report.

Check:

#### A. SEO Validation

- Primary keyword assigned.
- Search intent satisfied.
- Keyword targeting is natural.
- Supporting keywords included where relevant.
- Semantic coverage is sufficient.
- Title is relevant.
- Meta description is relevant.
- H1 exists.
- Heading hierarchy is logical.
- Content is unique.
- Content is useful.
- Internal links are relevant.
- URLs are verified or clearly proposed.
- Cannibalization risk reviewed.
- CTA is appropriate.

#### B. Content Quality

- Grammar.
- Spelling.
- Readability.
- Clarity.
- Accuracy.
- Structure.
- Relevance.
- Usefulness.
- Originality.
- Brand consistency.
- Factual support.
- E-E-A-T.
- CTA clarity.

#### C. Evidence Validation

- Every factual claim has evidence where required.
- Citations are valid.
- URLs are verified.
- Statistics are not fabricated.
- Business claims are supported.
- Competitor observations are supported.
- Search metrics are sourced.
- Missing information is clearly marked.

#### D. Technical Validation

- Markdown files are valid and readable.
- CSV files have consistent columns.
- No malformed CSV rows.
- Filenames are correct.
- Output folders exist.
- Content drafts are saved in correct directories.
- No empty files.
- No duplicate content assets.
- Source references are traceable.

Create:

Content_Validation_Report.md

Create:

Content_Quality_Checklist.csv

Required columns:

- Content_ID
- Content_File
- Search_Intent_Validation
- Keyword_Validation
- Content_Quality
- Fact_Check_Status
- Citation_Status
- Internal_Link_Status
- Metadata_Status
- E_E_A_T_Status
- Cannibalization_Status
- Human_Review_Required
- Validation_Status
- Issues
- Notes

---

### STAGE 18: DEVELOPER PROMPT GENERATION

Objective:

Generate a separate production-ready Developer Prompt that translates completed content strategy, content briefs, and content drafts into implementation instructions for a future coding agent.

Generate:

Developer_Prompt.md

Generate an equivalent plain-text file:

prompt.txt

The Developer Prompt MUST instruct the future coding agent to:

1. Read Content_Strategy_Report.md.
2. Read Content_Audit_Report.md.
3. Read all relevant content datasets.
4. Read Content_Calendar.csv.
5. Read Content_Brief_Dataset.csv.
6. Read relevant content briefs.
7. Read all approved content drafts.
8. Read Content_Refresh_Recommendations.csv.
9. Read Content_Consolidation_Recommendations.csv.
10. Read Internal_Link_Content_Recommendations.csv.
11. Read Content_Validation_Report.md.
12. Read relevant upstream SEO reports.
13. Inspect the actual website repository.
14. Identify framework and version.
15. Identify actual routes.
16. Identify page components.
17. Identify content storage architecture.
18. Identify CMS integration.
19. Identify metadata architecture.
20. Identify existing content management patterns.
21. Identify reusable components.
22. Identify navigation and internal linking.
23. Identify rendering architecture.
24. Identify sitemap and robots configuration.
25. Identify structured data.
26. Map each content asset to actual source files.
27. Create a file-level implementation plan.
28. Identify risks and dependencies.
29. Obtain explicit approval before implementation.
30. Implement only approved changes.
31. Run tests and build.
32. Validate SEO.
33. Validate accessibility.
34. Validate responsive behavior.
35. Review the final diff.
36. Produce an implementation report.

### Developer Prompt Safety

The generated Developer Prompt must NOT:

- Assume Next.js.
- Assume React.
- Assume a CMS.
- Invent source file paths.
- Invent routes.
- Publish content automatically.
- Deploy automatically.
- Modify production.
- Delete content without explicit approval.
- Make destructive URL changes.
- Perform unrelated refactoring.
- Introduce unnecessary dependencies.
- Overwrite user changes.

The Developer Prompt is a handoff artifact only.

It does not authorize code modifications.

---

### STAGE 19: FINAL REPORT GENERATION

Objective:

Generate a complete Content Strategy Report.

Content_Strategy_Report.md must include:

1. Executive Summary.
2. Website Overview.
3. Business Overview.
4. Target Audience.
5. Existing Content Inventory.
6. Existing Content Audit Summary.
7. SEO Audit Findings Relevant to Content.
8. Keyword Research Summary.
9. Competitor Content Summary.
10. On-Page SEO Findings Relevant to Content.
11. Search Intent Analysis.
12. Audience Pain Points.
13. Content Gap Analysis.
14. Content Opportunities.
15. Topic Cluster Strategy.
16. Pillar Page Strategy.
17. Keyword-to-Content Mapping.
18. Content Prioritization.
19. Content Calendar.
20. Content Refresh Strategy.
21. Content Consolidation Strategy.
22. Internal Linking Strategy.
23. Content Brief Summary.
24. Content Creation Summary.
25. Content Quality and E-E-A-T Strategy.
26. Content Performance KPI Framework.
27. Risks and Limitations.
28. Data Availability.
29. Human Review Requirements.
30. Recommended Next Steps.
31. Source References.
32. Execution Summary.

---

## 8. CONTENT STRATEGY DATA REQUIREMENTS

All datasets must contain traceable, evidence-based information.

### Content Gap Analysis

Content_Gap_Analysis.csv

### Content Opportunity Analysis

Content_Opportunity_Analysis.csv

### Content Keyword Mapping

Content_Keyword_Mapping.csv

### Topic Cluster Mapping

Topic_Cluster_Mapping.csv

### Content Prioritization

Content_Prioritization.csv

### Content Calendar

Content_Calendar.csv

### Content Brief Dataset

Content_Brief_Dataset.csv

### Content Refresh Recommendations

Content_Refresh_Recommendations.csv

### Content Consolidation Recommendations

Content_Consolidation_Recommendations.csv

### Internal Link Content Recommendations

Internal_Link_Content_Recommendations.csv

### Content Performance KPI Framework

Content_Performance_KPI_Framework.csv

All datasets must:

- Have consistent headers.
- Contain no malformed rows.
- Use verified source information.
- Include evidence where relevant.
- Clearly distinguish recommendations from facts.
- Use standardized priority values.
- Use standardized statuses.
- Avoid fabricated metrics.
- Avoid duplicate records.

---

## 9. OUTPUT FILES

### 1. Content_Strategy_Report.md

Complete strategic report.

### 2. Content_Audit_Report.md

Detailed analysis of existing website content.

### 3. Content_Gap_Analysis.csv

Content gaps.

### 4. Content_Opportunity_Analysis.csv

New and existing content opportunities.

### 5. Content_Keyword_Mapping.csv

Keyword-to-content mapping.

### 6. Topic_Cluster_Mapping.csv

Pillar and supporting topic cluster relationships.

### 7. Content_Prioritization.csv

Prioritized content opportunities.

### 8. Content_Calendar.csv

Publishing plan.

### 9. Content_Brief_Dataset.csv

Master content brief dataset.

### 10. Content_Refresh_Recommendations.csv

Existing content refresh recommendations.

### 11. Content_Consolidation_Recommendations.csv

Content consolidation recommendations.

### 12. Internal_Link_Content_Recommendations.csv

Content-level internal linking strategy.

### 13. Content_Performance_KPI_Framework.csv

Future performance measurement framework.

### 14. Developer_Prompt.md

Production-ready developer handoff prompt.

### 15. prompt.txt

Plain-text equivalent of Developer_Prompt.md.

### 16. Content Briefs

Detailed briefs for prioritized content assets.

### 17. Content Drafts

Complete SEO content drafts for selected high-priority opportunities.

### 18. Content_Validation_Report.md

Validation results.

### 19. Content_Quality_Checklist.csv

Quality assurance dataset.

### 20. Content_Execution_Log.md

Execution record.

### 21. Execution_Summary.md

Final execution summary.

---

## 10. EVIDENCE AND SOURCE RULES

1. Use verified information.
2. Maintain source references.
3. Record URLs.
4. Record source titles.
5. Record access dates.
6. Record the relevant evidence.
7. Record upstream report paths.
8. Distinguish facts from recommendations.
9. Distinguish measured metrics from estimates.
10. Distinguish external research from internal website data.
11. Do not invent search volume.
12. Do not invent keyword difficulty.
13. Do not invent traffic.
14. Do not invent rankings.
15. Do not invent conversions.
16. Do not invent competitor data.
17. Do not invent customer feedback.
18. Do not invent business claims.
19. Do not invent testimonials.
20. Do not invent case studies.

When data is unavailable:

- Mark it NOT_AVAILABLE.
- Document the reason.
- Identify the affected analysis.
- Explain the limitation.

---

## 11. EXECUTION RULES

1. Execute every stage sequentially.
2. Do not skip stages.
3. Read mandatory upstream reports before starting research.
4. Reuse previous datasets.
5. Do not unnecessarily repeat keyword research.
6. Perform additional research only where required.
7. Maintain evidence.
8. Maintain source references.
9. Maintain execution logs.
10. Use free tools first.
11. Do not purchase subscriptions.
12. Do not modify website source code.
13. Do not publish content.
14. Do not modify CMS.
15. Do not deploy.
16. Do not delete existing content.
17. Do not invent data.
18. Clearly mark incomplete work.
19. Validate every output.
20. Verify files before reporting completion.
21. Preserve previous execution outputs.
22. Use versioned execution folders when required.
23. Prioritize business relevance and search intent over keyword volume alone.
24. Content must provide genuine value to users.
25. Do not generate content solely to manipulate search rankings.
26. Do not produce thin, repetitive, or scaled low-value content.
27. Human expert review must be required for content involving specialized claims, legal matters, financial matters, healthcare, safety, or unverifiable technical claims.
28. Never claim content is published unless publication was explicitly authorized and verified.

---

## 12. FINAL VALIDATION CHECKLIST

Before marking the workflow complete, verify:

### Upstream Data

- [ ] SEO Audit Report discovered.
- [ ] Keyword Research Report discovered.
- [ ] Competitor Analysis Report discovered.
- [ ] On-Page SEO Report discovered.
- [ ] Relevant CSV files read.
- [ ] Upstream data inventory generated.
- [ ] Missing dependencies documented.

### Research

- [ ] Business analysis completed.
- [ ] Audience research completed.
- [ ] Existing content inventory completed.
- [ ] Search intent research completed.
- [ ] Content gap analysis completed.
- [ ] Competitor content analysis completed.
- [ ] Content opportunities discovered.
- [ ] Topic clusters identified.
- [ ] Keyword-to-content mapping completed.
- [ ] Content prioritization completed.

### Strategy

- [ ] Content calendar generated.
- [ ] Content briefs generated.
- [ ] Refresh recommendations generated.
- [ ] Consolidation recommendations generated.
- [ ] Internal linking strategy generated.
- [ ] KPI framework generated.

### Content Creation

- [ ] High-priority content drafts generated.
- [ ] Content satisfies search intent.
- [ ] Keywords are used naturally.
- [ ] Content is original.
- [ ] Content is useful.
- [ ] Unsupported claims removed.
- [ ] Citations verified.
- [ ] CTAs included where appropriate.
- [ ] Internal links verified.
- [ ] Human review requirements documented.

### Developer Handoff

- [ ] Developer_Prompt.md generated.
- [ ] prompt.txt generated.
- [ ] Both files contain equivalent instructions.
- [ ] Developer Prompt requires repository inspection.
- [ ] Developer Prompt does not assume source file paths.
- [ ] Approval before implementation is required.
- [ ] No implementation permission is implied.

### Validation

- [ ] Content_Strategy_Report.md exists.
- [ ] Content_Audit_Report.md exists.
- [ ] All required CSV files exist.
- [ ] CSV structure validated.
- [ ] Content briefs exist.
- [ ] Content drafts exist.
- [ ] Content_Validation_Report.md exists.
- [ ] Content_Quality_Checklist.csv exists.
- [ ] Execution logs exist.
- [ ] Execution summary exists.
- [ ] Evidence is traceable.
- [ ] No empty files.
- [ ] No fabricated data.
- [ ] All files are saved in the correct directory.

---

## 13. FINAL SUCCESS CRITERIA

The workflow is COMPLETED only when:

1. All mandatory upstream reports have been discovered and reviewed.
2. Existing website content has been audited.
3. Search intent and audience analysis have been completed.
4. Content gaps have been identified.
5. Content opportunities have been prioritized.
6. Topic clusters have been created.
7. Keyword-to-content mapping has been completed.
8. Content calendar has been generated.
9. Content briefs have been generated.
10. High-priority content drafts have been created.
11. Content refresh and consolidation recommendations have been generated.
12. Internal linking content strategy has been generated.
13. Content KPI framework has been generated.
14. Developer Prompt has been generated.
15. Plain-text prompt has been generated.
16. Validation has been completed.
17. All outputs have been verified.
18. Evidence and source references are traceable.
19. Execution summary has been generated.

If any requirement cannot be completed:

- Mark the workflow PARTIALLY_COMPLETED or BLOCKED.
- Document the missing requirement.
- Document the reason.
- Document the impact.
- Document the next action.

Never report COMPLETED when required deliverables are missing.

---

## 14. FINAL EXECUTION SUMMARY

At the end of the workflow, provide a concise summary containing:

- Website.
- Execution date.
- Workflow name.
- Status.
- Upstream workflows used.
- Number of existing pages audited.
- Number of content gaps identified.
- Number of content opportunities identified.
- Number of topic clusters.
- Number of content briefs created.
- Number of content drafts created.
- Number of content refresh recommendations.
- Number of consolidation recommendations.
- Number of prioritized content assets.
- Number of Developer Prompt files generated.
- Research tools used.
- Data limitations.
- Human review requirements.
- Output directory.
- Next recommended workflow.

The next workflow should be determined based on the completed Content Strategy outputs and the overall SEO orchestration plan.

END OF MASTER PROMPT.
