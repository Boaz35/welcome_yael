# Yael Heimer onboarding page

This is a single, self-contained page (`index.html`), deployed to Render as a static site through a Blueprint (`render.yaml`). There's no build step and no dependencies.

## Deploy with the Blueprint

1. Create a GitHub or GitLab repo and push these files to its root:
   `index.html`, `render.yaml`, `favicon.svg`, `robots.txt`
2. In Render, open **New > Blueprint**, connect the repo, and click **Apply**.
3. Render creates the `yael-onboarding` static site and gives it a URL like `https://yael-onboarding.onrender.com`.

After that, every push to the default branch redeploys automatically. Changes to `render.yaml` sync on the next push as well.

## What the Blueprint sets

| Setting | Value |
|---|---|
| Runtime | `static` |
| Build | none (just an echo, because Render requires a buildCommand) |
| Publish path | repo root |
| PR previews | off |
| Headers | `noindex`, framing limited to the same origin, nosniff, a strict referrer policy, and `no-cache` on the HTML so edits show up immediately |

## Notes

- **Privacy:** anyone with the URL can open the site. Search engines are blocked three ways (meta tag, `X-Robots-Tag` header, `robots.txt`), but there's no password. To restrict it to the team, put Cloudflare Access or another auth proxy in front of a custom domain.
- **Custom domain:** in Render, open the site and go to **Settings > Custom Domains**, for example `onboarding.zemingo.com`. Custom domains are managed in the dashboard, not in the Blueprint.
- **Editing:** change `index.html`, commit, and push.
