<h1 id="mlperf-v2-1-resnet">MLperf v2.1 ResNet</h1>

↑ **Parent:** [MLperf](mlperf.md)  
🏷️ **Tags:** [ResNet](residual-neural-network.md)

Instructions at:
- [https://github.com/mlcommons/inference/blob/v2.1/vision/classification_and_detection](https://github.com/mlcommons/inference/blob/v2.1/vision/classification_and_detection)
- [https://github.com/mlcommons/inference/blob/v2.1/vision/classification_and_detection/GettingStarted.ipynb](https://github.com/mlcommons/inference/blob/v2.1/vision/classification_and_detection/GettingStarted.ipynb)

[Ubuntu 22.10](ubuntu-22-10.md) setup with tiny dummy manually generated [ImageNet](imagenet.md) and run on [ONNX](onnx.md):
```
sudo apt install pybind11-dev

git clone https://github.com/mlcommons/inference
cd inference
git checkout v2.1

virtualenv -p python3 .venv
. .venv/bin/activate
pip install numpy==1.24.2 pycocotools==2.0.6 onnxruntime==1.14.1 opencv-python==4.7.0.72 torch==1.13.1

cd loadgen
CFLAGS="-std=c++14" python setup.py develop
cd -

cd vision/classification_and_detection
python setup.py develop
wget -q https://zenodo.org/record/3157894/files/mobilenet_v1_1.0_224.onnx
export MODEL_DIR="$(pwd)"
export EXTRA_OPS='--time 10 --max-latency 0.2'

tools/make_fake_imagenet.sh
DATA_DIR="$(pwd)/fake_imagenet" ./run_local.sh onnxruntime mobilenet cpu --accuracy
```

Last line of output on [P51](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md), which appears to contain the benchmark results
```
TestScenario.SingleStream qps=58.85, mean=0.0138, time=0.136, acc=62.500%, queries=8, tiles=50.0:0.0129,80.0:0.0137,90.0:0.0155,95.0:0.0171,99.0:0.0184,99.9:0.0187
```
where presumably `qps` means queries per second, and is the main results we are interested in, the more the better.

Running:
```
tools/make_fake_imagenet.sh
```
produces a tiny [ImageNet subset](imagenet-subset.md) with 8 images under `fake_imagenet/`.

`fake_imagenet/val_map.txt` contains:
```
val/800px-Porsche_991_silver_IAA.jpg 817
val/512px-Cacatua_moluccensis_-Cincinnati_Zoo-8a.jpg 89
val/800px-Sardinian_Warbler.jpg 13
val/800px-7weeks_old.JPG 207
val/800px-20180630_Tesla_Model_S_70D_2015_midnight_blue_left_front.jpg 817
val/800px-Welsh_Springer_Spaniel.jpg 156
val/800px-Jammlich_crop.jpg 233
val/782px-Pumiforme.JPG 285
```
where the numbers are the category indices from [ImageNet1k](imagenet-large-scale-visual-recognition-challenge-dataset.md). At [https://gist.github.com/yrevar/942d3a0ac09ec9e5eb3a](https://gist.github.com/yrevar/942d3a0ac09ec9e5eb3a) see e.g.:
- 817: 'sports car, sport car',
- 89: 'sulphur-crested cockatoo, Kakatoe galerita, Cacatua galerita',
and so on, so they are coherent with the image names. By quickly looking at the script we see that it just downloads from Wikimedia and manually creates the file.

TODO prepare and test on the actual [ImageNet](imagenet.md) validation set, README says:

> Prepare the imagenet dataset to come.

Since that one is undocumented, let's try the [COCO dataset](coco-dataset.md) instead, which uses [COCO 2017](coco-2017.md) and is also a bit smaller. Note that his is not part of MLperf anymore since v2.1, only [ImageNet](imagenet.md) and open images are used. But still:
```
wget https://zenodo.org/record/4735652/files/ssd_mobilenet_v1_coco_2018_01_28.onnx
DATA_DIR_BASE=/mnt/data/coco
export DATA_DIR="${DATADIR_BASE}/val2017-300"
mkdir -p "$DATA_DIR_BASE"
cd "$DATA_DIR_BASE"
wget http://images.cocodataset.org/zips/val2017.zip
wget http://images.cocodataset.org/annotations/annotations_trainval2017.zip
unzip val2017.zip
unzip annotations_trainval2017.zip
mv annotations val2017
cd -
cd "$(git-toplevel)"
python tools/upscale_coco/upscale_coco.py --inputs "$DATA_DIR_BASE" --outputs "$DATA_DIR" --size 300 300 --format png
cd -
```

Now:
```
./run_local.sh onnxruntime mobilenet cpu --accuracy
```
fails immediately with:
```
No such file or directory: '/path/to/coco/val2017-300/val_map.txt
```
The more plausible looking:
```
./run_local.sh onnxruntime mobilenet cpu --accuracy --dataset coco-300
```
first takes a while to preprocess something most likely, which it does only one, and then fails:
```
Traceback (most recent call last):
  File "/home/ciro/git/inference/vision/classification_and_detection/python/main.py", line 596, in <module>
    main()
  File "/home/ciro/git/inference/vision/classification_and_detection/python/main.py", line 468, in main
    ds = wanted_dataset(data_path=args.dataset_path,
  File "/home/ciro/git/inference/vision/classification_and_detection/python/coco.py", line 115, in __init__
    self.label_list = np.array(self.label_list)
ValueError: setting an array element with a sequence. The requested array has an inhomogeneous shape after 2 dimensions. The detected shape was (5000, 2) + inhomogeneous part.
```

TODO!

**Table of contents**

- [Run MLperf v2.1 ResNet on Imagenette](run-mlperf-v2-1-resnet-on-imagenette.md)

## ↑ Ancestors (11)

1. [MLperf](mlperf.md)
2. [Deep learning benchmark](deep-learning-benchmark.md)
3. [Deep learning](deep-learning.md)
4. [Artificial neural network](artificial-neural-network.md)
5. [Neural network](neural-network.md)
6. [Machine learning](machine-learning-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [COCO 2017](coco-2017.md)
- [ONNX](onnx.md)
- [ResNet implementation](resnet-implementation.md)
- [Run MLperf v2.1 ResNet on Imagenette](run-mlperf-v2-1-resnet-on-imagenette.md)
