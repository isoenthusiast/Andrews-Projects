---
description: "Scaffold a complete new browser game or app: folder, index.html, package.json, plus README and INSTRUCTIONS entries"
argument-hint: "Describe the game, e.g. 'a snake game with power-ups'"
agent: "agent"
---

Build a new self-contained app for this repo from this idea:

> ${input:gameIdea:Describe the game or app you want}

Work through the whole pattern. A new app is not finished until every step is done.

1. **Name it.** Choose a kebab-case folder name in the repo's style (`ball-physics`,
   `tower-defense`). Ask me if the idea is ambiguous or would collide with an existing folder.
2. **Create `<folder>/index.html`** following
   [browser-app.instructions.md](../instructions/browser-app.instructions.md) — the required
   skeleton, the shared dark theme, inline CSS and JS, keyboard *and* touch controls, a restart
   control, and `requestAnimationFrame` with delta time if it animates. No build step, no bundler,
   no dependencies; ask me before adding a CDN `<script src>`.
3. **Create `<folder>/package.json`** matching the siblings exactly — `name`, `version: "1.0.0"`,
   a one-line `description`, and `"private": true`. No dependencies and no scripts.
4. **Persist state** under `<folder-name>` (and `<folder-name>-best` for a high score) if there is
   progress worth keeping.
5. **Update `README.md`** — add one row per game to the project table in the existing format.
6. **Update `INSTRUCTIONS.md`** — add a `## <Name>` section with Location, How to Play or How to
   Use, a Controls table, and Features, following
   [project-docs.instructions.md](../instructions/project-docs.instructions.md).
7. **Verify** by opening `index.html` in a browser and actually playing it. Report the file paths
   you created and how you checked it. There is no test suite, linter or build command to run.

If the idea is really two or more games sharing one page, also follow
[collection-pages.instructions.md](../instructions/collection-pages.instructions.md).

Do not commit anything unless I ask.
