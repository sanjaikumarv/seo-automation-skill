---
name: seo-orchestrator
description: Run the full nine-stage SEO workflow for a website, from intake and audit through a consolidated report, granular website changes, and master developer implementation prompt.
---

# SEO Master Workflow Orchestrator

## Skill Description

A comprehensive master workflow orchestrator that coordinates the full multi-stage SEO automation workflow across specialized skills:
- **What this skill does:** Collects initial intake parameters, sets up the output directory root (`OUT_PUT_ROOT_FOLDER`), dynamically discovers and verifies all SEO skills, enforces strict sequential execution, manages inter-skill context passing, validates stage deliverables (mandating both `<skill>-overall-report.md` and `<skill>-website-changes.md` per stage), logs execution progress, and verifies final reports.
- **Its primary objective:** Coordinate the end-to-end SEO automation process autonomously without mid-run interruptions, ensuring zero data fabrication, strict Google Search Essentials compliance, and canonical artifact persistence.
- **When it should be used:** When initiating an SEO campaign for any website, domain, or business entity from scratch or when re-running the full SEO pipeline.
- **What output or result it produces:** Manages execution state, outputs `orchestration-summary.md`, `execution-tracker.md`, and `execution-log.md` in `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/00-orchestration/`, and ensures the compilation of all downstream reports.

## Shared Resources

This skill utilizes the following shared documentation:
- Universal Input Variables: `../shared/INPUT_VARIABLES.md`
- Canonical Output Standards: `../shared/OUTPUT_STANDARDS.md`
- Shared SEO Tools: `../shared/TOOLS.md`
- SEO Quality Standards: `../shared/SEO_STANDARDS.md`
- Research Guidelines: `../shared/RESEARCH_GUIDELINES.md`

---

## Step 0 · Intake & Environment Setup

1. **Intake Collection:** Resolve the required project inputs before beginning execution:
   - Target Website URL (`{{WEBSITE_URL}}`)
   - Business / Website Name (`{{WEBSITE_NAME}}`)
   - Services or Products Offered (`{{SERVICES}}`)
   - Initial Seed Keywords (`{{SEED_KEYWORDS}}`)
   - Target Country / Geography (`{{TARGET_COUNTRY}}` / `{{TARGET_GEOGRAPHY}}`)
   - Target Audience & Business Type (`{{TARGET_AUDIENCE}}` / `{{BUSINESS_TYPE}}`)
   - Frontend Tech Stack (e.g. Next.js App Router / React / Tailwind CSS; verify against repository)
   - **Output Root Directory (`OUT_PUT_ROOT_FOLDER`):** Default to `C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs`. If the user specifies an alternative directory, use that path.

2. **Output Hierarchy Initialization:**
   Set the run root:
   ```text
   {OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/
   ```
   (Default: `C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs\{{CURRENT_DATE}}/{{DOMAIN_NAME}}/`)

   Initialize the standardized stage directories:
   - `00-orchestration/`
   - `01-website-audit/`
   - `02-keyword-research/`
   - `03-competitor-analysis/`
   - `04-on-page-seo/`
   - `05-content-strategy/`
   - `06-technical-seo/`
   - `07-off-page-seo/`
   - `08-seo-monitoring/`
   - `09-final-seo-report/`

3. **Tracking Initialization:**
   Create `execution-tracker.md` and `execution-log.md` in `00-orchestration/`. Initialize all stages as `PENDING`.

---

## Steps 1–9 · Strict Sequential Execution Matrix

| Step | Skill Name | Stage Directory | Primary Strategic Report | Mandatory Website Changes Report | Upstream Dependencies |
| :---: | :--- | :--- | :--- | :--- | :--- |
| **01** | `seo-audit` | `01-website-audit/` | `website-audit-overall-report.md` | `website-audit-website-changes.md` | Step 0 Intake |
| **02** | `seo-keyword-research` | `02-keyword-research/` | `keyword-research-overall-report.md` | `keyword-research-website-changes.md` | Stage 01 |
| **03** | `seo-competitor-analysis` | `03-competitor-analysis/` | `competitor-analysis-overall-report.md` | `competitor-analysis-website-changes.md` | Stages 01, 02 |
| **04** | `seo-on-page` | `04-on-page-seo/` | `on-page-seo-overall-report.md` | `on-page-seo-website-changes.md` | Stages 01, 02, 03 |
| **05** | `seo-content-strategy` | `05-content-strategy/` | `content-strategy-overall-report.md` | `content-strategy-website-changes.md` | Stages 01, 02, 03, 04 |
| **06** | `technical-seo` | `06-technical-seo/` | `technical-seo-overall-report.md` | `technical-seo-website-changes.md` | Stages 01, 02, 03, 04, 05 |
| **07** | `off-page-seo` | `07-off-page-seo/` | `off-page-seo-overall-report.md` | `off-page-seo-website-changes.md` | Stages 01 through 06 |
| **08** | `seo-monitoring` | `08-seo-monitoring/` | `seo-monitoring-overall-report.md` | `seo-monitoring-website-changes.md` | Stages 01 through 07 |
| **09** | `seo-final-report` | `09-final-seo-report/` | `final-seo-overall-report.md` | `final-seo-website-changes.md` | Stages 01 through 08 |

---

## Stage Execution & Validation Protocol

For each stage in numerical order:

1. **Lock & Initialize:** Verify that the previous stage has fully completed and validated. Mark the current stage `INITIALIZING`.
2. **Context Passing:** Pass the project intake, `OUT_PUT_ROOT_FOLDER`, run root, and exact upstream artifact file paths to the current skill.
3. **Run Stage:** Mark stage `RUNNING`. Execute the skill's complete methodology using free tools first (see `../shared/TOOLS.md`).
4. **Mandatory Deliverables Check:** Mark stage `VALIDATING`.
   - Verify that `<skill-name>-overall-report.md` exists and is non-empty.
   - Verify that `<skill-name>-website-changes.md` exists and is non-empty.
   - Verify that required supporting datasets (CSVs, briefs, schemas) exist in the stage directory.
   - Verify that all findings cite evidence and unknown analytics are labeled `[Public observational search data; requires Google Search Console verification]`.
5. **Stage Completion:** Update `execution-tracker.md` to `COMPLETED` and proceed to the next stage. Never run multiple stages in parallel.

---

## Final Verification & Deliverable Publishing

Upon completion of Stage 09:

1. **Verify Master Deliverables:**
   - `09-final-seo-report/final-seo-overall-report.md`
   - `09-final-seo-report/final-seo-website-changes.md` (consolidating all website updates)
   - `09-final-seo-report/seo-implementation-roadmap.md`
   - `09-final-seo-report/seo-priority-matrix.csv`
   - Granular implementation plans:
     - `keyword-implementation-plan.csv`
     - `metadata-implementation-plan.csv`
     - `heading-implementation-plan.csv`
     - `content-implementation-plan.csv`
     - `technical-implementation-plan.csv`
     - `internal-linking-implementation-plan.csv`
     - `new-page-implementation-plan.csv`
   - `09-final-seo-report/Master_Developer_Implementation_Prompt.md`
2. **Publish Orchestration Summary:**
   Compile `00-orchestration/orchestration-summary.md` detailing all execution times, deliverable paths, executive takeaways, and direct links to artifacts.
