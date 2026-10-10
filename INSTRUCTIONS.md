# Andrew's Projects — Game Instructions

## Tic-Tac-Toe

**Location:** `tic-tac-toe/index.html`

### How to Play
- Open `tic-tac-toe/index.html` in any browser.
- **Player X** goes first, then **Player O**.
- Click any empty square to place your mark.
- Get **three in a row** (horizontally, vertically, or diagonally) to win.
- If all 9 squares fill up with no winner, the game is a draw.

### Controls
| Action | How |
|---|---|
| Place mark | Click an empty cell |
| New game | Click the **New Game** button or press **R** key |
| Reset scores | Double-click the logo area (or refresh the page) |

### Features
- Scoreboard tracks wins for X, O, and draws.
- Winning cells highlight with a pulsing green glow.
- Modern dark gradient theme.

---

## Hangman

**Location:** `hangman/index.html`

### How to Play
- Open `hangman/index.html` in any browser.
- A hidden word is shown as blank spaces `_ _ _ _`.
- A **hint** is displayed below the word (e.g. 💡 *White frozen flakes from the sky*).
- Click a letter on the on-screen keyboard — or press it on your **physical keyboard**.
  - ✅ **Correct guess** — the letter fills in all matching blanks.
  - ❌ **Wrong guess** — one part of the hangman is drawn.
- Guess the word before the **stick figure is complete** (6 wrong guesses max).

### Controls
| Action | How |
|---|---|
| Guess a letter | Click the letter button or press the key on your keyboard |
| New word | Click **New Word** button or press **Enter** |
| Reset scores | Click **Reset Scores** button |

### Features
- **100+ kid-friendly words** (2 syllables or less) with helpful hints.
- Visual hangman drawn step-by-step on a canvas.
- Scoreboard tracks wins and losses.
- Letters turn green (correct) or red (wrong).
- Words are not repeated until all have been used.

---

## Clock

**Location:** `clock/index.html`

### How to Use
- Open `clock/index.html` in any browser.
- A live **analog clock** is drawn on a canvas, with the current time shown **digitally** below it.
- The date is displayed above the clock.

### Controls
| Action | How |
|---|---|
| Switch 12-hour / 24-hour | Click the **12-hour / 24-hour** button |
| Show / hide seconds | Click the **Seconds on / off** button |

### Features
- Smooth sweeping second hand with a glow effect.
- Numbers and tick marks on the analog face.
- Matches the same dark theme as the other games.

---

## Game Collection — 长城守卫战 + 植物大战僵尸 3 + 组合模式

**Location:** `tower-defense/index.html`

Three games share this one page. Opening it shows a **title screen with a mode picker** — one card per game, each showing that game's current save (wave and resources) or *暂无存档*.

| Action | How |
|---|---|
| Start a game | Click its card on the title screen |
| Continue | If that game has a save, clicking its card resumes it straight away |
| Switch games | Click **☰ 切换游戏** (bottom-right corner) at any time |
| Keep progress | Each game saves separately, so switching never costs you anything |

Only one game is mounted at a time, so the three never interfere. Everything below applies to each game individually.

---

## Tower Defense — 长城守卫战 (Great Wall Defense)

**Location:** `tower-defense/index.html` — pick 长城守卫战 on the title screen.

### How to Play
- Open `tower-defense/index.html` in any browser.
- Invaders march down the ancient road toward the **Great Wall gate** on the right.
- Build **pagoda towers** on the empty ground beside the road. Every tower covers a circular **range** — place them so the road passes through it.
- Kill invaders to earn **silver** (银两). You start with 150 silver and 20 points of **wall** (城墙).
- If an invader reaches the gate, you lose wall. A normal enemy costs 1 wall, a boss costs 5.
- **Survive all 20 waves** to win. Lose all your wall and the city falls.
- Waves 10 and 20 bring **bosses** — the 将军 (General) and the 龍 (Black Dragon).

### Towers
| Tower | Cost | Role |
|---|---|---|
| 箭塔 Archer Tower | 50 | Fast single-target damage — best value early |
| 火炮台 Fire Cannon | 100 | Slow, high damage, **splash** — great against crowds |
| 寒冰塔 Frost Pagoda | 75 | **Slows** enemies so other towers get more shots |
| 雷龙塔 Dragon Lightning | 150 | **Chain lightning** hits several enemies at once |

Each tower can be upgraded twice (max level 3). Upgrades add a storey to the pagoda and boost damage, range, and fire rate.

### Enemies
| Enemy | Trait |
|---|---|
| 流寇 Raider | Standard foot soldier |
| 快马 Fast Rider | Nearly twice as fast — priority target |
| 盾兵 Shield Trooper | High HP and armour, shrugs off small hits |
| 邪僧 Wicked Monk | Balanced, arrives in large groups |
| 將 General | **Boss** — wave 10 |
| 龍 Black Dragon | **Final boss** — wave 20 |

### Controls
| Action | How |
|---|---|
| Select a tower to build | Click its card in the sidebar, or press **1**–**4** |
| Build | Click any empty ground cell |
| Upgrade / sell | Click a built tower, then **升级** (upgrade) or **拆除** (sell) |
| Cancel | Press **Esc** or **right-click** |
| Pause | Press **Space** or click **暂停** |
| Start next wave early | Click the button while it counts down — **earns bonus silver** |
| Game speed | **1×** / **2×** / **3×** buttons |
| Sound on/off | **🔊 音效** button |
| Save / load | **保存进度** (save) and **读取存档** (load) buttons |
| Restart | **重新开始** button |

### Saving your game
Your progress is **saved automatically** to the browser's local storage, so you can close the tab and pick up later.

- **自动保存** — a checkpoint is written every time a wave is cleared, and shortly after you build, upgrade or sell a tower.
- **保存进度** — save right now (you can save mid-wave, with invaders on the road).
- **读取存档** — restore the saved game. Because this replaces your current run, the button asks for a **second click to confirm**.
- **清除存档** — delete the save.
- When you reopen the game, the title screen shows your saved wave, silver and wall, with a **继续上一局** (continue) button.
- Tower positions, upgrades, silver, wall, the current wave, and even enemies mid-march are all restored exactly.
- Finishing or losing a run clears the save. **重新开始** (restart) also clears it.
- Your **game speed** and **sound** settings are remembered separately.

### Tips
- Bounty silver grows with each wave, so late waves pay much more — spend early, spend often.
- Frost towers don't do much damage, but slowing enemies keeps them inside every other tower's range.
- Upgrade a few towers in strong spots before spreading thin — a level 3 tower is worth several level 1s.

### Features
- Ancient Chinese **scroll-map** visual theme — parchment terrain, ink-wash mountains, a red sun, and cloud scrolls.
- Canvas-rendered **pagoda towers** that gain a new roof tier with each upgrade.
- 4 tower types with splash, slow, and chain-lightning mechanics.
- 20 hand-tuned waves with two boss encounters.
- **Save & restore** — automatic checkpoints plus manual save/load via browser local storage, including mid-wave state.
- Procedural audio effects (WebAudio) with a mute toggle.

---

## Plants vs. Zombies 3 — 植物大战僵尸 3

**Location:** `tower-defense/index.html` — pick 植物大战僵尸 3 on the title screen.

The second game of the collection: a lane-defense built on the same single-file canvas architecture and the same save/load and speed/sound settings, but around the classic 5-lane / 9-column lawn.

### How to Play
- Open `tower-defense/index.html` in any browser and pick **植物大战僵尸 3** on the title screen.
- Zombies crawl in from the right. If one reaches the house on the left, you lose.
- Plant on the **5 × 9 lawn**. Each row has one **割草机 (lawn mower)** that fires automatically the first time a zombie breaks through — a one-time save per row.
- **阳光 (sun)** is your currency. It falls from the sky and pops out of sunflowers — click a sun to collect it, or hire the **兔子园丁 (rabbit gardener)** and let it run around hoovering them up.
- Survive all **20 waves**. Wave 10 brings a **巨人僵尸 (Gargantuar)**, wave 20 the **僵尸博士 (Zomboss)** — who also calls in reinforcements while he advances.

### Plants
| Plant | Cost | Role |
|---|---|---|
| 向日葵 Sunflower | 50 | Produces 25 sun every 11 s — build these first |
| 豌豆射手 Peashooter | 100 | Fires one pea down its lane |
| 坚果墙 Wall-nut | 50 | 4000 HP wall — soaks up bites for the row behind it |
| 寒冰射手 Snow Pea | 175 | Frozen pea that slows zombies to half speed |
| 双发射手 Repeater | 200 | Fires two peas per shot |
| 三线射手 Threepeater | 325 | Hits the lane above, its own lane, and the lane below |
| 樱桃炸弹 Cherry Bomb | 150 | Detonates a 3 × 3 area |
| 土豆雷 Potato Mine | 25 | Arms for 14 s, then blows up the next zombie to step on it |
| 火爆辣椒 Jalapeno | 125 | Burns every zombie in its whole lane |

Every plant goes on **cooldown** after planting, shown as a dark overlay sliding up its seed packet. A plant that has been bitten grows a small health bar above it — green, then amber, then red as it runs out — and it only appears once the plant has taken damage, so an untouched lawn stays clean.

### 兔子园丁 · Rabbit gardener
A one-off **☀1000** hire button in 设置 · SETTINGS. Pay it once and a rabbit moves onto the lawn and starts hopping after sun: every sun that lands is fetched and collected for you, for the rest of the run. There is **no levelling and nothing to upgrade** — a single purchase, and the button changes to **🐰 兔子园丁：在岗** so you can see it is working. Having grabbed a sun it simply waits there for the next one instead of walking home, and it travels with your save, so loading a run keeps it, while **重新开始** starts you without one.

### 融合 · Combining plants (fusion)
Drag one planted plant **onto** another: both vanish and a single **fused plant** grows in the cell you dropped onto. Fused plants wear a golden aura and do the job of both parents at once.

- Only the pairs listed below fuse — anything else answers *"A + B 无法融合"* and costs you nothing.
- Fusion is free apart from the two plants, and the result starts at full health.
- The **融合 · FUSION** box in the sidebar lists every recipe; hover a row to see what the result does.
- Both parents are consumed, so look before you drag.

| Recipe | Result |
|---|---|
| 豌豆射手 + 豌豆射手 | 双发射手 — two peas per shot |
| 双发射手 + 双发射手 | 四发射手 — four peas per shot |
| 豌豆射手 + 寒冰射手 | 寒冰双发 — two frozen peas |
| 双发射手 + 寒冰射手 | 寒冰双发 |
| 寒冰射手 + 寒冰射手 | 极寒射手 — much stronger and longer slow |
| 豌豆射手 + 三线射手 | 五线射手 — hits all five lanes |
| 豌豆射手 + 坚果墙 | 坚果射手 — 4200 HP shooter |
| 双发射手 + 坚果墙 | 重装双发 — armoured double shooter |
| 向日葵 + 向日葵 | 双子向日葵 — double the sun |
| 向日葵 + 豌豆射手 | 太阳花射手 — sun **and** peas |
| 向日葵 + 寒冰射手 | 阳光寒冰 — sun **and** slow |
| 向日葵 + 坚果墙 | 阳光坚果 — sun **and** 4600 HP |
| 向日葵 + 双发射手 | 阳光双发 — sun **and** double peas |
| 坚果墙 + 坚果墙 | 高坚果 — 8000 HP wall |
| 樱桃炸弹 + 樱桃炸弹 | 灭世之核 — 5×5 blast |
| 樱桃炸弹 + 火爆辣椒 | 灭世之核 |
| 火爆辣椒 + 火爆辣椒 | 烈焰风暴 — burns three lanes |
| 土豆雷 + 土豆雷 | 连环雷区 — blows up three zombies |
| 土豆雷 + 樱桃炸弹 | 连环雷区 |

### Zombies
| Zombie | Trait |
|---|---|
| 普通僵尸 Basic | Standard walker |
| 路障僵尸 Conehead | Road cone soaks 370 extra damage |
| 铁桶僵尸 Buckethead | Metal bucket takes 1100 extra damage |
| 旗帜僵尸 Flag Zombie | Marks the start of a huge wave; moves faster |
| 巨人僵尸 Gargantuar | **Boss** — wave 10, smashes plants almost instantly |
| 僵尸博士 Zomboss | **Final boss** — wave 20, high HP, spawns extra zombies |

### Controls
| Action | How |
|---|---|
| Select a plant | Click its seed packet, or press **1**–**9** |
| Plant | Click an empty lawn cell |
| Collect sun | Click a falling sun |
| Inspect / dig up | Click a planted plant, then **铲除** in the sidebar |
| **Combine two plants** | Drag one planted plant onto another (see 融合 below) |
| Shovel | Click the **🥄** button, then click a plant |
| Cancel | Press **Esc** or **right-click** |
| Pause | Press **Space** or click **暂停** |
| Start the next wave early | Click the wave button while it counts down |
| Game speed | **1×** / **2×** / **3×** buttons |
| Sound on/off | **🔊 音效** button |
| Auto-collect sun | Hire the **🐰 兔子园丁** in 设置 (☀1000, then it gathers every sun for the rest of the run) |
| Save / load | **保存进度** and **读取存档**; also auto-saves after each wave, each planting and each wave start |

### Saving your game
Identical to the Tower Defense project, but with its own save key — the games never overwrite each other.

- A checkpoint is written when a wave is cleared and shortly after you plant or dig up a plant.
- **保存进度** saves immediately, mid-wave, with zombies on the lawn.
- **读取存档** replaces the current run.
- When you reopen the page, the title screen offers **继续上一局**.
- Sun, waves, plants, mid-march zombies, uncollected sun, mower states and cooldowns are all restored.
- Winning or losing clears the save.
- **Game speed**, **sound** and **auto-collect** are remembered separately.

### Tips
- Open with two or three **sunflowers** before your first shooter — the first wave only starts when you press the button.
- Sky sun keeps falling during the pre-wave lull, so there is no rush.
- A **坚果墙** in the sixth column buys your shooters a lot of time.
- 土豆雷 is the cheapest way to delete one early zombie; remember it needs 14 s to arm.
- 樱桃炸弹 / 火爆辣椒 are the panic buttons — save them for cone and bucket clusters.

### Features
- Classic **5-lane × 9-column lawn** rendered on a single canvas — house, porch and picket fence included.
- **Fusion**: drag one plant onto another to combine them into one of **19 hybrid plants**, drawn as both parents under a golden aura.
- 9 plants and 6 zombies, all drawn procedurally (no image assets), with squash-free walk and chew animation.
- Sun economy with clickable sky sun and sunflower output, plus an optional auto-collect toggle.
- Per-row **lawn mowers** as a one-time safety net.
- Zombie **armour** (cone / bucket) that visibly absorbs damage before the walker drops.
- 20 waves with flag waves, two bosses, and a Zomboss that spawns reinforcements.
- Wave progress bar with flag markers, wave preview, and PvZ-style "一大波僵尸正在接近！" alerts.
- Save & restore, 1×/2×/3× speed, pause, and procedural WebAudio sound with a mute toggle.

---

## 组合模式 — Combined (长城守卫战 × 植物大战僵尸 3)

**Location:** `tower-defense/index.html` — pick 组合模式 on the title screen.

The third game of the collection: the Great Wall and the lawn in one battle. Both defences live on the **same 5 × 9 lawn** — plants paid for with **阳光 (sun)** and 长城 pagoda towers paid for with **银两 (silver)** — against a joint army of PvZ zombies **and** the Wall's 蛮族 invaders.

### How to Play
- Enemies come in from the right down **five lanes**. If one gets through, the **割草机 (lawn mower)** in that row fires once; after that, anything that gets past **eats the 城墙 (wall)**.
- The wall starts at **20** and is drawn as a **长城关门** on the left of the lawn. A normal enemy takes 1 wall, 将军 5, 黑龙 8. Wall at 0 = 长城失守.
- **阳光** starts at 50. It falls from the sky and drops from 向日葵; spend it on plants.
- **银两** starts at 150. Every enemy you kill pays a bounty; spend it on towers.
- Survive **20 waves** to win. Waves 5 / 10 / 15 / 20 are 一大波 (flag) waves.

### Defending — two systems, one lawn
| System | Currency | Where | How |
|---|---|---|---|
| **植物 Plants** | 阳光 ☀ | Lawn cell | Click a seed packet (or **1**–**9**), then click an empty cell |
| **炮塔 Towers** | 银两 🪙 | Lawn cell | Click a tower card in **炮塔 · TOWERS** (or press **Q**/**W**/**E**/**R**), then click an empty cell |

One occupant per cell — a plant and a tower can never share a square.

| Tower | Cost | Role |
|---|---|---|
| 箭塔 Archer Tower | 50 | Fast single-target damage — best value early |
| 火炮台 Fire Cannon | 100 | Slow, high damage, **splash** — great against crowds |
| 寒冰塔 Frost Pagoda | 75 | **Slows** enemies so every other defender gets more shots |
| 雷龙塔 Dragon Lightning | 150 | **Chain lightning** hits several enemies at once |

Towers fire at whatever is closest to the wall inside their **circular range** — they shoot across lanes, so one tower can cover several rows. Each tower upgrades twice (max level 3): click a built tower and use **升级** (upgrade) or **拆除** (sell, refunds half of everything you put in).

Plants work exactly as in 植物大战僵尸 3 — including **drag-to-fuse** (all 19 hybrids above).

### The joint army
| Enemy | Side | Trait |
|---|---|---|
| 普通僵尸 / 路障僵尸 / 铁桶僵尸 | PvZ | Walkers; cone and bucket armour soaks damage |
| 旗帜僵尸 | PvZ | Marks a huge wave |
| 巨人僵尸 | PvZ | **Boss** — wave 10, smashes plants almost instantly |
| 僵尸博士 | PvZ | **Final boss** — wave 20, also calls in reinforcements |
| 流寇 Raider | Wall | Standard foot soldier |
| 快马 Fast Rider | Wall | Nearly twice as fast — priority target |
| 盾兵 Shield Trooper | Wall | High HP **and armour** — small hits barely scratch it |
| 邪僧 Wicked Monk | Wall | Balanced, arrives in groups |
| 将军 General | Wall | **Boss** — wave 10 |
| 黑龙 Black Dragon | Wall | **Final boss** — wave 20 |

Both 蛮族 and zombies **chew plants** that block them, and both drop silver when killed.

- **Wave 10** is a double boss: 巨人僵尸 **and** 将军 together.
- **Wave 20** is 僵尸博士 **and** 黑龙 together.

### Controls
| Action | How |
|---|---|
| Select a plant | Click its packet in the tray, or press **1**–**9** |
| Select a tower | Click a card in 炮塔 · TOWERS, or press **Q** / **W** / **E** / **R** |
| Build | Click an empty lawn cell (plants cost ☀, towers cost 🪙) |
| Collect sun | Click a falling sun, or hire the **🐰 兔子园丁** (☀1000) and it collects them for you |
| Inspect | Click a plant or a built tower — the sidebar shows its stats |
| Upgrade / sell a tower | Select it, then **升级** / **拆除** |
| Dig up a plant | Click a plant, then **铲除** — or use the **🥄** shovel |
| Combine two plants | Drag one planted plant onto another (see 融合 above) |
| Cancel | Press **Esc** or **right-click** |
| Pause | Press **Space** or click **暂停** |
| Start the next wave early | Click the wave button while it counts down |
| Game speed | **1×** / **2×** / **3×** buttons |
| Sound / rabbit gardener | **🔊 音效** button and the **🐰 兔子园丁** hire button |
| Save / load | **保存进度** and **读取存档** |

### Saving your game
Identical to the other two games, but with its own key (`comb_save_v1`) — the three never overwrite each other.

- A checkpoint is written after each wave, and shortly after you plant, dig, build, upgrade or sell.
- **保存进度** saves immediately, mid-wave, with enemies on the lawn.
- The title screen shows the saved wave, 阳光, 银两 and 城墙, with **继续上一局**.
- Sun, waves, plants, towers (with their levels), silver, wall, mid-march enemies, uncollected sun, mower states and cooldowns are all restored.
- Winning or losing clears the save. **Game speed**, **sound** and **auto-collect** are remembered separately.

### Tips
- Open the way you would in PvZ — 向日葵 first — but a single 箭塔 (50 银两) placed mid-lawn pays for itself fast, because every kill it makes funds the next tower.
- A tower covers several rows; plants only shoot their own lane (except 三线射手 and 五线射手). Put towers where the lanes are busiest.
- 寒冰塔 + 火炮台 is the best pair: the slow keeps enemies inside the splash radius.
- Armour is real: 盾兵 (240) and 铁桶僵尸 (1100) laugh at 箭塔 arrows — bring 火炮台 or 雷龙塔 for them.
- Each row's mower is a one-time save, and the wall is your real life bar. Do not rely on mowers: 20 leaks past the mowers and the 长城 falls.

### Features
- The PvZ lawn, the Wall's rampart-and-gate art, and both games' rosters in **one battlefield**.
- Two currencies running side by side: sun for plants, silver for towers.
- Four 长城 pagoda towers with 3 upgrade levels, splash, slow and chain-lightning, drawn procedurally.
- Fully mixed waves with **twin bosses** at wave 10 (巨人僵尸 + 将军) and wave 20 (僵尸博士 + 黑龙).
- Invaders and zombies share the same lane AI — both bite plants and both pay bounties.
- **城墙 (wall) HP** replaces the instant loss: leaks hurt, 20 points of damage and the wall falls.
- Plant **fusion** (19 hybrids), lawn mowers, sun economy, 1×/2×/3× speed, pause, save & restore — all carried over.

---

## Running the Games
All apps are **pure HTML/CSS/JavaScript** — no build tools or servers required. Simply double-click any `index.html` file to use it in your browser.
