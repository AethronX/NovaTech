# NovaTech Store

A fully self-contained single-page store for NovaTech — PC & Gaming hardware in Muscat, Oman.

The entire application (markup, styles, scripts, fonts and images) is bundled into a single
[`index.html`](./index.html) file with no external network requests, so it can be hosted on any
static host.

## Deploy on Vercel

This repo is ready to deploy on **Vercel** as a static site — no build step required.

1. In the Vercel dashboard, go to **Add New… → Project** and import this repository.
2. Project settings:
   - **Framework preset:** `Other`
   - **Build command:** *(leave empty)*
   - **Output directory:** *(leave empty — repository root is served)*
3. Deploy. Vercel serves `index.html` at the site root.

The included [`vercel.json`](./vercel.json) enables clean URLs and rewrites all
paths to `index.html`, so the single-page app resolves on any route. Any push to
the connected branch triggers an automatic redeploy.

### Deploy with the Vercel CLI (optional)

```bash
npx vercel deploy --prod
```

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
