# Inner Orrery

An emotion journal you can fly through, made for the **Kaleidoscope Project: Body, Cognition and Emotion and Their Interactions**.

Every feeling you log becomes a star. Its color mixes the three "beads" of the kaleidoscope (body, cognition, emotion), its distance from the center is its intensity, and entries that share a body sensation, a context, a baseline or trigger words link up into constellations. Feelings with the same name fall into resonance and orbit together, and older entries sink slowly inward: history becomes baseline.

Live at **https://inner-orrery.pages.dev**

## How it works

1. **Log a feeling.** Eight short questions walk through the seven parameters from class (label, bodily signature, trigger, context, history and baseline, failure mode, regulation) plus how loud each bead was. Only the name is required.
2. **It lands in a region of space.** Each feeling is placed on Russell's circumplex model of affect, by valence (unpleasant to pleasant) and arousal (calm to intense), and each quarter is its own place:

   | Region | Feelings | What is there |
   | --- | --- | --- |
   | The Horizon | intense, unpleasant | a black hole |
   | Ember Nebula | intense, pleasant | a stellar nursery around a young cluster |
   | Tidepool | calm, pleasant | a sun with a red-dwarf companion |
   | The Drift | calm, unpleasant | a planetary nebula around a white dwarf |

3. **Patterns form.** The Patterns view says in plain sentences what the entries show (how baseline changed misreads, each feeling's bodily signature, what lowered intensity), charts intensity before and after each entry, and breaks down the beads, regions, reads and regulation.

## Features

- **Real physics.** The black hole is ray-traced through the Schwarzschild metric in WebGL2: gravitational lensing, the lensed far side of the disk, the photon ring, Doppler beaming and gravitational redshift. Journal stars behind it are lensed too. The nebulae are volumetric; the planets are lit by each region's light.
- **Star map.** A spiral galaxy plots every entry on the two circumplex axes, with trails joining feelings of the same name from oldest to newest.
- **Journal.** Search, filter by region or misreads, sort, edit, delete with undo, and replay the whole sky in order.
- **Project report.** Patterns → Export project report saves a printable HTML summary with a picture of the sky, the framework, the insights and every entry.
- **Sound.** A generative score plays quietly and changes key and mood with each region, with soft sounds for exploring. The Play song button in the top-right corner plays a track made for this project and swaps the page for a picture while it plays.
- **Settings.** Visual quality (including a flat, non-3D view), motion, shortcut keys, sound, and your data.
- **Resilient.** If the 3D view is lost or a device cannot keep up, the page switches to a lighter view and recovers when it can.
- **Accessible.** Keyboard reachable, screen-reader labels and a skip link, reduced-motion support, and no axe-core violations.

## Privacy

There is no server and no account. Entries are saved only in the visitor's own browser (`localStorage`), so every visitor gets a private sky. Clearing site data erases it; use **Journal → JSON** to back up and **Import** to restore or move to another device. The journal reminds you when a backup is due.

## Controls

Drag or arrow keys to orbit · scroll, pinch or +/− to zoom · double-click or 0 to reset · 1–4 to travel to a region · M for the star map · Escape to close.

## Deploying

A static site with no build step. On Cloudflare Pages: framework preset **None**, build command empty, build output directory empty (the repository root). Every push to `main` deploys.

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles, shaders and script |
| `hidden-track.mp3` | The song behind Play song |
| `keys.jpg` | The picture shown while the song plays |
| `og.png` | Link preview image |
| `favicon.svg`, `icon-*.png`, `manifest.webmanifest` | Icons and home-screen install |
| `_headers` | Cloudflare Pages response headers |
