# csvgrep from csvkit

↑ **Parent:** [Csvkit](csvkit.md)

Simple example:
```
printf '00,11,22\n33,44,55\n' | csvgrep -H -c2 -r '^11$' | tail -n+2
```
output:
```
00,11,22
```

More verbose description:
- [https://stackoverflow.com/questions/19711723/awk-to-filter-csv-files/77273608#77273608](https://stackoverflow.com/questions/19711723/awk-to-filter-csv-files/77273608#77273608)
- [https://unix.stackexchange.com/questions/97070/filter-a-csv-file-based-on-the-5th-column-values-of-a-file-and-print-those-reco/758651#758651](https://unix.stackexchange.com/questions/97070/filter-a-csv-file-based-on-the-5th-column-values-of-a-file-and-print-those-reco/758651#758651)

## ↑ Ancestors (10)

1. [Csvkit](csvkit.md)
2. [CSV CLI tool](csv-cli-tool.md)
3. [Comma-separated values](comma-separated-values.md)
4. [Data file format](data-file-format.md)
5. [File format](file-format.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
