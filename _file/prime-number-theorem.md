<h1 id="_file/prime-number-theorem">prime-number-theorem</h1>

↑ **Parent:** [Prime number theorem](../prime-number-theorem.md)

Consider this is a study in failed [computational number theory](../computational-number-theory.md).

The $n/ln(n)$ approximation converges really slowly, and we can't easy go far enough to see that the ration converges to 1 with only [awk](../awk.md) and [primes](../primes-bsdgames.md):
```
sudo apt intsall bsdgames
cd prime-number-theorem
./main.py 100000000
```
Runs in 30 minutes tested on [Ubuntu 22.10](../ubuntu-22-10.md) and [P51](../ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md), producing:

<a id="image-linear-pi-n-vs-n-ln-n-approximation-plot"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/prime-number-theorem/pi.png)

**[Figure 2](#image-linear-pi-n-vs-n-ln-n-approximation-plot). Linear $\pi(n)$ vs $n/ln(n)$ approximation plot**. $f(n) = n$ and $f(n) = log(n)$ are added to give a better sense of scale. $log(n)$ is too close to 0 and not visible, and the approximation almost overlaps entirely with $pi$.

<a id="image-pi-n-n-ln-n"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/prime-number-theorem/pi-minus.png)

**[Figure 3](#image-pi-n-n-ln-n). $\pi(n) - n/ln(n)$**. It is clear that the difference diverges, albeit very slowly.

<a id="image-pi-n-over-n-ln-n"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/prime-number-theorem/pi-over.png)

**[Figure 4](#image-pi-n-over-n-ln-n). $\pi(n)/(n/ln(n))$**. We just don't have enough points to clearly see that it is converging to 1.0, the convergence truly is very slow. The [logarithm integral](../logarithmic-integral-function.md) approximation is much much better, but we can't calculate it in [awk](../awk.md), sadface.

But looking at: [https://en.wikipedia.org/wiki/File:Prime_number_theorem_ratio_convergence.svg](https://en.wikipedia.org/wiki/File:Prime_number_theorem_ratio_convergence.svg) we see that it takes way longer to get closer to 1, even at $10^{24}$ it is still not super close. Inspecting the code there we see:
```
(* Supplement with larger known PrimePi values that are too large for \
Mathematica to compute *)
LargePiPrime = {{10^13, 346065536839}, {10^14, 3204941750802}, {10^15,
     29844570422669}, {10^16, 279238341033925}, {10^17,
    2623557157654233}, {10^18, 24739954287740860}, {10^19,
    234057667276344607}, {10^20, 2220819602560918840}, {10^21,
    21127269486018731928}, {10^22, 201467286689315906290}, {10^23,
    1925320391606803968923}, {10^24, 18435599767349200867866}};
```
so OK, it is not something doable on a [personal computer](../personal-computer.md) just like that.

## ↑ Ancestors (6)

1. [Prime number theorem](../prime-number-theorem.md)
2. [Prime number](../prime-number.md)
3. [Number theory](../number-theory.md)
4. [Area of mathematics](../area-of-mathematics.md)
5. [Mathematics](../mathematics-split.md)
6. [Ciro Santilli's Homepage](../split.md)
