<h1 id="activatedgeek-lenet-5-use-onnx-for-inference">activatedgeek/LeNet-5 use ONNX for inference</h1>

↑ **Parent:** [Activatedgeek/LeNet-5](activatedgeek-lenet-5.md)

Now let's try and use the trained [ONNX](onnx.md) file for inference on some manually drawn images on [GIMP](gimp.md):

<a id="image-number-9-drawn-with-mouse-on-gimp-by-ciro-santilli-2023"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/Digit_9_hand_drawn_by_Ciro_Santilli_on_GIMP_with_mouse_white_on_black.png)

**[Figure 4](#image-number-9-drawn-with-mouse-on-gimp-by-ciro-santilli-2023). Number 9 drawn with mouse on GIMP by Ciro Santilli (2023)**

Note that:
- the images must be drawn with white on black. If you use black on white, it the accuracy becomes terrible. This is a good very example of [brittleness in AI](ai-brittleness.md) systems!
- images must be converted to 32x32 for `lenet.onnx`, as that is what training was done on. The training step converted the 28x28 images to 32x32 as the first thing it does before training even starts

We can try the code adapted from [https://thenewstack.io/tutorial-using-a-pre-trained-onnx-model-for-inferencing/](https://thenewstack.io/tutorial-using-a-pre-trained-onnx-model-for-inferencing/) at [lenet/infer.py](lenet/infer.py):
```
cd lenet
cp ~/git/LeNet-5/lenet.onnx .
wget -O 9.png https://raw.githubusercontent.com/cirosantilli/media/master/Digit_9_hand_drawn_by_Ciro_Santilli_on_GIMP_with_mouse_white_on_black.png
./infer.py 9.png
```
and it works pretty well! The program outputs:
```
9
```
as desired.

We can also try with images directly from [Extract MNIST images](extract-mnist-images.md).
```
infer_mnist.py lenet.onnx mnist_png/out/testing/1/*.png
```
and the accuracy is great as expected.

## ↑ Ancestors (14)

1. [Activatedgeek/LeNet-5](activatedgeek-lenet-5.md)
2. [LeNet implementation](lenet-implementation.md)
3. [LeNet](lenet.md)
4. [List of convolutional neural networks](list-of-convolutional-neural-networks.md)
5. [Convolutional neural network](convolutional-neural-network.md)
6. [ANN model](ann-model.md)
7. [Artificial neural network](artificial-neural-network.md)
8. [Neural network](neural-network.md)
9. [Machine learning](machine-learning-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)
