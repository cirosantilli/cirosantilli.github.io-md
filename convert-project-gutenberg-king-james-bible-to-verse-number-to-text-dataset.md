# Convert project Gutenberg King James Bible to verse number to text dataset

↑ **Parent:** [Bible dataset](bible-dataset.md)

This section is about converting: [https://www.gutenberg.org/ebooks/10](https://www.gutenberg.org/ebooks/10), and most likely the [plaintext](human-readable-format.md) version: [https://stackoverflow.com/a/43060761/895245](https://stackoverflow.com/a/43060761/895245) to the same data format as [https://www.kaggle.com/datasets/oswinrh/bible](https://www.kaggle.com/datasets/oswinrh/bible) mapping book/chapter/verse to the text:

```
1 1 1 In the beginning God created the heaven and the earth.
1 1 2 And the earth was without form, and void; and darkness was upon the face of the deep.
```

On particular annoyance is that the txt version has multiple verses per line at times.

We'd likely just want to use a slightly modified version of: [https://stackoverflow.com/a/43060761/895245](https://stackoverflow.com/a/43060761/895245) that searches for patterns of type:
```
(\d+):(\d+)
```
with incremental integers.

## ↑ Ancestors (9)

1. [Bible dataset](bible-dataset.md)
2. [Bible](bible.md)
3. [Christianism](christianism.md)
4. [Abrahamic religion](abrahamic-religion.md)
5. [Religion](religion-split.md)
6. [Social science](social-science.md)
7. [Scientific method](scientific-method.md)
8. [Science](science-split.md)
9. [Ciro Santilli's Homepage](split.md)
