# Super Hop 3D

A 3D platformer that runs in any mobile or desktop browser. Plain HTML with
WebGL via Three.js 0.186 (ES modules from jsDelivr), no build step: the whole game lives in `index.html`.

Rendering uses PBR materials with a soft rim light on characters, an image-based sky environment
(horizon glow, a low sun on the evening levels, stars in the dark ones), neutral tone mapping, soft
shadows, bloom and ambient occlusion. Effects are shader particles (sparks, glow, smoke), shock rings,
impact flashes, a short hit-stop and screen shake; every world has its own weather (pollen, petals,
drifting sand, snow, sprinkles, ash). Quality drops automatically (AO, then bloom, then resolution) when
the frame rate falls, so older phones stay playable. Needs Safari 16.4+ or a current Chrome/Firefox.

Sound is synthesised with WebAudio: a compressor and reverb on the mix, sound effects panned and
attenuated by where they happen, footsteps per surface, chiptune music with drums, an arpeggio and an
echo on the lead (it speeds up when time runs low and as a boss loses health), and an ambience bed
per world (birdsong, wind, lava bubbles, candy chimes).

- Three worlds, ten levels: Green Hills, Sky Trail; Sunny Dunes, Ice Peaks, Lava Fortress; Candy Valley, Jelly Bridges
- A boss at the end of every world: King Chestnut (1-3), Fire Shell (2-4), Grumble the storm cloud (3-3).
  Dodge the attack, then stomp or ground-pound the boss while it is dazed (stars circle its head); three hits
  win the fight, and each hit calls in help (chestnuts, hoppers or bugs)
- Blocks, bricks, shields, springs, jelly bounce pads, moving and falling platforms, slippery ice, lava, rotating fire bars, checkpoints, flagpole finish
- Action button: a spin attack on the ground (a small hop in the air), a ground pound when high in the air.
  The pound's shockwave flattens everything nearby, spiky shells included, smashes bricks when big,
  super-bounces off springs and jelly, and a jump right after it springs higher with a flip
- Kicked enemies fly off and bowl over the ones they hit; defeats in quick succession build a combo with a bonus
- Enemies: walkers (they spot the hero and hurry), spiky shells, bouncing hoppers, Buzz the diving bug
  (buzzes, then dives at where you stood), cannons that fire cannonballs (jump, stomp or spin them away)
- Power-ups from "?" blocks: the mushroom (grow, smash bricks, survive one hit), then the fire pepper for the
  big hero (the action button throws bouncing fireballs that aim at the nearest enemy ahead; a hit costs the
  pepper, not the size), then a shield
- Friendly NPCs (Promobot, Kvak the frog, Ping the penguin) give hints in speech bubbles, some hand out a shield
- Dino: a rideable companion (faster, higher jump, one extra jump in the air, stomps spiky enemies; runs off when you get hit)
- Iskra: a helper star that pulls in nearby coins and catches one fall into a pit or lava per checkpoint
- Lira: a fairy who flies out of every castle and thanks the hero in the last one
- Collectibles are the Promobile mark
- Touch controls on phones (left thumb stick, jump and action buttons, swipe to turn the camera);
  on desktop WASD or arrows, Space to jump, Shift or F for the action button, mouse drag or Q/E for the camera

## Play

Open the GitHub Pages site on a phone. On iPhone use Safari → Share → Add to Home Screen
to launch it full screen like an app.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
