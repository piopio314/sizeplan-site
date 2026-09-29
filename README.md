# SizePlan website

Static marketing and help site for SizePlan MT5. Plain HTML and CSS, no build
step, hosted on GitHub Pages.

- `index.html` - landing page
- `quick-start.html` - install, first trade, inputs, troubleshooting
- `faq.html` - frequently asked questions
- `404.html` - GitHub Pages not-found page (uses root-relative links)
- `assets/style.css` - shared styles; palette matches the EA panel
- `assets/logo.svg` - logo and favicon

Rules: English only; describe only behaviour the current EA build has; never
promise profits; keep the risk warning in every footer. The custom domain is
`sizeplan.com` (file `CNAME`; DNS at Porkbun: four GitHub Pages A records and
`www` CNAME to `piopio314.github.io`).
