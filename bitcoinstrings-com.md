<h1 id="bitcoinstrings-com">BitcoinStrings.com</h1>

↑ **Parent:** [How to extract data from the Bitcoin blockchain](how-to-extract-data-from-the-bitcoin-blockchain.md)

[https://bitcoinstrings.com](https://bitcoinstrings.com) has all `strings -n20` strings, we can obtain the whole thing and clean it up a bit with:
```
wget -O all.html https://bitcoinstrings.com/all
cp all.html all-recode.html
recode html..ascii all-recode.html
awk '!seen[$0]++' all-recode.html > all-uniq.html
```
`awk` to skip the gazillion "mined by message" repeats.

A lot of in that website stuff appears to be cut up at the 20 mark. As shown in [Force of Will](cool-data-embedded-in-the-bitcoin-blockchain/force-of-will.md), this is possibly because they didn't use `-w` in `strings -n20`, and the text after the newlines was less than 20 characters.

That website can be replicated by downloading the [Bitcoin](bitcoin.md) blockchain locally, then:
```
cd .bitcoin/blocks
for f in blk*.dat; do strings -n20 -w $f | awk '!seen[$0]++' > ${f%.dat}.txt; done
tail +n1 *.txt
```

Remove most of the binary crap:
```
head -n-1 *.txt | grep -e '[. ]' | grep -iv 'mined by' | less
```

## ↑ Ancestors (10)

1. [How to extract data from the Bitcoin blockchain](how-to-extract-data-from-the-bitcoin-blockchain.md)
2. [Bitcoin](bitcoin.md)
3. [List of cryptocurrencies](list-of-cryptocurrencies.md)
4. [Cryptocurrency](cryptocurrency-split.md)
5. [Blockchain](blockchain.md)
6. [Money](money.md)
7. [Social technology](social-technology-split.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Len Sassaman tribute](cool-data-embedded-in-the-bitcoin-blockchain/len-sassaman-tribute.md)
