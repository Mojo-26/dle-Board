# The Dle Board 🟩🟨🟩

A personal corkboard-style hub for daily puzzle games in the "dle" family — Wordle-likes, geography guessers, music games, logic puzzles, and more. Search, browse, star your favorites, and discover something new every day.

---

## What it is

A single HTML file you can open in any browser, host on GitHub Pages, or share directly with friends and coworkers. No installation, no account, no server required. Just open and play.

---

## Features

- **200+ games** across 18 categories including Words, Geography, Music, Movies/TV, Math/Logic, Video Games, Sports, Science, History, and more
- **Search** by name, category, or description
- **Category filters** to browse one genre at a time
- **Favorite stars** — tap ☆ on any game to save it; favorites float to the top of the list and persist between visits
- **Favorites filter** — tap the "☆ Favorites" button to see only your starred games
- **Today's Pick** — a daily game recommendation that's the same for everyone on the same day, seeded by the date
- **Random pick** — the "show me something else" button picks a new game at random whenever you tap it
- **Fully mobile-friendly** — works on any phone browser

---

## How to use it

### Option A — Open the file directly
Download `index.html`, double-click it (or drag it into a browser window), and it opens immediately. No internet required except to visit the actual game sites when you tap "Play."

### Option B — Host on GitHub Pages (recommended)
Hosting it gives everyone a permanent link instead of passing a file around, and lets you update the site for everyone at once.

1. Create a free account at [github.com](https://github.com)
2. Create a new **public** repository (e.g. `dle-board`)
3. Upload `index.html` and rename it to exactly `index.html`
4. Go to **Settings → Pages**, set the branch to `main` and folder to `/(root)`, and save
5. Your live link will appear at `https://yourusername.github.io/dle-board/` within a minute or two

To update the site later, just edit `index.html` directly in the GitHub browser editor (tap the pencil icon on the file), make your changes, and tap **Commit changes**. Everyone sees the updates within a minute, no file-sharing needed.

---

## How to add a game

Open `index.html` in any plain text editor (Notepad, TextEdit, VS Code, or the GitHub browser editor). Search for the line that starts with `const RAW = [` — just below it is a long list of entries that look like this:

```
["Doctordle","https://doctordle.org","Science/Nature","Diagnose a patient based on their symptoms and history."],
```

Copy any line, paste it right after the original, and fill in the four pieces in order:

1. **Name** — the game's display name
2. **URL** — the full web address including `https://`
3. **Category** — must exactly match one of the 18 existing categories (see list below)
4. **Description** — a short one-sentence description of how the game works

Keep the quotes, commas, and square brackets exactly as shown. Every line in the list needs a comma at the end except the very last one.

### Existing categories

`Words` · `Math/Logic` · `Shapes/Patterns` · `Card/Board` · `Geography` · `Science/Nature` · `History` · `Estimation` · `Vehicles` · `Movies/TV` · `Music` · `Video Games` · `Sports` · `Trivia` · `Novelty` · `Colors` · `Food` · `Misc`

If you want to add a brand new category, you'll also need to add it to the `GROUP` mapping object a little further down in the code — just follow the pattern already there and assign it to one of the four color groups (A, B, C, or D).

---

## How favorites work

Favorites are saved in your browser's local storage, meaning:

- They persist between visits on the same device and browser
- They are **personal** — each visitor has their own separate favorites list
- They do **not** sync between devices or people
- Clearing your browser data will reset them

---

## A note on ads and commercial use

The game list in this project is adapted from [The Dles](https://github.com/aukspot/dles) by aukspot, which is licensed under [GPL-3.0](https://github.com/aukspot/dles/blob/main/LICENSE). That license permits commercial use (including running ads), but requires that attribution and the open license be kept intact in any public or distributed version. The design, layout, daily-pick feature, and favorites system are original to this project.

---

## Credits

Game list adapted from [The Dles](https://github.com/aukspot/dles) by aukspot, used under the GPL-3.0 license. Not affiliated with any of the games listed. Each game links to its own independent website.

Built with plain HTML, CSS, and JavaScript — no frameworks, no dependencies, no build step.
