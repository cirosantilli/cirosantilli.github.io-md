# Build bsdgames from source

↑ **Parent:** [bsdgames](bsdgames.md)

Many of the games are disabled by default on [Ubuntu](ubuntu.md). But we can enable some games and build from source with:

```
apt-get source bsdgames
cd bsdgames-*
sed -ri '/^bsd_games_cfg_no_build_dirs=/s/ number / /' config.params
./configure
make -j
```

Here we enabled the game [number](number-bsdgames.md), so now we can:
```
number/number 123
```
which gives:
```
one hundred twenty-three.
```

We can also "install" it locally with:
```
make install
```
which puts the games locally under:
```
debian/bsdgames/usr/games/number
```
which you can add to your [`PATH` environment variable](path-environment-variable.md).

Tested on Ubuntu 24.04, bsdgames 2.17. 

## ↑ Ancestors (7)

1. [bsdgames](bsdgames.md)
2. [Text-based game](text-based-game.md)
3. [Video game graphics](video-game-graphics.md)
4. [Video game](video-game-split.md)
5. [Game](game.md)
6. [Art](art-split.md)
7. [Ciro Santilli's Homepage](split.md)
