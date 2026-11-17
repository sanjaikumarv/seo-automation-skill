# Master SEO Implementation Package: Actionable Updates for Website

- **Target Website:** https://strawhatdevs.com
- **Business Name:** Straw Hat Devs
- **Frontend Tech Stack:** Next.js (App Router) / React / Tailwind CSS *(or user-selected stack)*
- **Compiled From:** `seo-audit-report.md`, `technical-seo-report.md`, `keyword-research-report.md`, `on-page-seo-report.md`, `local-seo-report.md`, `off-page-seo-report.md`, `generated-content.md`, `seo-monitoring-report.md`
- **Execution Status:** READY TO DEPLOY

---

## 🚀 Production-Ready Developer Prompt (Copy & Paste to AI Coding Agent)

> **Copy and paste the prompt below into Antigravity, Cursor, Claude Code, GitHub Copilot, or ChatGPT to apply all SEO updates directly to your codebase:**

```markdown
You are a Senior Full-Stack Frontend Engineer and Technical SEO Implementation Specialist.

Your task is to implement all finalized SEO updates from this `outputs/seo-updates.md` file directly into this website's codebase with 100% accuracy and zero visual or functional regressions.

### Project Context & Tech Stack:
- Framework: Next.js (App Router / Pages Router) / React / Tailwind CSS (Detect exact project structure from repo).
- Target Website: https://strawhatdevs.com

---

### Implementation Instructions:

#### 1. Page Metadata & Head Configuration
For every page listed in Section 2:
- If Next.js App Router: Update the exported `metadata` object or `generateMetadata()` in `app/[route]/page.tsx` or `layout.tsx`:
  - `title`: Exact recommended title string.
  - `description`: Exact recommended meta description string.
  - `alternates.canonical`: Self-referencing canonical URL.
  - `openGraph` and `twitter`: Title, description, URL, and og-image.
- If Next.js Pages Router / React: Update `<Head>` with `<title>`, `<meta name="description">`, and `<link rel="canonical">`.
- If Static HTML / Astro / Nuxt: Update document `<head>` or framework SEO component (`useSeoMeta()`).

#### 2. Headings & Content Structure
For each page:
- Verify there is exactly ONE `<h1>` element matching the recommended H1 string.
- Update subheadings (`<h2>`, `<h3>`) to align with the recommended semantic hierarchy.
- Maintain all existing CSS / Tailwind classes, layout wrappers, and styling.

#### 3. Image Alt Attributes
- Locate image tags (`<img>` or framework `<Image>` components).
- Add the exact recommended `alt` text attribute into each asset.
- Ensure decorative images retain empty `alt=""`.

#### 4. Contextual Internal Links
- Locate the source pages specified in Section 4.
- Insert contextual hyperlinks using the exact specified anchor texts and relative destination paths (`/services/...`).

#### 5. Structured Data (JSON-LD Schema)
- Inject the provided JSON-LD code blocks from Section 3 using `<script type="application/ld+json">`.
- In Next.js, use `<script type="application/ld+json" dangerouslySetInnerHTML={{ __html: JSON.stringify(schema) }} />`.

#### 6. Server Directives & Robots.txt
- Create or update `public/robots.txt` matching Section 1.A.
- Configure HTTP-to-HTTPS and canonical 301 redirection rules in `next.config.js` or server config.

---

### Verification Checklist:
- [ ] Run `npm run build` or project build script to ensure zero compilation or TypeScript errors.
- [ ] Inspect pages in browser to confirm zero layout breakage.
- [ ] Output a clean git diff summary of all modified files.
```

---

## 1. Global Technical & Infrastructure Updates

### A. Robots.txt Configuration (`public/robots.txt`)
```txt
User-agent: *
Allow: /

# Sitemaps
Sitemap: https://strawhatdevs.com/sitemap.xml
```

### B. Canonical Tags & Redirect Rules
- **Canonical Rule:** Self-referencing canonical URL on every page.
- **Redirection (Next.js `next.config.js`):**
```js
// next.config.js
module.exports = {
  async redirects() {
    return [
      {
        source: '/:path*',
        has: [{ type: 'host', value: 'www.strawhatdevs.com' }],
        destination: 'https://strawhatdevs.com/:path*',
        permanent: true,
      },
    ];
  },
};
```

---

## 2. Page-by-Page Metadata & Headings Code Updates

### Page 1: Homepage (`/`)

#### Framework Implementation (Next.js App Router: `app/page.tsx` or `app/layout.tsx`):
```tsx
import type { Metadata } from 'next';

export const metadata: Metadata = {
  title: 'Custom Web & Mobile App Development Company | Straw Hat Devs',
  description: 'Straw Hat Devs engineers scalable custom software, web platforms, and mobile apps for startups and enterprises. Get your project roadmap and quote today.',
  alternates: {
    canonical: 'https://strawhatdevs.com',
  },
  openGraph: {
    title: 'Custom Web & Mobile App Development Company | Straw Hat Devs',
    description: 'Straw Hat Devs engineers scalable custom software, web platforms, and mobile apps.',
    url: 'https://strawhatdevs.com',
    siteName: 'Straw Hat Devs',
    type: 'website',
  },
};
```

#### Heading Updates in Component:
```tsx
// Replace Hero Heading
<h1>Scalable Custom Software, Web & Mobile App Development</h1>

// Recommended H2 Section Headings
<h2>Full-Stack Web Application Development</h2>
<h2>Mobile App Engineering (iOS & Android)</h2>
<h2>UI/UX Design & Cloud Infrastructure Solutions</h2>
<h2>Frequently Asked Questions</h2>
```

#### Image Alt Attributes:
```tsx
<Image 
  src="/hero-banner.webp" 
  alt="Straw Hat Devs custom software development team building web applications" 
  width={1200} 
  height={630} 
  priority 
/>
```

---

### Page 2: Services / Web Development (`/services/web-development`)

#### Framework Implementation:
```tsx
export const metadata: Metadata = {
  title: 'Custom Web Development Services & Solutions | Straw Hat Devs',
  description: 'Build high-performance, responsive web applications tailored to your business needs with Straw Hat Devs. Expert React, Next.js, and Node.js engineers.',
  alternates: {
    canonical: 'https://strawhatdevs.com/services/web-development',
  },
};
```

#### Heading Updates:
```tsx
<h1>Enterprise & Custom Web Development Services</h1>
<h2>Modern Frontend Engineering with React & Next.js</h2>
<h2>Secure Backend Architecture & Scalable APIs</h2>
<h2>E-Commerce & Custom Web Portal Development</h2>
```

---

## 3. Structured Data Markup (JSON-LD Code Blocks)

### A. Organization & WebSite Schema (`app/layout.tsx`)
```tsx
export default function RootLayout({ children }: { children: React.ReactNode }) {
  const jsonLd = {
    '@context': 'https://schema.org',
    '@type': 'Organization',
    name: 'Straw Hat Devs',
    url: 'https://strawhatdevs.com',
    logo: 'https://strawhatdevs.com/logo.png',
    sameAs: [
      'https://linkedin.com/company/strawhatdevs',
      'https://github.com/strawhatdevs',
    ],
    contactPoint: {
      '@type': 'ContactPoint',
      contactType: 'Customer Support',
      url: 'https://strawhatdevs.com/contact',
    },
  };

  return (
    <html lang="en">
      <head>
        <script
          type="application/ld+json"
          dangerouslySetInnerHTML={{ __html: JSON.stringify(jsonLd) }}
        />
      </head>
      <body>{children}</body>
    </html>
  );
}
```

### B. Service Schema (`app/services/web-development/page.tsx`)
```tsx
const serviceSchema = {
  '@context': 'https://schema.org',
  '@type': 'Service',
  serviceType: 'Web Development',
  provider: {
    '@type': 'Organization',
    name: 'Straw Hat Devs',
    url: 'https://strawhatdevs.com',
  },
  areaServed: 'Global',
  description: 'Custom enterprise web application development using modern frontend and backend technologies.',
};
```

### C. FAQPage Schema
```tsx
const faqSchema = {
  '@context': 'https://schema.org',
  '@type': 'FAQPage',
  mainEntity: [
    {
      '@type': 'Question',
      name: 'What technologies do Straw Hat Devs specialize in?',
      acceptedAnswer: {
        '@type': 'Answer',
        text: 'We specialize in modern full-stack web and mobile development including React, Next.js, Node.js, Python, Flutter, and cloud deployments.',
      },
    },
    {
      '@type': 'Question',
      name: 'How long does a custom software development project take?',
      acceptedAnswer: {
        '@type': 'Answer',
        text: 'Project timelines vary by scope; typical MVPs launch in 4-8 weeks, while comprehensive enterprise systems follow milestone-based agile sprints.',
      },
    },
  ],
};
```

---

## 4. Contextual Internal Links to Insert

| Source Page | Anchor Text to Hyperlink | Target Destination URL |
| :--- | :--- | :--- |
| Homepage (`/`) | `"custom web development services"` | `/services/web-development` |
| Homepage (`/`) | `"mobile application engineering"` | `/services/mobile-development` |
| Service Pages | `"request a project consultation"` | `/contact` |
| Blog Posts | `"explore our software engineering capabilities"` | `/services` |

---

## 5. Deployment Checklist for Developers
- [ ] 1. Copy the **Developer Prompt** from the top of this document into your coding agent or assign to developer.
- [ ] 2. Update `<title>` and `<meta name="description">` metadata across pages.
- [ ] 3. Update single `<h1>` tag and structure `<h2>` headings.
- [ ] 4. Add `alt` attributes to images.
- [ ] 5. Inject JSON-LD schema blocks into layout or `<head>`.
- [ ] 6. Deploy `public/robots.txt` and verify `/sitemap.xml`.
- [ ] 7. Run `npm run build` or project build script to verify zero compilation errors.
