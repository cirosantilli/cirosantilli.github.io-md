<h1 id="run-mlperf-v2-1-resnet-on-imagenette">Run MLperf v2.1 ResNet on Imagenette</h1>

↑ **Parent:** [MLperf v2.1 ResNet](mlperf-v2-1-resnet.md)

Let's run on this Imagenet10 subset called [Imagenette](imagenette.md).

First ensure that you get the dummy test data run working as per [MLperf v2.1 ResNet](mlperf-v2-1-resnet.md).

Next, in the `imagenette2` directory, first let's create a 224x224 scaled version of the inputs as required by the benchmark at [https://mlcommons.org/en/inference-datacenter-21/](https://mlcommons.org/en/inference-datacenter-21/):
```
#!/usr/bin/env bash
rm -rf val224x224
mkdir -p val224x224
for syndir in val/*: do
  syn="$(dirname $syndir)"
  for img in "$syndir"/*; do
    convert "$img" -resize 224x224 "val224x224/$syn/$(basename "$img")"
  done
done
```
and then let's create the `val_map.txt` file to match the format expected by MLPerf:
```
#!/usr/bin/env bash
wget https://gist.githubusercontent.com/aaronpolhamus/964a4411c0906315deb9f4a3723aac57/raw/aa66dd9dbf6b56649fa3fab83659b2acbf3cbfd1/map_clsloc.txt
i=0
rm -f val_map.txt
while IFS="" read -r p || [ -n "$p" ]; do
  synset="$(printf '%s\n' "$p" | cut -d ' ' -f1)"
  if [ -d "val224x224/$synset" ]; then
    for f in "val224x224/$synset/"*; do
      echo "$f $i" >> val_map.txt
    done
  fi
  i=$((i + 1))
done < <( sort map_clsloc.txt )
```
then back on the mlperf directory we download our model:
```
wget https://zenodo.org/record/4735647/files/resnet50_v1.onnx
```
and finally run!
```
DATA_DIR=/mnt/sda3/data/imagenet/imagenette2 time ./run_local.sh onnxruntime resnet50 cpu --accuracy
```
which gives on [P51](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md):
```
TestScenario.SingleStream qps=164.06, mean=0.0267, time=23.924, acc=87.134%, queries=3925, tiles=50.0:0.0264,80.0:0.0275,90.0:0.0287,95.0:0.0306,99.0:0.0401,99.9:0.0464
```
where `qps` presumably means "querries per second". And the `time` results:
```
446.78user 33.97system 2:47.51elapsed 286%CPU (0avgtext+0avgdata 964728maxresident)k
```
The `time=23.924` is much smaller than the `time` executable because of some lengthy pre-loading (TODO not sure what that means) that gets done every time:
```
INFO:imagenet:loaded 3925 images, cache=0, took=52.6sec
INFO:main:starting TestScenario.SingleStream
```

Let's try on the [GPU](graphics-processing-unit.md) now:
```
DATA_DIR=/mnt/sda3/data/imagenet/imagenette2 time ./run_local.sh onnxruntime resnet50 gpu --accuracy
```
which gives:
```
TestScenario.SingleStream qps=130.91, mean=0.0287, time=29.983, acc=90.395%, queries=3925, tiles=50.0:0.0265,80.0:0.0285,90.0:0.0405,95.0:0.0425,99.0:0.0490,99.9:0.0512
455.00user 4.96system 1:59.43elapsed 385%CPU (0avgtext+0avgdata 975080maxresident)k
```
TODO lower `qps` on GPU!

## ↑ Ancestors (12)

1. [MLperf v2.1 ResNet](mlperf-v2-1-resnet.md)
2. [MLperf](mlperf.md)
3. [Deep learning benchmark](deep-learning-benchmark.md)
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
