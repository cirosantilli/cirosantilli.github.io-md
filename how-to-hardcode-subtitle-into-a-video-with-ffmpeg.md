# How to hardcode subtitle into a video with FFmpeg?

↑ **Parent:** [Subtitle](subtitle.md)

- [https://superuser.com/questions/869248/hardcoding-subs-with-ffmpeg](https://superuser.com/questions/869248/hardcoding-subs-with-ffmpeg)
- [https://askubuntu.com/questions/485100/how-may-i-burn-srt-subtitles-to-video-with-avconv](https://askubuntu.com/questions/485100/how-may-i-burn-srt-subtitles-to-video-with-avconv)

On [Ubuntu](ubuntu.md) 20.10, just:
```
ffmpeg -i input.mp4 -vf "subtitles=subtitle.srt" output.mp4
```

To change font size: [https://stackoverflow.com/questions/21363334/how-to-add-font-size-in-subtitles-in-ffmpeg-video-filter](https://stackoverflow.com/questions/21363334/how-to-add-font-size-in-subtitles-in-ffmpeg-video-filter)
```
ffmpeg -i input.mp4 -vf "subtitles=subtitle.srt:force_style='Fontsize=64'" output.mp4
```
The default appears to be 24, so just multiply that by whatever seems like a reasonable factor.

Note howver that [.ass subtitle files](substation-alpha.md) can contain style information, which ffmpeg respects. [Aegisub](aegisub.md) can produce and preview such styles, making .ass one of the best options.

## ↑ Ancestors (8)

1. [Subtitle](subtitle.md)
2. [Video file format](video-file-format.md)
3. [File format](file-format.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
