# Voxel World

A single-file, Minecraft-style voxel world that runs in any modern browser. First-person
controls with gravity, jumping, and surface collision so you always run *on top* of the
terrain. Built with [three.js](https://threejs.org/) — no build step, no dependencies to install.

## Play

Just open `index.html` in a browser, or host it for free with **GitHub Pages**:

1. Push this folder to a GitHub repo.
2. Repo **Settings → Pages → Build from branch**, pick your branch and `/ (root)`.
3. Open the published URL.

## Controls

**Desktop**
- `WASD` move · mouse look (click to lock) · `Space` jump
- `Ctrl` sprint · `Shift` sneak (won't walk off ledges) · `Esc` pause
- `1`–`8` swap the world texture

**Mobile / touch**
- Left thumb = joystick (push to the rim to sprint)
- Drag the right side of the screen to look
- Jump button, bottom-right

## Features

- **World types** — Hills, Flat, and Island, regenerated procedurally on each pick.
- **Whole-world retexture** — eight block types (grass, dirt, stone, cobble, brick, sand, planks, snow) from the bottom hotbar.
- **Skin loader** — load a standard Minecraft skin PNG; its right arm shows as your first-person arm.
- Procedural pixel-art textures generated at runtime, so there are no external assets.

## Tech notes

Everything lives in `index.html`: heightmap world generation, a merged-geometry mesh
with a 2-slot texture atlas, axis-resolved surface collision with auto-step and edge
walls, and a separate overlay pass for the first-person arm. three.js is loaded from a CDN.
