# ImageNet

↑ **Parent:** [Computer vision dataset](computer-vision-dataset.md)  
🏷️ **Tags:** [Closed standard](closed-standard.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ImageNet)

14 million images with more than 20k categories, typically denoting prominent objects in the image, either common daily objects, or a wild range of animals. About 1 million of them also have [bounding boxes](bounding-box.md) for the objects. The images have different sizes, they are not all standardized to a single size like [MNIST](mnist-database.md)[https://stackoverflow.com/questions/36109886/what-is-the-resolution-of-an-image-in-imagenet-dataset](https://stackoverflow.com/questions/36109886/what-is-the-resolution-of-an-image-in-imagenet-dataset).

Each image appears to have a single label associated to it. Care must have been taken somehow with categories, since some images contain severl possible objects, e.g. a person and some object.

In practice, the [ILSVRC](imagenet-large-scale-visual-recognition-challenge-dataset.md) subset of [ImageNet](imagenet.md) is the most commonly used dataset.

Official project page: [https://www.image-net.org/](https://www.image-net.org/)

The data license is restrictive and forbids commercial usage: [https://www.image-net.org/download.php](https://www.image-net.org/download.php). Also as a result you have to login to download the dataset. Super annoying.

How to visualize: [https://datascience.stackexchange.com/questions/111756/where-can-i-view-the-imagenet-classes-as-a-hierarchy-on-wordnet](https://datascience.stackexchange.com/questions/111756/where-can-i-view-the-imagenet-classes-as-a-hierarchy-on-wordnet)

The categories are all part of [WordNet](wordnet.md), which means that there are several parent/child categories such as dog vs type of dog available. [ImageNet1k](imagenet-large-scale-visual-recognition-challenge-dataset.md) only appears to have leaf nodes however (i.e. no "dog" label, just specific types of dog).

A major model that performed well on [ImageNet](imagenet.md) starting on 2012 and became notable is [AlexNet](alexnet.md).

**Table of contents**

- [Fei-Fei Li](fei-fei-li.md)
- [ImageNet subset](imagenet-subset.md)
  - [Imagenette](imagenette.md)
  - [ImageNet Large Scale Visual Recognition Challenge dataset](imagenet-large-scale-visual-recognition-challenge-dataset.md)
- [ImageNet1k download](imagenet1k-download.md)
- [ImageNet competition](imagenet-competition.md)
  - [ImageNet 2015](imagenet-2015.md)

## ↑ Ancestors (8)

1. [Computer vision dataset](computer-vision-dataset.md)
2. [Computer vision](computer-vision.md)
3. [Machine learning](machine-learning-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (8)

- [AlexNet](alexnet.md)
- [CIFAR-10](cifar-10.md)
- [ImageNet](imagenet.md)
- [ImageNet Large Scale Visual Recognition Challenge dataset](imagenet-large-scale-visual-recognition-challenge-dataset.md)
- [ImageNet subset](imagenet-subset.md)
- [MLperf](mlperf.md)
- [MLperf v2.1 ResNet](mlperf-v2-1-resnet.md)
- [MNIST database](mnist-database.md)
