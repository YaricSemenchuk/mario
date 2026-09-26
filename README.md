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
per world (birdsong, wind, lava bubbles, candy chimes, the sea). Every open world has a tune of its own, and the kart
and the jet ski hum louder and higher as they speed up.

- Five open worlds with no timer and no game over; a fall only sends the hero back to the last flag he touched.
  Promo Island sits between them: a village with a fountain, houses and a windmill, a beach with a pier, a lake under
  a waterfall cliff (with a cave behind the water), a vegetable garden, a lighthouse on a plateau, a forest on terraces
  and a sky island above it. The hero swims (the action button is a stroke forward, a jump leaps out of the water) and
  walks up and down slopes
- Behind the island's gates lie four more worlds, each with its own folk, quests, eight stars and doors to its levels:
  - the Desert: an oasis and a bazaar, the Sphinx, the Great Pyramid with a tomb inside, a mesa climbed by riding a
    wandering dust devil, a field of quicksand (the hero sinks and has to jump out), dunes and a melon patch
  - Ice Peaks: a penguin village of igloos, a skating rink, a steaming hot spring, the Ice Mountain with a crystal cave,
    a trail up to the summit and a slippery ski slope that pulls the hero downhill, and the Fire Mountain with a crater
    of lava (it burns and throws the hero up) and the doors to the Lava Fortress and the Fire Shell
  - Candy Land: a gingerbread town round a chocolate fountain on an island in a sea of strawberry milk, a giant layered
    cake, a chocolate lake under a chocolate waterfall with a cave behind it, a lollipop forest, and a jelly field that
    bounces the hero up to candy-floss clouds and a floating island
  - the Sky Factory: steel decks over a sea of clouds with conveyor belts, a crane, a landing stage reached over blinking
    tiles, a tower climbed on fans, a warehouse full of bugs and a great hall with a corridor of presses
- Stars: 42 in the worlds and one for every level cleared, 56 in all. They come from folk and secrets: lost ones to bring
  home (froglets, camel calves, penguin chicks, gingerbread kids, little robots follow the hero once found), eight red
  badges in every world, gardens and warehouses to clear of enemies, ring races against the clock, treasure dug up with a
  ground pound on an X, magic blocks that last twelve seconds after a blue button, the baker's five ingredients, four big
  switches that restart the factory, summits, caves and towers. The pause card lists a world's stars with a hint for
  each one still missing; on the island it also sums up every world
- The World Gates on the island's square open with stars: the first leads to the Green levels, the others into the
  worlds (3, 8, 15 and 24 stars). Every world has a gate home and a door for each of its levels; a cleared level returns
  the hero in front of its door
- Every badge goes into a wallet the shops take (Murr's on the island, his cousins' in every world), in three tabs:
  - perks to switch on and off: a coin magnet, spring boots with a jump in the air, faster sneakers, a star compass over
    the hero's head, Iskra always along, a spare heart and a mushroom in the pocket for the levels, an hourglass with
    a minute more; and goods for right now (a shield, a mushroom, the fire pepper, one star on the island)
  - skins: thirteen costumes, caps in eight colours, and hats and glasses (a crown, a cowboy hat, a tricorn, a Viking
    helmet, a top hat, a bobble hat, cat ears, sunglasses, headphones, a halo, a flower)
  - rides, called with the ride button (V on a keyboard) in the open worlds: a scooter, a go-kart that bowls enemies
    over, a snowboard that flies on snow, ice and sand, a jet ski for the water, a pogo stick that bounces by itself and
    squashes spiky shells, and a little cloud that glides, jumps in the air and skims water. A hit knocks the hero off
- Progress is saved in the browser: stars, finished quests, what every collection has found, the wallet and the shop
- Fourteen levels: Green Hills, Sky Trail, King Chestnut (Green world); Sunny Dunes (Desert); Ice Peaks, Lava Fortress,
  Fire Shell (Ice Peaks); Candy Valley, Jelly Bridges, Grumble (Candy Land); Gear Works, Cloud Heights, Storm Tower,
  Megabot (Sky Factory)
- World 4 brings conveyor belts (with you, against you, or hanging over a drop), hydraulic presses with a warning
  circle (ride on top of them or slip underneath), tiles that light up in turns, and fans whose wind lifts the hero
- A boss at the end of every world: King Chestnut (1-3), Fire Shell (2-4), Grumble the storm cloud (3-3) and Megabot (4-4),
  who fires fans of cannonballs, leaps with a shockwave and then overheats.
  Dodge the attack, then stomp or ground-pound the boss while it is dazed (stars circle its head); three hits
  win the fight, and each hit calls in help (chestnuts, hoppers or bugs)
- The hero is a jointed puppet: knees, elbows, ankles, waist and neck bend in the run cycle and every pose, the hips
  dip so planted feet stay on the ground, eyes blink and follow nearby enemies and coins, the mouth has several shapes,
  and a scarf and a cowlick swing with the motion. Idle time brings fidgets (look around, stretch, tap a foot, wave at
  the camera) and eventually a nap; on a ledge the hero teeters and windmills
- Moves: a triple jump (land and jump again while running, the third one flips), a skid when reversing at speed with a
  side flip out of it, wall slides and wall kicks, plus the spin, ground pound and fireballs below
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
- Friendly NPCs (Promobot, Kvak the frog, Ping the penguin, Foma the hedgehog, Murr the cat, Captain Claw the crab, Gorbi
  the camel, the snowman Plombir, granny Pryanya and the gingerbread kids, the gummy-bear baker and more) give hints and
  quests in speech bubbles, some hand out a shield
- Dino: a rideable companion (faster, higher jump, one extra jump in the air, stomps spiky enemies; runs off when you get hit)
- Iskra: a helper star that pulls in nearby coins and catches one fall into a pit or lava per checkpoint
- Lira: a fairy who flies out of every castle and thanks the hero in the last one
- Collectibles are the Promobile mark
- Touch controls on phones (left thumb stick, jump and action buttons, swipe to turn the camera);
  on desktop WASD or arrows, Space to jump, Shift or F for the action button, mouse drag or Q/E for the camera, V for a ride

## Play

Open the GitHub Pages site on a phone. On iPhone use Safari → Share → Add to Home Screen
to launch it full screen like an app.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
