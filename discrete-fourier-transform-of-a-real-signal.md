# Discrete Fourier transform of a real signal

↑ **Parent:** [Discrete Fourier transform](discrete-fourier-transform.md)

See sections: "Example 1 - N even", "Example 2 - N odd" and "Representation in terms of sines and cosines" of [https://www.statlect.com/matrix-algebra/discrete-Fourier-transform-of-a-real-signal](https://www.statlect.com/matrix-algebra/discrete-Fourier-transform-of-a-real-signal)

The transform still has complex numbers.

Summary:
- $X_0$ is real
- $X_1 = \conj{X_{N-1}}$
- $X_2 = \conj{X_{N-2}}$
- $X_k = \conj{X_{N-k}}$
Therefore, we only need about half of $X_k$ to represent the signal, as the other half can be derived by conjugation.

"Representation in terms of sines and cosines" from [https://www.statlect.com/matrix-algebra/discrete-Fourier-transform-of-a-real-signal](https://www.statlect.com/matrix-algebra/discrete-Fourier-transform-of-a-real-signal) then gives explicit formulas in terms of $X_k$.

[NumPy](numpy.md) for example has "Real FFTs" for this: [https://numpy.org/doc/1.24/reference/routines.fft.html#real-ffts](https://numpy.org/doc/1.24/reference/routines.fft.html#real-ffts)

<a id="image-dft-of-2-sin-t-plus-cos-4t-with-25-points-discrete-fourier-transform-of-a-real-signal"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/home/numpy/fft_plot.svg" alt="" height="600">

**[Figure 3](#image-dft-of-2-sin-t-plus-cos-4t-with-25-points-discrete-fourier-transform-of-a-real-signal). DFT of $2 \sin(t) + \cos(4t)$ with 25 points**. Source at: [numpy/fft\_plot.py](_file/numpy/fft_plot.py.md). This plot illustrates how the DFT of a real signal is symmetric around the middle point, and so only half of the transform points are needed to reconstruct the original signal. We also see how the phase of the sinusoids determines if their DFT components are real or imaginary.

## ↑ Ancestors (6)

1. [Discrete Fourier transform](discrete-fourier-transform.md)
2. [Fourier series](fourier-series.md)
3. [Calculus](calculus-split.md)
4. [Area of mathematics](area-of-mathematics.md)
5. [Mathematics](mathematics-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Numpy/fft.py](_file/numpy/fft.py.md)
- [Discrete Fourier transform](discrete-fourier-transform.md)
