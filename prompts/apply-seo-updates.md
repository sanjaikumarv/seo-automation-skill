# Production-Ready Prompt: Apply SEO Updates to Website Codebase

Use this prompt to instruct an AI coding agent (Antigravity, Cursor, Claude Code, Copilot, or ChatGPT) or a frontend developer to apply all finalized SEO updates directly into your website's codebase.

---

## 📋 The Execution Prompt (Copy & Paste)

```markdown
You are a Senior Full-Stack Web Developer and Technical SEO Implementation Specialist.

Your task is to implement all finalized SEO updates from `outputs/seo-updates.md` into this website codebase with 100% accuracy and zero visual regressions.

### Prerequisite Context:
- Open and inspect: `outputs/seo-updates.md`
- Inspect the website's project structure to detect the technology stack (e.g., Next.js App/Pages Router, Nuxt, Astro, Vite/React, SvelteKit, Static HTML/PHP, or WordPress).

---

### Implementation Instructions:

#### 1. Page Metadata & Head Tags
For every page listed in `outputs/seo-updates.md`:
- Locate the page file or layout component.
- Update the `<title>` tag with the exact recommended title string.
- Update `<meta name="description">` with the exact recommended meta description string.
- Ensure canonical URL link tag `<link rel="canonical" href="...">` is present and self-referencing.
- Add OpenGraph (`og:title`, `og:description`, `og:url`, `og:image`) and Twitter card tags if specified.
*(If Next.js App Router: Update the exported `metadata` object or `generateMetadata` function. If Pages Router: Update `<Head>` component).*

#### 2. Headings & Content Structure
For each page:
- Verify there is exactly **one** `<h1>` tag matching the recommended H1.
- Update subheadings (`<h2>`, `<h3>`) to align with the recommended semantic hierarchy.
- Maintain existing styling classes and components — modify only text copy and heading levels.

#### 3. Image Alt Attributes
- Locate the image tags (`<img>` or framework `<Image>` components) identified in the report.
- Insert the exact recommended `alt` text attribute into each image element.
- Ensure decorative images without SEO value retain empty `alt=""`.

#### 4. Contextual Internal Links
- Find the source pages specified in the internal linking plan.
- Insert contextual hyperlinks using the exact recommended anchor texts and destination URLs.
- Ensure links use relative paths for internal navigation and preserve styling.

#### 5. Structured Data (JSON-LD Schema)
- Locate the `<head>` or root layout of the website (or page-specific components).
- Inject the provided Schema.org JSON-LD code blocks using `<script type="application/ld+json">`.
- Ensure JSON syntax is valid, escaped properly, and verified against Schema.org standards.

#### 6. Server Directives & Robots.txt
- Update or create `public/robots.txt` (or server equivalent) matching the exact specification.
- If redirect rules are specified (301 redirects for broken/changed URLs), add them to the routing configuration (e.g., `next.config.js` redirects, `.htaccess`, or `nginx.conf`).

---

### Safety & Verification Protocol:
1. **Safety First:** Create a git branch (e.g. `git checkout -b chore/apply-seo-updates`) before modifying files.
2. **Build Verification:** Run the project build script (`npm run build` / `npm test`) to ensure zero syntax errors, broken imports, or JSX errors.
3. **No Styling Breakages:** Ensure all CSS classes, Tailwind utility classes, or styled-components remain intact.
4. **Summary Diff:** Provide a clean summary of all modified files with code diffs highlighting the applied SEO changes.
```
