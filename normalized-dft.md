# Normalized DFT

↑ **Parent:** [Discrete Fourier transform](discrete-fourier-transform.md)

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

## ↑ Ancestors (6)

1. [Discrete Fourier transform](discrete-fourier-transform.md)
2. [Fourier series](fourier-series.md)
3. [Calculus](calculus-split.md)
4. [Area of mathematics](area-of-mathematics.md)
5. [Mathematics](mathematics-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Qiskit/qft.py](_file/qiskit/qft.py.md)
