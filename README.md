# Spin & Win

A self-contained, single-file HTML ice-breaker prize wheel. No build step, no dependencies, no server required.

## Files

- **`index.html`** — the game. Host sets up prizes (name, icon, quantity, odds) on a setup screen, then starts the wheel. Includes a player check-in form (name + contact number), live stock tracking, confetti on a win, and a spin log.
- `spin-and-win-builder.html` — identical copy of `index.html`, kept under its original name.
- `spin-and-win-fixed-prizes.html` — an earlier variant with prizes hardcoded (iPhone Pro Max, T-shirt, Shoes, Mug, Voucher RM20, Try Again) instead of editable on-screen.

## Run it locally

Just double-click `index.html` — it opens in any browser, no server needed.

## Deploy to GitHub Pages

1. Create a new GitHub repo (or use an existing one) and push this folder's contents to it.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Pick the branch (e.g. `main`) and folder `/ (root)`, then **Save**.
5. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/` within a minute or two — that URL serves `index.html` automatically.

```bash
git init
git add index.html README.md
git commit -m "Add Spin & Win game"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Notes

- Each device that opens the page runs its own independent game instance — prize stock and the spin log are **not** synced across devices (no backend). Best used as one screen the host operates, or shared as a link where each player's session is tracked separately.
- Works offline once loaded; no external network calls at runtime.
