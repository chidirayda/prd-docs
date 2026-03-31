# Rayda Docs

This site renders the markdown files in this folder as a browsable docs website.

## Documents

Use the sidebar or the links below. Always open the docs site via **`/` (index.html)** so pages render as HTML, not raw Markdown.

- [PRDs](prds/README.md)
  - [Kits, curated budget catalogs, and in-storage assets](prds/kits-and-storage-in-catalogs.md)

## Viewing locally

Serve the docs folder as the site root:

```bash
cd docs && python3 -m http.server 5173
```

Then open `http://localhost:5173/`.

Note: Docsify uses hash routing, so “shareable” links look like `/#/prds/...`. If you open a `.md` URL directly (e.g. `/prds/foo.md`), most static servers will show raw Markdown.

## Hosting

You can host this `docs/` folder as a static site.

### Option A: GitHub Pages

- Put this repo on GitHub
- In repository settings, enable Pages
- Set the Pages source to the branch/folder that contains `docs/index.html`

### Option B: Netlify / Vercel

- Create a new site from this repository
- Configure the build as “no build”
- Publish directory: the repository root (so `/docs/index.html` is accessible), or configure the platform to serve `docs/` as the site root.
