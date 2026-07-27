# Deploy to GitHub Pages

This repository is a standalone static Astro site. GitHub Actions builds `dist/` and deploys it through `.github/workflows/deploy.yml`.

## Repository setup

1. Create the public `zhongyangchuwu.github.io` repository and add it as this repository's `origin` remote.
2. Push the `main` branch.
3. In **Settings → Pages**, select **GitHub Actions** as the publishing source.
4. Do not enable Pages until template identity and example content have been replaced with real material.

A public standalone repository is the simplest option for a public personal homepage. GitHub Pages publishes public content even when the source repository is private, and private-repository Pages requires an eligible GitHub plan.

## Custom domain

The intended public address is `https://zycw.dev`. `astro.config.mjs` already sets this as Astro's `site` URL and deliberately has no `base` setting.

1. In **Settings → Pages**, set the custom domain to `zycw.dev`.
2. At the DNS provider, point the apex domain to GitHub Pages using all four `A` records:

   ```text
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

3. Remove any conflicting active origin for `zycw.dev` before switching DNS.
4. Wait for GitHub DNS verification, then enable **Enforce HTTPS**.

GitHub Pages custom domains are configured in repository settings; a committed `CNAME` file is not required for this Actions workflow.

## Verify

After a deployment:

1. Confirm the **Deploy to GitHub Pages** workflow succeeds.
2. Open the deployment URL shown in the `github-pages` environment.
3. Verify the homepage, a content-detail page, RSS, and static assets.
4. After the DNS switch, verify `https://zycw.dev` and the desired `www` behavior.
