# btcdeb

↑ **Parent:** [Bitcoin script debugger](bitcoin-script-debugger.md)

[https://github.com/bitcoin-core/btcdeb](https://github.com/bitcoin-core/btcdeb)

Tested on [Ubuntu 23.10](ubuntu-23-10.md):
```
sudo apt install libtool
git clone https://github.com/bitcoin-core/btcdeb
cd btcdeb
git checkout 4fd007e57b79cba9b5ffdf5ffe599778c0d63b88
./autogen.sh
./configure
make -j
```
Patch submited at: [https://github.com/bitcoin-core/btcdeb/pull/143](https://github.com/bitcoin-core/btcdeb/pull/143)

Then we use it;
```
./btcdeb '[OP_1 OP_2 OP_ADD]'
```
and inside the shell:
```
btcdeb 5.0.24 -- type `./btcdeb -h` for start up options
LOG: signing segwit taproot
notice: btcdeb has gotten quieter; use --verbose if necessary (this message is temporary)
3 op script loaded. type `help` for usage information
script  |  stack 
--------+--------
1       | 
2       | 
OP_ADD  | 
#0000 1
btcdeb> step
                <> PUSH stack 01
script  |  stack 
--------+--------
2       |      01
OP_ADD  | 
#0001 2
btcdeb> step
                <> PUSH stack 02
script  |  stack 
--------+--------
OP_ADD  |      02
        |      01
#0002 OP_ADD
btcdeb> step
                <> POP  stack
                <> POP  stack
                <> PUSH stack 03
script  |  stack 
--------+--------
        |      03
btcdeb> step
script  |  stack 
--------+--------
        |      03
btcdeb> step
at end of script
btcdeb>
```

## ↑ Ancestors (12)

1. [Bitcoin script debugger](bitcoin-script-debugger.md)
2. [Bitcoin script](bitcoin-script.md)
3. [How Bitcoin works](how-bitcoin-works.md)
4. [Bitcoin](bitcoin.md)
5. [List of cryptocurrencies](list-of-cryptocurrencies.md)
6. [Cryptocurrency](cryptocurrency-split.md)
7. [Blockchain](blockchain.md)
8. [Money](money.md)
9. [Social technology](social-technology-split.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Merged by others](ciro-santilli-s-open-source-contributions/merged-by-others.md)
