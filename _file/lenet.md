<h1 id="_file/lenet">lenet</h1>

↑ **Parent:** [Activatedgeek/LeNet-5](../activatedgeek-lenet-5.md)

This is a small fork of [activatedgeek/LeNet-5](../activatedgeek-lenet-5.md) by [Ciro Santilli](../ciro-santilli-split.md) adding better integration and automation for:
- [extracting MNIST images](../extract-mnist-images.md) as [PNG](../portable-network-graphics.md)
- [ONNX](../onnx.md) CLI inference taking any image files as input
- a [Python `tkinter`](../python-tkinter.md) GUI that lets you draw and see inference live
- running on [GPU](../graphics-processing-unit.md)

Install on [Ubuntu 24.10](../ubuntu-24-10.md):
```
sudo apt install protobuf-compiler
cd lenet
virtualenv -p python3 .venv
. .venv/bin/activate
pip install -r requirements-python-3-12.txt
```

Download and extract [MNIST](../mnist-database.md) train, test accuracy, and generate the [ONNX](../onnx.md) `lenet.onnx`:
```
./train.py
```
[Extract MNIST images](../extract-mnist-images.md) as [PNG](../portable-network-graphics.md):
```
./extract_pngs.py
```
Infer some individual images using the [ONNX](../onnx.md):
```
./infer.py data/MNIST/png/test/0/*.png
```
Draw on a [GUI](../graphical-user-interface.md) and see live inference using the [ONNX](../onnx.md):
```
./draw.py
```
TODO: the following are missing for this to work:
- start a background task. This we know how to do: [https://stackoverflow.com/questions/1198262/tkinter-locks-python-when-an-icon-is-loaded-and-tk-mainloop-is-in-a-thread/79502287#79502287](https://stackoverflow.com/questions/1198262/tkinter-locks-python-when-an-icon-is-loaded-and-tk-mainloop-is-in-a-thread/79502287#79502287)
- get bytes from the canvas: all methods are ugly: [https://stackoverflow.com/questions/9886274/how-can-i-convert-canvas-content-to-an-image](https://stackoverflow.com/questions/9886274/how-can-i-convert-canvas-content-to-an-image)

## ↑ Ancestors (14)

1. [Activatedgeek/LeNet-5](../activatedgeek-lenet-5.md)
2. [LeNet implementation](../lenet-implementation.md)
3. [LeNet](../lenet.md)
4. [List of convolutional neural networks](../list-of-convolutional-neural-networks.md)
5. [Convolutional neural network](../convolutional-neural-network.md)
6. [ANN model](../ann-model.md)
7. [Artificial neural network](../artificial-neural-network.md)
8. [Neural network](../neural-network.md)
9. [Machine learning](../machine-learning-split.md)
10. [Computer](../computer-split.md)
11. [Information technology](../information-technology.md)
12. [Area of technology](../area-of-technology.md)
13. [Technology](../technology-split.md)
14. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (2)

- [Activatedgeek/LeNet-5](../activatedgeek-lenet-5.md)
- [Python `tkinter` image editor with image recognition](../python-tkinter-image-editor-with-image-recognition.md)
