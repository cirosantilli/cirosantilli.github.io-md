# Crate image with given text in ImageMagick

↑ **Parent:** [ImageMagick HOWTO](imagemagick-howto.md)

Digits 0 to 9, white on black background:
```
for i in `seq 0 9`; do convert -size 512x512 xc:black -pointsize 500 -gravity center -fill white -draw "text 0,0 \"$i\"" $i.png; done
```

Bibliography:
- [https://stackoverflow.com/questions/67012057/how-to-generate-an-image-with-a-number-in-it](https://stackoverflow.com/questions/67012057/how-to-generate-an-image-with-a-number-in-it)

## ↑ Ancestors (11)

1. [ImageMagick HOWTO](imagemagick-howto.md)
2. [ImageMagick](imagemagick.md)
3. [Image manipulation software](image-manipulation-software.md)
4. [Image software](image-software.md)
5. [Multimedia software](multimedia-software.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
