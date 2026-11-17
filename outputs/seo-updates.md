# Master SEO Updates Package — Next.js App Router

Run: `strawhatdevs-2026-11-18` | Observed: 18 November 2026, IST

Target: https://www.strawhatdevs.com/en | Brand: Straw Hat Devs

## Production-Ready Developer Apply Prompt

```text
Work in the actual Straw Hat Devs Next.js website repository. Read this SEO package and the eight linked reports before editing. The live site strongly indicates Next.js App Router on Vercel, but the exact version, source paths, dependencies and existing locale/auth/CMS implementation must be inspected in the repository first. The paths below are inferred integration targets, not files inspected in this career-operations workspace.

Implement the verified P1 canonical, hreflang and locale-routing fixes first, preserving design, current functionality, auth boundaries, analytics ownership, CMS integration and existing educational content. Use https://www.strawhatdevs.com as the canonical origin. Give each indexable URL its own actual locale/path canonical; do not let root metadata collapse course/blog/service pages onto the homepage. Pair locale alternates only for genuinely equivalent translated pages. Reject invalid locale/resource routes with real 404 responses. Keep valid nonlocalized assets, APIs, robots and sitemap outside locale rewriting. Reduce avoidable root slash redirects without removing useful language behavior.

Apply the approved per-page metadata below to existing English commercial pages, avoiding title-template duplication and inherited generic OG/Twitter values. Do not apply English copy to Tamil routes. Add the reviewed consulting content, contextual links and factual Organization/Service/BreadcrumbList data. FAQ markup is optional semantic markup only: Google retired FAQ rich results in May 2026. Do not add invented business addresses, coordinates, ratings, clients, certifications, dates, prices or performance metrics.

Preserve all 34 existing sitemap paths while correcting their host, and reconcile with the full indexable CMS/routes inventory. Add valid missing pages only after inspection and canonical fixes. Do not replace the sitemap with the eight-page business shortlist. Do not add six proposed service routes until implemented with useful reviewed content. Keep auth pages deliberately noindex and out of the sitemap, without blocking crawlers from reading noindex.

Use the confirmed form success path for any future analytics event and the existing consent/GTM setup; do not send personal/project data or double-count leads. Account configuration, Google Business Profile edits, outreach, deployment and external submission are separate actions and are not requested by this handoff prompt.

Run the repository's existing applicable checks/build, route/metadata assertions, JSON-LD parsing and responsive checks. Test both a valid page and negative/error cases. Explain any version-dependent adaptation. Return changed files, evidence of checks, remaining unknowns and a reviewable diff. Stop before deployment. If an evidence claim conflicts with actual source or current production, report and resolve the discrepancy instead of blindly pasting snippets.
```

## Scope and priority decisions

This is a proposed local developer handoff. No website files, external accounts, listings, messages, analytics settings or deployment were changed in this run.

| Priority | Verified finding / business need | Action and affected URLs |
| --- | --- | --- |
| P1 | 20 of 29 English 200 samples declare the root apex canonical | Correct canonical path/host for all indexable routes, including courses and blogs beyond this page shortlist |
| P1 | Solutions/insights have apex path canonicals; sitemap uses apex | Align preferred www host in metadata, robots and every sitemap URL |
| P1 | `/sitemap_index.xml` and nested fake-locale paths return content with 200 | Validate locale values; use true 404 for these routes |
| P1 | Contact/about/work inherit education metadata | Give existing commercial pages distinct intent and snippets |
| P1/P2 | Broad software, local web and e-commerce buying intents need distinct content | Improve home/consulting; launch proposed web/e-commerce pages only after review |
| P2 | Home image is 895,857 bytes; performance unmeasured | Inspect LCP and optimize responsive image delivery before changing loading priority |
| P2 | Contact success tracking not verified | Inspect existing GTM/form success/consent; implement validated lead semantics if authorized |
| P2 | No verified GBP/office details; older profile website | Owner identity review; conditional profile/schema work, separate from code-ready fixes |

Next.js App Router detection is supported by RSC/Flight payloads, app chunks and public headers. Exact version and repo layout remain unknown. Date of public baseline: 18 November 2026 IST. No numeric performance or ranking improvement is promised.

## 1. Shared canonical origin and per-page metadata

Inferred locations: `src/lib/seo.ts` (or equivalent existing utility) and server page metadata exports. Merge with the existing metadata system, never add duplicate hardcoded head tags. Use a root metadataBase with the www origin; **remove inherited root-only canonical/language defaults from shared layouts** and set those per page. Preserve actual ownership verification and brand assets.

```ts
// Proposed helper in src/lib/seo.ts; reconcile with actual project imports.
import type { Metadata } from 'next';

export const SITE_ORIGIN = 'https://www.strawhatdevs.com';

type SeoInput = {
  path: string;
  title: string;
  description: string;
  languagePaths?: Record<string, string>;
};

export function buildPageMetadata(input: SeoInput): Metadata {
  // Internal paths only. Reject protocol-relative values and malformed origins.
  if (!input.path.startsWith('/') || input.path.startsWith('//')) {
    throw new Error('Expected an internal canonical path');
  }
  const canonical = new URL(input.path, SITE_ORIGIN).href;
  const languages: Record<string, string> = {};
  for (const [language, path] of Object.entries(input.languagePaths ?? {})) {
    if (!path.startsWith('/') || path.startsWith('//')) {
      throw new Error('Expected an internal localized path');
    }
    languages[language] = new URL(path, SITE_ORIGIN).href;
  }
  return {
    metadataBase: new URL(SITE_ORIGIN),
    title: { absolute: input.title }, // Avoid a parent's title-template suffix.
    description: input.description,
    alternates: {
      canonical,
      languages, // Only explicitly supplied, verified page equivalents.
    },
    openGraph: {
      type: 'website',
      siteName: 'Straw Hat Devs',
      url: canonical,
      title: input.title,
      description: input.description,
      images: [{
        url: `${SITE_ORIGIN}/brand/social-banner.png`,
        width: 1200,
        height: 630,
        alt: 'Straw Hat Devs',
      }],
    },
    twitter: {
      card: 'summary_large_image',
      title: input.title,
      description: input.description,
      images: [`${SITE_ORIGIN}/brand/social-banner.png`],
    },
  };
}
```

The existing social-banner resource returned 200 during this run; declared OG dimensions are retained from current metadata, not independently image-decoded. Keep page-specific blog article types and images in the actual article implementation; the helper above is for business pages, not a global forced replacement for article metadata.

Approved draft values for the eight **existing** English pages:

```json
{
  "/en": {
    "title": "Software Development Company in India | Straw Hat Devs",
    "description": "Build custom software, web and mobile apps, SaaS platforms and AI workflows with Straw Hat Devs. Discuss your startup or SME project in India or globally."
  },
  "/en/consulting": {
    "title": "Software Consulting for Startups & SMEs | Straw Hat Devs",
    "description": "Plan custom software, review architecture and improve business workflows with Straw Hat Devs. Explore practical software consulting for startups and SMEs."
  },
  "/en/solutions/manufacturing-software": {
    "title": "Manufacturing Software Development | Straw Hat Devs",
    "description": "Connect production stages, order tracking and operational handoffs with custom manufacturing software. Discuss a practical starting point with Straw Hat Devs."
  },
  "/en/solutions/dealer-order-management": {
    "title": "Custom Dealer Order Management Software | Straw Hat Devs",
    "description": "Bring catalogs, dealer orders, approvals and status updates into one workflow. Explore custom dealer order management software and discuss your needs."
  },
  "/en/solutions/workflow-automation": {
    "title": "Workflow Automation for Businesses | Straw Hat Devs",
    "description": "Reduce repetitive handoffs with workflow automation for your business. Connect systems, define review steps and scope a practical first release."
  },
  "/en/contact": {
    "title": "Contact Straw Hat Devs | Discuss Your Software Project",
    "description": "Tell Straw Hat Devs about your software, website, app or automation project. Share your goals and discuss a practical next step for your business workflow."
  },
  "/en/about": {
    "title": "About Straw Hat Devs | Software for Startups and SMEs",
    "description": "Meet the approach behind Straw Hat Devs: practical engineering, clear project scope and maintainable software for startups, SMEs and growing business teams."
  },
  "/en/work": {
    "title": "Software Solutions for Business Workflows | Straw Hat Devs",
    "description": "Explore software solutions for manufacturing, dealer orders and connected business workflows. Discuss a scoped first release tailored to your operations."
  }
}
```

Example integration for the actual `/en/consulting` route (the project's dynamic locale architecture may require a localized generateMetadata function rather than this literal English example):

```ts
import { buildPageMetadata } from '@/lib/seo';

export const metadata = buildPageMetadata({
  path: '/en/consulting',
  title: 'Software Consulting for Startups & SMEs | Straw Hat Devs',
  description: 'Plan custom software, review architecture and improve business workflows with Straw Hat Devs. Explore practical software consulting for startups and SMEs.',
  // Add ta: '/ta/consulting' only after verifying true translated equivalence,
  // and ensure the Tamil page returns reciprocal links to this exact page.
  languagePaths: { en: '/en/consulting' },
});
```

In a shared `[lang]` route, select the localized title/copy and route pair from the project's actual translation inventory. Do not hardcode `/en/consulting` for all locale values. Use `en` for the intended global English version; an `en-IN` region variant should represent an actual regional version, not just be appended for keywords. An optional x-default must point to the intentional fallback, not a nonexistent selector page.

## 2. Locale validation, root redirects and utility noindex

Inferred integration: existing `app/[lang]/layout.tsx`, `src/app/[lang]/layout.tsx`, or equivalent locale guard. Add the guard before rendering existing content; keep all existing providers, styling, auth and layout markup.

```ts
// Helper; import from a shared locale module if the project already has one.
export function isSupportedLocale(value: string): value is 'en' | 'ta' {
  return value === 'en' || value === 'ta';
}
```

```tsx
// Fragment inside the existing localized layout implementation.
// Modern App Router params are asynchronous; adapt types to installed Next version.
import { notFound } from 'next/navigation';

// Within the existing async layout, before returning its existing JSX:
const { lang } = await params;
if (!isSupportedLocale(lang)) notFound();
```

The layout fragment is intentionally not a full replacement file. Inspect the site's actual middleware/proxy behavior: static resources, `/api`, `/_next`, `/robots.txt`, `/sitemap.xml` and filenames with extensions must not be interpreted as locales. Do not redirect unknown filenames to home. `/sitemap_index.xml` is not an existing valid XML index and should be 404 unless a real index is deliberately implemented. A path segment such as `sitemap_index.xml` must never be accepted as `[lang]`.

Root normalization: apex to www already works; remove the `/en/` to `/en` extra hop by using the actual no-trailing-slash destination in the existing language redirect. Keep temporary redirects where language negotiation is temporary; do not force a global permanent English redirect without understanding current language behavior. For Next.js 16+, the convention is proxy; older versions may use middleware. Do not create two competing handlers or rename the current file blindly.

For the existing localized auth subtree, add deliberate robots metadata in its server layout/page, merging with the project architecture:

```ts
import type { Metadata } from 'next';
export const metadata: Metadata = {
  robots: {
    index: false,
    follow: true,
    googleBot: { index: false, follow: true },
  },
};
```

Do not use a homepage canonical to “remove” login pages. Keep these routes out of the sitemap and accessible to crawlers for noindex discovery. Private data still requires actual authentication.

## 3. Robots and complete sitemap host correction

Inferred location: `app/robots.ts` or `src/app/robots.ts`, preserving existing intended restrictions:

```ts
import type { MetadataRoute } from 'next';

export default function robots(): MetadataRoute.Robots {
  return {
    rules: [{ userAgent: '*', allow: '/', disallow: ['/private/', '/admin/'] }],
    sitemap: 'https://www.strawhatdevs.com/sitemap.xml',
  };
}
```

Review whether private/admin paths are locale-prefixed in source; their actual routes were not inspected. Do not block auth pages merely to hide them from the index, and do not remove intentional pre-existing bot rules. XML host correction should preserve the full dynamic route/content inventory.

The following minimal sitemap example preserves **all 34 current sitemap paths**. It is a baseline, not a replacement for a richer CMS sitemap implementation. Reconcile dynamic course/blog articles and other public indexable pages missing from the current sitemap. Do not include auth, VR utilities or proposed service routes by default. Keep lastModified absent when actual substantive content dates are unknown; do not insert today's date for every page on each build.

```ts
import type { MetadataRoute } from 'next';

const origin = 'https://www.strawhatdevs.com';
const existingSitemapPaths = [
  "/en/insights",
  "/en/insights/manufacturing-order-workflow",
  "/en/insights/healthcare-front-desk-workflows",
  "/en/insights/retail-mart-inventory-visibility",
  "/en/insights/shopping-mall-iot-pilot",
  "/en/insights/saas-first-useful-release",
  "/en",
  "/en/blogs",
  "/en/courses",
  "/en/tools",
  "/en/consulting",
  "/en/solutions/manufacturing-software",
  "/en/solutions/dealer-order-management",
  "/en/solutions/workflow-automation",
  "/en/about",
  "/en/work",
  "/en/contact",
  "/ta/insights",
  "/ta/insights/manufacturing-order-workflow",
  "/ta/insights/healthcare-front-desk-workflows",
  "/ta/insights/retail-mart-inventory-visibility",
  "/ta/insights/shopping-mall-iot-pilot",
  "/ta/insights/saas-first-useful-release",
  "/ta",
  "/ta/blogs",
  "/ta/courses",
  "/ta/tools",
  "/ta/consulting",
  "/ta/solutions/manufacturing-software",
  "/ta/solutions/dealer-order-management",
  "/ta/solutions/workflow-automation",
  "/ta/about",
  "/ta/work",
  "/ta/contact"
] as const;

export default function sitemap(): MetadataRoute.Sitemap {
  return existingSitemapPaths.map(path => ({ url: `${origin}${path}` }));
}
```

Do not rewrite English entries as Tamil entries or publish missing language translations just to fill this list. Validate live content/language and canonical consistency. Existing valid course/blog detail pages discovered outside this 34-entry list can be added after inspecting their indexability and fixing their canonicals. If the CMS already provides real updatedAt values, retain those dates.

## 4. Visible content, H1s and internal linking

Read and apply the reviewed [consulting page draft](generated-content.md) with the exact H1 and five H2s from [Step 4](on-page-seo-report.md). Preserve the existing consultation CTA and inquiry integration. Use `next/link` for internal paths in the actual source. Do not change the landing page into a client portfolio or imply measured delivery outcomes.

Existing English H1 specifications:

| Page | Proposed H1 |
| --- | --- |
| /en | A software development company for startups and SMEs |
| /en/consulting | Software consulting services for startups and SMEs |
| /en/solutions/manufacturing-software | Manufacturing software development for clearer operations |
| /en/solutions/dealer-order-management | Dealer order management software built around your workflow |
| /en/solutions/workflow-automation | Workflow automation services for connected business systems |
| /en/contact | Contact Straw Hat Devs about your software project |
| /en/about | The software team behind Straw Hat Devs |
| /en/work | Software solutions for real business workflows |

Contextual links to existing destinations: home → consulting; consulting → manufacturing/dealer/workflow solutions; each solution → contact; manufacturing insight → manufacturing solution; SaaS insight → consulting; business pages → about for approach. Keep the learning CTA clearly separate. Step 4 contains the full anchor/context table.

All page-specific H2/H3 blueprints and current metadata comparisons are in Step 4. Existing image alt descriptions should be preserved until visually reviewed; do not add Coimbatore to every image. Keep empty alt for genuinely decorative delivery images. Correct missing raw-HTML learning headings in their own components after checking rendered behavior; do not blanket-inject duplicate H1s.

## 5. Factual consulting schema and safe rendering

Proposed data for `/en/consulting`, from Steps 4 and 7. This core graph deliberately excludes the unverified LocalBusiness draft and optional FAQ node. If the root layout already emits Organization, reuse its stable identity rather than duplicating competing facts.

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://www.strawhatdevs.com/#organization",
      "name": "Straw Hat Devs",
      "url": "https://www.strawhatdevs.com/en"
    },
    {
      "@type": "Service",
      "@id": "https://www.strawhatdevs.com/en/consulting#service",
      "name": "Software consulting services",
      "serviceType": "Software consulting and custom software development",
      "url": "https://www.strawhatdevs.com/en/consulting",
      "provider": {
        "@id": "https://www.strawhatdevs.com/#organization"
      },
      "areaServed": [
        {
          "@type": "Country",
          "name": "India"
        },
        "Worldwide"
      ]
    },
    {
      "@type": "BreadcrumbList",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://www.strawhatdevs.com/en"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Software consulting",
          "item": "https://www.strawhatdevs.com/en/consulting"
        }
      ]
    }
  ]
}
```

Render a reviewed graph from a Server Component (inferred location `components/JsonLd.tsx`):

```tsx
export function JsonLd({ data }: { data: Record<string, unknown> }) {
  return <script type="application/ld+json" dangerouslySetInnerHTML={{
    __html: JSON.stringify(data).replace(/</g, '\u003c'),
  }} />;
}
```

Source the data from trusted reviewed content and keep the visible page consistent. Full optional consulting FAQPage markup appears in generated-content.md and matches its visible Q&A exactly. Google no longer shows FAQ rich results, so omit FAQ markup if its only purpose would have been that feature. Keep useful visible FAQs. JSON parsing does not prove schema/search eligibility.

For manufacturing, dealer and workflow pages, build a Service node with the actual route, unique `#service` ID, mapped service name and the same provider ID. Do not copy consulting's URL/name across all solution pages. Add breadcrumbs matching real navigation. Do not attach ratings, prices or address to satisfy a schema template.

## 6. Performance and infrastructure proposals

- The existing hero PNG is 895,857 bytes. Confirm whether it is the LCP element, then use the responsive next/image approach in Step 2 or generate appropriately sized modern variants. Preserve actual image aspect ratio and avoid preloading both original and optimized forms.
- Inspect the installed Next version before using `preload` (modern API) versus `priority` (older API). Preload only the image that matters in the actual viewport; keep lower cards lazy.
- Audit the home page's private/no-store rendering causes before caching. Never set public immutable cache headers on personalized HTML or auth pages. Keep hashed static assets and dynamic pages separate.
- Profile heavy interactions, VR/tools and third-party code before altering script loading. Do not remove the existing GTM container or schedule embed just to improve an unmeasured score.
- Add nosniff/referrer policy by merging the exact header fragment in Step 2. Keep current HSTS. Do not enforce a speculative CSP allowlist or HSTS includeSubDomains/preload without reviewing dependencies.

Performance lab/field scores remain unknown because both PageSpeed requests returned 429. Mobile overflow, touch target checks, console errors and DOM parity remain browser validation work. Do not advertise an untested score or guaranteed metric reduction.

## 7. Lead measurement integration

The Step 8 success-branch dataLayer snippet is the proposed integration point; it fires `generate_lead` after backend confirmation and includes only `form_id: project_inquiry` and the path. Reuse the existing consent/GTM flow, reconcile any existing lead event, and avoid duplicate pushes on re-render/double click. Do not send field contents, email, phone, name or free-text project details into ordinary analytics events.

The actual handler/API source was not inspected, so no claim is made that a named `onSuccess` function or endpoint exists. Add the event at the real confirmed-success branch. A CTA click, failed submission or scheduling page view is not a confirmed lead. GA4 account key-event settings are a separate owner-approved action.

## 8. Proposed service-page launch backlog

These six routes are **not discovered live pages**. Title/description/H1 are drafted below; full heading blueprints are in Step 4, and web/e-commerce body drafts are in Step 7. Only add links, sitemap entries and schema after approved implementation with useful page-specific content.

| Proposed route | Primary intent | Title | Description | H1 |
| --- | --- | --- | --- | --- |
| /en/services/web-development | web development services | Web Development Services in Coimbatore \| Straw Hat Devs | Plan a business website or web application with Straw Hat Devs. Explore web development services for Coimbatore businesses, Indian startups and global SMEs. | Web development services for Coimbatore businesses and beyond |
| /en/services/ecommerce-development | e-commerce website development in Coimbatore | E-commerce Development in Coimbatore \| Straw Hat Devs | Build an e-commerce website around your catalog, checkout and order workflows. Discuss custom store development for Coimbatore businesses with Straw Hat Devs. | E-commerce website development for Coimbatore businesses |
| /en/services/saas-development | SaaS development services | SaaS & Multi-Tenant App Development \| Straw Hat Devs | Scope a SaaS release with tenant-aware access, onboarding and business workflows. Discuss SaaS and multi-tenant application development with Straw Hat Devs. | SaaS development services for a useful first release |
| /en/services/mobile-app-development | mobile app development services | Mobile App Development for Startups \| Straw Hat Devs | Plan mobile applications around your customers and business workflows. Discuss app requirements, integrations and a scoped first release with Straw Hat Devs. | Mobile app development services for startups and SMEs |
| /en/services/ai-applications | AI application development services | AI Application Development Services \| Straw Hat Devs | Turn a business use case into an AI application with clear evaluation and human review. Discuss AI integration and application development with Straw Hat Devs. | AI application development services for practical use cases |
| /en/services/seo-optimization | SEO optimization services in Coimbatore | SEO Optimization Services in Coimbatore \| Straw Hat Devs | Improve technical foundations, page intent and local search signals with SEO optimization. Discuss an evidence-based plan for your website with Straw Hat Devs. | SEO optimization services for Coimbatore businesses |

SaaS copy should cover multi-tenancy, roles, onboarding and operating needs; AI application copy should distinguish evaluated features from workflow automation; mobile copy should explain app requirements. Avoid inventing platform partnerships. SEO delivery and business-development services require clear scope; do not promise rankings, leads or sales results. Do not create one location page per spelling or synonym.

## 9. Owner-dependent and unsupported changes — excluded from apply-ready code

- No verified physical address, current public phone, Google Business Profile ownership, categories or review data. Do not deploy LocalBusiness address/geo/ratings; Step 5's partial draft is explicitly on hold. Keep Organization/Service data instead.
- The company LinkedIn page uses the earlier website and the terms page still shows legacy support email. Owner must confirm the desired website/contact update; no profile/account changes performed.
- No authenticated GSC/GA4 history or backlink exports. Step 8 contains an empty-real-data KPI template; Step 6 contains research concepts and unsent outreach, not acquired links or completed campaigns.
- No original client outcome metrics or proof of finished case studies. Keep concepts/examples distinct from delivered client work.
- No source repository inspected, dependency lockfile available, framework build run, deployment performed, or formal legal review attempted.

## 10. Acceptance checks before review/deployment

| Check | Expected result | Negative case |
| --- | --- | --- |
| Canonical | One absolute www canonical preserving actual locale and path | Consulting/course/blog must never point to root |
| Hreflang | Real translated equivalents, reciprocal and 200 | No service-to-language-homepage pair; omit unavailable translation |
| Routes | `/en` and valid service/learning paths render | Invalid-locale resource such as `/sitemap_index.xml` returns 404; `/en/not-a-real-page` stays 404 |
| Sitemap | All intended existing paths retained, current canonical host and indexability | No auth, redirecting paths or draft routes |
| Metadata | Titles/descriptions match the saved plan after rendering | No doubled title suffix or inherited generic social metadata |
| Content | Approved H1/H2 and valid internal destinations | No unlaunched service links or invented case studies |
| JSON-LD | Parses, consistent IDs and visible facts | No raw injected `<script>` content, unknown address/coordinates/ratings |
| Lead event | One event for successful accepted inquiry in authorized staging test | Zero lead events for validation failure, server failure and consent-denied blocked tracking |
| Responsive UI | Useful content and controls at 360/390/768 widths | No clipped CTA, overflow or unusable nav/form |
| Auth / cache | No personalized data exposed across sessions | No global public immutable HTML caching |

Run the actual repo's existing lint/typecheck/tests/build commands, adapting to its package manager. Do not invent `npm` scripts or mark a build successful from a report-only workspace. Compare page-source and browser output, record before/after checks and use external structured-data validation for relevant types. After authorized deployment, check GSC-selected canonicals and sitemap processing over time; inspection/requesting indexing is not performed by this report.

## Deliverables and current validation

- [1. seo-audit-report.md](seo-audit-report.md)
- [2. technical-seo-report.md](technical-seo-report.md)
- [3. keyword-research-report.md](keyword-research-report.md)
- [4. on-page-seo-report.md](on-page-seo-report.md)
- [5. local-seo-report.md](local-seo-report.md)
- [6. off-page-seo-report.md](off-page-seo-report.md)
- [7. generated-content.md](generated-content.md)
- [8. seo-monitoring-report.md](seo-monitoring-report.md)
- [9. seo-updates.md](seo-updates.md)


This package was produced after all eight prior reports were saved and read in sequence. The audit includes the discovered page catalog, the keyword report maps existing/proposed pages, Step 4 specifies 14 metadata pairs with exact counts, and Step 7 matches the consulting H1/H2 and FAQ/schema data. JSON blocks are parsed locally. No website build or actual deployment was tested.

Primary technical references consulted 18 November 2026: [Next metadata](https://nextjs.org/docs/app/api-reference/functions/generate-metadata), [Next sitemap](https://nextjs.org/docs/app/api-reference/file-conventions/metadata/sitemap), [Next Image](https://nextjs.org/docs/app/api-reference/components/image), [Proxy convention](https://nextjs.org/docs/app/api-reference/file-conventions/proxy), [Google canonical guidance](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls), [localized URLs](https://developers.google.com/search/docs/specialty/international/localized-versions), [Search updates including FAQ retirement](https://developers.google.com/search/updates), and [GA4 lead events](https://developers.google.com/analytics/devguides/collection/ga4/reference/events#generate_lead). Business evidence is linked in the audit and retained in [crawl.json](evidence/crawl.json).
