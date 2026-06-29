# Open Sensory, LLC — What We're Working On

A simple static Bootstrap site presenting strategic concepts for discussion with
agricultural industry leaders. Built as plain HTML + Bootstrap (via CDN), so it
runs on GitHub Pages with no build step.

## Structure

```
.
├── index.html                     # Landing page with one-sentence concept cards
├── assets/
│   └── css/
│       └── styles.css             # Shared styling
├── pages/                         # One detail page per concept
│   ├── ag-tech-benchmarking.html
│   ├── olive-oil-landscape.html
│   ├── succession-planning.html
│   ├── crop-hedging.html
│   ├── crop-protection-upheaval.html
│   └── crop-alerts.html
└── Concepts_2026.md               # Source notes (not published)
```

## Editing content

- **Card summaries** live in `index.html` (one `<p class="card-text">` per card).
- **Full descriptions** live in the matching file under `pages/`.
- To add a new concept: copy an existing file in `pages/`, edit it, then add a
  new card linking to it in `index.html`.

## Preview locally

Open `index.html` directly in a browser, or run a local server:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Publish with GitHub Pages

1. Create a repository on GitHub and push this folder:

   ```bash
   git init
   git add .
   git commit -m "Initial concepts site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```

2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose branch **main** and folder **/ (root)**, then **Save**.
5. After a minute, your site is live at
   `https://<your-username>.github.io/<repo>/`.

No Jekyll or build configuration is required. If you ever want to disable
Jekyll processing, add an empty `.nojekyll` file at the root.
