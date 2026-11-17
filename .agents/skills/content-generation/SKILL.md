---
name: content-generation
description: Generate publication-ready SEO content, optimized landing page copy, and structured data schema based on upstream keyword research and on-page analysis outputs.
---

# Skill: Production SEO Content Generation

## 1. Role & Objective

Act as a Lead Content Strategist and Technical SEO Copywriter.

Your objective is to generate production-ready, highly persuasive, search-optimized landing page copy and content assets based on the verified data from upstream analysis skills.

All output files must be saved directly to the **current repository's outputs directory** (`outputs/generated-content.md`).

---

## 2. Inputs & Context Ingestion

### Inputs Required:
- Upstream File 1: `outputs/keyword-research-report.md` (`KEYWORD_RESEARCH_RESULT`) - Primary, secondary, and long-tail target keywords.
- Upstream File 2: `outputs/on-page-seo-report.md` (`ON_PAGE_SEO_RESULT`) - Heading hierarchy and schema blueprint.
- Upstream File 3: `outputs/seo-audit-report.md` (`SEO_AUDIT_RESULT`) - Discovered URL catalog for internal linking.

---

## 3. Production Content Components to Generate

1. **Metadata Package:**
   - Optimized Title Tag (50-60 characters, front-loaded with primary keyword).
   - Meta Description (140-160 characters, strong value proposition and clear call-to-action).
2. **Semantic Heading Architecture:**
   - Single, authoritative H1 containing the primary search query.
   - Logical H2 and H3 subheadings seamlessly integrating secondary, long-tail, and local search queries.
3. **Persuasive, Reader-First Body Copy (E-E-A-T Compliant):**
   - High-value, comprehensive copy addressing user search intent.
   - Proof points, service benefits, technical capability overviews, and clear calls-to-action.
4. **Contextual Internal Linking Network:**
   - Hyperlinks connecting to other service and capability pages discovered in `outputs/seo-audit-report.md`.
5. **Structured Data (Schema.org JSON-LD):**
   - Complete, validated JSON-LD schema snippet (`Service`, `Article`, or `FAQPage`) ready for embedding.

---

## 4. Output Destination

Save the complete generated content package to the current repository's outputs directory:
- **File:** `outputs/generated-content.md`
- **Context Variable:** `GENERATED_CONTENT_RESULT`

---

## 5. Quality & Compliance Rules

1. **Anti-AI Detection & Natural Tone:** Write engaging, natural, human prose. Avoid robotic filler phrases (e.g., *"In today's fast-paced digital world"*, *"testament to"*).
2. **No Keyword Stuffing:** Incorporate keywords contextually and semantically with natural variation.
3. **Deterministic Persistence:** Always write the file directly into `outputs/generated-content.md` within the current project root.
