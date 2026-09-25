# Super Hop 3D

A 3D platformer that runs in any mobile or desktop browser. Plain HTML with
WebGL via Three.js, no build step: the whole game lives in `index.html`.

- Five worlds: Green Hills (1-1), Sky Trail (1-2), Sunny Dunes (2-1), Ice Peaks (2-2), Lava Fortress (2-3)
- Blocks, bricks, shields, springs, moving and falling platforms, slippery ice, lava, rotating fire bars, checkpoints, flagpole finish
- Enemies: walkers, spiky shells, bouncing hoppers
- Friendly NPCs (Promobot, Kvak the frog, Ping the penguin) give hints in speech bubbles, some hand out a shield
- Collectibles are the Promobile mark
- Touch controls on phones (left thumb stick, jump button, swipe to turn the camera), keyboard and mouse on desktop

## Play

Open the GitHub Pages site on a phone. On iPhone use Safari → Share → Add to Home Screen
to launch it full screen like an app.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
