# AGENTS.md

## What this repo is

Static marketing landing page for AgriPath, a GPS spray-tracking app for
Android (mobile app code lives elsewhere; this repo is the website only).
Published at `agripath.app` via GitHub Pages, deployed straight from the
`master`/`main` branch (per `README.md`) with no build or CI step.

## Stack

Pure hand-written HTML5 and CSS3, no frameworks, no build pipeline. Verified
by file listing: the repo has no `package.json`, no `node_modules`, and no
JS bundler config, only `index.html`, `style.css`, and static assets
(`icon.png`, `adaptive-icon.png`, `favicon.png`, `app-screenshot.jpg`,
`og.png`, `humans.txt`, `robots.txt`, `sitemap.xml`, `CNAME`). `humans.txt`
states explicitly: "Standards: HTML5, CSS3. Components: Hand-written. No
frameworks. No trackers."

## Commands

None. There is no build, lint, or test tooling in this repo. Edit
`index.html` / `style.css` directly and preview by opening `index.html` in
a browser, or serve the folder with any static file server.

## Layout

- `index.html` - the entire page markup, including SEO meta tags (title,
  description, keywords, canonical, Open Graph, Twitter Card) and a
  `SoftwareApplication`/`MobileApplication` JSON-LD block describing the app.
- `style.css` - all styling.
- `CNAME` - pins the custom domain `agripath.app` for GitHub Pages.
- `robots.txt` / `sitemap.xml` - crawling and single-URL sitemap for
  `https://agripath.app/`.
- `humans.txt` - team/site credits, states no frameworks and no trackers.
- `icon.png`, `adaptive-icon.png`, `favicon.png`, `app-screenshot.jpg`,
  `og.png` - image assets, per `README.md` copied here from `../assets/`
  in a sibling app project (not part of this repo, not inspected).

## Conventions

- No JavaScript, no analytics/tracking scripts, no external dependencies
  besides Google Fonts (`Inter`, `Source Serif 4`), loaded via `<link>` in
  `index.html`.
- SEO metadata (title, description, OG/Twitter tags, JSON-LD) is
  maintained by hand inside `index.html`; keep in sync with page copy.
- `sitemap.xml` and `humans.txt` both carry a `Last update` / `lastmod`
  date; update these when publishing changes.

## Gaps

No `package.json`, license file, or CI config exists. The `../assets/`
source directory referenced in `README.md` is outside this repo and was
not inspected.
