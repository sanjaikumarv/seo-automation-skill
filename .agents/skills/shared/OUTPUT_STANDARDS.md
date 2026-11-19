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
        │   └── Keyword_Mapping.csv
        ├── competitor-analysis/
        │   └── Competitor_Analysis_Report.md
        ├── on-page-seo/
        │   ├── On_Page_SEO_Report.md
        │   └── Title_Meta_Optimization.csv
        ├── content-strategy/
        │   ├── Content_Strategy_Report.md
        │   └── Content_Calendar.csv
        ├── technical-seo/
        │   ├── Technical_SEO_Report.md
        │   └── Technical_SEO_Implementation_Plan.csv
        ├── off-page-seo/
        │   ├── Off_Page_SEO_Report.md
        │   └── Outreach_Strategy.md
        ├── seo-monitoring/
        │   ├── SEO_Monitoring_Report.md
        │   └── SEO_KPI_Framework.md
        └── final-seo-report/
            ├── SEO_Consolidated_Final_Report.md
            ├── Master_Developer_Implementation_Prompt.md
            └── seo-updates.md
```

If the date-and-domain directory already contains an earlier run, keep the same structure under `outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/runs/<run-id>/`. Use the paths recorded for the active run when reading upstream artifacts. The orchestrator can also publish the completed implementation package at `outputs/seo-updates.md` when that path is available.

---

## 2. Deliverable Matrix by Skill

| Skill Directory           | Skill Name                    | Canonical Output Directory | Primary Required Deliverable       | Supporting Artifacts                            |
| ------------------------- | ----------------------------- | -------------------------- | ---------------------------------- | ----------------------------------------------- |
| `seo-orchestrator`        | SEO Orchestrator              | `seo-orchestration/`       | `Orchestration_Summary.md`         | `Execution_Tracker.md`, `Execution_Log.md`      |
| `seo-audit`               | Comprehensive SEO Audit       | `audit-report/`            | `SEO_Audit_Report.md`              | `evidence/` (raw crawls, headers, responses)    |
| `seo-keyword-research`    | Strategic Keyword Research    | `keyword-research/`        | `Keyword_Research_Report.md`       | `Keyword_Mapping.csv`, keyword clusters   |
| `seo-competitor-analysis` | Competitor SEO Analysis       | `competitor-analysis/`     | `Competitor_Analysis_Report.md`    | Content & backlink gap tables                   |
| `seo-on-page`             | On-Page SEO Optimization      | `on-page-seo/`             | `On_Page_SEO_Report.md`            | `Title_Meta_Optimization.csv`, heading blueprints        |
| `seo-content-strategy`    | Content Strategy & Planning   | `content-strategy/`        | `Content_Strategy_Report.md`       | `Content_Calendar.csv`, content briefs           |
| `technical-seo`           | Technical SEO Implementation  | `technical-seo/`           | `Technical_SEO_Report.md`          | `Technical_SEO_Implementation_Plan.csv`, JSON-LD schemas |
| `off-page-seo`            | Off-Page & Authority Building | `off-page-seo/`            | `Off_Page_SEO_Report.md`           | `Outreach_Strategy.md`, link prospect catalog   |
| `seo-monitoring` | SEO Monitoring & Governance | `seo-monitoring/`        | `SEO_Monitoring_Report.md`         | `SEO_KPI_Framework.md`, tracking configuration      |
| `seo-final-report`        | Consolidated Final Report     | `final-seo-report/`        | `SEO_Consolidated_Final_Report.md` | `Master_Developer_Implementation_Prompt.md`, `seo-updates.md` (orchestrated run) |

---

## 3. Mandatory Output Validation Rules

Every skill must validate generated artifacts prior to declaring completion:

1. **Existence Verification:** The target stage directory under the active run's output root must exist.
2. **File Non-Empty Check:** Required files must exist with a size strictly greater than 0 bytes.
3. **Dynamic Variable Resolution:** Ensure placeholders like `{{DOMAIN_NAME}}` or `{{WEBSITE_URL}}` have been rendered with real project values in the generated deliverables, while templates and skill instruction files preserve the variable tokens.
4. **Current Workspace Directory Guardrail:** Never write files outside the workspace root (e.g. absolute paths to other projects or temporary OS folders).
