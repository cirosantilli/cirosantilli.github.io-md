# FFmpeg sound synthesis

↑ **Parent:** [FFmpeg](ffmpeg.md)

Simple [sines](sine.md) and variants:
- [https://unix.stackexchange.com/questions/82112/stereo-tone-generator-for-linux/536860#536860](https://unix.stackexchange.com/questions/82112/stereo-tone-generator-for-linux/536860#536860)
- [https://stackoverflow.com/questions/5109038/linux-sine-wave-audio-generator/57610684#57610684](https://stackoverflow.com/questions/5109038/linux-sine-wave-audio-generator/57610684#57610684)
- [https://superuser.com/questions/724391/how-to-generate-a-sine-wave-with-ffmpeg](https://superuser.com/questions/724391/how-to-generate-a-sine-wave-with-ffmpeg)
- [https://stackoverflow.com/questions/59551013/how-to-generate-stereo-sine-wave-using-ffmpeg-with-different-frequencies-for-eac/77730492#77730492](https://stackoverflow.com/questions/59551013/how-to-generate-stereo-sine-wave-using-ffmpeg-with-different-frequencies-for-eac/77730492#77730492)

2 second 1000 Hz:
```
ffmpeg -f lavfi -i "sine=f=1000:d=2" out.wav
```

## ↑ Ancestors (8)

1. [FFmpeg](ffmpeg.md)
2. [Multimedia software](multimedia-software.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Ciro Santilli's Stack Overflow contributions](ciro-santilli-s-stack-overflow-contributions.md)
