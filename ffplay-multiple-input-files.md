# ffplay multiple input files

↑ **Parent:** [ffplay](ffplay.md)

TODO possible? [https://superuser.com/questions/559768/ffplay-how-to-play-together-separate-video-and-audio-files](https://superuser.com/questions/559768/ffplay-how-to-play-together-separate-video-and-audio-files)

For synthesized streams like `sine` we can do it e.g.
```
ffplay -autoexit -nodisp -f lavfi -i '
sine=frequency=500[a];
sine=frequency=1000[b];
[a][b]amerge, atrim=end=2
'
```
but it does not seem to accept multiple `-i` for some reason. So is there a way to open a file from some filter? E.g.:
```
ffplay -i tmp.wav -i tmp.mkv -filter_complex "[0:a]atrim=end=2[a];[1:v]trim=end=2[v]" -map '[a]' -map '[v]'
```
fails with:
```
Argument 'tmp.mkv' provided as input filename, but 'tmp.wav' was already specified.
```

## ↑ Ancestors (9)

1. [ffplay](ffplay.md)
2. [FFmpeg](ffmpeg.md)
3. [Multimedia software](multimedia-software.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [ffplay](ffplay.md)
