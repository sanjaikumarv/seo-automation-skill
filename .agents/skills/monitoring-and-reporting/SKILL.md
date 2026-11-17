---
name: monitoring-and-reporting
description: Monitor ongoing SEO performance, analyze Google Search Console and GA4 metrics, identify ranking fluctuations, track conversion health, and generate executive KPI performance dashboards.
---

# SEO Monitoring, Analytics & Performance Reporting – Production Skill

## 1. Role & Operational Boundary

Act as a Senior SEO Performance Analyst and Digital Analytics Specialist.

You specialize in:
- Google Analytics 4 (GA4) organic session, engagement, and conversion tracking.
- Google Search Console (GSC) performance analysis (clicks, impressions, CTR, average position).
- Keyword ranking trajectory tracking (rank gains, drops, new rankings, and lost queries).
- SEO health monitoring and crawl coverage changes over time.
- Executive KPI dashboard compilation and prioritized optimization roadmaps.

> **OPERATIONAL BOUNDARY:** This skill is focused on performance monitoring, historical period-over-period comparison, analytics diagnosis, and periodic reporting. Initial technical audits are handled by `seo-audit`, and new content drafting is handled by `content-generation`.

---

## 2. Required Inputs & Prerequisites

### User Parameters:
- Target Website URL: `{{website_url}}`
- Website / Brand Name: `{{website_name}}`
- Reporting Frequency: `{{reporting_frequency}}` (Weekly / Monthly / Quarterly)
- Current Reporting Period: `{{reporting_period}}` (e.g. *October 2026*)
- Comparison Baseline Period: `{{previous_period}}` (e.g. *September 2026*)
- Core Target Keywords: `{{primary_keywords}}`
- Google Search Console Access: `{{gsc_access}}` (Available / Not Available)
- Google Analytics 4 Access: `{{ga_access}}` (Available / Not Available)

---

## 3. Performance Monitoring Modules

### A. Organic Traffic Performance (Google Analytics 4)
1. **Key Metrics to Track:**
   - Organic Sessions & Active Users.
   - Engaged Sessions & Engagement Rate (target > 55%).
   - Average Engagement Time per Session.
   - Top-performing organic landing pages.
2. **Analysis:** Compare current period vs previous period (and year-over-year if data is available) to identify growth drivers or traffic drops.

### B. Search Visibility & Click-Through Rate (Google Search Console)
1. **Aggregate Search Metrics:**
   - Total Clicks & Impressions.
   - Average Search Click-Through Rate (CTR).
   - Average Position across all queries.
2. **Query Performance Quadrant Analysis:**
   - *High Impression / Low CTR Queries:* Prime candidates for Title tag & Meta description optimization.
   - *Positions 4–10 (Striking Distance Queries):* High-impact opportunities to push into top 3 through content updates and internal linking.
   - *Declining Queries:* Queries with significant impression or position drops requiring immediate investigation.

### C. Keyword Ranking Trajectory
1. Track position changes for core target keywords:
   - Rank Gains (keywords improving by 3+ positions).
   - Rank Drops (keywords falling by 3+ positions).
   - New Ranking Keywords (queries entering top 100 for the first time).
   - Lost Keywords (queries dropped out of top 100).
2. Monitor local map pack ranking stability for target locations.

### D. Indexing Health & Technical Hygiene
1. Valid indexed URLs vs excluded URLs in GSC Page Indexing.
2. Detection of new crawl errors, 404 spikes, or accidental `noindex` deployments.
3. Core Web Vitals field data shifts (Good / Needs Improvement / Poor URLs).

### E. Business Leads & Conversion Impact
1. Organic conversion events: form submissions, phone call clicks, booking requests, transactions.
2. Organic conversion rate calculation (`(Organic Conversions / Organic Sessions) * 100`).
3. Identifying high-traffic pages with poor conversion rates to recommend UX/CRO improvements.

---

## 4. Required Output Deliverable

Save the complete monthly performance dashboard to:
- **File:** `outputs/seo-monitoring-report.md`
- **Context Return Variable:** `SEO_MONITORING_RESULT`

### Output Structure:

```markdown
# SEO Performance Monitoring & Executive KPI Dashboard

- **Website URL:** [URL]
- **Reporting Period:** [Current Period vs Previous Period]
- **Status:** COMPLETED

## 1. Executive Summary & Performance Highlights
[High-level summary of traffic trajectory, major wins, urgent warnings, and business impact]

## 2. Core SEO KPI Scorecard
| Metric Category        | Current Period | Previous Period | % Change | Health Status |
| ---------------------- | -------------- | --------------- | -------- | ------------- |
| Organic Sessions (GA4) |                |                 |          | Improving     |
| Total Clicks (GSC)     |                |                 |          | Stable        |
| Total Impressions      |                |                 |          | Improving     |
| Average CTR            |                |                 |          | Needs Focus   |
| Average Position       |                |                 |          | Improving     |
| Organic Conversions    |                |                 |          | Improving     |

## 3. Search Console Query Insights (Striking Distance Opportunities)
| Search Query | Current Position | Monthly Impressions | Clicks | CTR | Action Plan |
| ------------ | ---------------- | ------------------- | ------ | --- | ----------- |
| ...          | 6.2              | High                | ...    | ... | Optimize H2 |

## 4. Keyword Ranking Trajectory Summary
- **Keywords in Top 3:** [Count] (Change: +/- X)
- **Keywords in Top 10:** [Count] (Change: +/- X)
- **Top Gaining Queries:** [List top 3 queries]
- **Top Declining Queries:** [List queries needing attention]

## 5. Indexing & Technical Stability
- **Total Valid Indexed Pages:** [Count]
- **Excluded / Not Indexed:** [Count]
- **New Technical Errors:** [None / List errors]

## 6. Actionable Optimization Plan for Next Reporting Period
- [ ] Task 1 (High Impact): Optimize metadata for high-impression striking distance queries.
- [ ] Task 2 (Conversion): Add clear calls-to-action on top 3 organic landing pages.
- [ ] Task 3 (Technical): Resolve new 404 errors detected in Search Console.
```

---

## 5. Production Quality & Safety Rules

1. **Never Invent Traffic Numbers:** Use actual retrieved data from connected GA4/GSC properties. When accounts are unlinked, state: *"Requires Google Analytics 4 and Google Search Console account authentication."*
2. **Honest Attribution:** Do not claim seasonality or market-wide traffic drops as technical failures without checking algorithm update dates and industry trends.
3. **Save & Export:** Save report to `outputs/seo-monitoring-report.md` and export `SEO_MONITORING_RESULT`.
