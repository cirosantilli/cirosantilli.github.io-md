<h1 id="_file/python/pytorch/matmul.py">python/pytorch/matmul.py</h1>

↑ **Parent:** [PyTorch](../../../pytorch.md)

[Matrix multiplication](../../../matrix-multiplication.md) example.

Fundamental since [deep learning is mostly matrix multiplication](../../../deep-learning-is-mostly-matrix-multiplication.md).

[NumPy](../../../numpy.md) does not automatically use the [GPU](../../../graphics-processing-unit.md) for it: [https://stackoverflow.com/questions/49605231/does-numpy-automatically-detect-and-use-gpu](https://stackoverflow.com/questions/49605231/does-numpy-automatically-detect-and-use-gpu), and PyTorch is one of the most notable compatible implementations, as it uses the same memory structure as NumPy arrays.

Sample runs on [P51](../../../ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md) to observe the [GPU](../../../graphics-processing-unit.md) speedup:
```
$ time ./matmul.py g 10000 1000 10000 100
real    0m22.980s
user    0m22.679s
sys     0m1.129s
$ time ./matmul.py c 10000 1000 10000 100
real    1m9.924s
user    4m16.213s
sys     0m17.293s
```

## ↑ Ancestors (11)

1. [PyTorch](../../../pytorch.md)
2. [Deep learning framework](../../../deep-learning-framework.md)
3. [Deep learning](../../../deep-learning.md)
4. [Artificial neural network](../../../artificial-neural-network.md)
5. [Neural network](../../../neural-network.md)
6. [Machine learning](../../../machine-learning-split.md)
7. [Computer](../../../computer-split.md)
8. [Information technology](../../../information-technology.md)
9. [Area of technology](../../../area-of-technology.md)
10. [Technology](../../../technology-split.md)
11. [Ciro Santilli's Homepage](../../../split.md)
