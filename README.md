# Inner Orrery

An emotion journal drawn as a ray-traced black hole, made for the **Kaleidoscope Project: Body, Cognition and Emotion and Their Interactions**.

Every feeling you log becomes a star orbiting a black hole. Its color is its mix of the three "beads" (body, cognition, emotion), its distance from the horizon is its intensity, and entries that share a body signature, context, baseline or trigger link up into constellations. Feelings with the same label fall into resonance and orbit together, and older signals sink slowly inward: history becomes baseline.

## What's inside

- **A real black hole.** Each pixel traces a light ray through the Schwarzschild metric in WebGL2: gravitational lensing, the lensed far side of the accretion disk, the photon ring, Doppler beaming and gravitational redshift. The wide-field bending is softened slightly so the background stays readable.
- **The seven parameters.** Each log walks through label, bodily signature, trigger, context, history and baseline, failure mode, and regulation.
- **Patterns.** Bead balance, misread rate, how baseline affects misreads, which regulation strategies lowered intensity, and recurring signatures.
- **Replay, Kaleidoscope, Capture, Export and Import.**
- **A hidden track.** Find the faint star in the top-right corner.

## Privacy

There is no server and no account. Journal entries are saved only in the visitor's own browser (`localStorage`), so every visitor gets their own private sky. Clearing site data erases it, so use **Journal → JSON** to keep a backup, and **Import** to restore it or move it to another device.

## Deploying

It is a static site with no build step. On Cloudflare Pages: framework preset **None**, build command empty, build output directory empty (the repository root). Every push to `main` deploys.

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles, shaders and script |
| `hidden-track.mp3` | The hidden track |
| `og.png` | Link preview image |
| `favicon.svg` | Tab icon |
| `_headers` | Cloudflare Pages response headers |

Controls: drag or arrow keys to orbit, scroll, pinch or +/− to zoom, double-click or 0 to reset.
