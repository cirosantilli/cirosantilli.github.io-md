# torchvision ResNet

↑ **Parent:** [torchvision](torchvision.md)

[https://pytorch.org/vision/0.13/models.html](https://pytorch.org/vision/0.13/models.html) has a minimal runnable example adapted to [python/pytorch/resnet_demo.py](python/pytorch/resnet_demo.py).

That example uses a [ResNet](residual-neural-network.md) pre-trained on the [COCO dataset](coco-dataset.md) to do some inference, tested on [Ubuntu 22.10](ubuntu-22-10.md):
```
cd python/pytorch
wget -O resnet_demo_in.jpg https://upload.wikimedia.org/wikipedia/commons/thumb/6/60/Rooster_portrait2.jpg/330px-Rooster_portrait2.jpg
./resnet_demo.py resnet_demo_in.jpg resnet_demo_out.jpg
```
This first downloads the model, which is currently 167 MB.

We know it is COCO because of the docs: [https://pytorch.org/vision/0.13/models/generated/torchvision.models.detection.fasterrcnn_resnet50_fpn_v2.html](https://pytorch.org/vision/0.13/models/generated/torchvision.models.detection.fasterrcnn_resnet50_fpn_v2.html) which explains that 
```
FasterRCNN_ResNet50_FPN_V2_Weights.DEFAULT
```
is an alias for:
```
FasterRCNN_ResNet50_FPN_V2_Weights.COCO_V1
```

The runtime is relatively slow on [P51](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md), about 4.7s.

After it finishes, the program prints the recognized classes:
```
['bird', 'banana']
```
so we get the expected `bird`, but also the more intriguing `banana`.

By looking at the output image with bounding boxes, we understand where the banana came from!

<a id="image-python-pytorch-resnet-demo-in-jpg"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/60/Rooster_portrait2.jpg/330px-Rooster_portrait2.jpg)

**[Figure 6](#image-python-pytorch-resnet-demo-in-jpg). python/pytorch/resnet\_demo\_in.jpg**. [Source](https://commons.wikimedia.org/wiki/File:Rooster_portrait2.jpg).

<a id="image-python-pytorch-resnet-demo-out-jpg"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/home/python/pytorch/resnet_demo_out.jpg)

**[Figure 7](#image-python-pytorch-resnet-demo-out-jpg). python/pytorch/resnet\_demo\_out.jpg**. The beak was of course a banana, not a beak!

## ↑ Ancestors (12)

1. [torchvision](torchvision.md)
2. [PyTorch](pytorch.md)
3. [Deep learning framework](deep-learning-framework.md)
4. [Deep learning](deep-learning.md)
5. [Artificial neural network](artificial-neural-network.md)
6. [Neural network](neural-network.md)
7. [Machine learning](machine-learning-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [ResNet implementation](resnet-implementation.md)
