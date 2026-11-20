# Inner Orrery

An emotion journal drawn as a ray-traced black hole, made for the **Kaleidoscope Project: Body, Cognition and Emotion and Their Interactions**.

Every feeling you log becomes a star orbiting a black hole. Its color is its mix of the three "beads" (body, cognition, emotion), its distance from the horizon is its intensity, and entries that share a body signature, context, baseline or trigger link up into constellations. Feelings with the same label fall into resonance and orbit together, and older signals sink slowly inward: history becomes baseline.

## What's inside

- **A real black hole.** Each pixel traces a light ray through the Schwarzschild metric in WebGL2: gravitational lensing, the lensed far side of the accretion disk, the photon ring, Doppler beaming and gravitational redshift. The wide-field bending is softened slightly so the background stays readable.
- **An explorable universe.** Feelings are placed on Russell's circumplex model of affect (valence × arousal), and each quarter is a different place: **The Horizon** (intense, unpleasant) is a black hole, **Ember Nebula** (intense, pleasant) a stellar nursery, **Tidepool** (calm, pleasant) a quiet sun with a red-dwarf companion, and **The Drift** (calm, unpleasant) a planetary nebula. The **Star map** is a spiral galaxy that plots every entry on the two axes; warp between regions from the map, the markers on the horizon, or keys 1–4 and M.
- **The seven parameters.** Each log walks through label, bodily signature, trigger, context, history and baseline, failure mode, and regulation.
- **Patterns.** Bead balance, misread rate, how baseline affects misreads, which regulation strategies lowered intensity, and recurring signatures.
- **Replay, Capture, Export and Import.**
- **Play song.** The button in the top-right corner plays a track made for this project, and the sky pulses with its beat.

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

Controls: drag or arrow keys to orbit, scroll, pinch or +/− to zoom, double-click or 0 to reset, 1–4 to travel to a region, M for the Star map.
