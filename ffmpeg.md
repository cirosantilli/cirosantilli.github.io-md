# FFmpeg

↑ **Parent:** [Multimedia software](multimedia-software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/FFmpeg)

FFmpeg is the [assembler](assembler-computing.md) of audio and video.

As a result, [Ciro Santilli](ciro-santilli-split.md) who likes "lower level stuff", has had many many hours if image manipulation fun with this software, see e.g.:
- the "Media" section of [the best articles by Ciro Articles](articles-split.md).
- [Figure "Ciro knows how to convert videos to GIFs"](ciro-santilli-s-stack-overflow-contributions.md#image-ciro-knows-how-to-convert-videos-to-gifs)

As older Ciro grows, the more he notices that FFmpeg can do basically any lower level audio video task. It is just an amazing piece of software, the immediate go-to for any low level operation.

FFmpeg was created by [Fabrice Bellard](fabrice-bellard.md), which Ciro deeply respects.

Resize a video: [https://superuser.com/questions/624563/how-to-resize-a-video-to-make-it-smaller-with-ffmpeg](https://superuser.com/questions/624563/how-to-resize-a-video-to-make-it-smaller-with-ffmpeg):
```
ffmpeg -i input.avi -filter:v scale=720:-1 -c:a copy output.mkv
```
Unlike every other convention under the sun, the height in `scale` is the first number.

**Table of contents**

- [FFmpeg filter graph](ffmpeg-filter-graph.md)
- [ffplay](ffplay.md)
  - [ffplay multiple input files](ffplay-multiple-input-files.md)
- [FFmpeg sound synthesis](ffmpeg-sound-synthesis.md)
- [FFmpeg video synthesis](ffmpeg-video-synthesis.md)
- [FFmpeg is the backend of YouTube](ffmpeg-is-the-backend-of-youtube.md)
- [Concatenate two videos with ffmpeg](concatenate-two-videos-with-ffmpeg.md)

## ↑ Ancestors (7)

1. [Multimedia software](multimedia-software.md)
2. [Software](software-split.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (5)

- [Google Pixel 3a (2020)](ciro-santilli-s-hardware/google-pixel-3a-2020.md)
- [Csound](csound.md)
- [Fabrice Bellard](fabrice-bellard.md)
- [The art of programming](the-art-of-programming.md)
- [The most awesome systems programmers](the-most-awesome-systems-programmers.md)
