# Sudoku Duel

A small two-player Sudoku game for couples (or anyone) to play side by side on the same screen. No sign-up, no server — it's a single HTML file.

**[Play it live](#) once GitHub Pages is enabled — see below.**

## Features

- Two independent Sudoku boards, one per player, generated fresh each round
- Per-player timers, started together, stopped the moment each board is solved
- Live conflict highlighting (duplicate numbers in a row/column/box are flagged)
- Confetti when a board is solved, and again when both players finish
- A winner/tie summary comparing solve times
- **Rooms**: name a room and it's saved in the browser's local storage, so you can resume a game later or run separate saved rounds for different play sessions on the same device
- Three difficulty levels (easy / medium / hard)

## Running it locally

No build step or dependencies — just open the file in a browser:

```bash
git clone https://github.com/YOUR-USERNAME/sudoku-duel.git
cd sudoku-duel
open index.html   # or just double-click it, or drag it into a browser tab
```

## Deploying with GitHub Pages

1. Push this repo to GitHub (see below if you haven't yet).
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
4. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
5. GitHub will publish the site at `https://YOUR-USERNAME.github.io/sudoku-duel/` within a minute or two.

## Pushing this to GitHub for the first time

From inside this folder:

```bash
git init
git add .
git commit -m "Initial commit: Sudoku Duel"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/sudoku-duel.git
git push -u origin main
```

(Create the empty repo on GitHub first at github.com/new — don't initialize it with a README there, to avoid a merge conflict.)

## Notes on how rooms work

Everything runs client-side. "Rooms" are saved in the browser's `localStorage`, keyed by room name — there's no account system or cross-device sync. This is built for two people sharing one screen; playing from two separate devices in real time would need a small backend to sync state, which isn't included here.

## License

MIT — see [LICENSE](./LICENSE).
