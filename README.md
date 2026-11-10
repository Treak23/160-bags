# 160 Bags

A tiny browser game. A plane at Fukuoka can't depart until 160 missing bags are loaded, and you are the only ground handler on shift.

**Play:** https://treak23.github.io/160-bags/ (once GitHub Pages is enabled, see below)

## How to play

- Bags roll past on the conveyor, each with a flight tag.
- Tap (or click) every bag tagged **FUK** to load it. Each one counts as 5 bags, so 32 correct taps finishes the round.
- Let everything else pass. Loading a wrong bag adds **20 seconds** to the delay clock.
- A missed FUK bag comes around again.
- The belt speeds up as the counter climbs, and look-alike tags (FUI, PUK, FVK...) in near-identical colours start to appear. Read the code, not the colour.
- When all 160 are loaded the plane departs and you get a rating based on how late it left.

## Run locally

It is a single `index.html` with no dependencies or build step. Open the file in a browser, or serve the folder:

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

Works with touch on mobile and mouse on desktop. Sound effects use Web Audio and start after the first tap.

## Hosting on GitHub Pages

1. On GitHub, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose the branch that contains `index.html` (for example `main`) and the `/ (root)` folder, then **Save**.
4. After a minute or so the game is live at `https://treak23.github.io/160-bags/`.

The empty `.nojekyll` file tells Pages to serve the files as they are.
