<h1 id="compile-micropython-code-for-micro-bit-locally-on-ubuntu-22-04-with-your-own-firmware">Compile MicroPython code for Micro Bit locally on <a href="systems-programming.html#ubuntu-22-04">Ubuntu 22.04</a> with your own firmware</h1>

↑ **Parent:** [Compile MicroPython code for Micro Bit locally](compile-micropython-code-for-micro-bit-locally.md)

TODO didn't manage from source [Ubuntu 22.04](ubuntu-22-04.md), their setup bitrotted way too fast... it's shameful even. Until I gave up and went for the magic [Docker](docker-software.md) of + [https://github.com/bbcmicrobit/micropython](https://github.com/bbcmicrobit/micropython), and it bloody worked:
```
git clone https://github.com/bbcmicrobit/micropython
cd micropython
git checkout 7fc33d13b31a915cbe90dc5d515c6337b5fa1660
docker pull ghcr.io/carlosperate/microbit-toolchain:latest
docker run -v $(pwd):/home --rm ghcr.io/carlosperate/microbit-toolchain:latest yt target bbc-microbit-classic-gcc-nosd@https://github.com/lancaster-university/yotta-target-bbc-microbit-classic-gcc-nosd
docker run -v $(pwd):/home --rm ghcr.io/carlosperate/microbit-toolchain:latest make all

# Build one.
tools/makecombinedhex.py build/firmware.hex examples/counter.py -o build/counter.hex
cp build/counter.hex "/media/$USER/MICROBIT/"

# Build all.
for f in examples/*; do b="$(basename "$f")"; echo $b; tools/makecombinedhex.py build/firmware.hex "$f" -o "build/${b%.py}.hex"; done
```

The pre-Docker attempts:
```
sudo add-apt-repository -y ppa:team-gcc-arm-embedded
sudo apt update
sudo apt install gcc-arm-embedded
sudo apt install cmake ninja-build srecord libssl-dev

# Rust required for some Yotta component, OMG.
sudo snap install rustup
rustup default 1.64.0

python3 -m pip install yotta
```

The line:
```
sudo add-apt-repository -y ppa:team-gcc-arm-embedded
```
warns:
```
E: The repository 'https://ppa.launchpadcontent.net/team-gcc-arm-embedded/ppa/ubuntu jammy Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
```
and then the update/`sudo apt-get install gcc-arm-embedded` fails, bibliography:
- [https://askubuntu.com/questions/732985/force-update-from-unsigned-repository](https://askubuntu.com/questions/732985/force-update-from-unsigned-repository)
- [https://askubuntu.com/questions/1243252/how-to-install-arm-none-eabi-gdb-on-ubuntu-20-04-lts-focal-fossa](https://askubuntu.com/questions/1243252/how-to-install-arm-none-eabi-gdb-on-ubuntu-20-04-lts-focal-fossa)

Attempting to install [Yotta](yotta-build-system.md):
```
sudo -H pip3 install yotta
```
or:
```
python3 -m pip install --user yotta
```
was failing with:
```
Exception: Version mismatch: this is the 'cffi' package version 1.15.1, located in '/tmp/pip-build-env-dinhie_9/overlay/local/lib/python3.10/dist-packages/cffi/api.py'.  When we import the top-level '_cffi_backend' extension module, we get version 1.15.0, located in '/usr/lib/python3/dist-packages/_cffi_backend.cpython-310-x86_64-linux-gnu.so'.  The two versions should be equal; check your installation.
```
Running:
```
python3 -m pip install --user cffi==1.15.1
```
did not help. Bibliography:
- [https://stackoverflow.com/questions/58552666/exception-version-mismatch-this-is-the-cffi-package-version-1-13-1](https://stackoverflow.com/questions/58552666/exception-version-mismatch-this-is-the-cffi-package-version-1-13-1)
- [https://github.com/ARMmbed/yotta/issues/289](https://github.com/ARMmbed/yotta/issues/289)
- [https://github.com/pyocd/pyOCD/issues/163](https://github.com/pyocd/pyOCD/issues/163)
- [http://docs.yottabuild.org/#installing-on-linux](http://docs.yottabuild.org/#installing-on-linux)

From a clean [virtualenv](virtualenv.md), it appears to move further, and then fails at:
```
Building wheel for cmsis-pack-manager (pyproject.toml) ... error
error: [Errno 2] No such file or directory: 'cargo'
```
So we install [Rust](rust-programming-language.md) and try again, OMG:
```
sudo snap install rustup
rustup default stable
```
which at the time of writing was `rustc 1.64.0`, and then OMG, it worked!! We have the `yt` command.

However, it is still broken, e.g.:
```
git clone https://github.com/lancaster-university/microbit-samples
cd microbit-samples
git checkout 285f9acfb54fce2381339164b6fe5c1a7ebd39d5
cp source/examples/invaders/* source
yt clean
yt build
```
blows up:
```
annot import name 'soft_unicode' from 'markupsafe'
```
bibliography:
- [https://github.com/aws/aws-sam-cli/issues/3661](https://github.com/aws/aws-sam-cli/issues/3661)
- [https://stackoverflow.com/questions/72191560/importerror-cannot-import-name-soft-unicode-from-markupsafe](https://stackoverflow.com/questions/72191560/importerror-cannot-import-name-soft-unicode-from-markupsafe)

## ↑ Ancestors (13)

1. [Compile MicroPython code for Micro Bit locally](compile-micropython-code-for-micro-bit-locally.md)
2. [Run MicroPython on Micro Bit](run-micropython-on-micro-bit.md)
3. [Program the Micro Bit with X](program-the-micro-bit-with-x.md)
4. [Micro Bit](micro-bit.md)
5. [Microcontroller devboard](microcontroller-devboard.md)
6. [Microprocessor development board](microprocessor-development-board.md)
7. [Printed circuit board](printed-circuit-board.md)
8. [Circuit board](circuit-board.md)
9. [Electronic circuit](electronic-circuit.md)
10. [Electronics](electronics-split.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Compile MicroPython code for Micro Bit locally](compile-micropython-code-for-micro-bit-locally.md)
- [Program the Micro Bit in C](program-the-micro-bit-in-c.md)
