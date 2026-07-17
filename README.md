# ZYCW Main Site

Static personal homepage and research portfolio for `https://zycw.dev`, built with Astro 7.

## Local development

From the monorepo root:

```sh
just site-dev
```

Or from this directory:

```sh
npm ci
npm run dev -- --host 127.0.0.1 --port 4322
```

## Build

```sh
just site-build
```

The static output is written to `dist/`.

## Deployment

GitHub Pages builds this application through the root workflow at `.github/workflows/deploy-main-site.yml`. It runs from `apps/main-site`, uploads `dist/`, and deploys the resulting static artifact.

The production domain is configured in `astro.config.mjs` as `https://zycw.dev`; see [../../docs/github-pages.md](../../docs/github-pages.md) for repository, Pages, and DNS setup.

## Content

The restored template content is intentionally present for editing. Replace the Claude Shannon identity, avatar, social links, and example academic content with real material before enabling public Pages deployment.
