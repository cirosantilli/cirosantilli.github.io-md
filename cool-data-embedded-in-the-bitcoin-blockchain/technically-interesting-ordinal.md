# Technically interesting ordinal

↑ **Parent:** [Ordinal ruleset inscription](ordinal-ruleset-inscription.md)

This section is about ordinals that are interesting primarily due to technical reasons linked to edge cases of the protocol.

Interesting MIME types:
- [https://ordinals.com/inscription/dad86d722156b8c384c1f3243e40aa7a0f6f5be496bc24e19485831584f9803fi0](https://ordinals.com/inscription/dad86d722156b8c384c1f3243e40aa7a0f6f5be496bc24e19485831584f9803fi0): mime type is an UTF-8 orange emoji "🟠"
- [https://ordinals.com/inscription/bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22i0](https://ordinals.com/inscription/bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22i0): mime type is an [XSS](../cross-site-scripting.md) attempt:
  ```
  <script>alert('xss in content type')</script> tx=bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22
  ```
- [https://ordinals.com/inscription/bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22i0](https://ordinals.com/inscription/bc7b86245159cdf8bc63489687909f766a0a0e08279d23fb077cdd60ab1e9f22i0): mime type is "FuckYou"
- [https://ordinals.com/inscription/00b0ece72217ce49b637b3f9bf5335bc245e588568aa0676581b40c1bedc521di0](https://ordinals.com/inscription/00b0ece72217ce49b637b3f9bf5335bc245e588568aa0676581b40c1bedc521di0): the mime is a long [JSON](../json.md). However, it does appear to be a valid feature as it rendered specially on [ordinals.com](ordinals-com.md).

Different `ord` markers:
- 71e85885522047240a9e70542145dbf2385e1bd468e6ac6002aa755422ea10f5 uses `takingnames`. Decode with:
  ```
  bitcoin-core.cli decodescript "$(bitcoin-core.cli getrawtransaction 71e85885522047240a9e70542145dbf2385e1bd468e6ac6002aa755422ea10f5 true | jq -r '.vin[0].txinwitness[1]')" | jq -r .asm | sed 's/.* 0 //;s/ OP_ENDIF//;s/ //g' | xxd -r -p > 71e85885522047240a9e70542145dbf2385e1bd468e6ac6002aa755422ea10f5.png
  ```

  gives the [PNG](../portable-network-graphics.md) of the wireframe draing of a washing machine with transparent background.

**Table of contents**

- [Largest ordinal inscription](largest-ordinal-inscription.md)
  - [Largest text ordinal inscription](largest-text-ordinal-inscription.md)
    - [Ordinal ASCII art inscription](ordinal-ascii-art-inscription.md)
      - [We are 256, We are 1](we-are-256-we-are-1.md)
- [Cursed ordinal](cursed-ordinal.md)

## ↑ Ancestors (14)

1. [Ordinal ruleset inscription](ordinal-ruleset-inscription.md)
2. [Images](images.md)
3. [Media type](media-type.md)
4. [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)
5. [Bitcoin inscription](../bitcoin-inscription.md)
6. [Bitcoin](../bitcoin.md)
7. [List of cryptocurrencies](../list-of-cryptocurrencies.md)
8. [Cryptocurrency](../cryptocurrency-split.md)
9. [Blockchain](../blockchain.md)
10. [Money](../money.md)
11. [Social technology](../social-technology-split.md)
12. [Area of technology](../area-of-technology.md)
13. [Technology](../technology-split.md)
14. [Ciro Santilli's Homepage](../split.md)
