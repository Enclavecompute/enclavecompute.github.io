# Enclave Compute Website

Public marketing site for [Enclave Compute](https://www.enclavecompute.net), a Garner-based AI enablement consultancy serving small businesses across the Research Triangle.

## Positioning

Enclave Compute helps teams turn one painful workflow at a time into a useful AI capability. The company is vendor-pragmatic:

- managed business AI for ordinary research, writing, and operations;
- connected automation for repeatable, reviewable processes; and
- private, on-premise execution when sensitive data or offline operation requires it.

## Stack

- [Astro](https://astro.build/) static site
- GitHub Pages deployment
- `@astrojs/sitemap` for sitemap generation
- Plain Astro components and CSS; no client framework

## Development

```bash
npm ci
npm run astro -- dev --background
npm run astro -- dev status
npm run astro -- dev logs
npm run astro -- dev stop
```

## Verification

Run all checks before opening or merging a change:

```bash
npm run astro -- check
npm run build
npm audit --audit-level=high
```

The static output is written to `dist/`.

## Content rules

- Lead with measurable business workflows, not technology categories.
- Treat cloud, automation, and local AI as deployment choices—not ideologies.
- Qualify privacy, compliance, availability, and redaction claims.
- Label prototypes, synthetic-data tests, and evaluation results honestly.
- Keep human review explicit for clinical, legal, financial, or public-facing work.
- Do not publish client names, testimonials, or outcome claims without permission and supporting evidence.

## Structure

- `src/pages/index.astro` — homepage and primary positioning
- `src/pages/services/` — service-specific landing pages
- `src/pages/industries/` — industry landing pages
- `src/layouts/` — shared metadata, navigation, and landing-page layouts
- `src/styles/global.css` — site styles and responsive rules
- `public/llms.txt` — concise public description for AI crawlers

## Deployment

The production site deploys from the repository's GitHub Pages workflow. A commit or local build is not publication; review and explicit approval are required before pushing a branch that will update the public site.
