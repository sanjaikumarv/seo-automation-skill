---
name: seo-orchestrator
description: Run the full nine-stage SEO workflow for a website, from intake and audit through a consolidated report and master developer implementation prompt. Use for a complete SEO campaign or rerun.
---

# SEO Orchestrator

## Step 0 · Intake

1. Resolve the website URL, business or brand name, services or products, seed queries, and target geography from the current request. Ask once for any missing required inputs before starting. Validate the HTTP(S) URL and derive the domain for file paths.
2. Use the frontend stack supplied by the user. If absent, check the available project source or public site evidence. If the stack remains unconfirmed, use Next.js (App Router), React, and Tailwind CSS as a developer handoff assumption and require verification against the repository before implementation.
3. Carry forward any available audience, SEO objectives, brand voice, known competitors, and authorized data sources such as Google Search Console, GA4, and crawl exports. Record missing optional data and continue without mid-run questions.
4. Identify the active project workspace or the writable ChatGPT working directory used for downloadable artifacts. Read the shared input, output, tool, SEO, and research standards from the repository's sibling `shared/` directory or the package's `references/shared/` directory. Set the run date and a run ID. Use `outputs/<date>/<domain>/` as the run root. If it already has results from another run, use `outputs/<date>/<domain>/runs/<run-id>/`. Keep the same run root across all stages.
5. Initialize all nine stages as PENDING. Create `seo-orchestration/Execution_Tracker.md` and `seo-orchestration/Execution_Log.md` in the run root. Record state transitions under the run ID in `logs/pipeline-state.json` relative to the active workspace, preserving earlier entries.

## Steps 1–9 · Execute in order

| Step | Skill name | Stage | Minimum upstream stages to read |
| --- | --- | --- | --- |
| 1 | `seo-audit` | SEO audit | Intake |
| 2 | `seo-keyword-research` | Keyword research and URL mapping | 1 |
| 3 | `seo-competitor-analysis` | Competitor analysis | 1–2 |
| 4 | `seo-on-page` | On-page SEO | 1–3 |
| 5 | `seo-content-strategy` | Content strategy and creation | 1–4 |
| 6 | `technical-seo` | Technical SEO | 1–5 |
| 7 | `off-page-seo` | Off-page SEO and link building | 1–6 |
| 8 | `seo-monitoring` | Monitoring and performance tracking | 1–7 |
| 9 | `seo-final-report` | Consolidated analysis and master developer prompt | 1–8 |

Use these exact skill names. The source Markdown's `seo-technical` and `seo-off-page` refer to `technical-seo` and `off-page-seo`.

For each stage, complete this loop before advancing:

1. Confirm intake or the preceding stage is complete. Mark the stage INITIALIZING and acquire the logical execution lock. Only one stage may initialize, run, validate, or update completion records at a time.
2. Load the matching skill from the registered skill list or the repository's sibling `<skill>/SKILL.md`. If the host cannot load sibling skills, read the full bundled workflow at `references/stages/<skill>.md`. Follow those instructions in the current session when the host has no separate skill invocation action. A `$skill-name` mention is a way to select a skill in Codex, not a shell command. Record the actual skill source and invocation method.
3. Pass the intake, run root, and required upstream files to the current stage. Read the relevant artifacts from the recorded paths for this run, including their evidence, timestamps, and limitations. The active run's recorded paths take precedence over examples and latest-run discovery in a stage skill.
4. Mark the stage RUNNING. Execute its full methodology and write its deliverables using its canonical filenames. Follow Google Search Essentials. Cite verifiable evidence and use “Public observational search data; requires Google Search Console verification.” where authenticated search or analytics data is unavailable. Record optional data or tool limitations explicitly.
5. Mark the stage VALIDATING. Check required files are present, non-empty, readable, under the run root, and contain the required sections and resolved project values. Check any format-specific artifacts using the stage instructions. Record the actual files, timestamps, evidence limitations, and validation result. Mark COMPLETED and release the lock only after validation and record updates.

Maintain the tracker with stage, skill, instruction source, invocation method, status, start and finish times, output paths, and validation result. Keep a chronological execution log with the intake, stage transitions, limitations, failures, and retries. For a known, recoverable failure, make a safe bounded retry in the same run. If it persists, mark the stage FAILED or BLOCKED, record the cause and artifacts, and stop dependent stages. A missing required skill, input, or upstream artifact blocks the stage.

## Final validation

1. Read back `SEO_Consolidated_Final_Report.md` and `Master_Developer_Implementation_Prompt.md` from the recorded final-stage directory. Verify the report synthesizes all completed upstream findings and the prompt includes repository verification, prioritized changes, and acceptance checks for the frontend stack. The prompt is a handoff for future implementation.
2. Write `seo-orchestration/Orchestration_Summary.md` with the project and run details, stages and validation outcomes, evidence-backed findings and opportunities, limitations, and links to the deliverables. If the run stopped early, record the failure and the remaining stages in the summary.
3. Verify the tracker, log, summary, and completed deliverables. Report the site, date, run status, stage results, key findings, limitations, and verified artifact links. In a file sandbox, expose the report and implementation prompt as downloads.
