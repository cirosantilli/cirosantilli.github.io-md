# CNN convolution kernels are also learnt

↑ **Parent:** [Convolutional neural network](convolutional-neural-network.md)

CNN convolution kernels are not hardcoded. They are learnt and optimized via [backpropagation](backpropagation.md). You just specify their size! Example in [PyTorch](pytorch.md) you'd do just:
```
nn.Conv2d(1, 6, kernel_size=(5, 5))
```
as used for example at: [activatedgeek/LeNet-5](activatedgeek-lenet-5.md).

This can also be inferred from: [https://stackoverflow.com/questions/55594969/how-to-visualise-filters-in-a-cnn-with-pytorch](https://stackoverflow.com/questions/55594969/how-to-visualise-filters-in-a-cnn-with-pytorch) where we see that the kernels are not perfectly regular as you'd expected from something hand coded.

## ↑ Ancestors (10)

1. [Convolutional neural network](convolutional-neural-network.md)
2. [ANN model](ann-model.md)
3. [Artificial neural network](artificial-neural-network.md)
4. [Neural network](neural-network.md)
5. [Machine learning](machine-learning-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
