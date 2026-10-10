# 🧬 Evolution — Creature Simulator (Browser Recreation)

A single-page recreation of [Keiwan's *Evolution*](https://keiwan.itch.io/evolution) — the sandbox where you build a creature and let a **neural network + genetic algorithm** teach it to run.

**Open `index.html` in any browser.** No server or build tools needed. (Uses Matter.js physics from a CDN — needs internet on first load.)

---

## How to use

### 1. Build a creature (Build mode)

Tools (keyboard shortcuts in brackets):

| Tool | What it does |
|---|---|
| ⬤ Joint (`J`) | Click the canvas to place a joint (a little weighted ball) |
| 🦴 Bone (`B`) | Click **2 joints** to connect them with a rigid bone |
| 💪 Muscle (`M`) | Click **2 bones** to add a muscle between them |
| ✋ Move (`V`) | Drag a joint to reposition it |
| 🧽 Erase (`E`) | Click a joint / bone / muscle to delete it |

**Important — how muscles work (just like the real game):**
- A muscle connects two **bones** and pulls/pushes their **centers**.
- Put the muscle **across a joint** — e.g. connect the thigh bone to the shin bone so pulling their centers together **bends the knee**. A muscle from hip to foot also works.
- One muscle per joint is enough (they both contract *and* expand).
- Scroll to zoom, drag the empty canvas to pan.

**Presets:** two starting bodies are included —
- 🦕 **4-leg runner** — low, wide, stable.
- 🦘 **Hopper** — a compact body with legs; easier for the brain to learn a bouncing run.

### 2. Run evolution (Simulate mode)

- **Task** — pick what the creatures learn:
  - 🏃 **Run** — go as far right as possible
  - ⬆️ **Jump** — jump as high as possible
  - 🕊️ **Fly** — get high *and* stay off the ground
- **▶ Start Evolution** — spawns a population, simulates, scores each by the task, then evolves the brains (tournament selection → crossover → mutation) and repeats.
- **Speed** — 1× to 24× (faster = more generations per second).
- **Population** — more creatures = more variety (and slower per generation).
- **Sim time / gen** — how many seconds each creature runs per generation.
- **Mutation rate** — lower = fine-tune, higher = explore more.
- **Hidden layer(s)** — network size, e.g. `10` or `8,6`. Bigger is not better!
- **Clock input** — gives the brain a sense of time so it can learn periodic gaits. Keep it on.

### 3. The goal

Fitness is measured per task (same formulas as the real game):
- **Run:** distance ÷ (55 m × sim time) → 100% ≈ 5.5 m/s
- **Jump:** max height ÷ 20 m
- **Fly:** (max height ÷ 40 m + fraction of time airborne) ÷ 2

Watch the **best creature** (the camera follows it), check the **stats panel** for best fitness / distance / height, and let it run for as many generations as you can. The creatures start slow and wobbly, then evolve into crawlers and hoppers.

---

## Tips for the competition

1. **For "furthest":** use a stable, low creature (the 4-leg runner) and crank up **sim time** — a creature that never falls over wins the long game.
2. **For "fastest":** the hopper tends to learn quicker bursts; try longer legs and lighter joints.
3. **For jumping/flying:** build a dedicated design — a tall, springy body with big muscles for jumping; a wide, flappy one for flying (stay airborne!).
4. Let it evolve with **population ~20** and mutation ~0.15, then drop mutation when it plateaus.
5. **Save the winning setup:** your creature design + settings are all in the editor — screenshot it or rebuild it for the final run.

## Faster learning

The GA uses **tournament selection**, elitism, gentle mutation with occasional big jumps, random re-seeds to escape local optima, and a forward-only movement bonus — so early generations learn much quicker than before. Idle creatures also go to sleep, so more generations fit into the same time.

## Notes

- This is a physics + neuroevolution demo, not a full clone — expect wobbly first generations. The brain only evolves (network weights), not the body; **your body design is what matters most**.
- The physics is stable and the sim is fully offline-capable except for the Matter.js CDN.
