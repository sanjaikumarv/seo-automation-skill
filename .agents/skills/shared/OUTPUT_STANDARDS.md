# Canonical Output Directory Standards & Artifact Matrix

This document defines the canonical directory structure, artifact naming standards, and deliverable verification requirements for the complete SEO skills ecosystem.

---

## 1. Canonical Output Hierarchy

All skills must write their outputs inside the active workspace directory under the following canonical hierarchy:

```text
outputs/
└── {{CURRENT_DATE}}/
    └── {{DOMAIN_NAME}}/
        ├── seo-orchestration/
        │   ├── Execution_Tracker.md
        │   ├── Execution_Log.md
        │   └── Orchestration_Summary.md
        ├── audit-report/
        │   ├── SEO_Audit_Report.md
        │   └── evidence/
        ├── keyword-research/
        │   ├── Keyword_Research_Report.md
        │   └── Keyword_Mapping_Master.md
        ├── competitor-analysis/
        │   └── Competitor_Analysis_Report.md
        ├── on-page-seo/
        │   ├── On_Page_SEO_Report.md
        │   └── Metadata_Matrix.md
        ├── content-strategy/
        │   ├── Content_Strategy_Report.md
        │   └── Content_Calendar.md
        ├── technical-seo/
        │   ├── Technical_SEO_Report.md
        │   └── Developer_Technical_Tasks.md
        ├── off-page-seo/
        │   ├── Off_Page_SEO_Report.md
        │   └── Outreach_Playbook.md
        ├── seo-monitoring/
        │   ├── SEO_Monitoring_Report.md
        │   └── KPI_Scorecard.md
        └── final-seo-report/
            ├── SEO_Consolidated_Final_Report.md
            └── Master_Developer_Implementation_Prompt.md
```

---

## 2. Deliverable Matrix by Skill

| Skill Directory           | Skill Name                    | Canonical Output Directory | Primary Required Deliverable       | Supporting Artifacts                            |
| ------------------------- | ----------------------------- | -------------------------- | ---------------------------------- | ----------------------------------------------- |
| `master-orchestrator`     | SEO Master Orchestrator       | `seo-orchestration/`       | `Orchestration_Summary.md`         | `Execution_Tracker.md`, `Execution_Log.md`      |
| `seo-audit`               | Comprehensive SEO Audit       | `audit-report/`            | `SEO_Audit_Report.md`              | `evidence/` (raw crawls, headers, responses)    |
| `seo-keyword-research`    | Strategic Keyword Research    | `keyword-research/`        | `Keyword_Research_Report.md`       | `Keyword_Mapping_Master.md`, keyword clusters   |
| `seo-competitor-analysis` | Competitor SEO Analysis       | `competitor-analysis/`     | `Competitor_Analysis_Report.md`    | Content & backlink gap tables                   |
| `seo-on-page`             | On-Page SEO Optimization      | `on-page-seo/`             | `On_Page_SEO_Report.md`            | `Metadata_Matrix.md`, heading blueprints        |
| `seo-content-strategy`    | Content Strategy & Planning   | `content-strategy/`        | `Content_Strategy_Report.md`       | `Content_Calendar.md`, content briefs           |
| `technical-seo`           | Technical SEO Implementation  | `technical-seo/`           | `Technical_SEO_Report.md`          | `Developer_Technical_Tasks.md`, JSON-LD schemas |
| `off-page-seo`            | Off-Page & Authority Building | `off-page-seo/`            | `Off_Page_SEO_Report.md`           | `Outreach_Playbook.md`, link prospect catalog   |
| `seo-monitoring`          | SEO Monitoring & Governance   | `seo-monitoring/`          | `SEO_Monitoring_Report.md`         | `KPI_Scorecard.md`, tracking configuration      |
| `seo-final-report`        | Consolidated Final Report     | `final-seo-report/`        | `SEO_Consolidated_Final_Report.md` | `Master_Developer_Implementation_Prompt.md`     |

---

## 3. Mandatory Output Validation Rules

Every skill must validate generated artifacts prior to declaring completion:

1. **Existence Verification:** The target directory `outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/{{SKILL_OUTPUT_DIRECTORY}}/` must exist.
2. **File Non-Empty Check:** Required files must exist with a size strictly greater than 0 bytes.
3. **Dynamic Variable Resolution:** Ensure placeholders like `{{DOMAIN_NAME}}` or `{{WEBSITE_URL}}` have been rendered with real project values in the generated deliverables, while templates and skill instruction files preserve the variable tokens.
4. **Current Workspace Directory Guardrail:** Never write files outside the workspace root (e.g. absolute paths to other projects or temporary OS folders).
