# Discrete Fourier transform

↑ **Parent:** [Fourier series](fourier-series.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Discrete_Fourier_transform)

Input: a sequence of $N$ [complex numbers](complex-number.md) $x_k$.

Output: another sequence of $N$ [complex numbers](complex-number.md) $X_k$ such that:

$$
x_n = \frac{1}{N} \sum_{k=0}^{N-1} X_k e^{i 2 \pi \frac{k n}{N}}
$$

Intuitively, this means that we are braking up the complex signal into $N$ [sinusoidal](sinusoidal.md) frequencies:
- $X_0$: is kind of magic and ends up being a constant added to the signal because $e^{i 2 \pi \frac{k n}{N}} = e^{0} = 1$
- $X_1$: [sinusoidal](sinusoidal.md) that completes one cycle over the signal. The larger the $N$, the larger the resolution of that [sinusoidal](sinusoidal.md). But it completes one cycle regardless.
- $X_2$: [sinusoidal](sinusoidal.md) that completes two cycles over the signal
- ...
- $X_{N-1}$: [sinusoidal](sinusoidal.md) that completes $N-1$ cycles over the signal
and  is the amplitude of each sine.

We use [Zero-based numbering](zero-based-numbering.md) in our definitions because it just makes every formula simpler.

Motivation: similar to the [Fourier transform](fourier-transform.md):
- compression: a [sine](sine.md) would use N points in the time domain, but in the frequency domain just one, so we can throw the rest away. A sum of two sines, only two. So if your signal has periodicity, in general you can compress it with the transform
- noise removal: many systems add noise only at certain frequencies, which are hopefully different from the main frequencies of the actual signal. By doing the transform, we can remove those frequencies to attain a better [signal-to-noise](signal-to-noise-ratio.md)
In particular, the [discrete Fourier transform](discrete-fourier-transform.md) is used in [signal processing](signal-processing.md) after a [analog-to-digital converter](analog-to-digital-converter.md). [Digital signal processing](digital-signal-processing.md) historically likely grew more and more over analog processing as digital [processors](processor-computing.md) got faster and faster as it gives more flexibility in algorithm design.

Sample software implementations:
- [numpy.fft](numpy-fft.md), notably see the example: [numpy/fft.py](_file/numpy/fft.py.md)

<a id="image-dft-of-2-sin-t-plus-cos-4t-with-25-points-discrete-fourier-transform"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/home/numpy/fft_plot.svg" alt="" height="600">

**[Figure 2](#image-dft-of-2-sin-t-plus-cos-4t-with-25-points-discrete-fourier-transform). DFT of $2 \sin(t) + \cos(4t)$ with 25 points**. This is a simple example of a [discrete Fourier transform](discrete-fourier-transform.md) for a real input signal. It illustrates how the [DFT](discrete-fourier-transform.md) takes N [complex numbers](complex-number.md) as input, and produces N [complex numbers](complex-number.md) as output. It also illustrates how the [discrete Fourier transform of a real signal](discrete-fourier-transform-of-a-real-signal.md) is symmetric around the center point.

**Table of contents**

- [Discrete Fourier transform of a real signal](discrete-fourier-transform-of-a-real-signal.md)
- [Normalized DFT](normalized-dft.md)
- [Fast Fourier transform](fast-fourier-transform.md)

## 🏷️ Tagged (2)

- [Numpy.fft](numpy-fft.md)
- [Quantum Fourier transform](quantum-fourier-transform.md)

## ↑ Ancestors (5)

1. [Fourier series](fourier-series.md)
2. [Calculus](calculus-split.md)
3. [Area of mathematics](area-of-mathematics.md)
4. [Mathematics](mathematics-split.md)
5. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [Numpy/fft.py](_file/numpy/fft.py.md)
- [Qiskit/qft.py](_file/qiskit/qft.py.md)
- [The best articles by Ciro Santilli](articles-split.md)
- [Deletionism on Wikipedia](deletionism-on-wikipedia.md)
- [Discrete Fourier transform](discrete-fourier-transform.md)
- [Fast Fourier transform](fast-fourier-transform.md)
