# jq ignore missing attribute

↑ **Parent:** [jq](jq.md)


```
echo '[{"a": 1, "b": 2}, {"b": 3}]' | jq '.[] | select(.a) | .a'
```
Output:
```
1
```
and no empty lines as desired.

Bibliography:
- [https://stackoverflow.com/questions/42097410/how-to-check-for-presence-of-key-in-jq-before-iterating-over-the-values](https://stackoverflow.com/questions/42097410/how-to-check-for-presence-of-key-in-jq-before-iterating-over-the-values)

## ↑ Ancestors (9)

1. [jq](jq.md)
2. [JSON](json.md)
3. [Data file format](data-file-format.md)
4. [File format](file-format.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
