# Twin prime conjecture

↑ **Parent:** [Twin prime](twin-prime.md)  
🏷️ **Tags:** [Famous conjecture](famous-conjecture.md), [Prime k-tuple conjecture](prime-k-tuple-conjecture.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Twin_prime_conjecture)

Let's show them how it's done with [primes](primes-bsdgames.md) + [awk](awk.md). Edit. They have a `-d` option which also shows gaps!!! Too strong:
```
sudo apt install bsdgames
primes -d 1 100 | awk '/\(2\)/{print $1 - 2, $1 }'
```
gives us the list of all twin primes up to 100:
```
0 2
3 5
5 7
11 13
17 19
29 31
41 43
59 61
71 73
```
Tested on [Ubuntu 22.10](ubuntu-22-10.md).

## ↑ Ancestors (8)

1. [Twin prime](twin-prime.md)
2. [Prime k-tuple](prime-k-tuple.md)
3. [Type of prime number](type-of-prime-number.md)
4. [Prime number](prime-number.md)
5. [Number theory](number-theory.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Prime k-tuple conjecture](prime-k-tuple-conjecture.md)
- [The beauty of mathematics](the-beauty-of-mathematics.md)
- [Yitang Zhang's theorem](yitang-zhang-s-theorem.md)
