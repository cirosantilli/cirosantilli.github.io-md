# Bibliography

↑ **Parent:** [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)

<a id="_1580"></a>
Other Bitcon analysis:<a id="_1581"></a>

<a id="_1582"></a>
- <a id="_1583"></a>
  "Annotated blockchain project"<a id="_1584"></a>

  <a id="_1585"></a>
  - [https://etherpad.mit.edu/p/r.e33d2e7230fafc0612a0f2e7ebc87bae](https://etherpad.mit.edu/p/r.e33d2e7230fafc0612a0f2e7ebc87bae)
  <a id="_1586"></a>
  - [https://etherpad.mit.edu/p/r.19b7b3e2c5ea08a61cb0bef0aeb213fd](https://etherpad.mit.edu/p/r.19b7b3e2c5ea08a61cb0bef0aeb213fd) image list (February 8, 2017) We tried going over it, but it is just too much work, the huge majority of the results are just [AtomSea & EMBII](atomsea-and-embii.md) so not that interesting.
  <a id="_1587"></a>
  - [https://archive.ph/Zz7m5](https://archive.ph/Zz7m5)
  <a id="_1588"></a>
  - [https://www.reddit.com/r/Bitcoin/comments/5wax5v/a_group_is_working_on_building_a_fully_annotated/](https://www.reddit.com/r/Bitcoin/comments/5wax5v/a_group_is_working_on_building_a_fully_annotated/)
  <a id="_1589"></a>
  - [https://archive.4plebs.org/pol/thread/111742853/](https://archive.4plebs.org/pol/thread/111742853/)
  Does the same as this page, just that it is an uncomprehensible mess of broken links. But they have soe good ideas!

  <a id="_1590"></a>
  Their main techniques seem to be:<a id="_1591"></a>

  ```
  mkdir binout
  for file in blk*dat; do echo "$file"; binwalk --dd='.*' "$file" -C binout/. --log=binout/"$file""res.txt"; done
  ```
  and:<a id="_1592"></a>

  ```
  mkdir subfileout
  for file in blk*dat; do mkdir subfileout/"$file"; done
  for file in blk*dat; do echo "$file"; hachoir-subfile --category=image,video,audio,container,archive,misc "$file" subfileout/"$file" > subfileout/"$file""subfile.txt"; done
  ```
  which seem promising.

  <a id="_1593"></a>
  These are installable on Ubuntu 23.10 with:<a id="_1594"></a>

  ```
  sudo apt install binwalk hachoir
  ```

  <a id="_1595"></a>
  TODO how to they automatically map back to transaction IDs? There is a line "Script to add the TX ID to each file." Our attempts: [Section "Get transaction id from position in dat file"](../get-bitcoin-transaction-id-from-position-in-dat-file.md)

**Table of contents**

- [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014.md)
- [A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin by Matzutt et al. (2018)](a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin-by-matzutt-et-al-2018.md)
- [Messages from the mines](messages-from-the-mines.md)
- [Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes.md)

## ↑ Ancestors (11)

1. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
2. [Bitcoin inscription](../bitcoin-inscription.md)
3. [Bitcoin](../bitcoin.md)
4. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
5. [Cryptocurrency](../cryptocurrency-split.md)
6. [Blockchain](../blockchain.md)
7. [Money](../money.md)
8. [Social technology](../social-technology-split.md)
9. [Area of technology](../area-of-technology.md)
10. [Technology](../technology-split.md)
11. [Ciro Santilli's Homepage](../split.md)
