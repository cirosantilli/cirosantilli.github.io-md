# Cataclysm: Dark Days Ahead

↑ **Parent:** [Survival game](survival-game.md)  
🏷️ **Tags:** [Open source video game](open-source-video-game.md), [Roguelike](roguelike.md), [Text-based game](text-based-game.md), [Zombie video game](zombie-video-game.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cataclysm:_Dark_Days_Ahead)

Seems to simulate the world in an extremely elaborate way.

Ciro can't help but to think that with a little content work, this game engine could also produce a [Factorio](factorio.md)-like (conveyor belts mentioned in passing at: [https://discourse.cataclysmdda.org/t/vehicle-unloading/10783](https://discourse.cataclysmdda.org/t/vehicle-unloading/10783)), or a [The Sims](the-sims.md)-like, or an Stardew-valley-like. E.g. even stuff like house building is already included: [https://www.youtube.com/watch?v=QnCYGSlZ1gE](https://www.youtube.com/watch?v=QnCYGSlZ1gE)

They're also adding more and more allyied NPC management in "faction camps" it seems: [https://www.reddit.com/r/cataclysmdda/comments/edg5y0/a_beginners_guide_to_faction_bases/](https://www.reddit.com/r/cataclysmdda/comments/edg5y0/a_beginners_guide_to_faction_bases/) thus approaching the game further to [Dwarf Fortress](dwarf-fortress.md) or [RimWorld](rimworld.md).

[Ciro Santilli](ciro-santilli-split.md) played this for 1 day and a half non-stop with [save scumming](cataclysm-dda-save-scum.md) in 2022, then he deleted his saves and uninstalled the game, and started Googling to see how end games can look like, [as usual](high-flying-bird-vs-gophers.md).

The problem is that it is a bit hard to find edited gameplay with highlights only, the type of people who play those games are just regular nerds right. But there is a lot of gameplay videos, just not edited ones.

Then two days later Ciro re-downloaded it and played more, just no so nonstop, the urge was too strong. Two days later, he deleted the save again after clearing out a middle sized town, and reaching a large town.

Then Ciro learned about debug menu, which is the best way to experience all buildings/weapons/abilities easily without grinding more than necessary. TODO any simple easy way to become invincible there? [https://discourse.cataclysmdda.org/t/prompt-for-certain-debug-commands/19209/5](https://discourse.cataclysmdda.org/t/prompt-for-certain-debug-commands/19209/5)

> We do not accept feature requests for the debug menu.

Lol. Found a "Debug invincibility" and "Debug invisibility" under mutations.

But a few days later he played a bit more for a day non-stop after having learnt some more techniques from YouTube, and then deleted again.

Ciro noticed that the part of this game that he likes the most is the early game. Raiding low populated areas like farms is joy. Once you get a car and stabilize, things become a bit less fun, and it is then just a matter of getting more and more powerful with a lot of routine work, which takes time. Sleeping in tents is quite tempting as well, there's a campfire overmap tile that is great. You can actually take down tents Ciro later learnt... that's awesome.

A major joy of this type of game is the ability to loot shops and homes without any moral implications since the former owners are all dead/zombified.

Another major joy is the incredible value you attach to items you discover, because they are truly life changing.

For example, Ciro was first obsessed with his duffel bag, which could carry huge volumes, and made fixing it a top priority once it got ripped!

Then he was obsessed about the 4x4 car he found, which looks like this:
```
fffffF
fttsfF
fttsfF
fffffF
```
where:
- `f`: frame
- `F`: reinforced frame
- `t`: trunk
- `s`: seat
What a great design! Enough room for a lot of loot, and also the reinforced frame to kill zombies without destroying the car, all while not being overly heavy which spends a lot of fuel, not being too wide which makes maneuvering in cities with broken cars on the road hard! Also the trunks were large enough for large water tanks, which solves your clean water supply forever.

Humvees are also good, but they are wider, have a lot of useless seats, and consume diesel, a lot of diesel, runs out very quickly. But they are even tougher than the 4x4, and have a turret that can fire at zombies.

It should be noted however that larger towns are generally just too much to use a car to clear, you will just waste too much fuel/car damage/real world time. The only way is to go at night it seems.

And then guns. The power of a guns is something to behold. Encounters that would easily be your death become one shot escapes. But of course, ammo is very limited, so you want to use each precious shot wisely! FEMA camps are a good place to get some easy powerful rifles and reasonable amount of ammo. Just drive in front of the entrance, and make the armed guards follow you out, then run them over. Try not to attract the zombie inside though, they are useless civilians without weapons, and just take up your time.

This game is also very good to learn some [English](english-language.md) if you are not a native, as you have to learn what all those bit and bobs you never needed to say before are.

The default [tileset](tileset.md) when running `cataclysm-tiles` is a huge improvement over the text version, but still, could be a bit higher res. Overmap tilesets were only added in 2021 it seems: [https://www.reddit.com/r/cataclysmdda/comments/pxtqsn/new_overmap_tileset_available/](https://www.reddit.com/r/cataclysmdda/comments/pxtqsn/new_overmap_tileset_available/). Edit: 0.F appears to come with the proper Ultima tileset by defualt via `cataclysm-dda-data` Ubuntu 22.04 package. Fantastic!

There are other built-in tiles under settings, but all of them are way too resolution for a casual gamer.

[https://github.com/I-am-Erk/CDDA-Tilesets](https://github.com/I-am-Erk/CDDA-Tilesets) has a good tileset pack. To install on [Ubuntu 21.10](ubuntu-21-10.md), drop the release under:
```
~/.local/share/cataclysm-dda/gfx/
```
and then select `UltCa` from Settings \> Tiles in the main menu. It does make things much more immediately understandable. Edit: after some initial plays, Ciro had a second look at the default `-tiles` graphics, and they are not so bad. But still, the higher resolution is better. Edit: looks like they are going to merge it in-tree, which is great! [https://github.com/CleverRaven/Cataclysm-DDA/commits/master/gfx/UltimateCataclysm](https://github.com/CleverRaven/Cataclysm-DDA/commits/master/gfx/UltimateCataclysm)

No default sounds, but has a soundpacks mechanism. Sad for now default, but cool for the configurability:
- [https://github.com/damalsk/damalsksoundpack/releases](https://github.com/damalsk/damalsksoundpack/releases). It makes a large noise every time you walk, which is very annoying. Ambient sounds and music are OK though. It should really give a comfy music when in the shelter though.
Installation is similar to tilesets, but you put it under `sounds/` instead of `gfx/`. Restart required to select the soundpack option, and another restart required for the selected option to be used, clunky.

This is the type of thing that prevents wider adoption of this game, it is just too hard to figure out things.

The other major requirement for casual players would be mouse clicking stuff with dropdown menus that show what you can do there (e.g. `E` and `Shift` + `G`), and better menus, everything should be also doable with a mouse in addition to the keyboard shortcuts.

Besides the zombies, it also has some high tech stuff like bionics and aliens mixed in. And mods add other stuff, e.g. [https://cddawiki.chezzo.com/cdda_wiki/index.php?title=Magiclysm](https://cddawiki.chezzo.com/cdda_wiki/index.php?title=Magiclysm) which is quite cool. The design document/lore spoilers explain that this is the actual cause of te cataclysm: [https://cataclysmdda.org/lore-background.html](https://cataclysmdda.org/lore-background.html)

The cool thing about this type of game is that enemies are really powerful, which is so much more realistic. Even a single zombie has to be given lots of respect, especially since healing is a slow process like real life, and killing one feels like an achievement.

Some other cool points:
- [https://www.reddit.com/r/cataclysmdda/comments/3m92cc/are_worlds_truly_infinite/](https://www.reddit.com/r/cataclysmdda/comments/3m92cc/are_worlds_truly_infinite/) the map is truly infinite. Everything is persistent. They must freeze things in some state of course when the player is not around, and hydrate it (using [React.js](react-split.md)-like terminology!) when you come back, but they all look very plausibly continuous to how things where. They call the fully simulated world the "reality bubble": [https://cddawiki.chezzo.com/cdda_wiki/index.php?title=Reality_bubble](https://cddawiki.chezzo.com/cdda_wiki/index.php?title=Reality_bubble) That pages says though that not everything hydrates. Shame there are no oceans yet: [https://www.reddit.com/r/cataclysmdda/comments/huvnon/when_are_we_getting_oceans/](https://www.reddit.com/r/cataclysmdda/comments/huvnon/when_are_we_getting_oceans/)

  But there are lakes, and lake islands: [http://cddawiki.chezzo.com/cdda_wiki/index.php?title=Lake](http://cddawiki.chezzo.com/cdda_wiki/index.php?title=Lake) but they are quite rare on the mapgen, outside of fixed scenario starts.

  There could definitely be some more biome variety in the game though, e.g. hills, mountains, deserts, tropical forests, and so on. As it stands in 2021, the game is basically a USA midwest simulator. This is confirmed in the official design document: [https://cataclysmdda.org/lore-background.html](https://cataclysmdda.org/lore-background.html).

  Hills: [https://www.reddit.com/r/cataclysmdda/comments/ar9kam/hills_and_mountains/](https://www.reddit.com/r/cataclysmdda/comments/ar9kam/hills_and_mountains/)

  This also make the survival scenarios a bit ridiculous. Middle of nowhere means you walk a little bit out of the woods and you reach a huge shopping mall!

Tips for beginners:
- a [Reddit](reddit.md) list: [https://www.reddit.com/r/cataclysmdda/comments/hsxpco/things_you_wish_you_knew_when_you_started_playing/](https://www.reddit.com/r/cataclysmdda/comments/hsxpco/things_you_wish_you_knew_when_you_started_playing/)
- go to town at night, zombies are even blinder than you, it is possible to sneak by massive hoards, fighting one enemy at a time, even when they are well packed together. The only possible reason to go out during the day is to smash zombies with a car without crashing.
- favoriting items makes you not drop them by default with `,`. This is fundamental so you can drop loot while keeping survival stuff on you.
- indestructible and faster than you early game enemies, encounter means certain death: Survivor zombie, Giant cockroach, Giant wasp. Walking on trails is also potentially deadly, which is very annoying... sometimes you only see dealy enemies like wolves when you are on top of them on trails. Not sure what to do about that.
- pick up all items from any surrounding tile: `/`, then on left `I` for inventory, on right `A` for area. You can also examine items with `e` if not everything fits, and sort by category with `s`. That's the most important menu in the game!
- duffel bags are the best thing ever made, carry huge volumes, and you can craft them too!
- smash (`S`) zombie corpses after you kill them, or else they will re-raise after a few hours. They will be wounded and easy to kill however.
- [just like in real life](street-reclamation.md), cars are the ultimate killing machine. For some reason though, it does not smash zombie corpses. They can also carry infinite crap, after clearing up a town, you can just pick up EVERYTHING without thinking too much, just hit `,`. To bulk move things into/off a car, just hold Enter until the inventory is full. So sort huge piles by category: Shift + V then S:.
  - to get fuel from other cars, you need a rubber hose that can be easily obtained by smashing a refrigerator.
  - you can just siphon directly from one vehicle to another if you stop them close by, no need to go through containers every time!
  - you will learn where are good places to find cars:
    - bridges
    - prisons
    - mine entrance parking lots
    - car refueling/repair stations
  [Just like in real life](ciro-santilli-s-cycling.md), bicycles are pretty good if you can't find a working car, as they don't consume fuel, just stamina. You can even go around hordes if you are crazy enough, and try to look for working cars in towns, but going on the countryside would be wiser. Just make sure you always have enough stamina to cycle out to safety if your electric motor isn't working, which is often the case!

  Electric cars can also be recharged from the sun, which means they will never run out. They are generally not very strong, so not suitable for ramming, and the battery runs out relatively soon. But great to stop out of town.
- head encumbrance does not seem to do anything besides limit how many hats you can wear, so do ware that motorcycle helmet: [https://www.reddit.com/r/cataclysmdda/comments/a5nq6c/head_encumbrance/](https://www.reddit.com/r/cataclysmdda/comments/a5nq6c/head_encumbrance/)
- headlamps are a must
- on the overmap `m`, you can fast travel with `Shift + W` twice. Not perfect path finding, but saves a lot of useless clicking!
- on the EVAC shelter computer, contact us is not useless at all! It shows the nearest refugee center, and can show a lot of map because it shows the full road path there
- climb buildings to see further out. You can start by climbing the EVAC shelter via gutter with `>`! But to go down pipes you have to examine it, not `<`, it's weird. Edit: actually, you can "climb down" any ledge, so that's why. But you can still get hurt, so don't do it unless it is really necessary. You will want to carry the telescope, or a binoculars with you at all times most likely, as it is just a huge asset. You just can't climb back up without the water pipe. Radio tower and silos are other good buildings to climb, and radio towers often contain telescopes which allow you to see very very far, climbing those is a top priority when scouting a new region. Don't jump down, even of 1 floor, as it hurts you. A bit exaggerated, but so be it.
- you can grind fabrication easily to level 1 even without a book: [https://www.reddit.com/r/cataclysmdda/comments/6r2477/best_way_to_grind_fabrication/](https://www.reddit.com/r/cataclysmdda/comments/6r2477/best_way_to_grind_fabrication/) This is fundamental to make the all important brazier. And you'll learn that dumping things in the brazier unnecessarily burns them out, the uninsuitive "Construct" \> "Firewood Source" is a must.
- place brazier immediately outside of the EVAC shelter window, this way you avoid smoke problems, but can still cook from the inside.
- shopping carts are the very best mechanism to carry a lot of loot in town besides a car. And there's a foldable version that can fit into cars, but you have to craft it... [https://www.youtube.com/watch?v=kccBl7cksPY](https://www.youtube.com/watch?v=kccBl7cksPY). Most important item ever.
- there's a built-in debug menu that allows you to cheat whatever you want: spawn items, change your stats (e.g. 10000 strenght and smash through walls? no problem), learn skills, reveal map, and teleport. You have to bind a key to it before using it from `?`, `,` is a good bind candidate. Now that's real fun, being [God](god.md).
- auto-smash mode is a must
- you likely should look into spears: [https://www.reddit.com/r/cataclysmdda/comments/7m99jb/why_melee_with_anything_besides_spears/](https://www.reddit.com/r/cataclysmdda/comments/7m99jb/why_melee_with_anything_besides_spears/). Reach attacks from spears are OP, as you can hit a zombie, run, wait for it to come in range, hit from afar, run, and so on. Then after killing a zombie, you wait until your stamina recovered with `|`. This allows to safely kill anything as fast as you without taking hits. Wooden spear is a good first one, and it is not flimsy and lasts a while, like 30-50 zombies maybe. A pitch fork is another good option if you can find one.

How a typical early day looks like for a newbie: go to down, fight 5 zombies, get some stuff from houses, and run back home because your limbs are too weak and could break. Get home 10AM, and read the hole day and night. Repeat.

A fun play style is: get a car, clear out a small town with a library, bring food and books back to the base, fill the 4 60L tanks with water and bring them on the car as well, and then just read for several days until the food runs out. Repeat. It is not super serious if you don't have a car though, as even "shallow water" pools found in every forest can fill one of them. Exploitative mechanic BTW.

Top feature requests for [Ciro Santilli](ciro-santilli-split.md):
- [https://www.reddit.com/r/cataclysmdda/comments/2mni5z/can_i_store_items_in_a_backpack_and_drop_the/](https://www.reddit.com/r/cataclysmdda/comments/2mni5z/can_i_store_items_in_a_backpack_and_drop_the/). As of 0.E-3-1, drop happens automatically on Take off, but then you have to pick up items that go overweight/volume one by one.
- find items in my inventory by quality, or at least all item qualities in a single sortable table, otherwise it is too hard to know which item can do what
- fill all empty containers with something, e.g. water from a large pool into 25 plastic bottles
- view wound details without having to select bandage or antiseptic. `@` "EFFECTS" has a summary, but it is too tiny, that stats window should be fullscreen for sure
- realism requests. Ciro is a big fan of realism in CDDA, the more the better, and if you don't like something, just use the debug menu!
  - [shitting](feces.md)/[peeing](urine.md) system
  - when you wash clothes (currently important because zombie worn clothes that you pickup are generally filthy and reduce morale), make the clothes wet and require drying. There are even already some rotation clothes handers in houses, but just putting on a bench would be enough. And of course, higher temperatures mean faster drying, next to a fire would be ideal. Wearing wet clothes would of course make you cold and demoralized.
- exercise/fitness
  - [https://discourse.cataclysmdda.org/t/suggestion-fitness/25754](https://discourse.cataclysmdda.org/t/suggestion-fitness/25754)
  - [https://github.com/CleverRaven/Cataclysm-DDA/issues/44370](https://github.com/CleverRaven/Cataclysm-DDA/issues/44370)

TODO how to create a custom non random map/scenario? Possible from JSON: [https://discourse.cataclysmdda.org/t/guide-to-adding-new-content-to-cdda-for-first-time-modders/17781/13/](https://discourse.cataclysmdda.org/t/guide-to-adding-new-content-to-cdda-for-first-time-modders/17781/13/) ?

Their dominating Q&A communication channels are terrible, as of 2021 everything you google leads to: [https://www.reddit.com/r/cataclysmdda/](https://www.reddit.com/r/cataclysmdda/) which suffers from [online forums that lock threads after some time are evil](online-forums-that-lock-threads-after-some-time.md) (edit: this changed since). They've since made a discourse thankfully however: [https://discourse.cataclysmdda.org/](https://discourse.cataclysmdda.org/)

Source code overview:
- it is funny how the `lang/` directory with translations is by far the largest of the repo ta 100MB, way larger than `gfx`, it's comical

One of the things it simulates is some level of builing stuff:
- you can build a wooden house: [https://www.youtube.com/watch?v=QnCYGSlZ1gE](https://www.youtube.com/watch?v=QnCYGSlZ1gE) including floor, roof, windows. There are also concrete walls. Of course, building is useless, what you really want is a super mega truck that doubles as a home.
- you can dig water channels from rivers/lakes with a digging tool to bring water to your doorstep. TODO can you dig down deeper than "pit", minecraft style?

  OK, you can build a "Dig downstair" and it works. With a pickaxe you can carve stone sideways. With infinite cheated strength you can just mash the rock walls. The have salts and coal sometimes, funny. Upper floor does not collapse. TODO can't dig the second one "You cannot build here".
- TODO can you generate power e.g. in solar cells or not, and wire it into home appliances? [https://www.reddit.com/r/cataclysmdda/comments/4zm7tf/solar_panels_useless/](https://www.reddit.com/r/cataclysmdda/comments/4zm7tf/solar_panels_useless/) from 2016 says no.
  - [https://cddawiki.chezzo.com/cdda_wiki/index.php?title=Power](https://cddawiki.chezzo.com/cdda_wiki/index.php?title=Power) says yes "farmhouse kitchen running off of outside solar, cabled in"
  - [https://www.reddit.com/r/cataclysmdda/comments/9j9e16/wired_homes_and_electrical_systemgrid/](https://www.reddit.com/r/cataclysmdda/comments/9j9e16/wired_homes_and_electrical_systemgrid/) from 2018 says no due to fundamental reality bubble limitations, the only way is with power coming from stuff mounted on vehicles...
  The solution would be simple... just mark the edge incoming wire from the reality bubble as a magic source that has a given voltage/max amperage/total power or total wattage available. Would be good enough. Sure, some estimates might be hard, e.g. how much sun is there in a far away location of the map, etc. but just having some average of those values would be good enough. E.g. average temperature of an off bubble tile would also be useful to calculate food rotting time.

  A related obvious application would be refrigerators. [https://www.youtube.com/watch?v=G6B0KBJHvZs](https://www.youtube.com/watch?v=G6B0KBJHvZs) from 2021 mentions again that you can't have power without vehicles. TODO do the refrigerators in a powered 01 lab protect food?

  The fork [https://github.com/cataclysmbnteam/Cataclysm-BN](https://github.com/cataclysmbnteam/Cataclysm-BN) is actually trying to add an electric grid...

<a id="video-cataclysm-dark-days-ahead-review-by-ssethtzeentach-2018"></a>
**[Video 15](#video-cataclysm-dark-days-ahead-review-by-ssethtzeentach-2018). Cataclysm: Dark Days Ahead Review by SsethTzeentach (2018)** [Source](https://www.youtube.com/watch?v=Cyoj4-niEPc&amp;t=244s). This game really is right up Seth's alley, glad he tried it out. Perhaps his review was partly what motivated [Ciro Santilli](ciro-santilli-split.md) to give it a try. But the other part, perhaps even more important, was the joy of trying out crappy [open source video games](open-source-video-game.md). Ciro especially likes Seth's observation that you could just go all in Mad Max mode. Since vehicles are so powerful, you can just clean up towns with them and basic weapons, then either get a new vehicle when the old one goes bust, or at least very easily find gas. Another good observation is that crafting in this game is amazing.

**Table of contents**

- [Cataclysm DDA build from source on Ubuntu 21.10](cataclysm-dda-build-from-source-on-ubuntu-21-10.md)
- [Cataclysm DDA multiplayer](cataclysm-dda-multiplayer.md)
- [Cataclysm DDA save scum](cataclysm-dda-save-scum.md)
- [Cataclysm DDA on browser](cataclysm-dda-on-browser.md)

## ↑ Ancestors (6)

1. [Survival game](survival-game.md)
2. [Video game genre](video-game-genre.md)
3. [Video game](video-game-split.md)
4. [Game](game.md)
5. [Art](art-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)
- [Open source video game](open-source-video-game.md)
- [Not work](sponsor/updates/4/not-work.md)
