# ImageNet1k download

↑ **Parent:** [ImageNet](imagenet.md)

The official page: [https://www.image-net.org/challenges/LSVRC/index.php](https://www.image-net.org/challenges/LSVRC/index.php) points to a download link on [Kaggle](kaggle.md): [https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data](https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data) Kaggle says that the size is 167.62 GB!

To download from Kaggle, create an API token on kaggle.com, which downloads a `kaggle.json` file then:
```
mkdir -p ~/.kaggle
mv ~/down/kaggle.json ~/.kaggle
python3 -m pip install kaggle
kaggle competitions download -c imagenet-object-localization-challenge
```
The download speed is wildly server/limited and take A LOT of hours. Also, the tool does not seem able to pick up where you stopped last time.

Another download location appears to be: [https://huggingface.co/datasets/imagenet-1k](https://huggingface.co/datasets/imagenet-1k) on [Hugging Face](hugging-face.md), but you have to login due to their license terms. Once you login you have a very basic data explorer available: [https://huggingface.co/datasets/imagenet-1k/viewer/default/train](https://huggingface.co/datasets/imagenet-1k/viewer/default/train).

Bibliography:
- [http://www.adeveloperdiary.com/data-science/computer-vision/how-to-prepare-imagenet-dataset-for-image-classification/](http://www.adeveloperdiary.com/data-science/computer-vision/how-to-prepare-imagenet-dataset-for-image-classification/)
- [https://stackoverflow.com/questions/65685437/access-to-imagenet-data-download](https://stackoverflow.com/questions/65685437/access-to-imagenet-data-download)

## ↑ Ancestors (9)

1. [ImageNet](imagenet.md)
2. [Computer vision dataset](computer-vision-dataset.md)
3. [Computer vision](computer-vision.md)
4. [Machine learning](machine-learning-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
