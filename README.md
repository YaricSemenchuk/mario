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
per world (birdsong, wind, lava bubbles, candy chimes, the sea, the beeps of a moon base). Every open world has a tune
of its own, the kart, the jet ski and the moon rover hum louder and higher as they speed up, and under the water every
sound is muffled.

- Seven open worlds with no timer and no game over; a fall only sends the hero back to the last flag he touched.
  Promo Island sits between them: a village with a fountain, houses and a windmill, a beach with a pier, a lake under
  a waterfall cliff (with a cave behind the water), a vegetable garden, a lighthouse on a plateau, a forest on terraces
  and a sky island above it. The hero swims (the action button is a stroke forward, a jump leaps out of the water) and
  walks up and down slopes
- Behind the island's gates lie six more worlds, each with its own folk and quests; the first four have ten stars and
  doors to their levels, the last two are open worlds of ten quests each:
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
  - the Coral Sea: a lagoon deep enough to dive in, inside a ring of rocky islets. A harbour with a long pier, Turtle
    Beach, a lighthouse rock, a sandbar, floating jet ski ramps, and under the water a coral reef with an octopus's
    garden, Captain Claw's sunken ship with a hold to swim into, a kelp forest and a tunnel along the sea floor up into a
    dry grotto. A jet ski is lent free at every pier. In deep water the action button dives: held it swims down, the jump
    swims up, a tap is a stroke that knocks out jellyfish; the hero wears a snorkel mask and the view turns blue
  - the Moon Station: a crater plain under a black sky with the Earth in it. Everyone wears a glass helmet; gravity is
    weak, so jumps go twice as high, and the air tank's jets give one more jump in the air. A base of glass domes, a rocket
    on its launch pad (five fuel cells and it takes off), the aliens' flying saucers, a crater with a gravity lift up to a
    belt of floating asteroids, the Moon Mountain with a crystal cave, an observatory and a dark lunar sea. A moon rover
    is lent at the base
- Stars: 72 in the worlds and one for every level cleared, 86 in all. They come from folk and secrets: lost ones to bring
  home (froglets, camel calves, penguin chicks, gingerbread kids, little robots, baby turtles that swim under the water,
  little aliens follow the hero once found), eight red badges in every world, gardens, warehouses and a reef to clear of
  enemies, ring races against the clock (on foot, on jet skis over the ramps, on moon rovers), treasure dug up with a
  ground pound on an X, magic blocks that last twelve seconds after a blue button, collections for someone (the baker's
  five ingredients, the rocket's fuel cells), big switches (the factory, the moon's antennas), summits, caves and towers,
  and three newer kinds:
  - deliveries: carry something from one of the folk to another, held over the head: a basket, a letter, a jug of water,
    hot cocoa, a pie, an oil can, a telescope lens. Some are chains (the one who gets it hands over the next thing), some
    have a clock (the water evaporates, the cocoa cools). A hit, a fall or a dip in the water loses it, and it goes back to
    whoever gave it
  - runaways to catch: a froglet round the fountain, a penguin chick on the rink, the Gingerbread Man, a dolphin you only
    catch on a jet ski. They run off when the hero comes near and stop for breath now and then
  - beacons to light before the time runs out, in any order: caravan lanterns, signal lights, buoys at sea, solar panels
  Quests follow one another: some open only after another is done (the post after the garden is saved, the chase on
  the rink after the spiky shells are gone) or once the one who needs help has asked for it. Every finished quest also pays 20
  badges. A line under the buttons shows the quest in hand (what is carried and to whom, the rings or beacons so far, who
  is following), with a clock for the timed ones. The pause card lists a world's stars with a hint for each one still
  missing; on the island it also sums up every world and says where the gates are
- The World Gates open with stars: five on the island's square (the first leads to the Green levels, the others into the
  worlds at 3, 8, 15 and 24 stars), the Sea Gate at the end of the pier (30) and the Star Gate on a cloud islet above the
  forest (42). Every world has a gate home and a door for each of its levels; a cleared level returns the hero in front
  of its door
- Every badge goes into a wallet the shops take (Murr's on the island, his cousins' in every world), in three tabs:
  - perks to switch on and off: a coin magnet, spring boots with a jump in the air, faster sneakers, a star compass over
    the hero's head, Iskra always along, a spare heart and a mushroom in the pocket for the levels, an hourglass with
    a minute more; and goods for right now (a shield, a mushroom, the fire pepper, one star on the island)
  - skins: thirteen costumes, caps in eight colours, and hats and glasses (a crown, a cowboy hat, a tricorn, a Viking
    helmet, a top hat, a bobble hat, cat ears, sunglasses, headphones, a halo, a flower)
  - rides, called with the ride button (V on a keyboard) in the open worlds: a scooter, a go-kart that bowls enemies
    over, a snowboard that flies on snow, ice and sand, a jet ski for the water, a pogo stick that bounces by itself and
    squashes spiky shells, a little cloud that glides, jumps in the air and skims water, and a six-wheeled moon rover.
    A hit knocks the hero off. Blue pads lend a ride for free (the jet ski at the piers, the rover on the Moon) until the
    hero gets off it
- Progress is saved in the browser: stars, finished quests, what every collection has found, the wallet and the shop
- Friends online: "С друзьями" on the title (or "Играть с друзьями" in the pause card) makes a room with a five-letter
  code and a link to send. Friends in the same room see each other's heroes whenever they are in the same world or level:
  they run, jump, swim, ride and wave (G, or the hand button on a phone) on each other's screens, in their own costumes
  and hats, with a name over the head, or an arrow and the distance at the screen's edge when out of view. Everyone
  keeps their own world, stars, quests and wallet; only the pose travels. The friends list says where each one is, and
  "К другу" jumps into their open world right next to them (a race stops and a delivery drops, as after a fall). The
  browsers talk directly over WebRTC (Trystero, loaded from jsDelivr only when a room is joined), meeting through
  public Nostr relays, so there is still no server. Some mobile networks do not let two phones connect directly; Wi-Fi
  usually does
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
  the camel, the snowman Plombir, granny Pryanya and the gingerbread kids, the gummy-bear baker, grandpa Turtle, Inka the
  octopus, Splash the dolphin, mama Zyuzya the alien and more) give hints and quests in speech bubbles, some hand out a
  shield
- Dino: a rideable companion (faster, higher jump, one extra jump in the air, stomps spiky enemies; runs off when you get hit)
- Iskra: a helper star that pulls in nearby coins and catches one fall into a pit or lava per checkpoint
- Lira: a fairy who flies out of every castle and thanks the hero in the last one
- Collectibles are the Promobile mark
- Touch controls on phones (left thumb stick, jump and action buttons, swipe to turn the camera);
  on desktop WASD or arrows, Space to jump, Shift or F for the action button, mouse drag or Q/E for the camera, V for a ride,
  G to wave to friends

## Play

Open the GitHub Pages site on a phone. On iPhone use Safari → Share → Add to Home Screen
to launch it full screen like an app.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
