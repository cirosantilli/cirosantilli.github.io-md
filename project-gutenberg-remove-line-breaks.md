# Project Gutenberg remove line breaks

↑ **Parent:** [Project Gutenberg](project-gutenberg.md)

[https://ubuntuforums.org/archive/index.php/t-1132578.html](https://ubuntuforums.org/archive/index.php/t-1132578.html)

Their txt formats are so crap!

E.g. for;
```
wget -O pap.txt https://www.gutenberg.org/ebooks/1342.txt.utf-8
```
a good one is:
```
perl -0777 -pe 's/(?<!\r\n)\r\n(?!\r\n)( +)?/ /g' pap.txt
```

The `( +)?` is for the endlessly many quoted letters they have, which use four leading spaces per line as a quote marker.

## ↑ Ancestors (10)

1. [Project Gutenberg](project-gutenberg.md)
2. [Public domain archive](public-domain-archive.md)
3. [Public domain](public-domain.md)
4. [Free license](free-license.md)
5. [License](license.md)
6. [Law](law-split.md)
7. [Social technology](social-technology-split.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
