# Older updates

↑ **Parent:** [Updates](../updates-split.md)

- [https://en.wikipedia.org/wiki/Scott_Hassan](https://en.wikipedia.org/wiki/Scott_Hassan) I delved into a bit of [Wikipedia](../wikipedia.md) drama on the page of [Scott Hassan](../scott-hassan.md), initial coder of [Google Search](../google-search.md), which I created an am the main contributor.

  Originally I had added some details about this messy divorce which saw coverage in major publications such as the [New York Times](../new-york-times.md): [https://www.nytimes.com/2021/08/20/technology/Scott-Hassan-Allison-Huynh-divorce.html](https://www.nytimes.com/2021/08/20/technology/Scott-Hassan-Allison-Huynh-divorce.html) and Scott used puppets to remove those at several points in time over the years.

  Those removals were then reverted by other editors, not myself, indicating that editors wanted the details there.

  While preparing to finally decide this through moderation, I ended up finding that the divorce details should likely have been left out according to Wikipedia rules, because Scott is "relatively unknown" and a "low profile individual":
  - [https://en.wikipedia.org/w/index.php?title=Wikipedia:Biographies_of_living_persons&oldid=1235693634#People_who_are_relatively_unknown](https://en.wikipedia.org/w/index.php?title=Wikipedia:Biographies_of_living_persons&oldid=1235693634#People_who_are_relatively_unknown)
  - [https://en.wikipedia.org/wiki/Wikipedia:Who_is_a_low-profile_individual](https://en.wikipedia.org/wiki/Wikipedia:Who_is_a_low-profile_individual)
  and so I ended up removing them myself.

  This is yet once again [deletionism on Wikipedia](../deletionism-on-wikipedia.md) weakening the site, and making @OurBigBook stronger :-) Here is the uncensored one: [Scott Hassan](https://ourbigbook.com/-/topic/scott-hassan)

  I spent time on this partly because I'm mildly obsessed with founding myths of companies, but also partly to better understand the moderation process of Wikipedia.

  Posted at:
  - [https://mastodon.social/@cirosantilli/112908378712190057](https://mastodon.social/@cirosantilli/112908378712190057)
  - [https://x.com/cirosantilli/status/1820377809836978496](https://x.com/cirosantilli/status/1820377809836978496)
  - [https://www.facebook.com/cirosantilli/posts/pfbid0yoj6be1hS2YVNuPhHXXeErZ11ExER6A9XCxLYG44dEK96hNTVpuzEJDXLJBmoah6l](https://www.facebook.com/cirosantilli/posts/pfbid0yoj6be1hS2YVNuPhHXXeErZ11ExER6A9XCxLYG44dEK96hNTVpuzEJDXLJBmoah6l)
- [https://unix.stackexchange.com/questions/256138/is-there-any-decent-speech-recognition-software-for-linux/613392#613392](https://unix.stackexchange.com/questions/256138/is-there-any-decent-speech-recognition-software-for-linux/613392#613392) cool to see that the Vosk open source speech recognition software by [https://twitter.com/alphacep](https://twitter.com/alphacep) now has a convenient command line interface called vosk-transcriber!

  It allows you to just:

  ```
  vosk-transcriber -m ~/var/lib/vosk/vosk-model-en-us-0.22 -i in.ogg -o out.srt -t srt
  ```

  to extract a subtitle file out.srt from a .ogg audio input file.

  Accuracy is a bit meh, but we'll take it!

  Posted at:
  - [https://mastodon.social/@cirosantilli/112317205707461869](https://mastodon.social/@cirosantilli/112317205707461869)
  - [https://twitter.com/cirosantilli/status/1782535572143140900](https://twitter.com/cirosantilli/status/1782535572143140900)
  - [https://askubuntu.com/questions/161515/speech-recognition-app-to-convert-mp3-voice-to-text/423849#423849](https://askubuntu.com/questions/161515/speech-recognition-app-to-convert-mp3-voice-to-text/423849#423849)
- [https://video.stackexchange.com/questions/33531/how-to-remove-background-from-video-without-green-screen-on-the-command-line/37392#37392](https://video.stackexchange.com/questions/33531/how-to-remove-background-from-video-without-green-screen-on-the-command-line/37392#37392) tested this AI video background remover [https://github.com/nadermx/backgroundremover](https://github.com/nadermx/backgroundremover) by @nadermx. It had a few glitches, but I had fun.

  ![](https://ia600306.us.archive.org/10/items/ciro-santilli-selfie-in-cycling-kit-with-old-cottages-background-removal/Ciro_Santilli_selfie_in_cycling_kit_with_old_cottages_background_removal.gif)

  [https://unix.stackexchange.com/questions/233832/merge-two-video-clips-into-one-placing-them-next-to-each-other/774936#774936](https://unix.stackexchange.com/questions/233832/merge-two-video-clips-into-one-placing-them-next-to-each-other/774936#774936) I then learned how to stack videos side-by-side with ffmpeg to create this side-by-side demo. It also works for GIFs! [https://stackoverflow.com/questions/30927367/imagemagick-making-2-gifs-into-side-by-side-gifs-using-im-convert/78361093#78361093](https://stackoverflow.com/questions/30927367/imagemagick-making-2-gifs-into-side-by-side-gifs-using-im-convert/78361093#78361093)

  ![](https://web.archive.org/web/20240422123110im_/https://i.stack.imgur.com/gkJnK.gif)

  Posted at:
  - [https://twitter.com/cirosantilli/status/1781994384805822684](https://twitter.com/cirosantilli/status/1781994384805822684)
  - [https://mastodon.social/@cirosantilli/112308748237095260](https://mastodon.social/@cirosantilli/112308748237095260)
  - [https://www.facebook.com/cirosantilli/posts/pfbid02SqbYcRBvVkfivXmqmWJ1cc1KjEkbZyC8EXkBqgzZisgFPcXdADEXzrKCucWJn8uQl](https://www.facebook.com/cirosantilli/posts/pfbid02SqbYcRBvVkfivXmqmWJ1cc1KjEkbZyC8EXkBqgzZisgFPcXdADEXzrKCucWJn8uQl)
  - [https://archive.org/details/ciro-santilli-selfie-in-cycling-kit-with-old-cottages-background-removal](https://archive.org/details/ciro-santilli-selfie-in-cycling-kit-with-old-cottages-background-removal)
- Just found out that [my Lenovo ThinkPad P14s](../ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md) has an infrared camera, and recorded a quick test video on [Ubuntu 23.10](../ubuntu-23-10.md) with:
  ```
  fmpeg -y -f v4l2 -framerate 30 -video_size 640x360 -input_format gray -i /dev/video2 -c copy out.mkv
  ```


  - [https://mastodon.social/@cirosantilli/112261675634568209](https://mastodon.social/@cirosantilli/112261675634568209)
  - [https://twitter.com/cirosantilli/status/1778981935257116767](https://twitter.com/cirosantilli/status/1778981935257116767)
  - [https://www.facebook.com/cirosantilli/posts/pfbid027M3n2p8snE9otAWdHtJ3ig2AhrXoDGv4h68o1z8agHceQBbFHZpEoxg7KZbiWAgWl](https://www.facebook.com/cirosantilli/posts/pfbid027M3n2p8snE9otAWdHtJ3ig2AhrXoDGv4h68o1z8agHceQBbFHZpEoxg7KZbiWAgWl)
  - [https://www.linkedin.com/feed/update/urn:li:activity:7184755892410576897/](https://www.linkedin.com/feed/update/urn:li:activity:7184755892410576897/)
  - [https://www.youtube.com/watch?v=o1ZeR6pmf6o](https://www.youtube.com/watch?v=o1ZeR6pmf6o)
  - [https://commons.wikimedia.org/wiki/File:Infrared_video_of_Ciro_Santilli_waving_recorded_on_Lenovo_ThinkPad_P14s_with_FFmpeg_6.0_on_Ubuntu_23.10.webm](https://commons.wikimedia.org/wiki/File:Infrared_video_of_Ciro_Santilli_waving_recorded_on_Lenovo_ThinkPad_P14s_with_FFmpeg_6.0_on_Ubuntu_23.10.webm)

  <a id="image-ciro-santilli-waving-hello-in-infrared"></a>
  <img src="https://web.archive.org/web/20240413030921if_/https://i.sstatic.net/c5KbD2gY.gif" alt="" height="400">

  **[Figure 29](#image-ciro-santilli-waving-hello-in-infrared). Ciro Santilli waving hello in infrared**.

## ↑ Ancestors (3)

1. [Updates](../updates-split.md)
2. [Ciro Santilli](../ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](../split.md)
