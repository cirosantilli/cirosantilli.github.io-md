# Theories of Quantum Matter by Austen Lamacraft

↑ **Parent:** [Condensed matter university course](condensed-matter-physics.md#condensed-matter-university-course)  
🏷️ **Tags:** [CC BY-NC-ND 4.0 table of contents](law.md#cc-by-nc-nd-4-0-table-of-contents), [GitHub book repo](software.md#github-book-repo)

<a id="_3"></a>
<a id="_4"></a>
- [https://austen.uk/courses/tqm/](https://austen.uk/courses/tqm/)
<a id="_5"></a>
- [https://github.com/AustenLamacraft/Theories-of-Quantum-Matter](https://github.com/AustenLamacraft/Theories-of-Quantum-Matter) Written in [Jekyll](website.md#jekyll-software)

<a id="_6"></a>
As mentioned on the introduction, the main objective of the course is to try predict qualitative properties of materials, notably the existence of certain [phase transitions](statistical-physics.md#phase-transition), starting from first principle toy models.

<a id="_7"></a>
Key phenomena covered include:<a id="_8"></a>

<a id="_9"></a>
- [fractional quantum Hall effect](quantum-mechanics.md#fractional-quantum-hall-effect)

**Table of contents**

- [Many Body Wavefunctions](#many-body-wavefunctions)
  - [Bosons and Fermions](#many-body-wavefunctions/bosons-and-fermions)
    - [Two Particles](#many-body-wavefunctions/two-particles)
    - [Product States](#many-body-wavefunctions/product-states)
  - [The 1D Fermi Gas](#many-body-wavefunctions/the-1d-fermi-gas)
    - [Ground State](#many-body-wavefunctions/1d-fermi-gas-ground-state)
    - [Density; Density Matrix; Pair Distribution](#many-body-wavefunctions/1d-fermi-gas-density)
    - [Impenetrable Bose Gas](#many-body-wavefunctions/impenetrable-bose-gas)
- [Quantum Hall Effect](#quantum-hall-effect)
  - [Fractional Quantum Hall Effect](#quantum-hall-effect/fractional-quantum-hall-effect)
    - [Landau Levels](#quantum-hall-effect/landau-levels)
      - [Lowest Landau level](#quantum-hall-effect/lowest-landau-level)
        - [Filled LLL of Fermions](#quantum-hall-effect/filled-lll-of-fermions)
    - [The Laughlin Wavefunction](#quantum-hall-effect/the-laughlin-wavefunction)
    - [The Plasma Analogy](#quantum-hall-effect/the-plasma-analogy)
    - [Fractional Charge](#quantum-hall-effect/fractional-charge)
    - [Fractional Statistics](#quantum-hall-effect/fractional-statistics)
  - [Appendix](#quantum-hall-effect/quantum-hall-effect-appendix)
    - [Sampling from a complex wavefunction](#quantum-hall-effect/sampling-from-a-complex-wavefunction)
- [The Elastic Chain](#the-elastic-chain)
  - [The Classical System](#the-elastic-chain/the-classical-system)
    - [Equations of Motion](#the-elastic-chain/equations-of-motion)
    - [Hamiltonian Formulation](#the-elastic-chain/hamiltonian-formulation)
    - [Complex Coordinates](#the-elastic-chain/complex-coordinates)
  - [Quantum Oscillators](#the-elastic-chain/quantum-oscillators)
    - [The Quantum Chain](#the-elastic-chain/the-quantum-chain)
    - [Oscillator Quanta are Bosons!](#the-elastic-chain/oscillator-quanta-are-bosons)
    - [Thermodynamic ($N \to \infty$) limit](#the-elastic-chain/thermodynamic-n-to-infty-limit)
    - [Finite Temperature](#the-elastic-chain/finite-temperature)
    - [Position Fluctuations](#the-elastic-chain/position-fluctuations)
    - [Density Fluctuations](#the-elastic-chain/density-fluctuations)
  - [Appendix](#the-elastic-chain/appendix)
    - [Fourier review](#the-elastic-chain/fourier-review)
    - [Discrete Fourier Transform](#the-elastic-chain/discrete-fourier-transform)
    - [Properties of the Fourier Transform](#the-elastic-chain/properties-of-the-fourier-transform)
    - [Higher dimensions](#the-elastic-chain/higher-dimensions)
    - [Evaluating (56)](#the-elastic-chain/evaluating-56)

## Many Body Wavefunctions

↑ **Parent:** [Theories of Quantum Matter by Austen Lamacraft](theories-of-quantum-matter-by-austen-lamacraft.md)

<a id="many-body-wavefunctions/_10"></a>
<a id="many-body-wavefunctions/_11"></a>
- [https://austen.uk/courses/tqm/many-body-wavefunctions/](https://austen.uk/courses/tqm/many-body-wavefunctions/)
<a id="many-body-wavefunctions/_12"></a>
- [Solutions for the Schrodinger equation with multiple particles](quantum-mechanics.md#solutions-for-the-schrodinger-equation-with-multiple-particles)

<h3 id="many-body-wavefunctions/bosons-and-fermions">Bosons and Fermions</h3>

↑ **Parent:** [Many Body Wavefunctions](#many-body-wavefunctions)

<a id="many-body-wavefunctions/_13"></a>
<a id="many-body-wavefunctions/_14"></a>
- [https://austen.uk/courses/tqm/many-body-wavefunctions/#bosons-and-fermions](https://austen.uk/courses/tqm/many-body-wavefunctions/#bosons-and-fermions)
<a id="many-body-wavefunctions/_15"></a>
- [Fermions, bosons and anyons](relativistic-quantum-mechanics.md#fermions-bosons-and-anyons)

<h4 id="many-body-wavefunctions/two-particles">Two Particles</h4>

↑ **Parent:** [Bosons and Fermions](#many-body-wavefunctions/bosons-and-fermions)

<a id="many-body-wavefunctions/_16"></a>
<a id="many-body-wavefunctions/_17"></a>
- [https://austen.uk/courses/tqm/many-body-wavefunctions/#two-particles](https://austen.uk/courses/tqm/many-body-wavefunctions/#two-particles)
<a id="many-body-wavefunctions/_18"></a>
- [Solutions of the Schrodinger equation for two electrons](quantum-mechanics.md#solutions-of-the-schrodinger-equation-for-two-electrons)

<h4 id="many-body-wavefunctions/product-states">Product States</h4>

↑ **Parent:** [Bosons and Fermions](#many-body-wavefunctions/bosons-and-fermions)

<a id="many-body-wavefunctions/_19"></a>
<a id="many-body-wavefunctions/_20"></a>
- [https://austen.uk/courses/tqm/many-body-wavefunctions/#product-states](https://austen.uk/courses/tqm/many-body-wavefunctions/#product-states)
<a id="many-body-wavefunctions/_21"></a>
- [Product state](quantum-mechanics.md#separable-state)

<h3 id="many-body-wavefunctions/the-1d-fermi-gas">The 1D Fermi Gas</h3>

↑ **Parent:** [Many Body Wavefunctions](#many-body-wavefunctions)

<a id="many-body-wavefunctions/_22"></a>
<a id="many-body-wavefunctions/_23"></a>
- [https://austen.uk/courses/tqm/many-body-wavefunctions/#the-1d-fermi-gas](https://austen.uk/courses/tqm/many-body-wavefunctions/#the-1d-fermi-gas)
<a id="many-body-wavefunctions/_24"></a>
- [1D Fermi gas](condensed-matter-physics.md#1d-fermi-gas)

<h4 id="many-body-wavefunctions/1d-fermi-gas-ground-state">Ground State</h4>

↑ **Parent:** [The 1D Fermi Gas](#many-body-wavefunctions/the-1d-fermi-gas)

<a id="many-body-wavefunctions/_25"></a>
<a id="many-body-wavefunctions/_26"></a>
- [https://austen.uk/courses/tqm/many-body-wavefunctions/#ground-state](https://austen.uk/courses/tqm/many-body-wavefunctions/#ground-state)

<h4 id="many-body-wavefunctions/1d-fermi-gas-density">Density; Density Matrix; Pair Distribution</h4>

↑ **Parent:** [The 1D Fermi Gas](#many-body-wavefunctions/the-1d-fermi-gas)

<a id="many-body-wavefunctions/_27"></a>
<a id="many-body-wavefunctions/_28"></a>
- [https://austen.uk/courses/tqm/many-body-wavefunctions/#density-density-matrix-pair-distribution](https://austen.uk/courses/tqm/many-body-wavefunctions/#density-density-matrix-pair-distribution)

<h4 id="many-body-wavefunctions/impenetrable-bose-gas">Impenetrable Bose Gas</h4>

↑ **Parent:** [The 1D Fermi Gas](#many-body-wavefunctions/the-1d-fermi-gas)

<a id="many-body-wavefunctions/_29"></a>
<a id="many-body-wavefunctions/_30"></a>
- [https://austen.uk/courses/tqm/many-body-wavefunctions/#impenetrable-bose-gas](https://austen.uk/courses/tqm/many-body-wavefunctions/#impenetrable-bose-gas)
<a id="many-body-wavefunctions/_31"></a>
- [Impenetrable Bose Gas](condensed-matter-physics.md#impenetrable-bose-gas)

## Quantum Hall Effect

↑ **Parent:** [Theories of Quantum Matter by Austen Lamacraft](theories-of-quantum-matter-by-austen-lamacraft.md)

<a id="quantum-hall-effect/_32"></a>
<a id="quantum-hall-effect/_33"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect](https://austen.uk/courses/tqm/quantum-hall-effect)
<a id="quantum-hall-effect/_34"></a>
- [Quantum Hall effect](quantum-mechanics.md#quantum-hall-effect)

<h3 id="quantum-hall-effect/fractional-quantum-hall-effect">Fractional Quantum Hall Effect</h3>

↑ **Parent:** [Quantum Hall Effect](#quantum-hall-effect)

<a id="quantum-hall-effect/_35"></a>
<a id="quantum-hall-effect/_36"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#fractional-quantum-hall-effect](https://austen.uk/courses/tqm/quantum-hall-effect/#fractional-quantum-hall-effect)
<a id="quantum-hall-effect/_37"></a>
- [Fractional quantum Hall effect](quantum-mechanics.md#fractional-quantum-hall-effect)

<h4 id="quantum-hall-effect/landau-levels">Landau Levels</h4>

↑ **Parent:** [Fractional Quantum Hall Effect](#quantum-hall-effect/fractional-quantum-hall-effect)

<a id="quantum-hall-effect/_38"></a>
<a id="quantum-hall-effect/_39"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#landau-levels](https://austen.uk/courses/tqm/quantum-hall-effect/#landau-levels)
<a id="quantum-hall-effect/_40"></a>
- [Landau level](particle-physics.md#landau-level)

<h5 id="quantum-hall-effect/lowest-landau-level">Lowest Landau level</h5>

↑ **Parent:** [Landau Levels](#quantum-hall-effect/landau-levels)

<h6 id="quantum-hall-effect/filled-lll-of-fermions">Filled LLL of Fermions</h6>

↑ **Parent:** [Lowest Landau level](#quantum-hall-effect/lowest-landau-level)

<a id="quantum-hall-effect/_42"></a>
<a id="quantum-hall-effect/_43"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#filled-lll-of-fermions](https://austen.uk/courses/tqm/quantum-hall-effect/#filled-lll-of-fermions)

<h4 id="quantum-hall-effect/the-laughlin-wavefunction">The Laughlin Wavefunction</h4>

↑ **Parent:** [Fractional Quantum Hall Effect](#quantum-hall-effect/fractional-quantum-hall-effect)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/The_Laughlin_Wavefunction)

<a id="quantum-hall-effect/_44"></a>
<a id="quantum-hall-effect/_45"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#the-laughlin-wavefunction](https://austen.uk/courses/tqm/quantum-hall-effect/#the-laughlin-wavefunction)
<a id="quantum-hall-effect/_46"></a>
- [Laughlin wavefunction](condensed-matter-physics.md#laughlin-wavefunction)

<h4 id="quantum-hall-effect/the-plasma-analogy">The Plasma Analogy</h4>

↑ **Parent:** [Fractional Quantum Hall Effect](#quantum-hall-effect/fractional-quantum-hall-effect)

<a id="quantum-hall-effect/_47"></a>
<a id="quantum-hall-effect/_48"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#the-plasma-analogy](https://austen.uk/courses/tqm/quantum-hall-effect/#the-plasma-analogy)

<h4 id="quantum-hall-effect/fractional-charge">Fractional Charge</h4>

↑ **Parent:** [Fractional Quantum Hall Effect](#quantum-hall-effect/fractional-quantum-hall-effect)

<a id="quantum-hall-effect/_49"></a>
<a id="quantum-hall-effect/_50"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#fractional-charge](https://austen.uk/courses/tqm/quantum-hall-effect/#fractional-charge)
<a id="quantum-hall-effect/_51"></a>
- [Anyon](relativistic-quantum-mechanics.md#anyon)

<h4 id="quantum-hall-effect/fractional-statistics">Fractional Statistics</h4>

↑ **Parent:** [Fractional Quantum Hall Effect](#quantum-hall-effect/fractional-quantum-hall-effect)

<a id="quantum-hall-effect/_52"></a>
<a id="quantum-hall-effect/_53"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#fractional-statistics](https://austen.uk/courses/tqm/quantum-hall-effect/#fractional-statistics)

<h3 id="quantum-hall-effect/quantum-hall-effect-appendix">Appendix</h3>

↑ **Parent:** [Quantum Hall Effect](#quantum-hall-effect)

<a id="quantum-hall-effect/_54"></a>
<a id="quantum-hall-effect/_55"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#appendix](https://austen.uk/courses/tqm/quantum-hall-effect/#appendix)

<h4 id="quantum-hall-effect/sampling-from-a-complex-wavefunction">Sampling from a complex wavefunction</h4>

↑ **Parent:** [Appendix](#quantum-hall-effect/quantum-hall-effect-appendix)

<a id="quantum-hall-effect/_56"></a>
<a id="quantum-hall-effect/_57"></a>
- [https://austen.uk/courses/tqm/quantum-hall-effect/#sampling-from-a-complex-wavefunction](https://austen.uk/courses/tqm/quantum-hall-effect/#sampling-from-a-complex-wavefunction)

## The Elastic Chain

↑ **Parent:** [Theories of Quantum Matter by Austen Lamacraft](theories-of-quantum-matter-by-austen-lamacraft.md)

<a id="the-elastic-chain/_58"></a>
[https://austen.uk/courses/tqm/elastic-chain/](https://austen.uk/courses/tqm/elastic-chain/)

<h3 id="the-elastic-chain/the-classical-system">The Classical System</h3>

↑ **Parent:** [The Elastic Chain](#the-elastic-chain)

<a id="the-elastic-chain/_59"></a>
[https://austen.uk/courses/tqm/elastic-chain/#the-classical-system](https://austen.uk/courses/tqm/elastic-chain/#the-classical-system)

<h4 id="the-elastic-chain/equations-of-motion">Equations of Motion</h4>

↑ **Parent:** [The Classical System](#the-elastic-chain/the-classical-system)

<a id="the-elastic-chain/_60"></a>
[https://austen.uk/courses/tqm/elastic-chain/#the-classical-system](https://austen.uk/courses/tqm/elastic-chain/#the-classical-system)

<h4 id="the-elastic-chain/hamiltonian-formulation">Hamiltonian Formulation</h4>

↑ **Parent:** [The Classical System](#the-elastic-chain/the-classical-system)

<a id="the-elastic-chain/_61"></a>
[https://austen.uk/courses/tqm/elastic-chain/#hamiltonian-formulation](https://austen.uk/courses/tqm/elastic-chain/#hamiltonian-formulation)

<h4 id="the-elastic-chain/complex-coordinates">Complex Coordinates</h4>

↑ **Parent:** [The Classical System](#the-elastic-chain/the-classical-system)

<a id="the-elastic-chain/_62"></a>
[https://austen.uk/courses/tqm/elastic-chain/#complex-coordinates](https://austen.uk/courses/tqm/elastic-chain/#complex-coordinates)

<h3 id="the-elastic-chain/quantum-oscillators">Quantum Oscillators</h3>

↑ **Parent:** [The Elastic Chain](#the-elastic-chain)

<a id="the-elastic-chain/_63"></a>
[https://austen.uk/courses/tqm/elastic-chain/#quantum-oscillators](https://austen.uk/courses/tqm/elastic-chain/#quantum-oscillators)

<h4 id="the-elastic-chain/the-quantum-chain">The Quantum Chain</h4>

↑ **Parent:** [Quantum Oscillators](#the-elastic-chain/quantum-oscillators)

<a id="the-elastic-chain/_64"></a>
[https://austen.uk/courses/tqm/elastic-chain/#the-quantum-chain](https://austen.uk/courses/tqm/elastic-chain/#the-quantum-chain)

<h4 id="the-elastic-chain/oscillator-quanta-are-bosons">Oscillator Quanta are Bosons!</h4>

↑ **Parent:** [Quantum Oscillators](#the-elastic-chain/quantum-oscillators)

<a id="the-elastic-chain/_65"></a>
[https://austen.uk/courses/tqm/elastic-chain/#oscillator-quanta-are-bosons](https://austen.uk/courses/tqm/elastic-chain/#oscillator-quanta-are-bosons)

<h4 id="the-elastic-chain/thermodynamic-n-to-infty-limit">Thermodynamic (<span class="katex"><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.6833em;"></span><span class="mord mathnormal" style="margin-right:0.10903em;">N</span><span class="mspace" style="margin-right:0.2778em;"></span><span class="mrel">→</span><span class="mspace" style="margin-right:0.2778em;"></span></span><span class="base"><span class="strut" style="height:0.4306em;"></span><span class="mord">∞</span></span></span></span>) limit</h4>

↑ **Parent:** [Quantum Oscillators](#the-elastic-chain/quantum-oscillators)

<a id="the-elastic-chain/_66"></a>
[https://austen.uk/courses/tqm/elastic-chain/#thermodynamic-nto-infty-limit](https://austen.uk/courses/tqm/elastic-chain/#thermodynamic-nto-infty-limit)

<h4 id="the-elastic-chain/finite-temperature">Finite Temperature</h4>

↑ **Parent:** [Quantum Oscillators](#the-elastic-chain/quantum-oscillators)

<a id="the-elastic-chain/_67"></a>
[https://austen.uk/courses/tqm/elastic-chain/#finite-temperature](https://austen.uk/courses/tqm/elastic-chain/#finite-temperature)

<h4 id="the-elastic-chain/position-fluctuations">Position Fluctuations</h4>

↑ **Parent:** [Quantum Oscillators](#the-elastic-chain/quantum-oscillators)

<a id="the-elastic-chain/_68"></a>
[https://austen.uk/courses/tqm/elastic-chain/#position-fluctuations](https://austen.uk/courses/tqm/elastic-chain/#position-fluctuations)

<h4 id="the-elastic-chain/density-fluctuations">Density Fluctuations</h4>

↑ **Parent:** [Quantum Oscillators](#the-elastic-chain/quantum-oscillators)

<a id="the-elastic-chain/_69"></a>
[https://austen.uk/courses/tqm/elastic-chain/#density-fluctuations](https://austen.uk/courses/tqm/elastic-chain/#density-fluctuations)

<h3 id="the-elastic-chain/appendix">Appendix</h3>

↑ **Parent:** [The Elastic Chain](#the-elastic-chain)

<a id="the-elastic-chain/_70"></a>
[https://austen.uk/courses/tqm/elastic-chain/#appendix](https://austen.uk/courses/tqm/elastic-chain/#appendix)

<h4 id="the-elastic-chain/fourier-review">Fourier review</h4>

↑ **Parent:** [Appendix](#the-elastic-chain/appendix)

<a id="the-elastic-chain/_71"></a>
[https://austen.uk/courses/tqm/elastic-chain/#fourier-review](https://austen.uk/courses/tqm/elastic-chain/#fourier-review)

<h4 id="the-elastic-chain/discrete-fourier-transform">Discrete Fourier Transform</h4>

↑ **Parent:** [Appendix](#the-elastic-chain/appendix)

<a id="the-elastic-chain/_72"></a>
[https://austen.uk/courses/tqm/elastic-chain/#discrete-fourier-transform](https://austen.uk/courses/tqm/elastic-chain/#discrete-fourier-transform)

<h4 id="the-elastic-chain/properties-of-the-fourier-transform">Properties of the Fourier Transform</h4>

↑ **Parent:** [Appendix](#the-elastic-chain/appendix)

<a id="the-elastic-chain/_73"></a>
[https://austen.uk/courses/tqm/elastic-chain/#properties-of-the-fourier-transform](https://austen.uk/courses/tqm/elastic-chain/#properties-of-the-fourier-transform)

<h4 id="the-elastic-chain/higher-dimensions">Higher dimensions</h4>

↑ **Parent:** [Appendix](#the-elastic-chain/appendix)

<a id="the-elastic-chain/_74"></a>
[https://austen.uk/courses/tqm/elastic-chain/#higher-dimensions](https://austen.uk/courses/tqm/elastic-chain/#higher-dimensions)

<h4 id="the-elastic-chain/evaluating-56">Evaluating (56)</h4>

↑ **Parent:** [Appendix](#the-elastic-chain/appendix)

<a id="the-elastic-chain/_75"></a>
[https://austen.uk/courses/tqm/elastic-chain/#evaluating-eqrefcoll_uvar](https://austen.uk/courses/tqm/elastic-chain/#evaluating-eqrefcoll_uvar)

## ↑ Ancestors (7)

1. [Condensed matter university course](condensed-matter-physics.md#condensed-matter-university-course)
2. [Condensed matter Physics bibliography](condensed-matter-physics.md#condensed-matter-physics-bibliography)
3. [Condensed matter physics](condensed-matter-physics.md)
4. [Physics](physics.md)
5. [Natural science](science.md#natural-science)
6. [Science](science.md)
7. [Ciro Santilli's Homepage](README.md)
