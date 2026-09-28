# Sudoku Duel

A small two-player Sudoku game for couples (or anyone). Play **online from two different places**, or side by side on one screen. No sign-up, no server of your own — it's a single HTML file.

**[Play it live](#) once GitHub Pages is enabled — see below.**

## Playing online

1. One person opens the site, enters their name, picks a difficulty and taps **Create room**.
2. They send the 5-character code (or the **Share invite** link) to their partner.
3. The partner opens the site, enters their name and the code, and taps **Join room**.

Each player gets their own puzzle and can watch the other's board fill in live, with both timers running. Confetti when you finish, and a winner banner when you both do. If someone drops off, they can rejoin with the same name and code and pick up where they left off. The **Rematch** button starts fresh puzzles.

Online play is peer-to-peer (WebRTC via [PeerJS](https://peerjs.com/)'s free public broker), so there's nothing to host. The room lives only while the host keeps the page open. Some strict networks can block direct connections.

## Features

- Two independent Sudoku boards, one per player, generated fresh each round
- Per-player timers, started together, stopped the moment each board is solved
- Live conflict highlighting (duplicate numbers in a row/column/box are flagged)
- Confetti when a board is solved, and again when both players finish
- A winner/tie summary comparing solve times
- **Same-screen rooms**: name a room and it's saved in the browser's local storage, so you can resume a game later or run separate saved rounds for different play sessions on the same device
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

In same-screen mode, rooms are saved in the browser's `localStorage`, keyed by room name. Online rooms are temporary and aren't saved.

## License

MIT — see [LICENSE](./LICENSE).
