# Super Hop 3D

A 3D platformer that runs in any mobile or desktop browser. Plain HTML with
WebGL via Three.js 0.186 (ES modules from jsDelivr), no build step: the whole game lives in `index.html`.

Rendering uses PBR materials, an image-based sky environment, neutral tone mapping, soft shadows,
bloom and ambient occlusion. Quality drops automatically (AO, then bloom, then resolution) when the
frame rate falls, so older phones stay playable. Needs Safari 16.4+ or a current Chrome/Firefox.

- Three worlds, ten levels: Green Hills, Sky Trail; Sunny Dunes, Ice Peaks, Lava Fortress; Candy Valley, Jelly Bridges
- A boss at the end of every world: King Chestnut (1-3), Fire Shell (2-4), Grumble the storm cloud (3-3).
  Dodge the attack, then stomp the boss while it is dazed (stars circle its head); three hits win the fight
- Blocks, bricks, shields, springs, jelly bounce pads, moving and falling platforms, slippery ice, lava, rotating fire bars, checkpoints, flagpole finish
- Enemies: walkers, spiky shells, bouncing hoppers
- Power-up mushroom from "?" blocks: the hero grows, smashes bricks and survives one hit (already big: a shield instead)
- Friendly NPCs (Promobot, Kvak the frog, Ping the penguin) give hints in speech bubbles, some hand out a shield
- Dino: a rideable companion (faster, higher jump, one extra jump in the air, stomps spiky enemies; runs off when you get hit)
- Iskra: a helper star that pulls in nearby coins and catches one fall into a pit or lava per checkpoint
- Lira: a fairy who flies out of every castle and thanks the hero in the last one
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
