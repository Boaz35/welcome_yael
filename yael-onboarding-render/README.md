# Yael Heimer onboarding page (Render static site)

A single, self-contained page: `index.html`. There's no build step and nothing to install.

## Deploy

1. Push this folder to a GitHub or GitLab repo, with the files at the repo root.
2. In Render, choose **New > Blueprint**, pick the repo, and approve. `render.yaml` sets up the static site.
   - Manual alternative: **New > Static Site**, Build Command `echo ok`, Publish Directory `.`
3. Render gives you a URL like `https://yael-onboarding.onrender.com`. Every push to the main branch redeploys the site.

## Notes

- **Privacy:** Render static sites are public to anyone with the URL. Search engines are blocked (meta tag, `X-Robots-Tag`, `robots.txt`), but there's no password. To restrict access, put it behind Cloudflare Access or another auth proxy, or keep the claude.ai artifact as the private copy.
- **Custom domain:** in Render, open the site and go to Settings > Custom Domains, for example `onboarding.zemingo.com`.
- **Editing:** change `index.html` and push. The page caches with `no-cache`, so updates show up right away.
