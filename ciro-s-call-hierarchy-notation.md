<h1 id="ciro-s-call-hierarchy-notation">Ciro's call hierarchy notation</h1>

↑ **Parent:** [Debugging](debugging.md)

This is a simple hierarchical plaintext notation [Ciro Santilli](ciro-santilli-split.md) created to explain programs to himself.

It is usuall created by doing searches in an [IDE](integrated-development-environment.md), and then manually selecting the information of interest.

It attempts to capture intuitive information not only of the call graph itself, including callbacks, but of when things get called or not, by the addition of some context code.

For example, consider the following [pseudocode](pseudocode.md):
```
f1() {
}

f2(i) {
  if (i > 5) {
    f1()
  }
}

f3() {
  f1()
  f2_2()
}

f2_2() {
  for (i = 0; i < 10; i++) {

    f2(i)
  }
}

main() {
  f2_2()
  f3()
}
```
Supose that we are interested in determining what calls `f1`.

Then a reasonable call hierarchy for `f1` would be:
```
f2(i)
  if (i > 5) {
    f1()

  f2_2()
    for (i = 0; i < 10; i++) {
      f2(i)

    main
    f3
f3()
  main()
```

Some general principles:
- start with a regular call tree
- to include context:
  - remove any blank lines from the snippet of interest
  - add it indented below the function
  - and then follow it up with a blank line
  - and then finally add any callers at the same indentation level

## ↑ Ancestors (8)

1. [Debugging](debugging.md)
2. [Software bug](software-bug.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
