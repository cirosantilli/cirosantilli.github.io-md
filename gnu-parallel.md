# GNU parallel

↑ **Parent:** [List of command line utilities](list-of-command-line-utilities.md)  
🏷️ **Tags:** [GNU package](gnu-package.md), [Good](good.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GNU_parallel)

The author Ole Tange answers every question about it on [Stack Exchange](stack-exchange.md). What a legend!

This program makes you respect [GNU make](gnu-make.md) a bit more. Good old make with `-j` can not only parallelize, but also take in account a [dependency graph](dependency-graph.md).

Some examples under:
```
man parallel_exampes
```

To get the input argument explicitly job number use the magic string `{}`, e.g.:
```
printf 'a\nb\nc\n' | parallel echo '{}'
```
sample output:
```
a
b
c
```

To get the job number use `{#}` as in:
```
printf 'a\nb\nc\n' | parallel echo '{} {#}'
```
sample output:
```
a 1
b 2
c 3
c 3
```

`{%}` contains which thread the job running in, e.g. if we limit it to `2` threads with `-j2`:
```
printf 'a\nb\nc\nd\n' | parallel -j2 echo '{} {#} {%}'
```
sample output:
```
a 1 1
b 2 1
c 3 2
d 4 1
```
The percent must be a reference to "split the inputs module the number of workers", and modulo uses the `%` symbol in many programming languages such as [C](c-programming-language.md).

To pass multiple CLI arguments per command you can use `-X` e.g.:
```
printf 'a\nb\nc\nd\n' | parallel -j2 -X echo '{} {#} {%}'
```
sample output:
```
a b 1 1
c d 2 2
```

## ↑ Ancestors (10)

1. [List of command line utilities](list-of-command-line-utilities.md)
2. [Command line utility](command-line-utility.md)
3. [Command-line interface](command-line-interface.md)
4. [Computer user-interface](computer-user-interface.md)
5. [Software](software-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [The art of programming](the-art-of-programming.md)
