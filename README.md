# DexT2 — EgoSuite-Style GitHub Pages Website

A static website for **DexT2** modeled after [lightwheel.ai/media/egosuite-open100k](https://lightwheel.ai/media/egosuite-open100k), ready for direct deployment to GitHub Pages (`github.io`).

## Features

1. **Full-Screen 4×7 Egocentric GIF Hero Wall**:
   - Uses **28 distinct tasks** (out of the 29 `candidate = yes` & `not withdrawn` tasks; only `Pick up pipette` is omitted because all of its episodes are `< 5.3s`).
   - Each cell displays a **5-second egocentric GIF starting at `3.0s` (`3.0s–8.0s`)**, showing both hands actively interacting with objects.
   - Sticky hero scroll transition: at the top (`scrollY = 0`), the 4×7 GIF grid fills the screen unobstructed; scrolling down smoothly fades in the dark translucent title overlay before transitioning into the article body.
   - Includes header quick-toggles (`Show Task Labels` and `Title Overlay`) and hover badges on each grid cell.
2. **Article Sections with Placeholders**:
   - Follows the section hierarchy, typography, and gradient link styling of `lightwheel.ai/media/egosuite-open100k`, using structured placeholder paragraphs ready to be replaced with final copy.
3. **28-Task Episode Index Manifest**:
   - Full mapping of grid slot (`R1C1`–`R4C7`), task name, `session_id`, `episode_index`, `episode_id`, video source path, and exported OXT `.zarr` path in `assets/gifs/manifest.json`.

## Regenerating the 28 GIFs

```bash
.venv-module5/bin/python Dex-T2-website/scripts/generate_grid_gifs.py
```
