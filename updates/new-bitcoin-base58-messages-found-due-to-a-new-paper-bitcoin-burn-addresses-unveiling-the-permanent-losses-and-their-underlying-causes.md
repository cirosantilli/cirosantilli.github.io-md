# New Bitcoin Base58 messages found due to a new paper: Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes

↑ **Parent:** [Updates](../updates-split.md)  
🏷️ **Tags:** [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md)

<a id="_276"></a>
This is an update to the article: [Section "Base58 messages"](../cool-data-embedded-in-the-bitcoin-blockchain/base58-messages.md).

<a id="_277"></a>
While self Googling a bit, I found this paper [Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](../cool-data-embedded-in-the-bitcoin-blockchain/bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes.md) by Mohamed el Khatib and Arnaud Legout briefly cited [Cool data embedded in the Bitcoin blockchain](../cool-data-embedded-in-the-bitcoin-blockchain-split.md).

<a id="_278"></a>
In that paper, they attempted to find [Base58](../base58.md) Bitcoin addresses that looked as if they were fake and used only in order to contain Base58 data.

<a id="_279"></a>
While we had previously explored a few [Base58](../base58.md) messages, this was something that had been done mostly ad-hoc simply by looking at transactions with large amounts of unspent outputs. As a result, any smaller messages were missed.

<a id="_280"></a>
By looking through the data produced by the those researchers, we managed to find many new [Base58](../base58.md) messages, and highlighted many of the most interesting early messages at: [Section "Base58 messages"](../cool-data-embedded-in-the-bitcoin-blockchain/base58-messages.md).

<a id="_281"></a>
The cutest new example is [tx dea183908e40e0cebfee6a0d8362b299e07cf193fbc02ffd3308b43781eca208](https://www.blockchain.com/explorer/transactions/btc/dea183908e40e0cebfee6a0d8362b299e07cf193fbc02ffd3308b43781eca208) (2011-11-24) containing Eric Lombrozo's minimalistic wedding contract to Sandra Sandic:<a id="_282"></a>

```
1EricLombrozoXXXXXXXXXXXXXXXWACBVB
1969SandraSandicXXXXXXXXXXXXXvdEiU
```

<a id="_283"></a>
Announced at:<a id="_284"></a>

<a id="_285"></a>
- [https://mastodon.social/@cirosantilli/114218387671424003](https://mastodon.social/@cirosantilli/114218387671424003)
<a id="_286"></a>
- [https://x.com/cirosantilli/status/1904211594000715781](https://x.com/cirosantilli/status/1904211594000715781)

## ↑ Ancestors (3)

1. [Updates](../updates-split.md)
2. [Ciro Santilli](../ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](../split.md)
