# Mutqin — landing page

Static, no build step. Two languages, one shared runtime.

| File | Purpose |
| --- | --- |
| `index.html` | Arabic (RTL) — the primary version |
| `en.html` | English (LTR) |
| `support.js` | Runtime that renders both pages |
| `brand/` | Logos, wordmarks, favicons |
| `photos/` | Photography |
| `site.webmanifest` | Icons and theme colour for installed/mobile use |
| `.nojekyll` | Stops GitHub Pages from processing the folder |

## Deploy to GitHub Pages

1. Push the contents of this folder to the repository root (or to `/docs` on `main`).
2. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/` or `/docs`.
3. The Arabic page serves at the site root; English at `/en.html`.

Serve locally with any static server, e.g. `python3 -m http.server` — opening `index.html` from the filesystem works too.

## Responsive behaviour

Four tiers, matching the responsive preview:

| Width | Layout |
| --- | --- |
| < 520px | Single column, compressed spacing, mobile hero photo, full-screen menu |
| 520 – 819px | Single column cards, full-screen menu, 2×2 footer |
| 820 – 1179px | Two-column cards, full-screen menu, four-column footer |
| ≥ 1180px | Full desktop: inline nav, four-column sectors, three-column impact |

The hamburger appears below 1180px and opens a full-screen sheet whose logo and close button sit exactly where the header logo and menu button were. Horizontal scrolling is locked out at every width.

## Favicons

Declared in both pages: 32px and 512px PNGs, a 180px Apple touch icon, plus `site.webmanifest` and a `#0E0E0E` theme colour.

## Forms

The demo and contact popup is front-end only — the submit button posts nowhere. Before launch, point it at a handler (a form service, your CRM, or a WordPress endpoint) and add validation, a success state, and spam protection.

## Fonts

Almarai (Arabic) and Space Grotesk / Inter / IBM Plex Mono (English) load from Google Fonts. Self-host them if the site must work without external requests.
