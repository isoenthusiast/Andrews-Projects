# Andrew's Projects 🚀

A collection of applications and mini-games built by **Andrew** — using **AI** as a coding companion to learn, experiment, and create.

This repository serves as a **hands-on practice space** where AI helps turn ideas into working software, from quick prototypes to fully interactive games.

## 🎮 Projects

| Project | Description |
|---|---|
| [Tic-Tac-Toe](./tic-tac-toe/) | Classic X's and O's with a scoreboard |
| [Hangman](./hangman/) | Guess the word before the stick figure is complete — 100+ kid-friendly words |
| [Clock](./clock/) | A live analog + digital clock with 12/24-hour toggle |
| [Tower Defense](./tower-defense/) | 长城守卫战 — defend the Great Wall from 20–100 waves of invaders, with save & resume |
| [Plants vs. Zombies 3](./tower-defense/) | 植物大战僵尸 3 — a lawn-defense: 28 plants, harvest sun, fuse them into 44 hybrids, and stop 20–100 waves of 20 zombie types |
| [Combined mode](./tower-defense/) | 组合模式 — the Wall and the lawn in one battle: plants, silver-funded pagoda towers, wall HP and twin bosses |
| [Level Devil](./level-devil/) | A troll platformer: 10 levels that lie, collapse and betray you on the way to the door |
| [Hangman + Level Devil](./hangman-level-devil/) | Two games, one page — word-guessing hangman and the troll platformer, with a mode picker |
| [Cubes Adventures + Evolution](./cubes-evolution/) | Two games, one page — a blocky platform adventure and a creature simulator that evolves its own brain |
| [Qube Stack](./qube-puzzle/) | A one-tap 3D cube stacker with a slowly orbiting camera |
| More coming soon... | |

All three Tower Defense games live in a single page, `tower-defense/index.html`, with a title-screen **mode picker** and a **☰ 切换游戏** button to swap between them at any time. Each game saves separately, so switching never costs you progress. Each of them also has a **总波数 (Total waves)** slider in its 波次 · WAVE panel, so a run can be anywhere from **20 to 100 waves in steps of 10** — every 20-wave block adds a difficulty tier.

Hangman and Level Devil also share `hangman-level-devil/index.html` — the same mode-picker pattern, with **☰ Switch game** to swap between them.

Cubes Adventures and Evolution likewise share `cubes-evolution/index.html`, with **☰ Switch game** to swap between them. (Evolution loads its Matter.js physics engine from a CDN, so it needs an internet connection.)

## 🛠️ Tech Stack

- **Runtime:** Node.js
- **Language:** HTML, CSS, JavaScript (vanilla)
- **Version Control:** Git + GitHub

## 🎯 Purpose

- Practice building real applications with AI assistance
- Explore different game mechanics and UI designs
- Keep a growing portfolio of mini projects
- Have fun while learning to code!

---

*Built with 💻 and 🤖*
