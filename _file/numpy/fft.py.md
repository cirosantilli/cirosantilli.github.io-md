<h1 id="_file/numpy/fft.py">numpy/fft.py</h1>

↑ **Parent:** [Numpy.fft](../../numpy-fft.md)

Output:
```
sin(t)
fft
real 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
imag 0 -10 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 10
rfft
real 0 0 0 0 0 0 0 0 0 0 0
imag 0 -10 0 0 0 0 0 0 0 0 0

sin(t) + sin(4t)
fft
real 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
imag 0 -10 0 0 -10 0 0 0 0 0 0 0 0 0 0 0 10 0 0 10
rfft
real 0 0 0 0 0 0 0 0 0 0 0
imag 0 -10 0 0 -10 0 0 0 0 0 0
```
With our understanding of the [discrete Fourier transform](../../discrete-fourier-transform.md) we see clearly that:
- the signal is being decomposed into [sinusoidal](../../sinusoidal.md) components
- because we are doing the [Discrete Fourier transform of a real signal](../../discrete-fourier-transform-of-a-real-signal.md), for the `fft`, $X_k = \conj{X_{N-k}}$ so there is redundancy in the. We also understand that `rfft` simply cuts off and only keeps half of the coefficients

## ↑ Ancestors (13)

1. [Numpy.fft](../../numpy-fft.md)
2. [NumPy](../../numpy.md)
3. [Python scientific library](../../python-scientific-library.md)
4. [Python library](../../python-library.md)
5. [Python (programming language)](../../python-programming-language.md)
6. [List of programming languages](../../list-of-programming-languages.md)
7. [Programming language](../../programming-language-split.md)
8. [Software](../../software-split.md)
9. [Computer](../../computer-split.md)
10. [Information technology](../../information-technology.md)
11. [Area of technology](../../area-of-technology.md)
12. [Technology](../../technology-split.md)
13. [Ciro Santilli's Homepage](../../split.md)

## ← Incoming links (1)

- [Discrete Fourier transform](../../discrete-fourier-transform.md)
