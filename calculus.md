# Calculus

↑ **Parent:** [Area of mathematics](mathematics.md#area-of-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Calculus)

Well summarized as "the branch of mathematics that deals with [limits](#limit-mathematics)".

**Table of contents**

- [Mathematical analysis](#mathematical-analysis)
- [Limit (mathematics)](#limit-mathematics)
  - [Convergent series](#convergent-series)
  - [Continuous function](#continuous-function)
    - [Continuous problems are simpler than discrete ones](#continuous-problems-are-simpler-than-discrete-ones)
    - [Discrete](#discrete)
      - [Discretization](#discretization)
  - [Infinity](#infinity)
  - [L'Hôpital's rule](#l-hopital-s-rule)
- [Derivative](#derivative)
  - [Chain rule](#chain-rule)
    - [Multivariable chain rule](#multivariable-chain-rule)
  - [Differentiable function](#differentiable-function)
    - [Smoothness](#smoothness)
    - [Infinitely differentiable function](#infinitely-differentiable-function)
      - [Bump function](#bump-function)
        - [Flat top bump function](#flat-top-bump-function)
  - [Maxima and minima](#maxima-and-minima)
    - [Lifegard problem](#lifegard-problem)
    - [Derivative test](#derivative-test)
    - [Saddle point](#saddle-point)
  - [Newton dot notation](#newton-dot-notation)
  - [Partial derivative](#partial-derivative)
    - [Partial derivative notation](#partial-derivative-notation)
      - [Partial derivative symbol](#partial-derivative-symbol)
      - [Partial label partial derivative notation](#partial-label-partial-derivative-notation)
      - [Partial index partial derivative notation](#partial-index-partial-derivative-notation)
  - [Total derivative](#total-derivative)
  - [Directional derivative](#directional-derivative)
- [Integral](#integral)
  - [Area](#area)
    - [Volume](#volume)
  - [Riemann integral](#riemann-integral)
  - [Lebesgue integral](#lebesgue-integral)
    - [Lebesgue integral vs Riemann integral](#lebesgue-integral-vs-riemann-integral)
      - [Real world applications of the Lebesgue integral](#real-world-applications-of-the-lebesgue-integral)
    - [Lebesgue measurable](#lebesgue-measurable)
    - [Lebesgue integral of $\LP$ is complete but Riemann isn't](#lebesgue-integral-of-lp-is-complete-but-riemann-isn-t)
      - [Riesz-Fischer theorem](#riesz-fischer-theorem)
        - [$\LP$ is complete](#lp-is-complete)
        - [Fourier basis is complete for $\LTwo$](#fourier-basis-is-complete-for-l2)
          - [$L^p$ norm sequence convergence does not imply pointwise convergence](#lp-norm-sequence-convergence-does-not-imply-pointwise-convergence)
          - [Carleson's theorem](#carleson-s-theorem)
      - [Lp space](#lp-space)
        - [$L^1$](#l1-space)
        - [$\LTwo$](#l2)
          - [Plancherel theorem](#plancherel-theorem)
            - [The Fourier transform is a bijection in $L^2$](#the-fourier-transform-is-a-bijection-in-l-2)
            - [Every Riemann integrable function is Lebesgue integrable](#every-riemann-integrable-function-is-lebesgue-integrable)
- [Measure theory](#measure-theory)
- [Fourier series](#fourier-series)
  - [Applications of the Fourier series](#applications-of-the-fourier-series)
    - [Solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series)
  - [Discrete Fourier transform](#discrete-fourier-transform)
    - [Discrete Fourier transform of a real signal](#discrete-fourier-transform-of-a-real-signal)
    - [Normalized DFT](#normalized-dft)
    - [Fast Fourier transform](#fast-fourier-transform)
  - [Fourier transform](#fourier-transform)
    - [Multidimensional Fourier transform](#multidimensional-fourier-transform)
    - [Fourier inversion theorem](#fourier-inversion-theorem)
    - [Laplace transform](#laplace-transform)
  - [History of the Fourier series](#history-of-the-fourier-series)
- [Topology](#topology)
  - [Covering space](#covering-space)
    - [Double cover](#double-cover)
  - [Neighbourhood (mathematics)](#neighbourhood-mathematics)
  - [Topological space](#topological-space)
  - [Manifold](#manifold)
    - [Atlas (topology)](#atlas-topology)
      - [Coordinate chart](#coordinate-chart)
    - [Covariant derivative](#covariant-derivative)
    - [Differentiable manifold](#differentiable-manifold)
    - [Tangent space](#tangent-space)
      - [Tangent vector to a manifold](#tangent-vector-to-a-manifold)
    - [One-form](#one-form)
      - [Manifold by dimension](#manifold-by-dimension)
        - [3-manifold](#3-manifold)
        - [4-manifold](#4-manifold)
  - [Metric (mathematics)](#metric-mathematics)
    - [Metric space](#metric-space)
      - [Metric space vs normed vector space vs inner product space](#metric-space-vs-normed-vector-space-vs-inner-product-space)
      - [Complete metric space](#complete-metric-space)
      - [Normed vector space](#normed-vector-space)
        - [Inner product space](#inner-product-space)
          - [Inner product](#inner-product)
      - [Norm (mathematics)](#norm-mathematics)
        - [Norm induced by an inner product](#norm-induced-by-an-inner-product)
        - [Metric induced by a norm](#metric-induced-by-a-norm)
      - [Pseudometric space](#pseudometric-space)
  - [Compact space](#compact-space)
  - [Dense set](#dense-set)
  - [Connected space](#connected-space)
    - [Connected component](#connected-component)
    - [Simply connected space](#simply-connected-space)
      - [Loop (topology)](#loop-topology)
  - [Homotopy](#homotopy)
    - [Generalized Poincaré conjecture](#generalized-poincare-conjecture)
      - [Exotic sphere](#exotic-sphere)
      - [Poincaré conjecture](#poincare-conjecture)
      - [Classification of closed surfaces](#classification-of-closed-surfaces)
        - [Torus](#torus)
        - [Möbius strip](#mobius-strip)
        - [Klein bottle](#klein-bottle)
  - [Real coordinate space](#real-coordinate-space)
    - [Real line](#real-line)
    - [Real plane](#real-plane)
    - [Real coordinate space of dimension three](#real-coordinate-space-of-dimension-three)
    - [Real coordinate space of dimension four](#real-coordinate-space-of-dimension-four)
      - [Visualizing 4D](#visualizing-4d)
    - [Dimension](#dimension)
      - [Infinite dimensional](#infinite-dimensional)
        - [Finite dimensional](#finite-dimensional)
    - [Complex coordinate space](#complex-coordinate-space)
      - [Complex coordinate space of dimension 2](#complex-coordinate-space-of-dimension-2)
      - [Complex dot product](#complex-dot-product)
        - [Norm induced by the complex dot product](#norm-induced-by-the-complex-dot-product)
    - [Euclidean space](#euclidean-space)
      - [Euclidean metric signature matrix](#euclidean-metric-signature-matrix)
      - [Cartesian coordinate system](#cartesian-coordinate-system)
      - [Polar coordinate system](#polar-coordinate-system)
        - [Spherical coordinate system](#spherical-coordinate-system)
      - [Pythagorean theorem](#pythagorean-theorem)
      - [Non-Euclidean geometry](#non-euclidean-geometry)
        - [Elliptic geometry](#elliptic-geometry)
          - [Model of elliptic geometry](#model-of-elliptic-geometry)
            - [Projective elliptic geometry](#projective-elliptic-geometry)
        - [Hyperbolic gemoetry](#hyperbolic-gemoetry)
          - [Hyperbolic functions](#hyperbolic-functions)
            - [Hyperbolic sine](#hyperbolic-sine)
            - [Hyperbolic cossine](#hyperbolic-cossine)
- [Distribution (mathematics)](#distribution-mathematics)
  - [Dirac delta function](#dirac-delta-function)
    - [Green's function](#green-s-function)
    - [Heaviside step function](#heaviside-step-function)
  - [Normal distribution](#normal-distribution)
- [Complex analysis](#complex-analysis)
  - [Complex analysis bibliography](#complex-analysis-bibliography)
    - [Complex Analysis by Juan Carlos Ponce Campuzano](#complex-analysis-by-juan-carlos-ponce-campuzano)
  - [Holomorphic function](#holomorphic-function)
  - [Analytic continuation](#analytic-continuation)
    - [Visualizing the Riemann hypothesis and analytic continuation by 3Blue1Brown (2016)](#visualizing-the-riemann-hypothesis-and-analytic-continuation-by-3blue1brown-2016)
    - [Identity theorem](#identity-theorem)
      - [Riemann zeta function](#riemann-zeta-function)
        - [Riemann hypothesis](#riemann-hypothesis)
- [Hilbert space](#hilbert-space)
  - [Complete basis](#complete-basis)
- [Differential equation](#differential-equation)
  - [Euler number](#euler-number)
    - [Natural logarithm](#natural-logarithm)
      - [Logarithmic integral function](#logarithmic-integral-function)
      - [Euler-Mascheroni constant](#euler-mascheroni-constant)
  - [Linear differential equation](#linear-differential-equation)
    - [Holonomic function](#holonomic-function)
  - [Order of a differential equation](#order-of-a-differential-equation)
  - [Ordinary differential equation](#ordinary-differential-equation)
    - [Existence and uniqueness of solutions of ordinary differential equations](#existence-and-uniqueness-of-solutions-of-ordinary-differential-equations)
      - [Peano existence theorem](#peano-existence-theorem)
      - [Picard-Lindelöf theorem](#picard-lindelof-theorem)
    - [System of ordinary differential equations](#system-of-ordinary-differential-equations)
      - [System of linear ordinary differential equations](#system-of-linear-ordinary-differential-equations)
  - [Partial differential equation](#partial-differential-equation)
    - [Analytical method to solve a partial differential equation](#analytical-method-to-solve-a-partial-differential-equation)
      - [Separation of variables](#separation-of-variables)
    - [Numerical method to solve a partial differential equation](#numerical-method-to-solve-a-partial-differential-equation)
      - [Variational formulation of a partial differential equation](#variational-formulation-of-a-partial-differential-equation)
        - [Weak solution](#weak-solution)
      - [Finite element method](#finite-element-method)
    - [Important partial differential equation](#important-partial-differential-equation)
      - [Laplace's equation](#laplace-s-equation)
        - [Legendre polynomials](#legendre-polynomials)
        - [Poisson's equation](#poisson-s-equation)
          - [Uniqueness theorem for Poisson's equation](#uniqueness-theorem-for-poisson-s-equation)
        - [Harmonic function](#harmonic-function)
          - [Spherical harmonic](#spherical-harmonic)
      - [Heat equation](#heat-equation)
        - [Heat equation solution with Fourier series](#heat-equation-solution-with-fourier-series)
      - [Wave equation](#wave-equation)
        - [Damped wave equation](#damped-wave-equation)
          - [Plucked string model](#plucked-string-model)
        - [Wave equation boundary condition](#wave-equation-boundary-condition)
        - [Wave equation on string with one vibrating side](#wave-equation-on-string-with-one-vibrating-side)
        - [Wave equation solver](#wave-equation-solver)
        - [Wave equation solution with Fourier series](#wave-equation-solution-with-fourier-series)
        - [The wave equation can be seen as infinitely many infinitesimal coupled oscillators](#the-wave-equation-can-be-seen-as-infinitely-many-infinitesimal-coupled-oscillators)
        - [Lossy 1D Wave Equation](#lossy-1d-wave-equation)
        - [Wave](#wave)
          - [Wavelength](#wavelength)
          - [Standing wave](#standing-wave)
          - [Envelope (waves)](#envelope-waves)
        - [Polarization](#polarization)
          - [String polarization](#string-polarization)
        - [Diffraction](#diffraction)
          - [Huygens-Fresnel principle](#huygens-fresnel-principle)
            - [Kirchhoff's diffraction formula](#kirchhoff-s-diffraction-formula)
              - [Fraunhofer diffraction](#fraunhofer-diffraction)
              - [Fresnel diffraction](#fresnel-diffraction)
        - [Refraction](#refraction)
        - [Resonance](#resonance)
        - [Wave interference](#wave-interference)
          - [Interference pattern](#interference-pattern)
        - [2D wave equation on a circular domain](#2d-wave-equation-on-a-circular-domain)
          - [Bessel function](#bessel-function)
            - [Fourier-Bessel series](#fourier-bessel-series)
        - [Helmholtz equation](#helmholtz-equation)
    - [Existence and uniqueness of solutions of partial differential equations](#existence-and-uniqueness-of-solutions-of-partial-differential-equations)
    - [Partial differential equation solver](#partial-differential-equation-solver)
      - [FreeFem](#freefem)
        - [FreeFem examples](#freefem-examples)
          - [heat-dirichlet.1d.freefem](#heat-dirichlet-1d-freefem)
          - [heat-dirichlet-2d-freefem](#heat-dirichlet-2d-freefem)
      - [FEniCS Project](#fenics-project)
        - [Hans Petter Langtangen](#hans-petter-langtangen)
    - [System of partial differential equations](#system-of-partial-differential-equations)
    - [Classification of second order partial differential equations into elliptic, parabolic and hyperbolic](#classification-of-second-order-partial-differential-equations-into-elliptic-parabolic-and-hyperbolic)
      - [Elliptic partial differential equation](#elliptic-partial-differential-equation)
      - [Parabolic partial differential equation](#parabolic-partial-differential-equation)
      - [Hyperbolic partial differential equation](#hyperbolic-partial-differential-equation)
      - [Which boundary conditions lead to existence and uniqueness of a second order PDE](#which-boundary-conditions-lead-to-existence-and-uniqueness-of-a-second-order-pde)
  - [Phase space](#phase-space)
  - [Boundary condition](#boundary-condition)
    - [Initial condition](#initial-condition)
    - [Boundary value problem](#boundary-value-problem)
    - [Dirichlet boundary condition](#dirichlet-boundary-condition)
    - [Neumann boundary condition](#neumann-boundary-condition)
      - [Cauchy boundary condition](#cauchy-boundary-condition)
      - [Robin boundary condition](#robin-boundary-condition)
      - [Open boundary condition](#open-boundary-condition)
      - [Mixed boundary condition](#mixed-boundary-condition)
    - [Time dependent boundary condition](#time-dependent-boundary-condition)
  - [Control theory](#control-theory)
    - [Control engineering](#control-engineering)
    - [Control system](#control-system)
    - [Feedback](#feedback)
      - [Feedback control algorithm](#feedback-control-algorithm)
        - [Proportional-integral-derivative controller](#proportional-integral-derivative-controller)
- [Series (mathematics)](#series-mathematics)
  - [Power series](#power-series)
    - [Analytic function](#analytic-function)
      - [Sine and cossine](#sine-and-cossine)
        - [Sinusoidal](#sinusoidal)
        - [Sine](#sine)
        - [Cosine](#cosine)
    - [Radius of convergence](#radius-of-convergence)
    - [Taylor series](#taylor-series)
- [Gradient, Divergence, Curl, and Laplacian](#gradient-divergence-curl-and-laplacian)
  - [Curl (mathematics)](#curl-mathematics)
  - [Nabla symbol](#nabla-symbol)
    - [Del](#del)
  - [Divergence](#divergence)
  - [Gradient](#gradient)
  - [Laplace operator](#laplace-operator)
    - [d'Alembert operator](#d-alembert-operator)
- [Infinitesimal](#infinitesimal)

## Mathematical analysis

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mathematical_analysis)

A fancy name for [calculus](calculus.md), with the "more advanced" connotation.

## Limit (mathematics)

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Limit_(mathematics))

The fundamental concept of [calculus](calculus.md)!

The reason why the epsilon delta definition is so venerated is that it fits directly into well known methods of the [formalization of mathematics](formalization-of-mathematics.md), making the notion completely precise.

### Convergent series

↑ **Parent:** [Limit (mathematics)](#limit-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Convergent_series)

### Continuous function

↑ **Parent:** [Limit (mathematics)](#limit-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Continuous_function)

#### Continuous problems are simpler than discrete ones

↑ **Parent:** [Continuous function](#continuous-function)

This is a general philosophy that [Ciro Santilli](ciro-santilli.md), and likely others, observes over and over.

Basically, [continuity](#continuous-function), or higher order conditions like [differentiability](#differentiable-function) seem to impose greater constraints on problems, which make them more solvable.

Some good examples of that:
- complex [discrete](#discrete) problems:
  - [classification of finite groups](group.md#classification-of-finite-groups)
- simple [continuous](#continuous-function) problems:
  - characterization of [Lie groups](geometry.md#lie-group)

#### Discrete

↑ **Parent:** [Continuous function](#continuous-function)

Something that is very not [continuous](#continuous-function).

Notably studied in [discrete mathematics](mathematics.md#discrete-mathematics).

##### Discretization

↑ **Parent:** [Discrete](#discrete)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Discretization)

### Infinity

↑ **Parent:** [Limit (mathematics)](#limit-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Infinity)

> Chuck Norris counted to infinity. Twice.

There are a few related concepts that are called infinity in [mathematics](mathematics.md):
- [limits](#limit-mathematics) that are greater than any number
- the [cardinality](formalization-of-mathematics.md#cardinality) of a [set](formalization-of-mathematics.md#set-mathematics) that does not have a finite number of elements
- in some number systems, there is an explicit "element at infinity" that is not a [limit](#limit-mathematics), e.g. [projective geometry](geometry.md#projective-geometry)

<h3 id="l-hopital-s-rule">L'Hôpital's rule</h3>

↑ **Parent:** [Limit (mathematics)](#limit-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/L'Hôpital's_rule)

## Derivative

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Derivative)

The derivative of a function gives its slope at a point.

More precisely, it give sthe inclination of a tangent line that passes through that point.

![](https://web.archive.org/web/20240417202558if_/https://upload.wikimedia.org/wikipedia/commons/0/0f/Tangent_to_a_curve.svg)

**[Figure 1](#_27)** [Source](https://en.wikipedia.org/wiki/File:Tangent\_to\_a\_curve.svg).

### Chain rule

↑ **Parent:** [Derivative](#derivative)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chain_rule)

Here's an example of the chain rule. Suppose we want to calculate:

$$
\dv{}{x} e^{2x}
$$

So we have:

$$
f(x) = e^x \\
g(x) = 2x
$$

and so:

$$
f'(x) = e^x \\
g'(x) = 2
$$

Therefore the final result is:

$$
f'(g(x))g'(x) = e^{2x} 2 = 2 e ^{2x}
$$

#### Multivariable chain rule

↑ **Parent:** [Chain rule](#chain-rule)

### Differentiable function

↑ **Parent:** [Derivative](#derivative)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Differentiable_function)

#### Smoothness

↑ **Parent:** [Differentiable function](#differentiable-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Smoothness)

#### Infinitely differentiable function

↑ **Parent:** [Differentiable function](#differentiable-function)

##### Bump function

↑ **Parent:** [Infinitely differentiable function](#infinitely-differentiable-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bump_function)

###### Flat top bump function

↑ **Parent:** [Bump function](#bump-function)

[https://math.stackexchange.com/questions/1786964/is-it-possible-to-construct-a-smooth-flat-top-bump-function](https://math.stackexchange.com/questions/1786964/is-it-possible-to-construct-a-smooth-flat-top-bump-function)

### Maxima and minima

↑ **Parent:** [Derivative](#derivative)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Maxima_and_minima)

Given a [function](formalization-of-mathematics.md#function-mathematics) $f$:
- from some space. For beginners the [real numbers](formalization-of-mathematics.md#real-number) but more generally [topological spaces](#topological-space) should work in general
- to the [real numbers](formalization-of-mathematics.md#real-number)
we want to find the points $x$ of the [domain](formalization-of-mathematics.md#domain-of-a-function) of $f$ where the value of $f$ is smaller (for minima, or larger for maxima) than all other points in some [neighbourhood](#neighbourhood-mathematics) of $x$.

In the case of [Functionals](mechanics.md#functional), this problem is treated under the theory of the [calculus of variations](mechanics.md#calculus-of-variations).

#### Lifegard problem

↑ **Parent:** [Maxima and minima](#maxima-and-minima)

[https://pumphandle.consulting/2020/09/04/the-lifeguard-problem-solved/](https://pumphandle.consulting/2020/09/04/the-lifeguard-problem-solved/)

#### Derivative test

↑ **Parent:** [Maxima and minima](#maxima-and-minima)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Derivative_test)

#### Saddle point

↑ **Parent:** [Maxima and minima](#maxima-and-minima)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Saddle_point)

### Newton dot notation

↑ **Parent:** [Derivative](#derivative)

### Partial derivative

↑ **Parent:** [Derivative](#derivative)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Partial_derivative)

#### Partial derivative notation

↑ **Parent:** [Partial derivative](#partial-derivative)

##### Partial derivative symbol

↑ **Parent:** [Partial derivative notation](#partial-derivative-notation)  
🏷️ **Tags:** [Mathematical symbol that looks like a Greek letter but isn't](mathematics.md#mathematical-symbol-that-looks-like-a-greek-letter-but-isn-t)

Nope, it is not a [Greek letter](linguistics.md#greek-alphabet), notably it is not a lowercase [delta](linguistics.md#delta-letter). It is just some random made up symbol that looks like a [letter D](linguistics.md#d). Which is of course derived from [delta](linguistics.md#delta-letter), which is why it is all so damn confusing.

I think the symbol is usually just read as "[D](linguistics.md#d)" as in "d f d x" for $\pdv{F(x, y, z)}{x}$.

##### Partial label partial derivative notation

↑ **Parent:** [Partial derivative notation](#partial-derivative-notation)

##### Partial index partial derivative notation

↑ **Parent:** [Partial derivative notation](#partial-derivative-notation)

This notation is not so common in basic mathematics, but it is so incredibly convenient, especially with [Einstein notation](linear-algebra.md#einstein-notation) as shown at [Section "Einstein notation for partial derivatives"](linear-algebra.md#einstein-notation-for-partial-derivatives):

$$
\partial_0 F(x, y, z) = \pdv{F(x, y, z)}{x} \\
\partial_1 F(x, y, z) = \pdv{F(x, y, z)}{y} \\
\partial_2 F(x, y, z) = \pdv{F(x, y, z)}{x} \\
$$

This notation is similar to [partial label partial derivative notation](#partial-label-partial-derivative-notation), but it uses indices instead of labels such as $x$, $y$, etc.

### Total derivative

↑ **Parent:** [Derivative](#derivative)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Total_derivative)

The total derivative of a function assigns for every point of the domain a linear map with same domain, which is the best linear approximation to the function value around this point, i.e. the tangent plane.

E.g. in 1D:

$$
Total derivative = D[f(x_0)](x) = f(x_0) + \pdv{f}{x}(x_0) \times x
$$

and in 2D:

$$
D[f(x_0, y_0)](x, y) = f(x_0, y_0) + \pdv{f}{x}(x_0, y_0) \times x + \pdv{f}{y}(x_0, y_0) \times y
$$

### Directional derivative

↑ **Parent:** [Derivative](#derivative)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Directional_derivative)

## Integral

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Integral)

### Area

↑ **Parent:** [Integral](#integral)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Area)

#### Volume

↑ **Parent:** [Area](#area)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Volume)

[3D](#real-coordinate-space-of-dimension-three) [area](#area).

### Riemann integral

↑ **Parent:** [Integral](#integral)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Riemann_integral)

The easy and less generic [integral](#integral). The harder one is the [Lebesgue integral](#lebesgue-integral).

### Lebesgue integral

↑ **Parent:** [Integral](#integral)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lebesgue_integration)

"More complex and general" integral. Matches the [Riemann integral](#riemann-integral) for "simple functions", but also [works for some "funkier" functions that Riemann does not work for](#lebesgue-integral-vs-riemann-integral).

[Ciro Santilli](ciro-santilli.md) sometimes wonders how much someone can gain from learning this besides [the beauty of mathematics](mathematics.md#the-beauty-of-mathematics), since we can hand-wave a [Lebesgue integral](#lebesgue-integral) on almost anything that is of practical use. The beauty is good reason enough though.

#### Lebesgue integral vs Riemann integral

↑ **Parent:** [Lebesgue integral](#lebesgue-integral)

Advantages over Riemann:
- [Lebesgue integral of $\LP$ is complete but Riemann isn't](#lebesgue-integral-of-lp-is-complete-but-riemann-isn-t).
- [https://youtu.be/PGPZ0P1PJfw?t=710](https://youtu.be/PGPZ0P1PJfw?t=710) you are able to switch the order of integrals and limits of function sequences on non-uniform convergence. TODO why do we care? This is linked to the [Fourier series](#fourier-series) of course, but concrete example?

<a id="video-riemann-integral-vs-lebesgue-integral-by-the-bright-side-of-mathematics-2018"></a>
**[Video 1](#video-riemann-integral-vs-lebesgue-integral-by-the-bright-side-of-mathematics-2018). Riemann integral vs. Lebesgue integral by The Bright Side Of Mathematics (2018)** [Source](https://youtube.com/watch?v=PGPZ0P1PJfw). [https://youtube.com/watch?v=PGPZ0P1PJfw&t=808](https://youtube.com/watch?v=PGPZ0P1PJfw&t=808) shows how Lebesgue can be visualized as a partition of the function range instead of domain, and then you just have to be able to measure the size of pre-images.

One advantage of that is that the range is always one dimensional.

But the main advantage is that having infinitely many discontinuities does not matter.

Infinitely many discontinuities can make the Riemann partitioning diverge.

But in Lebesgue, you are instead measuring the size of preimage, and to fit infinitely many discontinuities in a finite domain, the size of this preimage is going to be zero.

So then the question becomes more of "how to define the measure of a subset of the domain".

Which is why we then fall into [measure theory](#measure-theory)!

---

##### Real world applications of the Lebesgue integral

↑ **Parent:** [Lebesgue integral vs Riemann integral](#lebesgue-integral-vs-riemann-integral)

In "practice" it is likely "useless", because the functions that it can integrate that Riemann can't are just too funky to appear in practice :-)

Its value is much more indirect and subtle, as in "it serves as a solid basis of [quantum mechanics](quantum-mechanics.md)" due to the definition of [Hilbert spaces](#hilbert-space).

Bibliography:
- [https://math.stackexchange.com/questions/53121/how-do-people-apply-the-lebesgue-integration-theory](https://math.stackexchange.com/questions/53121/how-do-people-apply-the-lebesgue-integration-theory)
- [https://www.quora.com/What-are-some-real-life-applications-of-Lebesgue-Integration](https://www.quora.com/What-are-some-real-life-applications-of-Lebesgue-Integration)

#### Lebesgue measurable

↑ **Parent:** [Lebesgue integral](#lebesgue-integral)

<h4 id="lebesgue-integral-of-lp-is-complete-but-riemann-isn-t">Lebesgue integral of <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.6833em;"></span><span class="mord"><span class="mord mathnormal">L</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.6644em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">p</span></span></span></span></span></span></span></span></span></span></span> is complete but Riemann isn't</h4>

↑ **Parent:** [Lebesgue integral](#lebesgue-integral)

$\LP$ is:
- [complete](#complete-metric-space) under the Lebesgue integral, this result is may be called the [Riesz-Fischer theorem](#riesz-fischer-theorem)
- not complete under the [Riemann integral](#riemann-integral): [https://math.stackexchange.com/questions/397369/space-of-riemann-integrable-functions-not-complete](https://math.stackexchange.com/questions/397369/space-of-riemann-integrable-functions-not-complete)

And then this is why [quantum mechanics](quantum-mechanics.md) basically lives in [$\LTwo$](#l2): not being complete makes no sense physically, it would mean that you can get closer and closer to states that don't exist!

TODO intuition

##### Riesz-Fischer theorem

↑ **Parent:** [Lebesgue integral of $\LP$ is complete but Riemann isn't](#lebesgue-integral-of-lp-is-complete-but-riemann-isn-t)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Riesz–Fischer_theorem)

A measurable function defined on a closed interval is square integrable (and therefore in [$\LTwo$](#l2)) if and only if [Fourier series](#fourier-series) converges in [$\LTwo$](#l2) norm the function:

$$
\lim_{N \to \infty} \left \Vert S_N f - f \right \|_2 = 0
$$

###### $\LP$ is complete

↑ **Parent:** [Riesz-Fischer theorem](#riesz-fischer-theorem)

TODO

<h6 id="fourier-basis-is-complete-for-l2">Fourier basis is complete for <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.8141em;"></span><span class="mord"><span class="mord mathnormal">L</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">2</span></span></span></span></span></span></span></span></span></span></span></h6>

↑ **Parent:** [Riesz-Fischer theorem](#riesz-fischer-theorem)

[https://math.stackexchange.com/questions/316235/proving-that-the-fourier-basis-is-complete-for-cr-2-pi-c-with-l2-norm](https://math.stackexchange.com/questions/316235/proving-that-the-fourier-basis-is-complete-for-cr-2-pi-c-with-l2-norm)

[Riesz-Fischer theorem](#riesz-fischer-theorem) is a norm version of it, and [Carleson's theorem](#carleson-s-theorem) is stronger pointwise almost everywhere version.

Note that the [Riesz-Fischer theorem](#riesz-fischer-theorem) is weaker because the pointwise limit could not exist just according to it: [$l^p$ norm sequence convergence does not imply pointwise convergence](#lp-norm-sequence-convergence-does-not-imply-pointwise-convergence).

###### $L^p$ norm sequence convergence does not imply pointwise convergence

↑ **Parent:** [Fourier basis is complete for $\LTwo$](#fourier-basis-is-complete-for-l2)

[https://math.stackexchange.com/questions/138043/does-convergence-in-lp-imply-convergence-almost-everywhere](https://math.stackexchange.com/questions/138043/does-convergence-in-lp-imply-convergence-almost-everywhere)

There are explicit examples of this. We can have ever thinner disturbances to convergence that keep getting less and less area, but never cease to move around.

If it does converge pointwise to something, then it must match of course.

<h6 id="carleson-s-theorem">Carleson's theorem</h6>

↑ **Parent:** [Fourier basis is complete for $\LTwo$](#fourier-basis-is-complete-for-l2)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Carleson's_theorem)

The [Fourier series](#fourier-series) of an [$\LTwo$](#l2) function (i.e. the function generated from the infinite sum of weighted sines) converges to the function pointwise almost everywhere.

The theorem also seems to hold (maybe trivially given the transform result) for the [Fourier series](#fourier-series) (TODO if trivially, why trivially).

Only proved in 1966, and known to be a hard result without any known simple proof.

This theorem of course implies that [Fourier basis is complete for $\LTwo$](#fourier-basis-is-complete-for-l2), as it explicitly constructs a decomposition into the Fourier basis for every single function.

TODO vs [Riesz-Fischer theorem](#riesz-fischer-theorem). Is this just a stronger pointwise result, while Riesz-Fischer is about norms only?

One of the many [fourier inversion theorems](#fourier-inversion-theorem).

##### Lp space

↑ **Parent:** [Lebesgue integral of $\LP$ is complete but Riemann isn't](#lebesgue-integral-of-lp-is-complete-but-riemann-isn-t)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lp_space)

Integrable functions to the power $p$, usually and in this text assumed under the [Lebesgue integral](#lebesgue-integral) because: [Lebesgue integral of $\LP$ is complete but Riemann isn't](#lebesgue-integral-of-lp-is-complete-but-riemann-isn-t)

<h6 id="l1-space"><span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.8141em;"></span><span class="mord"><span class="mord mathnormal">L</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">1</span></span></span></span></span></span></span></span></span></span></span></h6>

↑ **Parent:** [Lp space](#lp-space)

<h6 id="l2"><span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.8141em;"></span><span class="mord"><span class="mord mathnormal">L</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">2</span></span></span></span></span></span></span></span></span></span></span></h6>

↑ **Parent:** [Lp space](#lp-space)

[$\LP$](#lp-space) for $p == 2$.

$\LTwo$ is by far the most important of $\LP$ because it is [quantum mechanics states](quantum-mechanics.md#mathematical-formulation-of-quantum-mechanics) live, because the total probability of being in any state has to be 1!

[$\LTwo$](#l2) has some crucially important properties that other $\LP$ don't (TODO confirm and make those more precise):
- it is the only $\LP$ that is [Hilbert space](#hilbert-space) because it is the only one where an inner product compatible with the metric can be defined:
  - [https://math.stackexchange.com/questions/2005632/l2-is-the-only-hilbert-space-parallelogram-law-and-particular-ft-gt](https://math.stackexchange.com/questions/2005632/l2-is-the-only-hilbert-space-parallelogram-law-and-particular-ft-gt)
  - [https://www.quora.com/Why-is-L2-a-Hilbert-space-but-not-Lp-or-higher-where-p-2](https://www.quora.com/Why-is-L2-a-Hilbert-space-but-not-Lp-or-higher-where-p-2)
- [Fourier basis is complete for $\LTwo$](#fourier-basis-is-complete-for-l2), which is great for solving [differential equation](#differential-equation)

###### Plancherel theorem

↑ **Parent:** [$\LTwo$](#l2)

Some sources say that this is just the part that says that the [norm](#norm-mathematics) of a [$\LTwo$](#l2) function is the same as the norm of its [Fourier transform](#fourier-transform).

Others say that this theorem actually says that the [Fourier transform](#fourier-transform) is [bijective](formalization-of-mathematics.md#bijection).

The comment at [https://math.stackexchange.com/questions/446870/bijectiveness-injectiveness-and-surjectiveness-of-fourier-transformation-define/1235725#1235725](https://math.stackexchange.com/questions/446870/bijectiveness-injectiveness-and-surjectiveness-of-fourier-transformation-define/1235725#1235725) may be of interest, it says that the [bijection](formalization-of-mathematics.md#bijection) statement is an easy consequence from the [norm](#norm-mathematics) one, thus the confusion.

TODO does it require it to be in [$l^1$](#l1-space) as well? [Wikipedia](website.md#wikipedia) [https://en.wikipedia.org/w/index.php?title=Plancherel_theorem&oldid=987110841](https://en.wikipedia.org/w/index.php?title=Plancherel_theorem&oldid=987110841) says yes, but [https://courses.maths.ox.ac.uk/node/view_material/53981](https://courses.maths.ox.ac.uk/node/view_material/53981) does not mention it.

<h6 id="the-fourier-transform-is-a-bijection-in-l-2">The Fourier transform is a bijection in <span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.8141em;"></span><span class="mord"><span class="mord mathnormal">L</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">2</span></span></span></span></span></span></span></span></span></span></span></h6>

↑ **Parent:** [Plancherel theorem](#plancherel-theorem)

As mentioned at [Section "Plancherel theorem"](#plancherel-theorem), some people call this part of [Plancherel theorem](#plancherel-theorem), while others say it is just a corollary.

This is an important fact in [quantum mechanics](quantum-mechanics.md), since it is because of this that it makes sense to talk about [position and momentum space](quantum-mechanics.md#position-and-momentum-space) as two dual representations of the [wave function](quantum-mechanics.md#wave-function) that contain the exact same amount of information.

###### Every Riemann integrable function is Lebesgue integrable

↑ **Parent:** [Plancherel theorem](#plancherel-theorem)

But only for the proper Riemann integral: [https://math.stackexchange.com/questions/2293902/functions-that-are-riemann-integrable-but-not-lebesgue-integrable](https://math.stackexchange.com/questions/2293902/functions-that-are-riemann-integrable-but-not-lebesgue-integrable)

## Measure theory

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Measure_(mathematics))

Main motivation: [Lebesgue integral](#lebesgue-integral).

The Bright Side Of Mathematics 2019 playlist: [https://www.youtube.com/watch?v=xZ69KEg7ccU&list=PLBh2i93oe2qvMVqAzsX1Kuv6-4fjazZ8j](https://www.youtube.com/watch?v=xZ69KEg7ccU&list=PLBh2i93oe2qvMVqAzsX1Kuv6-4fjazZ8j)

The key idea, is that we can't define a measure for the power set of R. Rather, we must select a large measurable subset, and the Borel sigma algebra is a good choice that matches intuitions.

## Fourier series

↑ **Parent:** [Calculus](calculus.md)  
🏷️ **Tags:** [Complete basis](#complete-basis)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fourier_series)

Approximates an original function by sines. If the function is "well behaved enough", the approximation is to arbitrary precision.

[Fourier](mathematics.md#joseph-fourier)'s original motivation, and a key application, is [solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series).

Can only be used to approximate for periodic functions (obviously from its definition!). The [Fourier transform](#fourier-transform) however overcomes that restriction:
- [https://math.stackexchange.com/questions/1115240/can-a-non-periodic-function-have-a-fourier-series](https://math.stackexchange.com/questions/1115240/can-a-non-periodic-function-have-a-fourier-series)
- [https://math.stackexchange.com/questions/1378633/every-function-can-be-represented-as-a-fourier-series](https://math.stackexchange.com/questions/1378633/every-function-can-be-represented-as-a-fourier-series)

The Fourier series behaves really nicely in [$\LTwo$](#l2), where it always exists and converges pointwise to the function: [Carleson's theorem](#carleson-s-theorem).

<a id="video-but-what-is-a-fourier-series-by-3blue1brown-2019"></a>
**[Video 2](#video-but-what-is-a-fourier-series-by-3blue1brown-2019). But what is a Fourier series? by 3Blue1Brown (2019)** [Source](https://www.youtube.com/watch?v=r6sGWTCMz2k). Amazing 2D visualization of the decomposition of complex functions.

### Applications of the Fourier series

↑ **Parent:** [Fourier series](#fourier-series)

#### Solving partial differential equations with the Fourier series

↑ **Parent:** [Applications of the Fourier series](#applications-of-the-fourier-series)

See: [https://math.stackexchange.com/questions/579453/real-world-application-of-fourier-series/3729366#3729366](https://math.stackexchange.com/questions/579453/real-world-application-of-fourier-series/3729366#3729366) from [heat equation solution with Fourier series](#heat-equation-solution-with-fourier-series).

[Separation of variables](#separation-of-variables) of certain equations like the [heat equation](#heat-equation) and [wave equation](#wave-equation) are solved immediately by calculating the [Fourier series](#fourier-series) of initial conditions!

Other basis besides the Fourier series show up for other equations, e.g.:
- [Bessel function](#bessel-function)
- [Hermite polynomials](quantum-mechanics.md#hermite-polynomials)

### Discrete Fourier transform

↑ **Parent:** [Fourier series](#fourier-series)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Discrete_Fourier_transform)

Input: a sequence of $N$ [complex numbers](formalization-of-mathematics.md#complex-number) $x_k$.

Output: another sequence of $N$ [complex numbers](formalization-of-mathematics.md#complex-number) $X_k$ such that:

$$
x_n = \frac{1}{N} \sum_{k=0}^{N-1} X_k e^{i 2 \pi \frac{k n}{N}}
$$

Intuitively, this means that we are braking up the complex signal into $N$ [sinusoidal](#sinusoidal) frequencies:
- $X_0$: is kind of magic and ends up being a constant added to the signal because $e^{i 2 \pi \frac{k n}{N}} = e^{0} = 1$
- $X_1$: [sinusoidal](#sinusoidal) that completes one cycle over the signal. The larger the $N$, the larger the resolution of that [sinusoidal](#sinusoidal). But it completes one cycle regardless.
- $X_2$: [sinusoidal](#sinusoidal) that completes two cycles over the signal
- ...
- $X_{N-1}$: [sinusoidal](#sinusoidal) that completes $N-1$ cycles over the signal
and  is the amplitude of each sine.

We use [Zero-based numbering](software.md#zero-based-numbering) in our definitions because it just makes every formula simpler.

Motivation: similar to the [Fourier transform](#fourier-transform):
- compression: a [sine](#sine) would use N points in the time domain, but in the frequency domain just one, so we can throw the rest away. A sum of two sines, only two. So if your signal has periodicity, in general you can compress it with the transform
- noise removal: many systems add noise only at certain frequencies, which are hopefully different from the main frequencies of the actual signal. By doing the transform, we can remove those frequencies to attain a better [signal-to-noise](technology.md#signal-to-noise-ratio)
In particular, the [discrete Fourier transform](#discrete-fourier-transform) is used in [signal processing](technology.md#signal-processing) after a [analog-to-digital converter](electronics.md#analog-to-digital-converter). [Digital signal processing](technology.md#digital-signal-processing) historically likely grew more and more over analog processing as digital [processors](computer-hardware.md#processor-computing) got faster and faster as it gives more flexibility in algorithm design.

Sample software implementations:
- [numpy.fft](programming-language.md#numpy-fft), notably see the example: [numpy/fft.py](programming-language.md#_file/numpy/fft.py)

<a id="image-dft-of-2-sin-t-plus-cos-4t-with-25-points-discrete-fourier-transform"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/home/numpy/fft_plot.svg" alt="" height="600">

**[Figure 2](#image-dft-of-2-sin-t-plus-cos-4t-with-25-points-discrete-fourier-transform). DFT of $2 \sin(t) + \cos(4t)$ with 25 points**. This is a simple example of a [discrete Fourier transform](#discrete-fourier-transform) for a real input signal. It illustrates how the [DFT](#discrete-fourier-transform) takes N [complex numbers](formalization-of-mathematics.md#complex-number) as input, and produces N [complex numbers](formalization-of-mathematics.md#complex-number) as output. It also illustrates how the [discrete Fourier transform of a real signal](#discrete-fourier-transform-of-a-real-signal) is symmetric around the center point.

#### Discrete Fourier transform of a real signal

↑ **Parent:** [Discrete Fourier transform](#discrete-fourier-transform)

See sections: "Example 1 - N even", "Example 2 - N odd" and "Representation in terms of sines and cosines" of [https://www.statlect.com/matrix-algebra/discrete-Fourier-transform-of-a-real-signal](https://www.statlect.com/matrix-algebra/discrete-Fourier-transform-of-a-real-signal)

The transform still has complex numbers.

Summary:
- $X_0$ is real
- $X_1 = \conj{X_{N-1}}$
- $X_2 = \conj{X_{N-2}}$
- $X_k = \conj{X_{N-k}}$
Therefore, we only need about half of $X_k$ to represent the signal, as the other half can be derived by conjugation.

"Representation in terms of sines and cosines" from [https://www.statlect.com/matrix-algebra/discrete-Fourier-transform-of-a-real-signal](https://www.statlect.com/matrix-algebra/discrete-Fourier-transform-of-a-real-signal) then gives explicit formulas in terms of $X_k$.

[NumPy](programming-language.md#numpy) for example has "Real FFTs" for this: [https://numpy.org/doc/1.24/reference/routines.fft.html#real-ffts](https://numpy.org/doc/1.24/reference/routines.fft.html#real-ffts)

<a id="image-dft-of-2-sin-t-plus-cos-4t-with-25-points-discrete-fourier-transform-of-a-real-signal"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/home/numpy/fft_plot.svg" alt="" height="600">

**[Figure 3](#image-dft-of-2-sin-t-plus-cos-4t-with-25-points-discrete-fourier-transform-of-a-real-signal). DFT of $2 \sin(t) + \cos(4t)$ with 25 points**. Source at: [numpy/fft\_plot.py](programming-language.md#_file/numpy/fft_plot.py). This plot illustrates how the DFT of a real signal is symmetric around the middle point, and so only half of the transform points are needed to reconstruct the original signal. We also see how the phase of the sinusoids determines if their DFT components are real or imaginary.

#### Normalized DFT

↑ **Parent:** [Discrete Fourier transform](#discrete-fourier-transform)

There are actually two possible definitions for the DFT:
- 1/N, given as "the default" in many sources:$$
  x_n = \frac{1}{N} \sum_{k=0}^{N-1} X_k e^{i 2 \pi \frac{k n}{N}}
  $$
- $1/\sqrt{N}$, known as the "normalized DFT" by some sources: [https://www.dsprelated.com/freebooks/mdft/Normalized_DFT.html](https://www.dsprelated.com/freebooks/mdft/Normalized_DFT.html), definition which we adopt:$$
  x_n = \frac{1}{N} \sum_{k=0}^{N-1} X_k e^{i 2 \pi \frac{k n}{N}}
  $$

The $1/\sqrt{N}$ is nicer mathematically as the inverse becomse more symmetric, and power is conserved between time and frequency domains.
- [https://math.stackexchange.com/questions/3285758/scaling-magnitude-of-the-dft](https://math.stackexchange.com/questions/3285758/scaling-magnitude-of-the-dft)
- [https://dsp.stackexchange.com/questions/63001/why-should-i-scale-the-fft-using-1-n](https://dsp.stackexchange.com/questions/63001/why-should-i-scale-the-fft-using-1-n)
- [https://www.dsprelated.com/freebooks/mdft/Normalized_DFT.html](https://www.dsprelated.com/freebooks/mdft/Normalized_DFT.html)

#### Fast Fourier transform

↑ **Parent:** [Discrete Fourier transform](#discrete-fourier-transform)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fast_Fourier_transform)

An efficient [algorithm](computer-science.md#algorithm) to calculate the [discrete Fourier transform](#discrete-fourier-transform).

### Fourier transform

↑ **Parent:** [Fourier series](#fourier-series)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fourier_transform)

Continuous version of the [Fourier series](#fourier-series).

Can be used to represent functions that are not periodic: [https://math.stackexchange.com/questions/221137/what-is-the-difference-between-fourier-series-and-fourier-transformation](https://math.stackexchange.com/questions/221137/what-is-the-difference-between-fourier-series-and-fourier-transformation) while the [Fourier series](#fourier-series) is only for periodic functions.

Of course, every function defined on a finite line segment (i.e. a [compact space](#compact-space)).

Therefore, the [Fourier transform](#fourier-transform) can be seen as a generalization of the [Fourier series](#fourier-series) that can also decompose functions defined on the entire [real line](#real-line).

As a more concrete example, just like the [Fourier series](#fourier-series) is how you solve the [heat equation](#heat-equation) on a line segment with [Dirichlet boundary conditions](#dirichlet-boundary-condition) as shown at: [Section "Solving partial differential equations with the Fourier series"](#solving-partial-differential-equations-with-the-fourier-series), the [Fourier transform](#fourier-transform) is what you need to solve the problem when the [domain](formalization-of-mathematics.md#domain-of-a-function) is the entire [real line](#real-line).

#### Multidimensional Fourier transform

↑ **Parent:** [Fourier transform](#fourier-transform)

Lecture notes:
- [http://www.robots.ox.ac.uk/~az/lectures/ia/lect2.pdf](http://www.robots.ox.ac.uk/~az/lectures/ia/lect2.pdf) Lecture 2: 2D Fourier transforms and applications by A. Zisserman (2014)

<a id="video-how-the-2d-fft-works-by-mike-x-cohen-2017"></a>
**[Video 3](#video-how-the-2d-fft-works-by-mike-x-cohen-2017). How the 2D FFT works by Mike X Cohen (2017)** [Source](https://www.youtube.com/watch?v=v743U7gvLq0). Animations showing how the 2D Fourier transform looks like for simple inpuf functions.

#### Fourier inversion theorem

↑ **Parent:** [Fourier transform](#fourier-transform)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fourier_inversion_theorem)

A set of theorems that prove under different conditions that the [Fourier transform](#fourier-transform) has an inverse for a given space, examples:
- [Carleson's theorem](#carleson-s-theorem) for [$\LTwo$](#l2)

#### Laplace transform

↑ **Parent:** [Fourier transform](#fourier-transform)

<a id="video-the-laplace-transform-a-generalized-fourier-transform-by-steve-brunton-2020"></a>
**[Video 4](#video-the-laplace-transform-a-generalized-fourier-transform-by-steve-brunton-2020). The Laplace Transform: A Generalized Fourier Transform by Steve Brunton (2020)** [Source](https://www.youtube.com/watch?v=7UvtU75NXTg). Explains how the Laplace transform works for functions that do not go to zero on infinity, which is a requirement for the [Fourier transform](#fourier-transform). No applications in that video yet unfortunately.

### History of the Fourier series

↑ **Parent:** [Fourier series](#fourier-series)

First published by Fourier in 1807 to solve the [heat equation](#heat-equation).

## Topology

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Topology)

Topology is the plumbing of [calculus](calculus.md).

The key concept of topology is a [neighbourhood](#neighbourhood-mathematics).

Just by havin the notion of neighbourhood, concepts such as [limit](#limit-mathematics) and [continuity](#continuous-function) can be defined without the need to specify a precise numerical value to the distance between two points with a [metric](#metric-mathematics).

As an example. consider the [orthogonal group](geometry.md#orthogonal-group), which is also naturally a [topological space](#topological-space). That group does not usually have a notion of distance defined for it by default. However, we can still talk about certain properties of it, e.g. that [the orthogonal group is compact](geometry.md#the-orthogonal-group-is-compact), and that [the orthogonal group has two connected components](geometry.md#connected-components-of-the-orthogonal-group).

### Covering space

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Covering_space)

Basically it is a larger space such that there exists a [surjection](formalization-of-mathematics.md#surjective-function) from the large space onto the smaller space, while still being compatible with the [topology](#topology) of the small space.

We can characterize the cover by how injective the function is. E.g. if two elements of the large space map to each element of the small space, then we have a [double cover](#double-cover) and so on.

#### Double cover

↑ **Parent:** [Covering space](#covering-space)

### Neighbourhood (mathematics)

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Neighbourhood_(mathematics))

The key concept of [topology](#topology).

### Topological space

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Topological_space)

### Manifold

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Manifold)

We map each point and a small enough [neighbourhood](#neighbourhood-mathematics) of it to [$\R^n$](#real-coordinate-space), so we can talk about the manifold points in terms of coordinates.

Does not require any further structure besides a consistent [topological](#topology) map. Notably, does not require [metric](#metric-mathematics) nor an addition operation to make a [vector space](linear-algebra.md#vector-space).

Manifolds are [cool](cirism.md#good). Especially [differentiable manifolds](#differentiable-manifold) which we can do [calculus](calculus.md) on.

A notable example of a [Non-Euclidean geometry](#non-euclidean-geometry) manifold is the space of [generalized coordinates](mechanics.md#generalized-coordinate) of a [Lagrangian](mechanics.md#lagrangian). For example, in a problem such as the [double pendulum](mechanics.md#double-pendulum), some of those generalized coordinates could be angles, which wrap around and thus are not [euclidean](#euclidean-space).

#### Atlas (topology)

↑ **Parent:** [Manifold](#manifold)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Atlas_(topology))

Collection of [coordinate charts](#coordinate-chart).

The key element in the definition of a [manifold](#manifold).

##### Coordinate chart

↑ **Parent:** [Atlas (topology)](#atlas-topology)

#### Covariant derivative

↑ **Parent:** [Manifold](#manifold)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Covariant_derivative)

A generalized definition of [derivative](#derivative) that works on [manifolds](#manifold).

TODO: how does it maintain a single value even across different [coordinate charts](#coordinate-chart)?

#### Differentiable manifold

↑ **Parent:** [Manifold](#manifold)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Differentiable_manifold)

TODO find a concrete numerical example of doing [calculus](calculus.md) on a differentiable manifold and visualizing it. Likely start with a boring circle. That would be sweet...

#### Tangent space

↑ **Parent:** [Manifold](#manifold)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tangent_space)

TODO what's the point of it.

Bibliography:
- [https://www.youtube.com/watch?v=j1PAxNKB_Zc](https://www.youtube.com/watch?v=j1PAxNKB_Zc) Manifolds \#6 - Tangent Space (Detail) by WHYB maths (2020). This is worth looking into.
  - [https://www.youtube.com/watch?v=oxB4aH8h5j4](https://www.youtube.com/watch?v=oxB4aH8h5j4) actually gives a more concrete example. Basically, the vectors are defined by saying "we are doing the [Directional derivative](#directional-derivative) of any function along this direction".

    One thing to remember is that of course, the most convenient way to define a function $f$ and to specify a direction, is by using one of the [coordinate charts](#coordinate-chart).

    We can then just switch between charts by change of basis.
- [http://jakobschwichtenberg.com/lie-algebra-able-describe-group/](http://jakobschwichtenberg.com/lie-algebra-able-describe-group/) by [Jakob Schwichtenberg](physicist.md#jakob-schwichtenberg)
- [https://math.stackexchange.com/questions/1388144/what-exactly-is-a-tangent-vector/2714944](https://math.stackexchange.com/questions/1388144/what-exactly-is-a-tangent-vector/2714944) What exactly is a tangent vector? on [Stack Exchange](stack-overflow.md#stack-exchange)

##### Tangent vector to a manifold

↑ **Parent:** [Tangent space](#tangent-space)

A member of a [tangent space](#tangent-space).

#### One-form

↑ **Parent:** [Manifold](#manifold)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/One-form)

[https://www.youtube.com/watch?v=tq7sb3toTww&list=PLxBAVPVHJPcrNrcEBKbqC_ykiVqfxZgNl&index=19](https://www.youtube.com/watch?v=tq7sb3toTww&list=PLxBAVPVHJPcrNrcEBKbqC_ykiVqfxZgNl&index=19) mentions that it is a bit like a [dot product](linear-algebra.md#dot-product) but for a [tangent vector to a manifold](#tangent-vector-to-a-manifold): it measures how much that vector [derives](#derivative) along a given direction.

##### Manifold by dimension

↑ **Parent:** [One-form](#one-form)

###### 3-manifold

↑ **Parent:** [Manifold by dimension](#manifold-by-dimension)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/3-manifold)

###### 4-manifold

↑ **Parent:** [Manifold by dimension](#manifold-by-dimension)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/4-manifold)

### Metric (mathematics)

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Metric_(mathematics))

A metric is a function that give the distance, i.e. a [real number](formalization-of-mathematics.md#real-number), between any two elements of a space.

A metric may be induced from a [norm](#norm-mathematics) as shown at: [Section "Metric induced by a norm"](#metric-induced-by-a-norm).

Because a [norm can be induced by an inner product](#norm-induced-by-an-inner-product), and the [inner product](#inner-product) given by the [matrix representation of a positive definite symmetric bilinear form](linear-algebra.md#matrix-representation-of-a-positive-definite-symmetric-bilinear-form), in simple cases metrics can also be represented by a [matrix](linear-algebra.md#matrix).

#### Metric space

↑ **Parent:** [Metric (mathematics)](#metric-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Metric_space)

Canonical example: [Euclidean space](#euclidean-space).

##### Metric space vs normed vector space vs inner product space

↑ **Parent:** [Metric space](#metric-space)

TODO examples:
- [metric space](#metric-space) that is not a [normed vector space](#normed-vector-space)
- [norm](#norm-mathematics) vs [metric](#metric-mathematics): a norm gives size of one element. A [metric](#metric-mathematics) is the distance between two elements. Given a norm in a space with subtraction, we can obtain a distance function: the [metric induced by a norm](#metric-induced-by-a-norm).

<a id="image-hierarchy-of-topological-metric-normed-and-inner-product-spaces"></a>
![](https://upload.wikimedia.org/wikipedia/commons/7/74/Mathematical_Spaces.png)

**[Figure 4](#image-hierarchy-of-topological-metric-normed-and-inner-product-spaces). Hierarchy of topological, metric, normed and inner product spaces**. [Source](https://commons.wikimedia.org/wiki/File:Mathematical_Spaces.png).

##### Complete metric space

↑ **Parent:** [Metric space](#metric-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Complete_metric_space)

In plain English: the space has no visible holes. If you start walking less and less on each step, you always converge to something that also falls in the space.

One notable example where completeness matters: [Lebesgue integral of $\LP$ is complete but Riemann isn't](#lebesgue-integral-of-lp-is-complete-but-riemann-isn-t).

##### Normed vector space

↑ **Parent:** [Metric space](#metric-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Normed_vector_space)

###### Inner product space

↑ **Parent:** [Normed vector space](#normed-vector-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inner_product_space)

Subcase of a [normed vector space](#normed-vector-space), therefore also necessarily a [vector space](linear-algebra.md#vector-space).

###### Inner product

↑ **Parent:** [Inner product space](#inner-product-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inner_product)

Appears to be analogous to the [dot product](linear-algebra.md#dot-product), but also defined for [infinite dimensions](#infinite-dimensional).

##### Norm (mathematics)

↑ **Parent:** [Metric space](#metric-space)

Vs [metric](#metric-mathematics):
- a norm is the size of one element. A [metric](#metric-mathematics) is the distance between two elements.
- a norm is only defined on a [vector space](linear-algebra.md#vector-space). A [metric](#metric-mathematics) could be defined on something that is not a vector space. Most basic examples however are also [vector spaces](linear-algebra.md#vector-space).

###### Norm induced by an inner product

↑ **Parent:** [Norm (mathematics)](#norm-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Norm_induced_by_an_inner_product)

An [inner product](#inner-product) $x \cdot y$ induces a [norm](#norm-mathematics) with:

$$
|x| = \sqrt{<x, x>}
$$

###### Metric induced by a norm

↑ **Parent:** [Norm (mathematics)](#norm-mathematics)

In a [vector space](linear-algebra.md#vector-space), a [metric](#metric-mathematics) may be induced from a norm by using [subtraction](formalization-of-mathematics.md#subtraction):

$$
d(x, y) = |x - y|
$$

##### Pseudometric space

↑ **Parent:** [Metric space](#metric-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pseudometric_space)

[Metric space](#metric-space) but where the distance between two distinct points can be zero.

Notable example: [Minkowski space](relativity.md#minkowski-space).

### Compact space

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Compact_space)

### Dense set

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dense_set)

### Connected space

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Connected_space)

#### Connected component

↑ **Parent:** [Connected space](#connected-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Connected_component)

When a [disconnected space](#connected-space) is made up of several smaller [connected spaces](#connected-space), then each smaller component is called a "connected component" of the larger space.

See for example the

#### Simply connected space

↑ **Parent:** [Connected space](#connected-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Simply_connected_space)

##### Loop (topology)

↑ **Parent:** [Simply connected space](#simply-connected-space)

### Homotopy

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Homotopy)

<h4 id="generalized-poincare-conjecture">Generalized Poincaré conjecture</h4>

↑ **Parent:** [Homotopy](#homotopy)  
🏷️ **Tags:** [Classification (mathematics)](mathematics.md#classification-mathematics)

There are two cases:
- (topological) manifolds
- differential manifolds

Questions: are all compact manifolds / differential manifolds homotopic / diffeomorphic to the sphere in that dimension?
- for topological manifolds: this is a generalization of the [Poincaré conjecture](#poincare-conjecture).

  Original problem posed, $n = 3$ for topological manifolds.

  [Millennium Prize Problems](mathematics.md#millennium-prize-problems).

  Last to be proven, only the 4-differential manifold case missing as of 2013.

  Even the truth for all $n > 4$ was proven in the 60's!

  Why is low dimension harder than high dimension?? Surprise!

  AKA: classification of compact 3-manifolds. The result turned out to be even simpler than compact 2-manifolds: there is only one, and it is equal to the 3-sphere.

  For dimension two, we know there are infinitely many: [classification of closed surfaces](#classification-of-closed-surfaces)
- for differential manifolds:

  Not true in general. First counter example is $n = 7$. Surprise: what is special about the number 7!?

  Counter examples are called [exotic spheres](#exotic-sphere).

  Totally unpredictable count table:

  | Dimension | Smooth types |
  | --- | --- |
  | 1 | 1 |
  | 2 | 1 |
  | 3 | 1 |
  | 4 | ? |
  | 5 | 1 |
  | 6 | 1 |
  | 7 | 28 |
  | 8 | 2 |
  | 9 | 8 |
  | 10 | 6 |
  | 11 | 992 |
  | 12 | 1 |
  | 13 | 3 |
  | 14 | 2 |
  | 15 | 16256 |
  | 16 | 2 |
  | 17 | 16 |
  | 18 | 16 |
  | 19 | 523264 |
  | 20 | 24 |

  $n = 4$ is an open problem, there could even be infinitely many. Again, why are things more complicated in lower dimensions??

##### Exotic sphere

↑ **Parent:** [Generalized Poincaré conjecture](#generalized-poincare-conjecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Exotic_sphere)

<h5 id="poincare-conjecture">Poincaré conjecture</h5>

↑ **Parent:** [Generalized Poincaré conjecture](#generalized-poincare-conjecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Poincaré_conjecture)

##### Classification of closed surfaces

↑ **Parent:** [Generalized Poincaré conjecture](#generalized-poincare-conjecture)  
🏷️ **Tags:** [Classification (mathematics)](mathematics.md#classification-mathematics)

- [https://en.wikipedia.org/wiki/Surface_(topology)#Classification_of_closed_surfaces](https://en.wikipedia.org/wiki/Surface_(topology)#Classification_of_closed_surfaces)
- [http://www.proofwiki.org/wiki/Classification_of_Compact_Two-Manifolds](http://www.proofwiki.org/wiki/Classification_of_Compact_Two-Manifolds)

So simple!! You can either:
- cut two holes and glue a handle. This is easy to visualize as it can be embedded in [$\R^3$](#real-coordinate-space-of-dimension-three): you just get a [Torus](#torus), then a double torus, and so on
- cut a single hole and glue a [Möbius strip](#mobius-strip) in it. Keep in mind that this is possible because the [Möbius strip](#mobius-strip) has a single boundary just like the hole you just cut. This leads to another infinite family that starts with:
  - 1: [real projective plane](geometry.md#real-projective-plane)
  - 2: [Klein bottle](#klein-bottle)

A handle cancels out a [Möbius strip](#mobius-strip), so adding one of each does not lead to a new object.

You can glue a Mobius strip into a single hole in dimension larger than 3! And it gives you a Klein bottle!

Intuitively speaking, they can be sees as the smooth surfaces in N-dimensional space (called an embedding), such that deforming them is allowed. 4-dimensions is enough to embed cover all the cases: 3 is not enough because of the Klein bottle and family.

###### Torus

↑ **Parent:** [Classification of closed surfaces](#classification-of-closed-surfaces)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Torus)

<h6 id="mobius-strip">Möbius strip</h6>

↑ **Parent:** [Classification of closed surfaces](#classification-of-closed-surfaces)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Möbius_strip)

###### Klein bottle

↑ **Parent:** [Classification of closed surfaces](#classification-of-closed-surfaces)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Klein_bottle)

[sphere](geometry.md#sphere) with two [Möbius strips](#mobius-strip) stuck into it as per the [classification of closed surfaces](#classification-of-closed-surfaces).

### Real coordinate space

↑ **Parent:** [Topology](#topology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Real_coordinate_space)

#### Real line

↑ **Parent:** [Real coordinate space](#real-coordinate-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Real_line)

#### Real plane

↑ **Parent:** [Real coordinate space](#real-coordinate-space)

#### Real coordinate space of dimension three

↑ **Parent:** [Real coordinate space](#real-coordinate-space)

#### Real coordinate space of dimension four

↑ **Parent:** [Real coordinate space](#real-coordinate-space)

Important 4D spaces:
- [3-sphere](geometry.md#3-sphere)

##### Visualizing 4D

↑ **Parent:** [Real coordinate space of dimension four](#real-coordinate-space-of-dimension-four)

Simulate it. Just simulate it.

<a id="video-4d-toys-a-box-of-four-dimensional-toys-by-miegakure-2017"></a>
**[Video 5](#video-4d-toys-a-box-of-four-dimensional-toys-by-miegakure-2017). 4D Toys: a box of four-dimensional toys by Miegakure (2017)** [Source](http://youtube.com/watch?v=0t4aKJuKP0Q).

#### Dimension

↑ **Parent:** [Real coordinate space](#real-coordinate-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dimension)

##### Infinite dimensional

↑ **Parent:** [Dimension](#dimension)

[https://math.stackexchange.com/questions/466707/what-are-some-examples-of-infinite-dimensional-vector-spaces](https://math.stackexchange.com/questions/466707/what-are-some-examples-of-infinite-dimensional-vector-spaces)

###### Finite dimensional

↑ **Parent:** [Infinite dimensional](#infinite-dimensional)

#### Complex coordinate space

↑ **Parent:** [Real coordinate space](#real-coordinate-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Complex_coordinate_space)

##### Complex coordinate space of dimension 2

↑ **Parent:** [Complex coordinate space](#complex-coordinate-space)

##### Complex dot product

↑ **Parent:** [Complex coordinate space](#complex-coordinate-space)

This section is about the definition of the [dot product](linear-algebra.md#dot-product) over [$\C^n$](#complex-coordinate-space), which extends the definition of the [dot product](linear-algebra.md#dot-product) over [$\R^n$](#real-coordinate-space).

Some motivation is discussed at: [https://math.stackexchange.com/questions/2459814/what-is-the-dot-product-of-complex-vectors/4300169#4300169](https://math.stackexchange.com/questions/2459814/what-is-the-dot-product-of-complex-vectors/4300169#4300169)

The complex dot product is defined as:

$$
\sum a_i \overline{b_i}
$$

E.g. in $\C^1$:

$$
(a + bi) \cdot (c + di) = (a + bi) (\overline{c + di}) = (a + bi) (c - di) = (ac + bd) + (bc - ad)i
$$

We can see therefore that this is a [form](linear-algebra.md#form-mathematics), and a positive definite because:

$$
(a + bi) \cdot (a + bi) = (aa + bb) + (ba - ab)i = a^2 + b^2
$$

Just like the usual [dot product](linear-algebra.md#dot-product), this will be a [positive definite symmetric bilinear form](linear-algebra.md#positive-definite-symmetric-bilinear-form) by definition.

###### Norm induced by the complex dot product

↑ **Parent:** [Complex dot product](#complex-dot-product)  
🏷️ **Tags:** [Norm induced by an inner product](#norm-induced-by-an-inner-product)

Given:

$$
x = \sum_{k=1}^n a_k + b_k i \in \C^n, a_k, b_k \in \R
$$

the norm ends up being:

$$
|x| = \sqrt{\sum_{k=1}^n a_k^2 + b_k^2}
$$

E.g. in [$\C^2$](#complex-coordinate-space-of-dimension-2):

$$
|(2 + 3i, -1 + 5i)| = \sqrt{2^2 + 3^2 + (-1)^2 + 5^2} = \sqrt{4 + 9 + 1 + 25} = \sqrt{39}
$$

#### Euclidean space

↑ **Parent:** [Real coordinate space](#real-coordinate-space)  
🏷️ **Tags:** [Metric space](#metric-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Euclidean_space)

[$\R^n$](#real-coordinate-space) with extra structure added to make it into a [metric space](#metric-space).

##### Euclidean metric signature matrix

↑ **Parent:** [Euclidean space](#euclidean-space)

The [identity matrix](linear-algebra.md#identity-matrix).

##### Cartesian coordinate system

↑ **Parent:** [Euclidean space](#euclidean-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cartesian_coordinate_system)

##### Polar coordinate system

↑ **Parent:** [Euclidean space](#euclidean-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polar_coordinate_system)

###### Spherical coordinate system

↑ **Parent:** [Polar coordinate system](#polar-coordinate-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Spherical_coordinate_system)

##### Pythagorean theorem

↑ **Parent:** [Euclidean space](#euclidean-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pythagorean_theorem)

##### Non-Euclidean geometry

↑ **Parent:** [Euclidean space](#euclidean-space)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Non-Euclidean_geometry)

###### Elliptic geometry

↑ **Parent:** [Non-Euclidean geometry](#non-euclidean-geometry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Elliptic_geometry)

###### Model of elliptic geometry

↑ **Parent:** [Elliptic geometry](#elliptic-geometry)

###### Projective elliptic geometry

↑ **Parent:** [Model of elliptic geometry](#model-of-elliptic-geometry)

Each elliptic space can be modelled with a [real projective space](geometry.md#real-projective-space). The best thing is to just start thinking about the [real projective plane](geometry.md#real-projective-plane).

###### Hyperbolic gemoetry

↑ **Parent:** [Non-Euclidean geometry](#non-euclidean-geometry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hyperbolic_gemoetry)

###### Hyperbolic functions

↑ **Parent:** [Hyperbolic gemoetry](#hyperbolic-gemoetry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hyperbolic_functions)

###### Hyperbolic sine

↑ **Parent:** [Hyperbolic functions](#hyperbolic-functions)

###### Hyperbolic cossine

↑ **Parent:** [Hyperbolic functions](#hyperbolic-functions)

## Distribution (mathematics)

↑ **Parent:** [Calculus](calculus.md)

Generalize [function](formalization-of-mathematics.md#function-mathematics) to allow adding some useful things which people wanted to be classical functions but which are not,

It therefore requires you to redefine and reprove all of calculus.

For this reason, most people are tempted to assume that all the hand wavy intuitive arguments [undergrad](university.md#undergraduate-education) teachers give are true and just move on with life. And they generally are.

One notable example where distributions pop up are the [eigenvectors](linear-algebra.md#eigenvector) of the [position operator](quantum-mechanics.md#position-operator) in [quantum mechanics](quantum-mechanics.md), which are given by [Dirac delta functions](#dirac-delta-function), which is most commonly rigorously defined in terms of [distribution](#distribution-mathematics).

Distributions are also defined in a way that allows you to do calculus on them. Notably, you can define a [derivative](#derivative), and the derivative of the [Heaviside step function](#heaviside-step-function) is the [Dirac delta function](#dirac-delta-function).

### Dirac delta function

↑ **Parent:** [Distribution (mathematics)](#distribution-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dirac_delta_function)

The "0-width" pulse [distribution](#distribution-mathematics) that integrates to a step.

There's not way to describe it as a classical [function](formalization-of-mathematics.md#function-mathematics), making it the most important example of a [distribution](#distribution-mathematics).

Applications:
- [position operator](quantum-mechanics.md#position-operator) in [quantum mechanics](quantum-mechanics.md). It's not a coincidence that the function is named after [Paul Dirac](physicist.md#paul-dirac).

<h4 id="green-s-function">Green's function</h4>

↑ **Parent:** [Dirac delta function](#dirac-delta-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Green's_function)

#### Heaviside step function

↑ **Parent:** [Dirac delta function](#dirac-delta-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Heaviside_step_function)

### Normal distribution

↑ **Parent:** [Distribution (mathematics)](#distribution-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Normal_distribution)

## Complex analysis

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Complex_analysis)

The surprising thing is that a bunch of results are simpler in complex analysis!

### Complex analysis bibliography

↑ **Parent:** [Complex analysis](#complex-analysis)

#### Complex Analysis by Juan Carlos Ponce Campuzano

↑ **Parent:** [Complex analysis bibliography](#complex-analysis-bibliography)  
🏷️ **Tags:** [CC BY-NC-SA](law.md#cc-by-nc-sa), [Visual math HTML book](mathematics.md#visual-math-html-book)

[https://complex-analysis.com](https://complex-analysis.com)

### Holomorphic function

↑ **Parent:** [Complex analysis](#complex-analysis)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Holomorphic_function)

Being a complex holomorphic function is an extremely strong condition.

The existence of the first derivative implies the existence of all derivatives.

Another extremely strong consequence is the [identity theorem](#identity-theorem).

"Holos" means "entire" in Greek, so maybe this is a reference to the fact that due to the identity theorem, knowing the function on a small open ball implies knowing the function everywhere.

### Analytic continuation

↑ **Parent:** [Complex analysis](#complex-analysis)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Analytic_continuation)

[visualizing the Riemann hypothesis and analytic continuation by 3Blue1Brown (2016)](#visualizing-the-riemann-hypothesis-and-analytic-continuation-by-3blue1brown-2016) is a good quick visual non-mathematical introduction is to it.

The key question is: how can this continuation be unique since we are defining the function outside of its original domain?

The answer is: due to the [identity theorem](#identity-theorem).

#### Visualizing the Riemann hypothesis and analytic continuation by 3Blue1Brown (2016)

↑ **Parent:** [Analytic continuation](#analytic-continuation)

Good ultra quick visual non-mathematical introduction to the Riemann hypothesis and analytic continuation.

**[Video 6](#_395)** [Source](http://youtube.com/watch?v=sD0NjbwqlYw).

#### Identity theorem

↑ **Parent:** [Analytic continuation](#analytic-continuation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Identity_theorem)

Essentially, defining an [holomorphic function](#holomorphic-function) on any open subset, no matter how small, also uniquely defines it everywhere.

This is basically why it makes sense to talk about [analytic continuation](#analytic-continuation) at all.

One way to think about this is because the [Taylor series](#taylor-series) matches the exact value of an holomorphic function no matter how large the difference from the starting point.

Therefore a holomorphic function basically only contains as much information as a countable sequence of numbers.

##### Riemann zeta function

↑ **Parent:** [Identity theorem](#identity-theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Riemann_zeta_function)

###### Riemann hypothesis

↑ **Parent:** [Riemann zeta function](#riemann-zeta-function)  
🏷️ **Tags:** [Hilbert's problems](mathematics.md#hilbert-s-problems), [Millennium Prize Problems](mathematics.md#millennium-prize-problems)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Riemann_hypothesis)

[visualizing the Riemann hypothesis and analytic continuation by 3Blue1Brown (2016)](#visualizing-the-riemann-hypothesis-and-analytic-continuation-by-3blue1brown-2016) is a good quick visual non-mathematical introduction is to it.

One of the [Millennium Prize Problems](mathematics.md#millennium-prize-problems) and [Hilbert's problems](mathematics.md#hilbert-s-problems).

<a id="video-what-is-the-riemann-hypothesis-really-about-by-hexagonvideos-2022"></a>
**[Video 7](#video-what-is-the-riemann-hypothesis-really-about-by-hexagonvideos-2022). What is the Riemann hypothesis REALLY about? by HexagonVideos (2022)** [Source](https://www.youtube.com/watch?v=e4kOh7qlsM4).

## Hilbert space

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hilbert_space)

Key for [quantum mechanics](quantum-mechanics.md), see: [mathematical formulation of quantum mechanics](quantum-mechanics.md#mathematical-formulation-of-quantum-mechanics), the most important example by far being [$\LTwo$](#l2).

### Complete basis

↑ **Parent:** [Hilbert space](#hilbert-space)

Finding a complete basis such that each vector solves a given [differential equation](#differential-equation) is the basic method of solving [partial differential equation](#partial-differential-equation) through [separation of variables](#separation-of-variables).

The first example of this you must see is [solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series).

Notable examples:
- [Fourier series](#fourier-series) for the [heat equation](#heat-equation) as shown at [Fourier basis is complete for $\LTwo$](#fourier-basis-is-complete-for-l2) and [solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series)
- [Hermite functions](quantum-mechanics.md#hermite-functions) for the [quantum harmonic oscillator](quantum-mechanics.md#quantum-harmonic-oscillator)
- [Legendre polynomials](#legendre-polynomials) for [Laplace's equation](#laplace-s-equation) in [spherical coordinates](#spherical-coordinate-system)
- [Bessel function](#bessel-function) for the [2D wave equation on a circular domain](#2d-wave-equation-on-a-circular-domain) in [polar coordinates](#polar-coordinate-system)

## Differential equation

↑ **Parent:** [Calculus](calculus.md)  
🏷️ **Tags:** [Functional equation](mathematics.md#functional-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Differential_equation)

### Euler number

↑ **Parent:** [Differential equation](#differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Euler_number)

#### Natural logarithm

↑ **Parent:** [Euler number](#euler-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Natural_logarithm)

##### Logarithmic integral function

↑ **Parent:** [Natural logarithm](#natural-logarithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Logarithmic_integral_function)

Sample software implementations:
- [SymPy](software.md#sympy): [python/sympy\_cheat/logarithm\_integral.py](software.md#_file/python/sympy_cheat/logarithm_integral.py)

##### Euler-Mascheroni constant

↑ **Parent:** [Natural logarithm](#natural-logarithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Euler–Mascheroni constant)

[Convergence](#convergent-series): [https://math.stackexchange.com/questions/629630/simple-proof-euler-mascheroni-gamma-constant](https://math.stackexchange.com/questions/629630/simple-proof-euler-mascheroni-gamma-constant)

### Linear differential equation

↑ **Parent:** [Differential equation](#differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_differential_equation)

The name is a bit obscure if you don't think in very generalized terms right out of the gate. It refers to a [linear polynomial](formalization-of-mathematics.md#linear-polynomial) of [multiple variables](formalization-of-mathematics.md#multivariate-polynomial), which by definition must have the super simple form of:

$$
f(x_0, x_1, ..., x_n) = c_0x_0 + c_1x_1 + ... + c_nx_n + k
$$

and then we just put the unknown $y$ and each derivative into that simple polynomial:

$$
f(y(x), y'(x), ..., y^{(n)}(x)) = c_0y + c_1y' + ... + c_ny^{(n)} + k
$$

except that now the $c_i$ are not just constants, but they can also depend on the argument $x$ (but not on $y$ or its derivatives).

Explicit solutions exist for the very specific cases of:
- constant coefficients, any degree. These were known for a long time, and are were studied when [Ciro was at university](ciro-santilli.md#ciro-santilli-s-formal-education) in the [University of São Paulo](university.md#university-of-sao-paulo).
- degree 1 and any coefficient

#### Holonomic function

↑ **Parent:** [Linear differential equation](#linear-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Holonomic_function)

### Order of a differential equation

↑ **Parent:** [Differential equation](#differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Order_of_a_differential_equation)

Order of the highest derivative that appears.

### Ordinary differential equation

↑ **Parent:** [Differential equation](#differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ordinary_differential_equation)

#### Existence and uniqueness of solutions of ordinary differential equations

↑ **Parent:** [Ordinary differential equation](#ordinary-differential-equation)  
🏷️ **Tags:** [Existence and uniqueness](formalization-of-mathematics.md#existence-and-uniqueness)

##### Peano existence theorem

↑ **Parent:** [Existence and uniqueness of solutions of ordinary differential equations](#existence-and-uniqueness-of-solutions-of-ordinary-differential-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Peano_existence_theorem)

<h5 id="picard-lindelof-theorem">Picard-Lindelöf theorem</h5>

↑ **Parent:** [Existence and uniqueness of solutions of ordinary differential equations](#existence-and-uniqueness-of-solutions-of-ordinary-differential-equations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Picard–Lindelöf theorem)

#### System of ordinary differential equations

↑ **Parent:** [Ordinary differential equation](#ordinary-differential-equation)

##### System of linear ordinary differential equations

↑ **Parent:** [System of ordinary differential equations](#system-of-ordinary-differential-equations)

### Partial differential equation

↑ **Parent:** [Differential equation](#differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Partial_differential_equation)

#### Analytical method to solve a partial differential equation

↑ **Parent:** [Partial differential equation](#partial-differential-equation)

##### Separation of variables

↑ **Parent:** [Analytical method to solve a partial differential equation](#analytical-method-to-solve-a-partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Separation_of_variables)

Technique to solve [partial differential equations](#partial-differential-equation)

Naturally leads to the [Fourier series](#fourier-series), see: [solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series), and to other analogous expansions:

One notable application is the solution of the [Schrödinger equation](quantum-mechanics.md#schrodinger-equation) via the [time-independent Schrödinger equation](quantum-mechanics.md#time-independent-schrodinger-equation).

Bibliography:
- [https://math.libretexts.org/Bookshelves/Differential_Equations/Book%3A_Differential_Equations_for_Engineers_(Lebl)/4%3A_Fourier_series_and_PDEs/4.06%3A_PDEs_separation_of_variables_and_the_heat_equation](https://math.libretexts.org/Bookshelves/Differential_Equations/Book%3A_Differential_Equations_for_Engineers_(Lebl)/4%3A_Fourier_series_and_PDEs/4.06%3A_PDEs_separation_of_variables_and_the_heat_equation) on [LibreTexts](social-technology.md#libretexts) for the [heat equation](#heat-equation)

#### Numerical method to solve a partial differential equation

↑ **Parent:** [Partial differential equation](#partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Numerical_methods_for_partial_differential_equations)

The [finite element method](#finite-element-method) is one of the most common ways to solve PDEs in practice.

##### Variational formulation of a partial differential equation

↑ **Parent:** [Numerical method to solve a partial differential equation](#numerical-method-to-solve-a-partial-differential-equation)

[https://www.cis.upenn.edu/~cis515/cis515-12-sl11.pdf](https://www.cis.upenn.edu/~cis515/cis515-12-sl11.pdf)

Used for example in [FreeFem](#freefem) and [FEniCS Project](#fenics-project) as the input description of the PDEs, TODO why.

###### Weak solution

↑ **Parent:** [Variational formulation of a partial differential equation](#variational-formulation-of-a-partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Weak_solution)

##### Finite element method

↑ **Parent:** [Numerical method to solve a partial differential equation](#numerical-method-to-solve-a-partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Finite_element_method)

Used to solve [partial differential equation](#partial-differential-equation).

TODO understand, give intuition, justification of bounds and [JavaScript](programming-language.md#javascript) demo.

#### Important partial differential equation

↑ **Parent:** [Partial differential equation](#partial-differential-equation)

The majority likely comes from [physics](physics.md):
- [heat equation](#heat-equation)
- [wave equation](#wave-equation)
- [Maxwell's equations](electromagnetism.md#maxwell-s-equations)
- [Schrödinger equation](quantum-mechanics.md#schrodinger-equation)
- [Navier-Stokes equations](mechanics.md#navier-stokes-equations)

<h5 id="laplace-s-equation">Laplace's equation</h5>

↑ **Parent:** [Important partial differential equation](#important-partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Laplace's_equation)

Like a [heat equation](#heat-equation) but for functions without time dependence, space-only.

TODO confirm: does the solution of the heat equation always converge to the solution of the Laplace equation as time tends to infinity?

In one dimension, the Laplace equation is boring as it is just a straight line since the second derivative must be 0. That also matches our intuition of the limit solution of the heat equation.

Uniqueness: [Uniqueness theorem for Poisson's equation](#uniqueness-theorem-for-poisson-s-equation).

###### Legendre polynomials

↑ **Parent:** [Laplace's equation](#laplace-s-equation)  
🏷️ **Tags:** [Complete basis](#complete-basis)

Show up when solving the [Laplace's equation](#laplace-s-equation) on [spherical coordinates](#spherical-coordinate-system) by [separation of variables](#separation-of-variables), which leads to the [differential equation](#differential-equation) shown at: [https://en.wikipedia.org/w/index.php?title=Legendre_polynomials&oldid=1018881414#Definition_via_differential_equation](https://en.wikipedia.org/w/index.php?title=Legendre_polynomials&oldid=1018881414#Definition_via_differential_equation).

<h6 id="poisson-s-equation">Poisson's equation</h6>

↑ **Parent:** [Laplace's equation](#laplace-s-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Poisson's_equation)

Generalization of [Laplace's equation](#laplace-s-equation) where the value is not necessarily 0.

<h6 id="uniqueness-theorem-for-poisson-s-equation">Uniqueness theorem for Poisson's equation</h6>

↑ **Parent:** [Poisson's equation](#poisson-s-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Uniqueness_theorem_for_Poisson's_equation)

###### Harmonic function

↑ **Parent:** [Laplace's equation](#laplace-s-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Harmonic_function)

A solution to [Laplace's equation](#laplace-s-equation).

###### Spherical harmonic

↑ **Parent:** [Harmonic function](#harmonic-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Spherical_harmonics)

Correspond to the angular part of [Laplace's equation](#laplace-s-equation) in spherical coordinates after using [separation of variables](#separation-of-variables) as shown at: [https://en.wikipedia.org/wiki/Spherical_harmonics#Laplace's_spherical_harmonics](https://en.wikipedia.org/wiki/Spherical_harmonics#Laplace's_spherical_harmonics)

##### Heat equation

↑ **Parent:** [Important partial differential equation](#important-partial-differential-equation)  
🏷️ **Tags:** [Important partial differential equation](#important-partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Heat_equation)

Besides being useful in engineering, it was very important historically from a "development of mathematics point of view", e.g. [it was the initial motivation for the Fourier series](#history-of-the-fourier-series).

Some interesting properties:
- TODO confirm: for a fixed boundary condition that does not depend on time, the solutions always approaches one specific equilibrium function.

  This is in contrast notably with the [wave equation](#wave-equation), which can oscillate forever.
- TODO: for a given point, can the temperature go down and then up, or is it always monotonic with time?
- information propagates instantly to infinitely far. Again in contrast to the wave equation, where information propagates at wave speed.

Sample numerical solutions:
- with [FreeFem](#freefem):
  - [heat-dirichlet.1d.freefem](#heat-dirichlet-1d-freefem)
  - [heat-dirichlet-2d-freefem](#heat-dirichlet-2d-freefem)

###### Heat equation solution with Fourier series

↑ **Parent:** [Heat equation](#heat-equation)  
🏷️ **Tags:** [Solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series)

See: [https://math.stackexchange.com/questions/579453/real-world-application-of-fourier-series/3729366#3729366](https://math.stackexchange.com/questions/579453/real-world-application-of-fourier-series/3729366#3729366)

##### Wave equation

↑ **Parent:** [Important partial differential equation](#important-partial-differential-equation)  
🏷️ **Tags:** [Important partial differential equation](#important-partial-differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wave_equation)

Describes perfect lossless waves on the surface of a string, or on a water surface.

Uniqueness: [https://math.stackexchange.com/questions/1113622/uniqueness-of-solutions-to-the-wave-equation](https://math.stackexchange.com/questions/1113622/uniqueness-of-solutions-to-the-wave-equation)

As mentioned at: [https://math.stackexchange.com/questions/579453/real-world-application-of-fourier-series/3729366#3729366](https://math.stackexchange.com/questions/579453/real-world-application-of-fourier-series/3729366#3729366) from [solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series) citing [https://courses.maths.ox.ac.uk/node/view_material/1720](https://courses.maths.ox.ac.uk/node/view_material/1720), analogously to the [heat equation](#heat-equation), the wave linear equation can be be solved nicely with [separation of variables](#separation-of-variables).

###### Damped wave equation

↑ **Parent:** [Wave equation](#wave-equation)

###### Plucked string model

↑ **Parent:** [Damped wave equation](#damped-wave-equation)

Staring from a [triangle wave](https://ourbigbook.com/go/topic/triangle-wave), this explains why we always get the same musical notes:
- [https://www.math.hmc.edu/~ajb/PCMI/lecture7.pdf](https://www.math.hmc.edu/~ajb/PCMI/lecture7.pdf) "7.5.1. Musical instruments" is very good. Also mentions that in the [piano](music.md#piano) it is more like an initial speed is applied, and it is not the same as plucking
- [https://music.stackexchange.com/questions/135635/confusion-about-overtones-and-a-slow-motion-video-of-a-plucked-string](https://music.stackexchange.com/questions/135635/confusion-about-overtones-and-a-slow-motion-video-of-a-plucked-string)
- [https://music.stackexchange.com/questions/60833/what-determines-the-relative-volumes-of-the-harmonics-when-plucking-a-guitar-str](https://music.stackexchange.com/questions/60833/what-determines-the-relative-volumes-of-the-harmonics-when-plucking-a-guitar-str)
See also: [solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series).

TODO: do higher overtones decay faster in time than the base ones?
- [https://www.physicsforums.com/threads/why-do-harmonics-decay-faster-than-the-fundamental.955731/](https://www.physicsforums.com/threads/why-do-harmonics-decay-faster-than-the-fundamental.955731/) But presumaby yes, damping force is proportional to speed, and higher harmonics have higher speeds going up and down

<a id="video-motion-of-plucked-string-by-dan-russell"></a>
**[Video 8](#video-motion-of-plucked-string-by-dan-russell). Motion of Plucked String by Dan Russell.** [Source](https://www.youtube.com/watch?v=_X72on6CSL0).

<a id="video-slow-motion-rubber-string-pulled-and-released-by-pavel-radzivilovsky"></a>
**[Video 9](#video-slow-motion-rubber-string-pulled-and-released-by-pavel-radzivilovsky). Slow motion: rubber string pulled and released by Pavel Radzivilovsky.** [Source](https://www.youtube.com/watch?v=Qr_rxqwc1jE). Good symmetric example. But unfortunately the video is too short.

Featured at: [https://www.reddit.com/r/Physics/comments/kyocxr/what_happens_when_a_plucked_string_is_released/](https://www.reddit.com/r/Physics/comments/kyocxr/what_happens_when_a_plucked_string_is_released/)

---

###### Wave equation boundary condition

↑ **Parent:** [Wave equation](#wave-equation)

###### Wave equation on string with one vibrating side

↑ **Parent:** [Wave equation](#wave-equation)

<a id="video-modes-on-a-string-by-geoff-martin"></a>
**[Video 10](#video-modes-on-a-string-by-geoff-martin). Modes on a String by geoff martin.** [Source](https://www.youtube.com/watch?v=cnH2ltfW48U).

###### Wave equation solver

↑ **Parent:** [Wave equation](#wave-equation)

This section talks about solvers/simulators dedicated solving the [wave equation](#wave-equation). Of course, any serious solver will likely be able to solve a wider range of PDE, so this section contains mostly fun toys. For more serious stuff see: [Section "PDE solver"](#partial-differential-equation-solver).

[JavaScript](programming-language.md#javascript) toy solvers:
- [https://jtiscione.github.io/webassembly-wave/index.html](https://jtiscione.github.io/webassembly-wave/index.html) circular domain, create waves with mouse click
- [https://dionyziz.com/graphics/wave-experiment/](https://dionyziz.com/graphics/wave-experiment/) with useless 3D [WebGL](web-technology.md#webgl) visualization :-), waves with mouse click. Solving itself done on [CPU](computer-hardware.md#central-processing-unit), not GPU.

Related:
- [https://stackoverflow.com/questions/69949335/how-to-simulate-a-wave-equation](https://stackoverflow.com/questions/69949335/how-to-simulate-a-wave-equation)

###### Wave equation solution with Fourier series

↑ **Parent:** [Wave equation](#wave-equation)  
🏷️ **Tags:** [Solving partial differential equations with the Fourier series](#solving-partial-differential-equations-with-the-fourier-series)

[https://web.archive.org/web/20200621205928/https://courses.maths.ox.ac.uk/node/view_material/1720](https://web.archive.org/web/20200621205928/https://courses.maths.ox.ac.uk/node/view_material/1720) also mentioned at [https://math.stackexchange.com/questions/579453/real-world-application-of-fourier-series/3729366#3729366](https://math.stackexchange.com/questions/579453/real-world-application-of-fourier-series/3729366#3729366) from [heat equation solution with Fourier series](#heat-equation-solution-with-fourier-series).

###### The wave equation can be seen as infinitely many infinitesimal coupled oscillators

↑ **Parent:** [Wave equation](#wave-equation)

TODO confirm, see also: [coupled oscillators](mechanics.md#coupled-oscillators). And then this idea can be used to define/motivate [quantum field theory](quantum-field-theory.md) in terms of [quantum harmonic oscillators](quantum-mechanics.md#quantum-harmonic-oscillator) with [second quantization](quantum-field-theory.md#second-quantization).

- [https://youtu.be/SMmFgIEGYtw?t=324](https://youtu.be/SMmFgIEGYtw?t=324) Quantum Field Theory 2a - Field Quantization I by [ViaScience](particle-physics.md#viascience) (2018)

###### Lossy 1D Wave Equation

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lossy_1D_Wave_Equation)

[https://ccrma.stanford.edu/~jos/pasp/Lossy_1D_Wave_Equation.html](https://ccrma.stanford.edu/~jos/pasp/Lossy_1D_Wave_Equation.html)

###### Wave

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wave)

###### Wavelength

↑ **Parent:** [Wave](#wave)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wavelength)

###### Standing wave

↑ **Parent:** [Wave](#wave)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Standing_wave)

<a id="image-standing-wave-caused-by-wave-interference-of-two-waves"></a>
![](https://upload.wikimedia.org/wikipedia/commons/5/5d/Waventerference.gif)

**[Figure 5](#image-standing-wave-caused-by-wave-interference-of-two-waves). Standing wave caused by wave interference of two waves**. [Source](https://commons.wikimedia.org/wiki/File:Waventerference.gif).

###### Envelope (waves)

↑ **Parent:** [Wave](#wave)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Envelope_(waves))

###### Polarization

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polarization_(waves))

Start with: [Section "String polarization"](#string-polarization).

Then go to: [Section "Polarization of light"](photon.md#polarization-of-light).

###### String polarization

↑ **Parent:** [Polarization](#polarization)

This is about the polarization of a string in 3D space. That is the first concept of polarization you must have in mind!

###### Diffraction

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Diffraction)

###### Huygens-Fresnel principle

↑ **Parent:** [Diffraction](#diffraction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Huygens–Fresnel principle)

<h6 id="kirchhoff-s-diffraction-formula">Kirchhoff's diffraction formula</h6>

↑ **Parent:** [Huygens-Fresnel principle](#huygens-fresnel-principle)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kirchhoff's_diffraction_formula)

Approximation to [Huygens-Fresnel principle](#huygens-fresnel-principle).

###### Fraunhofer diffraction

↑ **Parent:** [Kirchhoff's diffraction formula](#kirchhoff-s-diffraction-formula)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fraunhofer_diffraction)

Far field approximation to [Kirchhoff's diffraction formula](#kirchhoff-s-diffraction-formula), i.e. when the plane of observation is far from the object diffracting.

###### Fresnel diffraction

↑ **Parent:** [Kirchhoff's diffraction formula](#kirchhoff-s-diffraction-formula)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fresnel_diffraction)

Near field approximation to [Kirchhoff's diffraction formula](#kirchhoff-s-diffraction-formula), i.e. when the plane of observation is near the object diffracting.

###### Refraction

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Refraction)

###### Resonance

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Resonance)

Resonance is a really cool thing.

Examples:
- [mechanical resonance](mechanics.md#mechanical-resonance), notably:
  - pipe instruments
- [electronic oscillators](electronics.md#electronic-oscillator), notably:
  - [LC oscillator](electronics.md#lc-oscillator), and notably the lossy version [RLC circuit](electronics.md#rlc-circuit)

Perhaps a key insight of resonance is that the reonant any lossy system tends to look like the resonance frequency quite quickly even if the initial condition is not the resonant condition itself, because everything that is not the resonant frequency interferes destructively and becomes noise. Some examples of that:
- striking a bell or drum can be modelled by applying an impuse to the system
- playing a pipe instrument comes down to blowing a piece that vibrates randomly, and then leads the pipe to vibrate mostly in the resonant frequency. Likely the same applies to bowed string instruments, the bow must be creating a random vibration.
- playing a plucked string instrument comes down to initializing the system to an triangular wave form and then letting it evolve. TODO find a simulation of that!

Another cool aspect of resonance is that it was kind of the motivation for [de Broglie hypothesis](quantum-mechanics.md#matter-wave), as [de Broglie](physicist.md#louis-de-broglie) was kind of thinking that electroncs might show discrete jumps on [atomic spectra](quantum-mechanics.md#emission-spectrum) because of constructive interference.

###### Wave interference

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wave_interference)

###### Interference pattern

↑ **Parent:** [Wave interference](#wave-interference)

What you see along a line or plane in a [wave interference](#wave-interference).

Notably used for the pattern of the [double-slit experiment](quantum-mechanics.md#double-slit-experiment).

###### 2D wave equation on a circular domain

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vibrations_of_a_circular_membrane)

###### Bessel function

↑ **Parent:** [2D wave equation on a circular domain](#2d-wave-equation-on-a-circular-domain)  
🏷️ **Tags:** [Complete basis](#complete-basis)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bessel_function)

Shows up when trying to solve [2D wave equation on a circular domain](#2d-wave-equation-on-a-circular-domain) in [polar coordinates](#polar-coordinate-system) with [separation of variables](#separation-of-variables), where we have to decompose the initial condition in termes of a [fourier-Bessel series](#fourier-bessel-series), exactly like the [Fourier series](#fourier-series) appears when solving the wave equation in linear coordinates.

For the same fundamental reasons, also appears when calculating the [Schrödinger equation solution for the hydrogen atom](quantum-mechanics.md#schrodinger-equation-solution-for-the-hydrogen-atom).

###### Fourier-Bessel series

↑ **Parent:** [Bessel function](#bessel-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fourier–Bessel_series)

Completeness: [https://math.stackexchange.com/questions/2192665/is-this-set-of-bessel-functions-a-basis-for-all-c10-a-functions](https://math.stackexchange.com/questions/2192665/is-this-set-of-bessel-functions-a-basis-for-all-c10-a-functions) TODO

This is the [Bessel function](#bessel-function) analogue to [Fourier basis is complete for $\LTwo$](#fourier-basis-is-complete-for-l2).

###### Helmholtz equation

↑ **Parent:** [Wave equation](#wave-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Helmholtz_equation)

[eigenvalue](linear-algebra.md#eigenvalue) problem of [Laplace's equation](#laplace-s-equation).

#### Existence and uniqueness of solutions of partial differential equations

↑ **Parent:** [Partial differential equation](#partial-differential-equation)  
🏷️ **Tags:** [Existence and uniqueness](formalization-of-mathematics.md#existence-and-uniqueness)

If you have a [PDE](#partial-differential-equation) that models [physical phenomena](physics.md), it is fundamental that:
- there must exist a solution for every physically valid initial condition, otherwise it means that the equation does not describe certain cases of reality
- the solution must be unique, otherwise how are we to choose between the multiple solutions?

Unlike for [ordinary differential equations](#ordinary-differential-equation) which have the [Picard–Lindelöf theorem](https://en.wikipedia.org/wiki/Picard–Lindelöf_theorem), the existence and uniqueness of solution is not well solved for PDEs.

For example, [Navier-Stokes existence and smoothness](mechanics.md#navier-stokes-existence-and-smoothness) was one of the [Millennium Prize Problems](mathematics.md#millennium-prize-problems).

#### Partial differential equation solver

↑ **Parent:** [Partial differential equation](#partial-differential-equation)  
🏷️ **Tags:** [Numerical software](software.md#numerical-software)

##### FreeFem

↑ **Parent:** [Partial differential equation solver](#partial-differential-equation-solver)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/FreeFem++)

[https://freefem.org/](https://freefem.org/)

[https://github.com/FreeFem/FreeFem-sources](https://github.com/FreeFem/FreeFem-sources)

Started in 1987 and written in Pascal, by the French from [Pierre and Marie Curie University](university.md#pierre-and-marie-curie-university), the French are really strong in [numerical analysis](mathematics.md#numerical-analysis).

Ciro wasn't expecting it to be as old. Ported to C++ in 1992.

The fact that French wrote it can be seen in the documentation, for example [https://doc.freefem.org/tutorials/index.html](https://doc.freefem.org/tutorials/index.html) uses file extension `mycode.edp` instead of `mycode.pde` where `dep` stands for "[Équation aux dérivées partielles](https://fr.wikipedia.org/wiki/Équation_aux_dérivées_partielles)".

Besides the painful build, using FreeFem is relatively simple, as can be seen from the examples on the website.

They do use a [domain-specific language](computer.md#domain-specific-language) on the examples, which appears to be the main/only interface, which is a bad thing, Ciro would rather have a [Python](programming-language.md#python-programming-language) [API](software.md#application-programming-interface) as the "main API", which is more the approach taken by the [FEniCS Project](#fenics-project), but so be it. This [domain-specific language](computer.md#domain-specific-language) business means that you always stumble upon basic stuff you want to do but can't, and then you have to think about how to share data between the simulation and the plotting. The plotting notably is super complex and they can't implement all of what people want, upstream examples often offload that to gnuplot. This is potentially a big advantage of [FEniCS Project](#fenics-project).

It nice though that they do have some graphics out of the box, as that allows to quickly debug common problems.

Uses [variational formulation of a partial differential equation](#variational-formulation-of-a-partial-differential-equation), which is not immediately obvious to beginners? The introduction [https://doc.freefem.org/tutorials/poisson.html](https://doc.freefem.org/tutorials/poisson.html) gives an ultra quick example, but your are mostly on your own with that.

On Ubuntu 20.04, the `freefem` is a bit out-of-date (3.5.8, there isn't even a tag for that in the [GitHub](software.md#github) repo, and refs/tags/release\_3\_10 is from 2010!) and fails to run the examples from the website. It did work with the example package though, but the output does not have color, which makes me sad :-)
```
sudo apt install freefem freefem-examples
freefem /usr/share/doc/freefem-examples/heat.pde
```

So let's just compile the latest v4.6 it from source, on Ubuntu 20.04:
```
sudo apt build-dep freefem
git clone https://github.com/FreeFem/FreeFem-sources
cd FreeFem-sources
# Post v4.6 with some fixes.
git checkout 3df0e2370d9752801ac744b11307b14e16743a44

# Won't apply automatically due to tab hell.
# https://superuser.com/questions/607410/how-to-copy-paste-tab-characters-via-the-clipboard-into-terminal-session-on-gnom
git apply <<'EOS'
diff --git a/3rdparty/ff-petsc/Makefile b/3rdparty/ff-petsc/Makefile
index dc62ab06..13cd3253 100644
--- a/3rdparty/ff-petsc/Makefile
+++ b/3rdparty/ff-petsc/Makefile
@@ -204,7 +204,7 @@ $(SRCDIR)/tag-make-real:$(SRCDIR)/tag-conf-real
 $(SRCDIR)/tag-install-real :$(SRCDIR)/tag-make-real
     cd $(SRCDIR) && $(MAKE) PETSC_DIR=$(PETSC_DIR) PETSC_ARCH=fr install
     -test -x "`type -p otool`" && make changer
-    cd $(SRCDIR) && $(MAKE) PETSC_DIR=$(PETSC_DIR) PETSC_ARCH=fr check
+    #cd $(SRCDIR) && $(MAKE) PETSC_DIR=$(PETSC_DIR) PETSC_ARCH=fr check
     test -e $(DIR_INSTALL_REAL)/include/petsc.h
     test -e $(DIR_INSTALL_REAL)/lib/petsc/conf/petscvariables
     touch $@
@@ -293,7 +293,6 @@ $(SRCDIR)/tag-tar:$(PACKAGE)
     -tar xzf $(PACKAGE)
     patch -p1 < petsc-hpddm.patch
 ifeq ($(WIN32DLLTARGET),)
-    patch -p1 < petsc-metis.patch
 endif
     touch $@
 $(PACKAGE):
EOS

autoreconf -i
./configure --enable-download --enable-optim --prefix="$(pwd)/../FreeFem-install"
./3rdparty/getall -a
cd 3rdparty/ff-petsc
make petsc-slepc
cd -
./reconfigure
make -j`nproc`
make install
cd ../FreeFem-install
PATH="${PATH}:$(pwd)/bin" ./bin/FreeFem++ ../FreeFem-sources/examples/tutorial/
```

Ciro's initial build experience was a bit painful, possibly because it was done on a relatively new Ubuntu 20.04 as of June 2020, but in the end it worked: [https://github.com/FreeFem/FreeFem-sources/issues/141](https://github.com/FreeFem/FreeFem-sources/issues/141)

The main/only dependency appears to be [PETSc](https://en.wikipedia.org/wiki/Portable,_Extensible_Toolkit_for_Scientific_Computation) which is used by default, which is a good sign, as that library appears to automatically parallelize a single input to several backends (single [CPU](computer-hardware.md#central-processing-unit), MPI, GPU) so you know things will scale up as you reach simulations.

The problem is that it compiling such a complex dependency opens up much more room for hard to solve compilation errors, and takes a lot more time.

###### FreeFem examples

↑ **Parent:** [FreeFem](#freefem)

<h6 id="heat-dirichlet-1d-freefem">heat-dirichlet.1d.freefem</h6>

↑ **Parent:** [FreeFem examples](#freefem-examples)

1-dimensional [heat equation](#heat-equation) example with [Dirichlet boundary condition](#dirichlet-boundary-condition)
- [freefem/heat-dirichlet.1d.freefem](freefem/heat-dirichlet.1d.freefem)

###### heat-dirichlet-2d-freefem

↑ **Parent:** [FreeFem examples](#freefem-examples)

2-dimensional [heat equation](#heat-equation) example with [Dirichlet boundary condition](#dirichlet-boundary-condition):
- [freefem/heat-dirichlet.2d.freefem](freefem/heat-dirichlet.2d.freefem)

##### FEniCS Project

↑ **Parent:** [Partial differential equation solver](#partial-differential-equation-solver)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/FEniCS_Project)

[https://fenicsproject.org/](https://fenicsproject.org/)

One big advantage over [FreeFem](#freefem) is that it uses plain old [Python](programming-language.md#python-programming-language) to describe the problems instead of a [domain-specific language](computer.md#domain-specific-language). [Matplotlib](software.md#matplotlib) is used for plotting by default, so we get full Python power out of the box!

Also uses [variational formulation of a partial differential equation](#variational-formulation-of-a-partial-differential-equation) like [FreeFem](#freefem) which is a pain.

One downside is that its documentation is a Springer published PDF [https://link.springer.com/content/pdf/10.1007%2F978-3-319-52462-7.pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-52462-7.pdf) which is several years out-of-date (tested with FEnics 2016.2. Newbs. This causes problems e.g.: [https://stackoverflow.com/questions/53730427/fenics-did-not-show-figure-nameerror-name-interactive-is-not-defined/57390687#57390687](https://stackoverflow.com/questions/53730427/fenics-did-not-show-figure-nameerror-name-interactive-is-not-defined/57390687#57390687)

[system of partial differential equations](#system-of-partial-differential-equations) are mentioned at: [https://link.springer.com/content/pdf/10.1007%2F978-3-319-52462-7.pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-52462-7.pdf) 3.5 "A system of advection–diffusion–reaction equations". You don't need to manually iterate between the equations.

On Ubuntu 20.04 as per [https://fenicsproject.org/download/](https://fenicsproject.org/download/)
```
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:fenics-packages/fenics
sudo apt-get update
sudo apt-get install --no-install-recommends fenics
sudo apt install fenics
python3 -m pip install -u matplotlib
```
Before 2020-06, it was failing with:
```
E: The repository 'http://ppa.launchpad.net/fenics-packages/fenics/ubuntu focal Release' does not have a Release file.
```
but they seem to have created the Ubuntu 20.04 package as of 2020-06, so it now worked! [https://askubuntu.com/questions/866901/what-can-i-do-if-a-repository-ppa-does-not-have-a-release-file](https://askubuntu.com/questions/866901/what-can-i-do-if-a-repository-ppa-does-not-have-a-release-file)

TODO heat equation [hello world](software.md#hello-world-program).

###### Hans Petter Langtangen

↑ **Parent:** [FEniCS Project](#fenics-project)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hans_Petter_Langtangen)

[GitHub](software.md#github) account: [https://github.com/hplgit](https://github.com/hplgit)

It should be mentioned that when you start [Googling](google.md) for [PDE](#partial-differential-equation) stuff, you will reach Han's writings a lot under his [GitHub Pages](software.md#github-pages): [http://hplgit.github.io/](http://hplgit.github.io/), and he is one of the main authors of the [FEniCS Project](#fenics-project).

Unfortunately he died of [cancer](biology.md#cancer) in 2016, shame, he seemed like a good educator.

He also published to [GitHub](software.md#github) pages with his own crazy [markdown](computer.md#markdown)-like multi-output [markup language](computer.md#markup-language): [https://github.com/hplgit/doconce](https://github.com/hplgit/doconce).

Rest in peace, Hans.

#### System of partial differential equations

↑ **Parent:** [Partial differential equation](#partial-differential-equation)

In many important applications, what you have to solve is not just a single [partial differential equation](#partial-differential-equation), but multiple partial differential equations coupled to each other. This is the case for many key PDEs including:
- [Maxwell's equations](electromagnetism.md#maxwell-s-equations), see: [Section "Explicit scalar form of the Maxwell's equations"](electromagnetism.md#explicit-scalar-form-of-the-maxwell-s-equations)
- [Navier-Stokes equations](mechanics.md#navier-stokes-equations)
- [Schrödinger equation](quantum-mechanics.md#schrodinger-equation), see: [Section "Why are complex numbers used in the Schrodinger equation?"](quantum-mechanics.md#why-are-complex-numbers-used-in-the-schrodinger-equation)

#### Classification of second order partial differential equations into elliptic, parabolic and hyperbolic

↑ **Parent:** [Partial differential equation](#partial-differential-equation)

One major application of this classification is that different [boundary conditions](#boundary-condition) are suitable for different types of [partial differential equations](#partial-differential-equation) as explained at: [which boundary conditions lead to existence and uniqueness of a second order PDE](#which-boundary-conditions-lead-to-existence-and-uniqueness-of-a-second-order-pde).

Bibliography:
- [https://math.stackexchange.com/questions/1090299/why-are-elliptic-parabolic-hyperbolic-pdes-called-elliptic-parabolic-hyperb](https://math.stackexchange.com/questions/1090299/why-are-elliptic-parabolic-hyperbolic-pdes-called-elliptic-parabolic-hyperb)

##### Elliptic partial differential equation

↑ **Parent:** [Classification of second order partial differential equations into elliptic, parabolic and hyperbolic](#classification-of-second-order-partial-differential-equations-into-elliptic-parabolic-and-hyperbolic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Elliptic_partial_differential_equation)

##### Parabolic partial differential equation

↑ **Parent:** [Classification of second order partial differential equations into elliptic, parabolic and hyperbolic](#classification-of-second-order-partial-differential-equations-into-elliptic-parabolic-and-hyperbolic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Parabolic_partial_differential_equation)

##### Hyperbolic partial differential equation

↑ **Parent:** [Classification of second order partial differential equations into elliptic, parabolic and hyperbolic](#classification-of-second-order-partial-differential-equations-into-elliptic-parabolic-and-hyperbolic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hyperbolic_partial_differential_equation)

##### Which boundary conditions lead to existence and uniqueness of a second order PDE

↑ **Parent:** [Classification of second order partial differential equations into elliptic, parabolic and hyperbolic](#classification-of-second-order-partial-differential-equations-into-elliptic-parabolic-and-hyperbolic)

[http://www.cns.gatech.edu/~predrag/courses/PHYS-6124-12/StGoChap6.pdf](http://www.cns.gatech.edu/~predrag/courses/PHYS-6124-12/StGoChap6.pdf) 6.1 "Classification of PDE's" clarifies which boundary conditions are needed for existence and uniqueness of each [type of second order of PDE](#classification-of-second-order-partial-differential-equations-into-elliptic-parabolic-and-hyperbolic):
- [elliptic partial differential equation](#elliptic-partial-differential-equation) and [parabolic partial differential equation](#parabolic-partial-differential-equation): [Dirichlet boundary condition](#dirichlet-boundary-condition) or [Neumann boundary condition](#neumann-boundary-condition)
- [hyperbolic partial differential equation](#hyperbolic-partial-differential-equation): [Cauchy boundary condition](#cauchy-boundary-condition)

### Phase space

↑ **Parent:** [Differential equation](#differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phase_space)

This idea comes up particularly in the [phase space coordinate](mechanics.md#phase-space-coordinate) of [Hamiltonian mechanics](mechanics.md#hamiltonian-mechanics).

### Boundary condition

↑ **Parent:** [Differential equation](#differential-equation)

#### Initial condition

↑ **Parent:** [Boundary condition](#boundary-condition)

Basically a subset of the [boundary condition](#boundary-condition) for when one of the parameters is time and we are specifying values for the time 0.

#### Boundary value problem

↑ **Parent:** [Boundary condition](#boundary-condition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Boundary_value_problem)

#### Dirichlet boundary condition

↑ **Parent:** [Boundary condition](#boundary-condition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dirichlet_boundary_condition)

Specifies fixed values.

Can be used for [elliptic partial differential equations](#elliptic-partial-differential-equation) and [parabolic partial differential equations](#parabolic-partial-differential-equation).

Numerical examples:
- with [FreeFem](#freefem):
  - [heat-dirichlet.1d.freefem](#heat-dirichlet-1d-freefem)
  - [heat-dirichlet-2d-freefem](#heat-dirichlet-2d-freefem)

#### Neumann boundary condition

↑ **Parent:** [Boundary condition](#boundary-condition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Neumann_boundary_condition)

Specifies the derivative in a direction normal to the boundary.

Can be used for [elliptic partial differential equations](#elliptic-partial-differential-equation) and [parabolic partial differential equations](#parabolic-partial-differential-equation).

##### Cauchy boundary condition

↑ **Parent:** [Neumann boundary condition](#neumann-boundary-condition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cauchy_boundary_condition)

Sets both a [Dirichlet boundary condition](#dirichlet-boundary-condition) and a [Neumann boundary condition](#neumann-boundary-condition) for a single part of the boundary.

Can be used for [hyperbolic partial differential equations](#hyperbolic-partial-differential-equation).

We understand intuitively that this imposes stricter requirements on solutions, which makes it easier to guarantee uniqueness, but also harder to have existence. TODO intuitively why hyperbolic need this extra level of restriction.

##### Robin boundary condition

↑ **Parent:** [Neumann boundary condition](#neumann-boundary-condition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Robin_boundary_condition)

Linear combination of a [Dirichlet boundary condition](#dirichlet-boundary-condition) and [Neumann boundary condition](#neumann-boundary-condition) at each point of the boundary.

Examples:
- [heat equation](#heat-equation) when metal plaque is immersed in a large external environment of fixed temperature.

  In this case, the normal derivative at the boundary is proportional to the difference between the temperature of the boundary and the fixed temperature of the external environment.

  The result as time tends to infinity is that the temperature of the plaque tends to that of the environment.

  Shown a solved example in the [FreeFem](#freefem) tutorial: [https://doc.freefem.org/tutorials/thermalConduction.html](https://doc.freefem.org/tutorials/thermalConduction.html) ([https://github.com/FreeFem/FreeFem-doc/blob/1d5996d8b891fd553fd318321249c2c30f693fc3/source/tutorials/thermalConduction.rst)](https://github.com/FreeFem/FreeFem-doc/blob/1d5996d8b891fd553fd318321249c2c30f693fc3/source/tutorials/thermalConduction.rst))

##### Open boundary condition

↑ **Parent:** [Neumann boundary condition](#neumann-boundary-condition)

In the context of wave-like equations, an open-boundary condition is one that "lets the wave go through without reflection".

This condition is very useful when we want to simulate infinite domains with a numerical method. [Ciro Santilli](ciro-santilli.md) wants to do this all the time when trying to come up with demos for his [physics](physics.md) writings.

Here are some resources that cover such boundary conditions:
- [https://www.asc.tuwien.ac.at/~arnold/pdf/graz/graz.pdf](https://www.asc.tuwien.ac.at/~arnold/pdf/graz/graz.pdf) lots of slides
- [http://hplgit.github.io/wavebc/doc/pub/._wavebc_cyborg002.html](http://hplgit.github.io/wavebc/doc/pub/._wavebc_cyborg002.html) mentions them and gives a 1D formula. It mentions that things get complicated in 2D and 3D TODO why.

  The other page: [http://hplgit.github.io/wavebc/doc/pub/._wavebc_cyborg003.html](http://hplgit.github.io/wavebc/doc/pub/._wavebc_cyborg003.html) shows solution demos.

##### Mixed boundary condition

↑ **Parent:** [Neumann boundary condition](#neumann-boundary-condition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mixed_boundary_condition)

Multiple [boundary conditions](#boundary-condition) for different parts of the boundary.

#### Time dependent boundary condition

↑ **Parent:** [Boundary condition](#boundary-condition)

Most commonly, [boundary conditions](#boundary-condition) such as the [Dirichlet boundary condition](#dirichlet-boundary-condition) are taken to be fixed values in time.

But it also makes sense to think about cases where those values vary in time.

Some bibliography:
- [https://math.stackexchange.com/questions/261251/heat-equation-with-time-dependent-boundary-conditions](https://math.stackexchange.com/questions/261251/heat-equation-with-time-dependent-boundary-conditions)
- [https://secure.math.ubc.ca/~peirce/M257_316_2012_Lecture_20.pdf](https://secure.math.ubc.ca/~peirce/M257_316_2012_Lecture_20.pdf)

### Control theory

↑ **Parent:** [Differential equation](#differential-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Control_theory)

This basically adds one more ingredient to [partial differential equations](#partial-differential-equation): a [function](formalization-of-mathematics.md#function-mathematics) that we can select.

And then the question becomes: if this function has such and such limitation, can we make the solution of the [differential equation](#differential-equation) have such and such property?

It's quite fun from a mathematics point of view!

Control theory also takes into consideration possible [discretization](#discretization) of the domain, which allows using [numerical methods to solve partial differential equations](#numerical-method-to-solve-a-partial-differential-equation), as well as digital, rather than analogue control methods.

#### Control engineering

↑ **Parent:** [Control theory](#control-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Control_engineering)

#### Control system

↑ **Parent:** [Control theory](#control-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Control_system)

#### Feedback

↑ **Parent:** [Control theory](#control-theory)

##### Feedback control algorithm

↑ **Parent:** [Feedback](#feedback)

###### Proportional-integral-derivative controller

↑ **Parent:** [Feedback control algorithm](#feedback-control-algorithm)

## Series (mathematics)

↑ **Parent:** [Calculus](calculus.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Series_(mathematics))

### Power series

↑ **Parent:** [Series (mathematics)](#series-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Power_series)

#### Analytic function

↑ **Parent:** [Power series](#power-series)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Analytic_function)

##### Sine and cossine

↑ **Parent:** [Analytic function](#analytic-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sine_and_cossine)

###### Sinusoidal

↑ **Parent:** [Sine and cossine](#sine-and-cossine)  
🏷️ **Tags:** [Periodic function](formalization-of-mathematics.md#periodic-function)

A function that is either a [sine](#sine) or [cosine](#cosine), i.e. we don't know or care where the origin is exactly.

This is particularly relevant in [electronics](electronics.md), where the [oscilloscope](electronics.md#oscilloscope)'s time origin is set to match the wave.

###### Sine

↑ **Parent:** [Sine and cossine](#sine-and-cossine)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sine)

###### Cosine

↑ **Parent:** [Sine and cossine](#sine-and-cossine)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cosine)

#### Radius of convergence

↑ **Parent:** [Power series](#power-series)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Radius_of_convergence)

#### Taylor series

↑ **Parent:** [Power series](#power-series)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Taylor_series)

## Gradient, Divergence, Curl, and Laplacian

↑ **Parent:** [Calculus](calculus.md)

### Curl (mathematics)

↑ **Parent:** [Gradient, Divergence, Curl, and Laplacian](#gradient-divergence-curl-and-laplacian)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Curl_(mathematics))

Points in the direction in which a wind spinner spins fastest.

### Nabla symbol

↑ **Parent:** [Gradient, Divergence, Curl, and Laplacian](#gradient-divergence-curl-and-laplacian)  
🏷️ **Tags:** [Mathematical symbol that looks like a Greek letter but isn't](mathematics.md#mathematical-symbol-that-looks-like-a-greek-letter-but-isn-t)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nabla_symbol)

As if [Greek letters](linguistics.md#greek-alphabet) weren't enough, [physicists](physicist.md) and [mathematicians](mathematics.md#mathematician) also like to make up tons of symbols, [some of which look like the could actually be Greek letters](mathematics.md#mathematical-symbol-that-looks-like-a-greek-letter-but-isn-t)!

Nabla is one of those: it was completely made up in modern times, and just happens to look like an inverted upper case [delta](linguistics.md#delta-letter) to make things even more confusing!

Nabla means "harp" in Greek, which looks like the symbol.

#### Del

↑ **Parent:** [Nabla symbol](#nabla-symbol)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Del)

Oh, and if it weren't enough, [mathematicians](mathematics.md#mathematician) have a separate name for the damned [nabla symbol](#nabla-symbol) : "del" instead of "nabla".

TODO why is it called "Del"? Is is because it is an inverted uppercase [delta](linguistics.md#delta-letter)?

### Divergence

↑ **Parent:** [Gradient, Divergence, Curl, and Laplacian](#gradient-divergence-curl-and-laplacian)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Divergence)

Takes a [vector](linear-algebra.md#vector-mathematics) field as input and produces a scalar field.

Mnemonic: it gives out the amount of fluid that is going in or out of a given volume per unit of time.

Therefore, if you take a cubic volume:
- the input has to be the 6 flows across each face, therefore 3 derivatives
- the output is the variation of the quantity of fluid, and therefore a scalar

### Gradient

↑ **Parent:** [Gradient, Divergence, Curl, and Laplacian](#gradient-divergence-curl-and-laplacian)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gradient)

Takes a scalar field as input and produces a vector field.

Mnemonic: the gradient shows the direction in which the function increases fastest.

Think of a color gradient going from white to black from left to right.

Therefore, it has to:
- take a scalar field as input. Otherwise, how do you decide which vector is larger than the other?
- output a vector field that contains the direction in which the scalar increases fastest locally at each point. This has to give out vectors, since we are talking about directions

### Laplace operator

↑ **Parent:** [Gradient, Divergence, Curl, and Laplacian](#gradient-divergence-curl-and-laplacian)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Laplace_operator)

Can be denoted either by:
- the upper case [Greek letter](linguistics.md#greek-alphabet) [delta](linguistics.md#delta-letter)
- [nabla symbol](#nabla-symbol) squared
Our default symbol is going to be:

$$
\laplacian{}
$$

<h4 id="d-alembert-operator">d'Alembert operator</h4>

↑ **Parent:** [Laplace operator](#laplace-operator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/d'Alembert_operator)

The [laplace operator](#laplace-operator) for [Minkowski space](relativity.md#minkowski-space).

Can be nicely written with [Einstein notation](linear-algebra.md#einstein-notation) as shown at: [Section "d'Alembert operator in Einstein notation"](linear-algebra.md#d-alembert-operator-in-einstein-notation).

## Infinitesimal

↑ **Parent:** [Calculus](calculus.md)  
🏷️ **Tags:** [Evil](cirism.md#evil)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Infinitesimal)

Just use [limit](#limit-mathematics) instead, please. The [French](continent.md#france) are particularly guilty of this.

## ↑ Ancestors (3)

1. [Area of mathematics](mathematics.md#area-of-mathematics)
2. [Mathematics](mathematics.md)
3. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (6)

- [Differentiable manifold](#differentiable-manifold)
- [Limit (mathematics)](#limit-mathematics)
- [Manifold](#manifold)
- [Mathematical analysis](#mathematical-analysis)
- [SymPy](software.md#sympy)
- [Topology](#topology)
