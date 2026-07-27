# Deploy to GitHub Pages

This repository is a standalone static Astro user site. GitHub Actions builds `dist/` and deploys it through `.github/workflows/deploy.yml`.

## Default deployment

The current public address is:

```text
https://zhongyangchuwu.github.io/
```

Because this repository is the `zhongyangchuwu.github.io` user-site repository, it is served from the domain root. `astro.config.mjs` sets this URL as Astro's `site` value and deliberately has no `base` setting.

GitHub Pages is configured to use the **GitHub Actions** publishing source. Do not switch the source back to branch/Jekyll publishing: Astro source files are not Jekyll content.

## Repository workflow

1. Push `main`.
2. The **Deploy to GitHub Pages** workflow installs dependencies, builds `dist/`, uploads the artifact, and deploys it.
3. Confirm the workflow succeeds and open the `github-pages` deployment URL.

## Optional custom domain

`zycw.dev` is deferred. When you decide to use it:

1. Change Astro's `site` value to `https://zycw.dev`.
2. In **Settings → Pages**, set the custom domain to `zycw.dev`.
3. At the DNS provider, point the apex domain to GitHub Pages using all four `A` records:

   ```text
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

4. Remove any conflicting origin, wait for verification, then enable **Enforce HTTPS**.

Custom domains are configured in GitHub repository settings; this Actions workflow does not require a committed `CNAME` file.

## Content reminder

The repository currently contains restored template content. Replace Claude Shannon's identity, avatar, social links, and example academic content with real material before treating the public site as your personal homepage.
