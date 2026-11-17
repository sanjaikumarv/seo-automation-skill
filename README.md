# Multi-Workflow AI Automation

An enterprise-grade, sequential multi-agent automation system featuring specialized skills and declarative workflow pipelines.

---

## 1. Directory Structure

```
ai-automation/
│
├── .agents/
│   └── skills/
│       ├── master-orchestrator/
│       │   └── SKILL.md             # Master controller executing declarative workflows
│       ├── seo-audit/
│       │   └── SKILL.md             # Comprehensive Technical SEO & Infrastructure Audit
│       ├── keyword-research/
│       │   └── SKILL.md             # Keyword Discovery, Intent Mapping & Content Gaps
│       ├── resume-analysis/
│       │   └── SKILL.md             # ATS Compatibility, Keyword Gap & Impact Audit
│       └── content-generation/
│           └── SKILL.md             # SEO Content, Landing Pages, Schema & Resume Rewrites
│
├── workflows/
│   ├── seo-workflow.json            # SEO audit -> keyword research -> content generation
│   ├── resume-workflow.json         # Resume ATS analysis -> tailored resume & cover letter
│   └── content-workflow.json        # Keyword research -> reader-first content generation
│
├── outputs/                         # Destination for all generated reports and deliverables
│   └── .gitkeep
│
└── logs/                            # Real-time state tracking and execution logs
    ├── .gitkeep
    └── pipeline-state.json
```

---

## 2. Workflows & Skill Execution Pipelines

### A. SEO Automation Workflow (`workflows/seo-workflow.json`)
```
[User Input: Website URL, Target Country]
  │
  ▼
[Step 1: seo-audit]
  │  Writes: outputs/seo-audit-report.md
  ▼
[Step 2: keyword-research]
  │  Reads: outputs/seo-audit-report.md
  │  Writes: outputs/keyword-research-report.md
  ▼
[Step 3: content-generation]
  │  Reads: outputs/seo-audit-report.md & outputs/keyword-research-report.md
  │  Writes: outputs/generated-content.md
```

### B. Resume Optimization Workflow (`workflows/resume-workflow.json`)
```
[User Input: Candidate Resume, Target Job Description]
  │
  ▼
[Step 1: resume-analysis]
  │  Writes: outputs/resume-analysis-report.md (ATS Score, Keyword Gaps, XYZ Bullet Audit)
  ▼
[Step 2: content-generation (Resume Mode)]
  │  Reads: outputs/resume-analysis-report.md
  │  Writes: outputs/tailored-resume.md (Executive Summary, XYZ Bullet Rewrites, Cover Letter)
```

### C. Targeted Content Generation Workflow (`workflows/content-workflow.json`)
```
[User Input: Topic / Niche, Target Audience]
  │
  ▼
[Step 1: keyword-research]
  │  Writes: outputs/keyword-research-report.md
  ▼
[Step 2: content-generation (SEO Content Mode)]
  │  Reads: outputs/keyword-research-report.md
  │  Writes: outputs/generated-content.md (Metadata, H1-H3 Hierarchy, Schema JSON-LD)
```

---

## 3. Data Passing Contract (Inter-Skill Access)

Every skill writes its output to a deterministic markdown file in `outputs/` and exports a structured context variable:

| Workflow | Step | Running Skill | Upstream File Read | Generated Deliverable |
| :--- | :--- | :--- | :--- | :--- |
| **SEO** | 1 | `seo-audit` | Initial User Inputs | `outputs/seo-audit-report.md` |
| **SEO** | 2 | `keyword-research` | `outputs/seo-audit-report.md` | `outputs/keyword-research-report.md` |
| **SEO** | 3 | `content-generation`| `outputs/seo-audit-report.md` + `outputs/keyword-research-report.md` | `outputs/generated-content.md` |
| **Resume** | 1 | `resume-analysis` | Candidate Resume & Job Description | `outputs/resume-analysis-report.md` |
| **Resume** | 2 | `content-generation`| `outputs/resume-analysis-report.md` | `outputs/tailored-resume.md` |
| **Content**| 1 | `keyword-research` | Topic & Target Audience | `outputs/keyword-research-report.md` |
| **Content**| 2 | `content-generation`| `outputs/keyword-research-report.md` | `outputs/generated-content.md` |

---

## 4. Execution Directives

1. **Sequential Execution:** Steps are executed in strict chronological order. Step N cannot start until Step N-1 has status `COMPLETED`.
2. **Context Continuity:** Downstream skills must ingest and cite the outputs of upstream skills before formulating recommendations.
3. **Audit Logging:** Every step transition is tracked in `logs/pipeline-state.json`.
4. **Data Integrity:** No fabricated metrics, rankings, or qualifications.
