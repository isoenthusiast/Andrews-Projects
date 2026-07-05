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

## Running the Games
Both games are **pure HTML/CSS/JavaScript** — no build tools or servers required. Simply double-click any `index.html` file to play in your browser.
