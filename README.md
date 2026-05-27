# AgriPath landing page

Static landing page for [agripath.app](https://agripath.app). Pure hand-written HTML and CSS, no build step.

## Files

- `index.html`: the page
- `style.css`: all styling
- `CNAME`: tells GitHub Pages to serve this site at `agripath.app`
- `icon.png`, `adaptive-icon.png`, `favicon.png`, `app-screenshot.jpg`: copied from `../assets/` so GitHub Pages can serve them from this folder

## Publishing on GitHub Pages

1. In the repo settings on GitHub, go to **Settings - Pages**.
2. Set **Source** to `Deploy from a branch`, branch `master` (or `main`), folder `/landing`. Save.
3. GitHub Pages will publish from this folder. The included `CNAME` file pins the custom domain to `agripath.app`.
4. Under **Settings - Pages**, enable **Enforce HTTPS** once the certificate provisions (usually a few minutes after DNS is correct).

## DNS records (at your domain registrar)

Point `agripath.app` to GitHub Pages by adding these records on the apex (`@`) record:

| Type | Host | Value           |
|------|------|-----------------|
| A    | @    | 185.199.108.153 |
| A    | @    | 185.199.109.153 |
| A    | @    | 185.199.110.153 |
| A    | @    | 185.199.111.153 |

And for `www`:

| Type  | Host | Value                          |
|-------|------|--------------------------------|
| CNAME | www  | `<your-github-user>.github.io.` |

Propagation usually takes 5-30 minutes. Verify with `dig agripath.app` or `nslookup agripath.app`.
