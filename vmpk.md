# vmpk

↑ **Parent:** [MIDI](midi.md)

[https://vmpk.sourceforge.io/](https://vmpk.sourceforge.io/)

Opens a virtual [MIDI](midi.md) piano [GUI](graphical-user-interface.md). It just works on [Ubuntu](ubuntu.md) 20.04: [https://askubuntu.com/questions/34391/virtual-midi-piano-keyboard-setup/1298026#1298026](https://askubuntu.com/questions/34391/virtual-midi-piano-keyboard-setup/1298026#1298026)

VMPK is a virtual device that replicates what you would get by connecting a physical MIDI keyboard to your computer. It is not a [software synthesizer](software-synthesizer.md) on its own. But it does connect to a working synthesizer by default (Sonivox EAS) which makes it produce sounds out-of-the box.

TODO: then I messed with my sound settings, and then it stopped working by default on the default "MIDI Connection" \> "MIDI Out Driver" \> "Network". But it still works on "SonivoxEAS".

A [hello world](hello-world-program.md) of actually connecting it to a specific software synthesizer manually on [Advanced Linux Sound Architecture](advanced-linux-sound-architecture.md) with `aconnect` can be found at: [https://askubuntu.com/questions/34391/virtual-midi-piano-keyboard-setup/1298026#1298026](https://askubuntu.com/questions/34391/virtual-midi-piano-keyboard-setup/1298026#1298026)

Save to a [MIDI](midi.md) file: [https://askubuntu.com/questions/709673/save-as-midi-when-playing-from-vmpk-qsynth/1298231#1298231](https://askubuntu.com/questions/709673/save-as-midi-when-playing-from-vmpk-qsynth/1298231#1298231)

Reasonable default key mappings to keyboard covering 2 octaves.

3 multiple simultaneous keys did not work (tested "ZQI"). This might just be a limitation of [my keyboard](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md) however.

TODO how to save to a `.mid` file? [https://askubuntu.com/questions/709673/save-as-midi-when-playing-from-vmpk-qsynth](https://askubuntu.com/questions/709673/save-as-midi-when-playing-from-vmpk-qsynth)

[SourceForge](sourceforge.md).

## ↑ Ancestors (9)

1. [MIDI](midi.md)
2. [List of audio file formats](list-of-audio-file-formats.md)
3. [Audio file format](audio-file-format.md)
4. [File format](file-format.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (5)

- [Advanced Linux Sound Architecture](advanced-linux-sound-architecture.md)
- [Ardour (software)](ardour-software.md)
- [FluidSynth](fluidsynth.md)
- [LMMS](lmms.md)
- [SoundFont](soundfont.md)
