# MLperf

↑ **Parent:** [Deep learning benchmark](deep-learning-benchmark.md)

[https://mlcommons.org/en/](https://mlcommons.org/en/) Their homepage is not amazingly organized, but it does the job.

Benchmark focused on [deep learning](deep-learning.md). It has two parts:
- [training](training-ml.md): produces a trained network
- [inference](inference-ml.md): uses the trained network
Furthermore, a specific network model is specified for each benchmark in the closed category: so it goes beyond just specifying the dataset.

Results can be seen e.g. at:
- [training](training-ml.md): [https://mlcommons.org/en/training-normal-21/](https://mlcommons.org/en/training-normal-21/) ([archive](https://web.archive.org/web/20230923035847/https://mlcommons.org/en/training-normal-21/))
- [inference](inference-ml.md): [https://mlcommons.org/en/inference-datacenter-21/](https://mlcommons.org/en/inference-datacenter-21/) ([https://web.archive.org/web/20230923030959/https://mlcommons.org/en/inference-datacenter-21/)](https://web.archive.org/web/20230923030959/https://mlcommons.org/en/inference-datacenter-21/))
Those URLs broke as of 2025 of course, now you have to click on their Tableau down to the 2.1 round and there's no fixed URL for it:
- [https://mlcommons.org/benchmarks/training/](https://mlcommons.org/benchmarks/training/)
- [https://mlcommons.org/benchmarks/inference-datacenter/](https://mlcommons.org/benchmarks/inference-datacenter/)

And there are also separate repositories for each:
- [https://github.com/mlcommons/inference](https://github.com/mlcommons/inference)
- [https://github.com/mlcommons/training](https://github.com/mlcommons/training)

E.g. on [https://mlcommons.org/en/training-normal-21/](https://mlcommons.org/en/training-normal-21/) we can see what the the benchmarks are:

| Dataset | Model |
| --- | --- |
| [ImageNet](imagenet.md) | [ResNet](residual-neural-network.md) |
| KiTS19 | 3D U-Net |
| [OpenImages](open-images-dataset.md) | RetinaNet |
| [COCO dataset](coco-dataset.md) | Mask R-CNN |
| LibriSpeech | RNN-T |
| Wikipedia | BERT |
| 1TB Clickthrough | DLRM |
| [Go](go-game.md) | [MiniGo](minigo.md) |

**Table of contents**

- [MLperf v2.1 ResNet](mlperf-v2-1-resnet.md)
  - [Run MLperf v2.1 ResNet on Imagenette](run-mlperf-v2-1-resnet-on-imagenette.md)

## ↑ Ancestors (10)

1. [Deep learning benchmark](deep-learning-benchmark.md)
2. [Deep learning](deep-learning.md)
3. [Artificial neural network](artificial-neural-network.md)
4. [Neural network](neural-network.md)
5. [Machine learning](machine-learning-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Cerebras](cerebras.md)
