# Zyvantiq — Product Requirements Document (PRD)

> **Document purpose:** Build-ready product and engineering specification for an AI coding agent.
>
> **Project:** Zyvantiq corporate website  
> **Repository:** https://github.com/HYVIKAS6/zyvantiq  
> **Reference:** https://equiwiz.com/  
> **Document version:** 1.0  
> **Prepared:** 12 November 2026  
> **Status:** Ready for implementation, subject to the business-content decisions called out below.

---

## 1. Executive summary

Build **Zyvantiq**, a polished, responsive, search-optimized B2B technology and digital engineering website. Use Equiwiz as a reference for breadth of information architecture and conversion patterns—not as a source to copy its wording, branding, images, testimonials, customer logos, metrics, or visual design.

The proposed Zyvantiq positioning is:

> **Zyvantiq helps ambitious businesses design, build, modernize, and scale intelligent digital products with software engineering, AI, data, and cloud expertise.**

The site must explain what Zyvantiq does, who it helps, how engagements work, and what outcomes it can credibly deliver. It must guide enterprise decision-makers from discovery to a qualified project enquiry. It is a **marketing and lead-generation website**, not a SaaS product: do not build user accounts, dashboards, payments, or an admin portal for the first release.

Implement the site using reusable templates and typed content data. The service, sub-service, industry, case-study, article, and job pages should be generated from structured content rather than duplicated page components.

## 2. Business assumptions and content integrity

The repository is empty and no Zyvantiq brand guide, verified company profile, portfolio, contact details, customer list, or approved claims were supplied. Therefore:

1. Treat the service positioning and information architecture in this PRD as a proposed starting point for a company similar in category to the reference site.
2. Put all editable company details in one typed `siteConfig`/content configuration: legal name, tagline, email, phone, office locations, social URLs, booking URL, and copyright text.
3. Do not invent years in business, project counts, revenue impact, client names, testimonials, certifications, office locations, employee counts, awards, or delivery statistics.
4. Do not publish fake case studies or imply that illustrative sample projects were delivered by Zyvantiq. Use clearly marked internal draft/sample records or an honest “Case studies coming soon” state until approved evidence is supplied.
5. Do not show fabricated customer logos or partner badges. Hide the customer-logo strip when no approved logos exist.
6. The contact email, phone numbers, Calendly/booking URL, social links, and careers destination must be configurable and must not be guessed. If not configured, hide the relevant link or provide a clearly worded contact fallback—never render a dead `href="#"`.
7. Do not reuse Equiwiz copy, design assets, logos, or photographs. Write original Zyvantiq copy and use original, licensed, or properly attributed visual assets.

## 3. Product goals

### 3.1 Primary goals

- Establish Zyvantiq as a credible technology engineering and consulting partner.
- Clearly communicate the company’s service catalogue across software/product engineering, enterprise applications, cloud/DevOps/security, low-code/no-code, staff augmentation, AI, and data.
- Help visitors find solutions relevant to their industry and business problem.
- Convert qualified visitors through project enquiry and consultation scheduling.
- Demonstrate credibility through verified case studies, approved testimonials, transparent process descriptions, and technical depth.
- Support search discovery with unique, indexable pages for major services, sub-services, industries, insights, and case studies.
- Keep the implementation maintainable: one page template per content type, shared components, structured content, strict TypeScript, and limited client-side JavaScript.

### 3.2 Success measures

Instrument these events when analytics consent and configuration are available:

- Project CTA click-through rate.
- Contact-form starts, successful submissions, and validation errors.
- Consultation-booking link clicks.
- Service and industry page visits.
- Case-study and insight engagement.
- Mobile navigation usage and navigation abandonment.
- Organic landing-page traffic and search-index coverage.

Do not fabricate a launch baseline or target. Establish baseline metrics after launch and set targets with the business owner.

### 3.3 Non-goals for release 1

- SaaS product functionality, user accounts, role-based customer dashboards, billing, or payment processing.
- A custom CMS/admin application. Keep content data-driven and easy to update in code; a CMS can be added later if editorial volume requires it.
- Live chat or an AI chatbot unless separately approved and configured.
- Complex scroll-jacking, heavy 3D scenes, video backgrounds, or animation-heavy sections that compromise performance/accessibility.
- Copying the reference company’s exact content, layout, testimonials, customer metrics, artwork, or branding.

## 4. Audience and user journeys

### 4.1 Primary audiences

- **CTO / CIO / VP Engineering:** needs architecture, modernization, security, scalability, and delivery confidence.
- **Founder / Product leader:** needs product discovery, MVP delivery, SaaS engineering, UX, and a team that can execute.
- **Business / Operations leader:** needs workflow automation, low-code solutions, data visibility, and system integration.
- **Data / AI leader:** needs practical AI/ML implementation, data platforms, analytics, governance, and production operations.
- **Talent / HR partner:** wants to understand engineering team augmentation or explore careers.

### 4.2 Core journeys

1. **New project:** Home → service family → relevant sub-service → case study/process → Start a Project → contact form → success confirmation.
2. **Industry discovery:** Home → industry directory → industry page → related services/case study → contact.
3. **Technical evaluation:** Service page → technology/process/security sections → case study → About → consultation CTA.
4. **Thought leadership:** Insights listing → article → related article/service → contact CTA.
5. **Candidate:** Careers → role detail → application instructions or configured external application destination.

Every journey must have a clear next step and working links. Avoid CTA dead ends.

## 5. Brand and experience direction

### 5.1 Brand personality

Confident, practical, technically sharp, clear, modern, collaborative, and outcome-oriented. The site should feel like a credible engineering partner—not a generic template, crypto landing page, or consumer app.

### 5.2 Proposed visual direction

This is a proposed starter system, not a supplied brand guide; keep it easy to change through design tokens.

- **Primary canvas:** warm white / very light cool gray.
- **Primary text:** deep ink/navy.
- **Primary accent:** electric blue or blue-violet for links and primary CTAs.
- **Secondary accent:** restrained teal for data/AI highlights.
- **Surfaces:** white cards, subtle neutral borders, restrained shadows, generous whitespace.
- **Typography:** modern sans-serif with clear display/body hierarchy; self-host or use `next/font` so layout does not depend on runtime third-party font requests.
- **Logo:** create a simple original text wordmark “zyvantiq” and a small geometric mark only as a temporary brand treatment. Keep it replaceable when official artwork is provided.
- **Imagery:** use a small, consistent set of high-quality, licensed technical, product, data, cloud, and team visuals. Prefer optimized images and custom diagrams over random stock-photo mosaics.

Create reusable design tokens for color, type scale, spacing, radius, shadows, containers, breakpoints, and motion. Use consistent container widths, vertical rhythm, button styles, card patterns, and focus states.

### 5.3 Interaction principles

- Subtle, purposeful transitions only; respect `prefers-reduced-motion`.
- Buttons and links have hover, focus-visible, active, disabled, and loading states as relevant.
- Menus work with pointer, keyboard, touch, and screen readers.
- Avoid essential content that appears only on hover.
- Use semantic landmarks, heading order, native form controls, and visible focus indicators.

## 6. Information architecture and route inventory

Use the following routes (trailing slash policy must be consistent; prefer canonical URLs without a trailing slash unless the hosting setup dictates otherwise).

### 6.1 Global routes

- `/` — Home
- `/services` — Services overview
- `/ai-data` — AI & Data overview
- `/industries` — Industries overview
- `/work` — Case studies / selected work
- `/insights` — Articles listing
- `/about` — About Zyvantiq
- `/careers` — Careers listing
- `/contact` — Contact and project enquiry
- `/privacy` — Privacy policy
- `/security` — Security and trust overview (publish only statements that have been verified)
- `/terms` — Terms (only if legally reviewed and required)

### 6.2 Service families

Create family landing pages using one reusable service-family template:

- `/services/product-engineering-saas`
- `/services/enterprise-software`
- `/services/cloud-devops-security`
- `/services/low-code-no-code`
- `/services/staff-augmentation`

Create sub-service detail pages from typed data under the relevant family route. Required catalogue:

**Product Engineering & SaaS**
- Product strategy and consulting
- SaaS development and platforms
- Legacy product modernization
- UX/UI design and product experience
- Product maintenance and support

**Enterprise Software & Applications**
- Custom software development
- Software architecture
- Legacy application modernization
- Digital transformation consulting
- API development and integration
- Mobile application development
- Customer experience platforms

**Cloud, DevOps & Security**
- Cloud strategy and consulting
- Cloud migration and modernization
- Cloud-native development
- DevOps, CI/CD and automation
- Cloud and application security

**Low-Code / No-Code Development**
- Microsoft Power Platform
- OutSystems development
- Zoho Creator development
- Citizen-development enablement
- Enterprise system integration

**Staff Augmentation**
- Dedicated engineering teams
- Offshore development centre model

### 6.3 AI & Data families and sub-services

Family pages:
- `/ai-data/artificial-intelligence`
- `/ai-data/machine-learning`
- `/ai-data/data-engineering`
- `/ai-data/data-analytics-bi`

Sub-service catalogue:

**Artificial Intelligence**
- AI strategy and roadmap consulting
- Generative AI solutions
- AI integration and implementation
- AI application development
- Intelligent agent development
- LLM development and customization
- On-demand AI expertise
- Conversational AI and chatbot development

**Machine Learning**
- MLOps and model governance
- Natural language processing
- Computer vision and image analytics

**Data Engineering**
- Big-data solutions and management
- Data warehouse strategy and implementation
- Data governance and compliance consulting
- Data visualization and dashboards
- Data strategy and roadmap consulting
- Data-platform modernization

**Data Analytics & BI**
- Data analytics
- Robotic process automation
- Data science consulting
- Predictive analytics

Use readable, stable slugs generated from content data. Each leaf page should have its own URL, title, meta description, canonical URL, breadcrumb, content, related services, and CTA.

### 6.4 Industry pages

Create an industry directory and data-driven detail page for each:

- FinTech
- HRTech
- EdTech
- Retail & eCommerce
- LegalTech
- Manufacturing
- Healthcare
- Cleantech
- InsurTech
- Travel & Hospitality
- Software & Hi-Tech

Each industry page must explain business context, common challenges, relevant solution areas, typical workflows/integrations, considerations around compliance or security (only where accurate), related services, and a conversion CTA. Do not claim Zyvantiq has regulated-industry certifications or customer experience without evidence.

### 6.5 Work / case studies

- `/work` — filterable or grouped case-study index (only add filters if there are enough real entries to justify them).
- `/work/[slug]` — case-study detail template.

Case-study schema: title, slug, industry, summary, client name (optional and permission-based), challenge, approach, solution, technology list, verified outcomes, hero image, related services, publication state, and SEO metadata.

A case study cannot be published without an approved source for client naming and outcome claims. Until real content exists, show a restrained empty state with a CTA; do not fill the page with invented “10x” or percentage results.

### 6.6 Insights / blog

- `/insights` — listing with category/topic filters only if functional.
- `/insights/[slug]` — article page.

Article schema: title, slug, excerpt, author, author role (optional), publication date, updated date, reading time (calculated or reviewed), category, tags, hero image/alt text, body, related links, and SEO metadata. No fake author biographies or publication dates. Include “draft” articles only in source control, never in the public listing.

### 6.7 About, careers, contact, and legal

- **About:** company overview, principles, capabilities, delivery approach, leadership/team only when approved, and CTA.
- **Careers:** list open positions from data; role detail includes location, work mode, employment type, responsibilities, qualifications, and application instructions. Hide closed roles. Do not list fabricated openings.
- **Contact:** enquiry form, configured email/phone/location, optional booking link, and privacy notice.
- **Privacy:** publish a real policy that accurately describes collected data, purposes, processors, retention, rights, and contact details. Obtain legal review before production.
- **Security:** publish only accurate security practices and certifications. Do not imply SOC 2, ISO, HIPAA, PCI, GDPR certification, or audit completion unless evidence exists.

## 7. Page-level requirements

### 7.1 Header and navigation

- Responsive global header with original Zyvantiq wordmark.
- Desktop navigation: Services, AI & Data, Industries, Work, Insights, About, Careers, Contact; prominent “Start a Project” CTA.
- Services, AI & Data, and Industries should use accessible mega-menus with clear groups and links.
- Mobile menu uses a keyboard-accessible drawer or disclosure pattern; lock body scroll while open, close on Escape and route selection, and restore focus appropriately.
- Header may become sticky after scroll, but must not obscure anchor targets or page content.

### 7.2 Home page section order

1. Header.
2. Hero: concise value proposition, supporting copy, primary “Start a Project” CTA, secondary “Explore Services” CTA, and a purposeful visual (abstract system diagram, product interface composition, or custom illustration).
3. Trust strip: approved client/partner logos only; hide if none are approved.
4. Capability overview: five service families plus AI & Data.
5. About / positioning section: what Zyvantiq does and why its engineering approach matters.
6. Selected industries grid.
7. Delivery approach / engagement lifecycle: Discover → Define → Design → Build → Validate → Launch & Evolve (adapt labels if needed).
8. Featured work: verified case studies only; empty state if none approved.
9. Differentiators: architecture-first thinking, practical AI, security-minded delivery, collaboration, and maintainability—describe capabilities, not unverifiable superlatives.
10. Approved testimonials only; hide if none exist.
11. Insights preview: published articles only.
12. FAQ: concise, genuinely helpful answers about engagement, delivery, integrations, security, and project starts.
13. Final CTA band.
14. Footer.

### 7.3 Service-family and detail template

Every service page should contain:

- Breadcrumbs and a specific H1.
- Outcome-led introduction in plain language.
- Clear CTA(s).
- Service/sub-service cards or capability list.
- Problems addressed and typical outcomes (qualitative unless metrics are verified).
- Delivery approach / lifecycle.
- Technology and platform expertise (only technologies the business is prepared to support).
- Relevant use cases and integrations.
- Related industries and services.
- Approved case study/testimonial where available.
- FAQ where useful.
- Final CTA.

Do not dump a long list of technology logos without explaining how they relate to customer needs.

### 7.4 Industry template

- Industry-specific hero and concise positioning.
- Industry challenges / operating context.
- Zyvantiq solution areas.
- Relevant capabilities and integrations.
- Data, privacy, security, and regulatory considerations, written carefully and without unsupported certification claims.
- Relevant verified work, when available.
- Related services and CTA.

### 7.5 Work, insights, careers templates

- Consistent listing cards and clear empty states.
- Detail pages have readable typography, semantic content structure, related links, and social-share metadata where applicable.
- Provide a back-to-list link and breadcrumbs.
- Do not expose draft content in public routes or sitemap.

### 7.6 Contact form

Required fields:
- Enquiry type: Project / Sales, Partnership, Careers, Other.
- First name.
- Last name.
- Work email.
- Company.
- Job title (optional if the business prefers a shorter form).
- Project details / message.
- Required privacy acknowledgement with a link to the privacy policy.

Behavior:
- Inline validation with clear accessible error messages.
- Normalize and validate on the server; client-side validation is for UX only.
- Provide submitting, success, and failure states.
- Prevent duplicate rapid submissions.
- Use a honeypot and minimum-completion-time check; add provider-backed rate limiting and optional CAPTCHA/Turnstile if configured.
- Send submissions server-side to a configured email provider. Do not expose provider credentials in the browser.
- If email integration is not configured, do not pretend to submit successfully. Return a clear failure/fallback state and log a safe diagnostic without storing sensitive message content in logs.
- Never persist enquiry content to an unprotected database. If persistence/CRM integration is added later, document consent, retention, access control, and deletion policy.

## 8. Recommended technical architecture

### 8.1 Primary stack

Use a modern TypeScript-first stack chosen for strong server rendering, small client bundles, maintainability, and deployment simplicity:

- **Language:** TypeScript, strict mode.
- **Framework:** Next.js 16.x using the App Router.
- **UI:** React 19.x (use the stable version compatible with the chosen Next.js release).
- **Styling:** Tailwind CSS 4.x plus a small set of CSS variables/design tokens.
- **Package manager:** pnpm with a committed lockfile.
- **Runtime:** Node.js 26 Active LTS, unless the deployment platform does not yet support it; in that case use the newest supported Active LTS and record why.
- **Icons:** one consistent, tree-shakeable icon library (e.g. Lucide) or custom inline SVGs; do not mix icon packs.
- **Validation:** Zod for server-side request/content validation where appropriate.
- **Email:** a provider adapter (for example, Resend) configured through environment variables; never hardcode secrets.
- **Testing:** Playwright for key browser journeys; lightweight unit tests for validation and data utilities.
- **Deployment target:** Vercel is preferred for a Next.js application, but keep standard Node deployment compatibility.

**Version baseline checked on 12 November 2026:** Next.js `16.4.6`, React `19.3.1`, Tailwind CSS `4.3.5`, and Node.js `26.13.0` (26.x Active LTS). Before installation, verify the current stable releases and their official peer/runtime requirements; do not install prerelease/canary builds in production. Use compatible stable versions and commit `pnpm-lock.yaml`.

### 8.2 Rendering and performance strategy

- Default to React Server Components; add `'use client'` only for components that genuinely need browser state, events, or browser APIs.
- Pre-render stable marketing content statically. Use dynamic rendering only for content/forms that require it.
- Use Next.js navigation, metadata, image, and font capabilities instead of reimplementing them.
- Use `next/image` for raster images with explicit dimensions/aspect ratios and responsive sizing.
- Prefer CSS transitions and static/transform-based effects over large animation libraries.
- Avoid global client state libraries; this site does not require one.
- Avoid adding a database, headless CMS, or API layer without a demonstrated requirement.
- Keep route content and configuration in typed modules; separate content from presentation.
- Use dynamic route templates for service sub-pages, industries, case studies, articles, and roles.
- Lazy-load below-the-fold interactive elements and non-critical media.
- Avoid loading analytics, chat, video, or third-party scripts before consent where consent is required.

### 8.3 Suggested source layout

~~~text
zyvantiq/
├── public/
│   ├── images/
│   ├── icons/
│   └── fonts/                 # only if licensed self-hosted fonts are supplied
├── src/
│   ├── app/
│   │   ├── (marketing)/
│   │   │   ├── page.tsx
│   │   │   ├── services/
│   │   │   ├── ai-data/
│   │   │   ├── industries/
│   │   │   ├── work/
│   │   │   ├── insights/
│   │   │   ├── about/
│   │   │   ├── careers/
│   │   │   ├── contact/
│   │   │   ├── privacy/
│   │   │   └── security/
│   │   ├── api/contact/route.ts
│   │   ├── sitemap.ts
│   │   ├── robots.ts
│   │   ├── manifest.ts
│   │   ├── layout.tsx
│   │   └── globals.css
│   ├── components/
│   │   ├── layout/             # header, mega-menu, footer, breadcrumbs
│   │   ├── navigation/
│   │   ├── sections/           # reusable page sections
│   │   ├── cards/
│   │   ├── forms/
│   │   └── ui/                 # buttons, badges, accordions, etc.
│   ├── content/                # typed content records and article content
│   ├── config/                 # site config and navigation config
│   ├── lib/                    # SEO, validation, email adapter, helpers
│   └── types/
├── tests/
├── .env.example
├── .gitignore
├── next.config.ts
├── package.json
├── pnpm-lock.yaml
├── tsconfig.json
└── README.md
~~~

Adjust this layout if the current Next.js conventions or generated scaffold differ; do not force a folder convention that adds complexity.

### 8.4 Content model and data strategy

Create strongly typed records for:
- `ServiceFamily` and `ServiceDetail`.
- `Industry`.
- `CaseStudy`.
- `Article`.
- `JobOpening`.
- `Testimonial`.
- `NavigationItem`.

Each record should include a stable slug and metadata fields. Use one shared page template per record type. Add validation for slug uniqueness and required fields. Content records should have a publication status; drafts must not be rendered, linked, or added to sitemap.

Store the site-wide editable fields in a single configuration file. Keep content in TypeScript/MDX/Markdown as appropriate. For the initial site, avoid introducing a database or CMS just to render static pages.

## 9. SEO, accessibility, security, and privacy

### 9.1 SEO

- Unique title and meta description for every indexable route.
- Canonical URL per page.
- Open Graph and social-sharing metadata.
- Dynamic XML sitemap containing published routes only.
- Correct `robots.txt`; staging/preview deployments must not accidentally be indexed.
- Semantic HTML, correct H1/H2 hierarchy, meaningful link text, image alt text, and internal linking.
- Structured data where valid: Organization, WebSite, Service, BreadcrumbList, Article, and JobPosting (only for actual open roles). Do not add fake review/rating schema or unsupported claims.
- No duplicate title/description content across all dynamic pages.

### 9.2 Accessibility

Target WCAG 2.2 AA where practical:
- Full keyboard navigation.
- Visible focus indicators.
- Accessible mega-menu/mobile menu and accordions.
- Proper labels, instructions, and error associations on forms.
- Adequate color contrast.
- Reduced-motion support.
- Logical heading and landmark structure.
- Do not communicate information through color alone.
- Test key flows with automated accessibility checks and manual keyboard navigation.

### 9.3 Security

- Keep all secrets in environment variables; commit `.env.example` with names and descriptions only.
- Validate all untrusted form input on the server.
- Add safe security headers (including a considered CSP, frame protections, MIME sniffing protection, and referrer policy) compatible with Next.js assets and any explicitly approved integrations.
- Do not expose stack traces, secrets, internal provider responses, or personal enquiry data to clients.
- Avoid unsafe HTML injection. Sanitize any Markdown/MDX content pipeline and keep authoring restricted to trusted source files.
- Do not log raw contact messages, tokens, or unnecessary personal data.
- Use provider-backed rate limiting in serverless deployments; do not rely on process-memory counters.
- Keep dependencies current and run vulnerability checks in CI.

## 10. Content and copywriting requirements

- Write original, concise, specific copy for Zyvantiq.
- Lead with customer problems and outcomes, then explain capabilities and technology.
- Use plain language; define acronyms where they first appear.
- Avoid unsupported superlatives such as “best,” “leading,” “world-class,” or guaranteed delivery claims.
- Never copy Equiwiz paragraphs, headings, testimonials, statistics, images, or client logos.
- For technology stacks, list only tools Zyvantiq can substantiate. Do not display every popular framework as a capability badge.
- Use clear calls to action consistently: “Start a Project,” “Talk to Our Team,” and “Explore Services.”
- Keep all copy editable in data/content files, not buried inside large JSX components.

## 11. Functional requirements and acceptance criteria

### 11.1 Navigation and routing

- [ ] All header/footer links resolve to valid internal or configured external destinations.
- [ ] Desktop mega-menus support mouse and keyboard operation.
- [ ] Mobile navigation works at narrow widths and closes predictably.
- [ ] Breadcrumbs reflect the actual route hierarchy.
- [ ] Unknown routes render a branded 404 page with working navigation.

### 11.2 Content pages

- [ ] Every service family, AI/data family, service detail, and industry route is rendered from structured data and uses the correct shared template.
- [ ] Each page includes unique H1, title, description, CTA, related links, and canonical metadata.
- [ ] Draft/placeholder content is not publicly exposed.
- [ ] Case studies and testimonials are hidden unless approved and evidence-backed.
- [ ] Blog list and article details work; published status controls visibility.
- [ ] Careers listing hides closed jobs; role pages show only approved openings.

### 11.3 Contact conversion

- [ ] Required fields validate on client and server.
- [ ] Invalid requests return field-specific errors.
- [ ] Valid submission is delivered through configured server-side email integration.
- [ ] A submission is not reported as successful when the email integration is missing or fails.
- [ ] Loading, success, and failure states are accessible and visually clear.
- [ ] Honeypot/time-trap and rate-limiting strategy are implemented.
- [ ] Privacy acknowledgement is present and links to the policy.

### 11.4 Quality and performance

- [ ] `pnpm lint`, `pnpm typecheck`, `pnpm test`, and `pnpm build` pass (script names may be adapted but all checks must exist).
- [ ] No TypeScript `any` unless justified and documented.
- [ ] No browser console errors or hydration mismatch warnings on key routes.
- [ ] Images are optimized; no layout shift caused by missing dimensions.
- [ ] No unnecessary client-side dependencies or duplicated component implementations.
- [ ] Validate Core Web Vitals on representative mobile and desktop routes; aim for good results (LCP ≤ 2.5 s, INP ≤ 200 ms, CLS ≤ 0.1) under suitable field/lab conditions, and document any blockers.
- [ ] Test at widths around 360 px, 390 px, 768 px, 1024 px, and 1440 px.

### 11.5 Accessibility and SEO

- [ ] Keyboard-only navigation is usable.
- [ ] Contrast and focus states are checked.
- [ ] Metadata, canonical tags, sitemap, and robots are correct.
- [ ] JSON-LD validates for applicable content types.
- [ ] No broken internal links or orphaned primary routes.

## 12. Testing plan

### Unit tests

Test slug generation/uniqueness, content publication filters, navigation data, form schema validation, email payload construction, and metadata helpers.

### Component tests

Test mobile navigation state, mega-menu keyboard behavior, accordion behavior, form error rendering, loading/success/failure states, and card links.

### End-to-end tests (Playwright)

At minimum:
1. Home loads and its primary CTA navigates to contact.
2. Desktop mega-menu opens and a service link navigates correctly.
3. Mobile menu opens, navigates, and closes.
4. A service-family and an industry detail route load with unique heading and metadata.
5. Contact form rejects invalid data and shows field errors.
6. Contact form success is only shown when the configured test email adapter accepts the request.
7. An unknown route shows the branded 404.
8. Published article/case study routes work; draft records are not visible.

Use deterministic test adapters/mocks for external email and analytics services. Do not send real enquiries during automated tests.

## 13. Delivery plan for the coding agent

Execute in this order; keep changes small and verify each phase:

### Phase 0 — Repository reconnaissance

- Inspect the repository, default branch, recent history, files, and current configuration before making changes.
- The repository is expected to be empty, but verify rather than assume.
- Check Node/pnpm availability and supported deployment runtime.
- Record any blockers; do not overwrite existing user work if the repository is no longer empty.

### Phase 1 — Foundation

- Initialize the Next.js App Router project with TypeScript, Tailwind, ESLint, and the chosen package manager.
- Configure strict TypeScript, aliases, formatting/linting, scripts, `.gitignore`, and `.env.example`.
- Add the base layout, design tokens, fonts, metadata defaults, global error/404/not-found handling, and shared container primitives.

### Phase 2 — Design system and site shell

- Implement responsive header, accessible mega-menus, mobile navigation, breadcrumbs, buttons, cards, section wrappers, CTA band, and footer.
- Verify keyboard and mobile interaction before adding all routes.

### Phase 3 — Content model and reusable templates

- Implement typed data schemas and records for service families/sub-services, AI/data families/sub-services, industries, case studies, articles, and jobs.
- Implement shared listing/detail templates and publication filtering.
- Generate route metadata from data. Validate all slugs are unique.

### Phase 4 — Core pages and conversion flow

- Build Home, Services, AI & Data, Industries, Work, Insights, About, Careers, Contact, Privacy, and Security pages.
- Add the contact route, server-side validation, configured email adapter, and safe anti-spam controls.
- Keep unverified portfolio, testimonial, metrics, contact, and company claims hidden or clearly marked as unpublished source data.

### Phase 5 — SEO, accessibility, and optimization

- Add sitemap, robots, canonical URLs, Open Graph, applicable JSON-LD, image optimization, security headers, and analytics consent handling if analytics is configured.
- Audit responsive behavior, color contrast, keyboard operation, reduced motion, and page performance.

### Phase 6 — Verification and handoff

- Run lint, typecheck, unit tests, Playwright, and production build.
- Fix all material failures; do not suppress errors merely to obtain a green build.
- Update README with setup, environment variables, scripts, architecture notes, and deployment steps.
- Provide a completion summary: pages implemented, integrations configured, test results, required business inputs, and known limitations.
- Do not deploy to production, create external services, spend money, or publish company claims without explicit authorization and credentials.

## 14. AI coding-agent operating instructions

**You are the senior full-stack engineer responsible for implementing this PRD.** Treat the requirements and acceptance criteria as binding.

1. Start by inspecting the actual repository and environment. Do not assume files or dependencies exist.
2. Create a concise implementation plan, then execute it. Do not stop after producing mockups or a static homepage.
3. Build the complete first-release website and all routes described here using reusable templates and structured data.
4. Use TypeScript strict mode. Prefer simple, explicit code over clever abstractions. Avoid `any`, duplicated data, duplicated page components, unnecessary dependencies, and over-engineered state management.
5. Use Server Components by default. Keep client components small and isolated. Do not mark the entire app as a client component.
6. Use semantic HTML and accessible interaction patterns. A visually attractive but keyboard-inaccessible menu/form is not acceptable.
7. Make mobile design a first-class requirement, not a desktop layout squeezed onto a phone.
8. Make the visual design distinctive to Zyvantiq. Use Equiwiz only as a reference for breadth, navigation structure, page patterns, and conversion flow. Do not clone it.
9. Do not fabricate content. If company data is missing, implement a config-driven field and hide the corresponding public UI until it is supplied. Use explicit TODOs in source documentation, not public-facing fake claims.
10. Keep secrets out of source control. Add `.env.example`, validate missing configuration, and make integration failure visible to the user in a safe way.
11. Add meaningful loading, empty, error, and success states. Never leave buttons that do nothing or links pointing to `#`.
12. Avoid adding an external service unless the PRD requires it. If an integration requires credentials, implement a clean adapter and document the missing environment variables.
13. Test routes, form behavior, navigation, responsive layouts, accessibility, SEO, and production build. Fix warnings that indicate real defects.
14. Do not suppress TypeScript/ESLint/build failures, disable security checks, or replace real functionality with fake success behavior.
15. Keep the README and PRD aligned with the implementation. If a technical decision must deviate from this PRD, document why and choose the simplest secure option.
16. Preserve existing user changes if any are discovered. Do not force-push, rewrite history, or delete files without a clear need.
17. Do not claim deployment or external email delivery succeeded unless verified by actual tool output.

## 15. Environment variables

Create `.env.example` with descriptions for any variable actually used. Likely names:

~~~dotenv
NEXT_PUBLIC_SITE_URL=http://localhost:3000
CONTACT_TO_EMAIL=
CONTACT_FROM_EMAIL=
RESEND_API_KEY=
TURNSTILE_SECRET_KEY=
NEXT_PUBLIC_TURNSTILE_SITE_KEY=
UPSTASH_REDIS_REST_URL=
UPSTASH_REDIS_REST_TOKEN=
NEXT_PUBLIC_ANALYTICS_ID=
~~~

Only implement the corresponding integration when selected/configured. Do not expose secret variables through `NEXT_PUBLIC_`. In production, `NEXT_PUBLIC_SITE_URL` must be set to the canonical public origin. Add a typed environment validation module and fail safely with clear diagnostics when required production variables are absent.

## 16. Definition of done

The initial release is complete only when:

- The site runs locally using the documented setup.
- All required global, family, detail, industry, work, insights, company, careers, contact, and legal routes work.
- Shared templates render content from typed data; no large duplicated page implementations exist.
- Navigation, responsive layouts, CTAs, breadcrumbs, and contact flow function.
- Contact success is truthful and depends on a real configured test adapter/provider response.
- Public content contains no fake statistics, customers, testimonials, certifications, or case-study results.
- SEO, accessibility, security, and performance requirements have been checked.
- Lint, typecheck, tests, and production build pass.
- README and `.env.example` are complete.
- The agent reports what remains dependent on Zyvantiq business input.

## 17. Business inputs needed before production launch

These are content/configuration inputs, not blockers to building the reusable website foundation:

- Approved legal/company name and tagline.
- Official logo and brand palette (or approval of the proposed starter visual system).
- Verified company description, operating locations, and contact email/phone.
- Approved booking URL and social links.
- Confirmation of the exact services and technologies Zyvantiq offers.
- Approved industries to target.
- Client permissions, verified case studies, metrics, testimonials, and logos (if available).
- Published articles and named authors (if available).
- Real job openings and application process (if hiring).
- Privacy-policy/legal review and data-retention requirements.
- Email provider/domain configuration and production environment variables.
- Analytics/consent requirements for target markets.

## 18. Reference and implementation sources

The following sources informed the information architecture and technology baseline. They are references for structure and current technical documentation, not sources to copy content from.

### Website reference

- Equiwiz home and navigation: https://equiwiz.com/
- Equiwiz work / case-study index: https://equiwiz.com/work/
- Equiwiz contact page and enquiry-field pattern: https://equiwiz.com/contact/

### Technical references (checked 12 November 2026)

- Next.js App Router: https://nextjs.org/docs/app
- Next.js installation and runtime requirements: https://nextjs.org/docs/app/getting-started/installation
- Next.js metadata and Open Graph: https://nextjs.org/docs/app/getting-started/metadata-and-og-images
- React version information: https://react.dev/versions
- Next.js releases: https://github.com/vercel/next.js/releases
- Tailwind CSS releases: https://github.com/tailwindlabs/tailwindcss/releases
- Node.js release schedule: https://github.com/nodejs/Release

---

**End of PRD.** Build the product described here—not a screenshot-only imitation of the reference site.
