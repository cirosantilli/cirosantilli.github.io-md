# Project Euler problem 910 solution

↑ **Parent:** [Project Euler problem 910](project-euler-problem-910.md)

Numerical solution from [https://github.com/lucky-bai/projecteuler-solutions/issues/102](https://github.com/lucky-bai/projecteuler-solutions/issues/102):
```
547480666
```

- [https://github.com/cirosantilli/project-euler-solutions/blob/master/solvers/910.py](https://github.com/cirosantilli/project-euler-solutions/blob/master/solvers/910.py)
- [https://github.com/cirosantilli/project-euler-solutions/blob/master/solvers/910.md](https://github.com/cirosantilli/project-euler-solutions/blob/master/solvers/910.md)

Ideas:

```
A(x) = x + 1
Z(u)(v) = v
S(u)(v)(w) = v(u(v)(w))
```

Let's resolve the second example ourselves:


```
S
  (S)
  (S(S))
  (S(Z))
(A)
(0)

S
(S)
(
  S
  (S(S))
  (S(Z))
)
(A)
(0)

S
(S(S))
(S(Z))
(
  S
  (
    S
    (S(S))
    (S(Z))
  )
  (A)
)
(0)

S
(Z)
(
  S(S)
  (S(Z))
  (
    S
    (
      S
      (S(S))
      (S(Z))
    )
    (A)
  )
)
(0)

S(S)
(S(Z))
(
  S
  (
    S
    (S(S))
    (S(Z))
  )
  (A)
)
(
  Z
  (
    S(S)
    (S(Z))
    (
      S
      (
        S
        (S(S))
        (S(Z))
      )
      (A)
    )
  )
  (0)
)

S
(S)
(S(Z))
(
  S
  (
    S
    (S(S))
    (S(Z))
  )
  (A)
)
(0)
```
TODO: how long would this be?

So we see that all of these rules resolve quite quickly and do not go into each other. `S` however offers some problems, in that:

```
C_0 = Z
C_i = S(C_{i-1})
D_i = C_i(S)(S)
```

So we see that `D_i` goes somewhat simply into `C_i`, and `C_i` is recursive giving:
```
S^i(Z)
```

Calculate the nine first digits of:
```
D_a(D_b)(D_c)(C_d)(A)(e)
```

Removing `D_a`:
```
S^i(Z)S)(S)(D_b)(D_c)(C_d)(A)(e)
```

## ↑ Ancestors (15)

1. [Project Euler problem 910](project-euler-problem-910.md)
2. [Main Project Euler problem](main-project-euler-problem.md)
3. [Project Euler problem](project-euler-problem.md)
4. [Project Euler](project-euler-split.md)
5. [Exercism](exercism.md)
6. [Competitive programming website](competitive-programming-website.md)
7. [Competitive programming](competitive-programming.md)
8. [Knowledge olympiad by domain of knowledge](knowledge-olympiad-by-domain-of-knowledge.md)
9. [Knowledge olympiad](knowledge-olympiad.md)
10. [STEM prize](stem-prize.md)
11. [Prize](prize.md)
12. [Social technology](social-technology-split.md)
13. [Area of technology](area-of-technology.md)
14. [Technology](technology-split.md)
15. [Ciro Santilli's Homepage](split.md)
