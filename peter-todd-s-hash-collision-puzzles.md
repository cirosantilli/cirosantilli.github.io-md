<h1 id="peter-todd-s-hash-collision-puzzles">Peter Todd's hash collision puzzles</h1>

↑ **Parent:** [Bitcoin non-standard transaction](bitcoin-non-standard-transaction.md)  
🏷️ **Tags:** [Puzzle script](puzzle-script.md)

- [https://bitcointalk.org/index.php?topic=293382.0](https://bitcointalk.org/index.php?topic=293382.0)
- [https://xiaohuiliu.medium.com/bitcoin-zk-bounty-series-part-2-finding-hash-collisions-5e3aa3eb3925](https://xiaohuiliu.medium.com/bitcoin-zk-bounty-series-part-2-finding-hash-collisions-5e3aa3eb3925)
- [https://bitcoinjs-guide.bitcoin-studio.com/bitcoinjs-guide/v5/part-three-pay-to-script-hash/puzzles/computational_puzzle_sha1_collision_p2sh](https://bitcoinjs-guide.bitcoin-studio.com/bitcoinjs-guide/v5/part-three-pay-to-script-hash/puzzles/computational_puzzle_sha1_collision_p2sh)

As mentioned at the prize was claimed at [8d31992805518fd62daa3bdd2a5c4fd2cd3054c9b3dca1d78055e9528cff6adc](https://www.blockchain.com/explorer/transactions/btc/8d31992805518fd62daa3bdd2a5c4fd2cd3054c9b3dca1d78055e9528cff6adc) (2017-02-23) which spends several inputs with the same unlock script that presents two different constantants that have the same [SHA-1](sha-1.md):
```
printf 255044462d312e330a25e2e3cfd30a0a0a312030206f626a0a3c3c2f57696474682032203020522f4865696768742033203020522f547970652034203020522f537562747970652035203020522f46696c7465722036203020522f436f6c6f7253706163652037203020522f4c656e6774682038203020522f42697473506572436f6d706f6e656e7420383e3e0a73747265616d0affd8fffe00245348412d3120697320646561642121212121852fec092339759c39b1a1c63c4c97e1fffe017f46dc93a6b67e013b029aaa1db2560b45ca67d688c7f84b8c4c791fe02b3df614f86db1690901c56b45c1530afedfb76038e972722fe7ad728f0e4904e046c230570fe9d41398abe12ef5bc942be33542a4802d98b5d70f2a332ec37fac3514e74ddc0f2cc1a874cd0c78305a21566461309789606bd0bf3f98cda8044629a1 | xxd -r -p | sha1sum
printf 255044462d312e330a25e2e3cfd30a0a0a312030206f626a0a3c3c2f57696474682032203020522f4865696768742033203020522f547970652034203020522f537562747970652035203020522f46696c7465722036203020522f436f6c6f7253706163652037203020522f4c656e6774682038203020522f42697473506572436f6d706f6e656e7420383e3e0a73747265616d0affd8fffe00245348412d3120697320646561642121212121852fec092339759c39b1a1c63c4c97e1fffe017346dc9166b67e118f029ab621b2560ff9ca67cca8c7f85ba84c79030c2b3de218f86db3a90901d5df45c14f26fedfb3dc38e96ac22fe7bd728f0e45bce046d23c570feb141398bb552ef5a0a82be331fea48037b8b5d71f0e332edf93ac3500eb4ddc0decc1a864790c782c76215660dd309791d06bd0af3f98cda4bc4629b1 | xxd -r -p | sha1sum
```
both giving
```
f92d74e3874587aaf443d1db961d4e26dde13e9c
```
It was claimed on the same day that [Google](google-split.md) disclosed the collision: [https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html](https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html)

Both of these are [PDF](pdf.md) prefixes, so they start with the PDF [file signature](file-signature.md), but are not fully viewable PDFs on their own. 

**Table of contents**

- [Peter Todd](peter-todd.md)

## ↑ Ancestors (13)

1. [Bitcoin non-standard transaction](bitcoin-non-standard-transaction.md)
2. [Bitcoin script type](bitcoin-script-type.md)
3. [Bitcoin script](bitcoin-script.md)
4. [How Bitcoin works](how-bitcoin-works.md)
5. [Bitcoin](bitcoin.md)
6. [List of cryptocurrencies](list-of-cryptocurrencies.md)
7. [Cryptocurrency](cryptocurrency-split.md)
8. [Blockchain](blockchain.md)
9. [Money](money.md)
10. [Social technology](social-technology-split.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [ASCII art](cool-data-embedded-in-the-bitcoin-blockchain/ascii-art.md)
