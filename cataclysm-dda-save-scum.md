# Cataclysm DDA save scum

↑ **Parent:** [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)

Tested as of Cataclysm: Dark Days Ahead 0.E-3-1, seems possible built-in:
- Disable autosave on settings
- Quisave (Esc + 9)
- To restore the save, just close the game window directly before clicking Yes or No on the "Watch the last moments of your life" dialog.

A less risky save scum can be achieved with [rsync](rsync.md):
```
rsync -av ~/.local/share/cataclysm-dda/save/ ~/.local/share/cataclysm-dda/save.bak/
```
and after you die:
```
rsync -av ~/.local/share/cataclysm-dda/save.bak/ ~/.local/share/cataclysm-dda/save/
```

## ↑ Ancestors (7)

1. [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)
2. [Survival game](survival-game.md)
3. [Video game genre](video-game-genre.md)
4. [Video game](video-game-split.md)
5. [Game](game.md)
6. [Art](art-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Cataclysm: Dark Days Ahead](cataclysm-dark-days-ahead.md)
