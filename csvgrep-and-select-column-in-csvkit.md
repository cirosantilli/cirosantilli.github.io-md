# csvgrep and select column in csvkit

↑ **Parent:** [Csvkit](csvkit.md)

There seems to be no way without a pipe, you seem to need to reparse the columns, e.g. the tutorial at: [https://csvkit.readthedocs.io/en/latest/tutorial/2_examining_the_data.html#csvgrep-find-the-data-you-need](https://csvkit.readthedocs.io/en/latest/tutorial/2_examining_the_data.html#csvgrep-find-the-data-you-need) does:
```
csvcut -c county,item_name,total_cost data.csv | csvgrep -c county -m LANCASTER
```

Asked at: [https://stackoverflow.com/questions/77266699/how-to-fillter-a-csv-file-with-csvgrep-and-print-only-certain-columns](https://stackoverflow.com/questions/77266699/how-to-fillter-a-csv-file-with-csvgrep-and-print-only-certain-columns)

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

## ← Incoming links (1)

- [Csvkit](csvkit.md)
