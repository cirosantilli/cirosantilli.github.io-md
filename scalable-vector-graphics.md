# Scalable Vector Graphics

↑ **Parent:** [Vector graphics](vector-graphics.md)  
🏷️ **Tags:** [Good](good.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

[Companies](company-split.md) have been really slow to support SVG features in their browsers, and that is very saddening: [https://medium.com/@michaelmangial1/introduction-to-scalable-vector-graphics-6450c03e8d2e](https://medium.com/@michaelmangial1/introduction-to-scalable-vector-graphics-6450c03e8d2e)

You can't drop SVG support for `canvas` until there's a way to run untrusted [JavaScript](javascript.md) on the browser!

[SVG](scalable-vector-graphics.md) does have some compatibility annoyances, notably [SVG fonts](svg-fonts.md). But we should as a society work to standardize and implement a fix those, the benefits of SVG are just too great!

Examples:
- [svg/svg.svg](svg/svg.svg) a minimal somewhat sane SVG:
  - if the `width` and `height` properties were not given, you get the default 300x150, which seems to be set in the SVG standard:
    - [https://stackoverflow.com/questions/40156710/why-does-this-svg-image-have-a-height-of-150px](https://stackoverflow.com/questions/40156710/why-does-this-svg-image-have-a-height-of-150px)
    - [https://css-tricks.com/scale-svg](https://css-tricks.com/scale-svg)
- how to add na SVG image to a [HTML](html.md) file:
  - [svg/svg.html](svg/svg.html): external image. The included file is [svg/svg.svg](svg/svg.svg).
  - [svg/inline.html](svg/inline.html): inline.
- [svg/billion-laughs.svg](svg/billion-laughs.svg)
- [svg/html.svg](svg/html.svg)
- [svg/triangle.svg](svg/triangle.svg)
- [svg/viewBox.svg](svg/viewBox.svg): this attribute allows you to control the default SVG `svg width=` and `height=` while keeping the coordinates of the drawing untouched. If the `viewBox` aspect ratio differs from the width/height ratio, you likely want to play with `preserveAspectRatio`, otherwise you would get white spaces by default on the generated image
- [CSS](cascading-style-sheets.md) with SVG:
  - [svg/style.svg](svg/style.svg): inline CSS
  - [svg/style-external.svg](svg/style-external.svg): external CSS with: `<?xml-stylesheet type="text/css" href="svg.css" ?>`, see also: [https://stackoverflow.com/questions/18434094/how-to-style-svg-with-external-css](https://stackoverflow.com/questions/18434094/how-to-style-svg-with-external-css)
    - [svg/subdir/style-external.html](svg/subdir/style-external.html): is the relative CSS relative to the HTML or to the SVG? Answer: to the SVG... OMG. So how to make it work reliably?
  - [svg/current-color.html](svg/current-color.html) and [svg/current-color.svg](svg/current-color.svg): illustrates `fill="currentColor"`. Only works for inline SVG however... See also: [https://stackoverflow.com/questions/13000682/how-do-i-have-an-svg-image-inherit-colors-from-the-html-document/13002311](https://stackoverflow.com/questions/13000682/how-do-i-have-an-svg-image-inherit-colors-from-the-html-document/13002311)
- [JavaScript](javascript.md) with SVG:
  - [svg/script.svg](svg/script.svg)
  - [svg/external-js.svg](svg/external-js.svg)
- [svg/defs.html](svg/defs.html) hows how `defs` works
  - [svg/defs-external.html](svg/defs-external.html) tries to include external `defs` from [svg/defs.svg](svg/defs.svg), but that fails like everything else related to external SVGs

**Table of contents**

- [SVG tutorial](svg-tutorial.md)
  - [SVG background color](svg-background-color.md)
  - [SVG fonts](svg-fonts.md)
- [Join two SVG side-by-side from the command line](join-two-svg-side-by-side-from-the-command-line.md)
- [SVG version](svg-version.md)
  - [SVG 1.0](svg-1-0.md)
  - [SVG 1.1](svg-1-1.md)
  - [SVG 1.2](svg-1-2.md)
  - [SVG 2](svg-2.md)

## ↑ Ancestors (8)

1. [Vector graphics](vector-graphics.md)
2. [Image file format](image-file-format.md)
3. [File format](file-format.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Good](good.md)
