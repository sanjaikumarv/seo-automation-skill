# Technical SEO Engineering Deep-Dive

Run: `strawhatdevs-2026-11-18` | Observed: 18 November 2026, IST

Target: https://www.strawhatdevs.com/en | Brand: Straw Hat Devs

## Architecture and evidence

Read the completed [baseline audit](seo-audit-report.md). Public responses identify `X-Powered-By: Next.js`, `Server: Vercel`, `Vary: RSC, Next-Router-State-Tree...`, App Router chunk paths and `self.__next_f.push` Flight payloads. **Next.js App Router is strongly supported by public evidence**. The exact Next.js version, repository layout, Tailwind dependency version and server runtime are unknown; inspect package.json before implementation. Server-rendered homepage and solution content is present in the initial response. CMS image URLs on blog pages reference Sanity CDN; no private CMS access was used.

Raw evidence: [crawl.json](evidence/crawl.json). Authentication for GSC/GA4 was not supplied. Public HTTP probes do not reproduce Google's render queue, index coverage categories or selected canonicals.

## Server configuration and security headers

| Item | Observed public response | Recommendation |
| --- | --- | --- |
| HTTPS / HSTS | HTTPS succeeds; `Strict-Transport-Security: max-age=63072000` | Keep existing HSTS. Do not add includeSubDomains/preload without checking all subdomains |
| HTTP/2 and HTTP/3 | Not negotiated/measured by this audit client | Verify with an HTTP/2/3-capable client; do not assume absent |
| HTML compression | `Content-Encoding: gzip` | Already compressed for this request; Brotli support under a different Accept-Encoding is untested |
| Home HTML caching | `private, no-cache, no-store, max-age=0, must-revalidate`; Age 0; Vercel MISS | Determine whether auth, cookies or locale detection make the page dynamic. Cache only anonymous stable content |
| Sitemap caching | `public, max-age=0, must-revalidate`; Vercel HIT; XML content type | Ensure sitemap regeneration follows actual content changes |
| Hero PNG caching | `public, max-age=0, must-revalidate`; content length 895,857 | Prefer responsive image optimization; immutable cache only content-hashed assets |
| CSP / X-Content-Type-Options / X-Frame-Options | Not present in sampled home response headers | Add nosniff and suitable referrer policy; assess frame-ancestors/CSP in report-only before enforcement |
| Secure cookies | Not meaningfully evaluated; no authenticated session | Inspect auth cookies separately; no claim of insecure cookies |

Do not set `Cache-Control: public, immutable` on personalized HTML, auth, API or all assets globally. Security headers are defense-in-depth recommendations; their absence is not evidence of a ranking penalty.

## Indexing, sitemap and routing diagnosis

The XML parser accepted the 34-entry sitemap at `/sitemap.xml`; this is a urlset, not a sitemap index. Its small size does not require splitting. Both `en` and `ta` entries are present. All checked preferred-host equivalents return 200, but the declared sitemap URLs use the redirecting apex host. All entries carry the same lastmod `2026-11-16T07:00:52.765Z`; this looks like build-level generation and is not proof each page changed then. Populate lastmod from actual content updates or omit it when unknown.

For distinct commercial/course/blog URLs, inherited root canonicals conflict with the page's content. Page-specific canonicals on solutions and insights still use the redirecting apex. Normalize to `https://www.strawhatdevs.com`, and preserve the locale and real path. Emit reciprocal hreflang only where a genuine localized equivalent exists; do not map a service page to a language homepage. Translated route existence alone does not prove its content is translated; verify language before pairing.

**Route defect reproduced:** `/sitemap_index.xml` is interpreted as a locale and serves home HTML with 200. Nested routes under this invalid locale also return content. Valid `/en/not-a-real-page` returns 404. Repair locale validation in `app/[lang]/layout.tsx` or the project's existing locale guard; the location is inferred. Exclude real XML/TXT/static endpoints from locale rewriting. Keep invalid locale/resource routes as 404; redirect only intentional unprefixed paths to their actual canonical equivalents.

## JavaScript rendering and DOM parity

Home and service H1/copy/links are visible without running JS, so this is not a blanket client-only site. `/en/courses`, `/en/blogs` and sampled course details have no H1 in initial HTML; inspect their client rendering and deliver a useful server heading. Full raw-versus-rendered DOM parity, hydration errors, long tasks and Googlebot rendering overhead were **not measured**. Do not convert every page to static rendering or remove necessary client interactions without inspecting components.

GTM container markup is present; this proves a container reference, not working GA4 conversion tracking. Browser console errors, consent behavior and tag duplication require a rendered browser test.

## Core Web Vitals remediation hypotheses

| Metric | Measured value | Observed candidate | Proposed change / acceptance |
| --- | --- | --- | --- |
| LCP | Unknown; PSI 429 on mobile/desktop | Home 1536x864 PNG is 895,857 bytes and preloaded | Convert/serve responsive optimized variants; measure actual LCP element before changing preload |
| INP | Unknown | Site delivers many App Router scripts and GTM | Profile interactions, move nonessential scripts later, split heavy interactive tools; validate against recorded long tasks |
| CLS | Unknown | Images already declare dimensions; embeds/forms may change layout | Preserve aspect ratios and reserve schedule/embed space; inspect filmstrip/field shifts |
| TTFB | Not measured | Dynamic no-store home response | Trace server data fetching and locale/session work; cache only proven public content and remeasure |

For a confirmed hero image, an App Router component can use:

```tsx
import Image from 'next/image';

export function EngineeringHero() {
  return <Image src="/coding-on-laptop.png"
    alt="Software engineering illustration" width={1536} height={864}
    sizes="(max-width: 768px) 100vw, 1200px"
    style={{ width: '100%', height: 'auto' }} />;
}
```

This preserves the existing asset and aspect ratio; it is a template for a verified placement, not a replacement screenshot design. Avoid manually preloading both an original PNG and an optimized srcset. With Next.js 16+, the Image API exposes `preload`; older versions use `priority`. Inspect the installed version and measured LCP before selecting one. Keep below-fold cards lazy. Do not add eager loading to every service image.

Add these headers to the existing configuration rather than replacing unrelated settings:

```ts
// Fragment inside the project's existing NextConfig (file path inferred).
async headers() {
  return [{
    source: '/:path*',
    headers: [
      { key: 'X-Content-Type-Options', value: 'nosniff' },
      { key: 'Referrer-Policy', value: 'strict-origin-when-cross-origin' },
    ],
  }];
}
```

CSP requires an inventory of GTM, Sanity, fonts, APIs and the existing scheduling embed; an untested locked-down policy could break them. Do not invent an allowlist or bypass nonce requirements to make a snippet appear complete.

## Implementation order and tests

1. **P1:** Fix canonicals, real locale equivalents and invalid-locale responses. Check original apex/HTTP roots, `/en`, `/ta`, consulting, a solution, an insight, a course and an invalid locale. Verify final HTTP status, a single canonical and reciprocal alternates.
2. **P1:** Update robots/sitemap to the preferred host and actual paths. Keep a full URL inventory; do not replace it with the commercial shortlist. Verify every XML location returns 200 without a redirect, is indexable and declares the same canonical.
3. **P2:** Diagnose dynamic rendering/caching using the actual repo. Preserve auth isolation. Check page output both signed in and signed out before any caching change.
4. **P2:** Optimize the image pipeline after mobile/desktop measurements are available. Run lab measurements with the same test setup before/after; obtain field data over time. No numerical improvement is promised.
5. **P2:** Add deliberate noindex for auth utilities; preserve crawl access so crawlers can see noindex. Do not use robots blocking as the only index-removal mechanism.
6. **P3:** Assess optional security headers and remove placeholder verification metadata.

Current framework implementation references: [Next metadata](https://nextjs.org/docs/app/api-reference/functions/generate-metadata), [sitemap API](https://nextjs.org/docs/app/api-reference/file-conventions/metadata/sitemap), [Image API](https://nextjs.org/docs/app/api-reference/components/image), [Proxy convention](https://nextjs.org/docs/app/api-reference/file-conventions/proxy). Google guidance: [canonical signals](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls), [localized equivalents](https://developers.google.com/search/docs/specialty/international/localized-versions). Consulted 18 November 2026. All code is proposed; no production changes were applied.
