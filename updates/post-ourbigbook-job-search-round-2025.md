# Post OurBigBook job search round 2025

↑ **Parent:** [Updates](../updates-split.md)

<a id="_98"></a>
I shouldn't be doing this on funded [OurBigBook](../ourbigbook.md) time which is until the end of May, but I was getting too nervous and decided to start a casual job search to test the waters.

<a id="_99"></a>
In particular I want to see if I can get past the HR lady step without toning down my online profiles. If nothing works out for the next round I'll be hiding anything too spicy like:<a id="_100"></a>

<a id="_101"></a>
- prominently seeking funding for [OurBigBook](../ourbigbook.md) on my [LinkedIn](../linkedin.md) profile
<a id="_102"></a>
- [CIA 2010 covert communication websites](../cia-2010-covert-communication-websites-split.md) references. This will be my first job hunt since I have published that article. Wish me luck.
<a id="_103"></a>
- [gay Putin](https://cirosantilli.com/china-dictatorship/gay-putin) profile picture on [Stack Overflow](../stack-overflow-split.md)
Another interesting point is to see if French companies are more likely to reply given that [Ciro Santilli](../ciro-santilli-split.md) studied at [École Polytechnique](../ecole-polytechnique-split.md) which the French worship.

<a id="image-gay-putin-currently-used-in-ciro-santilli-s-stack-overflow-profile"></a>
![](https://web.archive.org/web/20240707132335im_/https://cdn.i-scmp.com/sites/default/files/styles/1200x800/public/images/methode/2017/04/06/0a2ae706-1a94-11e7-b4ed-ac719e54b474_1280x720_145124.jpg?itok=1PDxSxTA)

**[Figure 2](#image-gay-putin-currently-used-in-ciro-santilli-s-stack-overflow-profile). Gay Putin, currently used in Ciro Santilli's Stack Overflow profile**. Ciro's profiles may be a bit too much for the HR ladies who reject his job applications on the spot. To be fair, perhaps not enough years of experience for certain applications and job hopping may have something to do with it too. But since they don't ever tell you anything not to get sued, we'll never know.

<a id="_104"></a>
I'm looking in particular either for:<a id="_105"></a>

<a id="_106"></a>
- [machine learning](../machine-learning-split.md)-adjacent jobs in companies that seem to be doing something that could further [AGI](../artificial-general-intelligence.md), e.g. [automatic code generation](../automatic-programming.md) or [robotics](../robotics-split.md) would be ideal
<a id="_107"></a>
- [quantum computing](../quantum-computing-split.md)
<a id="_108"></a>
- [systems programming](../systems-programming-split.md), which is what I actually have work experience with

<a id="_109"></a>
I spent the last two weeks doing that:<a id="_110"></a>

<a id="_111"></a>
- one week browsing everything of interest in [London](../london.md) and [Paris](../paris.md) and sending applications to anything that seemed both relevant and interesting. Maintaining an application list at: [Section "Job application by Ciro Santilli"](../job-application-by-ciro-santilli.md).
<a id="_112"></a>
- <a id="_113"></a>
  one week on a very laborious but somewhat interesting take home exercise for [Linux kernel](../linux-kernel.md) engineer a [Canonical](../canonical-company.md), makers of [Ubuntu](../ubuntu.md).

  <a id="_114"></a>
  I had a week to finish 5 practical coding and packaging questions, and I tried to do everything as perfectly as possible, but I somewhat underestimated the amount of work and wait needed to do everything and didn't manage to finish question 4 and missed 5. Oops let's see how that goes.

  <a id="_115"></a>
  At least this had a few good outcomes for the Internet as I tried to document things as nicely as I could where they were missing from [Google](../google-split.md) as usual:<a id="_116"></a>

  <a id="_117"></a>
  - I re-tested [Linux Kernel Module Cheat](../linux-kernel-module-cheat-split.md) and made some small improvements. Things still worked from a [Ubuntu 24.10](../ubuntu-24-10.md) host (using Docker to [Ubuntu 22.04](../ubuntu-22-04.md)), and I also checked that kernel 6.8 builds and GDB step debugs after adding the newly required config `CONFIG_DEBUG_INFO_DWARF_TOOLCHAIN_DEFAULT`, also mentioned that at: [Why are there no debug symbols in my vmlinux when using gdb with /proc/kcore?](https://stackoverflow.com/questions/5416406/why-are-there-no-debug-symbols-in-my-vmlinux-when-using-gdb-with-proc-kcore/79598380#79598380)
  <a id="_118"></a>
  - I contributed some simple updates to [https://github.com/martinezjavier/ldd3](https://github.com/martinezjavier/ldd3) getting it closer to work on Linux kernel v6.8. That repository aims to keep the venerable examples from Linux kernel module book [LDD3](../linux-device-drivers-book-3rd-edition.md) alive on newer kernels, and is a very good source for kernel module developers.
  <a id="_119"></a>
  - [How to compile a Linux kernel module?](https://stackoverflow.com/questions/37507320/how-to-compile-a-linux-kernel-module/79594642#79594642): wrote a quick Ciro-approved tutorial
  <a id="_120"></a>
  - [Dynamic array in Linux kernel module](https://stackoverflow.com/questions/6034745/dynamic-array-in-linux-kernel-module/79601790#79601790): I gave an educational example of a dynamic byte array (like std::string) using the kvmalloc family of allocators
  <a id="_121"></a>
  - [quickemu](../quickemu.md): this is a good [emulator manager](../emulator-manager.md) and I think I'll be using it for [Ubuntu](../ubuntu.md) images when needed from now on. I wrote:<a id="_122"></a>

    <a id="_123"></a>
    - [How to run Ubuntu desktop on QEMU?](https://askubuntu.com/questions/884534/how-to-run-ubuntu-desktop-on-qemu/1545712#1545712): an introductory tutorial to the software as their README is not that good as is often the case. It's hard for project authors to predict what new users want or not. This is my second answer to this question, the [previous one](https://askubuntu.com/questions/884534/how-to-run-ubuntu-desktop-on-qemu/1046792#1046792) focusing on a more manual approach without third party helpers.
    <a id="_124"></a>
    - [How to share folder between guest/host? (Quickemu)](https://www.reddit.com/r/commandline/comments/v85fmx/how_to_share_folder_between_guesthost_quickemu/): I explained how to setup a 9p mount to share a directory between guest and host
  <a id="_125"></a>
  - [Error :: You must put some 'source' URIs in your sources.list](https://askubuntu.com/questions/496549/error-you-must-put-some-source-uris-in-your-sources-list/857433#857433): updated this answer for [Ubuntu 24.04](../ubuntu-24-04.md). This issue comes up when you want to do either of:<a id="_126"></a>

    ```
    sudo apt build-dep
    sudo apt source
    ```

    which don't work by default, and my answer explains how to do it from the GUI and CLI. The CLI method is specially important for [Docker](../docker-software.md) images. Since Ubuntu doesn't offer a stable CLI method for this, the method breaks from time to time and we have to find the new config file to edit.
  <a id="_127"></a>
  - <a id="_128"></a>
    [What is hardware enablement (HWE)?](https://askubuntu.com/questions/248914/what-is-hardware-enablement-hwe/1546835#1546835p): I learned a bit better how Ubuntu structures its kernel releases for each [Ubuntu release](../ubuntu-release.md)

    <a id="image-linux-kernel-version-used-for-each-ubuntu-release"></a>
    <img src="https://web.archive.org/web/20250506101112if_/https://i.sstatic.net/3sqTiQlD.png" alt="" height="600">

    **[Figure 3](#image-linux-kernel-version-used-for-each-ubuntu-release). Linux kernel version used for each Ubuntu release**. [Source](https://ubuntu.com/about/release-cycle). In particular, Ubuntu has HWE kernels which are updated kernels for older releases. E.g.<a id="_129"></a>

    <a id="_130"></a>
    - 24.04.0 and 24.04.1 had kernel 6.8
    <a id="_131"></a>
    - 24.04.2 moved up to kernel 6.11, the same one used in 24.10, to support newer hardware

    ---

  <a id="_132"></a>
  Some of the main issues I had were:<a id="_133"></a>

  <a id="_134"></a>
  - [compiling Linux kernel for Ubuntu](../compile-linux-kernel-for-ubuntu.md) is extremely slow. I was used to compiling for embedded system with [Buildroot](../buildroot.md), which finishes in minutes, but for Ubuntu is hours, presumably because they enable as many drivers as possible to make a single ISO work on as many different computers as possible, which makes sense, but also makes development harder
  <a id="_135"></a>
  - my [QEMU](../qemu.md) setup for Ubuntu was not quite as streamlined and I relearned a few things and set up [quickemu](../quickemu.md). By chance I had recently come across [quickemu](../quickemu.md) for testing [OurBigBook](../ourbigbook.md) on [MacOS](../macos.md), but I had to learn a bit how to set it up reasonably too

<a id="_136"></a>
I'll make sure to add two weeks of OurBigBook work after May to make up for this.

## ↑ Ancestors (3)

1. [Updates](../updates-split.md)
2. [Ciro Santilli](../ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (1)

- [Two Linux Kernel Module Cheat videos](two-linux-kernel-module-cheat-videos.md)
