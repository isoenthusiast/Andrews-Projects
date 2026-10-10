---
description: "Use when documenting a project in README.md or INSTRUCTIONS.md — adding a game to the project table, writing a how-to-play section, or updating docs after a feature change."
applyTo: ["README.md", "INSTRUCTIONS.md"]
---

# Documentation conventions

Two root files document the collection. Keep both in sync whenever a project is added, renamed, or
gains a feature. Both are UTF-8; preserve the emoji and the Chinese titles.

## README.md

The project table is the index. Match the existing row format exactly:

```markdown
| [Tetris](./tetris/) | Classic block-stacking game with hold and level tracking |
```

- Link with `./<folder>/` and describe the project in one short sentence, with no trailing period.
- Keep the `| More coming soon... | |` row last.
- A page hosting several games gets **one row per game**, each pointing at the shared folder, plus
  a short paragraph below the table explaining the mode picker.
- Mention a CDN dependency only when the app has one, as the Evolution row does.

## INSTRUCTIONS.md

One section per project, separated by `---`:

```markdown
## Tetris

**Location:** `tetris/index.html`

### How to Play
- Open `tetris/index.html` in any browser.
- ...rules and objective, in the order the player meets them...

### Controls
| Action | How |
|---|---|
| Move | Press **←** / **→** |
| Pause | Press **Space** |

### Features
- What makes it interesting, as a bullet list.
```

- Use `### How to Use` rather than `### How to Play` for non-game apps such as Clock.
- Add `### Saving your game` when progress persists, and `### Tips` when strategy helps.
- Write controls as an `| Action | How |` table, bolding key names and button labels.
- End the file with the shared `## Running the Games` section.
