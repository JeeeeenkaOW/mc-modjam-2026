# ModJam 2026 Teaser

A first-person, Minecraft-style teaser experience that runs in any modern browser.
Explore a foggy voxel world by torchlight, collect the letters **JULY 21**, and a
towering T-rex looms out of the mist with a thunderclap. Built with
[three.js](https://threejs.org/) — no build step, no install.

## Structure

```
.
├── index.html   ← the whole experience (three.js + world + logic, all inline)
└── sfx/         ← audio (ambient music + SFX), loaded at runtime
```

The audio lives in `sfx/` as separate files (small page, fast load). Because the page
fetches those files, **it must be served over HTTP — don't open `index.html` by
double-clicking** (browsers block `file://` fetches, so the SFX won't play locally).
Use any static server, or just deploy it (below).

## Deploy (Netlify)

It's a static site — no build command, no framework.

1. Push this folder to a GitHub repo.
2. In Netlify: **Add new site → Import from GitHub**, pick the repo.
3. Leave **build command** empty and set **publish directory** to `/` (the repo root).
4. Deploy. That's it.

## Controls

**Desktop** — `WASD` move · mouse look (click to lock) · `Space` jump
**Mobile** — left thumb joystick to move · drag the right side to look · Jump button

Sound starts on the first tap/click (browsers require a user gesture for audio); toggle
it with the **SOUND** control top-right, or the `M` key.

## Notes

- Everything is in `index.html`; the only external files are in `sfx/`.
- three.js is bundled inline, so there are no other dependencies.
