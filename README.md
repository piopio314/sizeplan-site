# SizePlan website

Static marketing and help site for SizePlan MT5. Plain HTML and CSS, no build
step, hosted on GitHub Pages.

- `index.html` - landing page
- `quick-start.html` - install, first trade, inputs, troubleshooting
- `faq.html` - frequently asked questions
- `404.html` - GitHub Pages not-found page (uses root-relative links)
- `assets/style.css` - shared styles; palette matches the EA panel
- `assets/logo.svg` - logo and favicon
- `assets/shot-*.webp` - real screenshots from the demo account (panel, chart,
  Trade Manager), trimmed by 3 px; the numbered pins on them are positioned in
  percent, so re-check them when a screenshot is replaced
- `assets/og-image.png` - 1200x630 social preview

Rules: English only; describe only behaviour the current EA build has; never
promise profits; keep the risk warning in every footer. The custom domain is
`sizeplan.com` (file `CNAME`; DNS at Porkbun: four GitHub Pages A records and
`www` CNAME to `piopio314.github.io`).

SEO: every page carries a canonical URL, Open Graph/Twitter tags
(`assets/og-image.png`, 1200x630) and JSON-LD (home: Organization, WebSite,
SoftwareApplication; FAQ: FAQPage built from the `<details>` answers; quick
start: TechArticle). `robots.txt` points to `sitemap.xml`. When a page is
added, add it to `sitemap.xml`; when a page changes, bump its `<lastmod>` and,
for the FAQ, regenerate the FAQPage JSON-LD so it matches the visible answers.
Internal links to the home page use `/`, never `index.html`, so Google sees a
single home URL. Search Console: domain property `sizeplan.com`, verified by a
DNS TXT record at Porkbun.

Design (2026-09-29): the site reads like an annotated chart - grid paper
(`.paper`), dashed level lines with a price tag on the right edge (`.level`),
numbered pins on real screenshots with a legend (`.pin`, `.legend`), and a
monospaced ledger for figures. Fonts: IBM Plex Sans / Sans Condensed / Mono
from Google Fonts. The home-page lot calculator is plain inline JavaScript; it
rounds down to the lot step and refuses to round up to the minimum lot, like
the EA. Keep screenshots from a demo account and say so in the caption.
