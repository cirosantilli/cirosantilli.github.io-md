# FFmpeg filter graph

↑ **Parent:** [FFmpeg](ffmpeg.md)

Filter graphs are a thing of great beauty. What an amazingly obscure [domain-specific language](domain-specific-language.md), but which can produce striking results with very little!!!

A quick example from [https://stackoverflow.com/questions/59551013/how-to-generate-stereo-sine-wave-using-ffmpeg-with-different-frequencies-for-eac/77730492#77730492](https://stackoverflow.com/questions/59551013/how-to-generate-stereo-sine-wave-using-ffmpeg-with-different-frequencies-for-eac/77730492#77730492) illustrates some of the fundamentals:


```
ffplay -autoexit -nodisp -f lavfi -i '
sine=frequency=500[a];
sine=frequency=1000[b];
[a][b]amerge, atrim=end=2
'
```
which creates a graph:
```
                              +--------+
[sine=frequency=500]--->[a]-->|        |
                              | amerge |-->[atrim]-->[output]
[sine=frequency=1000]-->[b]-->|        |
                              +--------+
```
and plays 500 Hz on the left channel and 1000 Hz on the right channel for 2 seconds.

So we see the following syntax patterns:
- `sine`, `amerge` and `atrim` are filters
- `sine=frequency=500`: the first `=` says "araguments follow"
  - `frequency=500` sets the `frequency` argument of the `sine` filter
  - for multiple arguments the syntax is to separate arguments with colons e.g. `sine=frequency=500:duration=2`
- `;`: separates statements
- `[a]`, `[b]`: sets the name of an edge
- `,`: creates unnamed edge between filters that have one input and one output

A list of all filters can be obtained ith:
```
ffmpeg -filters
```
and parameters for a single filter can be obtained with:
```
ffmpeg --help filter=sine
```
Related question: [https://stackoverflow.com/questions/69251087/in-ffmpeg-command-line-how-to-show-all-filter-settings-and-their-parameters-bef](https://stackoverflow.com/questions/69251087/in-ffmpeg-command-line-how-to-show-all-filter-settings-and-their-parameters-bef)

TODO dump graph to [ASCII art](ascii-art.md)? [https://trac.ffmpeg.org/wiki/FilteringGuide#Visualizingfilters](https://trac.ffmpeg.org/wiki/FilteringGuide#Visualizingfilters) mentions a `-dumpgraph` option, but haven't managed to use it yet.

Bibliography:
- [https://ffmpeg.org/ffmpeg-filters.html](https://ffmpeg.org/ffmpeg-filters.html) official documentation
- [https://trac.ffmpeg.org/wiki/FilteringGuide](https://trac.ffmpeg.org/wiki/FilteringGuide) some handy tips from the FFMpeg Wiki

## ↑ Ancestors (8)

1. [FFmpeg](ffmpeg.md)
2. [Multimedia software](multimedia-software.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
