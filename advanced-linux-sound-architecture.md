# Advanced Linux Sound Architecture

↑ **Parent:** [Linux audio system](linux-audio-system.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Advanced_Linux_Sound_Architecture)

ALSA can be thought as analogous to  physical wires linking up machines.

Except that instead of machines, you have separate programs. One such typical link is:
- from a MIDI source, e.g. [vmpk](vmpk.md) or a [MIDI](midi.md) editor with playback like [Ardour](ardour-software.md)
- to a synthesizer like [FluidSynth](fluidsynth.md) or [ZynAddSubFX](zynaddsubfx.md)

The advantage of this setup is that separate programs can collaborate to make complex sounds. 

The disadvantage of this setup is that it makes it very hard to reproduce results, you basically need a [Docker](docker-software.md) image with the exact same version of everything. And some script to launch and connect all programs correctly.

Some composition systems like [LMMS](lmms.md) reduce that problem by having synthesizers as plugins, so that you don't have to setup any connections yourself.

`aconnect` [vmpk](vmpk.md) [hello world](hello-world-program.md): [https://askubuntu.com/questions/34391/virtual-midi-piano-keyboard-setup/1298026#1298026](https://askubuntu.com/questions/34391/virtual-midi-piano-keyboard-setup/1298026#1298026)

## ↑ Ancestors (5)

1. [Linux audio system](linux-audio-system.md)
2. [Computer music](computer-music.md)
3. [Music](music-split.md)
4. [Art](art-split.md)
5. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [FluidSynth](fluidsynth.md)
- [vmpk](vmpk.md)
