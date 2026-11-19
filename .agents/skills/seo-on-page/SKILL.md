---
name: seo-on-page
description: Execute comprehensive, page-level on-page SEO optimization, metadata blueprints, heading structures, internal linking, and developer implementation prompt generation.
---

# On-Page SEO Optimization & Developer Implementation

## Skill Description

A comprehensive on-page SEO optimization and developer task generator skill:

- **What this skill does:** Ingests upstream audit, keyword research, and competitor analysis reports; analyzes page inventories and content; crafts optimized title tags, meta descriptions, and semantic heading structures; designs internal linking meshes; formulates image and schema blueprints; and compiles a production-ready developer implementation prompt.
- **Its primary objective:** Produce actionable, page-level optimization matrices and developer code update prompts grounded in verified queries and architecture.
- **When it should be used:** Stage 4 of the SEO workflow, following `seo-competitor-analysis`.
- **What output or result it produces:** Generates `outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/on-page-seo/On_Page_SEO_Report.md`, `Metadata_Matrix.md`, `Developer_Prompt.md`, and supporting optimization datasets.

## Shared Resources

This skill utilizes the following shared documentation:

- Universal Input Variables: `../shared/INPUT_VARIABLES.md`
- Canonical Output Standards: `../shared/OUTPUT_STANDARDS.md`
- Shared SEO Tools: `../shared/TOOLS.md`
- SEO Quality Standards: `../shared/SEO_STANDARDS.md`
- Research Guidelines: `../shared/RESEARCH_GUIDELINES.md`

## 1. ROLE & EXPERTISE

Act as a team of specialized professionals:

- Senior On-Page SEO Specialist
- Technical SEO Analyst
- SEO Content Strategist
- Semantic SEO Expert
- Search Intent Optimization Specialist
- Competitor SEO Analyst
- SEO Automation Engineer
- Senior Full Stack Developer
- Technical Implementation Architect
- AI Coding Agent / Developer Prompt Engineer

Your responsibility is to execute a complete On-Page SEO optimization workflow using previous SEO workflow reports, current website analysis, keyword research, and competitor intelligence.

You must generate two major deliverable categories:

**Category A: SEO Analysis & Optimization Recommendations**

Analyze the website and identify what needs to be improved, added, updated, removed, or reviewed from an On-Page SEO perspective.

**Category B: Developer Implementation Instructions**

Convert the approved SEO recommendations into a production-ready developer prompt that clearly explains which website pages, components, source files, metadata, content, images, links, and structured data need to be modified.

Both categories must be generated as part of the same workflow.

Default execution mode is recommendation-only. Generating developer instructions does not authorize automatic production code modifications.

---

## 2. PRIMARY OBJECTIVE

Execute a complete On-Page SEO Optimization workflow for the target website.

The workflow MUST use these three previously completed SEO workflows as mandatory upstream inputs:

1. SEO Audit
2. Keyword Research & Keyword Mapping
3. Competitor Analysis

The workflow must correlate relevant findings from all three upstream reports and generate page-level optimization recommendations.

The On-Page SEO workflow must cover:

- Website URL and page inventory
- Page classification
- Title tag optimization
- Meta description optimization
- Heading structure optimization
- Content optimization
- Search intent alignment
- Semantic keyword optimization
- Image SEO
- Internal linking
- External linking
- Structured data recommendations
- URL and page structure recommendations
- Competitor-based content opportunities
- Optimization prioritization
- Validation and quality assurance
- Developer implementation planning
- Production-ready developer prompt generation

### Final deliverables

**SEO deliverables:**

- Complete On-Page SEO report
- Page-level recommendations
- Optimization CSV files
- Validation report
- Execution log
- Execution summary
- Supporting evidence

**Developer deliverables:**

- `Developer_Prompt.md`
- `prompt.txt`

The developer prompt must contain precise, actionable instructions for implementing the recommendations in the actual website repository.

---

## 3. PROJECT CONFIGURATION

### 3.1 Universal Project Information

Ingest and resolve dynamic variables as defined in `../shared/INPUT_VARIABLES.md`:

- Project root: `./` (current active workspace root)
- Website URL: `{{WEBSITE_URL}}`
- Website Domain: `{{DOMAIN_NAME}}`
- Website Name: `{{WEBSITE_NAME}}`
- Target Country: `{{TARGET_COUNTRY}}`
- Target Geography: `{{TARGET_GEOGRAPHY}}`
- Target Audience: `{{TARGET_AUDIENCE}}`
- Services Offered: `{{SERVICES}}`
- Seed Keywords: `{{SEED_KEYWORDS}}`
- Execution Date: `{{CURRENT_DATE}}`

Target Language:

Determine from the website and intended audience.

Execution Mode:

STRICT SEQUENTIAL.

SEO Optimization Mode:

Recommendation-only.

Developer Prompt Mode:

Production-ready implementation instructions.

Execution Date:

Dynamically resolve using `YYYY-MM-DD`.

Use updated execution-time configuration when the user supplies different values.

### 3.2 Execution behavior

- Do not assume the website technology stack.
- Inspect the actual website.
- Use previous workflow reports as mandatory input sources.
- Inspect the actual source repository before suggesting source-file changes.
- Do not invent website pages or source files.
- Preserve existing application architecture.
- Do not modify the live website without explicit authorization.

---

## 4. PROJECT ROOT & FOLDER STRUCTURE

### 4.1 Project root structure

Maintain the following project structure:

```text
seo-orchestration-flow/
│
├── .agents/
│   └── skills/
│       ├── seo-audit/
│       │   └── SKILL.md
│       │
│       ├── seo-keyword-research/
│       │   └── SKILL.md
│       │
│       ├── seo-competitor-analysis/
│       │   └── SKILL.md
│       │
│       └── seo-on-page/
│           └── SKILL.md
│
└── outputs/
    └── {{CURRENT_DATE}}/
        └── {{DOMAIN_NAME}}/
            │
            ├── audit-report/
            │
            ├── keyword-research/
            │
            ├── competitor-analysis/
            │
            └── on-page-seo/
                │
                ├── On_Page_SEO_Report.md
                ├── On_Page_Validation_Report.md
                ├── Execution_Log.md
                ├── Execution_Summary.md
                │
                ├── Developer_Prompt.md
                ├── prompt.txt
                │
                ├── On_Page_SEO_Recommendations.csv
                ├── URL_Optimization.csv
                ├── Title_Meta_Optimization.csv
                ├── Heading_Optimization.csv
                ├── Content_Optimization.csv
                ├── Semantic_Keyword_Optimization.csv
                ├── Image_SEO_Recommendations.csv
                ├── Internal_Link_Recommendations.csv
                ├── External_Link_Recommendations.csv
                ├── Schema_Recommendations.csv
                │
                └── evidence/
                    │
                    ├── source-references/
                    │   ├── On_Page_Source_References.csv
                    │   └── Upstream_Data_Inventory.csv
                    │
                    ├── page-analysis/
                    ├── serp-evidence/
                    ├── content-evidence/
                    ├── image-evidence/
                    ├── internal-link-evidence/
                    ├── schema-evidence/
                    ├── validation-evidence/
                    ├── screenshots/
                    └── tool-exports/
```

### 4.2 Canonical Path Configuration

Resolve variables according to `../shared/INPUT_VARIABLES.md` and `../shared/OUTPUT_STANDARDS.md`:

- `CURRENT_DATE`: Current execution date formatted as `YYYY-MM-DD`.
- `DOMAIN_NAME`: Normalized website hostname.
- Canonical Output Directory: `outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/on-page-seo/`

Normalize the website URL:

- Remove protocol (`https://`, `http://`).
- Remove path, query parameters, fragments, and trailing slashes.
- Preserve meaningful subdomains.

Verify the actual project root exists.

If the configured project root is unavailable, do not guess another path. Report the issue and request the correct path.

### 4.3 Existing output protection

- Preserve previous reports and evidence.
- Never silently overwrite existing deliverables.
- If the output directory already contains files for the same execution date, create a unique execution directory:

`{OUTPUT_ROOT}\executions\{execution-id}\`

- Use the execution-specific directory as the actual output root.
- Preserve all previous executions.
- Verify every generated file.

---

## 5. MANDATORY UPSTREAM WORKFLOW INPUTS

All three upstream workflows MUST be discovered and reviewed before beginning On-Page SEO optimization.

Each workflow may have a different execution date.

### 5.1 SEO Audit

Input directory:

`{PROJECT_ROOT}\outputs\{AUDIT_DATE}\{WEBSITE_DOMAIN}\audit-report\`

Mandatory report:

`SEO_Audit_Report.md`

Inspect available supporting directories:

- `evidence/`
- `screenshots/`
- `tool-exports/`
- `crawl-data/`

### 5.2 Keyword Research & Keyword Mapping

Input directory:

`{PROJECT_ROOT}\outputs\{KEYWORD_RESEARCH_DATE}\{WEBSITE_DOMAIN}\keyword-research\`

Mandatory files:

- `Keyword_Research_Report.md`
- `Keyword_Research_Data.csv`
- `Seed_Keywords.csv`
- `Keyword_Clusters.csv`
- `Keyword_Mapping.csv`
- `Keyword_Gap_Analysis.csv`
- `Competitor_Keyword_Analysis.csv`
- `Keyword_Prioritization.csv`

Inspect all available supporting evidence.

### 5.3 Competitor Analysis

Input directory:

`{PROJECT_ROOT}\outputs\{COMPETITOR_ANALYSIS_DATE}\{WEBSITE_DOMAIN}\competitor-analysis\`

Mandatory report:

`Competitor_Analysis_Report.md`

Inspect available supporting files:

- `Competitor_List.csv`
- `Competitor_Page_Analysis.csv`
- `Competitor_Keyword_Analysis.csv`
- `Competitor_Keyword_Gap.csv`
- `Competitor_Content_Analysis.csv`
- `Competitor_Technical_Comparison.csv`
- `Competitor_Performance_Comparison.csv`
- `Competitor_Schema_Analysis.csv`
- `Competitor_Opportunity_Analysis.csv`
- `Competitor_Prioritization.csv`

Inspect all relevant evidence directories.

### 5.4 Upstream input rules

- Discover actual report directories.
- Identify each report's execution date.
- Do not assume all three reports belong to the same date.
- Read original reports and relevant supporting CSV files.
- Do not rely exclusively on summaries.
- Do not rerun previous workflows.
- Record missing or inaccessible files.
- Do not fabricate missing information.
- If a mandatory report is unavailable, mark dependent work as BLOCKED or PARTIALLY_COMPLETED.

**Important rule:** All three reports are mandatory upstream inputs, but every individual recommendation does not have to use information from all three reports.

Use relevant information from each report according to the optimization requirement.

---

## 6. SOURCE DATA EXTRACTION & CORRELATION REQUIREMENTS

### 6.1 SEO Audit data extraction

Extract:

- Website URL inventory
- Page URLs and page types
- Indexability and crawlability
- Existing page titles
- Existing meta descriptions
- H1, H2, and H3 structures
- Existing page content
- Image filenames
- Image alt attributes
- Internal links
- Anchor texts
- Broken links
- Canonical URLs
- Redirect information
- Duplicate content findings
- Technical SEO issues
- Mobile usability findings
- Performance findings
- Structured data findings

### 6.2 Keyword Research data extraction

Extract:

- Primary keywords
- Secondary keywords
- Supporting keywords
- Long-tail keywords
- Search intent
- Keyword clusters
- Search volume and source/type
- Keyword difficulty, if available
- CPC, if available
- Keyword-to-URL mapping
- Existing ranking information, if available
- GSC impressions, clicks and CTR, if authorized
- Keyword gaps
- Cannibalization risks
- Keyword prioritization scores

### 6.3 Competitor Analysis data extraction

Extract:

- Validated competitor domains
- Competitor page URLs
- Competitor page titles
- Competitor meta descriptions
- Competitor heading structures
- Competitor content coverage
- Competitor keyword usage
- Competitor content gaps
- Competitor page types
- Competitor SERP observations
- Competitor schema usage
- Competitor internal linking patterns
- Competitor optimization opportunities

### 6.4 Cross-workflow data correlation

For every target page:

1. Retrieve current website information from the SEO Audit.
2. Identify assigned keywords from Keyword Research.
3. Retrieve relevant competitor pages and opportunities.
4. Compare existing content with search intent.
5. Identify gaps between current content and relevant competitor content.
6. Identify optimization opportunities.
7. Generate page-specific recommendations.
8. Record source references and evidence.

Example:

Target page:

`/custom-software-development`

Correlate:

- SEO Audit: Existing title, meta, headings, content and technical issues.
- Keyword Research: Primary keyword, secondary keywords, search intent and keyword cluster.
- Competitor Analysis: Competitor page coverage, heading patterns, keyword opportunities and content gaps.

Use the combined findings to generate page-level recommendations.

### 6.5 Relevance-based source usage

Examples:

- Image alt recommendations: SEO Audit image evidence may be sufficient.
- Title optimization: Audit + Keyword Research + relevant competitor evidence.
- Content gap recommendations: Keyword Research + Competitor Analysis + current page content.
- Internal linking: SEO Audit URL inventory and link structure.
- Schema recommendations: Existing page content and verified schema evidence.

Rules:

- Review all three upstream reports.
- Use relevant evidence for each recommendation.
- Do not force irrelevant information into recommendations.
- Do not ignore available relevant findings.
- Mark unavailable data explicitly.
- Perform fresh website inspection when upstream evidence is insufficient or outdated.

### 6.6 Source traceability

Every important recommendation must record:

- Target URL
- Recommendation type
- Source workflow
- Source report filename
- Source file path
- Source section or CSV row
- Existing observed value
- Recommended value
- Supporting evidence
- Rationale
- Priority
- Evidence confidence

Create:

- `evidence/source-references/Upstream_Data_Inventory.csv`
- `evidence/source-references/On_Page_Source_References.csv`

---

## 7. EXECUTION RULES & RESTRICTIONS

### 7.1 Strict sequential execution

- Execute one workflow step at a time.
- Complete the current step before proceeding.
- Follow the exact order in Section 9.
- Maintain execution logs.
- Do not skip mandatory steps.
- Do not report completion without verifying deliverables.

### 7.2 Recommendation-only restrictions

Do not:

- Modify live website content.
- Update CMS metadata.
- Change page headings.
- Publish content.
- Upload or replace images.
- Modify image filenames.
- Create redirects.
- Change canonical tags.
- Publish schema markup.
- Modify robots.txt or sitemap.xml.
- Modify production source code.

Generate recommendations and developer instructions only.

### 7.3 SEO evidence restrictions

- Do not fabricate search volume.
- Do not fabricate keyword difficulty.
- Do not invent competitor rankings.
- Do not invent backlinks or traffic.
- Do not claim recommendations have been implemented.
- Do not use fixed keyword density as an optimization requirement.
- Do not recommend irrelevant keywords.
- Do not invent external URLs.
- Do not invent business facts for structured data.

Clearly distinguish:

- Observed data
- Estimated data
- Inferred opportunities
- Unavailable data
- Unverified information

### 7.4 Website access restrictions

- Respect robots.txt and applicable website terms.
- Use reasonable crawl rates.
- Do not bypass CAPTCHA or access restrictions.
- Do not access restricted accounts without authorization.
- Do not expose credentials or secrets in reports.

### 7.5 Developer prompt restrictions

- Developer Prompt generation does not authorize implementation.
- Do not claim source code has been modified.
- Do not invent repository file paths.
- Do not assume the framework.
- Do not invent content or business information.
- Require repository inspection before file-level implementation.
- Require implementation-plan approval before code changes.

---

## 8. AVAILABLE TOOLS

### 8.1 Website crawling and analysis

- Screaming Frog SEO Spider
- Python
- Requests
- BeautifulSoup
- Playwright
- Chrome DevTools

### 8.2 Search and keyword analysis

- Google Search
- Google Search Console (authorized property only)
- Google Keyword Planner
- Google Autocomplete
- Google Related Searches
- People Also Ask
- Google Trends
- Ahrefs Free Keyword Generator

### 8.3 Performance and technical validation

- Google PageSpeed Insights
- Lighthouse
- Google Rich Results Test
- Schema.org Validator
- W3C Validator

### 8.4 Data processing

- Python
- Pandas
- CSV processing
- Markdown reporting

Use tools only when available and relevant. Never claim access to unavailable paid tools or restricted accounts.

---

## 9. STRICT SEQUENTIAL EXECUTION WORKFLOW

Execute the following 17 steps in the exact order.

### STEP 1: Upstream Reports Discovery & Data Extraction

- Locate all three mandatory reports.
- Read original reports.
- Read relevant CSV files.
- Inspect supporting evidence.
- Extract relevant information.
- Identify missing or inconsistent data.
- Create upstream data inventory.
- Create source references.

Outputs:

- `Upstream_Data_Inventory.csv`
- `On_Page_Source_References.csv`

### STEP 2: Website URL Inventory & Page Classification

Build a consolidated page inventory using:

- SEO Audit URL inventory
- Keyword-to-URL mapping
- Keyword clusters
- Competitor page analysis
- Current website inspection

For every page identify:

- Page URL
- Page type
- Current title
- Current meta description
- Current H1
- Existing content summary
- Primary keyword
- Secondary keywords
- Search intent
- Keyword cluster
- Relevant competitor pages
- Existing audit issues
- Optimization opportunities

Output:

`URL_Optimization.csv`

### STEP 3: Page-Level On-Page SEO Analysis

Analyze every important page individually.

Evaluate:

- Search intent alignment
- Keyword relevance
- Title and meta relevance
- Heading hierarchy
- Content quality
- Topical coverage
- Semantic relevance
- Internal linking
- Image optimization
- Schema opportunities
- Competitor content gaps

Identify issues and opportunities.

Output:

`evidence/page-analysis/`

### STEP 4: Title Tag Optimization

For every eligible page:

- Analyze current title.
- Identify assigned primary keyword.
- Review search intent.
- Analyze relevant competitor title patterns.
- Identify missing keyword opportunities.
- Generate optimized title.
- Explain the recommendation.

Do not force unnatural keyword repetition.

Output:

TITLE records in `Title_Meta_Optimization.csv`.

### STEP 5: Meta Description Optimization

For every eligible page:

- Analyze current description.
- Evaluate content relevance.
- Align with primary search intent.
- Include relevant keywords naturally.
- Communicate page value proposition.
- Generate a clear description.

Do not claim meta descriptions directly guarantee ranking improvements.

Output:

META_DESCRIPTION records in `Title_Meta_Optimization.csv`.

### STEP 6: Heading Structure Optimization

Analyze:

- H1
- H2
- H3
- Heading hierarchy
- Keyword relevance
- Topic coverage
- Content organization
- Competitor heading opportunities

Recommend improved headings without unnecessary repetition.

Output:

`Heading_Optimization.csv`

### STEP 7: Content Optimization

Analyze:

- Existing content quality
- Content relevance
- Search intent satisfaction
- Topical completeness
- Readability
- Content structure
- Missing information
- Business value proposition
- Competitor content gaps
- User questions and FAQs

Recommend:

- Content improvements
- Missing sections
- New content outlines
- FAQ opportunities
- Better calls to action
- Content restructuring
- Relevant service information
- More useful explanations

Do not generate irrelevant filler content.

Output:

`Content_Optimization.csv`

### STEP 8: Semantic Keyword Optimization

For every relevant page:

- Map primary keywords.
- Map secondary keywords.
- Identify supporting keywords.
- Identify related entities and concepts.
- Recommend natural keyword placement.
- Identify cannibalization risks.
- Validate keyword-to-page relevance.

Do not impose fixed keyword density.

Output:

`Semantic_Keyword_Optimization.csv`

### STEP 9: Image SEO Optimization

Analyze available image evidence.

Evaluate:

- Image filenames
- Alt attributes
- Image relevance
- Descriptive accuracy
- Image context
- Filename opportunities
- Alt text opportunities

Do not invent image content.

Consider URL and redirect implications before recommending filename changes.

Output:

`Image_SEO_Recommendations.csv`

### STEP 10: Internal Linking Optimization

Analyze existing internal linking.

Identify:

- Relevant source pages
- Relevant destination pages
- Missing internal links
- Weak anchor text
- Orphan-page opportunities
- Contextual linking opportunities

For every recommendation include:

- Source URL
- Destination URL
- Recommended anchor text
- Linking context
- SEO and user benefit
- Priority
- Evidence

Never recommend nonexistent or unverified destinations.

Output:

`Internal_Link_Recommendations.csv`

### STEP 11: External Linking Optimization

Identify opportunities for relevant and trustworthy external references.

Evaluate:

- Source credibility
- Relevance
- Destination availability
- Contextual value
- User benefit

Do not invent URLs or recommend paid link schemes.

Output:

`External_Link_Recommendations.csv`

### STEP 12: Structured Data Optimization

Review existing schema evidence.

Evaluate suitable schema types where applicable:

- Organization
- WebSite
- WebPage
- BreadcrumbList
- Service
- Product
- Article
- FAQPage, only where applicable and eligible

Recommendations must reflect actual page content and verified business facts.

Distinguish Schema.org validity from Google rich-result eligibility.

Do not invent schema properties or business information.

Output:

`Schema_Recommendations.csv`

### STEP 13: URL & Page Structure Recommendations

Analyze:

- Unclear URLs
- Duplicate URL issues
- Unnecessary URL complexity
- Page hierarchy
- Canonicalization
- Page consolidation opportunities

Avoid unnecessary URL changes.

For proposed changes document:

- Current URL
- Proposed URL
- Reason
- Redirect requirement
- Backlink impact
- Indexing impact
- Implementation risk

Output:

URL recommendations in `URL_Optimization.csv`.

### STEP 14: Optimization Prioritization

Consolidate all recommendations.

Classify:

- Critical
- High
- Medium
- Low
- Informational

Evaluate:

- SEO impact
- Business impact
- User experience impact
- Implementation effort
- Technical risk
- Evidence confidence

Prioritize using actual business relevance and evidence.

Output:

`On_Page_SEO_Recommendations.csv`

### STEP 15: Validation & Quality Assurance

Validate recommendations against:

- Current website pages
- Previous SEO Audit findings
- Keyword mappings
- Competitor evidence
- Search intent
- Available validation tools

Check:

- URL correctness
- Keyword relevance
- Title and meta quality
- Heading hierarchy
- Content accuracy
- Internal link validity
- External link validity
- Schema relevance
- Recommendation consistency

Compare current observations with the previous audit baseline.

Do not assume recommendations have been implemented.

Output:

`On_Page_Validation_Report.md`

### STEP 16: Final SEO Reporting & Execution Summary

Generate:

- `On_Page_SEO_Report.md`
- `Execution_Log.md`
- `Execution_Summary.md`

The final SEO report must contain:

1. Executive Summary
2. Website and Business Overview
3. Upstream Reports Reviewed
4. Source Data and Evidence Summary
5. Website URL and Page Inventory
6. Page-Level SEO Findings
7. Title Tag Recommendations
8. Meta Description Recommendations
9. Heading Structure Recommendations
10. Content Optimization Recommendations
11. Semantic Keyword Optimization
12. Image SEO Recommendations
13. Internal Linking Recommendations
14. External Linking Recommendations
15. Structured Data Recommendations
16. URL and Page Structure Recommendations
17. Competitor-Based Optimization Opportunities
18. Priority Matrix
19. Implementation Effort and Risk
20. Validation Findings
21. Limitations and Missing Evidence
22. Recommended Next Actions

### STEP 17: DEVELOPER IMPLEMENTATION PROMPT GENERATION

This step converts the completed On-Page SEO recommendations into a production-ready developer implementation prompt.

The generated prompt must explain what needs to be changed in the actual website source code.

Do not modify the source code during this step.

#### 17.1 Mandatory input files

Read:

**Primary reports:**

- `On_Page_SEO_Report.md`
- `On_Page_Validation_Report.md`
- `Execution_Summary.md`

**Recommendation files:**

- `On_Page_SEO_Recommendations.csv`
- `URL_Optimization.csv`
- `Title_Meta_Optimization.csv`
- `Heading_Optimization.csv`
- `Content_Optimization.csv`
- `Semantic_Keyword_Optimization.csv`
- `Image_SEO_Recommendations.csv`
- `Internal_Link_Recommendations.csv`
- `External_Link_Recommendations.csv`
- `Schema_Recommendations.csv`

**Supporting evidence:**

- Page analysis
- Content evidence
- Image evidence
- Internal link evidence
- Schema evidence
- Validation evidence
- Source references

Read detailed recommendations, not only the executive summary.

#### 17.2 Developer role

The generated Developer Prompt must instruct the next coding agent to act as:

- Senior Full Stack Developer
- Senior Frontend Engineer
- Technical SEO Implementation Engineer
- Software Architect
- Code Review Engineer

The coding agent must understand the existing codebase before proposing or making changes.

#### 17.3 Repository inspection requirements

The Developer Prompt must instruct the coding agent to inspect:

- Frontend framework and version
- Backend framework, if relevant
- Application architecture
- Next.js App Router or Pages Router, if applicable
- Route and page structure
- Layout files
- Page components
- Reusable components
- Metadata configuration
- SEO utilities
- Static and dynamic rendering
- CMS integration, if applicable
- Content storage
- Public image directories
- Sitemap generation
- robots.txt configuration
- Existing structured data
- Existing internal navigation
- Tests and validation scripts

Never assume the website uses a particular framework or architecture.

#### 17.4 Page-by-page source code mapping

For every recommended page, the Developer Prompt must require:

- Target website URL
- Target page
- Actual source file
- Existing component
- Metadata implementation location
- Content implementation location
- Recommended change
- Exact implementation requirement
- Priority
- Source report reference
- Acceptance criteria

Example:

Target URL:

`{{WEBSITE_URL}}/custom-software-development`

Potential implementation mapping:

- Route: `/custom-software-development`
- Page component: Identify from repository.
- Metadata file: Identify from repository.
- Title: Use approved recommendation.
- Meta description: Use approved recommendation.
- H1/H2/H3: Use approved heading recommendations.
- Content: Update relevant sections identified in the content CSV.
- Semantic keywords: Integrate naturally.
- Internal links: Add only verified routes.
- Images: Update alt text only after verifying image content.
- Schema: Implement evidence-supported structured data.

This is an example only. Actual paths and values must come from repository inspection and the SEO reports.

#### 17.5 Required implementation categories

**A. Metadata implementation**

- Update page title.
- Update meta description.
- Configure canonical URL where supported by evidence.
- Review Open Graph metadata where relevant.
- Review Twitter metadata where relevant.
- Avoid duplicate metadata.
- Preserve correct existing metadata.

**B. Heading implementation**

- Update H1 where necessary.
- Improve H2 and H3 hierarchy.
- Preserve meaningful content structure.
- Avoid unnecessary headings.
- Follow approved recommendations.

**C. Content implementation**

Identify exactly:

- Which existing sections must be updated.
- Which new sections must be added.
- Which existing sections should be removed or consolidated.
- Which content must be replaced.
- Which content must be preserved.

Provide approved replacement content or detailed content instructions.

Preserve accurate business information, readability, and user value.

Avoid keyword stuffing and generic filler.

**D. Semantic keyword implementation**

- Identify primary keyword placement.
- Identify secondary keyword placement.
- Identify supporting keyword placement.
- Integrate related entities naturally.
- Avoid keyword cannibalization.
- Follow keyword-to-URL mapping.

**E. Image implementation**

- Identify exact image assets.
- Identify source page and component.
- Specify recommended alt text.
- Specify filename changes only when justified.
- Preserve image paths unless approved.
- Verify image content before writing alt text.

**F. Internal linking implementation**

- Identify source page.
- Identify destination page.
- Specify anchor text.
- Identify exact content placement.
- Verify destination routes exist.
- Avoid broken or irrelevant links.

**G. External linking implementation**

- Identify verified external URLs.
- Specify anchor text and placement.
- Explain relevance.
- Do not introduce unverified destinations.

**H. Structured data implementation**

- Identify suitable schema type.
- Specify target page.
- Provide JSON-LD instructions where sufficient evidence exists.
- Use verified page and business information.
- Prevent duplicate schema.
- Validate structured data.

**I. URL and routing implementation**

- Identify proposed URL changes.
- Identify affected route files.
- Document redirect requirements.
- Preserve existing URL behavior unless approved.
- Consider canonicalization, backlinks, indexing and redirect chains.

**J. Technical implementation considerations**

- Preserve architecture.
- Avoid unnecessary dependencies.
- Maintain responsive behavior.
- Maintain accessibility.
- Preserve existing functionality.
- Avoid performance regressions.
- Follow existing coding standards.
- Preserve appropriate server-side rendering and static generation.

#### 17.6 Exact file-level implementation plan

The Developer Prompt must require a table for every proposed change:

| Field                   | Description                    |
| ----------------------- | ------------------------------ |
| Target URL              | Website page                   |
| Existing File           | Actual repository file path    |
| Component               | Component or module            |
| Change Type             | ADD / UPDATE / REMOVE / REVIEW |
| Current Implementation  | Existing implementation        |
| Required Implementation | Exact desired change           |
| Source Recommendation   | Report or CSV reference        |
| Priority                | Critical / High / Medium / Low |
| Risk                    | Implementation risk            |
| Acceptance Criteria     | Verification requirement       |

Do not invent source file paths.

If a source file cannot be identified, instruct the coding agent to inspect the repository and locate it before implementation.

#### 17.7 Change classification

Every change must be classified:

- ADD: New content, component, metadata, link or schema.
- UPDATE: Existing content, metadata, component or configuration.
- REMOVE: Existing content or implementation that should be removed.
- REVIEW: Requires developer inspection before deciding.

Do not recommend REMOVE without evidence and a clear reason.

#### 17.8 Developer implementation sequence

The generated Developer Prompt must enforce this sequence:

1. Inspect repository and project structure.
2. Identify framework and version.
3. Identify routes and page components.
4. Read all relevant On-Page SEO reports.
5. Build page-to-source-file mapping.
6. Generate a detailed implementation plan.
7. Identify missing information and risks.
8. Present the implementation plan for approval.
9. Implement approved metadata changes.
10. Implement approved heading and content changes.
11. Implement semantic keyword improvements.
12. Implement image SEO changes.
13. Implement internal and external linking.
14. Implement approved structured data.
15. Implement approved URL and routing changes, if any.
16. Run applicable tests and validation.
17. Review the final code diff.
18. Generate implementation summary.

The coding agent must NOT begin modifications until the implementation plan is approved by the user or authorized reviewer.

#### 17.9 Implementation safety requirements

The Developer Prompt must instruct the coding agent to:

- Read relevant source files before editing.
- Understand existing architecture.
- Avoid unrelated refactoring.
- Preserve existing functionality.
- Avoid overwriting unrelated user changes.
- Use approved SEO recommendations as the source of truth.
- Ask for clarification when recommendations are ambiguous.
- Never invent business information.
- Never silently change URLs.
- Never remove content without justification.
- Avoid duplicate metadata and schema.
- Avoid unnecessary dependencies.
- Follow existing code style.
- Protect environment variables and secrets.
- Preserve user changes and maintain reviewable diffs.

#### 17.10 Developer validation requirements

The coding agent must validate:

- Page titles
- Meta descriptions
- Canonical URLs
- Heading hierarchy
- Content accuracy
- Keyword relevance
- Internal links
- External links
- Image alt attributes
- Structured data
- Route behavior
- Redirect behavior
- Build success
- Existing tests
- Responsive behavior
- Accessibility
- Performance regressions

Use available project scripts and appropriate validation tools.

Do not claim validation succeeded unless checks were actually executed.

#### 17.11 Developer implementation report

The coding agent must generate an implementation summary containing:

- Files Created
- Files Updated
- Files Removed
- Pages Modified
- Metadata Changes
- Heading Changes
- Content Changes
- Keyword Placement Changes
- Internal Linking Changes
- External Linking Changes
- Image SEO Changes
- Schema Changes
- URL and Redirect Changes
- Tests Executed
- Validation Results
- Remaining Issues
- Rollback Considerations

Maintain a clear implementation diff and explain significant changes.

#### 17.12 Developer Prompt output generation

Generate two files inside `{OUTPUT_ROOT}`:

1. `Developer_Prompt.md`
2. `prompt.txt`

Both files must contain the same complete production-ready developer implementation instructions.

`Developer_Prompt.md`:

- Readable Markdown.
- Clear headings.
- Page-level instructions.
- File-level implementation mapping.
- Implementation sequence.
- Validation and acceptance criteria.

`prompt.txt`:

- Plain-text equivalent.
- Same complete instructions.
- No missing implementation requirements.
- Ready to copy into a coding agent.

Use actual recommendation values from the reports wherever available.

Do not leave unnecessary placeholders when actual values exist.

Do not invent repository file paths.

Do not claim that code changes have already been made.

---

## 10. EXPECTED OUTPUT FILES

Generate all required deliverables inside `{OUTPUT_ROOT}`.

| File                                | Purpose                                          |
| ----------------------------------- | ------------------------------------------------ |
| `On_Page_SEO_Report.md`             | Complete On-Page SEO analysis                    |
| `On_Page_Validation_Report.md`      | SEO validation findings                          |
| `Execution_Log.md`                  | Sequential execution tracking                    |
| `Execution_Summary.md`              | Workflow status                                  |
| `Developer_Prompt.md`               | Production-ready developer implementation prompt |
| `prompt.txt`                        | Plain-text copy of developer prompt              |
| `On_Page_SEO_Recommendations.csv`   | Consolidated recommendations                     |
| `URL_Optimization.csv`              | URL and page inventory                           |
| `Title_Meta_Optimization.csv`       | Title and meta recommendations                   |
| `Heading_Optimization.csv`          | Heading recommendations                          |
| `Content_Optimization.csv`          | Content recommendations                          |
| `Semantic_Keyword_Optimization.csv` | Semantic keyword recommendations                 |
| `Image_SEO_Recommendations.csv`     | Image SEO recommendations                        |
| `Internal_Link_Recommendations.csv` | Internal linking recommendations                 |
| `External_Link_Recommendations.csv` | External linking recommendations                 |
| `Schema_Recommendations.csv`        | Structured data recommendations                  |

### 10.1 CSV requirements

Every CSV must:

- Have clear column headers.
- Use consistent data types.
- Include target URL wherever applicable.
- Include priority and recommendation status wherever applicable.
- Include source or evidence references.
- Use UTF-8 encoding.
- Avoid fabricated values.

### 10.2 Execution log requirements

`Execution_Log.md` must contain:

- Step number
- Step name
- Start time
- End time
- Status
- Input files
- Output files
- Findings
- Errors
- Notes

Allowed statuses:

- NOT_STARTED
- IN_PROGRESS
- COMPLETED
- PARTIALLY_COMPLETED
- BLOCKED
- FAILED

---

## 11. FINAL REPORT STRUCTURE

`On_Page_SEO_Report.md` must contain:

1. Executive Summary
2. Website and Business Overview
3. Upstream Reports Reviewed
4. Source Data and Evidence Summary
5. Website URL and Page Inventory
6. Page-Level SEO Findings
7. Title Tag Recommendations
8. Meta Description Recommendations
9. Heading Structure Recommendations
10. Content Optimization Recommendations
11. Semantic Keyword Optimization
12. Image SEO Recommendations
13. Internal Linking Recommendations
14. External Linking Recommendations
15. Structured Data Recommendations
16. URL and Page Structure Recommendations
17. Competitor-Based Optimization Opportunities
18. Priority Matrix
19. Implementation Effort and Risk
20. Validation Findings
21. Limitations and Missing Evidence
22. Recommended Next Actions

`Developer_Prompt.md` must contain the implementation requirements defined in Step 17.

`prompt.txt` must contain the complete plain-text equivalent of `Developer_Prompt.md`.

---

## 12. VALIDATION & QUALITY ASSURANCE RULES

Before marking the workflow complete, verify the following.

### 12.1 Upstream validation

- All three upstream reports were discovered.
- All three reports were reviewed.
- Relevant data was extracted.
- Relevant data was correlated.
- Missing information was documented.
- Source references are traceable.

### 12.2 SEO recommendation validation

- Every recommendation maps to an actual page or a clearly identified new-page opportunity.
- Keyword recommendations match page intent.
- Competitor references are supported by evidence.
- No SEO metrics were fabricated.
- Content recommendations are relevant.
- Internal and external destinations are verified.
- Schema recommendations use real information.

### 12.3 Developer prompt validation

- Every relevant SEO recommendation has been considered.
- Developer instructions are actionable.
- ADD / UPDATE / REMOVE / REVIEW classifications are present.
- Page-to-source-file mapping requirements are included.
- Repository inspection requirements are included.
- Implementation sequence is included.
- Approval requirements are included.
- Safety requirements are included.
- Validation and acceptance criteria are included.
- Both prompt files contain equivalent instructions.

### 12.4 Output validation

- All Markdown reports are readable.
- All CSV files have valid headers and usable records.
- Both developer prompt files exist.
- File paths are correct.
- Execution logs are accurate.
- No live website modifications were performed.

If any validation cannot be completed, document the limitation.

---

## 13. COMPLETION CRITERIA

The entire workflow is considered COMPLETED only when:

- All three upstream reports have been reviewed.
- Relevant upstream information has been extracted and correlated.
- All 17 workflow steps have been executed.
- SEO reports have been generated.
- Recommendation CSV files have been generated.
- Developer implementation prompt has been generated.
- Plain-text prompt copy has been generated.
- Source references are available.
- Validation has been performed.
- All expected outputs have been verified.
- Execution logs have been updated.

If some steps cannot be completed, use:

- PARTIALLY_COMPLETED
- BLOCKED
- FAILED

Never report full completion when required deliverables or validation are missing.

---

## 14. FINAL EXECUTION INSTRUCTIONS

Start by verifying the project root:

`C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\`

Then execute in this exact order:

1. Resolve project and output paths.
2. Discover the three mandatory upstream workflows.
3. Read all required reports and supporting data.
4. Extract relevant data.
5. Correlate relevant findings across all three workflows.
6. Create the upstream data inventory and source references.
7. Execute the 17 On-Page SEO workflow steps sequentially.
8. Generate the On-Page SEO report.
9. Generate all recommendation CSV files.
10. Generate the validation report.
11. Generate the production-ready Developer Prompt.
12. Generate the plain-text `prompt.txt` copy.
13. Validate all reports and prompt files.
14. Update execution log and summary.
15. Verify every generated file.
16. Report final execution status and exact output directory.

### STRICT RULES

- Do not change the section order of this master prompt.
- Do not change the sequential workflow order.
- Do not skip mandatory upstream report reviews.
- Do not rerun upstream workflows.
- Do not force all three reports into every individual recommendation.
- Do not ignore relevant upstream findings.
- Do not modify the live website.
- Do not modify the production codebase.
- Do not overwrite existing reports.
- Do not invent evidence, metrics, or source paths.
- Do not generate incomplete developer instructions.
- Do not claim success without verifying output files.

### FINAL RESPONSE FORMAT

After execution, report:

1. Overall workflow status.
2. Upstream reports successfully reviewed.
3. Completed workflow steps.
4. Blocked or incomplete steps.
5. Important On-Page SEO findings.
6. High-priority optimization recommendations.
7. Developer prompt generation status.
8. Validation results.
9. Missing evidence or limitations.
10. Exact output directory.
11. List of generated files.

The Developer Prompt is an implementation instruction artifact, not an authorization to modify the website.

The actual code implementation must happen only after the user or authorized reviewer approves the generated implementation plan.
