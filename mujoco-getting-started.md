# MuJoCo getting started

↑ **Parent:** [MuJoCo](mujoco.md)

Tested on [Ubuntu 23.10](ubuntu-23-10.md);
```
git clone https://github.com/google-deepmind/mujoco
cd mujoco
git checkout 5d46c39529819d1b31249e249ca399f306a108ac
mkdir -p build
cd build
cmake ..
make -j
```

Now let's play. Minimal interactive [UI](user-interface.md) simulation of a simple [MJCF](mjcf.md) scene with one falling cube:
```
bin/basic ../doc/_static/hello.xml
```
Test soure code: [https://github.com/google-deepmind/mujoco/blob/5d46c39529819d1b31249e249ca399f306a108ac/sample/basic.cc](https://github.com/google-deepmind/mujoco/blob/5d46c39529819d1b31249e249ca399f306a108ac/sample/basic.cc). The only thing you can do is [rotate](special-orthogonal-group.md) the scene with the [computer mouse](computer-mouse.md) it seems. Mentioned at: [https://mujoco.readthedocs.io/en/2.2.2/programming.html#sabasic](https://mujoco.readthedocs.io/en/2.2.2/programming.html#sabasic)

Some more interesting models can be found under the `model/` directory: [https://github.com/google-deepmind/mujoco/tree/5d46c39529819d1b31249e249ca399f306a108ac/model](https://github.com/google-deepmind/mujoco/tree/5d46c39529819d1b31249e249ca399f306a108ac/model) E.g. the imaginary humanoid robot [DeepMind](deepmind.md) used in many demos can be seen with:
```
bin/basic ../model/humanoid/humanoid.xml
```

A more advanced [UI](user-interface.md) with a few controls:
```
bin/simulate ../doc/_static/hello.xml
```
Test soure code: [https://github.com/google-deepmind/mujoco/tree/5d46c39529819d1b31249e249ca399f306a108ac/simulate](https://github.com/google-deepmind/mujoco/tree/5d46c39529819d1b31249e249ca399f306a108ac/simulate). Mentioned at: [https://mujoco.readthedocs.io/en/2.2.2/programming.html#sasimulate](https://mujoco.readthedocs.io/en/2.2.2/programming.html#sasimulate)

A very cool thing about that UI is that you can manually control joints. There are no joints in the hello.xml, but e.g. with the humanoid model:
```
bin/simulate ../model/humanoid/humanoid.xml
```
under "Control" you move each joint of the robot separately which is quite cool.

<a id="video-demo-of-mujoco-s-built-in-simulate-viewer-by-yuval-tassa-2019"></a>
**[Video 10](#video-demo-of-mujoco-s-built-in-simulate-viewer-by-yuval-tassa-2019). Demo of MuJoCo's built-in `simulate` viewer by Yuval Tassa (2019)** [Source](https://www.youtube.com/watch?v=0ORsj_E17B0).

There's also a `bin/record` test executable that presumably renders the simulation directly to a file:
```
bin/record ../doc/_static/hello.xml 5 60 rgb.out
ffmpeg -f rawvideo -pixel_format rgb24 -video_size 800x800 -framerate 60 -i rgb.out -vf "vflip" video.mp4
```
Mentioned at: [https://mujoco.readthedocs.io/en/2.2.2/programming.html#sarecord](https://mujoco.readthedocs.io/en/2.2.2/programming.html#sarecord) but TODO that produced a broken video, related issues:
- [https://github.com/google-deepmind/mujoco/issues/127](https://github.com/google-deepmind/mujoco/issues/127)
- [https://github.com/google-deepmind/mujoco/issues/824](https://github.com/google-deepmind/mujoco/issues/824)

## ↑ Ancestors (11)

1. [MuJoCo](mujoco.md)
2. [3D rigid body dynamics simulator](3d-rigid-body-dynamics-simulator.md)
3. [3D rigid body dynamics](3d-rigid-body-dynamics.md)
4. [Rigid body dynamics](rigid-body-dynamics.md)
5. [Rigid body](rigid-body.md)
6. [Point particle](point-particle.md)
7. [Mechanics](mechanics-split.md)
8. [Physics](physics-split.md)
9. [Natural science](natural-science.md)
10. [Science](science-split.md)
11. [Ciro Santilli's Homepage](split.md)
