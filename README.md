# ReefSpotter — USVI Reef Screen

A static landing-page template for an AI-assisted coral reef screening tool (VICAR Lab, U.S. Virgin Islands).

This is a pure static site — no build step, no backend. Open `index.html` in a browser to view it.

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | Main page |
| `terms.html` | Terms page |
| `gA.jpg`, `gB.jpg`, `vicar-logo-long.png` | Images used by the main page |
| `uploads/` | An older/duplicate copy of the site (not referenced by `index.html`) |
| `screenshots/` | Reference screenshots |

## Run locally

```bash
# Any static server works; Python's is built in:
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy

This is a static site, so it's hosted on **GitHub Pages** straight from the `main` branch.

**Live site:** <https://laurenkolinger.github.io/ReefSpotter/>

To re-enable or change Pages settings later:

```bash
# Enable Pages from the root of the main branch
gh api -X POST repos/laurenkolinger/ReefSpotter/pages -f "source[branch]=main" -f "source[path]=/"
```

Or via the web UI: **Settings → Pages → Source: Deploy from a branch → `main` / `root` → Save**.
Pushing to `main` redeploys automatically within a minute or two.

### Alternative hosts

Any static host works (Cloudflare Pages, Netlify, etc.): connect the repo, set build command to *(none)* and output directory to `/`.
