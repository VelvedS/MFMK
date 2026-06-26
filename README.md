# MA Food for MA Kids — Coalition Website

Static site for the Massachusetts Food for Massachusetts Kids coalition. Plain HTML / CSS — no build step, no JavaScript framework.

## Pages

| File | Page |
| --- | --- |
| `index.html` | Home (immersive hero) |
| `home-v2.html` | Alternate home (magazine-overlay layout) |
| `grant-information.html` | MA FRESH grant info |
| `policy-priorities.html` | Policy priorities |
| `our-coalition.html` | Coalition members + meeting info |
| `join-the-coalition.html` | Sign-up |
| `take-action.html` | Bill status, meet with legislators |
| `share-with-your-networks.html` | Social copy templates |
| `faq.html` | FAQ |

## Folders

- `assets/` — logo, hero photos, page photos, web fonts. Referenced from HTML via relative paths (`assets/logo.png`, `assets/pages/*.jpg`).
- `uploads/` — original source photos (kept for editorial reference; not strictly required for the site to render, but useful when re-cropping).
- `styles.css` — shared design tokens, header, footer, buttons, type.
- `pages.css` — shared layout helpers for subpage sections.

## Run locally

No build step. From this directory:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Or open `index.html` directly in a browser.

## Deploy to Vercel

Import the GitHub repo in the [Vercel dashboard](https://vercel.com/new). The included `vercel.json` enables clean URLs (so `/grant-information` works as well as `/grant-information.html`). No build command, no output directory — Vercel serves the static files directly.

Optional CLI:

```bash
npm i -g vercel
vercel       # first run, follow prompts
vercel --prod
```

## Push to GitHub

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-user>/<your-repo>.git
git push -u origin main
```
