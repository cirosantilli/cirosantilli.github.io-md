# ZynAddSubFX

↑ **Parent:** [Software synthesizer](software-synthesizer.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ZynAddSubFX)

[https://askubuntu.com/questions/220802/no-sound-zynaddsubfx-and-jack-wont-run/1297988#1297988](https://askubuntu.com/questions/220802/no-sound-zynaddsubfx-and-jack-wont-run/1297988#1297988)

Contains a large database of instruments, and allows you to edit them. This is a fun toy.

Instruments are edited on a [GUI](graphical-user-interface.md). It is a multi-window program, and you open new windows from new windows from new windows, all filled with hundreds of virtual knobs that you drag with your keyboard, and which would be better done from textual software like [Csound](csound.md). It is a thing of beauty.

It does not seem possible to program arbitrary [modular synthesizer](modular-synthesizer.md) circuits therefore. But if you understand [additive synthesis](additive-synthesis.md) and [subtractive synthesis](subtractive-synthesis.md) well, you can make some funky sounds with it.

It is basically a superset of all popular [hardware synthesizers](hardware-synthesizer.md) ever made.

Has its own built-in MIDI keyboard which is nice.

On Ubuntu 20.04 Version: 3.0.5:
```
sudo apt install zynaddsubfx
zynaddsubfx -O alsa
```
as per [https://askubuntu.com/questions/220802/no-sound-zynaddsubfx-and-jack-wont-run/1297988#1297988](https://askubuntu.com/questions/220802/no-sound-zynaddsubfx-and-jack-wont-run/1297988#1297988)  
To do anything of interest, switch to the Advanced UI:
- Misc
- Switch Interface Mode

The UI is completely different form what is shown on the website as of 2020: [https://zynaddsubfx.sourceforge.io/](https://zynaddsubfx.sourceforge.io/), it looks instead like: [https://www.youtube.com/watch?v=iVPr6iUuO3g](https://www.youtube.com/watch?v=iVPr6iUuO3g) Maybe on the website it is the new zyn-fusion UI... [https://www.reddit.com/r/linuxaudio/comments/bxn3ur/some_help_for_installing_zynfusion_zynaddsubfx/](https://www.reddit.com/r/linuxaudio/comments/bxn3ur/some_help_for_installing_zynfusion_zynaddsubfx/) so confusing.

And they have some crappy policy of asking for 45 USD for binary downloads.

Compiling from source:
```
git clone https://github.com/zynaddsubfx/zynaddsubfx
cd zynaddsubfx
git checkout a789866de4d45a784c1f4d95fcf5a1938347baef
sudo apt build-dep zynaddsubfx
mkdir build
cd build
cmake ..
make -j`nproc`
```
fails with:
```
Traceback (most recent call last):
  File "/usr/bin/cxxtestgen", line 7, in <module>
    import cxxtest.cxxtestgen
  File "/usr/share/cxxtest/cxxtest/__init__.py", line 33, in <module>
    from cxxtest.cxxtestgen import *
  File "/usr/share/cxxtest/cxxtest/cxxtestgen.py", line 18, in <module>
    import __release__
ModuleNotFoundError: No module named '__release__'
```
Ciro gives up for now.

## ↑ Ancestors (5)

1. [Software synthesizer](software-synthesizer.md)
2. [Computer music](computer-music.md)
3. [Music](music-split.md)
4. [Art](art-split.md)
5. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Advanced Linux Sound Architecture](advanced-linux-sound-architecture.md)
- [Evil](evil.md)
- [LMMS](lmms.md)
