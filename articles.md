# The best articles by Ciro Santilli

↑ **Parent:** [Ciro Santilli](ciro-santilli.md)

These are the best articles ever authored by [Ciro Santilli](ciro-santilli.md), most of them in the format of [Stack Overflow](stack-overflow.md) answers.

Ciro posts update about new articles [on his Twitter accounts](accounts.md#ciro-santilli-s-twitter-accounts).

A chronological list of all articles is also kept at: [Section "Updates"](updates.md).

Some random generally less technical in-tree essays will be present at: [Section "Essays by Ciro Santilli"](ciro-santilli.md#essays-by-ciro-santilli).

- Trended on [Hacker News](website.md#hacker-news):
  - [CIA 2010 covert communication websites](cia-2010-covert-communication-websites.md) on [2023-06-11](https://news.ycombinator.com/item?id=36279375). 190 points, a mild success.
  - [x86 Bare Metal Examples](https://github.com/cirosantilli/x86-bare-metal-examples) on [2019-03-19](https://news.ycombinator.com/item?id=19428700). 513 points. The third time something related to that repo trends. Hacker news people really like that repo!
    - again [2020-06-27](https://news.ycombinator.com/item?id=27654257) ([archive](https://web.archive.org/web/20210627201918/https://news.ycombinator.com/)). 200 points, repository traffic jumped from 25 daily unique visitors to 4.6k unique visitors on the day
  - [How to run a program without an operating system?](https://stackoverflow.com/questions/22054578/how-to-run-a-program-without-an-operating-system/32483545#32483545) on [2018-11-26](https://news.ycombinator.com/item?id=18531393) ([archive](https://web.archive.org/web/20181126123625/https://news.ycombinator.com)).	394 points. Covers x86 and ARM
  - [ELF Hello World Tutorial](elf-hello-world.md) on [2017-05-17](https://news.ycombinator.com/item?id=14359159) ([archive](https://web.archive.org/web/20170517174951/https://news.ycombinator.com/news)). 334 points.
  - [x86 Paging Tutorial](x86-paging.md) on [2017-03-02](https://news.ycombinator.com/item?id=13773219). Number 1 [Google](google.md) search result for "x86 Paging" [in 2017-08](https://archive.is/VUSNt). 142 points.

    <a id="image-bios-bare-metal-hello-world-running-on-a-lenovo-thinkpad-t430"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/BIOS_bare_metal_hello_world_running_on_a_Lenovo_ThinkPad_T430.jpg" alt="" height="500">

    **[Figure 1](#image-bios-bare-metal-hello-world-running-on-a-lenovo-thinkpad-t430). BIOS bare metal hello world running on a Lenovo ThinkPad T430**. [Source](https://stackoverflow.com/questions/22054578/how-to-run-a-program-without-an-operating-system/32483545\#32483545).
- [x86](computer-hardware.md#x86) [assembly](computer-hardware.md#assembly-language)
  - [What does "multicore" assembly language look like?](https://stackoverflow.com/questions/980999/what-does-multicore-assembly-language-look-like/33651438#33651438)
  - [What is the function of the push / pop instructions used on registers in x86 assembly?](https://stackoverflow.com/questions/4584089/what-is-the-function-of-the-push-pop-instructions-used-on-registers-in-x86-ass/33583134#33583134) Going down to memory spills, register allocation and graph coloring.
- [Linux kernel](systems-programming.md#linux-kernel)
  - [What do the flags in /proc/cpuinfo mean?](https://unix.stackexchange.com/a/219674/32558)
  - [How does kernel get an executable binary file running under linux?](https://stackoverflow.com/a/31394861/895245)
  - [How to debug the Linux kernel with GDB and QEMU?](https://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu/33203642#33203642)
  - [Can the sys\_execve() system call in the Linux kernel receive both absolute or relative paths?](https://stackoverflow.com/questions/33852690/can-the-sys-execve-system-call-in-the-linux-kernel-receive-both-absolute-or-re/42290593#42290593)
  - [What is the difference between the kernel space and the user space?](https://stackoverflow.com/questions/5957570/what-is-the-difference-between-the-kernel-space-and-the-user-space/44285809#44285809)
  - [Is there any API for determining the physical address from virtual address in Linux?](https://stackoverflow.com/questions/5748492/is-there-any-api-for-determining-the-physical-address-from-virtual-address-in-li/45128487#45128487)
  - [Why do people write the `#!/usr/bin/env` python shebang on the first line of a Python script?](https://stackoverflow.com/questions/2429511/why-do-people-write-the-usr-bin-env-python-shebang-on-the-first-line-of-a-pyt/40938801#40938801)
  - [How to solve "Kernel Panic - not syncing: VFS: Unable to mount root fs on unknown-block(0,0)"?](https://askubuntu.com/questions/41930/kernel-panic-not-syncing-vfs-unable-to-mount-root-fs-on-unknown-block0-0/1048477#1048477)
  - <a id="image-path-from-init-main-c-until-bzimage-in-the-linux-kernel-4-19"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/Path_from_init_main.c_until_bzImage_in_the_Linux_kernel_4.19.jpg" alt="" height="800">

    **[Figure 2](#image-path-from-init-main-c-until-bzimage-in-the-linux-kernel-4-19). Path from init/main.c until bzImage in the Linux kernel 4.19**. [Source](https://unix.stackexchange.com/questions/5518/what-is-the-difference-between-the-following-kernel-makefile-terms-vmlinux-vml/482978\#482978). From: [What is the difference between the following kernel Makefile terms: vmLinux, vmlinuz, vmlinux.bin, zimage & bzimage?](https://unix.stackexchange.com/questions/5518/what-is-the-difference-between-the-following-kernel-makefile-terms-vmlinux-vml/482978#482978)
  - Single program [Linux distro](systems-programming.md#linux-distribution)
    - [Is it possible to install the linux kernel alone?](https://unix.stackexchange.com/questions/17122/is-it-possible-to-install-the-linux-kernel-alone/200572#200572)
    - <img src="https://raw.githubusercontent.com/cirosantilli/media/master/End_of_Linux_boot_log_with_minimal_init_that_prints_FOOBAR.png" alt="" height="500">

      **[Figure 3](#_35)** [Source](https://unix.stackexchange.com/questions/122717/how-to-create-a-custom-linux-distro-that-runs-just-one-program-and-nothing-else/238579\#238579). From: [How to create a custom Linux distro that runs just one program and nothing else?](https://unix.stackexchange.com/questions/122717/how-to-create-a-custom-linux-distro-that-runs-just-one-program-and-nothing-else/238579#238579)
- [QEMU](systems-programming.md#qemu)
  - [How to add a new device in QEMU source code?](https://stackoverflow.com/questions/28315265/how-to-add-a-new-device-in-qemu-source-code/44612957#44612957)
  - [How to generate Ubuntu `debootstrap` disk images for QEMU?](https://askubuntu.com/questions/281763/is-there-any-prebuilt-qemu-ubuntu-image32bit-online/1081171#1081171)
  - [How to create a multi partition SD disk image without root privileges?](https://stackoverflow.com/questions/10949169/how-to-create-a-multi-partition-sd-image-without-root-privileges/52850819#52850819)
  - <a id="image-ubuntu-18-04-running-inside-qemu"></a>
    <img src="https://web.archive.org/web/20230325005127im_/https://i.stack.imgur.com/IPUkA.png" alt="" height="400">

    **[Figure 4](#image-ubuntu-18-04-running-inside-qemu). Ubuntu 18.04 running inside QEMU**. [Source](https://askubuntu.com/questions/884534/how-to-run-ubuntu-desktop-on-qemu/1046792\#1046792). From: [How to run Ubuntu desktop on QEMU?](https://askubuntu.com/questions/884534/how-to-run-ubuntu-desktop-on-qemu/1046792#1046792)
- [gcc](software.md#gnu-compiler-collection) and [Binutils](software.md#binutils):
  - [How do linkers and address relocation works?](https://stackoverflow.com/questions/3322911/what-do-linkers-do/33690144#33690144)
  - [What is incremental linking or partial linking?](https://stackoverflow.com/questions/29391965/what-is-partial-linking-in-gnu-linker/53959624#53959624)
  - [GOLD (`-fuse-ld=gold`) linker vs the traditional GNU ld and LLVM ldd](https://stackoverflow.com/questions/3476093/replacing-ld-with-gold-any-experience/53921263#53921263)
  - [What is the -fPIE option for position-independent executables in GCC and ld?](https://stackoverflow.com/questions/2463150/what-is-the-fpie-option-for-position-independent-executables-in-gcc-and-ld/51308031#51308031) Concrete examples by running program through [GDB](software.md#gnu-debugger) twice, and an assembly hello world with absolute vs PC relative load.
  - [How many GCC optimization levels are there?](https://stackoverflow.com/a/30308151/895245)
  - [Why does GCC create a shared object instead of an executable binary according to file?](https://stackoverflow.com/questions/34519521/why-does-gcc-create-a-shared-object-instead-of-an-executable-binary-according-to/55704865#55704865)
- [C](programming-language.md#c-programming-language)/[C++](programming-language.md#c-plus-plus): almost all of those fall into "disassemble [all the things](https://knowyourmeme.com/memes/all-the-things)" category. Ciro also does "standards dissection" and "a new version of the standard is out" answers, but those are boring:
  - [What does "static" mean in a C program?](https://stackoverflow.com/questions/572547/what-does-static-mean-in-a-c-program/14339047#14339047)
  - [In C++ source, what is the effect of `extern "C"`?](https://stackoverflow.com/questions/1041866/in-c-source-what-is-the-effect-of-extern-c/30526795#30526795)
  - [Char array vs Char Pointer in C](https://stackoverflow.com/questions/10186765/char-array-vs-char-pointer-in-c/30661089#30661089)
  - [How to compile glibc from source and use it?](https://stackoverflow.com/questions/847179/multiple-glibc-libraries-on-a-single-host/52454603#52454603)
  - [When should `static_cast`, `dynamic_cast`, `const_cast` and `reinterpret_cast` be used?](https://stackoverflow.com/questions/332030/when-should-static-cast-dynamic-cast-const-cast-and-reinterpret-cast-be-used/60414256#60414256)
  - [What exactly is `std::atomic` in C++?](https://stackoverflow.com/questions/31978324/what-exactly-is-stdatomic/58904448#58904448). This answer was originally more appropriately entitled "Let's disassemble some stuff", and got three downvotes, so Ciro changed it to a more professional title, and it started getting upvotes. People judge books by their covers.
  - <a id="code-nm-outputs-showing-that-objects-are-redefined-multiple-times-across-files-if-you-don-t-use-template-instantiation-properly"></a>
    ```
    notmain.o
    0000000000000000 0000000000000017 W MyTemplate<int>::f(int)
    main.o
    0000000000000000 0000000000000017 W MyTemplate<int>::f(int)
    ```
- [IEEE 754](mathematics.md#ieee-754)
  - [What is difference between quiet NaN and signaling NaN?](https://stackoverflow.com/questions/18118408/what-is-difference-between-quiet-nan-and-signaling-nan/55648118#55648118)
  - [In Java, what does NaN mean?](https://stackoverflow.com/questions/2618059/in-java-what-does-nan-mean/55673220#55673220)
  - <a id="code-visualization-of-subnormal-floating-point-numbers-vs-what-ieee-754-would-look-like-without-them"></a>
    ```
    Without subnormals:

              +---+---+-------+---------------+-------------------------------+
    exponent  | ? | 0 |   1   |       2       |               3               |
              +---+---+-------+---------------+-------------------------------+
              |   |   |       |               |                               |
              v   v   v       v               v                               v
              -----------------------------------------------------------------
    floats    *    **** * * * *   *   *   *   *       *       *       *       *
              -----------------------------------------------------------------
              ^   ^   ^       ^               ^                               ^
              |   |   |       |               |                               |
              0   |   2^-126  2^-125          2^-124                          2^-123
                  |
                  2^-127

    With subnormals:

              +-------+-------+---------------+-------------------------------+
    exponent  |   0   |   1   |       2       |               3               |
              +-------+-------+---------------+-------------------------------+
              |       |       |               |                               |
              v       v       v               v                               v
              -----------------------------------------------------------------
    floats    * * * * * * * * *   *   *   *   *       *       *       *       *
              -----------------------------------------------------------------
              ^   ^   ^       ^               ^                               ^
              |   |   |       |               |                               |
              0   |   2^-126  2^-125          2^-124                          2^-123
                  |
                  2^-127
    ```
- [Computer science](computer-science.md)
  - [Algorithms](computer-science.md#algorithm)
    - <a id="image-average-insertion-time-into-heaps-binary-search-tree-and-hash-maps-of-the-c-plus-plus-standard-library"></a>
      <img src="https://raw.githubusercontent.com/cirosantilli/media/master/C++_Heap_vs_BST_vs_hash_map_insert_time.png" alt="" height="1000">

      **[Figure 5](#image-average-insertion-time-into-heaps-binary-search-tree-and-hash-maps-of-the-c-plus-plus-standard-library). Average insertion time into heaps, binary search tree and hash maps of the C++ standard library**. [Source](https://stackoverflow.com/questions/6147242/heap-vs-binary-search-tree-bst/29548834\#29548834). From: [Heap vs Binary Search Tree (BST)](https://stackoverflow.com/questions/6147242/heap-vs-binary-search-tree-bst/29548834#29548834)
  - [Is it necessary for NP problems to be decision problems?](https://cs.stackexchange.com/questions/9664/is-it-necessary-for-np-problems-to-be-decision-problems/128702#128702)
  - [Polynomial time and exponential time](https://stackoverflow.com/questions/4317414/polynomial-time-and-exponential-time/68005934#68005934). Answered focusing on the definition of "exponential time".
  - [What is the smallest Turing machine where it is unknown if it halts or not?](https://cstheory.stackexchange.com/questions/20978/what-is-the-smallest-turing-machine-where-it-is-unknown-if-it-halts-or-not/53326#53326). Answer focusing on "blank tape" initial condition only. Large parts of it are summarizing the [Busy Beaver Challenge](computer-science.md#busy-beaver-challenge), but some additions were made.
- [Git](software.md#git)
  - <a id="code-ascii-art-depicting-the-binary-file-format-of-the-git-index-file"></a>

    ```
      | 0           | 4            | 8           | C              |
      |-------------|--------------|-------------|----------------|
    0 | DIRC        | Version      | File count  | ctime       ...| 0
      | ...         | mtime                      | device         |
    2 | inode       | mode         | UID         | GID            | 2
      | File size   | Entry SHA-1                              ...|
    4 | ...                        | Flags       | Index SHA-1 ...| 4
      | ...                                                       |
    ```
  - <a id="code-description-of-the-git-commit-object-binary-data-structure"></a>
    ```
    tree {tree_sha}
    {parents}
    author {author_name} <{author_email}> {author_date_seconds} {author_date_timezone}
    committer {committer_name} <{committer_email}> {committer_date_seconds} {committer_date_timezone}

    {commit message}
    ```
  - [How do I clone a subdirectory only of a Git repository?](https://stackoverflow.com/questions/600079/how-do-i-clone-a-subdirectory-only-of-a-git-repository/52269934#52269934)
- [Python](programming-language.md#python-programming-language)
  - [What is the difference between old style and new style classes in Python?](https://stackoverflow.com/a/19950198/895245)
  - [What is a mixin in Python, and why are they useful?](https://stackoverflow.com/a/20022860/895245)
  - [What are the differences between threads and processes in Python?](https://stackoverflow.com/questions/3044580/multiprocessing-vs-threading-python/55319297#55319297)

    <a id="image-python-threads-vs-processes-with-8-hyperthreads"></a>
    <img src="https://web.archive.org/web/20190607051221if_/https://i.stack.imgur.com/2x04m.png" alt="" height="600">

    **[Figure 6](#image-python-threads-vs-processes-with-8-hyperthreads). Python Threads vs Processes with 8 hyperthreads**. [Source](https://stackoverflow.com/questions/3044580/multiprocessing-vs-threading-python/55319297\#55319297).
- [Web technology](web-technology.md)
  - [What does enctype='multipart/form-data' mean?](https://stackoverflow.com/a/28380690/895245)
  - [JavaScript](programming-language.md#javascript)
    - [How does JavaScript `.prototype` work?](https://stackoverflow.com/a/23877420/895245)
    - [What is the difference between `.prop()` vs `.attr()` in JavaScript?](https://stackoverflow.com/a/24595458/895245)
- [OpenGL](software.md#opengl)
  - <a id="image-opengl-rendering-output-dumped-to-a-gif-file"></a>
    ![](https://raw.githubusercontent.com/cirosantilli/media/master/opengl-rotating-triangle-image-magick.gif)

    **[Figure 7](#image-opengl-rendering-output-dumped-to-a-gif-file). OpenGL rendering output dumped to  a GIF file**. [Source](https://stackoverflow.com/questions/3191978/how-to-use-glut-opengl-to-render-to-a-file/14324292\#14324292). From: [How to use GLUT/OpenGL to render to a file?](https://stackoverflow.com/questions/3191978/how-to-use-glut-opengl-to-render-to-a-file/14324292#14324292)
  - <a id="image-example-of-a-texture-atlas-containing-glyphs"></a>
    ![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Texture_Atlas.png/500px-Texture_Atlas.png)

    **[Figure 8](#image-example-of-a-texture-atlas-containing-glyphs). Example of a texture atlas containing glyphs**. [Source](https://en.wikipedia.org/wiki/File:Texture\_Atlas.png). Image by Nicolas P. Rougier, author of [Freetype GL](software.md#freetype-gl).

    Used on [Ciro Santilli](ciro-santilli.md)'s answer: [How to draw text using only OpenGL methods?](https://stackoverflow.com/questions/8847899/opengl-how-to-draw-text-using-only-opengl-methods/36065835#36065835)

    ---
  - <a id="image-opengl-glfrustrum-vs-glortho"></a>
    ![](https://raw.githubusercontent.com/cirosantilli/media/master/OpenGL_glFrustrum_on_left_vs_glOrtho_on_right.png)

    **[Figure 9](#image-opengl-glfrustrum-vs-glortho). OpenGL `glFrustrum` vs `glOrtho`**. [Source](https://stackoverflow.com/questions/2571402/how-to-use-glortho-in-opengl/36046924\#36046924). From: [How to use `glOrtho()` in OpenGL?](https://stackoverflow.com/questions/2571402/how-to-use-glortho-in-opengl/36046924#36046924)
  - [What are shaders in OpenGL?](https://stackoverflow.com/questions/17789575/what-are-shaders-in-opengl-and-what-do-we-need-them-for/36211337#36211337)
  - [Why do we use 4x4 matrices to transform things in 3D?](https://gamedev.stackexchange.com/questions/72044/why-do-we-use-4x4-matrices-to-transform-things-in-3d/118848#118848)
  - <a id="image-sinusoidal-circular-wave-heatmap-generated-with-an-opengl-shader-at-60-fps-on-sdl"></a>
    ![](https://raw.githubusercontent.com/cirosantilli/media/master/Sinusoidal_circular_wave_heatmap_generated_with_OpenGL_shader_at_60fps.gif)

    **[Figure 10](#image-sinusoidal-circular-wave-heatmap-generated-with-an-opengl-shader-at-60-fps-on-sdl). Sinusoidal circular wave heatmap generated with an OpenGL shader at 60 FPS on SDL**. [Source](https://stackoverflow.com/questions/30864752/is-it-possible-to-build-a-heatmap-from-point-data-at-60-times-per-second/39839788\#39839788). From: [Is it possible to build a heatmap from point data at 60 times per second?](https://stackoverflow.com/questions/30864752/is-it-possible-to-build-a-heatmap-from-point-data-at-60-times-per-second/39839788#39839788)

    Compared [CPU](computer-hardware.md#central-processing-unit) vs [GPU](computer-hardware.md#graphics-processing-unit) shaders.

    ---
  - [Image Processing with GLSL shaders?](https://stackoverflow.com/questions/13693946/image-processing-with-glsl-shaders/40641014#40641014) Compared the [CPU](computer-hardware.md#central-processing-unit) and GPU for a simple blur algorithm.

    ![](https://raw.githubusercontent.com/cirosantilli/media/master/Visualization_of_OpenGL_blur_algorithm_from_webcam_with_Ciro_Santilli_waving.gif)

    **[Figure 11](#_104)** [Source](https://stackoverflow.com/questions/13693946/image-processing-with-glsl-shaders/40641014\#40641014).

    <a id="video-opengl-gpu-glsl-fragment-shader-real-time-v4l2-linux-webcam-computer-vision-box-blur-vs-cpu"></a>
    **[Video 1](#video-opengl-gpu-glsl-fragment-shader-real-time-v4l2-linux-webcam-computer-vision-box-blur-vs-cpu). OpenGL GPU GLSL fragment shader real time v4l2 Linux webcam computer vision box blur vs CPU.** [Source](http://youtube.com/watch?v=MRhAljmHq-o).
- [Node.js](node-js.md)
  - [What's the difference between dependencies, devDependencies and peerDependencies in npm package.json file?](https://stackoverflow.com/a/22004559/895245)
- [Ruby on Rails](programming-language.md#ruby-on-rails)
  - [What is the difference between `+<%+`, `+<%=+`, `+<%#+` and `+-%>+` in ERB in Rails?](https://stackoverflow.com/a/25626629/895245)
- [POSIX](systems-programming.md#posix)
  - [What is POSIX?](https://stackoverflow.com/questions/1780599/what-is-the-meaning-of-posix/31865755#31865755) Huge classified overview of the most important things that POSIX specifies.
- [Systems programming](systems-programming.md)
  - [What do the terms "CPU bound" and "I/O bound" mean?](https://stackoverflow.com/questions/868568/what-do-the-terms-cpu-bound-and-i-o-bound-mean/33510470#33510470)
  - <a id="image-plot-of-real-user-and-sys-mean-times-of-the-output-of-time-for-cpu-bound-workload-with-8-threads"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/wall,_user,_and_sys_for_CPU-bound_work_with_8_hyperthreads.png" alt="" height="800">

    **[Figure 12](#image-plot-of-real-user-and-sys-mean-times-of-the-output-of-time-for-cpu-bound-workload-with-8-threads). Plot of "real", "user" and "sys" mean times of the output of time for CPU-bound workload with 8 threads**. [Source](https://stackoverflow.com/questions/556405/what-do-real-user-and-sys-mean-in-the-output-of-time1/53937376\#53937376). From: [What do 'real', 'user' and 'sys' mean in the output of time?](https://stackoverflow.com/questions/556405/what-do-real-user-and-sys-mean-in-the-output-of-time1/53937376#53937376)
  - <a id="code-logical-struture-pcie-device-functions-and-bars"></a>
    ```
    +--------+                  +------------+       +------+
    | device |>---------------->| function 0 |>----->| BAR0 |
    |        |                  |            |       +------+
    |        |>------------+    |            |
    |        |             |    |            |       +------+
       ...        ...      |    |            |>----->| BAR1 |
    |        |             |    |            |       +------+
    |        |>--------+   |    |            |
    +--------+         |   |         ...        ...    ...
                       |   |    |            |
                       |   |    |            |       +------+
                       |   |    |            |>----->| BAR5 |
                       |   |    +------------+       +------+
                       |   |
                       |   |
                       |   |    +------------+       +------+
                       |   +--->| function 1 |>----->| BAR0 |
                       |        |            |       +------+
                       |        |            |
                       |        |            |       +------+
                       |        |            |>----->| BAR1 |
                       |        |            |       +------+
                       |        |            |
                       |             ...        ...    ...
                       |        |            |
                       |        |            |       +------+
                       |        |            |>----->| BAR5 |
                       |        +------------+       +------+
                       |
                       |
                       |             ...
                       |
                       |
                       |        +------------+       +------+
                       +------->| function 7 |>----->| BAR0 |
                                |            |       +------+
                                |            |
                                |            |       +------+
                                |            |>----->| BAR1 |
                                |            |       +------+
                                |            |
                                     ...        ...    ...
                                |            |
                                |            |       +------+
                                |            |>----->| BAR5 |
                                +------------+       +------+
    ```
- [Electronics](electronics.md)
  - [Raspberry Pi](computer-hardware.md#raspberry-pi)
    - <a id="image-raspberry-pi-2-directly-connected-to-a-laptop-with-an-ethernet-cable"></a>
      ![](https://web.archive.org/web/20200809024904im_/https://i.stack.imgur.com/8C0mJ.jpg)

      **[Figure 13](#image-raspberry-pi-2-directly-connected-to-a-laptop-with-an-ethernet-cable). Raspberry Pi 2 directly connected to a laptop with an Ethernet cable**. Image from answer to: [How to hook up a Raspberry Pi via Ethernet to a laptop without a router?](https://stackoverflow.com/questions/16040128/hook-up-raspberry-pi-via-ethernet-to-laptop-without-router/39086537#39086537)

      <a id="image-raspberry-pi-2-connected-to-a-laptop-with-an-usb-uart-adapter"></a>
      ![](https://web.archive.org/web/20200809024904im_/https://i.stack.imgur.com/L0XyU.jpg)

      **[Figure 14](#image-raspberry-pi-2-connected-to-a-laptop-with-an-usb-uart-adapter). Raspberry Pi 2 connected to a laptop with an USB UART adapter**. Image from answer to: [How to hook up a Raspberry Pi via Ethernet to a laptop without a router?](https://stackoverflow.com/questions/16040128/hook-up-raspberry-pi-via-ethernet-to-laptop-without-router/39086537#39086537)

      <a id="image-raspberry-pi-os-being-emulated-on-qemu-2-5-0-on-ubuntu-16-04-with-a-modified-kernel"></a>
      <img src="https://web.archive.org/web/20210922124515im_/https://i.stack.imgur.com/TqIrP.png" alt="" height="600">

      **[Figure 15](#image-raspberry-pi-os-being-emulated-on-qemu-2-5-0-on-ubuntu-16-04-with-a-modified-kernel). Raspberry Pi OS being emulated on QEMU 2.5.0 on Ubuntu 16.04 with a modified kernel**. Image from answer to: [How to emulate the Raspberry Pi 2 on QEMU?](https://stackoverflow.com/questions/28880833/how-to-emulate-the-raspberry-pi-2-on-qemu/45814913#45814913)

      <a id="image-bare-metal-led-blinker-program-running-on-a-raspberry-pi-2"></a>
      ![](https://web.archive.org/web/20201112021056im_/https://i.stack.imgur.com/hztMj.gif)

      **[Figure 16](#image-bare-metal-led-blinker-program-running-on-a-raspberry-pi-2). Bare metal LED blinker program running on a Raspberry Pi 2**. Image from answer to: [How to run a C program with no OS on the Raspberry Pi?](https://stackoverflow.com/questions/29837892/how-to-run-a-c-program-with-no-os-on-the-raspberry-pi/40063032)
- [Computer security](software.md#computer-security)
  - [Why is the same origin policy so important?](https://security.stackexchange.com/a/72569/53321)
- Media
  - <a id="video-canon-in-d-in-c-language"></a>
    **[Video 2](#video-canon-in-d-in-c-language). Canon in D in C.** [Source](http://youtube.com/watch?v=JISozfHATms). From: [How is audio represented with numbers in computers?](https://stackoverflow.com/questions/732699/how-is-audio-represented-with-numbers-in-computers/36510894#36510894).

    The original [question was deleted, lol](stack-overflow.md#stack-overflow-content-deletion)...: [How to programmatically synthesize music?](https://stackoverflow.com/questions/2205070/programmatically-synthesizing-programming-music/52126471#52126471)

    ---
  - [How to resize a picture using ffmpeg's sws\_scale()?](https://stackoverflow.com/questions/12831761/how-to-resize-a-picture-using-ffmpegs-sws-scale/36487785#36487785)
  - [Is there any decent speech recognition software for Linux?](https://unix.stackexchange.com/questions/256138/is-there-any-decent-speech-recognition-software-for-linux/613392#613392) ran a few examples manually on `vosk-api` and compared to ground truth.
- [Eclipse](software.md#eclipse-ide)
  - [How to set up the Eclipse for remote C debugging with gdbserver?](https://stackoverflow.com/questions/4038760/how-to-set-up-the-eclipse-for-remote-c-debugging-with-gdbserver/45608937#45608937)
- [Computer hardware](computer-hardware.md)
  - [Are there good open source standard cell libraries to learn IC synthesis with EDA tools?](https://www.quora.com/Are-there-good-open-source-standard-cell-libraries-to-learn-IC-synthesis-with-EDA-tools/answer/Ciro-Santilli)
- [Scientific visualization software](software.md#scientific-visualization-software)
  - <a id="image-visit-zoom-in-10-million-straight-line-plot-with-some-manually-marked-points-best-articles"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/VisIt_zoom_in_10_million_straight_line_plot_with_some_marked_points.png" alt="" height="600">

    **[Figure 17](#image-visit-zoom-in-10-million-straight-line-plot-with-some-manually-marked-points-best-articles). VisIt zoom in 10 million straight line plot with some manually marked points**. [Source](https://stackoverflow.com/questions/5854515/large-plot-20-million-samples-gigabytes-of-data/55967461\#55967461). From: [Section "Survey of open source interactive plotting software with a 10 million point scatter plot benchmark by Ciro Santilli"](software.md#survey-of-open-source-interactive-plotting-software-with-a-10-million-point-scatter-plot-benchmark-by-ciro-santilli)
- [Numerical analysis](mathematics.md#numerical-analysis)
  - <a id="video-real-time-heat-equation-opengl-visualization-with-interactive-mouse-cursor-using-relaxation-method-by-ciro-santilli-2016"></a>
    **[Video 3](#video-real-time-heat-equation-opengl-visualization-with-interactive-mouse-cursor-using-relaxation-method-by-ciro-santilli-2016). Real-time heat equation OpenGL visualization with interactive mouse cursor using relaxation method by Ciro Santilli (2016)** [Source](http://youtube.com/watch?v=FOwYDlay8rI).
- [Computational physics](physics.md#computational-physics)
  - <a id="image-gnuplot-plot-of-the-y-position-of-a-sphere-bouncing-on-a-plane-simulated-in-bullet-physics-articles"></a>
    <img src="https://web.archive.org/web/20210225103255im_/https://i.stack.imgur.com/9eVe9.png" alt="" height="600">

    **[Figure 18](#image-gnuplot-plot-of-the-y-position-of-a-sphere-bouncing-on-a-plane-simulated-in-bullet-physics-articles). gnuplot plot of the y position of a sphere bouncing on a plane simulated in Bullet Physics**. [Source](https://stackoverflow.com/questions/11175694/bullet-physics-simplest-collision-example/36987063\#36987063). From: [What is the simplest collision example possible in a Bullet Physics simulation?](https://stackoverflow.com/questions/11175694/bullet-physics-simplest-collision-example/36987063#36987063)
- [Register transfer level](computer-hardware.md#register-transfer-level) languages like [Verilog](computer-hardware.md#verilog) and [VHDL](computer-hardware.md#vhdl)
  - [Verilog](computer-hardware.md#verilog):<a id="image-interacgive-asdf-controlled-demo-with-core-logic-written-in-verilog-using-verilator"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/verilog-interactive.gif" alt="" height="600">

    **[Figure 19](#image-interacgive-asdf-controlled-demo-with-core-logic-written-in-verilog-using-verilator). Interacgive ASDF-controlled demo with core logic written in Verilog using Verilator**. From: [Is it possible to do interactive user input and output simulation in VHDL or Verilog?](https://stackoverflow.com/questions/38108243/is-it-possible-to-do-interactive-user-input-and-output-simulation-in-vhdl-or-ver/38174654#38174654)

    See also: [Section "Verilator interactive example"](computer-hardware.md#verilator-interactive-example)

    ---
- [Android](systems-programming.md#android-operating-system)
  - <img src="https://raw.githubusercontent.com/cirosantilli/media/master/Android_AOSP_8.1.0_built_from_source_running_in_QEMU.png" alt="" height="600">

    **[Figure 20](#_157)** [Source](https://stackoverflow.com/questions/1809774/how-to-compile-the-android-aosp-kernel-and-test-it-with-the-android-emulator/48310014\#48310014). From: [How to compile the Android AOSP kernel and test it with the Android Emulator?](https://stackoverflow.com/questions/1809774/how-to-compile-the-android-aosp-kernel-and-test-it-with-the-android-emulator/48310014#48310014)
  - <a id="video-android-screen-showing-live-on-an-ubuntu-laptop-through-adb"></a>
    **[Video 4](#video-android-screen-showing-live-on-an-ubuntu-laptop-through-adb). Android screen showing live on an Ubuntu laptop through ADB.** [Source](https://www.youtube.com/watch?v=fVgeoMYm61Q). From: [How to see the Android screen live on an Ubuntu desktop through ADB?](https://android.stackexchange.com/questions/7686/is-there-a-way-to-see-the-devices-screen-live-on-pc-through-adb/154328#154328)
- [Debugging](software.md#debugging)
  - [What is the "Stack smashing detected" error in GCC and how to solve it?](https://stackoverflow.com/questions/1345670/stack-smashing-detected/51897264#51897264)
  - [What is RSS and VSZ in Linux memory management?](https://stackoverflow.com/questions/7880784/what-is-rss-and-vsz-in-linux-memory-management/57453334#57453334)
  - [How to print the call stack in C or C++?](https://stackoverflow.com/questions/3899870/print-call-stack-in-c-or-c/54365144#54365144)
  - [How to find memory leaks in C++ code?](https://stackoverflow.com/questions/6261201/how-to-find-memory-leak-in-a-c-code-project/57877190#57877190)
- [Program optimization](software.md#program-optimization)
  - [What is tail call optimization?](https://stackoverflow.com/questions/310974/what-is-tail-call-optimization/55230417#55230417)
  - <a id="image-gprof2dot-image-generated-from-the-gprof-data-of-a-simple-test-program"></a>
    <img src="https://web.archive.org/web/20200229164327if_/https://i.stack.imgur.com/mM8NQ.png" alt="" height="600">

    **[Figure 21](#image-gprof2dot-image-generated-from-the-gprof-data-of-a-simple-test-program). gprof2dot image generated from the gprof data of a simple test program**. [Source](https://stackoverflow.com/questions/375913/how-can-i-profile-c-code-running-on-linux/60265409\#60265409). From: [How can I profile C++ code running on Linux?](https://stackoverflow.com/questions/375913/how-can-i-profile-c-code-running-on-linux/60265409#60265409)

    The answer compares gprof, valgrind callgrind, perf and gperftools on a single simple executable.

    ---
- Data
  - <a id="image-mathematics-dump-of-wikipedia-cattree-articles"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master//Wikipedia_CatTree.png" alt="" height="600">

    **[Figure 22](#image-mathematics-dump-of-wikipedia-cattree-articles). Mathematics dump of Wikipedia CatTree**. [Source](https://cirosantilli.com/wikipedia-cattree/Mathematics). In this project, [Ciro Santilli](ciro-santilli.md) explored extracting the category and article tree out of the [Wikipedia dumps](website.md#wikipedia-dumps).
- [Mathematics](mathematics.md)
  - <a id="image-diagram-of-the-fundamental-theorem-on-homomorphisms-by-ciro-santilli-2020"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/Diagram_of_the_fundamental_theorem_on_homomorphisms_with_subtitles.svg" alt="" height="800">

    **[Figure 23](#image-diagram-of-the-fundamental-theorem-on-homomorphisms-by-ciro-santilli-2020). Diagram of the fundamental theorem on homomorphisms by Ciro Santilli (2020)** Shows the relationship between [group homomorphisms](group.md#group-homomorphism) and [normal subgroups](group.md#normal-subgroup).

    From: [What is the intuition behind normal subgroups?](https://math.stackexchange.com/questions/776039/intuition-behind-normal-subgroups/3732426#3732426)

    ---
  - [Section "Formalization of mathematics"](formalization-of-mathematics.md): some early thoughts that could be expanded. Ciro almost had a stroke when he understood this stuff in his teens.
  - <a id="image-simple-example-of-the-discrete-fourier-transform"></a>
    <img src="https://upload.wikimedia.org/wikipedia/commons/3/31/DFT_2sin%28t%29_%2B_cos%284t%29_25_points.svg" alt="" height="600">

    **[Figure 24](#image-simple-example-of-the-discrete-fourier-transform). Simple example of the Discrete Fourier transform**. [Source](https://commons.wikimedia.org/wiki/File:DFT_2sin%28t%29_%2B_cos%284t%29_25_points.svg). That was missing from [Wikipedia](website.md#wikipedia) page: [https://en.wikipedia.org/wiki/Discrete_Fourier_transform](https://en.wikipedia.org/wiki/Discrete_Fourier_transform)!
- [Network](computer.md#computer-network) programming
  - [How to make an HTTP get request in C without libcurl?](https://stackoverflow.com/questions/11208299/how-to-make-an-http-get-request-in-c-without-libcurl/35680609#35680609)
- [Physics](physics.md)
  - [What is the difference between plutonium and uranium?](chemistry.md#uranium-vs-plutonium-quora-answer-by-ciro-santilli)
  - <a id="image-spacetime-diagram-illustrating-how-faster-than-light-travel-implies-time-travel-articles"></a>
    <img src="https://raw.githubusercontent.com/cirosantilli/media/master/Faster_than_light_implies_time_travel_diagram.svg" alt="" height="600">

    **[Figure 25](#image-spacetime-diagram-illustrating-how-faster-than-light-travel-implies-time-travel-articles). Spacetime diagram illustrating how faster-than-light travel implies time travel**. From: [Does faster than light travel imply travelling back in time?](https://physics.stackexchange.com/questions/13001/does-superluminal-travel-imply-travelling-back-in-time/615079#615079)
- [Biology](biology.md)
  - <a id="image-top-view-of-an-open-oxford-nanopore-minion-articles"></a>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/Oxford_Nanopore_MinION_top_cropped.jpg/330px-Oxford_Nanopore_MinION_top_cropped.jpg" alt="" height="600">

    **[Figure 26](#image-top-view-of-an-open-oxford-nanopore-minion-articles). Top view of an open Oxford Nanopore MinION**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_top_cropped.jpg). From: [Section "How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it"](oxford-nanopore-river-bacteria.md)
  - <a id="image-mass-fractions-in-a-minimal-growth-medium-vs-an-amino-acid-cut-in-a-simulation-of-the-e-coli-whole-cell-model-by-covert-lab"></a>
    <img src="https://upload.wikimedia.org/wikipedia/commons/5/5f/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_mass_fraction_summary.svg" alt="" height="600">

    **[Figure 27](#image-mass-fractions-in-a-minimal-growth-medium-vs-an-amino-acid-cut-in-a-simulation-of-the-e-coli-whole-cell-model-by-covert-lab). Mass fractions in a minimal growth medium vs an amino acid cut in a simulation of the E. Coli Whole Cell Model by Covert Lab**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_mass_fraction_summary.svg). From: [Section "E. Coli Whole Cell Model by Covert Lab"](e-coli-whole-cell-model-by-covert-lab.md)
- [Quantum computing](quantum-computing.md)
  - [Section "Quantum computing is just matrix multiplication"](quantum-computing.md#programmer-s-model-of-quantum-computers)
  - <a id="image-visualization-of-the-continuous-deformation-of-states-as-we-walk-around-the-bloch-sphere-represented-as-photon-polarization-arrows"></a>
    ![](https://raw.githubusercontent.com/cirosantilli/media/master/matplotlib/bloch_sphere_walk.svg)

    **[Figure 28](#image-visualization-of-the-continuous-deformation-of-states-as-we-walk-around-the-bloch-sphere-represented-as-photon-polarization-arrows). Visualization of the continuous deformation of states as we walk around the Bloch sphere represented as photon polarization arrows**. From: [Understanding the Bloch sphere](https://physics.stackexchange.com/questions/204090/understanding-the-bloch-sphere/598254#598254).
- [Bitcoin](cryptocurrency.md#bitcoin)
  - [Section "Cool data embedded in the Bitcoin blockchain"](cool-data-embedded-in-the-bitcoin-blockchain.md)
- [GIMP](computer.md#gimp)
  - <a id="image-gimp-screenshot-part-of-how-to-combine-two-images-side-by-side-in-gimp"></a>
    <img src="https://web.archive.org/web/20210321083826if_/https://i.stack.imgur.com/r89lU.png" alt="" height="600">

    **[Figure 29](#image-gimp-screenshot-part-of-how-to-combine-two-images-side-by-side-in-gimp). GIMP screenshot part of how to combine two images side-by-side in GIMP?**
- Home DIY
  - <a id="image-total-blackout-cassette-roller-blind-with-curtains"></a>
    <img src="https://upload.wikimedia.org/wikipedia/commons/a/a6/Total_Blackout_Cassette_Roller_Blind_With_Curtains.jpg" alt="" height="600">

    **[Figure 30](#image-total-blackout-cassette-roller-blind-with-curtains). Total\_Blackout\_Cassette\_Roller\_Blind\_With\_Curtains.** [Source](https://commons.wikimedia.org/wiki/File:Total_Blackout_Cassette_Roller_Blind_With_Curtains.jpg). From: [Section "How to blackout your window without drilling"](window-blackout.md)
- [China](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-campaign-for-freedom-of-speech-in-china)
  - [What would happen if I walked around Beijing with a t-shirt that said "freedom of speech is pretty great"?](https://www.quora.com/What-would-happen-if-I-walked-around-Beijing-with-a-t-shirt-that-said-freedom-of-speech-is-pretty-great)

## 🏷️ Tagged (8)

- [Ciro Santilli's campaign for freedom of speech in China](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-campaign-for-freedom-of-speech-in-china)
- [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)
- [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)
- [ELF Hello World Tutorial](elf-hello-world.md)
- [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)
- [Programmer's model of quantum computers](quantum-computing.md#programmer-s-model-of-quantum-computers)
- [Uranium vs plutonium Quora answer by Ciro Santilli](chemistry.md#uranium-vs-plutonium-quora-answer-by-ciro-santilli)
- [x86 Paging Tutorial](x86-paging.md)

## ↑ Ancestors (2)

1. [Ciro Santilli](ciro-santilli.md)
2. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (10)

- [Ciro Santilli's Homepage](README.md)
- [Ciro Santilli's documentation superpowers](ciro-santilli.md#ciro-santilli-s-documentation-superpowers)
- [Ciro Santilli's Stack Overflow contributions](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-stack-overflow-contributions)
- [Computational physics](physics.md#computational-physics)
- [FFmpeg](software.md#ffmpeg)
- [Hacker News](website.md#hacker-news)
- [OpenGL](software.md#opengl)
- [QEMU](systems-programming.md#qemu)
- [Why you should give money to Ciro Santilli](sponsor.md#why-you-should-give-money-to-ciro-santilli)
- [Updates](updates.md)
