---
name: seo-final-report
description: Synthesize all upstream SEO findings into a consolidated master report and compile a production-ready, framework-native developer implementation prompt.
---

# SEO Consolidated Final Report & Master Developer Implementation Prompt

## Skill Description

The capstone consolidation and developer handoff skill of the SEO automation suite:
- **What this skill does:** Audits and ingests deliverables from all 8 upstream SEO stages (`01-website-audit/` through `08-seo-monitoring/`); synthesizes comprehensive strategic findings; resolves technical, on-page, and schema priorities; and compiles the final master deliverables: an executive consolidated SEO report, a master website changes register, dedicated CSV implementation plans, and a production-ready Master Developer Implementation Prompt tailored to the website's tech stack.
- **Its primary objective:** Translate all analytical SEO research into actionable, high-ROI developer instructions and an executive scorecard without ungrounded speculation or fabricated metrics.
- **When it should be used:** Stage 9 (final stage) of the SEO automation workflow, after all preceding stages are completed.
- **What output or result it produces:** Generates `final-seo-overall-report.md`, `final-seo-website-changes.md`, `Master_Developer_Implementation_Prompt.md`, `seo-implementation-roadmap.md`, `seo-priority-matrix.csv`, and 7 dedicated CSV implementation plans in `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/09-final-seo-report/`.

## Shared Resources

This skill utilizes the following shared documentation:
- Universal Input Variables: `../shared/INPUT_VARIABLES.md`
- Canonical Output Standards: `../shared/OUTPUT_STANDARDS.md`
- Shared SEO Tools: `../shared/TOOLS.md`
- SEO Quality Standards: `../shared/SEO_STANDARDS.md`
- Research Guidelines: `../shared/RESEARCH_GUIDELINES.md`

## 1. Role

You are a Senior SEO Strategist, Technical SEO Engineer, Website Optimization Architect, and AI Developer Prompt Engineer.

Your responsibility is to analyze all completed SEO workflow stages (Stages 01 through 08), consolidate their findings, and generate the final suite of production-ready deliverables:

1. `final-seo-overall-report.md` (and legacy mirror `SEO_Consolidated_Final_Report.md`): High-level executive synthesis of all 8 upstream stages.
2. `final-seo-website-changes.md`: The single, definitive master register containing every exact code, content, metadata, heading, schema, and internal linking change required for the website.
3. `Master_Developer_Implementation_Prompt.md`: A framework-native, production-ready prompt that can be given directly to an AI coding agent or software engineering team to execute the changes in the codebase.
4. `seo-implementation-roadmap.md` & `seo-priority-matrix.csv`: Phased execution roadmap organized by sprint priority (P0 to P3).
5. Dedicated Implementation CSV Datasets: Granular machine-readable files for developers and content managers (`keyword-implementation-plan.csv`, `metadata-implementation-plan.csv`, `heading-implementation-plan.csv`, `content-implementation-plan.csv`, `technical-implementation-plan.csv`, `internal-linking-implementation-plan.csv`, `new-page-implementation-plan.csv`).

Do not stop after generating SEO recommendations. Convert all validated recommendations into an actionable developer execution specification.

---

## 2. Project Configuration

In accordance with `../shared/INPUT_VARIABLES.md`, ingest and resolve dynamic variables:

- Project root: `./` (current active workspace root)
- Output Root Folder: `OUT_PUT_ROOT_FOLDER` (**Default:** `C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs`)
- Website URL: `{{WEBSITE_URL}}`
- Website Domain: `{{DOMAIN_NAME}}`
- Website Name: `{{WEBSITE_NAME}}`
- Brand Name: `{{BRAND_NAME}}`
- Business Type: `{{BUSINESS_TYPE}}`
- Target Markets: `{{TARGET_COUNTRY}}` / `{{TARGET_GEOGRAPHY}}`
- Target Audience: `{{TARGET_AUDIENCE}}`
- Services Offered: `{{SERVICES}}`
- Seed Keywords: `{{SEED_KEYWORDS}}`
- Execution Date: `{{CURRENT_DATE}}` (YYYY-MM-DD)
- Canonical Output Directory: `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/09-final-seo-report/`
- Primary Language: English
- Execution Mode: Strict Sequential Analysis
- Tool Preference: Free tools first, wherever suitable.

All recommendations must be relevant to the actual website, business model, target audience, and validated SEO findings.

---

## 3. Upstream SEO Workflow Outputs

Discover the completed outputs from the following workflow stages under `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/` (or dynamically locate latest completed runs under `{OUT_PUT_ROOT_FOLDER}/*/{{DOMAIN_NAME}}/`):

| Stage | Canonical Folder | Legacy Fallback | Mandatory Inputs to Ingest |
|---|---|---|---|
| Stage 01 SEO Audit | `01-website-audit/` | `audit-report/` | `website-audit-overall-report.md`, `website-audit-website-changes.md`, `url-inventory.csv`, `technical-issues.csv` |
| Stage 02 Keyword Research | `02-keyword-research/` | `keyword-research/` | `keyword-research-overall-report.md`, `keyword-research-website-changes.md`, `Keyword_Mapping.csv`, `Keyword_Clusters.csv` |
| Stage 03 Competitor Analysis | `03-competitor-analysis/` | `competitor-analysis/` | `competitor-analysis-overall-report.md`, `competitor-analysis-website-changes.md`, `Competitor_Keyword_Gap.csv` |
| Stage 04 On-Page SEO | `04-on-page-seo/` | `on-page-seo/` | `on-page-seo-overall-report.md`, `on-page-seo-website-changes.md`, `Title_Meta_Optimization.csv`, `Heading_Optimization.csv` |
| Stage 05 Content Strategy | `05-content-strategy/` | `content-strategy/` | `content-strategy-overall-report.md`, `content-strategy-website-changes.md`, `Content_Calendar.csv`, `Topic_Cluster_Mapping.csv` |
| Stage 06 Technical SEO | `06-technical-seo/` | `technical-seo/` | `technical-seo-overall-report.md`, `technical-seo-website-changes.md`, `Technical_SEO_Implementation_Plan.csv` |
| Stage 07 Off-Page SEO | `07-off-page-seo/` | `off-page-seo/` | `off-page-seo-overall-report.md`, `off-page-seo-website-changes.md`, `Outreach_Strategy.md` |
| Stage 08 SEO Monitoring | `08-seo-monitoring/` | `seo-monitoring/` | `seo-monitoring-overall-report.md`, `seo-monitoring-website-changes.md`, `SEO_KPI_Framework.md` |

### Discovery requirements

1. Discover the actual directories for each completed stage.
2. Identify the latest valid completed execution for each stage.
3. Inspect the contents of the discovered folders.
4. Select only relevant reports, datasets, evidence, and supporting files.
5. Do not blindly read every file.
6. Do not assume that a file exists simply because its folder is listed above.
7. Record missing stages, unavailable evidence, and incomplete data.
8. Preserve the source of every important finding.
9. Do not silently invent missing SEO data.

Analyze all available completed stages collectively.

---

## 4. Project and Website Discovery

Before consolidating recommendations:

1. Discover the website project repository if it is available.
2. Identify the frontend and backend technologies where relevant.
3. Identify the website framework, routing architecture, rendering approach, and CMS.
4. Discover existing SEO implementation patterns.
5. Identify existing metadata configuration.
6. Identify sitemap and robots.txt implementation.
7. Identify existing structured data.
8. Identify image optimization and asset management patterns.
9. Identify existing page URLs and page templates.
10. Identify existing internal linking architecture.

Important:

The final SEO report must not assume that the website repository was inspected if it was not accessible.

If the repository is unavailable, clearly state that the developer prompt must perform repository discovery before making changes.

Do not make changes to the website during this reporting stage.

---

## 5. Consolidated SEO Analysis

Analyze the available findings across all completed stages.

Cover:

- Technical SEO.
- On-page SEO.
- Keyword research and keyword mapping.
- Content strategy and content quality.
- Competitor analysis.
- Internal linking.
- Off-page SEO.
- Backlink opportunities.
- Website performance.
- SEO monitoring and historical performance.
- Indexing and crawlability.
- Search intent alignment.
- Page-level optimization opportunities.

Identify:

1. Critical issues.
2. High-priority issues.
3. Medium-priority improvements.
4. Low-priority improvements.
5. Duplicate recommendations.
6. Conflicting recommendations.
7. Outdated findings.
8. Recommendations that lack sufficient evidence.
9. Opportunities that require additional research.

Prioritize recommendations using SEO impact, business relevance, implementation effort, risk, and available evidence.

---

## 6. Website Page-by-Page Improvement Analysis

For every relevant existing website page, identify:

- Page URL.
- Current page purpose.
- Target audience.
- Primary keyword.
- Secondary keywords.
- Search intent.
- Current SEO issues.
- Recommended title tag.
- Recommended meta description.
- Recommended H1.
- Recommended H2/H3 structure.
- Content improvements.
- Internal linking opportunities.
- Image optimization requirements.
- Structured data requirements, if applicable.
- Canonical URL requirements.
- Priority.
- Expected SEO benefit.
- Validation criteria.

Do not generate arbitrary metadata without considering keyword research, search intent, page purpose, and brand positioning.

---

## 7. Content Improvement and New Page Recommendations

Identify:

- Existing pages requiring content updates.
- Missing content sections.
- Thin or incomplete content.
- Content duplication.
- Search intent mismatches.
- Missing service pages.
- Missing industry-specific pages.
- Missing landing pages.
- Relevant blog and educational content opportunities.

For each new page recommendation, provide:

- Suggested URL slug.
- Page title.
- Primary keyword.
- Secondary keywords.
- Search intent.
- Target audience.
- Page purpose.
- Recommended content structure.
- Internal linking requirements.
- Relevant conversion goal.
- Priority.

Do not recommend creating duplicate or unnecessary pages solely to target more keywords.

---

## 8. Image Optimization Analysis

Identify images that require SEO or performance improvements.

For each relevant image, provide:

- Page URL.
- Image location or filename, if available.
- Current image format, if known.
- Recommended image format.
- Recommended filename.
- Recommended alt text.
- Appropriate image dimensions, if known.
- Compression requirements.
- Lazy-loading requirements.
- Priority.

Do not invent image filenames, image dimensions, or image locations when evidence is unavailable.

---

## 9. Technical SEO Implementation Analysis

Evaluate and recommend improvements for:

- XML sitemap.
- robots.txt.
- Canonical URLs.
- Meta robots directives.
- Indexability.
- Crawlability.
- Redirects.
- Broken links.
- HTTP status codes.
- Duplicate URLs.
- Structured data.
- Breadcrumbs.
- Mobile usability.
- Core Web Vitals.
- Image loading.
- Rendering and hydration issues where relevant.
- Page performance.
- URL structure.
- HTTPS and security-related SEO requirements.

Distinguish verified issues from recommendations requiring further inspection.

---

## 10. Internal Linking and Keyword Mapping

Generate a consolidated keyword-to-page mapping.

For each target keyword, identify:

- Keyword.
- Search intent.
- Target page.
- Existing or recommended page.
- Primary or secondary keyword classification.
- Related supporting keywords.
- Internal linking opportunities.
- Priority.

Identify:

- Pages without meaningful internal links.
- Relevant contextual linking opportunities.
- Potential orphan pages, if evidence supports them.
- Excessive or irrelevant linking.
- Anchor text improvements.

Avoid keyword cannibalization by assigning clear primary keyword ownership to pages.

---

## 11. Consolidation and Prioritization

Merge all relevant recommendations from the upstream stages.

For every recommendation:

1. Identify its source stage.
2. Verify supporting evidence.
3. Remove duplicates.
4. Resolve conflicts using evidence and current website context.
5. Identify dependencies.
6. Estimate implementation complexity.
7. Assign priority.
8. Define acceptance criteria.

Use the following priority levels:

- P0: Critical issues affecting indexing, accessibility to search engines, or major website functionality.
- P1: High-impact SEO improvements.
- P2: Medium-impact improvements.
- P3: Low-impact or optional improvements.

Do not assign expected ranking improvements, traffic increases, or revenue gains without defensible evidence.

---

# 12. MANDATORY MASTER DELIVERABLES

This skill must compile and physically generate the following core deliverables in `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/09-final-seo-report/`:

### 12.1 Master Deliverable 1: Consolidated Strategic Report (`final-seo-overall-report.md`)
*(Note: Maintain `SEO_Consolidated_Final_Report.md` as an identical mirror/alias if legacy consumers exist)*

A comprehensive executive-level master report synthesizing findings from all 8 upstream stages:
1. Executive Summary & SEO Maturity Scorecard
2. Analysis Scope & Upstream Workflow Audit Coverage (`01-website-audit/` through `08-seo-monitoring/`)
3. Overall SEO Health & Search Visibility Assessment
4. Critical P0 Vulnerabilities & Immediate Indexing Risks
5. Keyword Research & Search Intent Architecture Synthesis
6. Competitor Benchmarking & Organic Market Share Gaps
7. On-Page SEO Blueprint Summary (Metadata, Headings, Semantic Content)
8. Content Strategy & Topical Authority Roadmap (Clusters, Pillars, New Pages)
9. Technical SEO Infrastructure & Core Web Vitals Remediation Summary
10. Off-Page SEO, Digital PR & Authority Building Playbook
11. Continuous SEO Monitoring, KPI Framework & Governance
12. Consolidated Risk Assessment & Trade-off Analysis
13. Limitations, Unverified Assumptions & Verification Steps
14. Strategic Recommendations & Expected ROI Impact

---

### 12.2 Master Deliverable 2: Consolidated Website Changes Register (`final-seo-website-changes.md`)

The single, definitive, page-by-page master register consolidating EVERY website modification required across all stages. Must contain complete, copy-paste ready tables with the following schemas:

#### Table 1: Master Metadata Implementation Table
| Page URL | Existing Title Tag | Suggested Optimized Title Tag | Existing Meta Description | Suggested Optimized Meta Description | Target Primary Keyword | Target Secondary Keywords | Priority (P0-P3) | Action (UPDATE/ADD) |
|---|---|---|---|---|---|---|---|---|

#### Table 2: Master HTML Heading Updates Table
| Page URL | Section / Component Location | Existing Heading Tag & Text | Suggested Heading Tag & Text | Target Keyword | Hierarchy Context | Priority (P0-P3) | Action |
|---|---|---|---|---|---|---|---|

#### Table 3: Master Body Content Updates Table
| Page URL | Section / Component Location | Existing Content Snippet | Suggested Optimized Content / Copy | Target Keywords Incorporated | Word Count Delta | Priority (P0-P3) | Action |
|---|---|---|---|---|---|---|---|

#### Table 4: Master Technical Code & Configuration Fixes Table
| Issue ID | File / Component Path | Category (Robots/Sitemap/CWV/Routing/Headers) | Current Code / Directive | Suggested Code Fix / Production Directive | Technical Justification | Priority (P0-P3) | Action |
|---|---|---|---|---|---|---|---|

#### Table 5: Master Internal Linking Implementation Table
| Source Page URL | Target Page URL | Existing Anchor Text / Status | Suggested Anchor Text | Exact In-Content Link Sentence / Placement | Priority (P0-P3) | Action |
|---|---|---|---|---|---|---|

#### Table 6: Master JSON-LD Schema Engineering Table
| Target Page URL | Schema Type | Current Schema State | Complete Validated JSON-LD Code Block | Validation Method | Priority (P0-P3) |
|---|---|---|---|---|---|

#### Table 7: Master New Pages to Create Table
| Proposed URL / Slug | Page Type (Landing/Service/Pillar/Blog) | Topic Cluster | Primary & Secondary Keywords | Target Word Count | Outline & Section Hierarchy | Primary CTA & Destination | Priority (P0-P3) |
|---|---|---|---|---|---|---|---|

---

# 13. MASTER DELIVERABLE 3: Master Developer Implementation Prompt (`Master_Developer_Implementation_Prompt.md`)

This is a mandatory deliverable.

Generate:
`{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/09-final-seo-report/Master_Developer_Implementation_Prompt.md`
*(and plain-text copy `prompt.txt`)*

This file must contain a complete, production-oriented prompt that can be copied and given directly to an AI coding tool or software developer.

The prompt must instruct the developer AI to inspect the actual website repository, understand its existing architecture, and implement the validated SEO recommendations.

Do not merely copy the SEO report into this file. Convert the report findings into specific developer instructions.

## 13.1 Developer Prompt: Role and Objective

The developer AI must act as a:

- Senior Full Stack Developer.
- Technical SEO Engineer.
- Website Performance Engineer.
- Frontend Architecture Specialist.
- SEO Implementation and Validation Engineer.

Its objective is to implement the approved SEO changes in the existing website without unnecessarily changing existing functionality, architecture, or visual design.

## 13.2 Repository Discovery Instructions

The developer AI must first:

1. Inspect the complete project structure.
2. Identify the framework and framework version.
3. Identify the routing architecture.
4. Identify the rendering strategy.
5. Identify existing SEO-related packages and utilities.
6. Inspect existing page layouts and templates.
7. Inspect existing metadata implementation.
8. Inspect existing sitemap and robots.txt.
9. Inspect structured data implementation.
10. Identify image handling and optimization patterns.
11. Identify existing tests and build commands.
12. Identify the correct locations for implementing each change.

It must not assume the website uses a particular framework or file structure.

It must follow the existing project's conventions unless a justified improvement is necessary.

## 13.3 Report-to-Code Implementation Mapping

For every recommendation in `SEO_Consolidated_Final_Report.md` and its relevant supporting files, generate an implementation task.

Each task must contain:

- Task ID.
- Priority.
- SEO issue or opportunity.
- Affected page URL.
- Relevant keyword.
- Required change.
- Expected implementation location.
- Recommended implementation approach.
- Dependencies.
- Acceptance criteria.
- Validation method.

The developer AI must maintain traceability between each implementation task and its source recommendation.

Do not implement unsupported or ambiguous recommendations without investigating them first.

## 13.4 Page-Level SEO Implementation

Implement validated page-specific requirements, including:

- Unique title tags.
- Unique meta descriptions.
- Correct H1 hierarchy.
- Appropriate H2 and H3 structure.
- Canonical URLs.
- Robots directives.
- Open Graph metadata.
- Social sharing metadata where relevant.
- Search-intent-aligned content updates.
- Keyword placement where natural and appropriate.
- Contextual internal links.
- Breadcrumbs where appropriate.
- Structured data where supported by actual page content.

Use the recommended values from the final SEO report.

Do not blindly apply identical metadata to every page.

Do not create keyword-stuffed content.

Preserve the website's brand voice and conversion-focused messaging.

## 13.5 New Page Implementation

For each approved new page:

1. Verify that the page does not already exist.
2. Check for duplicate URL or keyword targeting.
3. Create the page using the existing architecture.
4. Follow the existing design system and reusable components.
5. Implement the recommended page structure.
6. Add relevant metadata.
7. Add contextual internal links.
8. Add appropriate images and alt text.
9. Implement applicable structured data.
10. Verify routing and rendering.

Do not create pages that duplicate existing content or have no meaningful business purpose.

## 13.6 Technical SEO Implementation

Implement only applicable and validated requirements, including:

- XML sitemap generation and inclusion of canonical, indexable URLs.
- robots.txt configuration.
- Canonical URL handling.
- Indexing and noindex directives.
- Correct redirect behavior.
- Broken-link fixes.
- Structured data.
- Breadcrumb implementation.
- Correct HTTP status behavior.
- Mobile-friendly rendering.
- Image optimization.
- Appropriate lazy loading.
- Core Web Vitals improvements.
- Performance optimization.
- SEO-safe rendering and routing.

Do not block important resources or pages through incorrect robots.txt rules.

Do not introduce redirect chains, redirect loops, duplicate canonical declarations, or accidental noindex directives.

Do not add structured data for information that is not visibly supported by the page.

## 13.7 Image SEO Implementation

For each validated image recommendation:

- Locate the actual asset.
- Verify its usage.
- Apply appropriate descriptive filenames when practical.
- Implement accurate alt text.
- Use suitable image formats.
- Optimize image dimensions and compression.
- Use the project's existing image optimization strategy.
- Apply lazy loading to appropriate below-the-fold images.
- Avoid lazy loading critical above-the-fold or LCP images.

Do not remove or replace images without verifying their purpose.

## 13.8 Internal Linking Implementation

Implement approved internal links.

Requirements:

- Link relevant pages contextually.
- Use natural and descriptive anchor text.
- Avoid excessive exact-match anchor text.
- Fix validated broken internal links.
- Improve navigation to important service and landing pages.
- Avoid irrelevant links.
- Avoid creating circular or unnecessary linking patterns.

## 13.9 Content Implementation

Use the final report's approved content recommendations.

For each content update:

- Identify the exact target page.
- Preserve accurate business information.
- Follow the recommended heading hierarchy.
- Improve clarity and usefulness.
- Address the target search intent.
- Use primary and secondary keywords naturally.
- Add relevant contextual links.
- Preserve brand voice.
- Avoid fabricated claims, statistics, testimonials, and certifications.

Do not publish or externally distribute content automatically.

## 13.10 Implementation Execution Strategy

Execute changes in controlled phases:

**Phase 1 — Repository Discovery**

- Inspect project.
- Identify implementation locations.
- Create a baseline report.
- Identify risks and dependencies.

**Phase 2 — Critical Technical SEO**

- Fix verified critical technical issues.
- Verify crawlability and indexability.

**Phase 3 — On-Page SEO**

- Implement page metadata.
- Improve heading structures.
- Implement canonical and indexing requirements.

**Phase 4 — Content and Page Improvements**

- Update existing content.
- Create approved new pages.
- Verify page uniqueness and search intent.

**Phase 5 — Images and Internal Links**

- Implement image optimization.
- Implement approved internal linking changes.

**Phase 6 — Structured Data and Sitemap**

- Implement applicable structured data.
- Update sitemap and robots.txt as required.

**Phase 7 — Validation**

- Run build.
- Run lint.
- Run available automated tests.
- Validate affected routes.
- Check metadata and canonical tags.
- Validate sitemap and robots.txt.
- Check internal links.
- Validate structured data.
- Review performance and rendering regressions.

Execute sequentially. Do not skip a phase's required validation before proceeding.

## 13.11 Safety and Change Management

The developer AI must:

- Preserve existing application functionality.
- Avoid unrelated refactoring.
- Follow existing coding conventions.
- Avoid exposing secrets or environment variables.
- Avoid deleting existing pages or assets without justification.
- Avoid changing authentication, payment, business, or operational logic unnecessarily.
- Avoid destructive database or infrastructure changes.
- Avoid deploying to production without explicit authorization.
- Avoid publishing content without explicit authorization.
- Keep a clear record of all changed files.

If a change could introduce a significant regression, explain the risk and request approval before proceeding.

## 13.12 Developer Implementation Report

After implementation, create a report containing:

- Implementation summary.
- Completed tasks.
- Partially completed tasks.
- Pending tasks.
- Failed tasks.
- Files created.
- Files modified.
- Pages created or modified.
- Technical SEO changes.
- Metadata changes.
- Content changes.
- Image changes.
- Internal link changes.
- Build results.
- Lint results.
- Test results.
- SEO validation results.
- Remaining risks.
- Manual actions required.

Every task must be marked as one of:

- Completed.
- Partially Completed.
- Blocked.
- Not Implemented.
- Requires Approval.

Never claim a change was completed without verifying the actual code or test result.

## 13.13 Developer Prompt Must Be Self-Contained

The generated developer prompt must:

1. Include the website URL and business context.
2. Explain the objective.
3. Explain repository discovery requirements.
4. Include the validated SEO implementation requirements.
5. Include page-specific recommendations.
6. Include technical SEO requirements.
7. Include content and image requirements.
8. Include internal linking requirements.
9. Include implementation phases.
10. Include safety constraints.
11. Include testing and validation requirements.
12. Include implementation reporting requirements.

The developer AI must be able to understand the task without needing to reconstruct the SEO analysis from the conversation.

Where detailed page-level recommendations are available in supporting CSV files, the prompt must instruct the developer AI to inspect and use those files as implementation inputs.

Where information is unavailable, instruct the developer AI to investigate rather than invent values.

---

# 14. Dedicated Implementation Plans & Supporting Datasets

In addition to the primary markdown reports, this skill MUST compile dedicated, machine-readable implementation plans:

### 14.1 Phased Implementation Roadmap & Priority Matrix
- `seo-implementation-roadmap.md`: Step-by-step phased execution sprints:
  - Sprint 1 (Days 1–15, P0 Critical): Crawl blockers, indexing errors, robots.txt, 404s, mobile CWV bottlenecks.
  - Sprint 2 (Days 16–30, P1 High): Core service page metadata, H1/H2 hierarchy, primary keywords, essential JSON-LD schemas.
  - Sprint 3 (Days 31–60, P1–P2 Medium): Content expansions, internal linking mesh, priority topic cluster pages.
  - Sprint 4 (Days 61–90, P2–P3 Ongoing): Long-tail blogs, digital PR linkable assets, secondary schema enhancements.
- `seo-priority-matrix.csv`: Consolidated prioritization dataset scoring every single recommendation by Impact (1–5), Effort (1–5), Technical Risk, and Priority Tier (P0–P3).

### 14.2 Dedicated Granular Implementation Plans (CSVs)
1. `keyword-implementation-plan.csv`:
   - Columns: `page_url`, `page_title`, `target_primary_keyword`, `search_volume`, `keyword_difficulty`, `search_intent`, `target_secondary_keywords`, `keyword_cluster`, `action_required`, `priority`
2. `metadata-implementation-plan.csv`:
   - Columns: `page_url`, `current_title`, `suggested_title`, `current_meta_description`, `suggested_meta_description`, `primary_keyword`, `title_character_count`, `meta_character_count`, `priority`, `action`
3. `heading-implementation-plan.csv`:
   - Columns: `page_url`, `section_component`, `existing_heading_tag`, `existing_heading_text`, `suggested_heading_tag`, `suggested_heading_text`, `target_keyword`, `heading_level`, `priority`, `action`
4. `content-implementation-plan.csv`:
   - Columns: `page_url`, `content_section`, `existing_content_summary`, `suggested_optimized_copy`, `target_keywords`, `current_word_count`, `target_word_count`, `change_type`, `priority`
5. `technical-implementation-plan.csv`:
   - Columns: `issue_id`, `affected_url_or_file`, `category`, `current_issue_evidence`, `suggested_code_or_config_fix`, `technical_justification`, `risk_level`, `verification_method`, `priority`
6. `internal-linking-implementation-plan.csv`:
   - Columns: `source_url`, `target_url`, `existing_anchor_text`, `suggested_anchor_text`, `link_context_sentence`, `placement_section`, `priority`, `action`
7. `new-page-implementation-plan.csv`:
   - Columns: `target_url_slug`, `page_type`, `topic_cluster`, `primary_keyword`, `secondary_keywords`, `target_word_count`, `outline_summary`, `target_cta`, `priority`

### 14.3 Supporting Governance and Audit Logs
- `Project_Discovery_Report.md`
- `Consolidated_SEO_Findings.md`
- `Final_Report_Validation.md`
- `Execution_Summary.md`
- `Execution_Log.md`
- `prompt.txt` (Plain text copy of `Master_Developer_Implementation_Prompt.md`)

---

# 15. Mandatory Output Location

Resolve variables according to `../shared/INPUT_VARIABLES.md` and `../shared/OUTPUT_STANDARDS.md`:

- `OUT_PUT_ROOT_FOLDER`: Root directory for all generated outputs. **Default:** `C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs`.
- `CURRENT_DATE`: Current execution date formatted as `YYYY-MM-DD`.
- `DOMAIN_NAME`: Normalized website hostname.

Canonical Output Directory:
`{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/09-final-seo-report/`

Save primary deliverables at:
- Master Report: `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/09-final-seo-report/final-seo-overall-report.md` (and mirror `SEO_Consolidated_Final_Report.md`)
- Master Changes: `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/09-final-seo-report/final-seo-website-changes.md`
- Developer Prompt: `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/09-final-seo-report/Master_Developer_Implementation_Prompt.md`

All implementation CSVs and supporting files must reside directly in the same directory.
If files already exist for the current date, preserve them by creating a versioned execution directory (`executions/{execution-id}/`).

All supporting deliverables must be saved in the same final report directory unless a clearly justified subdirectory structure is necessary.

Do not save either primary deliverable only in the repository root, a temporary directory, or an upstream SEO stage directory.

---

# 16. File Creation and Verification

You must physically create both primary Markdown files.

Do not merely display their contents in chat.

After creation:

1. Verify both files exist at the exact required paths.
2. Verify both files have non-zero file sizes.
3. Read both files back.
4. Verify that the SEO report contains all required report sections.
5. Verify that the developer prompt contains all required implementation instructions.
6. Verify that the developer prompt includes concrete findings from the consolidated SEO analysis.
7. Verify that all references to supporting files use their actual generated paths.
8. Verify that no unsupported recommendation has been presented as a confirmed issue.

If file creation or validation fails, report the failure accurately.

Never claim successful file creation without verification.

---

# 17. Final Execution Summary

At completion, provide:

- Website analyzed.
- SEO workflow stages discovered.
- Stages unavailable or incomplete.
- Key consolidated findings.
- Critical implementation priorities.
- Exact path of the final SEO report.
- Exact path of the Master Developer Implementation Prompt.
- Supporting files created.
- Validation status.
- Any limitations.

Clearly explain that the Master Developer Implementation Prompt is intended to be supplied to an AI coding tool or developer together with access to the website repository and the generated supporting files.

Do not claim that website code changes have already been implemented. This skill produces the SEO analysis and the developer execution prompt; implementation is a separate authorized step.

---

# 18. Final Execution Instructions

Execute the workflow strictly sequentially.

First discover and analyze the completed upstream SEO outputs.

Then consolidate and validate all findings.

Next generate the SEO Consolidated Final Report.

After that, generate the Master Developer Implementation Prompt using the actual consolidated findings.

Finally, generate relevant supporting files, validate all deliverables, and provide their exact output paths.

**The workflow is not complete until both mandatory primary files have been physically created and verified.**
