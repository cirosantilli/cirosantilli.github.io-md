# Birch and Swinnerton-Dyer conjecture

↑ **Parent:** [Elliptic curve over the rational numbers](elliptic-curve-over-the-rational-numbers.md)  
🏷️ **Tags:** [Millennium Prize Problems](millennium-prize-problems.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Birch_and_Swinnerton-Dyer_conjecture)

The BSD conjecture states that if your name is long enough, it will always count as two letters on a famous conjecture.

Maybe also insert a joke about [BSD Operating Systems](berkeley-software-distribution.md) if you're into that kind of stuff.

The conjecture states that [Equation 10. "BSD conjecture"](#equation-bsd-conjecture) holds for every [elliptic curve over the rational numbers](elliptic-curve-over-the-rational-numbers.md) (which is defined by its  constants $a$ and $b$)

<a id="equation-bsd-conjecture"></a>
$$
\lim_{x \to \infty} \prod_{p \leq x} \frac{N_p}{p} = C \log(x)^r
$$

The conjecture, if true, provides a (possibly inefficient) way to calculate the [rank of an elliptic curve over the rational numbers](rank-of-an-elliptic-curve-over-the-rational-numbers.md), since we can calculate the [number of elements of an elliptic curve over a finite field](number-of-elements-of-an-elliptic-curve-over-a-finite-field.md) by [Schoof's algorithm](schoof-s-algorithm.md) in [polynomial time](p-complexity.md). So it is just a matter of calculating $N_p$ like that up to some point at which we are quite certain about $r$.

The [Wikipedia page of the this conecture](https://en.wikipedia.org/wiki/Birch_and_Swinnerton-Dyer_conjecture) is the perfect example of why [it is not possible to teach natural sciences on Wikipedia](it-is-not-possible-to-teach-natural-sciences-on-wikipedia.md). A [million dollar problem](millennium-prize-problems.md), and the page is thoroughly incomprehensible unless you already know everything!

<a id="image-lim-x-to-infty-prod-p-leq-x-frac-n-p-p-as-a-function-of-p-for-the-elliptic-curve-y-2-x-3-5x"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/BSD_data_plot_for_elliptic_curve_800h1.svg/500px-BSD_data_plot_for_elliptic_curve_800h1.svg.png" alt="" height="400">

**[Figure 3](#image-lim-x-to-infty-prod-p-leq-x-frac-n-p-p-as-a-function-of-p-for-the-elliptic-curve-y-2-x-3-5x). $\lim_{x \to \infty} \prod_{p \leq x} \frac{N_p}{p}$ as a function of $p$ for the elliptic curve $y^2 = x^3 - 5x$**. [Source](https://commons.wikimedia.org/wiki/File:BSD_data_plot_for_elliptic_curve_800h1.svg.png). The curve is known to have [rank](rank-of-an-elliptic-curve-over-the-rational-numbers.md) 1, and the logarithmic plot tends more and more to a line of slope 1 as expected from the conjecture, matching the rank.

<a id="video-birch-and-swinnerton-dyer-conjecture-by-kinertia-2020"></a>
**[Video 1](#video-birch-and-swinnerton-dyer-conjecture-by-kinertia-2020). Birch and Swinnerton-Dyer conjecture by Kinertia (2020)** [Source](https://www.youtube.com/watch?v=R9FKN9MIHlE).

<a id="video-the-1-000-000-birch-and-swinnerton-dyer-conjecture-by-absolutely-uniformly-confused-2022"></a>
**[Video 2](#video-the-1-000-000-birch-and-swinnerton-dyer-conjecture-by-absolutely-uniformly-confused-2022). The $1,000,000 Birch and Swinnerton-Dyer conjecture by Absolutely Uniformly Confused (2022)** [Source](https://www.youtube.com/watch?v=tjnwEGBUOLI). A respectable 1 minute attempt. But will be too fast for most people. The sweet spot is likely 2 minutes.

**Table of contents**

- [BSD conjecture bibliography](bsd-conjecture-bibliography.md)
  - [Birch and Swinnerton-Dyer conjecture in two minutes by Ciro Santilli](birch-and-swinnerton-dyer-conjecture-in-two-minutes-by-ciro-santilli.md)
  - [Notes on Elliptic Curves (II) by BSD](notes-on-elliptic-curves-ii-by-bsd.md)

## ↑ Ancestors (8)

1. [Elliptic curve over the rational numbers](elliptic-curve-over-the-rational-numbers.md)
2. [Domain of an elliptic curve](domain-of-an-elliptic-curve.md)
3. [Elliptic curve](elliptic-curve.md)
4. [Algebraic geometry](algebraic-geometry.md)
5. [Algebra](algebra-split.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Birch and Swinnerton-Dyer conjecture](birch-and-swinnerton-dyer-conjecture.md)
- [Quantum field theory](quantum-field-theory-split.md)
- [Rank of an elliptic curve over the rational numbers](rank-of-an-elliptic-curve-over-the-rational-numbers.md)
- [Reduction of an elliptic curve over the rational numbers to an elliptic curve over a finite field mod p](reduction-of-an-elliptic-curve-over-the-rational-numbers-to-an-elliptic-curve-over-a-finite-field-mod-p.md)
