# Hales Jobs — Landing Page

Conversion-focused recruitment landing page for **Hales Jobs** ([halesjobs.co.uk](https://halesjobs.co.uk/)), part of Hales Group Ltd. Hand-built to agency standard and deployed as a static site on Netlify.

**Live:** https://hales-jobs-landing.netlify.app

## Stack

- Static HTML5 / CSS3 / vanilla JS — no frameworks, no build step
- Self-hosted fonts: **Fraunces** (display) + **Instrument Sans** (body), served from `assets/fonts/` with preloads
- Production CSS is inlined into `index.html` for a single-request first paint; `styles.css` is the same stylesheet kept as a standalone copy
- `netlify.toml` — publish root, security headers, immutable caching for `/assets/*`, one-week cache for `styles.css` / `script.js`

## Run locally

Open `index.html` directly, or serve the folder:

```sh
python3 -m http.server 8000
# → http://localhost:8000
```

## Deploy

- **Zip / drag-and-drop:** zip the contents of this folder and deploy to Netlify — no build command required.
- **Git-connected Netlify site:** connect the repo, leave the build command empty, set publish directory to `.`

## Design & CRO notes

- Palette: cream `#F7F4EA`, paper `#FFFDF6`, forest `#0A3D22`, brand green `#006838`, lime `#8DC63F`
- SVG stroke-draw hero illustration, infinite logo/sector marquee, custom cursor, `prefers-reduced-motion` fallbacks
- Real content throughout: live roles, correct branch addresses and phone numbers, genuine candidate reviews, H.A.L.E.S. values, REC / GLAA / Stronger Together accreditations
- Conversion features: sticky apply CTA, job search filters, social proof, sector cards, branch finder
- SEO: JSON-LD `EmploymentAgency` schema (5 branches + parent org), canonical/OG/Twitter tags, `sitemap.xml`, `robots.txt`
- Accessibility: WCAG AA+ contrast, 18px base type, skip link, accessible accordion, focus styles
- Lighthouse (local audit): 98 performance / 100 accessibility / 100 best practices / 100 SEO
