# Super Mario 64 reverse engineering project

↑ **Parent:** [Super Mario 64](super-mario-64.md)  
🏷️ **Tags:** [Video game decompilation](video-game-decompilation.md)

[https://github.com/MitchellSternke/SuperMarioBros-C](https://github.com/MitchellSternke/SuperMarioBros-C)

OMG, both of those just [fucking](sexual-intercourse.md) work on [Ubuntu 20.04](ubuntu-20-04.md) with README instructions, it is unbelievable, those people don't have lives. And it builds the ROM [byte by byte equal from source](reproducible-builds.md)!

There are a few different versions:
- [https://github.com/n64decomp/sm64](https://github.com/n64decomp/sm64) for [emulator](emulator.md) (i.e. or real hardware), tested at 9214dddabcce4723d9b6cda2ebccbac209f6447d
- [https://github.com/sm64-port/sm64-port](https://github.com/sm64-port/sm64-port) [Ubuntu](ubuntu.md) native, tested at 6b47859f757a40096fedd6237f2bc3573d0bc2a4

  Full screen with F10.
- [https://github.com/sm64pc/sm64ex](https://github.com/sm64pc/sm64ex): fork of sm64-port, untested by [Ciro Santilli](ciro-santilli-split.md), but more new amazing usability features, notably:


  - `--skip-intro`: skips the annoying pipe intro and the need to wait for Lakitu to bring Peaches message!
  - in-game menu:
    - cheats:
    - hide HUD!
  - no level selection yet, but a matter of time?
    - [https://github.com/sm64pc/sm64ex/pull/417](https://github.com/sm64pc/sm64ex/pull/417)
    - [https://github.com/sm64pc/sm64ex/pull/402](https://github.com/sm64pc/sm64ex/pull/402)
    - [https://github.com/sm64pc/sm64ex/issues/425](https://github.com/sm64pc/sm64ex/issues/425)
    - [https://github.com/sm64pc/sm64ex/issues/424](https://github.com/sm64pc/sm64ex/issues/424)

  Also reported to work on ARM: [https://www.reddit.com/r/linux/comments/ityg6w/pinephone_playing_super_mario_64_30fps/](https://www.reddit.com/r/linux/comments/ityg6w/pinephone_playing_super_mario_64_30fps/)

  They also ported to browser with Emscripten: [https://github.com/sm64pc/sm64ex/wiki/Compiling-for-the-web](https://github.com/sm64pc/sm64ex/wiki/Compiling-for-the-web)

Tested with the USA ROM at [sha1sum](sha1sum.md) 9bef1128717f958171a4afac3ed78ee2bb4e86ce (you need a ROM to extract assets, which the project automates), which is also documented in the project itself: [https://github.com/sm64-port/sm64-port/blob/6b47859f757a40096fedd6237f2bc3573d0bc2a4/sm64.us.sha1](https://github.com/sm64-port/sm64-port/blob/6b47859f757a40096fedd6237f2bc3573d0bc2a4/sm64.us.sha1). Disclaimer: [Ciro Santilli](ciro-santilli-split.md) owns a copy of [Super Mario 64](super-mario-64.md).

The only dependency missing from Ubuntu packages is the [IRIX](https://en.wikipedia.org/wiki/IRIX) [QEMU](qemu.md) [user mode](https://cirosantilli.com/linux-kernel-module-cheat/#user-mode-simulation) which they need for their tooling. The project also has a QEMU fork for that, and provide a working deb.

From this project it was also noticed that certain ROM releases were not compiled with optimizations enabled, presumably because as a release title the compiler had optimization bugs! [https://www.resetera.com/threads/so-apparently-the-ntsc-build-of-mario-64-didnt-use-any-compiler-optimizations.166277/](https://www.resetera.com/threads/so-apparently-the-ntsc-build-of-mario-64-didnt-use-any-compiler-optimizations.166277/) But now they do have a working compiler, and by turning that switch FPS increases in certain levels!!!

It is good to know that this game will "never die".

Some quick stupid patches:

- jump really high:

  ```
  diff --git a/src/game/mario.c b/src/game/mario.c
  index 5b103fa..83c9f40 100644
  --- a/src/game/mario.c
  +++ b/src/game/mario.c
  @@ -826,7 +826,7 @@ static u32 set_mario_action_airborne(struct MarioState *m, u32 action, u32 actio
           case ACT_JUMP:
           case ACT_HOLD_JUMP:
               m->marioObj->header.gfx.unk38.animID = -1;
  -            set_mario_y_vel_based_on_fspeed(m, 42.0f, 0.25f);
  +            set_mario_y_vel_based_on_fspeed(m, 200.0f, 0.25f);
               m->forwardVel *= 0.8f;
               break;
  ```

Interesting entry points:
- `src/game/game_init.c`

TODO: enable the level select debug feature! [https://tcrf.net/Super_Mario_64_(Nintendo_64)/Debug_Content#Classic_Debug_Display](https://tcrf.net/Super_Mario_64_(Nintendo_64)/Debug_Content#Classic_Debug_Display) They actually shipped quite a few debug features into the retail game, and they have been reversed too. I tried this but it didn't work (or I don't know how to enable the level select menu):
```
diff --git a/src/game/main.c b/src/game/main.c
index 9e53e50..b7443a8 100644
--- a/src/game/main.c
+++ b/src/game/main.c
@@ -65,7 +65,7 @@ s8 sAudioEnabled = 1;
 u32 sNumVblanks = 0;
 s8 gResetTimer = 0;
 s8 D_8032C648 = 0;
-s8 gDebugLevelSelect = 0;
+s8 gDebugLevelSelect = 1;
 s8 D_8032C650 = 0;

 s8 gShowProfiler = FALSE;
```

The `enhancements/` folder contains a few sample patches.

<a id="image-screenshot-of-mupen64plus-running-on-ubuntu-20-04-emulating-super-mario-64-with-the-title-screen-hacked-by-ciro-santilli-based-on-the-super-mario-64-reverse-engineering-project"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/Screenshot_of_Mupen64Plus_running_on_Ubuntu_20.04_emulating_Super_Mario_64_with_the_title_screen_hacked_by_Ciro_Santilli.png" alt="" height="500">

**[Figure 5](#image-screenshot-of-mupen64plus-running-on-ubuntu-20-04-emulating-super-mario-64-with-the-title-screen-hacked-by-ciro-santilli-based-on-the-super-mario-64-reverse-engineering-project). Screenshot of mupen64Plus running on Ubuntu 20.04 emulating Super Mario 64 with the title screen hacked by Ciro Santilli based on the Super Mario 64 reverse engineering project**. The title was on a string, so the hack was trivial! The patch used was:
```
diff --git a/include/text_strings.h.in b/include/text_strings.h.in
index 749179b..626f87e 100644
--- a/include/text_strings.h.in
+++ b/include/text_strings.h.in
@@ -131,7 +131,7 @@
  */
 // Main Screens
 #define TEXT_MARIO _("MARIO") // View Score Menu
-#define TEXT_SELECT_FILE _("SELECT FILE")
+#define TEXT_SELECT_FILE _("HACKED BY CIRO")
 #define TEXT_CHECK_FILE _("CHECK FILE")
 #define TEXT_COPY_FILE _("COPY FILE")
 #define TEXT_ERASE_FILE _("ERASE FILE")
```

---

Some tutorials of hacking it:
- [https://www.youtube.com/watch?v=Jkb7Naczoww](https://www.youtube.com/watch?v=Jkb7Naczoww) SM64 Decomp Tutorial 1: Setting Up and First Code Changes by Bitlytic (2021)
- [https://www.youtube.com/watch?v=IuIpqX4neWg](https://www.youtube.com/watch?v=IuIpqX4neWg) Rovert Decomp Tech Demo by Rovert (2019) Metal cap makes Mario huge.
- [https://www.youtube.com/watch?v=5aG1Iyjo20w](https://www.youtube.com/watch?v=5aG1Iyjo20w) Is it Possible to Beat Super Mario 64 as Tiny Mario? (Mini Mario Challenge) coverts the obvious make Mario huge/tiny hack. Huge mario verion: [https://www.youtube.com/watch?v=pR_gol6zlIo](https://www.youtube.com/watch?v=pR_gol6zlIo). There was a pre-decompilation ROM hack doing that trivial change already: Tiny Huge Mario 64. Sample [tool-assisted speedrun](tool-assisted-speedrun.md): [https://www.youtube.com/watch?v=C7BjzZ_Nkk0](https://www.youtube.com/watch?v=C7BjzZ_Nkk0)

<a id="video-fixing-the-entire-sm64-source-code-by-kaze-emanuar-2022"></a>
**[Video 12](#video-fixing-the-entire-sm64-source-code-by-kaze-emanuar-2022). FIXING the ENTIRE SM64 Source Code by Kaze Emanuar (2022)** [Source](https://www.youtube.com/watch?v=t_rzYnXEQlE). Now that we have the source, [modders](video-game-modding.md) like this are going nuts.

## ↑ Ancestors (10)

1. [Super Mario 64](super-mario-64.md)
2. [Nintendo 64 game](nintendo-64-game.md)
3. [Nintendo 64](nintendo-64.md)
4. [Nintendo video game console](nintendo-video-game-console.md)
5. [Nintendo](nintendo.md)
6. [Video game console company](video-game-console-company.md)
7. [Video game](video-game-split.md)
8. [Game](game.md)
9. [Art](art-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Reverse engineering](reverse-engineering.md)
- [Super Mario 64 reverse engineering project](super-mario-64-reverse-engineering-project.md)
- [Tool-assisted speedrun](tool-assisted-speedrun.md)
