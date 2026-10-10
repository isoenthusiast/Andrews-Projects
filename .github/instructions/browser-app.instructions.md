---
description: "Use when creating or editing a single-file browser app or game page (index.html) in this repo. Covers the required HTML skeleton, the shared dark theme, canvas game-loop shape, localStorage key naming, WebAudio, and touch support."
applyTo: "**/index.html"
---

# Single-file browser app conventions

Every project here is one self-contained page. It must run by double-clicking `index.html` over
`file://` — no server, no build step, no bundler, no framework, no npm dependencies.

## Page skeleton

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Game Name</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }

        :root {
            --gold1: #f7971e;
            --gold2: #ffd200;
            --muted: #a0a0c0;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            color: #fff;
            user-select: none;
            -webkit-user-select: none;
            -webkit-tap-highlight-color: transparent;
        }
    </style>
</head>
<body>
    <!-- markup -->
    <script>
        // logic
    </script>
</body>
</html>
```

- Keep CSS in the inline `<style>` and JavaScript in the inline `<script>`. Do not use
  `<script type="module">` and do not split into separate `.css` / `.js` files.
- Use `lang="en"` normally. Use `lang="zh-CN"` only for a Chinese-first app, and then add
  `'Microsoft YaHei'` to the font stack (see `tower-defense/index.html`).

## Theme

Reuse the existing dark theme instead of inventing a new one:

| Role | Value |
|---|---|
| Accent | `--gold1: #f7971e` and `--gold2: #ffd200` (gradients use both) |
| Muted text | `--muted: #a0a0c0` |
| Page background | purple-dark — `linear-gradient(135deg, #0f0c29, #302b63, #24243e)` or flat `#08061a` |
| Body text | `#fff` |
| Font | `'Segoe UI', system-ui, -apple-system, sans-serif` |

A deliberate different art direction is acceptable when the game calls for it
(`tower-defense/` uses an ink-and-parchment palette), but keep the same structure and contrast.

## Interaction

- Support both keyboard and touch/pointer input. Put `touch-action: none` on canvases and handle
  pointer events rather than mouse-only handlers.
- Avoid hover-only affordances, and keep hit targets large enough for a finger.
- Provide a restart control, and an explicit HUD whenever there is a score, level or progress.

## Game loop

Animated games draw to a `<canvas>` and drive updates from `requestAnimationFrame` with delta
time, so speed does not depend on frame rate:

```js
let last = 0;
function frame(t) {
    const dt = Math.min((t - last) / 1000, 0.05); // clamp so a tab switch doesn't teleport
    last = t;
    update(dt);
    draw();
    requestAnimationFrame(frame);
}
requestAnimationFrame(frame);
```

## Persistence

Prefix every storage key with the folder name:

| Data | Key |
|---|---|
| Progress or save state | `<folder-name>` |
| High score or best | `<folder-name>-best` |

- Wrap storage access in `try/catch` — it can be unavailable or blocked in private modes.
- Apps with a save system probe for availability first, as `tower-defense/` does.

## Audio

Build the `AudioContext` lazily on the first user gesture, never on page load, and always give the
player a mute toggle that persists with their other settings.

## Related

- Multi-game pages: [collection-pages.instructions.md](./collection-pages.instructions.md)
- Documentation: [project-docs.instructions.md](./project-docs.instructions.md)
