# Term symbols for carbon ground state

↑ **Parent:** [Solutions for the Schrodinger equation with multiple particles](solutions-for-the-schrodinger-equation-with-multiple-particles.md)

This example covered for example at [Video 16. "Term Symbols Example 1 by TMP Chem (2015)"](#video-term-symbols-example-1-by-tmp-chem-2015).

[Carbon](carbon.md) has electronic structure 1s2 2s2 2p2.

For term symbols we only care about unfilled layers, because in every filled layer the total z angular momentum is 0, as one electron necessarily cancels out each other:
- [magnetic quantum number](magnetic-quantum-number.md) varies from -l to +l, each with z angular momentum $-l \hbar$ to $+l \hbar$ and so each cancels the other out
- [spin quantum number](spin-quantum-number.md) is either + or minus half, and so each pair of electron cancels the other out

So in this case, we only care about the 2 electrons in 2p2. Let's list out all possible ways in which the 2p2 electrons can be.

There are 3 p orbitals, with three different [magnetic quantum numbers](magnetic-quantum-number.md), each representing a different possible z [quantum angular momentum](angular-momentum-operator.md).

We are going to distribute 2 electrons with 2 different spins across them. All the possible distributions that don't violate the [Pauli exclusion principle](pauli-exclusion-principle.md) are:

```
m_l  +1  0 -1  m_L  m_S
     u_ u_ __    1    1
     u_ __ u_    0    1
     __ u_ u_   -1    1
     d_ d_ __    1   -1
     d_ __ d_    0   -1
     __ d_ d_   -1   -1
     u_ d_ __    1    0
     d_ u_ __    1    0
     u_ __ d_    0    0
     d_ __ u_    0    0
     __ u_ d_   -1    0
     __ d_ u_   -1    0
     ud __ __    2    0
     __ ud __    0    0
     __ __ ud   -2    0
```

where:
- `m_l` is $m_l$, the [magnetic quantum number](magnetic-quantum-number.md) of each electron. Remember that this gives a orbital (non-spin) [quantum angular momentum](angular-momentum-operator.md) of $m_l \hbar$ to each such electron
- `m_L` with a capital L is the sum of the $m_l$ of each electron
- `m_S` with a capital S is the sum of the spin angular momentum of each electron

For example, on the first line:
```
m_l  +1  0 -1  m_L  m_S
     u_ u_ __    1    1
```
we have:
- one electron with $m_l = +1$, and so angular momentum $\hbar$
- one electron with $m_l = +0$, and so angular momentum 0
and so the sum of them has angular momentum $0 + 1 \hbar = 1 \hbar$. So the value of $m_L$ is 1, we just omit the $\hbar$.

TODO now I don't understand the logic behind the next steps... I understand how to mechanically do them, but what do they mean? Can you determine the [term symbol](term-symbol.md) for individual microstates at all? Or do you have to group them to get the answer? Since there are multiple choices in some steps, it appears that you can't assign a specific term symbol to an individual microstate. And it has something to do with the [Slater determinant](slater-determinant.md). The previous lecture mentions it: [https://www.youtube.com/watch?v=7_8n1TS-8Y0](https://www.youtube.com/watch?v=7_8n1TS-8Y0) more precisely [https://youtu.be/7_8n1TS-8Y0?t=2268](https://youtu.be/7_8n1TS-8Y0?t=2268) about carbon.

[https://youtu.be/DAgEmLWpYjs?t=2675](https://youtu.be/DAgEmLWpYjs?t=2675) mentions that $^{3}D$ is not allowed because it would imply $L = 2, S = 1$, which would be a state `uu __ __` which violates the [Pauli exclusion principle](pauli-exclusion-principle.md), and so was not listed on our list of 15 states.

He then goes for $^{1}D$ and mentions:
- S = 1 so $m_S$ can only be 0
- L = 2 (D) so $m_L$ ranges in -2, -1, 0, 1, 2
and so that corresponds to states on our list:
```
ud __ __    2    0
u_ d_ __    1    0
u_ __ d_    0    0
__ u_ d_   -1    0
__ __ ud   -2    0
```
Note that for some we had a two choices, so we just pick any one of them and tick them off off from the table, which now looks like:
```
 +1  0 -1  m_L  m_S
 u_ u_ __    1    1
 u_ __ u_    0    1
 __ u_ u_   -1    1
 d_ d_ __    1   -1
 d_ __ d_    0   -1
 __ d_ d_   -1   -1
 d_ u_ __    1    0
 d_ __ u_    0    0
 __ d_ u_   -1    0
 __ ud __    0    0
```

Then for $^{3}P$ the choices are:
- S = 2 so $m_S$ is either -1, 0  or 1
- L = 1 (P) so $m_L$ ranges in -1, 0, 1
so we have 9 possibilities for both together. We again verify that 9 such states are left matching those criteria, and tick them off, and so on.

For the $m_S$, we have two electrons with spin up. The angular momentum of each electron is $1/2 \hbar$, and so given that we have two, the total is $1 \hbar$, so again we omit $\hbar$ and $m_S$ is 1.

<a id="video-term-symbols-example-1-by-tmp-chem-2015"></a>
**[Video 16](#video-term-symbols-example-1-by-tmp-chem-2015). Term Symbols Example 1 by TMP Chem (2015)** [Source](https://www.youtube.com/watch?v=doC9Z2S7lm8). Carbon atom.

Bibliography:
- [https://youtu.be/DAgEmLWpYjs?t=1962](https://youtu.be/DAgEmLWpYjs?t=1962) from [Video 15. "Atomic Term Symbols by T. Daniel Crawford (2016)"](term-symbol.md#video-atomic-term-symbols-by-t-daniel-crawford-2016)

## ↑ Ancestors (10)

1. [Solutions for the Schrodinger equation with multiple particles](solutions-for-the-schrodinger-equation-with-multiple-particles.md)
2. [Solutions of the Schrodinger equation](solutions-of-the-schrodinger-equation.md)
3. [Schrödinger equation](schrodinger-equation.md)
4. [Non-relativistic quantum mechanics](non-relativistic-quantum-mechanics.md)
5. [Quantum mechanics](quantum-mechanics-split.md)
6. [Particle physics](particle-physics-split.md)
7. [Physics](physics-split.md)
8. [Natural science](natural-science.md)
9. [Science](science-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Term symbol](term-symbol.md)
