# INKWIRE — political cartoons

A minimalist, single-page website for a political-cartoon desk. Static HTML, CSS and a little JavaScript — no build step, no dependencies, no tracking. All artwork is original inline SVG, so the page works offline and adapts to light and dark themes automatically.

## Stack

- `index.html` — the whole page, with hand-drawn inline SVG illustrations
- `styles.css` — the design system (tokens, type, grid, components)
- `assets/favicon.svg` — the mark
- Google Fonts: Newsreader (display), IBM Plex Sans (text), IBM Plex Mono (labels)

## Design system

The visual language combines two approaches:

- **Swiss International Style** — a 12-column grid, generous whitespace, opacity-based hierarchy, one accent colour, rectilinear geometry, narrow body measure.
- **Editorial minimalism** — a warm monochrome palette (bone canvas, charcoal ink), extreme typographic contrast, a 1px hairline border system, restrained motion.

Tokens live at the top of `styles.css`. The palette is warm monochrome plus a single editorial-red accent used only for marks, tags and links. Dark mode follows the operating system and can be overridden with the header toggle (the choice is remembered).

## Accessibility

- Semantic landmarks, a skip link, and labelled controls
- Visible `:focus-visible` rings
- `prefers-reduced-motion` disables the scroll-reveal animation
- `color-scheme: light dark` and warm near-black (never pure black) in dark mode
- Text on the `--ink-70` / `--ink-40` rungs keeps contrast against the canvas

## Run locally

Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

This is a GitHub Pages site. Push the repository, then set **Settings → Pages → Source** to the branch root (or run the included workflow). No build output is required.

## Licence

Code: MIT. The cartoons are original work — free to republish with credit.
