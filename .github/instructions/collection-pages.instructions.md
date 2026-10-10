---
description: "Use when building a page that hosts two or more games behind a title-screen mode picker and an in-game switch button, or when editing cubes-evolution, hangman-level-devil or tower-defense."
---

# Multi-game collection pages

Three pages host more than one game in a single `index.html`: `cubes-evolution/`,
`hangman-level-devil/` and `tower-defense/`. Follow the established shape.

## Structure

- A title-screen picker overlay lists each game as a card, and the games themselves start hidden.
- One `<button id="switchBtn" hidden>☰ Switch game</button>` sits at the bottom-right, visible
  only while a game is running, and returns the player to the picker. Use `☰ 切换游戏` in the
  Chinese-first `tower-defense/` page.
- Only the active game may run its loop, animation frames and timers. Stop them when switching
  away and rebuild or resume state on return — never let two games tick at once.

## Picker markup

Reuse the `pk-*` class names so every picker looks the same:

| Class | Purpose |
|---|---|
| `pk-grid` | Card container |
| `pk-card` | One card per game |
| `pk-name`, `pk-en` | Game title, plus its English or Chinese counterpart |
| `pk-desc`, `pk-tag` | One-line description, and a short feature tag |
| `pk-go` | Start button |
| `pk-foot`, `pk-note`, `pk-sub` | Footer hint, caveat, and subheading |

## Separate saves

Each game owns its own storage key, so switching never costs progress, and a manual save should
capture mid-run state — `tower-defense/` restores enemies mid-march. Document the picker in both
`README.md` (one row per game, plus a paragraph on the picker) and `INSTRUCTIONS.md`.

## Related

Follow [browser-app.instructions.md](./browser-app.instructions.md) for the page skeleton, theme,
storage and audio conventions.
