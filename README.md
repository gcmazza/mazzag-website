# Mazza Strategic Finance Consulting — website

This is the **workshop** repo: the actual website, kept separate from
[`mazzag-consulting`](https://github.com/gcmazza/mazzag-consulting) (the
factory's internal rules, journal, and specs).

Plain HTML/CSS, no build step, no framework. Open `index.html` and you're
reading the whole site.

- `index.html` — the page
- `styles.css` — all styling
- `assets/` — logo mark and the social link-preview image
- `sitemap.xml`, `robots.txt` — search engine plumbing
- `.github/workflows/deploy.yml` — deploys to Cloudflare Pages on every push to `main`

## Deploying

The workflow needs two repository secrets before it can deploy
(**Settings → Secrets and variables → Actions**):

- `CLOUDFLARE_API_TOKEN` — a token scoped to Cloudflare Pages deploys
- `CLOUDFLARE_ACCOUNT_ID` — your Cloudflare account ID

Neither value ever belongs in a chat or in this repo — see
[`tokens/TOKEN-MODEL.md`](https://github.com/gcmazza/mazzag-consulting/blob/main/tokens/TOKEN-MODEL.md)
in the office repo. Until both secrets are set, merges to `main` will fail
at the deploy step — the site itself is unaffected.

Both secrets and the Cloudflare Pages project (`mazzag-website`, Direct
Upload) are now configured — this merge is the deploy pipeline's first
real test end to end.
