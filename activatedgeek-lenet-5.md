<h1 id="activatedgeek-lenet-5">activatedgeek/LeNet-5</h1>

↑ **Parent:** [LeNet implementation](lenet-implementation.md)  
🏷️ **Tags:** [PyTorch model](pytorch-model.md)

[https://github.com/activatedgeek/LeNet-5](https://github.com/activatedgeek/LeNet-5)

This repository contains a very clean minimal [PyTorch](pytorch.md) implementation of [LeNet-5](lenet.md) for [MNIST](mnist-database.md).

It trains the [LeNet-5](lenet.md) [neural network](neural-network.md) on the [MNIST](mnist-database.md) dataset from scratch, and afterwards you can give it newly hand-written digits 0 to 9 and it will hopefully recognize the digit for you.

[Ciro Santilli](ciro-santilli-split.md) created a small fork of this repo at [lenet](_file/lenet.md) adding better automation for:
- [extracting MNIST images](extract-mnist-images.md) as PNG
- [ONNX](onnx.md) CLI inference taking any image files as input
- a [Python `tkinter`](python-tkinter.md) GUI that lets you draw and see inference live
- running on [GPU](graphics-processing-unit.md)

Install on [Ubuntu 24.10](ubuntu-24-10.md) with:
```
sudo apt install protobuf-compiler
git clone https://github.com/activatedgeek/LeNet-5
cd LeNet-5
git checkout 95b55a838f9d90536fd3b303cede12cf8b5da47f
virtualenv -p python3 .venv
. .venv/bin/activate
pip install \
  Pillow==6.2.0 \
  numpy==1.24.2 \
  onnx==1.13.1 \
  torch==2.0.0 \
  torchvision==0.15.1 \
  visdom==0.2.4 \
;
```
We use our own `pip install` because their requirements.txt uses `>=` instead of `==` making it random if things will work or not.

On [Ubuntu 22.10](ubuntu-22-10.md) it was instead:
```
pip install
  Pillow==6.2.0 \
  numpy==1.26.4 \
  onnx==1.17.0 torch==2.6.0 \
  torchvision==0.21.0 \
  visdom==0.2.4 \
;
```

Then run with:
```
python run.py
```
This script:
- does a fixed 15 [epochs](epoch-deep-learning.md) on the [training data](training-data-set.md)
- it then uses the trained net from memory to check accuracy with the [test data](test-data-set.md)
- then it also produces a `lenet.onnx` [ONNX](onnx.md) file which contains the trained network, nice!
It throws a billion exceptions because we didn't start the Visdom server, but everything works nevertheless, we just don't get a visualization of the training.

The terminal outputs lines such as:
```
Train - Epoch 1, Batch: 0, Loss: 2.311587
Train - Epoch 1, Batch: 10, Loss: 2.067062
Train - Epoch 1, Batch: 20, Loss: 0.959845
...
Train - Epoch 1, Batch: 230, Loss: 0.071796
Test Avg. Loss: 0.000112, Accuracy: 0.967500
...
Train - Epoch 15, Batch: 230, Loss: 0.010040
Test Avg. Loss: 0.000038, Accuracy: 0.989300
```

And the runtime on [Ubuntu 22.10](ubuntu-22-10.md), [P51](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md) was:
```
real    2m10.262s
user    11m9.771s
sys     0m26.368s
```

One of the benefits of the [ONNX](onnx.md) output is that we can nicely visualize the [neural network](neural-network.md) on [Netron](netron.md):

<a id="image-netron-visualization-of-the-activatedgeek-lenet-5-onnx-output"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/e9225ddf4bb8ce4bad8cc2a9d6503d683dec5db6/activatedgeek_LeNet-5_onnx.svg" alt="" height="1200">

**[Figure 3](#image-netron-visualization-of-the-activatedgeek-lenet-5-onnx-output). Netron visualization of the activatedgeek/LeNet-5 ONNX output**. From this we can see the bifurcation on the computational graph as done in the code at:
```
output = self.c1(img)
x = self.c2_1(output)
output = self.c2_2(output)
output += x
output = self.c3(output)
```

This doesn't seem to conform to the original [LeNet-5](lenet.md) however?

---

**Table of contents**

- [activatedgeek/LeNet-5 use ONNX for inference](activatedgeek-lenet-5-use-onnx-for-inference.md)
- [activatedgeek/LeNet-5 run on GPU](activatedgeek-lenet-5-run-on-gpu.md)
- [lenet](_file/lenet.md)

## ↑ Ancestors (13)

1. [LeNet implementation](lenet-implementation.md)
2. [LeNet](lenet.md)
3. [List of convolutional neural networks](list-of-convolutional-neural-networks.md)
4. [Convolutional neural network](convolutional-neural-network.md)
5. [ANN model](ann-model.md)
6. [Artificial neural network](artificial-neural-network.md)
7. [Neural network](neural-network.md)
8. [Machine learning](machine-learning-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [lenet](_file/lenet.md)
- [Activatedgeek/LeNet-5](activatedgeek-lenet-5.md)
- [CNN convolution kernels are also learnt](cnn-convolution-kernels-are-also-learnt.md)
- [MNIST database](mnist-database.md)
- [Netron](netron.md)
- [ONNX](onnx.md)
