# Nilsson algorithm for the Kolakoski sequence

↑ **Parent:** [Kolakoski sequence](kolakoski-sequence.md)

This algorithm is more efficient in space, using only $log(n)$, as it recursively compresses the state required to keep track of what to do next.

Time is still $O(n)$.

The table at [https://maths-people.anu.edu.au/~brent/pd/Kolakoski-UNSW.pdf](https://maths-people.anu.edu.au/~brent/pd/Kolakoski-UNSW.pdf) page 20 has a summary image, but it is hard to understand.

Let's do a step by step version now.

The notation we use is as follows:
```
1 2 (1) 1 (1)
```
means that:
- this is number 2
- there is 1 occurrence count left

Note that column 1 does not need to keep a count so we use notation such as:

```
1 2(0) 1(1)
```

The starting state is:
```
2 | 2 2(1) 2(1) 2(1) 2(1) ...
```
which means that it implicitly contains infinitely many `2(1)` at the end which we abbreviate just as:
```
2 | 2 2(1) ...
```
The actual algorithm will of course omit as many trailing `2(1)` as it can.

The update rules are:
- go left to right:
  - flip:
    ```
    x(0)       y(0)
    !x((!x)-1) unchanged
    ```

    continue going left to right.
  - repeat:
    ```
    x(0)   y(n > 0)
    x(x-1) y(n - 1)
    ```

    and then stop further updates.
Note that both rules don't overlap so that each update is always determined by only one of them at a time.

Also the first column is always implicitly `(0)`.

Use column 2 up once to repeat column 1:

```
2 | 2 2(1) ...
3 | 2 2(0) 2(1) ...
```

Here we:
- switch column 1 because column 2 reached 0 on previous step
- use column 3 up once to repeat column 2

```
2 | 2 2(1) ...
3 | 2 2(0) 2(1) ...
4 | 1 2(1) 2(0) 2(1) ...
```

- use column 2 up once to repeat 1

```
2 | 2 2(1) ...
3 | 2 2(0) 2(1) ...
4 | 1 2(1) 2(0) 2(1) ...
5 | 1 2(0) 2(1) 2(0) 2(1) ...
```

```
 2 | 2 2(1) ...
 3 | 2 2(0) 2(1) ...
 4 | 1 2(1) 2(0) 2(1) ...
 5 | 1 2(0) 2(0) 2(1) ...
 6 | 2 1(0) 2(1) 2(0) 2(1) ...
 7 | 1 1(0) 2(0) 2(0) 2(1) ...
 8 | 2 2(1) 1(0) 2(1) 2(0) 2(1) ...
 9 | 2 2(0) 1(0) 2(1) 2(0) 2(1) ...
10 | 1 1(0) 1(0) 2(0) 2(0) 2(1) ...
11 | 2 2(1) 2(1) 1(0) 2(1) 2(0) 2(1) ...
12 | 2 2(0) 2(1) 1(0) 2(1) 2(0) 2(1) ...
13 | 1 2(1) 2(0) 1(0) 2(1) 2(0) 2(1) ...
14 | 1 2(0) 2(0) 1(0) 2(1) 2(0) 2(1) ...
15 | 2 1(0) 1(0) 1(0) 2(0) 2(0) 2(1) ...
16 | 1 2(1) 2(1) 2(1) 1(0) 2(1) 2(0) 2(1) ...
```

## ↑ Ancestors (9)

1. [Kolakoski sequence](kolakoski-sequence.md)
2. [Integer sequence](integer-sequence.md)
3. [Numeric function](numeric-function.md)
4. [Function by signature](function-by-signature.md)
5. [Function (mathematics)](function-mathematics.md)
6. [Formalization of mathematics](formalization-of-mathematics-split.md)
7. [Area of mathematics](area-of-mathematics.md)
8. [Mathematics](mathematics-split.md)
9. [Ciro Santilli's Homepage](split.md)
