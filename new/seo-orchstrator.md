---
name: seo-orchestrator
description: Execute the complete SEO automation workflow by sequentially reading and following all five SEO skill files. Use when the user requests a complete SEO audit or end-to-end SEO analysis.
---

# SEO Master Orchestrator

## Role

You are the master controller of a strict sequential
SEO automation workflow.

Your responsibility is to execute all five skills
in the exact specified order.

## Required User Inputs

- Website URL
- Website Name
- Target Country
- Target Audience (optional)

Do not start until the mandatory inputs are available.

## Skill Locations

1. .agents/skills/website-audit/SKILL.md
2. .agents/skills/keyword-research/SKILL.md
3. .agents/skills/competitor-analysis/SKILL.md
4. .agents/skills/on-page-seo/SKILL.md
5. .agents/skills/seo-report/SKILL.md

## Execution Policy

STRICT SEQUENTIAL EXECUTION.

Never execute two skills simultaneously.

Never skip a skill.

Never assume that mentioning a skill means
that its instructions have been executed.

For every step:

1. Read the complete SKILL.md file.
2. Understand its instructions.
3. Validate its required inputs.
4. Execute the instructions.
5. Capture the complete output.
6. Validate the output.
7. Save the output in the execution context.
8. Continue to the next step only after success.

## Execution Steps

### STEP 1: Website Audit

Read and follow:
.agents/skills/website-audit/SKILL.md

Input:

- Website URL
- Website Name
- Target Country

Save the complete result as:
WEBSITE_AUDIT_RESULT

### STEP 2: Keyword Research

Read and follow:
.agents/skills/keyword-research/SKILL.md

Input:

- Original user inputs
- WEBSITE_AUDIT_RESULT

Save the complete result as:
KEYWORD_RESEARCH_RESULT

### STEP 3: Competitor Analysis

Read and follow:
.agents/skills/competitor-analysis/SKILL.md

Input:

- Original user inputs
- WEBSITE_AUDIT_RESULT
- KEYWORD_RESEARCH_RESULT

Save the complete result as:
COMPETITOR_ANALYSIS_RESULT

### STEP 4: On-Page SEO

Read and follow:
.agents/skills/on-page-seo/SKILL.md

Input:

- Original user inputs
- WEBSITE_AUDIT_RESULT
- KEYWORD_RESEARCH_RESULT
- COMPETITOR_ANALYSIS_RESULT

Save the complete result as:
ON_PAGE_SEO_RESULT

### STEP 5: Final SEO Report

Read and follow:
.agents/skills/seo-report/SKILL.md

Input:

- All previous skill results

Save the complete result as:
FINAL_SEO_REPORT

## Failure Handling

If any skill fails:

1. Stop execution.
2. Identify the failed skill.
3. Explain the failure.
4. Preserve completed results.
5. Do not execute later skills.
6. Ask the user before retrying if necessary.

Never silently skip a failed step.

## Progress Tracking

Maintain these statuses:

- PENDING
- IN_PROGRESS
- COMPLETED
- FAILED

Update execution status after every step.

Save execution logs under:
execution-logs/

Save final reports under:
output/

## Final Response

Display:

1. Website information
2. Execution summary
3. Individual skill statuses
4. Important findings
5. Final SEO report location
6. Limitations and failed operations

Only mark the workflow completed when all five
skills have successfully finished.
