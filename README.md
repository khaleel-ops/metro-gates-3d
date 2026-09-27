# Metro Gates 3D

An interactive 3D subway fare-gate scene in the browser. Hover a yellow card reader with the swipe-card cursor, click to tap in, and watch the glass gates swing open.

**Live:** https://khaleel-ops.github.io/metro-gates-3d/

## Controls

- **Mouse:** hover a yellow reader, click to tap your card
- **Keyboard:** `1` `2` `3` tap gates 1–3 (hidden buttons are also available to screen readers)
- Respects `prefers-reduced-motion`

## How it's built

A single static `index.html` — no build step, no image assets. Every texture (tile, concrete, riveted steel, signage, screens) is drawn procedurally on canvas.

- **Three.js** renders the station: area-lit fluorescent tubes, a reflective floor, bloom and a custom film-grade pass
- **GSAP** owns the render loop and drives every animation (gate swings, reader feedback, camera intro and parallax, card cursor)
- **HTML/CSS** layer for the card cursor, live gate labels and HUD

Libraries load from jsDelivr, so the page needs an internet connection.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
