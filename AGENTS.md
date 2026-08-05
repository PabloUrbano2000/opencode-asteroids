# AGENTS.md

Vanilla HTML5 Canvas Asteroids clone. No build step, no dependencies, no tests, no linter — do not introduce npm/bundlers.

## Run / verify
- Open `index.html` directly, or `npx serve .` → http://localhost:3000.
- There are no test/lint commands; verification is manual in the browser (move, shoot, destroy asteroids, check HUD and respawn).

## Layout
- `game.js` — all game logic in one file, loaded via a plain `<script>` tag. It is **not** an ES module: no `import`/`export`.
- `index.html` — canvas + inline CSS. `favicon.svg` — favicon only.

## Gotchas
- Canvas size is hardcoded twice: `W`/`H` constants in `game.js` and the `width`/`height` attributes in `index.html`. Keep in sync; `spawnAsteroids` reserves a 130px safe radius around `W/2, H/2`.
- HUD/UI copy is Spanish (`NIVEL`, `GAME OVER`, README too). Keep new UI text in Spanish.
- Asteroid `size` is 3 = grande, 2 = mediano, 1 = pequeño. `RADII`, `SPEEDS`, `POINTS` are indexed by size; `POINTS` descends (`[0, 100, 50, 20]`) — smaller asteroids score more.
- Input uses `KeyboardEvent.code` (`Space`, `ArrowUp`, …), not `e.key`.
- Entities use a `dead` flag; each frame `update()` filters them. Splits from collisions are collected and concatenated after the loop — don't add to `asteroids` while iterating.
