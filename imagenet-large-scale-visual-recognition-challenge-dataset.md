# ImageNet Large Scale Visual Recognition Challenge dataset

↑ **Parent:** [ImageNet subset](imagenet-subset.md)

Subset of [ImageNet](imagenet.md). About 167.62 GB in size according to [https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data](https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data).

Contains 1,281,167 images and exactly 1k categories which is why this dataset is also known as ImageNet1k: [https://datascience.stackexchange.com/questions/47458/what-is-the-difference-between-imagenet-and-imagenet1k-how-to-download-it](https://datascience.stackexchange.com/questions/47458/what-is-the-difference-between-imagenet-and-imagenet1k-how-to-download-it)

[https://www.kaggle.com/competitions/imagenet-object-localization-challenge/overview](https://www.kaggle.com/competitions/imagenet-object-localization-challenge/overview) clarifies a bit further how the categories are inter-related according to [WordNet](wordnet.md) relationships:

> The 1000 object categories contain both internal nodes and leaf nodes of ImageNet, but do not overlap with each other.

[https://image-net.org/challenges/LSVRC/2012/browse-synsets.php](https://image-net.org/challenges/LSVRC/2012/browse-synsets.php) lists all 1k labels with their [WordNet](wordnet.md) IDs.
```
n02119789: kit fox, Vulpes macrotis
n02100735: English setter
n02096294: Australian terrier
```
There is a bug on that page however towards the middle:
```
n03255030: dumbbell
href="ht:
n02102040: English springer, English springer spaniel
```
and there is one missing label if we ignore that dummy `href=` line. A thinkg of beauty!

Also the lines are not sorted by synset, if we do then the first three lines are:
```
n01440764: tench, Tinca tinca
n01443537: goldfish, Carassius auratus
n01484850: great white shark, white shark, man-eater, man-eating shark, Carcharodon carcharias
```

[https://gist.github.com/aaronpolhamus/964a4411c0906315deb9f4a3723aac57](https://gist.github.com/aaronpolhamus/964a4411c0906315deb9f4a3723aac57) has lines of type:
```
n02119789 1 kit_fox
n02100735 2 English_setter
n02110185 3 Siberian_husky
```
therefore numbered on the exact same order as [https://image-net.org/challenges/LSVRC/2012/browse-synsets.php](https://image-net.org/challenges/LSVRC/2012/browse-synsets.php)

[https://gist.github.com/yrevar/942d3a0ac09ec9e5eb3a](https://gist.github.com/yrevar/942d3a0ac09ec9e5eb3a) lists all 1k labels as a plaintext file with their benchmark IDs.
```
{0: 'tench, Tinca tinca',
 1: 'goldfish, Carassius auratus',
 2: 'great white shark, white shark, man-eater, man-eating shark, Carcharodon carcharias',
```
therefore numbered on sorted order of [https://image-net.org/challenges/LSVRC/2012/browse-synsets.php](https://image-net.org/challenges/LSVRC/2012/browse-synsets.php)

The official line numbering in-benchmark-data can be seen at `LOC_synset_mapping.txt`, e.g. [https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data?select=LOC_synset_mapping.txt](https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data?select=LOC_synset_mapping.txt)
```
n01440764 tench, Tinca tinca
n01443537 goldfish, Carassius auratus
n01484850 great white shark, white shark, man-eater, man-eating shark, Carcharodon carcharias
```

[https://huggingface.co/datasets/imagenet-1k](https://huggingface.co/datasets/imagenet-1k) also has some useful metrics on the split:
- train: 1,281,167 images, 145.7 GB zipped
- validation: 50,000 images, 6.67 GB zipped
- test: 100,000 images, 13.5 GB zipped

## ↑ Ancestors (10)

1. [ImageNet subset](imagenet-subset.md)
2. [ImageNet](imagenet.md)
3. [Computer vision dataset](computer-vision-dataset.md)
4. [Computer vision](computer-vision.md)
5. [Machine learning](machine-learning-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
