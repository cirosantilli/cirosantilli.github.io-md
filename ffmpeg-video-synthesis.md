# FFmpeg video synthesis

↑ **Parent:** [FFmpeg](ffmpeg.md)

Video with a solid color:
- 2 second white video:
  ```
  ffplay -autoexit -f lavfi -i 'color=white:640x480:d=3,format=rgb24,trim=end=2'
  ```

  Also add some audio:
  ```
  ffmpeg -lavfi "color=white:640x480:d=3,format=rgb24,trim=end=2[v];sine=f=1000:d=2[a]" -map '[a]' -map '[v]' out.mkv
  ```

  TODO how to ffplay the video + audio directly? `-map` does not seem to work unfortunately.
- 2 second white followed by 2 second black video:
  ```
  ffplay -autoexit -f lavfi -i 'color=white:640x480:d=3,format=rgb24,trim=end=2[a];color=black:640x480:d=3,format=rgb24,trim=end=2[b];[a][b]concat=n=2:v=1:a=0'
  ```
- bibliography:
  - [https://superuser.com/questions/1153930/how-to-generate-a-pure-white-background-video-with-ffmpeg](https://superuser.com/questions/1153930/how-to-generate-a-pure-white-background-video-with-ffmpeg)

Display count in seconds on the video:
- black text on white background. Start from 0 and count up to 2:
  ```
  ffplay -autoexit -f lavfi -i "
  color=white:480x480:d=3,
  format=rgb24,
  drawtext=
    fontcolor=black:
    fontsize=600:
    text='%{eif\:t\:d}':
    x=(w-text_w)/2:
    y=(h-text_h)/2
  "
  ```
- count 0 to 2 with one different sine wave per count:
  ```
  ffmpeg -lavfi "
  color=white:480x480:d=3,
  format=rgb24,
  drawtext=
  fontcolor=black:
  fontsize=600:
  text='%{eif\:t\:d}':
  x=(w-text_w)/2:
  y=(h-text_h)/2[v];
  sine=f=500:d=1[a1];
  sine=f=1000:d=1[a2];
  sine=f=2000:d=1[a3];
  [a1][a2][a3]concat=n=3:v=0:a=1[a];
  " -map '[v]' -map '[a]' count.mkv
  ```
- bibliography:
  - [https://gist.github.com/derand/31b8312fd64156120cb8f45825a1f0f7](https://gist.github.com/derand/31b8312fd64156120cb8f45825a1f0f7)
  - [https://www.reddit.com/r/ffmpeg/comments/11kxugt/make_a_video_timer_or_countdown/](https://www.reddit.com/r/ffmpeg/comments/11kxugt/make_a_video_timer_or_countdown/)
  - [https://stackoverflow.com/questions/11640458/how-can-i-generate-a-video-file-directly-from-an-ffmpeg-filter-with-no-actual-in/79618057#79618057](https://stackoverflow.com/questions/11640458/how-can-i-generate-a-video-file-directly-from-an-ffmpeg-filter-with-no-actual-in/79618057#79618057)

Bibliography:
- [https://ffmpeg.org//ffmpeg-filters.html#Video-Sources](https://ffmpeg.org//ffmpeg-filters.html#Video-Sources) main section of the documentation listing various video generators
- [https://stackoverflow.com/questions/11640458/how-can-i-generate-a-video-file-directly-from-an-ffmpeg-filter-with-no-actual-in](https://stackoverflow.com/questions/11640458/how-can-i-generate-a-video-file-directly-from-an-ffmpeg-filter-with-no-actual-in) generically asking how to generate the video without an input video

## ↑ Ancestors (8)

1. [FFmpeg](ffmpeg.md)
2. [Multimedia software](multimedia-software.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
