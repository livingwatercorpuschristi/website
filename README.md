# livingwatercorpuschristi.com — site bundle, v1.0

One-page corporate site with an English/Spanish toggle. Static files only: no build step, no forms, no cookies, no analytics. Version 1.0 (first live release, 2026-11-05). Earlier preview: Rev A.

## Files
- `index.html` — the whole page: copy, styles, script, and the Spanish strings.
- `assets/` — logo, header mark, 32 px favicon, social-share image (1200×630).
- `favicon.ico`, `apple-touch-icon.png` — browser and phone icons.
- `CNAME` — custom domain for GitHub Pages.
- `robots.txt`, `sitemap.xml`, `.nojekyll` — search and hosting housekeeping.

## Go live (GitHub Pages)
1. Put these files at the root of the `main` branch of a public GitHub repo.
2. Repo Settings → Pages → Deploy from a branch → `main`, `/ (root)`.
3. Custom domain: `livingwatercorpuschristi.com` (the `CNAME` file sets it).
4. DNS. Google says DNS for a domain bought through Google Workspace is hosted by Squarespace and reachable from the Google Admin console's domain settings. Add:
   - `A` on `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `AAAA` on `@` (optional): `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
   - `CNAME` on `www`: `livingwatercorpuschristi.github.io`
   - Remove any other `A`/`CNAME` records on `@` and `www`. Leave the `MX` and `TXT` records alone; they carry Google Workspace email.
5. After GitHub's DNS check passes, turn on Enforce HTTPS. That can take up to 24 hours.
6. Recommended: verify the domain under your GitHub account's Pages settings to block takeover.

## Editing
- English text is in the HTML. Spanish strings are the JSON object near the top of the script; each key matches an element's `data-i18n` attribute.
- Email links are assembled by script from `data-u`/`data-d` so simple scrapers don't see the addresses. Without script, the page shows `name [at] domain [dot] com`.
- Brand sources: `Marketing/01_brand-visual-direction.md` and `LWCC External Meeting Template Rev A`. The page background is `#EFEEEC`, matched to `LWCC Logo.png`.
