# Dungeon Crawl Stone Soup

↑ **Parent:** [Roguelike](roguelike.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dungeon_Crawl_Stone_Soup)

Appears to be _the_ best classic open source [roguelike](roguelike.md) of the 2020's.

This website is really cool! [http://crawl.akrasiac.org:8080/#lobby](http://crawl.akrasiac.org:8080/#lobby) You can spectate players live and chat! Also has statistics.

Devs of this game are smart, they have one good in-tree [tileset](tileset.md), unlike some other [text-based games](text-based-game.md) that didn't have an in-tree option...

Build on [Ubuntu 21.10](ubuntu-21-10.md):
```
sudo apt install build-essential libncursesw5-dev bison flex liblua5.1-0-dev \
libsqlite3-dev libz-dev pkg-config python3-yaml binutils-gold python-is-python3 \
libsdl2-image-dev libsdl2-mixer-dev libsdl2-dev libfreetype6-dev libpng-dev \
fonts-dejavu-core advancecomp pngcrush

git clone --depth 1 --branch 0.28.0 https://github.com/crawl/crawl
cd crawl/crawl-ref/source
echo 0.28-a > util/release_ver
make -j`nproc` TILES=y
./crawl
```

This launches the UI version already for you.

## ↑ Ancestors (7)

1. [Roguelike](roguelike.md)
2. [Role-playing video game](role-playing-video-game.md)
3. [Video game genre](video-game-genre.md)
4. [Video game](video-game-split.md)
5. [Game](game.md)
6. [Art](art-split.md)
7. [Ciro Santilli's Homepage](split.md)
