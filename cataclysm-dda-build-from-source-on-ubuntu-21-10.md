<h1 id="cataclysm-dda-build-from-source-on-ubuntu-21-10">Cataclysm DDA build from source on Ubuntu 21.10</h1>

↑ **Parent:** [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)


```
sudo apt build-dep cataclysm-dda-curses cataclysm-dda-data cataclysm-dda-data
git clone https://github.com/CleverRaven/Cataclysm-DDA
cd Cataclysm-DDA
git checkout cdda-experimental-2022-01-27-0622
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release -DTILES=ON -DSOUND=ON -DLOCALIZE=OFF ..
make -j`nproc`
```
fails with:
```
:part_index_’ may be used uninitialized [-Werror=maybe-uninitialized]
   55 |             return part_index_;
```
as reported at: [https://github.com/CleverRaven/Cataclysm-DDA/issues/52657](https://github.com/CleverRaven/Cataclysm-DDA/issues/52657) now open for 3 months. Basically every commit I tried fails with a different `-Werror` check, they don't test GCC new enough regularly.

## ↑ Ancestors (7)

1. [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)
2. [Survival game](survival-game.md)
3. [Video game genre](video-game-genre.md)
4. [Video game](video-game-split.md)
5. [Game](game.md)
6. [Art](art-split.md)
7. [Ciro Santilli's Homepage](split.md)
