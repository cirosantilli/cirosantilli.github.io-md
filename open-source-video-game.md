# Open source video game

↑ **Parent:** [Video game](video-game-split.md)  
🏷️ **Tags:** [Open source software](open-source-software.md)

Lists:
- [https://trilarion.github.io/opensourcegames/](https://trilarion.github.io/opensourcegames/)
- [https://www.slant.co/topics/1933/~best-open-source-games](https://www.slant.co/topics/1933/~best-open-source-games)
- [https://libregamewiki.org/Main_Page](https://libregamewiki.org/Main_Page)
- [https://www.reddit.com/r/opensourcegames/comments/197luuk/what_is_the_best_open_source_game_in_your_opinion/](https://www.reddit.com/r/opensourcegames/comments/197luuk/what_is_the_best_open_source_game_in_your_opinion/)
- [https://www.pcgamer.com/yall-know-about-these-huge-lists-of-free-open-source-game-clones-right/](https://www.pcgamer.com/yall-know-about-these-huge-lists-of-free-open-source-game-clones-right/) is a list of lists

Why would anyone ever waste time playing a closed source game, when this will inevitably lead to endless hours of decompilation down the line when you want to:
- fully understand how the game works, notably to help with [TASsing](tool-assisted-speedrun.md)
- improve the game's flaws as devs drop support ([or lose source code and have to later reverse-engineer their own fucking game](https://www.vg247.com/2018/09/14/isnt-ps4-xbox-switch-port-final-fantasy-8-preservation-may-answer/)?) :-)

Those who devote their time to the [useless](art-split.md) development of open source video games, [before we even have decent open source development tooling](integrated-development-environment.md), will, without a doubt, have their place in Heaven.

- tower defense
  - [https://www.edopedia.com/demo/pixeldefense](https://www.edopedia.com/demo/pixeldefense) possible source [https://github.com/jesseakt/PixelDefense](https://github.com/jesseakt/PixelDefense) 2020-03 desperately lacks a fast forward button and enemy health bars
- platformer
  - 2D platformer
    - teeworlds: does not run on Ubuntu 21.10, `X Error of failed request:  BadValue`
  - 3D platformer
    - [http://edelweiss.32x.io/](http://edelweiss.32x.io/)
- OpenClonk: Terraria-like 2D mining crafting game. Pretty well done. Not sure if you can have a super huge open world. The fact that the music stops completely so often is a bit saddening.
- [Pingus](https://en.wikipedia.org/wiki/Pingus): Lemmings clone. Very good!
- [https://github.com/The-Powder-Toy/The-Powder-Toy](https://github.com/The-Powder-Toy/The-Powder-Toy): [https://en.wikipedia.org/wiki/Falling-sand_game](https://en.wikipedia.org/wiki/Falling-sand_game) in C++. No Ubuntu 19.10 package it seems, but was easy to compile from source.
- [roguelike](roguelike.md)
  - [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)
- [Worms](worms-series.md) clone
  - Hedgewars
- pokemon clone:
  - Tuxemon. Worked on [Ubuntu 21.10](ubuntu-21-10.md). 20ea4181e1c0db04934ee69951ea1836a3b1f642
- ARPG
  - [Diablo II](diablo-ii.md) clones:
    - [https://github.com/flareteam/flare-game](https://github.com/flareteam/flare-game) game engine
    - [https://flarerpg.org/mods/flare-empyrean/](https://flarerpg.org/mods/flare-empyrean/) game made with the engine

    v1.12 download Worked well on [Ubuntu 21.10](ubuntu-21-10.md).
  - The Mana World: [https://www.themanaworld.org/](https://www.themanaworld.org/) Started somewhat as a loose The Secret of Mana clone, but they've added online play capabilities, effectively making it a [MMORPG](mmorpg.md).

    Their user acquisition as of 2021 is really bad. Download is a wiki page, there are two client versions, etc. The .deb did not work out o box on [Ubuntu 21.10](ubuntu-21-10.md) due to unmet dependencies:
    ```
    sudo apt install ./manaplus_amd64.deb
    ```
    fails with:
    ```
    manaplus : Depends: libpng12-0 (>= 1.2.13-4) but it is not installable
                Depends: libsdl-gfx1.2-4 (>= 2.0.22) but it is not installable
                Depends: manaplus-data (= 1.6.4.23-2) but 1.9.3.23-6 is to be installed
    ```
    so it won't be able to play without trying to compile and possibly minor ports since the deb does not packs dependencies. Some requests for a release with [all dependencies prepacked](cross-distro-package-manager.md):
    - [https://gitlab.com/manaplus/manaplus/-/issues/9](https://gitlab.com/manaplus/manaplus/-/issues/9)
    - [https://gitlab.com/manaplus/manaplus/-/issues/2](https://gitlab.com/manaplus/manaplus/-/issues/2)
    Their home page says it all:

    > Server status: Online: 9 players

    Sad.
- [Factorio](factorio.md) clones:
  - [https://github.com/tobspr/shapez.io](https://github.com/tobspr/shapez.io) Also browser based.

YouTube review channels:
- [https://www.youtube.com/c/OpenSourceGames](https://www.youtube.com/c/OpenSourceGames)

**Table of contents**

- [Open source video game library](open-source-video-game-library.md)
  - [Simple DirectMedia Layer](simple-directmedia-layer.md)
- [Open source video game asset](open-source-video-game-asset.md)
  - [game-icons.net](game-icons-net.md)

## 🏷️ Tagged (6)

- [Biomes (game)](biomes-game.md)
- [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)
- [Mindustry](mindustry.md)
- [Minetest](minetest.md)
- [Open source racing game](open-source-racing-game.md)
- [SuperTuxKart](supertuxkart.md)

## ↑ Ancestors (4)

1. [Video game](video-game-split.md)
2. [Game](game.md)
3. [Art](art-split.md)
4. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)
- [Video game](video-game-split.md)
