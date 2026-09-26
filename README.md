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
per world (birdsong, wind, lava bubbles, candy chimes, the sea, the beeps of a moon base, birds and distant calls in the
jungle). Every open world has a tune of its own (the survival game, the dragons' cup and the tank battle have their own too,
and Leviathan comes with the bosses' tune),
the kart, the jet ski and the moon rover hum louder and higher as they speed up, a tank's tracks clatter, the wind roars past
a flying dragon, and under the water every sound is muffled.

- Ten open worlds with no timer and no game over; a fall only sends the hero back to the last flag he touched.
  Promo Island sits between them: a village with a fountain, houses and a windmill, a beach with a pier, a lake under
  a waterfall cliff (with a cave behind the water), a vegetable garden, a lighthouse on a plateau, a forest on terraces
  and a sky island above it. The hero swims (the action button is a stroke forward, a jump leaps out of the water) and
  walks up and down slopes
- Behind the island's gates lie nine more worlds, each with its own folk and quests; the first four have ten stars and
  doors to their levels, the next two are open worlds of ten quests each, and the last three are open from the start:
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
  - Dino Valley: a green valley in a ring of red earth cliffs under a smoking volcano. A stone village of the cave folk
    (huts round a campfire, the chief Uga and the girl Ula), stone cars lent at a blue pad, the rideable Dino in his
    paddock, a lake under a waterfall with a beach, mama Bronti the brontosaurus and her nest, Ula's berry patch taken over
    by raptors, a volcano with a crater of lava, and the survival clearing in the middle (below). The wild ones roam the
    valley too: raptors that run the hero down and pounce, a triceratops that snorts and charges, a pterodactyl that dives
  - Dragon Peaks: islands in the sky over a sea of clouds, reached only by dragon. Five dragons stand on their perches at the
    roost; stepping on the ring in front of one puts the hero on its back (the golden one sleeps until the dragons' cup is
    won). Further off: an island with a stone ring to fly through, the Wind Spire nearly a hundred metres high, a canyon
    between two cliffs, an island with a waterfall pouring off into the clouds, the ruins of a cloud castle. Falling into
    the clouds brings the hero back to the last flag, still on the dragon
  - the Tank Range: a training ground on a grassy plain ringed by cliffs. A base with two hangars, a shop and a pad that
    lends tanks, three KV-44s standing by the hangars (the hero can climb onto them, and a blue pad next to them lends one
    to drive), a watchtower climbed on platforms
    round its column, the tank ground in the middle (earth walls, concrete blocks, sandbags and tank traps to hide behind,
    hangar doors the grumpy tanks roll out of) where Commander Mishka runs the tank battles and the battle with Leviathan
    (below), a shooting range with eight targets that only a shell lights, a pond with Captain Claw's treasure on its
    shore, and Ping's tank race round the tank ground
- The survival game (Dino Valley): a red pad in the middle of a clearing ringed with rock. A boulder closes the way in and
  the dinosaurs come in waves out of the ferns, more of them and more kinds each time: raptors, pterodactyls, a triceratops,
  and from the fourth wave a tyrannosaur that cannot be knocked over (its stamp sends a ring along the ground to jump
  over; a stomp on its back only bounces off, a ground pound next to it dazes it) and meteors that land on red circles.
  The hero has hearts instead of lives (three, four with the spare heart), a ride only takes a hit for him, hearts turn up
  on the grass now and then, and every wave lived through gives a heart back and ten badges. Three waves and five waves
  bring a star each; the best game is kept. "🦖 Выживание" on the title goes straight there
- Flying dragons: in the air a dragon flies on by itself; the stick turns it and tips its nose up and down (let go and it
  levels out), the jump button beats the wings for speed and height (held, it keeps climbing), the action button breathes
  fire, ice, leaves, lightning or stars, a puff that pops balloons, knocks enemies over and lights beacons. Diving speeds
  it up, it lands when it comes down slowly and only touches the ground when fast. A hit only slows it. The camera swings
  round behind it. Five dragons with their own speed, turning and climbing; each can be bought in the shops and then
  flies in every open world. "🐉 Драконы" on the title goes straight to the roost
- The dragons' cup (Dragon Peaks): two laps of a ring course high among the islands, round the Wind Spire and through the
  canyon, against three dragons ridden by Ping, Kvak and Murr, who follow the rings by themselves (a little faster when
  behind, slower when well ahead). Every ring gives a gust of speed; first place brings a star and wakes the golden dragon
- The tank: slow, it turns on the spot and drives the way it faces, and its armour shrugs hits off. The action button fires
  its gun; the turret turns by itself to whatever is in front of the camera (or of the tank): enemies, balloons, targets,
  a friend's tank in a tank battle, marked with a red ring and a chevron, and with nothing there it points where the
  camera looks. A sight (a ring with ticks where the shell would burst, and a dotted line out of the gun to it) shows the
  aim all the time: red on a target, dim while the gun reloads. A shell bursts on whatever it meets and knocks over what
  stands close by, and it shoots cannonballs down
- The KV-44: the long green tank of the cartoons with five turrets, the hero standing in the hatch of the big one. It is
  slower and turns more slowly than the tank, and its whole hull keeps clear of walls (where it cannot turn it backs up a
  little). The action button fires a salvo: the big gun, then the small turrets one after another (they all turn with
  the big one), and loading them all again takes a while. It also carries a grenade launcher on the roof of the big turret
  and a rocket pod on each side of it, each on a button of its own (C and R on desktop) that darkens while it loads: the
  grenade launcher lobs four grenades in a high arc onto the target (over walls, too) or onto the ground ahead, and the
  pods send off eight rockets that turn by themselves to the targets round the tank and burst on them. Its thick armour
  gives a heart more in a tank battle, and the tank's upgrades work on it too. It is lent on a blue pad by the hangars,
  bought in the shops, and it is what the hero drives against Leviathan
- Upgrading the tank: medals come for victories (one for every wave of a tank battle knocked out, three for Leviathan,
  three for a tank battle with friends won, one for a draw) and buy upgrades in the shops' "Tank" tab, three levels each: the gun reloads faster
  and grows longer and thicker; the shells burst wider, then come out of a pair of guns, then turn fiery and hit twice as
  hard; the armour gives the tank battle more hearts and puts skirts, plates and golden stars on the tank; the engine
  drives faster, turns faster, then gets rocket boosters. Friends see each other's upgraded tanks, but in games with
  friends every tank fights the same
- The tank battle (Tank Range): a red pad on the tank ground puts the hero in a tank (one already on a KV-44 fights on
  it) and a striped barrier closes the way in. Grumpy tanks with eyes over their guns roll out of the hangar doors in waves; each keeps its distance, drives from
  cover to cover, and fires a cannonball once its gun points at the hero with nothing in between (it glows first). They
  take two shells, the big one from the fourth wave takes six and fires three at once. The armour counts hearts (three,
  four with the spare heart), hearts turn up on the ground, every wave knocked out gives one back and ten badges, three and
  five waves bring a star each, and the best battle is kept. Every sixth wave is Leviathan's. "💥 Танки" on the title goes
  straight to the tank ground
- The battle with Leviathan (Tank Range): the purple pad on the tank ground puts the hero in a KV-44 of his own and wakes
  Leviathan, a huge dark tank with angry
  glowing eyes, spikes on its nose, a big turret with a pair of guns and three small turrets. It rises out of an
  underground hangar by the far wall (once the hero has made room) and three KV-44s roll in to help: long green tanks
  with five turrets each, red stars and friendly eyes, which drive round it by themselves and fire salvos at it and at
  the grumpy tanks, and whose armour cannonballs clang off, so they make good cover. Leviathan turns to the hero, fires
  fans of five cannonballs (glowing first), its small turrets fire at the hero and at the KV-44s, and its mortar drops
  shells round the hero on red rings. At two thirds and a third of its armour (the bar at the top) it calls up two
  grumpy tanks, the second time angrily, firing faster. It goes up in a string of bursts with its turret flying off,
  the grumpy tanks still about run away and the KV-44s cheer. The hero gets two hearts more for it; beating it brings a
  star, three medals and fifty badges
- Stars: 95 in the worlds and one for every level cleared, 109 in all. They come from folk and secrets: lost ones to bring
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
  - beacons to light before the time runs out, in any order: caravan lanterns, signal lights, buoys at sea, solar panels,
    dragon fires, and targets on the shooting range that only a shell lights
  Quests follow one another: some open only after another is done (the post after the garden is saved, the chase on
  the rink after the spiky shells are gone) or once the one who needs help has asked for it. Every finished quest also pays 20
  badges. A line under the buttons shows the quest in hand (what is carried and to whom, the rings or beacons so far, who
  is following), with a clock for the timed ones. The pause card lists a world's stars with a hint for each one still
  missing; on the island it also sums up every world and says where the gates are
- The World Gates open with stars: five on the island's square (the first leads to the Green levels, the others into the
  worlds at 3, 8, 15 and 24 stars), the Sea Gate at the end of the pier (30) and the Star Gate on a cloud islet above the
  forest (42), and on the cape past Foma's garden the Ancient Gate to Dino Valley, the Dragon Gate and the Tank Gate, open
  from the start.
  Every world has a gate home and a door for each of its levels; a cleared level returns the hero in front of its door
- Every badge goes into a wallet the shops take (Murr's on the island, his cousins' in every world), in three tabs:
  - perks to switch on and off: a coin magnet, spring boots with a jump in the air, faster sneakers, a star compass over
    the hero's head, Iskra always along, a spare heart and a mushroom in the pocket for the levels, an hourglass with
    a minute more; and goods for right now (a shield, a mushroom, the fire pepper, one star on the island)
  - skins: thirteen costumes, caps in eight colours, and hats and glasses (a crown, a cowboy hat, a tricorn, a Viking
    helmet, a top hat, a bobble hat, cat ears, sunglasses, headphones, a halo, a flower)
  - rides, called with the ride button (V on a keyboard) in the open worlds: a scooter, a go-kart that bowls enemies
    over, a snowboard that flies on snow, ice and sand, a jet ski for the water, a pogo stick that bounces by itself and
    squashes spiky shells, a little cloud that glides, jumps in the air and skims water, a six-wheeled moon rover, skis,
    a UFO whose beam pulls in badges, a helicopter, the stone car of the cave folk (no floor: the driver's feet run along
    the ground under it, its stone rollers bowl enemies over), a tank with a gun, the KV-44 with five turrets, and five
    dragons that fly (listed last).
    A hit knocks the hero off (a dragon only slows down, a tank's armour takes it). Blue pads lend a ride for free (the jet
    ski at the piers, the rover on the Moon, the stone car in Dino Valley, the dragons at their perches, tanks and KV-44s on
    the Tank Range) until the hero gets off it
- Progress is saved in the browser: stars, finished quests, what every collection has found, the wallet and the shop
- Friends online: "С друзьями" on the title (or "Играть с друзьями" in the pause card) makes a room with a five-letter
  code and a link to send. Friends in the same room see each other's heroes whenever they are in the same world or level:
  they run, jump, swim, ride and wave (G, or the hand button on a phone) on each other's screens, in their own costumes
  and hats, with a name over the head, or an arrow and the distance at the screen's edge when out of view. Everyone
  keeps their own world, stars, quests and wallet; only the pose travels. While they play together, a world gate or a level
  door open for one of them is open for all (the hello carries each player's stars and cleared levels). The friends list
  says where each one is, and "К другу" jumps into their open world right next to them (a race stops and a delivery drops,
  as after a fall). The browsers talk directly over WebRTC (Trystero, loaded from jsDelivr only when a room is joined),
  meeting through public Nostr relays, so there is still no server. Some mobile networks do not let two phones connect
  directly; Wi-Fi usually does
- Games with friends, started from the friends card for everyone in the room, wherever they are (each one says yes or
  no). The game is played in the host's open world, or on Promo Island from the title or a level, and whoever says yes
  is taken there:
  - a ring race: everyone gets the same ride (a kart, the stone car in Dino Valley, a tank on the Tank Range, the snowboard down the ice slalom,
    the jet ski on the lagoon, the rover on the Moon; in Dragon Peaks each flies the dragon they picked, high up round
    the dragons' cup course) and races the rings of the world's own race quest (the factory has a course round its oven),
    two or three laps on a loop, with a countdown, an arrow to the next ring, places on the fly and a fall putting the
    racer back at the last ring. The others have 25 seconds after the first finish
  - hide and seek: one player seeks (never the same one twice running), blindfolded for 25 seconds while the others hide;
    the name tags of everyone still hidden disappear, the seeker finds someone by running right up to them, and in the
    last minute the hidden ones call out "Ку-ку!" with their tags back on the seeker's screen for a moment
  - a tank battle, always on the Tank Range's tank ground: everyone gets a tank at a spot round its middle, the barrier
    closes, and for two minutes every hit on a friend's tank is a point. Shots travel to the others, who see the shell fly
    and burst; whether it hit is for the shooter's screen to say. A tank just hit cannot be hit again for a moment; most
    hits wins
  - gates are shut until the game ends, rides are off in hide and seek, nobody gets out of a tank in a battle, and a
    winner gets 20 badges
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
  on desktop WASD or arrows, Space to jump, Shift or F for the action button (in a tank, the gun; on a KV-44,
  a salvo, with C for its grenade launcher and R for its rockets), mouse drag or Q/E for the
  camera, V for a ride, G to wave to friends

## Play

Open the GitHub Pages site on a phone. On iPhone use Safari → Share → Add to Home Screen
to launch it full screen like an app.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
