# NovaTech Store

A fully self-contained single-page store for NovaTech — PC & Gaming hardware in Muscat, Oman.

The entire application (markup, styles, scripts, fonts and images) is bundled into a single
[`index.html`](./index.html) file with no external network requests, so it can be hosted on any
static host.

## Deploy on Cloudflare Pages

This repo is ready to deploy on **Cloudflare Pages** as a static site — no build step required.

1. In the Cloudflare dashboard, go to **Workers & Pages → Create → Pages → Connect to Git**.
2. Select this repository.
3. Build settings:
   - **Framework preset:** `None`
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/` (repository root)
4. Deploy. Cloudflare serves `index.html` at the site root.

Any push to the connected branch triggers an automatic redeploy.

### Deploy with Wrangler (optional)

```bash
npx wrangler pages deploy . --project-name novatech-store
```
