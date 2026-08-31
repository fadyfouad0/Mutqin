# Mutqin — ecosystem site

Static build for GitHub Pages.

- `index.html` — English
- `ar.html` — Arabic (RTL)
- `photos/`, `brand/` — image assets
- `support.js` — runtime

## Deploy

1. Commit this `docs/` folder to your repository.
2. Settings → Pages → Source: **Deploy from a branch**, Branch: `main`, Folder: `/docs`.
3. The site publishes at `https://<user>.github.io/<repo>/`.

The `.nojekyll` file is required so GitHub serves the files as-is.
