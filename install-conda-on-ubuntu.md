# Install Conda on Ubuntu

↑ **Parent:** [Conda](conda.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Install_Conda_on_Ubuntu)

Tested on [Ubuntu 20.04](ubuntu-20-04.md):
```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```
Add to your `.bashrc`:
```
PATH="$PATH:$HOME/miniconda3/bin"
```
and then to use it on a shell e.g. with Python 3.9 create the environment with:
```
conda create -y -n mytest3.9 python=3.9
```
and then use it with:
```
eval "$(command conda 'shell.bash' 'hook' 2> /dev/null)"
conda activate mytest3.9
```
Now you can use `python` and `pip` normally from inside that `mytest3.9` environment.

At that time, the exact installer under `latest` appears to have been: [https://repo.anaconda.com/miniconda/Miniconda3-py311_23.11.0-2-Linux-x86_64.sh](https://repo.anaconda.com/miniconda/Miniconda3-py311_23.11.0-2-Linux-x86_64.sh)

## ↑ Ancestors (11)

1. [Conda](conda.md)
2. [Python package manager](python-package-manager.md)
3. [Python (programming language)](python-programming-language.md)
4. [List of programming languages](list-of-programming-languages.md)
5. [Programming language](programming-language-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [runwayml/stable-diffusion](runwayml-stable-diffusion.md)
