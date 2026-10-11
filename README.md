# untitled — portfolio

Static portfolio site. No framework, no build step: open `index.html` or serve
the folder with any static server.

```
index.html          home — hero, work entries, how-I-work, contact
soldbycaleb.html    case study 01 — Shopify archive storefront
ablelion.html       case study 02 — static build-log site
style.css           shared design system (tokens, nav, cards, arch windows)
previews/sbc/       standalone rebuild of the SOLDBYCALEB homepage
previews/ablelion/  copy of the live ableLion site
```

## Look

Light gothic. Parchment field (`#f3f0e9`), near-black ink with a violet cast,
a single oxblood accent (`#7a1f2b`). Pirata One for the wordmark, drop caps
and numerals; Cormorant Garamond for display; EB Garamond for body and the
letter-spaced small-caps labels. Structure borrows from manuscript pages —
double rules, fleurons, centred section heads.

The work previews sit in **lancet-arch windows**: an SVG mask cuts the
pointed arch, and a second SVG draws the tracery (outline, mullion, sub-arch)
over the top.

## Previews

The work entries embed the real sites in iframes instead of using screenshots,
so they never go stale against a design change.

- `previews/ablelion/` is a straight copy of the ablelion repo (HTML + CSS +
  resized dashboard screenshots).
- `previews/sbc/` is a standalone rebuild of the current SOLDBYCALEB homepage
  — the Shopify theme is Liquid and needs a store to render, so the homepage
  was rebuilt as plain HTML/CSS/JS off the live theme files
  (`assets/custom.css`, `sections/*.liquid`, `templates/index.json`) and the
  real product photography. Refresh it whenever the theme changes.

Images in `previews/sbc/` are resized copies of the theme's `archive-*.png`,
`hero.png` and `lookbook.png`.

## Run it

```
python3 -m http.server 4321
```

Then open http://localhost:4321.

## Deploy

Push to GitHub and turn on Pages (branch: `main`, folder: `/`). Everything is
relative-path, so it works from a subdirectory too.
