# Kdenlive

↑ **Parent:** [Video editing software](video-editing-software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kdenlive)

This seems like a decent option, although it has bugs coming in and out all the time! Also it is quite hard to learn to use.

To get started:
- import a clip
- drag it onto the track area

Shortucts:
- Shift + R: cut tracks at current point. You can then select fragments to move around or delete.
- Shift mouse click drag: select multiple clips: [https://video.stackexchange.com/questions/21598/select-range-of-clips-in-kdenlive](https://video.stackexchange.com/questions/21598/select-range-of-clips-in-kdenlive)

To set the video length, search for "set outpoint" on "monitor".

Add subtitles:
- Effects
- Dynamic text
then drag on top of the video track. To add only to part of the video, cut it up first.

Preview has no sound on [Ubuntu](ubuntu.md) 20.10. Fixed as of [Ubuntu 22.04](ubuntu-22-04.md).

Sound worked on Ubuntu 21.04 though, but it then soon crashed with:


```
 = = SET EFFECT PARAM:  "rect"  =  0=1188 0 732 242
MUTEX LOCK!!!!!!!!!!!! slotactivateeffect:  1
// // // RESULTING REQUIRED SCENE:  1
Object 0x557293592da0 destroyed while one of its QML signal handlers is in progress.
Most likely the object was deleted synchronously (use QObject::deleteLater() instead), or the application is running a nested event loop.
This behavior is NOT supported!
qrc:/qml/EffectToolBar.qml:80: function() { [native code] }
Killed
```
amazing.

On Ubuntu 22.04 haven't crashed yet.

[Ubuntu 23.04](ubuntu-23-04.md) broke the clip drag and drop!
- [https://askubuntu.com/questions/1464992/cant-drag-clip-to-timeline-in-kdenlive-in-ubuntu-23-04/1469359#1469359](https://askubuntu.com/questions/1464992/cant-drag-clip-to-timeline-in-kdenlive-in-ubuntu-23-04/1469359#1469359)
- [https://gitlab.gnome.org/GNOME/mutter/-/issues/2715#note_1753579](https://gitlab.gnome.org/GNOME/mutter/-/issues/2715#note_1753579)
- [https://www.reddit.com/r/kdenlive/comments/12x0t6s/kdenlive_drag_and_drop_not_working/](https://www.reddit.com/r/kdenlive/comments/12x0t6s/kdenlive_drag_and_drop_not_working/)

## ↑ Ancestors (8)

1. [Video editing software](video-editing-software.md)
2. [Video file format](video-file-format.md)
3. [File format](file-format.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Translation of Xi Jinping saying those against raise their hands](updates/translation-of-xi-jinping-saying-those-against-raise-their-hands.md)
- [Two Linux Kernel Module Cheat videos](updates/two-linux-kernel-module-cheat-videos.md)
