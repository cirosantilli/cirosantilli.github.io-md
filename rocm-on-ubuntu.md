# ROCm on Ubuntu

↑ **Parent:** [ROCm](rocm.md)

Tested on [Ubuntu 23.10](ubuntu-23-10.md) with [P14s](ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md):
```
sudo apt install hipcc
git clone https://github.com/ROCm/HIP-Examples
cd HIP-Examples/HIP-Examples-Applications/HelloWorld
make
```
TODO fails with:
```
/bin/hipcc -g   -c -o HelloWorld.o HelloWorld.cpp
clang: error: cannot find ROCm device library for gfx1103; provide its path via '--rocm-path' or '--rocm-device-lib-path', or pass '-nogpulib' to build without ROCm device library
make: *** [<builtin>: HelloWorld.o] Error 1
```

Generic Ubuntu install bibliograpy:
- [https://askubuntu.com/questions/1429376/how-can-i-install-amd-rocm-5-on-ubuntu-22-04](https://askubuntu.com/questions/1429376/how-can-i-install-amd-rocm-5-on-ubuntu-22-04)
- [https://www.reddit.com/r/ROCm/comments/1438p6t/how_to_install_rocm_opencl_on_ubuntu_2304_rx580/](https://www.reddit.com/r/ROCm/comments/1438p6t/how_to_install_rocm_opencl_on_ubuntu_2304_rx580/)

## ↑ Ancestors (13)

1. [ROCm](rocm.md)
2. [GPU compute library](gpu-compute-library.md)
3. [General-purpose computing on graphics processing units](general-purpose-computing-on-graphics-processing-units.md)
4. [Graphics processing unit](graphics-processing-unit.md)
5. [Type of processor](type-of-processor.md)
6. [Processor (computing)](processor-computing.md)
7. [Computer hardware component type](computer-hardware-component-type.md)
8. [Computer hardware](computer-hardware-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)
