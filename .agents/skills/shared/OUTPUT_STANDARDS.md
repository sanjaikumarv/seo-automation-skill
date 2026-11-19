# Canonical Output Directory Standards & Artifact Matrix

This document defines the canonical directory structure, artifact naming standards, and deliverable verification requirements for the complete SEO skills ecosystem.

---

## 1. Canonical Output Hierarchy

All skills must write their outputs inside the active workspace directory under the following canonical hierarchy:

```text
{OUT_PUT_ROOT_FOLDER}/
└── {{CURRENT_DATE}}/
    └── {{DOMAIN_NAME}}/
        ├── 00-orchestration/
        │   ├── orchestration-summary.md
        │   ├── execution-tracker.md
        │   └── execution-log.md
        ├── 01-website-audit/
        │   ├── website-audit-overall-report.md
        │   ├── website-audit-website-changes.md
        │   ├── SEO_Audit_Report.md
        │   ├── url-inventory.csv
        │   ├── technical-issues.csv
        │   ├── on-page-issues.csv
        │   ├── crawl-report.csv
        │   └── evidence/
        ├── 02-keyword-research/
        │   ├── keyword-research-overall-report.md
        │   ├── keyword-research-website-changes.md
        │   ├── Keyword_Research_Report.md
        │   ├── Keyword_Research_Data.csv
        │   ├── Seed_Keywords.csv
        │   ├── Keyword_Clusters.csv
        │   ├── Keyword_Mapping.csv
        │   └── Keyword_Prioritization.csv
        ├── 03-competitor-analysis/
        │   ├── competitor-analysis-overall-report.md
        │   ├── competitor-analysis-website-changes.md
        │   ├── Competitor_Analysis_Report.md
        │   ├── Competitor_List.csv
        │   ├── Competitor_Page_Analysis.csv
        │   ├── Competitor_Keyword_Gap.csv
        │   └── Competitor_Opportunity_Analysis.csv
        ├── 04-on-page-seo/
        │   ├── on-page-seo-overall-report.md
        │   ├── on-page-seo-website-changes.md
        │   ├── On_Page_SEO_Report.md
        │   ├── Developer_Prompt.md
        │   ├── Title_Meta_Optimization.csv
        │   ├── Heading_Optimization.csv
        │   ├── Content_Optimization.csv
        │   └── Internal_Link_Recommendations.csv
        ├── 05-content-strategy/
        │   ├── content-strategy-overall-report.md
        │   ├── content-strategy-website-changes.md
        │   ├── Content_Strategy_Report.md
        │   ├── Content_Calendar.csv
        │   ├── Topic_Cluster_Mapping.csv
        │   ├── content-briefs/
        │   └── content-drafts/
        ├── 06-technical-seo/
        │   ├── technical-seo-overall-report.md
        │   ├── technical-seo-website-changes.md
        │   ├── Technical_SEO_Report.md
        │   ├── Technical_SEO_Implementation_Plan.csv
        │   └── Schema_Implementation_Recommendations.csv
        ├── 07-off-page-seo/
        │   ├── off-page-seo-overall-report.md
        │   ├── off-page-seo-website-changes.md
        │   ├── Off_Page_SEO_Report.md
        │   ├── Outreach_Strategy.md
        │   └── Link_Prospect_Catalog.csv
        ├── 08-seo-monitoring/
        │   ├── seo-monitoring-overall-report.md
        │   ├── seo-monitoring-website-changes.md
        │   ├── SEO_Monitoring_Report.md
        │   └── SEO_KPI_Framework.md
        └── 09-final-seo-report/
            ├── final-seo-overall-report.md
            ├── final-seo-website-changes.md
            ├── Master_Developer_Implementation_Prompt.md
            ├── seo-implementation-roadmap.md
            ├── seo-priority-matrix.csv
            ├── keyword-implementation-plan.csv
            ├── metadata-implementation-plan.csv
            ├── heading-implementation-plan.csv
            ├── content-implementation-plan.csv
            ├── technical-implementation-plan.csv
            ├── internal-linking-implementation-plan.csv
            └── new-page-implementation-plan.csv
```

- **Output Root Folder (`OUT_PUT_ROOT_FOLDER`):** Defaults to `C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs`.
- If the date-and-domain directory already contains an earlier run, preserve previous runs under `executions/<execution-id>/` subdirectories.

---

## 2. Deliverable Matrix by Skill

Every stage skill must generate two mandatory deliverables:
1. `<skill-name>-overall-report.md`: High-level strategic report (Executive Summary, Data Sources, Free Tools Used, Methodology, Findings, Opportunities, Risks, Priority, Limitations).
2. `<skill-name>-website-changes.md`: Concrete, page-by-page register of exact website changes needed (Page URL, Category, Current Implementation, Suggested Optimized Implementation, Reason, Priority P0–P3, Implementation Steps, Validation).

| Stage Number | Skill Directory | Skill Name | Stage Directory | Strategic Overall Report | Concrete Changes Register | Core Datasets |
|---|---|---|---|---|---|---|
| **00** | `seo-orchestrator` | SEO Orchestrator | `00-orchestration/` | `orchestration-summary.md` | N/A | `execution-tracker.md`, `execution-log.md` |
| **01** | `seo-audit` | SEO Audit | `01-website-audit/` | `website-audit-overall-report.md` | `website-audit-website-changes.md` | `url-inventory.csv`, `technical-issues.csv`, `on-page-issues.csv` |
| **02** | `seo-keyword-research` | Keyword Research | `02-keyword-research/` | `keyword-research-overall-report.md` | `keyword-research-website-changes.md` | `Keyword_Research_Data.csv`, `Keyword_Clusters.csv`, `Keyword_Mapping.csv` |
| **03** | `seo-competitor-analysis` | Competitor Analysis | `03-competitor-analysis/` | `competitor-analysis-overall-report.md` | `competitor-analysis-website-changes.md` | `Competitor_List.csv`, `Competitor_Keyword_Gap.csv` |
| **04** | `seo-on-page` | On-Page SEO | `04-on-page-seo/` | `on-page-seo-overall-report.md` | `on-page-seo-website-changes.md` | `Developer_Prompt.md`, `Title_Meta_Optimization.csv`, `Heading_Optimization.csv` |
| **05** | `seo-content-strategy` | Content Strategy | `05-content-strategy/` | `content-strategy-overall-report.md` | `content-strategy-website-changes.md` | `Content_Calendar.csv`, `Topic_Cluster_Mapping.csv`, briefs, drafts |
| **06** | `technical-seo` | Technical SEO | `06-technical-seo/` | `technical-seo-overall-report.md` | `technical-seo-website-changes.md` | `Technical_SEO_Implementation_Plan.csv`, JSON-LD schemas |
| **07** | `off-page-seo` | Off-Page SEO | `07-off-page-seo/` | `off-page-seo-overall-report.md` | `off-page-seo-website-changes.md` | `Outreach_Strategy.md`, link prospect catalog |
| **08** | `seo-monitoring` | SEO Monitoring | `08-seo-monitoring/` | `seo-monitoring-overall-report.md` | `seo-monitoring-website-changes.md` | `SEO_KPI_Framework.md`, KPI tracking configuration |
| **09** | `seo-final-report` | Final Report | `09-final-seo-report/` | `final-seo-overall-report.md` | `final-seo-website-changes.md` | `Master_Developer_Implementation_Prompt.md`, `seo-implementation-roadmap.md`, `seo-priority-matrix.csv`, and 7 dedicated implementation CSVs |

---

## 3. Mandatory Output Validation Rules

Every skill must validate generated artifacts prior to declaring completion:
1. **Existence Verification:** The target stage directory under `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/` must exist.
2. **File Non-Empty Check:** Required files must exist with a size strictly greater than 0 bytes.
3. **Twin-Report Check:** Both `<skill-name>-overall-report.md` and `<skill-name>-website-changes.md` must be present.
4. **Dynamic Variable Resolution:** Ensure placeholders like `{{DOMAIN_NAME}}` or `{{WEBSITE_URL}}` have been rendered with real project values in the generated deliverables.
5. **No Hallucinated Analytics:** Any observational data without Google Search Console / Google Analytics authentication must be explicitly flagged as `[Public observational search data; requires Google Search Console verification]`.
