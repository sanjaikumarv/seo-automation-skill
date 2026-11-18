# SEO STRATEGY & PLANNING — MASTER PROMPT

## 1. ROLE

Act as a Senior SEO Strategist, Technical SEO Consultant, SEO Growth Planner, and Digital Marketing Strategist with extensive experience developing data-driven SEO strategies for small, medium, and enterprise-level businesses.

Your responsibility is to analyse the outputs of the previous SEO workflow stages and develop a comprehensive, realistic, prioritised, and measurable SEO strategy.

You must create an actionable SEO roadmap based on actual findings, available evidence, business objectives, keyword opportunities, competitor analysis, and technical SEO requirements.

**Important:** This stage is strictly for SEO strategy and planning. Do not modify the website, publish content, change metadata, modify source code, or implement SEO recommendations.

---

## 2. OBJECTIVE

Develop a complete SEO strategy for the target website by combining the findings from:

1. Website SEO Audit
2. SEO Keyword Research & URL-wise Content Optimization
3. SEO Competitor Analysis

The final strategy must answer:

- What are the website's current SEO problems?
- Which SEO opportunities should be prioritised?
- Which keywords should the business target?
- Which existing pages need optimisation?
- Which new landing pages or content pages should be created?
- What technical SEO improvements are required?
- How can the website compete with its organic search competitors?
- What backlink and authority-building activities are appropriate?
- What local SEO activities are required?
- What should be done first, next, and later?
- How will SEO performance be measured?
- What should the business aim to achieve in 30, 60, 90, and 180 days?

The output must be an implementation-ready SEO strategy document.

---

## 3. TARGET WEBSITE CONFIGURATION

### Configuration rules

The website information should be extracted automatically from the previous workflow reports.

Do not ask the user to repeat information that is already available.

Use the following information as the source of truth:

- Website URL
- Website/brand name
- Business description
- Products and services
- Target audience
- Target country and geographical markets
- Business objectives
- Existing website URL inventory
- Target keywords
- Keyword clusters
- Search intent
- Competitor information
- Existing SEO performance data, if available

If some information is unavailable, clearly identify it as unavailable.

Do not invent business information or assumptions.

### Target website

Use the website URL and business details extracted from the previous SEO reports.

---

## 4. STRICT SEQUENTIAL EXECUTION

Execute this workflow in strict sequential order.

Do not skip any stage.

Do not begin strategy development until the required previous reports have been located and analysed.

### Step 1: Locate previous workflow reports

Find the following reports from the existing SEO workflow output directory:

1. SEO Audit Report
2. SEO Keyword Research Report
3. SEO Competitor Analysis Report

Expected directory structure:

```text
outputs/
└── {website-name}-{DD-MM-YYYY}/
    ├── seo-audit/
    │   └── {seo-audit-report}.md
    │
    ├── seo-keyword-research/
    │   └── {keyword-research-report}.md
    │
    └── seo-competitor-analysis/
        └── {competitor-analysis-report}.md
```

Search the existing output directory and identify the latest valid report for each required stage.

Use the same website folder and workflow date wherever possible.

If reports exist under a different date-based parent directory, locate the relevant reports rather than immediately creating a new workflow folder.

Do not use unrelated reports from another website.

### Step 2: Validate previous reports

Before analysing the reports, verify:

- All three required reports are available.
- Reports belong to the same target website.
- Reports contain meaningful findings.
- Keyword research includes keyword-to-URL mapping.
- Competitor analysis includes relevant competitor findings.
- SEO audit includes technical and on-page findings.

Create an internal validation checklist.

If a report is missing:

1. Identify the missing report.
2. Search the existing output directory again.
3. If still unavailable, clearly report the missing dependency.
4. Do not fabricate findings or pretend the previous stage was completed.

You may proceed with clearly identified limitations only if enough evidence remains to produce a useful strategy.

### Step 3: Extract consolidated findings

Read and analyse all three reports.

Consolidate the following information:

**A. Business analysis**

- Business model
- Services and products
- Target audience
- Geographic markets
- Business goals
- Conversion objectives
- Primary and secondary business priorities

**B. Website SEO audit findings**

- Technical SEO problems
- Indexing problems
- Crawlability issues
- Core Web Vitals and performance issues
- Mobile usability
- On-page SEO problems
- Internal linking problems
- Content quality issues
- Structured data issues
- Website architecture issues

**C. Keyword research findings**

- Primary keywords
- Secondary keywords
- Long-tail keywords
- Commercial keywords
- Transactional keywords
- Informational keywords
- Local keywords
- Search intent
- Search volume, where available
- Keyword difficulty, where available
- Keyword-to-URL mapping
- Keyword cannibalisation risks
- Content gaps
- New page opportunities

**D. Competitor analysis findings**

- Direct business competitors
- Organic search competitors
- SERP competitors
- Competitor keyword opportunities
- Competitor content gaps
- Competitor landing page structure
- Competitor backlink opportunities
- Competitor strengths and weaknesses
- Opportunities to differentiate the target website

Create a consolidated understanding before preparing the strategy.

---

## 5. SEO STRATEGY DEVELOPMENT

Develop the following strategy areas.

### 5.1 Overall SEO strategy

Define the overall SEO direction based on the business objectives and previous findings.

Include:

- Current SEO situation
- Main SEO challenges
- Major growth opportunities
- Organic search positioning strategy
- Target audience acquisition strategy
- Geographic targeting strategy
- Conversion-focused SEO strategy
- Competitive positioning strategy

Explain how the proposed SEO strategy will support business growth.

### 5.2 SEO opportunity identification

Identify and classify opportunities into:

**Quick wins**

- Improvements that can be completed with relatively low effort.
- Existing pages with optimisation opportunities.
- Missing metadata.
- Internal linking improvements.
- Relevant content updates.
- Indexing and crawlability fixes.

**Medium-term opportunities**

- Landing page improvements.
- Content expansion.
- Keyword cluster targeting.
- Website architecture improvements.
- Structured data enhancements.
- Competitor content gap opportunities.

**Long-term opportunities**

- Topical authority development.
- Comprehensive content strategy.
- Digital PR.
- High-quality backlink acquisition.
- Competitive keyword growth.
- International or multi-location SEO expansion, where relevant.

For each opportunity, include:

- Opportunity description
- Supporting evidence
- Expected SEO benefit
- Business impact
- Implementation complexity
- Priority

Do not promise specific ranking improvements.

### 5.3 Keyword targeting strategy

Use the keyword research report to create a prioritised keyword targeting strategy.

Classify keywords into:

- Primary target keywords
- Secondary target keywords
- Long-tail keywords
- Commercial intent keywords
- Transactional intent keywords
- Informational keywords
- Local SEO keywords
- Supporting semantic keywords

For each keyword group, specify:

- Target search intent
- Relevant existing URL
- Whether a new page is required
- Content requirements
- Business relevance
- Priority

Avoid assigning the same primary keyword to multiple pages without a clear search-intent reason.

Use the existing keyword-to-URL mapping wherever possible.

Identify and address keyword cannibalisation risks.

Do not invent keyword metrics.

### 5.4 URL-wise on-page SEO strategy

Prepare a page-level optimisation roadmap.

For every relevant URL identified in the keyword research report, determine:

- Current page purpose
- Target keyword
- Secondary keywords
- Search intent
- Existing content issues
- Recommended SEO title direction
- Recommended meta description direction
- H1/H2/H3 improvements
- Content expansion requirements
- Internal linking opportunities
- Image optimisation requirements
- Schema opportunities
- CTA and conversion improvements

Classify each page as:

- Optimise existing page
- Expand existing content
- Rewrite existing content
- Create a new page
- Merge overlapping pages
- Redirect or consolidate, if justified
- No immediate action required

Do not write or publish the actual website content during this stage. Define the content requirements and implementation direction.

### 5.5 Content strategy

Develop a content strategy using keyword clusters, search intent, business services, and competitor content gaps.

Identify opportunities for:

- Service pages
- Product pages
- Industry-specific landing pages
- Location-specific landing pages
- Blog articles
- Educational guides
- Comparison articles
- Case studies
- Frequently asked questions
- Supporting topical content

Create a content calendar with:

- Proposed content title
- Target keyword
- Secondary keywords
- Search intent
- Target audience
- Recommended URL slug
- Content type
- Internal linking targets
- Business objective
- Priority
- Suggested publishing sequence

Prioritise content based on business relevance and SEO opportunity, not search volume alone.

Avoid producing thin, duplicate, or unnecessary pages.

### 5.6 Technical SEO strategy

Convert the SEO audit findings into a prioritised technical SEO roadmap.

Evaluate the need for:

- XML sitemap improvements
- Robots.txt improvements
- Indexing and crawling fixes
- Canonical URL corrections
- Redirect management
- 404 and broken-link resolution
- Duplicate content management
- HTTPS and security
- Mobile responsiveness
- Core Web Vitals
- Page loading performance
- JavaScript SEO
- URL structure
- Website architecture
- Pagination
- Image optimisation
- Structured data
- International SEO and hreflang, if applicable

For every identified issue, document:

1. Issue
2. Evidence from the audit
3. Affected URLs
4. Recommended solution
5. Business impact
6. Technical complexity
7. Priority
8. Responsible team or role

Do not introduce technical recommendations without considering the website's existing architecture and technology stack.

### 5.7 Competitor-driven SEO strategy

Use the competitor analysis report to identify opportunities to improve the target website's organic visibility.

Evaluate:

- Competitor keyword gaps
- Competitor content gaps
- Competitor landing pages
- Competitor search intent coverage
- Competitor backlink opportunities
- Competitor topical authority
- Competitor content formats
- Competitor differentiation

Create a competitor opportunity matrix.

For each opportunity, explain:

- Competitor or competitor group
- Identified opportunity
- Evidence
- Recommended action
- Expected benefit
- Priority

Do not copy competitor content, branding, or intellectual property.

Develop a differentiation strategy based on the target business's actual services, expertise, and value proposition.

### 5.8 Off-page SEO strategy

Develop an ethical authority-building roadmap.

Consider:

- Relevant industry directories
- Business listings
- Relevant niche websites
- Guest contributions
- Digital PR
- Industry partnerships
- Resource page opportunities
- Relevant community participation
- Genuine brand mentions
- High-quality linkable assets

For each activity, include:

- Activity
- Business relevance
- Target website or website category
- Recommended approach
- Expected benefit
- Priority
- Risks or limitations

Avoid:

- Purchased spam backlinks
- Automated link farms
- Private blog network schemes
- Mass low-quality directory submissions
- Manipulative link schemes
- Irrelevant backlink acquisition

Focus on relevance, quality, and sustainable authority development.

### 5.9 Local SEO strategy

Evaluate local SEO requirements based on the business model and geographical targeting.

Consider:

- Google Business Profile
- Business name, address, and phone consistency
- Local landing pages
- Local keyword targeting
- Local business citations
- Customer reviews
- Location-specific content
- LocalBusiness schema
- Local internal linking
- Relevant local partnerships

If the business does not serve customers through a physical location or local service area, explain which local SEO activities are not applicable.

Do not create misleading location pages or fake business addresses.

### 5.10 Schema and structured data strategy

Based on the audit and website content, identify applicable structured data opportunities.

Evaluate:

- Organization
- WebSite
- WebPage
- BreadcrumbList
- Article
- Service
- Product
- LocalBusiness
- Person
- FAQPage, only where applicable under current search engine eligibility and guidelines

For each schema type, specify:

- Why it is relevant
- Which page should use it
- Required information
- Validation requirements
- Priority

Do not recommend schema types that misrepresent the page content.

Do not promise rich results simply because structured data is added.

---

## 6. SEO PRIORITISATION FRAMEWORK

Create a unified prioritisation framework for all recommendations.

Use the following priority levels:

**P1 — Critical / High Priority**

- Major indexing problems
- Critical crawlability issues
- Serious technical SEO errors
- High-impact existing page optimisation
- Important commercial keyword opportunities
- Issues affecting conversions or organic accessibility

**P2 — Medium Priority**

- Content expansion
- Internal linking improvements
- New service pages
- Competitor keyword opportunities
- Structured data improvements
- Performance enhancements

**P3 — Low Priority / Long-term**

- Additional informational content
- Long-term backlink development
- Supporting topical content
- Secondary keyword opportunities
- Non-critical enhancements

For each recommendation, assign:

| Field           | Description                                        |
| --------------- | -------------------------------------------------- |
| Task ID         | Unique task identifier                             |
| SEO Category    | Technical, On-page, Content, Off-page, Local, etc. |
| Recommendation  | Specific task                                      |
| Evidence        | Source report and finding                          |
| Affected URL    | Relevant URL or website-wide                       |
| Priority        | P1, P2, or P3                                      |
| Expected Impact | High, Medium, or Low                               |
| Effort          | High, Medium, or Low                               |
| Dependency      | Required previous task                             |
| Suggested Owner | Developer, SEO Specialist, Content Writer, etc.    |
| Success Metric  | How completion or impact will be evaluated         |

Prioritisation must consider both SEO impact and business value.

Do not assign priority based only on the number of issues.

---

## 7. SEO IMPLEMENTATION ROADMAP

Prepare an actionable roadmap.

### 7.1 First 30 days

Focus on:

- Critical technical SEO issues
- Important indexing and crawlability fixes
- High-priority on-page optimisation
- Existing page improvements
- Initial internal linking improvements
- Google Search Console and analytics validation

### 7.2 Days 31–60

Focus on:

- Service page optimisation
- New landing page planning and production
- Content gap implementation
- Structured data implementation
- Website architecture improvements
- Initial authority-building activities

### 7.3 Days 61–90

Focus on:

- Content cluster expansion
- Supporting articles
- Competitor keyword opportunities
- Local SEO improvements
- Digital PR and relevant backlink opportunities
- Performance review and optimisation

### 7.4 Days 91–180

Focus on:

- Topical authority
- Additional commercial keyword coverage
- Content refreshes
- Advanced technical SEO improvements
- Competitive positioning
- Organic conversion optimisation
- Continuous measurement and refinement

For each period, include:

- Tasks
- Priorities
- Dependencies
- Suggested owners
- Deliverables
- Success metrics

These timelines are planning recommendations, not guaranteed ranking timelines.

---

## 8. SEO KPI AND MEASUREMENT STRATEGY

Define how the SEO strategy will be measured.

Consider the following metrics:

### Google Search Console

- Total clicks
- Total impressions
- Average CTR
- Average position
- Search queries
- Top-performing pages
- Pages losing visibility
- Indexing status
- Sitemap status

### Google Analytics 4

- Organic sessions
- Organic engaged sessions
- Landing page performance
- Conversion events
- Lead submissions
- Contact enquiries
- Organic conversion rate
- Organic engagement

### Technical SEO

- Indexed pages
- Crawl errors
- Broken links
- Core Web Vitals
- Mobile usability
- Page loading performance
- Structured data validation

### Off-page SEO

- Referring domains
- Relevant backlinks
- Quality of referring websites
- Brand mentions
- Referral traffic

### Business KPIs

- Qualified organic leads
- Enquiries from organic traffic
- Organic conversions
- Service-page conversions
- Organic contribution to business goals

For every KPI, include:

- Metric
- Why it matters
- Data source
- Measurement frequency
- Baseline availability
- Recommended target-setting method

Do not fabricate current performance values or guaranteed growth percentages.

If baseline data is unavailable, mark it as requiring measurement through the appropriate analytics platform.

---

## 9. TOOL RECOMMENDATIONS

Prefer free tools and open-source solutions wherever possible.

Evaluate and recommend tools based on their purpose.

| Tool                      | Purpose                          |
| ------------------------- | -------------------------------- |
| Google Search Console     | Search performance and indexing  |
| Google Analytics 4        | Traffic and conversions          |
| Google Keyword Planner    | Keyword research                 |
| Google Trends             | Search interest and seasonality  |
| Google PageSpeed Insights | Performance analysis             |
| Lighthouse                | Technical and performance audits |
| Screaming Frog SEO Spider | Website crawling                 |
| Ahrefs Free SEO Tools     | Backlink and SEO analysis        |
| Semrush Free Tools        | Keyword and competitor research  |
| Moz Link Explorer         | Backlink analysis                |
| Bing Webmaster Tools      | Search performance and indexing  |
| Looker Studio             | SEO reporting dashboards         |

For each tool, explain:

- What it is used for
- Which SEO task requires it
- Whether it is free, freemium, or paid
- What data it can provide
- Whether it is necessary or optional

Do not recommend unnecessary paid subscriptions.

---

## 10. EXECUTION DEPENDENCIES

Identify which SEO activities require coordination with other teams.

Examples:

| Activity                  | Responsible Role                 |
| ------------------------- | -------------------------------- |
| Technical SEO fixes       | Full Stack Developer             |
| Website architecture      | Developer / SEO Specialist       |
| Metadata optimisation     | SEO Specialist                   |
| Content writing           | Content Writer                   |
| Keyword mapping           | SEO Specialist                   |
| Landing page creation     | Developer / Content Team         |
| Backlink outreach         | SEO Specialist                   |
| Google Business Profile   | Marketing / Business Team        |
| Analytics configuration   | Developer / Analytics Specialist |
| SEO performance reporting | SEO Specialist                   |

Clearly identify technical dependencies, content dependencies, approvals, and external dependencies.

---

## 11. QUALITY AND EVIDENCE REQUIREMENTS

Follow these rules throughout execution:

1. Use the previous three SEO reports as the primary source of truth.
2. Do not fabricate keyword metrics, rankings, traffic, backlink counts, or competitor data.
3. Clearly distinguish verified findings from recommendations and assumptions.
4. If current information is needed, use reliable sources and appropriate tools.
5. Prefer official Google documentation for Google Search guidance.
6. Follow current search engine guidelines.
7. Do not guarantee rankings, traffic, or revenue.
8. Do not recommend black-hat SEO techniques.
9. Do not recommend unnecessary content creation.
10. Avoid duplicate keyword targeting and keyword cannibalisation.
11. Prioritise business relevance and conversion opportunities.
12. Maintain consistency with the target website's actual business model.
13. Keep recommendations technically feasible for the existing website.
14. Do not implement any recommendation during this stage.

### Evidence classification

Use the following labels where appropriate:

- **VERIFIED:** Directly supported by available data or a reliable source.
- **OBSERVED:** Directly observed during website or competitor analysis.
- **ESTIMATED:** An estimate based on available evidence.
- **INFERRED:** A strategic conclusion based on findings.
- **UNAVAILABLE:** Required information could not be obtained.

---

## 12. FINAL REPORT STRUCTURE

Generate one comprehensive Markdown report with the following structure:

# SEO Strategy & Planning Report

## 1. Executive Summary

- Website overview
- Current SEO situation
- Major challenges
- Key opportunities
- Overall strategic direction

## 2. Previous Reports Validation

- SEO Audit Report
- Keyword Research Report
- Competitor Analysis Report
- Validation status
- Missing information and limitations

## 3. Consolidated SEO Findings

- Business findings
- Technical SEO findings
- Keyword research findings
- Competitor findings

## 4. SEO Goals and Objectives

- Business objectives
- SEO objectives
- Target audience
- Target markets
- Conversion objectives

## 5. Overall SEO Strategy

## 6. SEO Opportunity Analysis

- Quick wins
- Medium-term opportunities
- Long-term opportunities

## 7. Keyword Targeting Strategy

- Primary keywords
- Secondary keywords
- Long-tail keywords
- Search intent
- Keyword-to-URL mapping
- Cannibalisation risks

## 8. URL-wise On-Page SEO Roadmap

## 9. Content Strategy

- Content gaps
- New content opportunities
- Content clusters
- Content calendar

## 10. Technical SEO Strategy

## 11. Competitor-Driven SEO Strategy

## 12. Off-Page SEO Strategy

## 13. Local SEO Strategy

## 14. Schema and Structured Data Strategy

## 15. SEO Prioritisation Matrix

## 16. 30-Day SEO Roadmap

## 17. 60-Day SEO Roadmap

## 18. 90-Day SEO Roadmap

## 19. 180-Day SEO Roadmap

## 20. KPI and Measurement Strategy

## 21. Recommended SEO Tools

## 22. Team Responsibilities and Dependencies

## 23. Risks, Assumptions and Limitations

## 24. Final Recommendations

## 25. Next Workflow Stage

Clearly identify the next stage as:

**Stage 5 — Technical SEO Implementation**

Explain which technical SEO tasks should be executed first and which findings should be passed into the next stage.

---

## 13. OUTPUT DIRECTORY AND FILE NAMING

### Base output directory

Use the following base directory:

```text
C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs
```

This directory may be changed manually by the user when required.

### Folder naming convention

Use:

```text
{website-name}-{DD-MM-YYYY}
```

Example:

```text
strawhatdevs-18-11-2026
```

Generate the date once at execution time and reuse it throughout the folder and filename.

**IMPORTANT: Never include time, hours, minutes, seconds, or timestamps in folder names or filenames.**

### Stage-specific output folder

Create the following folder inside the existing website/date parent directory:

```text
seo-strategy-planning
```

Final directory structure:

```text
outputs/
└── {website-name}-{DD-MM-YYYY}/
    └── seo-strategy-planning/
        └── {website-name}-{DD-MM-YYYY}-seo-strategy-planning-reports.md
```

Example:

```text
C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs\strawhatdevs-18-11-2026\seo-strategy-planning\strawhatdevs-18-11-2026-seo-strategy-planning-reports.md
```

### File management rules

1. Check whether the website/date parent directory already exists.
2. If it exists, reuse it.
3. If it does not exist, create it.
4. Do not recreate, rename, or delete an existing parent directory.
5. Check whether the `seo-strategy-planning` folder already exists.
6. Reuse the existing folder if available.
7. Create it only if it does not exist.
8. Before saving, check whether the expected report file already exists.
9. Never overwrite an existing report without inspecting it and determining that an update is intended.
10. If an existing report must be preserved, use a clear non-conflicting filename without adding a timestamp.
11. Save the complete final report as Markdown.

### Output restrictions

Generate exactly one final report:

```text
{website-name}-{DD-MM-YYYY}-seo-strategy-planning-reports.md
```

Do not generate:

- JSON files
- CSV files
- Excel files
- PDF files
- Separate analysis reports
- Additional summary reports

The only final deliverable for this stage must be the consolidated Markdown report.

Verify that the report exists and contains the complete expected content before reporting that it has been saved.

If filesystem access is unavailable, clearly state that the file could not be saved. Never claim successful file creation without verification.

---

## 14. STRICT EXECUTION RULES

- Execute every section in the specified order.
- Reuse previous workflow reports automatically.
- Do not ask for website information already available in previous reports.
- Do not skip report validation.
- Do not fabricate unavailable information.
- Do not modify the website.
- Do not publish content.
- Do not make changes to Google Search Console or Google Analytics.
- Do not create backlinks.
- Do not execute technical SEO fixes.
- Do not generate multiple final reports.
- Save only the final consolidated Markdown report in the specified directory.
- Maintain the same website/date parent folder used by previous workflow stages.

## 15. FINAL EXECUTION INSTRUCTION

Begin by locating and validating the three previous SEO workflow reports.

Then consolidate their findings, develop the complete SEO strategy, prepare the prioritised roadmap, define KPIs, identify dependencies, and produce the final Markdown report.

Do not stop after providing recommendations in the conversation.

Complete the entire strategy and planning workflow, save the final report in the specified output directory, and verify the saved file.

At the end, provide:

1. Execution status
2. Previous report validation status
3. Number of strategic recommendations
4. Number of P1, P2, and P3 tasks
5. Roadmap coverage
6. Final report location
7. Next recommended stage: **Stage 5 — Technical SEO Implementation**

**Remember: This stage produces the SEO strategy and implementation roadmap only. Actual website changes must happen in the subsequent implementation stages.**
