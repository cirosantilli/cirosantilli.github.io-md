# Csound

↑ **Parent:** [Text-based music synthesizer](text-based-music-synthesizer.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Csound)

[https://www.csounds.com/](https://www.csounds.com/)

[https://github.com/csound/csound](https://github.com/csound/csound)

[XML](xml.md) file format (but with 99% of the action of interest in a [domain-specific language](domain-specific-language.md) on the `CsInstruments` and `CsScore` elements) that can be played and the reference implementation. Offers complex effects out-of-box apparently.

Allows you to easily define instruments with seemingly arbitrary mathematical functions, and then use them to play notes at given time intervals.

The instrument functions can be parametrized, and each note played can have different parameters.

The instrument definition actually defines a block diagram graph, much like a hardware synthesizer would.

Csound is so not-bloated that it contains an UI system. And it includes an interactive virtual MIDI keyboard that interacts with parameter knobs: [http://www.csounds.com/manual/html/MidiTop.html](http://www.csounds.com/manual/html/MidiTop.html)

But hey, it's fun. And like any other good [domain-specific language](domain-specific-language.md), [debugging](debugging.md) it is barbaric of course.

If only it had been written in [Python](python-programming-language.md)... the array manipulation boilerplate would be likely perfect for [NumPy](numpy.md), and this would have been exactly what [Ciro Santilli](ciro-santilli-split.md) wanted!

CSound states that one of its design goals is backward compatibility, and it shows. Some of the stuff is utterly arcane, e.g. you have to remember what `GEN10`, `GEN11`, etc. mean instead of having named enums.

It just worked on [Ubuntu](ubuntu.md) 20.04 no questions asked:
```
sudo apt install csound
git clone https://github.com/csound/csound
cd csound
git checkout 92409ecce053d707360a5794f5f4f6bf5ebf5d24
csound examples/xanadu.csd
```
which runs this file: [https://github.com/csound/csound/blob/92409ecce053d707360a5794f5f4f6bf5ebf5d24/examples/xanadu.csd](https://github.com/csound/csound/blob/92409ecce053d707360a5794f5f4f6bf5ebf5d24/examples/xanadu.csd) and this plays a relly cool sound demo:<a id="video-xanadu-csound-demo"></a>


**[Video 2](#video-xanadu-csound-demo). Xanadu Csound demo.** [Source](https://www.youtube.com/watch?v=7fXhVMDCfaA).

Save to file instead of playing:
```
csound -o xanadu.wav xanadu.csd
```
or direct ogg output:
```
csound --ogg -o xanadu.ogg xanadu.csd
```
or pipe to stdout to [FFmpeg](ffmpeg.md) TODO: [https://stackoverflow.com/questions/64970503/how-to-pipe-csound-output-to-ffmpeg-for-conversion-without-an-intermediate-file](https://stackoverflow.com/questions/64970503/how-to-pipe-csound-output-to-ffmpeg-for-conversion-without-an-intermediate-file)

TODO find the most amazing set of songs made with it on GitHub? Some examples:
- [http://www.csounds.com/toots/index.html](http://www.csounds.com/toots/index.html) has a good 101 on instrument design
- [Csound FLOSS manual](csound-floss-manual.md)
- [http://iainmccurdy.org/csound.html](http://iainmccurdy.org/csound.html) about 100 [CC BY-SA](cc-by-sa.md) examples. Each is a minimal study showing a specific technique, not a full composition, some seem advanced. Dude's a beast.
- [https://github.com/csound/csound/tree/f2e70825fb543a6b15011c6984371f61ab2a00dd/tests/soak](https://github.com/csound/csound/tree/f2e70825fb543a6b15011c6984371f61ab2a00dd/tests/soak) in-tree minimal examples
- [https://github.com/csound/manual/tree/4049b286493d972ff7248b5596e47e7ae97a0cf9/examples](https://github.com/csound/manual/tree/4049b286493d972ff7248b5596e47e7ae97a0cf9/examples) contains the examples for the manual which is rendered at: It's insane, but it's fun!  Ah those newbs who separate manuals from main tree.
- [http://linuxsynths.com/CsoundPatchesDemos/csound.html](http://linuxsynths.com/CsoundPatchesDemos/csound.html) on [LinuxSynths](linuxsynths.md)
- [https://github.com/csound/examples/tree/ae578159328178142c1055c7f78e28b42eb29774/csd](https://github.com/csound/examples/tree/ae578159328178142c1055c7f78e28b42eb29774/csd) as a few dozen examples
- [http://freaknet.org/martin/audio/csound/](http://freaknet.org/martin/audio/csound/) 10 pieces with source

Documentation-wise, it's a bit lacking. The only dude who can explain it really well, Dr [Richard Boulanger](https://en.wikipedia.org/wiki/Richard_Boulanger), made the "The Csound Book" [closed source](closed-source-software.md), so, congrats, this will forever hurt the popularity of Csound.

Examples:
- [csound/sine.csd](csound/sine.csd)
- [csound/amplitude_frequency.csd](csound/amplitude_frequency.csd)
- [csound/linen.csd](csound/linen.csd): simple attack/release [envelope](envelope-music.md), documented at: [http://www.csounds.com/manual/html/linen.html](http://www.csounds.com/manual/html/linen.html)
- [csound/chorus.csd](csound/chorus.csd): [chorus effect](chorus-effect.md)
- [csound/bend.csd](csound/bend.csd): bend using `linseg`
- [csound/vibrato.csd](csound/vibrato.csd)
- [csound/crossfade_generators.csd](csound/crossfade_generators.csd)
- [csound/table.csd](csound/table.csd)
- [csound/virtual_keyboard.csd](csound/virtual_keyboard.csd)

**Table of contents**

- [Csound FLOSS manual](csound-floss-manual.md)
- [CsoundQt](csoundqt.md)
- [Cabbage (Csound)](cabbage-csound.md)

## ↑ Ancestors (6)

1. [Text-based music synthesizer](text-based-music-synthesizer.md)
2. [Software synthesizer](software-synthesizer.md)
3. [Computer music](computer-music.md)
4. [Music](music-split.md)
5. [Art](art-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (7)

- [Csound FLOSS manual](csound-floss-manual.md)
- [Minimoog](minimoog.md)
- [MusicXML](musicxml.md)
- [Rosegarden](rosegarden.md)
- [SoundFont](soundfont.md)
- [SuperCollider](supercollider.md)
- [ZynAddSubFX](zynaddsubfx.md)
