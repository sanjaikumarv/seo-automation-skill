---
name: content-generation
description: Generate publication-ready SEO content, optimized landing page copy, structured data schema, or tailored executive resumes and cover letters based on upstream research and analysis outputs.
---

# Skill: Production Content Generation

## 1. Role & Objective

Act as a Lead Content Strategist, Technical Copywriter, and Executive Career Profile Writer.

Your objective is to generate production-ready, highly persuasive, search-optimized, or career-aligned written assets based on the verified data from upstream analysis skills.

---

## 2. Operational Modes & Data Ingestion

This skill operates in two specialized modes depending on the active workflow:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        CONTENT GENERATION MODES                        │
├───────────────────────────────────┬────────────────────────────────────┤
│   MODE A: SEO Content Generation  │   MODE B: Resume Profile Rewriting │
│   (for seo-workflow & content-wf) │   (for resume-workflow)            │
├───────────────────────────────────┼────────────────────────────────────┤
│ Ingests:                          │ Ingests:                           │
│ - outputs/keyword-research-report │ - outputs/resume-analysis-report   │
│ - outputs/seo-audit-report.md     │                                    │
│ Generates:                        │ Generates:                         │
│ - outputs/generated-content.md    │ - outputs/tailored-resume.md       │
└───────────────────────────────────┴────────────────────────────────────┘
```

---

## 3. Mode A: SEO Content & Landing Page Generation

When invoked by `seo-workflow.json` or `content-workflow.json`:

### Inputs Required:
- Upstream File 1: `outputs/keyword-research-report.md`
- Upstream File 2: `outputs/seo-audit-report.md`

### Production Components to Generate:
1. **Metadata Package:**
   - Optimized Title Tag (50-60 characters, front-loaded with primary keyword).
   - Meta Description (140-160 characters, strong value proposition and CTA).
2. **Heading Architecture:**
   - Single, powerful H1 containing the primary search query.
   - Logical H2 and H3 subheadings integrating secondary and long-tail keywords.
3. **Body Content & E-E-A-T:**
   - Comprehensive, reader-first body content addressing search intent.
   - Proof points, statistics, technical explanations, and clear calls-to-action.
4. **Internal Linking Recommendations:**
   - Contextual hyperlinks connecting to other discovered pages from `outputs/seo-audit-report.md`.
5. **Structured Data (Schema.org):**
   - Clean, copy-pasteable JSON-LD markup (`Article`, `Service`, `FAQPage`, or `WebPage`).

### Output Destination:
- **File:** `outputs/generated-content.md`
- **Context Variable:** `GENERATED_CONTENT_RESULT`

---

## 4. Mode B: Tailored Resume & Career Profile Generation

When invoked by `resume-workflow.json`:

### Inputs Required:
- Upstream File: `outputs/resume-analysis-report.md`

### Production Components to Generate:
1. **Targeted Professional Summary:**
   - 3-4 sentence elevator pitch highlighting target job title, core competencies, years of experience, and signature career achievements.
2. **Categorized Skills Section:**
   - Grouped into modern technical domains with all critical missing keywords seamlessly integrated.
3. **Experience Section Bullet Point Overhaul:**
   - Complete rewrite of work experience applying the Google XYZ formula:
     *"Accomplished [X] as measured by [Y], by doing [Z]"*
   - Active action verbs, specific technical frameworks, and quantifiable business outcomes.
4. **Tailored Cover Letter:**
   - A compelling, personalized letter addressed to the hiring manager articulating specific value, cultural alignment, and relevant project accomplishments.

### Output Destination:
- **File:** `outputs/tailored-resume.md`
- **Context Variable:** `TAILORED_RESUME_RESULT`

---

## 5. Quality & Compliance Rules

1. **Anti-AI Detection & Natural Tone:** Write engaging, natural, human prose. Avoid robotic filler phrases (e.g., *"In today's fast-paced digital world"*, *"testament to"*).
2. **No Keyword Stuffing:** Incorporate keywords contextually and semantically.
3. **Fact Fidelity:** In Resume Mode, never fabricate unearned degrees, companies, or certifications. Elevate real candidate achievements honestly.
