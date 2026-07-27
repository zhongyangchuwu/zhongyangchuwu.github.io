# ZYCW Main Site

Static personal homepage and research portfolio for `https://zycw.dev`, built with Astro 7.

## Development

```sh
npm ci
npm run dev -- --host 127.0.0.1 --port 4322
```

Open `http://127.0.0.1:4322/`.

## Build

```sh
npm run build
npm run preview -- --host 127.0.0.1 --port 4322
```

The static output is written to `dist/`.

## Deployment

GitHub Actions builds and deploys `dist/` through `.github/workflows/deploy.yml`. The production domain is configured as `https://zycw.dev` in `astro.config.mjs`; do not add an Astro `base` value while using this custom domain.

See [docs/github-pages.md](docs/github-pages.md) for GitHub Pages, custom-domain, DNS, and HTTPS setup.

## Content

The repository currently contains restored template content. Replace Claude Shannon's identity, avatar, social links, and example academic content with real material before enabling public Pages deployment.
