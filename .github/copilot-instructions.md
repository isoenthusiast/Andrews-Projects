# Project Guidelines

Andrew's Projects is a growing collection of small browser games and tools, built with AI as a
coding companion. Every project is a **self-contained single-file web app** — that is the defining
constraint of this repo.

## Architecture

- One folder per project at the repo root, named in kebab-case (`tetris/`, `tower-defense/`).
- Each folder contains `index.html` (markup, CSS and JS all inlined) and usually a
  metadata-only `package.json`.
- **No build step, no bundler, no framework, and no npm dependencies.** A page must work when
  `index.html` is opened directly from disk over `file://`.
- The only permitted external code is a version-pinned CDN `<script src>` (see Matter.js in
  `evolution/`), used only when a feature genuinely needs it. Ask before adding one.

## Conventions

- Reuse the existing dark theme rather than inventing a new one.
- Persist state to `localStorage` as `<folder-name>`, and high scores as `<folder-name>-best`.
- All files are UTF-8. Some apps mix Chinese and English text — never change the encoding.
- Documentation is part of the deliverable: a new app must be added to both `README.md` and
  `INSTRUCTIONS.md`.

## Build and test

There is nothing to build, lint, or run. `package.json` files declare no `scripts` and no
dependencies — they exist for metadata only. Verify a change by opening the page in a browser and
playing it.

## Detailed conventions

- [browser-app.instructions.md](./instructions/browser-app.instructions.md) — page skeleton, theme,
  game loop, storage and audio patterns for any `index.html`.
- [collection-pages.instructions.md](./instructions/collection-pages.instructions.md) — pages that
  host several games behind a mode picker.
- [project-docs.instructions.md](./instructions/project-docs.instructions.md) — `README.md` and
  `INSTRUCTIONS.md` structure.
- [new-game](./skills/new-game/SKILL.md) — a skill that scaffolds a whole new app end to end.
