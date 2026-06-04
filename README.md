# GMBIT — 3D Chess Arena

Premium, immersive 3D chess in the browser. Orbit a cinematic board, play a built-in AI at three strengths, with animated moves, capture effects, a check alert, soft ambient music, and a post-game review that scores your accuracy and coaches your improvement.

**Live:** `https://clutchpbcfo.github.io/gmbit/` _(after you deploy — see below)_

## Play
- **Drag** to orbit the board · **pinch / scroll** to zoom
- **Tap a piece**, then tap a highlighted square to move
- **New** restart · **Last** shows where your last piece moved (no take-backs) · **View** flips sides · **Resign** · **Music** toggle
- After each game: a **Game Review** — accuracy %, your mistakes, your biggest slip + the stronger move, and a coach tip.

## Files (what to deploy)
- `index.html` — the game (3D)
- `three.min.js` — bundled 3D engine (**required**, keep it next to index.html)
- `favicon.svg` — site icon
- `og-image.png` — social share preview
- `index-classic.html` — the clean 2D version (optional fallback)

> `GMBIT_CONCEPT.md` is **internal strategy — do NOT commit it** to the public repo. The included `.gitignore` already excludes it.

## Deploy to GitHub Pages
First create an **empty** repo at `github.com/clutchpbcfo/gmbit` (no README). Then, from this folder:

```bash
git init
git add index.html three.min.js favicon.svg og-image.png index-classic.html README.md .gitignore
git commit -m "GMBIT 3D — live build for testers"
git branch -M main
git remote add origin https://github.com/clutchpbcfo/gmbit.git
git push -u origin main
```

On GitHub: **Settings → Pages → Source: `main` / `/ (root)` → Save.**
Live in ~1 minute at **`https://clutchpbcfo.github.io/gmbit/`**.

(If you name the repo something other than `gmbit`, update the `og:image` / `twitter:image` URLs in `index.html` to match.)

### Optional: custom domain (gmbit.app)
Add a file named `CNAME` containing `gmbit.app`, push it, then point the domain's DNS at GitHub Pages per GitHub's instructions. Update the `og:image` URLs in `index.html` to `https://gmbit.app/og-image.png`.

## Tester feedback
The in-game **Feedback** button links to X (**@ClutchPBCFO**). To route feedback to a Telegram group instead, change the `href` on the `#feedback` link in `index.html`.

## Credits
Built by REACHFI. Three.js (r128) bundled locally.
