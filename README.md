# Open Sensory

Static Bootstrap site for Open Sensory. Hearing technology is the primary
narrative; agriculture technology stays live under `/agriculture/` and in the
footer only. Built as plain HTML + Bootstrap (via CDN) for GitHub Pages.

The entire site uses `noindex, nofollow` and is not intended for search indexing.

## Structure

```
.
├── index.html                 # Home — "Read the Room" (hearing tech)
├── about.html                 # Our story
├── contact.html               # General inquiry
├── agriculture/
│   ├── index.html             # Agriculture Technology concept cards
│   └── pages/                 # Concept detail pages
│       ├── ag-tech-benchmarking.html
│       ├── olive-oil-landscape.html
│       ├── succession-planning.html
│       ├── crop-hedging.html
│       ├── crop-protection-upheaval.html
│       └── crop-alerts.html
├── assets/
│   ├── css/styles.css
│   └── images/
└── Concepts_2026.md           # Source notes (not published)
```

## Editing content

- **Home / About / Contact** copy lives in the matching root HTML files.
- **Agriculture cards** live in `agriculture/index.html`.
- **Agriculture detail pages** live under `agriculture/pages/`.
- Primary nav: Home · About · Contact. Agriculture is footer-only.

## Preview locally

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Push updates to GitHub

The live site is served from the `main` branch of
[`node-econ/opensensory`](https://github.com/node-econ/opensensory) via GitHub Pages
at [opensensory.net](https://opensensory.net/).

After editing files locally:

```bash
git status
git add .
git commit -m "Describe your update here"
git push origin main
```

Notes:

- Do **not** commit `.env` (listed in `.gitignore`; contains credentials).
- Images belong in `assets/images/`. From agriculture detail pages, reference as
  `../../assets/images/your-file.jpg`.
- After pushing, hard-refresh the browser if you do not see the change right away.

## Publish with GitHub Pages

1. Push `main` to GitHub.
2. On GitHub: **Settings → Pages** → Deploy from branch **main** / **(root)**.
3. Custom domain: `opensensory.net` (see repo `CNAME`).

No Jekyll or build configuration is required. If you ever want to disable
Jekyll processing, add an empty `.nojekyll` file at the root.
