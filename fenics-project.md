# FEniCS Project

↑ **Parent:** [Partial differential equation solver](partial-differential-equation-solver.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/FEniCS_Project)

[https://fenicsproject.org/](https://fenicsproject.org/)

One big advantage over [FreeFem](freefem.md) is that it uses plain old [Python](python-programming-language.md) to describe the problems instead of a [domain-specific language](domain-specific-language.md). [Matplotlib](matplotlib.md) is used for plotting by default, so we get full Python power out of the box!

Also uses [variational formulation of a partial differential equation](variational-formulation-of-a-partial-differential-equation.md) like [FreeFem](freefem.md) which is a pain.

One downside is that its documentation is a Springer published PDF [https://link.springer.com/content/pdf/10.1007%2F978-3-319-52462-7.pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-52462-7.pdf) which is several years out-of-date (tested with FEnics 2016.2. Newbs. This causes problems e.g.: [https://stackoverflow.com/questions/53730427/fenics-did-not-show-figure-nameerror-name-interactive-is-not-defined/57390687#57390687](https://stackoverflow.com/questions/53730427/fenics-did-not-show-figure-nameerror-name-interactive-is-not-defined/57390687#57390687)

[system of partial differential equations](system-of-partial-differential-equations.md) are mentioned at: [https://link.springer.com/content/pdf/10.1007%2F978-3-319-52462-7.pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-52462-7.pdf) 3.5 "A system of advection–diffusion–reaction equations". You don't need to manually iterate between the equations.

On Ubuntu 20.04 as per [https://fenicsproject.org/download/](https://fenicsproject.org/download/)
```
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:fenics-packages/fenics
sudo apt-get update
sudo apt-get install --no-install-recommends fenics
sudo apt install fenics
python3 -m pip install -u matplotlib
```
Before 2020-06, it was failing with:
```
E: The repository 'http://ppa.launchpad.net/fenics-packages/fenics/ubuntu focal Release' does not have a Release file.
```
but they seem to have created the Ubuntu 20.04 package as of 2020-06, so it now worked! [https://askubuntu.com/questions/866901/what-can-i-do-if-a-repository-ppa-does-not-have-a-release-file](https://askubuntu.com/questions/866901/what-can-i-do-if-a-repository-ppa-does-not-have-a-release-file)

TODO heat equation [hello world](hello-world-program.md).

**Table of contents**

- [Hans Petter Langtangen](hans-petter-langtangen.md)

## ↑ Ancestors (7)

1. [Partial differential equation solver](partial-differential-equation-solver.md)
2. [Partial differential equation](partial-differential-equation.md)
3. [Differential equation](differential-equation.md)
4. [Calculus](calculus-split.md)
5. [Area of mathematics](area-of-mathematics.md)
6. [Mathematics](mathematics-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [FreeFem](freefem.md)
- [Hans Petter Langtangen](hans-petter-langtangen.md)
- [Variational formulation of a partial differential equation](variational-formulation-of-a-partial-differential-equation.md)
