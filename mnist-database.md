# MNIST database

↑ **Parent:** [Computer vision dataset](computer-vision-dataset.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/MNIST_database)

70,000 28x28 grayscale (1 byte per pixel) images of hand-written digits 0-9, i.e. 10 categories. 60k are considered [training data](training-data-set.md), 10k are considered for [test data](test-data-set.md).

This is THE "[OG](original-gangster.md)" [computer vision dataset](computer-vision-dataset.md).

Playing with it is the de-facto [computer vision](computer-vision.md) [hello world](hello-world-program.md).

It was on this dataset that [Yann LeCun](yann-lecun.md) made great progress with the [LeNet](lenet.md) model. Running [LeNet](lenet.md) on [MNIST](mnist-database.md) has to be the most classic computer vision thing ever. See e.g. [activatedgeek/LeNet-5](activatedgeek-lenet-5.md) for a minimal and modern [PyTorch](pytorch.md) educational implementation.

But it is important to note that as of the 2010's, the benchmark had become too easy for many applications. It is perhaps fair to say that the next big dataset revolution of the same importance was with [ImageNet](imagenet.md).

The dataset could be downloaded from [http://yann.lecun.com/exdb/mnist/](http://yann.lecun.com/exdb/mnist/) but as of March 2025 it was down and seems to have broken from time to time randomly, so [Wayback Machine](wayback-machine.md) to the rescue:
```
wget \
 https://web.archive.org/web/20120828222752/http://yann.lecun.com/exdb/mnist/train-images-idx3-ubyte.gz \
 https://web.archive.org/web/20120828182504/http://yann.lecun.com/exdb/mnist/train-labels-idx1-ubyte.gz \
 https://web.archive.org/web/20240323235739/http://yann.lecun.com/exdb/mnist/t10k-images-idx3-ubyte.gz \
 https://web.archive.org/web/20240328174015/http://yann.lecun.com/exdb/mnist/t10k-labels-idx1-ubyte.gz
```
but doing so is kind of pointless as both files use some crazy single-file custom binary format to store all images and labels. OMG!

OK-ish data explorer: [https://knowyourdata-tfds.withgoogle.com/#tab=STATS&dataset=mnist](https://knowyourdata-tfds.withgoogle.com/#tab=STATS&dataset=mnist)

<a id="image-mnist-image-1-of-a-0"></a>
![](http://web.archive.org/web/20230430064700im_/https://i.stack.imgur.com/7q9Zg.png)

**[Figure 8](#image-mnist-image-1-of-a-0). MNIST image 1 of a '0'**.

<a id="image-mnist-image-21-of-a-0"></a>
![](http://web.archive.org/web/20230430064700im_/https://i.stack.imgur.com/RemMm.png)

**[Figure 9](#image-mnist-image-21-of-a-0). MNIST image 21 of a '0'**.

<a id="image-mnist-image-3-of-a-1"></a>
![](http://web.archive.org/web/20230430064700im_/https://i.stack.imgur.com/qoTGE.png)

**[Figure 10](#image-mnist-image-3-of-a-1). MNIST image 3 of a '1'**.

**Table of contents**

- [Extract MNIST images](extract-mnist-images.md)
- [Best algorithm for MNIST](best-algorithm-for-mnist.md)
- [Fashion MNIST](fashion-mnist.md)

## ↑ Ancestors (8)

1. [Computer vision dataset](computer-vision-dataset.md)
2. [Computer vision](computer-vision.md)
3. [Machine learning](machine-learning-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
