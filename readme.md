# Dots & Daubs

Turn a photo into a paintable abstraction. Drop in a photograph and reduce it
to shapes — then export the result as an SVG, a PNG, or a numbered
painter's guide you can take to the easel.

The whole tool is a single self-contained page: `index.html`. Open it in a
browser (double-click it, or `npx serve .`) and it works entirely
client-side — photos never leave your machine.

## Styles

- **Dot grid** — a halftone-style grid of dots; dot size can follow
  brightness (dark = big or light = big), with jitter to loosen the grid.
- **Mosaic** — rigid tiles with adjustable grout gap and corner radius,
  colored by the average or the dominant color of each cell.
- **Quadtree** — squares that recursively subdivide where the photo has
  detail, so resolution is spent where the image is interesting.
- **Voronoi** — organic cells (or packed stipple dots) seeded randomly or
  clustered onto detailed areas.

## Shared controls

- **Limit palette** — median-cut quantization down to 2–16 colors, shown as
  numbered swatch chips (mix that many pots of paint).
- **Shape fill** — solid, or a per-shape linear gradient sampled from the
  photo at an adjustable angle.
- **Saturation**, background (paper / white / black / average / custom),
  and a **seed shuffle** for reproducible randomness.

## Exports

- **SVG** — resolution-independent, for digital use.
- **PNG** — 2400 px render.
- **Painter's guide** — the same composition as numbered outlines plus a
  palette legend with hex values: generative paint-by-numbers of your own
  photo.

---

This repo previously held a pebble {code} Slack brand-police bot; it has
been retired. (Its Slack token still exists in git history and should be
treated as revoked.)
