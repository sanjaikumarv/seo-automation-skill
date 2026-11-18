# COMPLETE SEO WORKFLOW MASTER ORCHESTRATOR

## Autonomous 13-Stage SEO Execution Pipeline

Execute the complete end-to-end SEO automation workflow in **STRICT SEQUENTIAL EXECUTION MODE** across all 13 specialized SEO stages.

---

> **EXECUTION PROTOCOL: INITIAL INTAKE → WORKFLOW DISCOVERY → ZERO-INTERRUPT EXECUTION → FINAL CONSOLIDATION**

1. **Initial Intake:** Collect the required project information before starting, unless the user has already provided it in the triggering message or existing workflow context.
2. **Workflow Discovery:** Before executing any SEO stage, locate and read all 13 individual stage prompts and their corresponding skill files.
3. **Execution Manifest:** Record the exact, verified file paths of every prompt and skill file. Never invent or assume file paths.
4. **Zero Mid-Run Questions:** After the initial intake is complete, execute Steps 1–13 continuously without stopping to request information already provided or discovered.
5. **Context Inheritance:** Every stage must automatically consume the initial project context and the outputs of all relevant completed stages.
6. **Missing Optional Data:** Do not interrupt execution for unavailable optional credentials, analytics access, or third-party account access. Document the limitation and continue with available evidence.
7. **Strict Sequential Execution:** Never execute two stages simultaneously. Complete, save, and verify the current stage before starting the next.
8. **Final Consolidation:** Step 13 must read and consolidate the reports from Steps 1–12. It must not repeat the entire SEO research and implementation workflow.
9. **No Website Modification in Step 13:** Step 13 generates a developer-ready implementation blueprint and coding-agent prompt. It does not directly modify the website.

---

# 1. INITIAL PROJECT INTAKE

Before starting Step 1, retrieve all available project details from the user's triggering message and current workflow context.

Do not ask the user to repeat information already supplied.

## Required project information

| #   | Field                        | Requirement                  | Description                                                        |
| --- | ---------------------------- | ---------------------------- | ------------------------------------------------------------------ |
| 1   | Target Website URL           | Required                     | Full website URL to audit and optimize                             |
| 2   | Business / Brand Name        | Required                     | Business or brand identity                                         |
| 3   | Frontend Technology Stack    | Required if not discoverable | Next.js, React, Astro, Vue, WordPress, etc.                        |
| 4   | Services / Products Offered  | Required                     | Core services, products, or business solutions                     |
| 5   | Target Keywords              | Recommended                  | User-provided seed keywords and priority search queries            |
| 6   | Target Geography             | Recommended                  | Countries, cities, or global target markets                        |
| 7   | Target Audience              | Optional                     | Industries, business sizes, customer personas, and decision-makers |
| 8   | Source Code Location         | Optional                     | Local project directory or accessible repository                   |
| 9   | Google Search Console Access | Optional                     | Search performance and indexing data                               |
| 10  | Google Analytics Access      | Optional                     | Traffic and conversion data                                        |
| 11  | Competitor Websites          | Optional                     | Competitors, if already known                                      |

### Intake rules

- Use the user's supplied information first.
- Discover the frontend stack from the source code when accessible.
- Discover additional relevant services and website pages during the audit.
- Discover competitors during Step 3.
- Discover and expand keywords during Step 2.
- Never fabricate missing business information, customer details, keywords, or geographical targets.
- If a required detail cannot be discovered and is essential to start the workflow, ask for that missing detail before beginning dependent work.
- Do not ask for optional credentials or information that is not necessary to continue.

### Initial intake request

If required information is missing, request only the missing information using this structure:

**Please provide the missing project information required to start the SEO workflow:**

1. Target Website URL
2. Business / Brand Name
3. Services / Products Offered
4. Target Keywords (if already available)

Frontend technology stack, source code location, target geography, and audience should be requested only when they cannot be discovered or reasonably proceeded with.

---

# 2. WORKFLOW DISCOVERY AND EXECUTION MANIFEST

Before running Step 1, discover the complete workflow structure.

The orchestrator must locate:

- All 13 individual SEO stage prompt files.
- All 13 corresponding skill files.
- Existing project context files.
- Existing SEO stage output reports.
- The workflow state or execution log, if present.

## 2.1 Expected stage prompt identifiers

Use these identifiers to locate the corresponding prompt files. They are search identifiers, not assumed file paths.

| Step | Expected prompt identifier              |
| ---- | --------------------------------------- |
| 1    | `website-seo-audit`                     |
| 2    | `seo-keyword-research`                  |
| 3    | `seo-competitor-analysis`               |
| 4    | `seo-strategy-planning`                 |
| 5    | `technical-seo-implementation`          |
| 6    | `on-page-seo-implementation`            |
| 7    | `content-seo`                           |
| 8    | `off-page-seo`                          |
| 9    | `local-seo-implementation`              |
| 10   | `schema-structured-data-implementation` |
| 11   | `seo-testing-validation`                |
| 12   | `seo-monitoring-reporting`              |
| 13   | `final-seo-implementation-prompt`       |

## 2.2 Corresponding skill discovery

For each stage:

1. Locate the corresponding skill directory.
2. Find its skill instruction file, such as `SKILL.md`.
3. Read the complete skill instructions.
4. Record the exact resolved file path.
5. Verify that the prompt and skill belong to the same SEO stage.
6. Identify any additional reference files required by that skill.
7. Record missing or inaccessible files as discovery failures.

Search the actual workspace and available agent skill directories. Do not assume every skill is located in `.agents/skills/`.

## 2.3 Execution manifest

Create an execution manifest before starting the SEO pipeline.

The manifest must include:

| Step | Stage                      | Prompt file path | Skill file path | Discovery status | Execution status |
| ---- | -------------------------- | ---------------- | --------------- | ---------------- | ---------------- |
| 1    | Website SEO Audit          | Verified path    | Verified path   | Pending          | Pending          |
| 2    | Keyword Research           | Verified path    | Verified path   | Pending          | Pending          |
| 3    | Competitor Analysis        | Verified path    | Verified path   | Pending          | Pending          |
| 4    | SEO Strategy & Planning    | Verified path    | Verified path   | Pending          | Pending          |
| 5    | Technical SEO              | Verified path    | Verified path   | Pending          | Pending          |
| 6    | On-Page SEO                | Verified path    | Verified path   | Pending          | Pending          |
| 7    | Content SEO                | Verified path    | Verified path   | Pending          | Pending          |
| 8    | Off-Page SEO               | Verified path    | Verified path   | Pending          | Pending          |
| 9    | Local SEO                  | Verified path    | Verified path   | Pending          | Pending          |
| 10   | Schema & Structured Data   | Verified path    | Verified path   | Pending          | Pending          |
| 11   | SEO Testing & Validation   | Verified path    | Verified path   | Pending          | Pending          |
| 12   | SEO Monitoring & Reporting | Verified path    | Verified path   | Pending          | Pending          |
| 13   | Final SEO Consolidation    | Verified path    | Verified path   | Pending          | Pending          |

**Important:**

- Replace all placeholder path descriptions with actual verified paths.
- Never display a placeholder as if it were a verified path.
- If multiple matching files exist, identify the correct one using its content and stage instructions.
- Do not silently substitute a different skill or prompt.
- If an essential stage prompt or skill is missing, report the exact missing dependency before starting the pipeline. Do not pretend that stage was executed.

---

# 3. PROJECT CONTEXT AND OUTPUT DIRECTORY MANAGEMENT

## 3.1 Dynamic project context

Create and maintain a single project context throughout the workflow.

The project context must contain:

- Project name
- Project slug
- Target website URL
- Business / brand name
- Services and products
- Frontend technology stack
- Target keywords
- Target geography
- Target audience
- Source code location
- Competitor information
- Relevant findings from completed stages
- References to all generated reports

All project-specific information must be dynamic.

**NEVER hardcode:**

- Website URLs
- Website names
- Brand names
- Company names
- Services
- Target keywords
- Competitors
- Target countries or cities
- Customer personas
- Technology stacks

Do not reuse context from a different project.

## 3.2 Output directory

Use the established SEO workflow output directory:

`C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs`

Create or reuse the project-specific parent directory using this convention:

`{PROJECT_SLUG}-{DD-MM-YYYY}`

Example structure:

```text
outputs/
└── {PROJECT_SLUG}-{DD-MM-YYYY}/
    ├── seo-audit/
    ├── seo-keyword-research/
    ├── seo-competitor-analysis/
    ├── seo-strategy-planning/
    ├── technical-seo-implementation/
    ├── on-page-seo-implementation/
    ├── content-seo/
    ├── off-page-seo/
    ├── local-seo-implementation/
    ├── schema-structured-data/
    ├── seo-testing-validation/
    ├── seo-monitoring-reporting/
    └── seo-final-implementation/
```

Rules:

1. Reuse the existing project/date parent directory if it exists.
2. Create missing stage directories only when necessary.
3. Do not create a different project folder for each stage.
4. Do not include timestamps or time values in folder or report filenames.
5. Before overwriting an existing report, inspect its contents.
6. Maintain one final Markdown report per stage.
7. Do not write reports into unrelated project directories.
8. Verify the saved file and its contents before marking the stage complete.

Each stage must follow its corresponding report naming convention:

`{PROJECT_SLUG}-{DD-MM-YYYY}-{STAGE_SLUG}-report.md`

Step 13 must save:

`{PROJECT_SLUG}-{DD-MM-YYYY}-seo-final-implementation-report.md`

---

# 4. AUTONOMOUS 13-STAGE EXECUTION PIPELINE

Execute all stages in the exact order below.

```text
┌──────────────────────────────────────────────────────────────┐
│            COMPLETE 13-STAGE SEO MASTER PIPELINE             │
└──────────────────────────────────────────────────────────────┘
                              │
                              ▼
                  [0. Initial Project Intake]
                              │
                              ▼
                  [Workflow Discovery]
                              │
                              ▼
                  [Execution Manifest]
                              │
                              ▼
             [1. Website SEO Audit]
                              │
                              ▼
             [2. SEO Keyword Research]
                              │
                              ▼
             [3. SEO Competitor Analysis]
                              │
                              ▼
             [4. SEO Strategy & Planning]
                              │
                              ▼
             [5. Technical SEO Implementation]
                              │
                              ▼
             [6. On-Page SEO Implementation]
                              │
                              ▼
             [7. Content SEO]
                              │
                              ▼
             [8. Off-Page SEO]
                              │
                              ▼
             [9. Local SEO]
                              │
                              ▼
             [10. Schema & Structured Data]
                              │
                              ▼
             [11. SEO Testing & Validation]
                              │
                              ▼
             [12. SEO Monitoring & Reporting]
                              │
                              ▼
             [13. Final SEO Consolidation]
                              │
                              ▼
              [FINAL IMPLEMENTATION BLUEPRINT]
                              │
                              ▼
                 [FINAL VERIFICATION]
```

---

# 5. STAGE-BY-STAGE EXECUTION INSTRUCTIONS

For every stage, follow this execution sequence:

1. Read the stage's verified prompt file.
2. Read its corresponding skill file.
3. Read any required reference files.
4. Load the initial project context.
5. Load relevant outputs from completed upstream stages.
6. Follow the stage prompt and skill instructions completely.
7. Use the tools specified by that stage.
8. Perform the required analysis and implementation planning.
9. Save the stage's final Markdown report.
10. Verify the report exists and contains the expected content.
11. Update the execution manifest and workflow state.
12. Pass the completed findings to the next dependent stage.
13. Only then begin the next stage.

Never skip a stage silently.

## STEP 1 — WEBSITE SEO AUDIT

**Expected prompt identifier:** `website-seo-audit`

**Expected skill identifier:** `seo-audit`

**Input sources:**

- Initial project context.
- Target website URL.
- Services and products.
- Target audience and geography, if available.
- Target keywords, if supplied.

**Execution:**

1. Audit the website's current SEO condition.
2. Crawl accessible website pages.
3. Inspect robots.txt and sitemap.xml.
4. Analyze indexability, crawlability, HTTPS, canonical tags, redirects, and status codes.
5. Inspect title tags, meta descriptions, headings, image alt text, and internal linking.
6. Evaluate mobile responsiveness and Core Web Vitals indicators.
7. Identify broken links, duplicate content, missing metadata, and technical errors.
8. Build a discovered URL and page inventory.
9. Record evidence, findings, severity, and limitations.

**Tools:** Screaming Frog, Google Search Console, Google PageSpeed Insights, Lighthouse, Google Rich Results Test, browser inspection, and suitable open-source alternatives.

**Output:**

`{PROJECT_FOLDER}/seo-audit/{PROJECT_SLUG}-{DATE}-seo-audit-report.md`

**Handoff:** Website baseline, URL inventory, technical issues, and SEO gaps to Steps 2–13.

---

## STEP 2 — SEO KEYWORD RESEARCH

**Expected prompt identifier:** `seo-keyword-research`

**Expected skill identifier:** `seo-keyword-research`

**Input sources:**

- Step 1 SEO audit report.
- Initial project context.
- Discovered pages and services.

**Execution:**

1. Research seed keywords.
2. Expand primary, secondary, long-tail, and local keywords.
3. Identify search intent.
4. Analyze keyword relevance and search demand where reliable data is available.
5. Identify question-based and informational queries.
6. Identify commercial and transactional opportunities.
7. Map keywords to existing URLs.
8. Identify keyword cannibalization and content gaps.
9. Recommend new pages where justified.

**Tools:** Google Keyword Planner, Google Trends, Google Search, Google Search Console, AnswerThePublic, AlsoAsked, and available open-source keyword research tools.

**Output:**

`{PROJECT_FOLDER}/seo-keyword-research/{PROJECT_SLUG}-{DATE}-seo-keyword-research-report.md`

**Handoff:** Keyword clusters, search intent, keyword-to-page mapping, and content opportunities to Steps 3, 4, 6, 7, and 9.

---

## STEP 3 — SEO COMPETITOR ANALYSIS

**Expected prompt identifier:** `seo-competitor-analysis`

**Expected skill identifier:** `seo-competitor-analysis`

**Input sources:**

- Step 1 SEO audit.
- Step 2 keyword research.
- Initial project context.

**Execution:**

1. Identify relevant organic search competitors.
2. Distinguish direct business competitors from SEO competitors.
3. Analyze competitor website structure and landing pages.
4. Compare keyword rankings and content coverage where data is available.
5. Identify competitor backlink profiles and referring domains.
6. Analyze competitor content strategies.
7. Identify keyword gaps and content gaps.
8. Identify competitor strengths, weaknesses, and opportunities.
9. Create a competitor comparison report.

**Tools:** Google Search, Ahrefs free tools, Semrush free tools, Moz Link Explorer, Similarweb, Screaming Frog, and available open-source alternatives.

**Output:**

`{PROJECT_FOLDER}/seo-competitor-analysis/{PROJECT_SLUG}-{DATE}-seo-competitor-analysis-report.md`

**Handoff:** Competitor insights, keyword gaps, backlink opportunities, and content opportunities to Steps 4, 7, and 8.

---

## STEP 4 — SEO STRATEGY & PLANNING

**Expected prompt identifier:** `seo-strategy-planning`

**Expected skill identifier:** `seo-strategy-planning`

**Input sources:**

- Steps 1–3 reports.
- Initial project context.

**Execution:**

1. Consolidate the audit, keyword, and competitor findings.
2. Define SEO objectives.
3. Define primary and secondary target audiences.
4. Prioritize target keywords and pages.
5. Build a page-level SEO strategy.
6. Define content clusters and topical authority opportunities.
7. Create a technical SEO improvement roadmap.
8. Define on-page and off-page priorities.
9. Define local SEO priorities where relevant.
10. Create a prioritized implementation roadmap.

**Tools:** Existing stage reports, Google Search, Google Search Console, spreadsheets, and appropriate analysis tools.

**Output:**

`{PROJECT_FOLDER}/seo-strategy-planning/{PROJECT_SLUG}-{DATE}-seo-strategy-planning-report.md`

**Handoff:** Prioritized SEO strategy, objectives, implementation roadmap, and page priorities to Steps 5–13.

---

## STEP 5 — TECHNICAL SEO IMPLEMENTATION

**Expected prompt identifier:** `technical-seo-implementation`

**Expected skill identifier:** `technical-seo-implementation`

**Input sources:**

- Step 1 audit.
- Step 4 strategy.
- Source code, if accessible.

**Execution:**

1. Analyze technical SEO problems.
2. Inspect robots.txt, sitemap.xml, canonicalization, redirects, and HTTP status codes.
3. Inspect rendering and indexability.
4. Analyze performance and Core Web Vitals opportunities.
5. Identify server configuration and caching issues.
6. Review mobile usability and responsive behavior.
7. Provide framework-specific technical implementation recommendations.
8. Identify exact source files when source code is accessible.
9. Provide safe code changes or implementation specifications.
10. Record validation requirements.

**Tools:** Screaming Frog, Google Search Console, PageSpeed Insights, Lighthouse, Chrome DevTools, HTTP inspection tools, schema validators, Git, and available project build/test tools.

**Output:**

`{PROJECT_FOLDER}/technical-seo-implementation/{PROJECT_SLUG}-{DATE}-technical-seo-implementation-report.md`

**Handoff:** Technical SEO findings, recommended fixes, verified file paths, and validation instructions to Steps 6, 10, 11, and 13.

---

## STEP 6 — ON-PAGE SEO IMPLEMENTATION

**Expected prompt identifier:** `on-page-seo-implementation`

**Expected skill identifier:** `on-page-seo-implementation`

**Input sources:**

- Steps 1–5 reports.
- Existing page inventory.
- Keyword-to-page mapping.
- Source code, if accessible.

**Execution:**

1. Optimize title tags and meta descriptions.
2. Define H1, H2, and H3 hierarchy.
3. Optimize URLs where justified.
4. Improve image alt text.
5. Recommend internal linking improvements.
6. Improve page-level keyword relevance.
7. Identify missing content sections.
8. Recommend semantic HTML improvements.
9. Generate page-specific metadata and on-page specifications.
10. Identify exact source files when possible.

**Tools:** Google Search, Google Search Console, Screaming Frog, Rich Results Test, browser inspection, and source-code tools.

**Output:**

`{PROJECT_FOLDER}/on-page-seo-implementation/{PROJECT_SLUG}-{DATE}-on-page-seo-implementation-report.md`

**Handoff:** Page-level optimization specifications to Steps 7, 10, 11, and 13.

---

## STEP 7 — CONTENT SEO

**Expected prompt identifier:** `content-seo`

**Expected skill identifier:** `content-seo`

**Input sources:**

- Steps 1–6 reports.
- Keyword-to-page mapping.
- Competitor content gaps.
- SEO strategy.

**Execution:**

1. Analyze existing content quality.
2. Identify missing or thin content.
3. Identify content opportunities based on search intent.
4. Plan service pages, landing pages, blogs, and supporting content.
5. Create content briefs.
6. Generate or recommend publication-ready content where requested by the stage prompt.
7. Optimize headings, keyword placement, semantic relevance, and FAQs.
8. Identify internal linking opportunities.
9. Avoid keyword stuffing and duplicate content.
10. Map every proposed content change to its target URL.

**Tools:** Google Search Console, Google Keyword Planner, Google Trends, Google Search, GA4, AnswerThePublic, AlsoAsked, Screaming Frog, Google Search Central, and appropriate open-source analysis tools.

**Output:**

`{PROJECT_FOLDER}/content-seo/{PROJECT_SLUG}-{DATE}-content-seo-report.md`

**Handoff:** Content briefs, replacement copy, new content recommendations, and URL mappings to Steps 9, 10, 11, and 13.

---

## STEP 8 — OFF-PAGE SEO

**Expected prompt identifier:** `off-page-seo`

**Expected skill identifier:** `off-page-seo`

**Input sources:**

- Steps 1–7 reports.
- Competitor backlink findings.
- Initial business context.

**Execution:**

1. Analyze available backlink data.
2. Identify referring domain opportunities.
3. Identify competitor backlink gaps.
4. Review anchor text distribution where data is available.
5. Identify potentially harmful or suspicious links without making unsupported claims.
6. Develop relevant link-building opportunities.
7. Plan digital PR and brand mention reclamation.
8. Recommend industry directories and relevant partnerships.
9. Create a sustainable off-page SEO roadmap.

**Tools:** Ahrefs free tools, Moz Link Explorer, Semrush free tools, Google Search, Bing Webmaster Tools, and appropriate open-source tools.

**Output:**

`{PROJECT_FOLDER}/off-page-seo/{PROJECT_SLUG}-{DATE}-off-page-seo-report.md`

**Handoff:** Backlink opportunities, authority-building strategy, and outreach recommendations to Steps 9, 12, and 13.

---

## STEP 9 — LOCAL SEO

**Expected prompt identifier:** `local-seo-implementation`

**Expected skill identifier:** `local-seo-implementation`

**Input sources:**

- Initial geography and business information.
- Steps 1–8 reports.
- Local keyword mappings.
- Source code, if accessible.

**Execution:**

1. Determine whether local SEO is relevant to the business.
2. Audit available Google Business Profile information.
3. Review business name, address, and phone consistency where information is available.
4. Analyze local search competitors.
5. Review local keyword opportunities.
6. Recommend location-specific landing pages where justified.
7. Develop local citation and review strategies.
8. Identify local schema opportunities.
9. Provide local SEO implementation specifications.

**Tools:** Google Business Profile, Google Maps, Google Search, Google Search Console, Google Keyword Planner, Google Trends, Bing Places, Screaming Frog, and appropriate open-source tools.

**Output:**

`{PROJECT_FOLDER}/local-seo-implementation/{PROJECT_SLUG}-{DATE}-local-seo-implementation-report.md`

**Handoff:** Local keyword strategy, business information requirements, location-page recommendations, and local SEO specifications to Steps 10, 11, and 13.

---

## STEP 10 — SCHEMA & STRUCTURED DATA IMPLEMENTATION

**Expected prompt identifier:** `schema-structured-data-implementation`

**Expected skill identifier:** `schema-structured-data-implementation`

**Input sources:**

- Steps 1–9 reports.
- Existing website content.
- Verified business information.
- Source code, if accessible.

**Execution:**

1. Audit existing structured data.
2. Identify missing or invalid schema.
3. Select appropriate schema types based on actual page content.
4. Prepare Organization, WebSite, WebPage, Service, BreadcrumbList, Article, and other applicable schemas.
5. Prepare LocalBusiness schema only when supported by verified business information.
6. Ensure structured data matches visible website content.
7. Identify exact files and components for implementation where source code is accessible.
8. Provide JSON-LD implementation specifications.
9. Document validation requirements.

**Tools:** Schema.org Validator, Google Rich Results Test, Screaming Frog, Google Search Console, Chrome DevTools, and source-code tools.

**Output:**

`{PROJECT_FOLDER}/schema-structured-data/{PROJECT_SLUG}-{DATE}-schema-structured-data-report.md`

**Handoff:** Schema specifications and validation requirements to Steps 11 and 13.

---

## STEP 11 — SEO TESTING & VALIDATION

**Expected prompt identifier:** `seo-testing-validation`

**Expected skill identifier:** `seo-testing-validation`

**Input sources:**

- Steps 1–10 reports.
- Source code, if accessible.
- Existing implementation evidence.

**Execution:**

1. Validate technical SEO recommendations.
2. Validate metadata and heading structures.
3. Validate canonical tags and redirects.
4. Validate sitemap.xml and robots.txt.
5. Validate structured data.
6. Check internal links and broken links.
7. Review mobile usability and performance.
8. Validate indexability and rendering.
9. Run available build, lint, and test commands when source code is accessible.
10. Separate verified results from recommendations that have not yet been implemented.
11. Record failures, warnings, and unresolved issues.

**Tools:** Screaming Frog, Google PageSpeed Insights, Lighthouse, Chrome DevTools, Google Search Console, Rich Results Test, Playwright, and available project build/lint/test tools.

**Output:**

`{PROJECT_FOLDER}/seo-testing-validation/{PROJECT_SLUG}-{DATE}-seo-testing-validation-report.md`

**Handoff:** Verified issues, test results, unresolved risks, and validation evidence to Steps 12 and 13.

---

## STEP 12 — SEO MONITORING & REPORTING

**Expected prompt identifier:** `seo-monitoring-reporting`

**Expected skill identifier:** `seo-monitoring-reporting`

**Input sources:**

- Steps 1–11 reports.
- Available Google Search Console data.
- Available GA4 data.
- Existing SEO performance data.

**Execution:**

1. Define SEO performance KPIs.
2. Establish an organic traffic monitoring framework.
3. Define keyword ranking and visibility tracking.
4. Track impressions, clicks, CTR, and average position when data is available.
5. Define conversion tracking requirements.
6. Identify pages requiring ongoing optimization.
7. Prepare a reporting dashboard specification.
8. Define weekly and monthly monitoring activities.
9. Create a future SEO improvement roadmap.
10. Clearly document unavailable analytics data and measurement limitations.

**Tools:** Google Search Console, Google Analytics 4, Looker Studio, Google PageSpeed Insights, Bing Webmaster Tools, Screaming Frog, Google Trends, and available backlink tools.

**Output:**

`{PROJECT_FOLDER}/seo-monitoring-reporting/{PROJECT_SLUG}-{DATE}-seo-monitoring-reporting-report.md`

**Handoff:** KPIs, baseline metrics, reporting specifications, and ongoing SEO roadmap to Step 13.

---

## STEP 13 — FINAL SEO CONSOLIDATION & IMPLEMENTATION BLUEPRINT

**Expected prompt identifier:** `final-seo-implementation-prompt`

**Expected skill identifier:** `final-seo-implementation`

**Input sources:**

All reports generated in Steps 1–12.

**Execution:**

1. Read all 12 completed SEO reports.
2. Consolidate all findings, issues, recommendations, and implementation requirements.
3. Resolve duplicate recommendations and identify conflicting recommendations.
4. Prioritize implementation tasks using P1, P2, P3, and P4.
5. Create a URL-by-URL implementation blueprint.
6. Specify exact metadata, heading, content, internal linking, and schema changes.
7. Specify image optimization requirements, including verified image paths, dimensions, compression, and replacement recommendations where evidence exists.
8. Identify exact source files and components to modify when source code is accessible.
9. Identify new pages, components, or files that need to be created.
10. Distinguish verified file paths from proposed file paths.
11. Generate a ready-to-use production implementation prompt for a coding agent.
12. Include implementation order, dependencies, acceptance criteria, and testing requirements.
13. Record unresolved questions and limitations.
14. Save the complete final SEO implementation report.

**Important restrictions:**

- Do not rerun Steps 1–12.
- Do not repeat keyword research, competitor research, or the full audit.
- Do not fabricate metrics, rankings, URLs, file paths, business claims, or image details.
- Do not modify the website source code in this stage.
- Use all previous stage reports as the primary evidence.
- Inspect source code only when necessary to identify exact implementation files.
- Preserve the distinction between verified facts, recommendations, and assumptions.

**Tools:** Previous stage Markdown reports, available project files, source-code inspection tools, and document analysis tools.

**Output:**

`{PROJECT_FOLDER}/seo-final-implementation/{PROJECT_SLUG}-{DATE}-seo-final-implementation-report.md`

**Final deliverable:** One complete, developer-ready SEO implementation blueprint with a coding-agent prompt.

---

# 6. STRICT SEQUENTIAL EXECUTION RULES

The orchestrator must follow these rules throughout the entire workflow.

### Rule 1 — No parallel stage execution

Never start Step N+1 until Step N has been completed, saved, and verified.

### Rule 2 — Read both prompt and skill

Every stage must use its own individual prompt file and corresponding skill file. Do not replace either with a summary or generic SEO knowledge.

### Rule 3 — Context inheritance

Every stage must inherit:

- Initial project information.
- All relevant upstream findings.
- Existing verified project details.
- Previous stage recommendations.
- Relevant file and URL inventories.

Do not ask the user to repeat existing context.

### Rule 4 — Preserve evidence

Every report must distinguish:

- Verified observations.
- Tool-derived results.
- Recommendations.
- Unverified assumptions.
- Access limitations.
- Pending implementation work.

### Rule 5 — Tool execution

Use the tools specified by each individual stage prompt and skill.

Prefer free and open-source tools where possible. Verify access and tool availability before relying on a tool. Do not claim a tool was executed if it was not.

### Rule 6 — Error handling

If a tool fails:

1. Record the failure.
2. Record its impact.
3. Try an appropriate available alternative when possible.
4. Continue with the evidence available.
5. Do not fabricate results to fill missing information.

### Rule 7 — Report verification

Before proceeding to the next stage:

1. Confirm the report exists.
2. Confirm it contains the expected sections and findings.
3. Confirm it belongs to the correct project.
4. Confirm the output path is correct.
5. Update the execution manifest.

### Rule 8 — No cross-project contamination

Never use another project's reports, keywords, competitors, website details, or output folders as current project evidence.

---

# 7. WORKFLOW STATE MANAGEMENT

Maintain a workflow state file in the current project's output directory.

Suggested file:

`pipeline-state.json`

Track:

- Project identity.
- Initial input values.
- Workflow discovery results.
- Prompt and skill paths.
- Current stage.
- Completed stages.
- Failed stages.
- Report paths.
- Tool failures.
- Execution timestamps in the state file only.
- Final completion status.

Example state structure:

```json
{
  "project": {
    "name": "DYNAMIC_PROJECT_NAME",
    "slug": "DYNAMIC_PROJECT_SLUG",
    "website_url": "DYNAMIC_WEBSITE_URL"
  },
  "workflow": {
    "total_stages": 13,
    "execution_mode": "STRICT_SEQUENTIAL",
    "current_stage": 1,
    "status": "IN_PROGRESS"
  },
  "stages": [
    {
      "step": 1,
      "name": "website-seo-audit",
      "status": "PENDING",
      "prompt_path": "VERIFIED_PROMPT_PATH",
      "skill_path": "VERIFIED_SKILL_PATH",
      "report_path": "EXPECTED_REPORT_PATH"
    }
  ]
}
```

The example is a structure only. Populate actual project values and verified paths at runtime.

Do not mark a stage as `COMPLETED` until its report has been saved and verified.

If execution is interrupted, inspect the state file and existing reports before resuming. Resume from the first incomplete stage without rerunning verified completed stages unless the user explicitly requests a fresh execution.

---

# 8. FINAL VERIFICATION

After Step 13 completes, verify that all 13 stage reports exist.

Expected deliverables:

1. Website SEO Audit Report
2. SEO Keyword Research Report
3. SEO Competitor Analysis Report
4. SEO Strategy & Planning Report
5. Technical SEO Implementation Report
6. On-Page SEO Implementation Report
7. Content SEO Report
8. Off-Page SEO Report
9. Local SEO Report
10. Schema & Structured Data Report
11. SEO Testing & Validation Report
12. SEO Monitoring & Reporting Report
13. Final SEO Implementation Blueprint

Verify:

- All 13 stage reports exist.
- All reports belong to the correct project.
- All reports are saved in their respective stage directories.
- No stage was skipped silently.
- The execution manifest contains verified prompt and skill paths.
- The final blueprint references the findings from Steps 1–12.
- The final coding-agent prompt is included in the Step 13 report.
- The pipeline state is updated accurately.

Only mark the workflow as `COMPLETED` if all required stages and final verification have succeeded.

If a stage could not complete, mark the workflow as `PARTIALLY_COMPLETED` or `FAILED`, as appropriate, and identify the exact reason.

---

# 9. FINAL EXECUTION SUMMARY

After completing the pipeline, display a concise summary:

## SEO Workflow Execution Summary

**Project:** Dynamically retrieved project name

**Website:** Dynamically retrieved website URL

**Execution Mode:** STRICT SEQUENTIAL

**Total Stages:** 13

**Completed Stages:** Actual count

**Failed / Incomplete Stages:** Actual count

**Reports Generated:** Actual count

**Final Blueprint:** Verified report path

**Workflow Status:** Actual status

Also display:

1. The execution manifest location.
2. The output directory.
3. Any unavailable tools or access limitations.
4. Any incomplete tasks.
5. The final SEO implementation blueprint location.

Do not claim that any report, tool execution, or implementation succeeded without verifying it.

---

# FINAL ORCHESTRATOR COMMAND

When this master prompt is invoked:

1. Retrieve the available project context.
2. Collect only missing required initial inputs.
3. Discover all 13 individual SEO prompts and their corresponding skills.
4. Read and verify every discovered prompt and skill.
5. Create the execution manifest.
6. Prepare the project-specific output directory.
7. Execute Steps 1–13 strictly sequentially.
8. Save and verify each stage report before moving forward.
9. Maintain context and report handoffs throughout execution.
10. Generate the final developer-ready implementation blueprint in Step 13.
11. Verify all deliverables.
12. Display the final execution summary.

**The objective is to execute the complete 13-stage SEO workflow autonomously, with reliable context inheritance, verified file paths, evidence-based findings, and a final actionable implementation blueprint.**
