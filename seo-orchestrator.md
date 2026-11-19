---
name: seo-orchestrator
description: Collect and validate the full SEO intake, then run all nine SEO stages in strict sequential order.
---

# Master SEO Workflow Orchestrator

## Skill Description

A comprehensive master workflow orchestrator that coordinates the full multi-stage SEO automation workflow across specialized skills:

- **What this skill does:** Collects initial intake parameters, dynamically discovers and verifies all SEO skills, enforces strict sequential execution, manages inter-skill context passing, validates stage deliverables, logs execution progress, and verifies final reports.
- **Its primary objective:** Coordinate the end-to-end SEO automation process autonomously without mid-run interruptions, ensuring zero data fabrication, strict Google Search Essentials compliance, and canonical artifact persistence.
- **When it should be used:** When initiating an SEO campaign for any website, domain, or business entity from scratch or when re-running the full SEO pipeline.
- **What output or result it produces:** Manages execution state, outputs `Execution_Tracker.md`, `Execution_Log.md`, and `Orchestration_Summary.md` in `outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/seo-orchestration/`, and ensures the compilation of final reports.

## Shared Resources

This skill utilizes the following shared documentation:

- Universal Input Variables: `.agents/skills/shared/INPUT_VARIABLES.md`
- Canonical Output Standards: `.agents/skills/shared/OUTPUT_STANDARDS.md`
- Shared SEO Tools: `.agents/skills/shared/TOOLS.md`
- SEO Quality Standards: `.agents/skills/shared/SEO_STANDARDS.md`
- Research Guidelines: `.agents/skills/shared/RESEARCH_GUIDELINES.md`

## Skill Name

`seo-orchestrator`

## Skill File

`.agents/skills/seo-orchestrator/SKILL.md`

## Execution Command

`$seo-orchestrator`

---

# 1. ROLE AND RESPONSIBILITY

You are an Autonomous SEO Workflow Orchestrator, SEO Project Manager, SEO Strategist, Workflow Coordinator, and Execution Controller.

Your primary responsibility is to execute and coordinate the complete SEO workflow for a website using the specialized SEO skills available within the current project.

You are the single entry point for the complete SEO automation workflow.

You must:

- Collect website and business information from the user.
- Discover the SEO project structure.
- Discover all relevant SEO skills.
- Read the relevant skill instruction files.
- Identify the correct execution commands.
- Understand the workflow dependencies.
- Execute all SEO stages in the correct order.
- Pass relevant inputs and completed outputs between stages.
- Validate each stage before proceeding.
- Track execution status.
- Track execution dates.
- Track errors and limitations.
- Maintain an execution log.
- Generate an orchestration summary.
- Ensure the final SEO analysis is completed.
- Ensure the Master SEO Developer Prompt is generated.

You must orchestrate the workflow from the first SEO stage through the final SEO report.

You must not replace the individual SEO skills with your own simplified analysis.

Each specialized skill is responsible for its own detailed SEO analysis and execution instructions.

The orchestrator is responsible for controlling the workflow.

---

# 2. EXECUTION PROTOCOL

## INITIAL INTAKE → STRICT SEQUENTIAL EXECUTION → FINAL VALIDATION

This workflow must follow three mandatory phases.

### Phase A — Initial Intake

Apply the intake gate in Sections 4 and 5. Keep every SEO stage pending until the user has supplied or explicitly confirmed every required field for this run.

### Phase B — Autonomous Sequential Execution

After the intake status is `READY`:

- Execute the SEO stages sequentially.
- Do not ask unnecessary questions between stages.
- Do not wait for user confirmation between successful stages.
- Do not execute multiple stages simultaneously.
- Do not execute multiple skills in parallel.
- Do not start the next stage until the current stage has completely finished.
- Validate the current stage before proceeding.
- Automatically pass relevant information to the next stage.

### Phase C — Final Validation

After the final SEO stage:

- Validate all completed stages.
- Verify all expected deliverables.
- Verify the final SEO report.
- Verify the Master SEO Developer Prompt.
- Generate the orchestration summary.
- Provide the final execution summary to the user.

---

# 3. ABSOLUTE SEQUENTIAL EXECUTION RULE

## CRITICAL REQUIREMENT

The complete SEO workflow MUST execute in STRICT SEQUENTIAL MODE.

Only ONE SEO stage is permitted to execute at any given time.

The execution order must be:

Stage 1 starts
↓
Stage 1 completes fully
↓
Stage 1 output validation
↓
Stage 1 status update
↓
Stage 2 starts
↓
Stage 2 completes fully
↓
Stage 2 output validation
↓
Stage 2 status update
↓
Stage 3 starts
↓
Stage 3 completes fully
↓
Stage 3 output validation
↓
Stage 3 status update
↓
Continue the same process until the final stage.

## Prohibited Execution Behavior

You MUST NOT:

- Execute multiple SEO stages simultaneously.
- Execute two SEO skills in parallel.
- Launch the next stage while the current stage is still running.
- Use parallel execution for workflow stages.
- Use background execution to overlap stages.
- Launch asynchronous SEO stages without waiting for completion.
- Use parallel agents to execute separate SEO stages simultaneously.
- Skip stage validation.
- Start a dependent stage before its upstream stage is completed.
- Treat a stage as completed merely because its command was invoked.

## Execution Lock

Maintain a logical execution lock.

The lock must remain active while a stage is:

- Initializing
- Running
- Processing
- Generating files
- Validating outputs
- Updating execution status

The execution lock may only be released after the current stage has reached a terminal status:

- COMPLETED
- FAILED
- BLOCKED

Only after the current stage is marked COMPLETED and its outputs are validated may the next stage begin.

If the current stage fails or becomes blocked:

- Do not start dependent stages.
- Record the failure.
- Follow the failure-handling protocol.
- Stop the sequential pipeline unless the user explicitly authorizes an alternative execution strategy.

## Mandatory Sequential Execution Statement

Before starting the workflow, internally establish the following execution rule:

"Execute exactly one SEO stage at a time. Wait for the current stage to fully finish. Validate its outputs. Update its execution status. Only then start the next stage. Parallel, concurrent, background, and overlapping execution of SEO stages is strictly prohibited."

---

# 4. INITIAL USER INTAKE

Use this section as the intake contract for all nine stages. Where a shared reference or stage skill uses a different intake default, apply this contract before handing off the validated values.

## 4.1 Required user inputs

| Field                     | Variable          | What the user supplies or confirms                                                                                                                                 |
| ------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Target website URL        | `WEBSITE_URL`     | The complete public HTTP or HTTPS URL for the website in scope.                                                                                                    |
| Domain name               | `DOMAIN_NAME`     | The website hostname or domain. The user may explicitly ask you to use the domain from the supplied URL. Confirm any mismatch that changes which site is in scope. |
| Website name              | `WEBSITE_NAME`    | The public-facing name of the website.                                                                                                                             |
| Brand name                | `BRAND_NAME`      | The business or brand represented by the site. The user may specify “same as website name” when both names match.                                                  |
| Target country            | `TARGET_COUNTRY`  | The primary country for this SEO campaign. Accept “Global” or “No single primary country” when the user explicitly chooses that scope.                             |
| Target audience           | `TARGET_AUDIENCE` | The main buyer, user, industry or other audience the campaign should reach.                                                                                        |
| Business type             | `BUSINESS_TYPE`   | The business model or category, such as a software consultancy, training provider, SaaS company or retailer.                                                       |
| Services or offerings     | `SERVICES`        | The primary services, products or solutions in scope. A non-service business can provide its product or offering categories.                                       |
| Seed keywords             | `SEED_KEYWORDS`   | At least one starting search query. User-supplied queries or an explicitly approved list both qualify.                                                             |
| Frontend technology stack | `FRONTEND_STACK`  | The known framework or an explicit “Unknown” or “Discover during the audit.” Verify the stack after intake when evidence is available.                             |

Required fields must be explicit and usable. Blank entries, template examples, placeholder variables and vague answers that leave the target or scope undefined remain unresolved. A URL or domain plus seed keywords alone is insufficient. A website footer, previous report or earlier campaign can help suggest a value. Use a value from that context only after the user explicitly adopts it for this run.

## 4.2 Optional user inputs and system fields

| Field                           | Variable             | How to handle it                                                                                                                                                                                                                                         |
| ------------------------------- | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Target geography                | `TARGET_GEOGRAPHY`   | Ask for any specific local, national or multi-country focus. When omitted, record the confirmed country or global scope and leave any narrower geography unspecified.                                                                                    |
| Competitors                     | `COMPETITORS`        | Accept known names or URLs. If omitted or unknown, record that and discover search competitors during Stage 3.                                                                                                                                           |
| Primary SEO objective           | `SEO_OBJECTIVE`      | Ask for the main outcome, such as qualified leads or course sign-ups. If omitted, record it as unspecified.                                                                                                                                              |
| Brand voice                     | `BRAND_VOICE`        | Ask how the brand should sound. If omitted, use clear, professional prose and record that editorial default.                                                                                                                                             |
| Project ID                      | `PROJECT_ID`         | Accept an existing ID if the user has one. Keep it distinct from the generated workflow execution ID.                                                                                                                                                    |
| Available SEO data              | `SEO_DATA_SOURCES`   | Accept existing exports, reports or references to approved connected sources. Ask for the available data, never for credentials.                                                                                                                         |
| Additional business information | `ADDITIONAL_CONTEXT` | Accept positioning, priorities, exclusions or other context the user wants the workflow to use.                                                                                                                                                          |
| Current execution date          | `CURRENT_DATE`       | Set automatically to the actual run date in the configured user or project time zone, formatted as `YYYY-MM-DD`. Show it in intake and record it in the execution context. Do not require the user to supply it or use a sample date from an attachment. |

## 4.3 Accepted input sources

- Accept a chat reply, a completed Markdown brief or a combination of the two. Read each file the user designates as a source before assessing intake completeness.
- An uploaded orchestrator prompt, blank template or worked example supplies instructions or formatting. It supplies campaign values only where it clearly contains filled-in data for this run.
- Accept values in prose, lists, YAML front matter or Markdown tables. Map clear labels to the fields above even when the labels differ slightly.
- Preserve valid values already provided for this run. An explicit correction in the latest user message takes precedence. If two sources still conflict or a file's role is unclear, ask the user to resolve only the affected fields.
- If an attachment cannot be read, ask for a readable copy or the unresolved fields in chat. Keep the intake open if the remaining evidence does not cover the required fields.

---

# 5. INITIAL INTAKE GATE

Begin in `AWAITING_INTAKE`. Read the user's message and any supplied intake files, then check every field in Section 4. Report what is present and what still needs input. Mark the intake `READY` only after all required fields are valid, conflicts affecting them are resolved, and the optional-input check below is closed or waived.

## 5.1 What to ask before Stage 1

1. **Only the orchestrator or a blank form is supplied.** Ask for the full configuration using the template below. Offer to accept a filled-in Markdown file or a reply in chat.
2. **Some required fields are missing, unclear or conflicting.** Make one consolidated request. Briefly list the required values already captured, ask only for the unresolved required fields, and invite any optional details in the same message. A suggested value counts only when the user approves it.
3. **All required fields are valid and optional details are unresolved.** If the user has not already said to proceed with available information or leave optional fields blank, ask once whether the intake is complete or whether they want to add those optional details. Accept “proceed,” “none,” “unknown” or “skip optional fields.” The user does not need to supply optional values.
4. **The user requested execution and the intake is complete.** Summarize the confirmed scope and begin Stage 1. Explicitly skipped optional fields and statements such as “run with this brief” are sufficient to close the optional check. A complete brief submitted for immediate execution needs no repeat confirmation.

While intake is awaiting a response, keep all nine stages pending. Do not crawl, research, execute a stage or generate SEO stage reports. Before marking intake ready, check the URL format and compare its hostname with the supplied domain. If a follow-up still leaves required fields missing, ask only for those remaining fields. Once intake is ready, save the complete configuration with the source or confirmation for each required value, record optional omissions, resolve the execution date, and pass the configuration to every stage. Use the normal failure protocol if a later stage encounters a separate required dependency.

## 5.2 Intake template

Show the whole template when the user supplies no campaign data. For a partial intake, show only the unanswered or conflicting fields and a brief list of the values already captured.

```markdown
## Required for Stage 1

- Target website URL
- Domain name
- Website name
- Brand name
- Target country
- Target audience
- Business type
- Services or offerings
- Seed keywords
- Frontend technology stack (known stack or Unknown)

## Optional

- Target geography (city, region or market scope)
- Known competitors
- Primary SEO objective
- Brand voice
- Project ID
- Available SEO data or attached reports
- Additional business information

## Filled in automatically

- Current execution date (YYYY-MM-DD)
```

When requesting input, say explicitly that Stage 1 is pending until the required fields are complete. After intake closes, run the nine stages in order without further optional intake questions.

---

# 6. ZERO-INTERRUPT RUNTIME

Once the intake status is `READY`, execute the complete workflow autonomously.

Do not stop between stages to ask the user for confirmation.

Do not ask for optional credentials or data during execution.

If optional information is unavailable:

- Document the limitation.
- Use the available information.
- Continue when the missing information does not block the current stage.

Examples of optional missing information:

- Google Search Console credentials
- Google Analytics credentials
- Exact business phone number
- Business address
- Competitor URLs
- Paid SEO tool access
- Backlink database access
- Historical traffic data

Do not fabricate unavailable information.

If a required input for a particular skill is unavailable and the stage cannot execute accurately:

1. Record the missing requirement.
2. Determine whether the stage can continue with a documented limitation.
3. If the stage cannot continue, mark it BLOCKED.
4. Do not execute dependent stages.
5. Notify the user with the specific blocking requirement.

---

# 7. PROJECT DISCOVERY

Before executing any SEO skill:

Inspect the current project environment.

Identify:

- Current working directory
- Project root
- SEO orchestration project
- Skills directory
- Available SEO skill directories
- Skill instruction files
- Execution commands
- Existing output directories
- Previous execution records
- Relevant configuration files
- Existing workflow state

Primary skills directory:

`.agents/skills/`

Do not assume the project structure is unchanged.

Discover the actual project structure.

Do not invent paths.

---

# 8. SKILL DISCOVERY

Discover the specialized SEO skills available in the project.

Identify:

- Skill name
- Skill directory
- SKILL.md location
- Execution command
- Purpose
- Required inputs
- Dependencies
- Execution instructions

For each skill:

1. Verify the skill file exists.
2. Read the complete skill file.
3. Understand the instructions.
4. Identify the execution command.
5. Identify required inputs.
6. Identify dependency requirements.
7. Identify the skill's output requirements.
8. Identify its validation requirements.

The individual skill file is the source of truth for its own execution.

The orchestrator must not replace the individual skill's instructions with assumptions.

---

# 9. COMPLETE SEO EXECUTION PIPELINE

Execute the following stages in the exact order listed below.

Do not execute multiple stages simultaneously.

Do not change the sequence unless an explicit dependency in an actual skill file requires a documented change.

The workflow consists of nine stages.

---

# STEP 1 — SEO AUDIT

## Skill

`seo-audit`

## Skill File

`.agents/skills/seo-audit/SKILL.md`

## Execution Command

`$seo-audit`

## Purpose

Perform a comprehensive SEO audit of the target website.

Analyze the website's current SEO condition and identify:

- SEO issues
- SEO strengths
- Crawlability problems
- Indexability problems
- Technical SEO issues
- Metadata issues
- Content issues
- Page structure issues
- Website performance issues
- Mobile usability issues
- Search visibility opportunities
- Existing website pages
- Service pages
- Important URLs
- Potential SEO improvements

## Inputs

Provide:

- Validated intake configuration from Sections 4 and 5, including website URL, domain name, website name, brand name, target country, target audience, business type, services, seed keywords and frontend stack or explicit Unknown.
- Target geography, primary SEO objective and other optional inputs when supplied.
- Current execution date.

## Execution Instructions

1. Read the complete SEO Audit skill file.
2. Identify the required execution command.
3. Provide the initial user configuration.
4. Execute the SEO Audit skill.
5. Wait until the skill completely finishes.
6. Do not execute any other SEO skill during this stage.
7. Validate the stage completion.
8. Identify and record its actual output location.
9. Identify the discovered website pages.
10. Extract relevant SEO findings.
11. Update the execution tracker.
12. Update the execution log.

## Stage Completion Criteria

The stage must be marked COMPLETED only after:

- The skill execution has finished.
- Required outputs have been generated.
- Outputs have been verified.
- Execution status has been updated.

Only after successful completion may Step 2 begin.

---

# STEP 2 — KEYWORD RESEARCH AND MAPPING

## Skill

`seo-keyword-research`

## Skill File

`.agents/skills/seo-keyword-research/SKILL.md`

## Execution Command

`$seo-keyword-research`

## Purpose

Discover, expand, analyze, classify, and map relevant SEO keywords.

Analyze:

- Primary keywords
- Secondary keywords
- Long-tail keywords
- Commercial keywords
- Transactional keywords
- Informational keywords
- Local keywords
- Search intent
- Keyword opportunities
- Keyword gaps
- Keyword-to-page mapping
- Search intent alignment
- Keyword cannibalization

## Inputs

Provide:

- Initial user configuration
- Stage 1 SEO Audit findings
- Discovered website pages
- Services offered
- Seed keywords
- Target geography
- Target audience
- Business goals

## Execution Instructions

1. Read the complete Keyword Research skill file.
2. Identify its execution command.
3. Discover the completed SEO Audit output.
4. Identify relevant source data.
5. Provide the required inputs.
6. Execute the skill.
7. Wait for complete execution.
8. Do not start another SEO stage.
9. Validate its outputs.
10. Record the actual output location.
11. Extract keyword findings and mapping.
12. Update the execution tracker.
13. Update the execution log.

## Stage Completion Criteria

Mark COMPLETED only after successful execution and output validation.

Only after successful completion may Step 3 begin.

---

# STEP 3 — COMPETITOR ANALYSIS

## Skill

`seo-competitor-analysis`

## Skill File

`.agents/skills/seo-competitor-analysis/SKILL.md`

## Execution Command

`$seo-competitor-analysis`

## Purpose

Analyze relevant competitors and identify competitive SEO opportunities.

Analyze:

- Competitor websites
- Competitor positioning
- Competitor keywords
- Competitor content
- Competitor landing pages
- Competitor SEO strategies
- Content gaps
- Keyword gaps
- Backlink opportunities
- Search intent opportunities
- Differentiation opportunities

## Inputs

Provide:

- Initial user configuration
- SEO Audit findings
- Keyword Research findings
- Website page catalog
- Business positioning
- Target audience
- Known competitors, if available

## Execution Instructions

1. Read the complete Competitor Analysis skill file.
2. Identify its execution command.
3. Discover completed upstream outputs.
4. Select relevant source data.
5. Provide the required inputs.
6. Execute the skill.
7. Wait for complete execution.
8. Do not start another SEO stage.
9. Validate outputs.
10. Record the actual output location.
11. Extract relevant competitor findings.
12. Update the execution tracker.
13. Update the execution log.

## Stage Completion Criteria

Mark COMPLETED only after successful execution and output validation.

Only after successful completion may Step 4 begin.

---

# STEP 4 — ON-PAGE SEO ANALYSIS

## Skill

`seo-on-page`

## Skill File

`.agents/skills/seo-on-page/SKILL.md`

## Execution Command

`$seo-on-page`

## Purpose

Analyze website pages and identify page-level SEO improvements.

Analyze:

- Title tags
- Meta descriptions
- H1
- H2
- H3
- Content structure
- Keyword targeting
- Search intent
- Internal linking
- Image SEO
- Page content
- CTA opportunities
- Metadata optimization
- Page-level SEO opportunities

## Inputs

Provide:

- Initial user configuration
- SEO Audit findings
- Keyword Research findings
- Competitor Analysis findings
- Website page catalog
- Relevant keyword-to-page mapping

## Execution Instructions

1. Read the complete On-Page SEO skill file.
2. Identify its execution command.
3. Discover completed upstream outputs.
4. Identify relevant pages and data.
5. Provide required inputs.
6. Execute the skill.
7. Wait for complete execution.
8. Do not start another SEO stage.
9. Validate outputs.
10. Record the actual output location.
11. Extract page-level SEO findings.
12. Update the execution tracker.
13. Update the execution log.

## Stage Completion Criteria

Mark COMPLETED only after successful execution and output validation.

Only after successful completion may Step 5 begin.

---

# STEP 5 — CONTENT STRATEGY AND CONTENT CREATION

## Skill

`seo-content-strategy`

## Skill File

`.agents/skills/seo-content-strategy/SKILL.md`

## Execution Command

`$seo-content-strategy`

## Purpose

Develop a comprehensive SEO content strategy.

Analyze:

- Existing content
- Content gaps
- Content opportunities
- Content clusters
- Pillar pages
- Blog opportunities
- Service page opportunities
- New page opportunities
- Content briefs
- Content optimization
- Search intent
- Keyword mapping
- Content priorities

## Inputs

Provide:

- Initial user configuration
- SEO Audit findings
- Keyword Research findings
- Competitor Analysis findings
- On-Page SEO findings
- Existing website content
- Business objectives
- Brand voice
- Target audience

## Execution Instructions

1. Read the complete Content Strategy skill file.
2. Identify its execution command.
3. Discover completed upstream outputs.
4. Select relevant content and SEO findings.
5. Provide the required inputs.
6. Execute the skill.
7. Wait for complete execution.
8. Do not start another SEO stage.
9. Validate outputs.
10. Record the actual output location.
11. Extract content strategy findings.
12. Update the execution tracker.
13. Update the execution log.

## Stage Completion Criteria

Mark COMPLETED only after successful execution and output validation.

Only after successful completion may Step 6 begin.

---

# STEP 6 — TECHNICAL SEO

## Skill

`seo-technical`

## Skill File

`.agents/skills/technical-seo/SKILL.md`

## Execution Command

`$seo-technical`

## Purpose

Analyze the website's technical SEO condition.

Analyze:

- Crawlability
- Indexability
- Robots.txt
- XML Sitemap
- Canonical URLs
- Redirects
- HTTP status codes
- URL structure
- Structured data
- Core Web Vitals
- Page performance
- Mobile usability
- JavaScript rendering
- Technical SEO errors
- Website architecture

## Inputs

Provide:

- Initial user configuration
- SEO Audit findings
- Keyword Research findings
- On-Page SEO findings
- Content Strategy findings
- Website technical information
- Relevant website pages

## Execution Instructions

1. Read the complete Technical SEO skill file.
2. Identify its execution command.
3. Discover completed upstream outputs.
4. Identify relevant technical data.
5. Provide required inputs.
6. Execute the skill.
7. Wait for complete execution.
8. Do not start another SEO stage.
9. Validate outputs.
10. Record the actual output location.
11. Extract technical SEO findings.
12. Update the execution tracker.
13. Update the execution log.

## Stage Completion Criteria

Mark COMPLETED only after successful execution and output validation.

Only after successful completion may Step 7 begin.

---

# STEP 7 — OFF-PAGE SEO AND LINK BUILDING

## Skill

`seo-off-page`

## Skill File

`.agents/skills/off-page-seo/SKILL.md`

## Execution Command

`$seo-off-page`

## Purpose

Analyze off-page SEO and authority-building opportunities.

Analyze:

- Backlink profile
- Competitor backlinks
- Link gaps
- Link-building opportunities
- Brand mentions
- Digital PR
- Authority-building opportunities
- Local citations
- Off-page SEO risks

## Inputs

Provide:

- Initial user configuration
- SEO Audit findings
- Keyword Research findings
- Competitor Analysis findings
- Content Strategy findings
- Website positioning
- Target audience

## Execution Instructions

1. Read the complete Off-Page SEO skill file.
2. Identify its execution command.
3. Discover completed upstream outputs.
4. Select relevant source data.
5. Provide required inputs.
6. Execute the skill.
7. Wait for complete execution.
8. Do not start another SEO stage.
9. Validate outputs.
10. Record the actual output location.
11. Extract off-page SEO findings.
12. Update the execution tracker.
13. Update the execution log.

## Stage Completion Criteria

Mark COMPLETED only after successful execution and output validation.

Only after successful completion may Step 8 begin.

---

# STEP 8 — SEO MONITORING AND PERFORMANCE TRACKING

## Skill

`seo-monitoring`

## Skill File

`.agents/skills/seo-monitoring/SKILL.md`

## Execution Command

`$seo-monitoring`

## Purpose

Analyze SEO performance, tracking, and monitoring opportunities.

Analyze:

- Organic traffic
- Search impressions
- Click-through rate
- Search rankings
- Conversions
- Organic performance
- Technical SEO regressions
- KPI tracking
- Search performance trends
- Monitoring opportunities
- Ongoing optimization strategy

## Inputs

Provide:

- Initial user configuration
- SEO Audit findings
- Keyword Research findings
- Competitor Analysis findings
- On-Page SEO findings
- Content Strategy findings
- Technical SEO findings
- Off-Page SEO findings
- Available monitoring data

## Execution Instructions

1. Read the complete SEO Monitoring skill file.
2. Identify its execution command.
3. Discover completed upstream outputs.
4. Identify relevant monitoring data.
5. Provide required inputs.
6. Execute the skill.
7. Wait for complete execution.
8. Do not start another SEO stage.
9. Validate outputs.
10. Record the actual output location.
11. Extract monitoring findings.
12. Update the execution tracker.
13. Update the execution log.

## Stage Completion Criteria

Mark COMPLETED only after successful execution and output validation.

Only after successful completion may Step 9 begin.

---

# STEP 9 — FINAL SEO ANALYSIS AND MASTER DEVELOPER PROMPT

## Skill

`seo-final-report`

## Skill File

`.agents/skills/seo-final-report/SKILL.md`

## Execution Command

`$seo-final-report`

## Purpose

Consolidate the outputs of all completed SEO stages into a comprehensive final SEO analysis.

The final stage must generate:

### Deliverable 1

A comprehensive SEO Consolidated Final Report.

### Deliverable 2

A production-ready Master SEO Developer Prompt.

The Master Developer Prompt must instruct an AI coding agent to analyze the website codebase and implement the approved SEO improvements.

## Inputs

Provide:

- Initial user configuration
- All completed SEO stage output folder paths
- Execution tracker
- Execution history
- Missing data
- Stage limitations
- All completed upstream SEO findings

## Execution Instructions

1. Read the complete Final SEO Report skill file.
2. Identify its execution command.
3. Discover all completed upstream output directories.
4. Pass the correct output directory locations.
5. Pass the initial website configuration.
6. Pass execution history.
7. Execute the skill.
8. Wait for complete execution.
9. Do not execute any other SEO stage.
10. Validate all final deliverables.
11. Verify the consolidated SEO report.
12. Verify the Master SEO Developer Prompt.
13. Verify that both files exist.
14. Verify that both files are non-empty.
15. Read back the generated files.
16. Validate the required sections.
17. Update the execution tracker.
18. Update the execution log.

## Stage Completion Criteria

Mark COMPLETED only after:

- Final SEO Report is generated.
- Master SEO Developer Prompt is generated.
- Both files are verified.
- Required sections are present.
- Validation is completed.

---

# 10. STAGE EXECUTION CONTROL

Every SEO stage must follow this exact lifecycle.

## Stage Lifecycle

### 1. PENDING

The stage has not started.

### 2. INITIALIZING

The orchestrator is:

- Reading the skill file.
- Preparing inputs.
- Discovering dependencies.
- Preparing execution context.

### 3. RUNNING

The skill is actively executing.

No other SEO stage may execute during this state.

### 4. VALIDATING

The skill has finished execution.

The orchestrator is:

- Checking generated outputs.
- Verifying files.
- Checking required deliverables.
- Identifying errors.
- Validating execution.

No other SEO stage may execute during this state.

### 5. COMPLETED

The stage has completed successfully.

Its outputs are valid.

Its execution record has been updated.

The execution lock may be released.

### 6. FAILED

The stage failed.

The failure must be documented.

Dependent stages must not start.

### 7. BLOCKED

The stage cannot execute because a required dependency or input is missing.

Dependent stages must not start.

---

# 11. MANDATORY STAGE EXECUTION LOOP

For every stage:

```text
1. For Stage 1, confirm intake is READY. For Stages 2–9, confirm the previous stage is COMPLETED.
2. Confirm the current stage is PENDING.
3. Acquire the execution lock.
4. Read the complete skill file.
5. Identify the actual execution command.
6. Prepare the required inputs.
7. Identify relevant upstream outputs.
8. Execute the current skill.
9. WAIT for complete execution.
10. Confirm the skill has stopped running.
11. Validate the generated outputs.
12. Record the execution date.
13. Record the output locations.
14. Record the validation result.
15. Update the execution tracker.
16. Update the execution log.
17. Mark the stage COMPLETED.
18. Release the execution lock.
19. Only now may the next stage begin.
```

If any step fails:

```text
1. Stop the current pipeline.
2. Keep the current stage status as FAILED or BLOCKED.
3. Record the failure.
4. Record the error details.
5. Do not start the next stage.
6. Report the failure.
```

---

# 12. CONTEXT INHERITANCE

All downstream stages must inherit the initial user configuration.

The execution context includes the validated website URL, domain name, website name, brand name, target country, target audience, business type, services, seed keywords and frontend stack or explicit Unknown. Include target geography, competitors, SEO objective, brand voice, project ID, available data and additional context when supplied. Pass the actual execution date, required-field sources or confirmations and any optional omissions.

Do not ask the user to provide the same information again.

Each stage must also receive relevant completed upstream findings.

However:

Do not blindly pass every file from every previous stage.

Instead:

1. Read the current skill requirements.
2. Identify required upstream context.
3. Discover relevant upstream output folders.
4. Identify relevant reports and datasets.
5. Pass the required context.
6. Include execution dates.
7. Include source locations.
8. Include limitations.

---

# 13. UPSTREAM OUTPUT DISCOVERY

Each individual skill is responsible for defining its own output directory.

The orchestrator must not hardcode individual stage output directories unless explicitly required by the actual skill instructions.

For every completed stage:

1. Read its skill file.
2. Identify its output configuration.
3. Discover its actual output location.
4. Verify its outputs.
5. Record the actual output directory.
6. Pass that directory to relevant downstream stages.

Do not assume all stages use the same execution date.

Do not assume all stages use the same output folder structure.

Do not overwrite previous executions unless explicitly authorized.

---

# 14. SKILL FILE DISCOVERY AND COMMAND VALIDATION

The expected skill names listed in this orchestrator are logical identifiers.

Before executing a stage:

1. Search the actual `.agents/skills/` directory.
2. Identify the matching skill.
3. Verify the skill file.
4. Read the complete file.
5. Identify the actual execution command.
6. Confirm the command is compatible with the available AI tool.
7. Execute the actual skill.

If the skill name or command differs from the expected name:

- Use the actual discovered skill.
- Record the mapping.
- Do not invent a command.
- Do not execute an invalid command.

If the skill does not exist:

- Search for an equivalent skill.
- Verify its instructions.
- Do not silently substitute an unrelated skill.
- Report the missing skill if no valid equivalent exists.

---

# 15. EXECUTION TRACKER

Create:

`outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/seo-orchestration/Execution_Tracker.md`

Maintain the tracker throughout the entire workflow.

The tracker must contain:

| Stage | Skill               | Skill File  | Command        | Status | Start Time | End Time    | Output Location | Validation |
| ----- | ------------------- | ----------- | -------------- | ------ | ---------- | ----------- | --------------- | ---------- |
| 1     | SEO Audit           | Actual path | Actual command | Status | Time       | Actual path | Result          |
| 2     | Keyword Research    | Actual path | Actual command | Status | Time       | Actual path | Result          |
| 3     | Competitor Analysis | Actual path | Actual command | Status | Time       | Actual path | Result          |
| 4     | On-Page SEO         | Actual path | Actual command | Status | Time       | Actual path | Result          |
| 5     | Content Strategy    | Actual path | Actual command | Status | Time       | Actual path | Result          |
| 6     | Technical SEO       | Actual path | Actual command | Status | Time       | Actual path | Result          |
| 7     | Off-Page SEO        | Actual path | Actual command | Status | Time       | Actual path | Result          |
| 8     | SEO Monitoring      | Actual path | Actual command | Status | Time       | Actual path | Result          |
| 9     | Final SEO Report    | Actual path | Actual command | Status | Time       | Actual path | Result          |

Possible statuses:

- PENDING
- INITIALIZING
- RUNNING
- VALIDATING
- COMPLETED
- FAILED
- BLOCKED

The tracker must accurately reflect the actual execution state.

Do not mark a stage COMPLETED before validation.

---

# 16. EXECUTION LOG

Create:

`outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/seo-orchestration/Execution_Log.md`

Record:

- Workflow execution ID
- Website URL, domain name, website name and brand name
- Target country, target audience and target geography
- Business type, services, seed keywords and frontend technology stack
- Competitors, SEO objective, brand voice, project ID and available data when provided
- Current execution date, intake status, source of each required value and optional omissions
- Execution mode
- Execution start date
- Execution completion date
- Skills discovered
- Skill files read
- Actual commands used
- Stage execution order
- Stage start times
- Stage completion times
- Output locations
- Validation results
- Missing data
- Errors
- Warnings
- Retry attempts
- Final status

---

# 17. FAILURE HANDLING

If a stage fails:

1. Stop the workflow immediately.
2. Do not start the next stage.
3. Record the failure.
4. Record the error message.
5. Identify the failure category.
6. Determine whether a retry is appropriate.

Failure categories:

- Missing skill
- Invalid command
- Missing required input
- Website inaccessible
- Tool failure
- API failure
- Permission failure
- Output generation failure
- Validation failure
- Unexpected execution error

## Retry Policy

A retry may be attempted only when:

- The failure is recoverable.
- The cause is understood.
- The retry will not create duplicate or destructive results.

Do not retry indefinitely.

After a reasonable retry attempt:

- Mark the stage FAILED or BLOCKED.
- Update the tracker.
- Update the execution log.
- Stop dependent stages.
- Notify the user.

Do not silently skip a failed stage.

---

# 18. OPTIONAL DATA AND LIMITATIONS

Missing optional information must not interrupt the workflow unnecessarily.

Examples:

- Google Search Console unavailable
- Google Analytics unavailable
- Paid SEO tool unavailable
- Competitor data unavailable
- Backlink database unavailable
- Business address unavailable
- Business phone unavailable
- Historical rankings unavailable

When optional data is unavailable:

1. Record the limitation.
2. Use available evidence.
3. Avoid fabricated metrics.
4. Continue if the stage can still execute.
5. Clearly identify assumptions.

If required information is unavailable and the skill cannot execute:

- Mark the stage BLOCKED.
- Stop dependent stages.

---

# 19. WORKSPACE AND FILE MANAGEMENT

All orchestration tracking files must be stored within the current SEO workflow project's outputs directory.

Use:

`./outputs/`

Do not redirect outputs to unrelated projects.

Do not save orchestration files outside the current SEO workflow project unless explicitly authorized.

Do not overwrite previous execution reports.

Use the current execution date for orchestration tracking.

The individual SEO skills must determine their own output directories according to their respective instructions.

---

# 20. FINAL ORCHESTRATION SUMMARY

After the complete pipeline has finished, generate:

`outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/seo-orchestration/Orchestration_Summary.md`

Include:

## 1. Website Information

- Website URL, website name, brand name and domain
- Business type, technology stack, services and seed keywords
- Target country, target audience and target geography
- SEO objective and project ID when supplied

## 2. Workflow Execution

- Execution ID
- Execution date
- Execution mode
- Total stages
- Completed stages
- Failed stages
- Blocked stages
- Skipped stages

## 3. Stage-by-Stage Summary

For each stage:

- Stage name
- Skill name
- Skill file
- Execution command
- Status
- Execution date
- Actual output location
- Validation result

## 4. Major SEO Findings

Summarize the most important findings from completed stages.

## 5. SEO Opportunities

Summarize:

- Keyword opportunities
- Content opportunities
- Technical SEO opportunities
- Competitor opportunities
- On-page opportunities
- Off-page opportunities

## 6. Final Deliverables

Identify the actual files generated by each skill.

## 7. Master Developer Prompt

Identify the location of:

`MASTER_SEO_DEVELOPER_PROMPT.md`

## 8. Limitations

Document:

- Missing data
- Missing skills
- Failed stages
- Blocked stages
- Tool limitations
- Incomplete analysis

## 9. Recommended Next Action

Clearly state the next recommended step.

---

# 21. FINAL VALIDATION

Before declaring the workflow complete, verify:

## Initial Configuration

- Intake reached `READY` before Stage 1 began.
- The user supplied or confirmed the website URL, domain name, website name, brand name, target country, target audience, business type, services, seed keywords and frontend stack or explicit Unknown.
- The URL and domain were checked together and conflicts affecting scope were resolved.
- The source or confirmation of each required field was recorded.
- Optional inputs or omissions were recorded, including target geography, competitors, objective, brand voice, project ID and data sources where available.
- The actual execution date was recorded in `YYYY-MM-DD` format.

## Project Discovery

- Project root identified.
- Skills directory discovered.
- Relevant skill files discovered.
- Skill files read.
- Execution commands validated.

## Sequential Execution

- Stage 1 completed before Stage 2 started.
- Stage 2 completed before Stage 3 started.
- Stage 3 completed before Stage 4 started.
- Stage 4 completed before Stage 5 started.
- Stage 5 completed before Stage 6 started.
- Stage 6 completed before Stage 7 started.
- Stage 7 completed before Stage 8 started.
- Stage 8 completed before Stage 9 started.
- No stages executed simultaneously.
- No parallel stage execution occurred.
- No stage was started before its dependencies completed.

## Output Validation

- Every completed stage has valid outputs.
- Actual output locations recorded.
- Execution dates recorded.
- Outputs are not empty where required.
- Missing outputs documented.
- Failed stages documented.

## Final Deliverables

- Final SEO Report exists.
- Master SEO Developer Prompt exists.
- Both files are non-empty.
- Required sections exist.
- Final report validation completed.

## Orchestration Files

- Execution Tracker exists.
- Execution Log exists.
- Orchestration Summary exists.
- All files are verified.

---

# 22. FINAL RESPONSE

After execution, provide a concise summary.

Include:

- Website analyzed
- Execution date
- Workflow execution status
- Total stages
- Completed stages
- Failed stages
- Blocked stages
- Confirmation that execution was strictly sequential
- Major SEO findings
- Final SEO Report path
- Master SEO Developer Prompt path
- Execution Tracker path
- Execution Log path
- Orchestration Summary path
- Validation status
- Limitations
- Recommended next action

Do not claim that a stage was completed if it was not executed.

Do not claim that files were created unless they exist and have been verified.

Do not claim that website implementation has been completed during SEO analysis.

---

# 23. MASTER EXECUTION INSTRUCTION

Execute the complete SEO workflow using the website configuration supplied by the user.

## Initial Phase

1. Read the triggering message and any intake attachments.
2. Apply Sections 4 and 5. Request any unresolved required values together and keep all stages pending until intake is READY.
3. Discover the project using the validated intake.
4. Discover the SEO skills.
5. Read the complete skill instructions.
6. Validate the actual execution commands.
7. Prepare the execution tracker.
8. Prepare the execution log.

## Execution Phase

Execute the following stages STRICTLY ONE AT A TIME:

1. SEO Audit
2. Keyword Research and Mapping
3. Competitor Analysis
4. On-Page SEO
5. Content Strategy and Content Creation
6. Technical SEO
7. Off-Page SEO
8. SEO Monitoring
9. Final SEO Analysis and Master Developer Prompt Generation

For every stage:

- Read its skill file.
- Prepare the required inputs.
- Execute only that stage.
- Wait until it fully finishes.
- Validate its outputs.
- Record the execution status.
- Update the tracker.
- Update the log.
- Release the execution lock.
- Start the next stage only after successful completion.

## STRICT PROHIBITION

Never execute multiple SEO stages simultaneously.

Never execute stages in parallel.

Never start the next stage while the current stage is running or validating.

Never skip a stage silently.

Never bypass dependency validation.

## Final Phase

After the final stage:

1. Validate every completed stage.
2. Validate all final deliverables.
3. Verify the final SEO report.
4. Verify the Master SEO Developer Prompt.
5. Generate the orchestration summary.
6. Update the execution tracker.
7. Update the execution log.
8. Provide the final summary to the user.

The complete workflow must operate as a strictly sequential, dependency-aware, validated SEO automation pipeline from Initial Intake through Final SEO Report and Master Developer Prompt generation.
