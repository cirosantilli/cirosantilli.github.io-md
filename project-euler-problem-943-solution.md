# Project Euler problem 943 solution

↑ **Parent:** [Project Euler problem 943](project-euler-problem-943.md)

Numerical solution:
```
1038733707
```

Programs:
- [https://github.com/cirosantilli/project-euler-solutions/blob/master/solvers/943.py](https://github.com/cirosantilli/project-euler-solutions/blob/master/solvers/943.py)

Explanation: [https://github.com/cirosantilli/project-euler-solutions/blob/master/solvers/943.md](https://github.com/cirosantilli/project-euler-solutions/blob/master/solvers/943.md)

A naive `T` in Python is:


```
from collections import deque

def T(a: int, b: int, N: int) -> int:
    total = a
    q = deque([a] * (a - 1))
    is_a = False
    for i in range(N - 1):
        cur = q.popleft()
        total += cur
        q.extend([a if is_a else b] * cur)
        is_a = not is_a
    return total

assert T(2, 3, 10) == 25
assert T(4, 2, 10**4) == 30004
assert T(5, 8, 10**6) == 6499871
```
which passes the tests, but takes half a second on [PyPy](pypy.md). So clearly it is not going to work for `22332223332233`  which has 14 digits.

Maybe if `T` is optimized enough, then we can just bruteforce over the ~40k possible sum ranges 2 to 223. 1 second would mean 14 hours to do them all, so bruteforce but doable. Otherwise another optimization step may be needed at that level as well: one wonders if multiple sums can be factored out, or if the modularity can of the answer can help in a meaningful way. The first solver was [ecnerwala](andrew-he.md) using C/C++ in 1 hour, so there must be another insight missing, unless they have access to a supercomputer.

The first idea that comes to mind to try and optimize `T` is that this is a [dynamic programming](dynamic-programming.md), but then the question is what is the recurrence relation.

The sequence appears to be a generalization of the [Kolakoski sequence](kolakoski-sequence.md) but to numbers other than 1 and 2, also known as the [Generalized Kolakoski sequence](generalized-kolakoski-sequence.md).

[https://maths-people.anu.edu.au/~brent/pd/Kolakoski-ACCMCC.pdf](https://maths-people.anu.edu.au/~brent/pd/Kolakoski-ACCMCC.pdf) "A fast algorithm for the Kolakoski sequence" might provide the solution, the paper says:

> It is conjectured that the algorithm runs in time $O(n^α)$ and space $O(n^α)$, where $α = log(2)/ log(3) \approx 0.631$

and provides exactly a recurrence relation and a [dynamic programming](dynamic-programming.md) approach.

[https://www.reddit.com/r/dailyprogrammer/comments/8df7sm/20180419_challenge_357_intermediate_kolakoski/](https://www.reddit.com/r/dailyprogrammer/comments/8df7sm/20180419_challenge_357_intermediate_kolakoski/) might offer some reference implementations. It references a longer slide by Brent: [https://maths-people.anu.edu.au/~brent/pd/Kolakoski-UNSW.pdf](https://maths-people.anu.edu.au/~brent/pd/Kolakoski-UNSW.pdf)

[https://www.reddit.com/r/algorithms/comments/8cv3se/kolakoski_sequence/](https://www.reddit.com/r/algorithms/comments/8cv3se/kolakoski_sequence/) asks for an implementation but no one gave anything. Dupe question: [https://math.stackexchange.com/questions/2740997/kolakoski-sequence](https://math.stackexchange.com/questions/2740997/kolakoski-sequence) contains an answer with Python and Rust code but just for the original 1,2 case.

[https://github.com/runbobby/Kolakoski](https://github.com/runbobby/Kolakoski) has some C++ code but it is not well documented so it's not immediately easy to understand what it actually does. It does appear to consider the m n case however.

Bibliography:
- [https://pubs.sciepub.com/tjant/5/4/4/index.html](https://pubs.sciepub.com/tjant/5/4/4/index.html) Some Formulas for the Generalized Kolakoski Sequence Kol(a, b) by Abdallah Hammam. Maybe these identities could be useful.

Announcements:
- [https://mastodon.social/@cirosantilli/115446059895647190](https://mastodon.social/@cirosantilli/115446059895647190)
- [https://x.com/cirosantilli/status/1982782344135107043](https://x.com/cirosantilli/status/1982782344135107043)
- [https://www.linkedin.com/feed/update/urn:li:activity:7386417197440454658/](https://www.linkedin.com/feed/update/urn:li:activity:7386417197440454658/)

## ↑ Ancestors (15)

1. [Project Euler problem 943](project-euler-problem-943.md)
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
