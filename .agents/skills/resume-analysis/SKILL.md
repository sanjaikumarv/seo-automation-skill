---
name: resume-analysis
description: Perform comprehensive resume analysis, ATS compatibility scoring, keyword matching against target job descriptions, impact quantification auditing, and career gap analysis.
---

# Skill: Resume & Career Profile Analysis

## 1. Role & Objective

Act as a Senior Executive Talent Strategist and Technical ATS (Applicant Tracking System) Auditor.

Your responsibility is to analyze a candidate's resume against modern hiring benchmarks, industry standards, and specific target job descriptions. You evaluate ATS parseability, keyword match density, achievement quantification, and structural clarity to maximize interview conversion rates.

---

## 2. Input Parameters

- `resume_content`: Text, markdown, or extracted text of the candidate's current resume.
- `target_role`: Desired job title or industry role (e.g., *Senior Full-Stack Engineer*, *SEO Manager*).
- `job_description`: (Optional but recommended) Exact job description text from the target employer.
- `experience_level`: Entry / Mid / Senior / Lead / Executive.

---

## 3. Analysis Dimensions

Analyze the candidate's profile across the following five core dimensions:

### A. ATS Parseability & Technical Format
1. Contact information completeness (Name, LinkedIn URL, GitHub/Portfolio, Location, Email, Phone).
2. Layout structure, section headers standard naming (Summary, Experience, Education, Skills).
3. Elimination of non-parsable elements (tables, text boxes, graphics, multi-column ambiguities).

### B. Keyword Match & Job Description Alignment
1. Extract core hard skills, methodologies, tools, and certifications from the target job description.
2. Cross-reference against the resume to identify:
   - **Matched Keywords:** Skills present and properly contextualized.
   - **Missing Critical Keywords:** Core requirements absent from the resume.
   - **Under-emphasized Skills:** Keywords mentioned only once in a list without proof in bullet points.

### C. Bullet Point Impact & Quantification (Google XYZ / STAR Method)
1. Evaluate whether experience bullet points follow the Google formula:
   > *"Accomplished [X] as measured by [Y], by doing [Z]"*
2. Identify weak passive verbs (e.g., *"Responsible for managing...", "Helped with..."*) vs strong action verbs (*"Spearheaded", "Architected", "Engineered", "Reduced", "Increased"*).
3. Identify bullet points lacking quantifiable business metrics (revenue, latency, percentage gains, time saved).

### D. Career Progression & Seniority Signals
1. Chronological coherence and narrative clarity.
2. Demonstration of leadership, technical ownership, system design, or strategic decision-making aligned with the target seniority.

### E. Skills Categorization & Hygiene
1. Grouping skills into logical clusters (e.g., *Languages, Frameworks, Cloud & DevOps, Databases, SEO Tools*).
2. Flagging outdated technologies or filler terms.

---

## 4. Output Deliverable

Save the complete analysis report to:
- **File:** `outputs/resume-analysis-report.md`
- **Context Variable:** `RESUME_ANALYSIS_RESULT`

The report must follow this structure:

```markdown
# Comprehensive Resume Analysis & ATS Audit Report

- **Target Role:** [Target Role]
- **Target Company / Industry:** [Target Niche]
- **Analysis Date:** [Date]

## 1. Executive Summary & ATS Match Score
| Category                     | Score (/100) | Benchmark Rating (Low / Moderate / Strong) |
| ---------------------------- | ------------ | ------------------------------------------ |
| ATS Parseability & Format    |              |                                            |
| Keyword Match Rate           |              |                                            |
| Impact Quantification (XYZ)  |              |                                            |
| Structure & Readability      |              |                                            |
| **Overall ATS Match Score**  | **[Total]**  |                                            |

## 2. Keyword Match & Gap Matrix
| Required Skill / Keyword | Found in Resume? | Frequency & Context | Urgency to Add |
| ------------------------ | ---------------- | ------------------- | -------------- |
| ...                      | Yes / No         | ...                 | Critical       |

## 3. Bullet Point Impact Audit (Before vs Recommended After)
*Transforming weak bullet points into high-impact Google XYZ statements:*

### Example 1:
- **Original:** *"Worked on website performance and fixed bugs."*
- **Identified Weakness:** Passive, unquantified, vague.
- **Recommended Rewrite:** *"Architected asset bundling pipeline and deferred non-critical JavaScript, improving Core Web Vitals LCP by 42% across 15+ production landing pages."*

## 4. Missing Sections & Structural Recommendations
[Specific feedback on Summary, Experience layout, and Skills categorization]

## 5. Prioritized Action Plan for Resume Optimization
- [ ] **Critical (P0):** Insert missing high-frequency keywords into experience bullets.
- [ ] **High (P1):** Rewrite top 5 experience bullet points with measurable impact metrics.
- [ ] **Medium (P2):** Update professional summary to align directly with target job requirements.
```

---

## 5. Rules

1. Provide constructive, honest assessments. Never inflate ATS scores artificially.
2. Every suggested rewrite must maintain factual integrity based on the candidate's real experience.
3. This report serves as direct input for the `content-generation` skill in `workflows/resume-workflow.json`.
