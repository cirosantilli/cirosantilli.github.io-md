# How Bitcoin works

↑ **Parent:** [Bitcoin](bitcoin.md)

Here is a very direct description of the system:
- each transaction (transaction is often abbreviated "tx") has a list of inputs, and a list of outputs
- each input is the output of a previous transaction. You verify your identity as the indented receiver by producing a [digital signature](digital-signature.md) for the [public key](public-key-cryptography.md) specified on the output
- each output specifies the [public key](public-key-cryptography.md) of the receiver and the value being sent
- the sum of output values cannot obvious exceed the sum of input values. If it is any less, the leftover is sent to the miner of the transaction as a transaction fee, which is an incentive for mining.
- once an output is used from an input, it becomes marked as spent, and cannot be reused again. Every input uses the selected output fully. Therefore, if you want to use an input of 1 [BTC](bitcoin.md) to pay 0.1 [BTC](bitcoin.md), what you do is to send 0.1 [BTC](bitcoin.md) to the receiver, and 0.9 [BTC](bitcoin.md) back to yourself as [change](change-bitcoin.md). This is why the vast majority of transactions has two outputs: one "real", and the other [change](change-bitcoin.md) back to self.
[Code 1. "Sample Bitcoin transaction graph"](#code-sample-bitcoin-transaction-graph) illustrates these concepts:
- `tx0`: magic transaction without any inputs, i.e. either [Genesis block](genesis-block.md) or a coinbase [mining reward](bitcoin-mining-reward.md). Since it is a magic transaction, it produces 3 Bitcoins from scratch: 1 in `out0` and 2 in `out1`. The initial value was actually 50 [BTC](bitcoin.md) and reduced with time: [Section "Bitcoin halving"](bitcoin-halving.md)
- `tx1`: regular transaction that takes:
  - a single input from `tx0 out0`, with value 1
  - produces two outputs:
    - `out0` for value 0.5
    - `out1` for value 0.3
  - this means that there was 0.2 left over from the input. This value will be given to the miner that mines this transaction.

  Since this is a regular transaction, no new coins are produced.
- `tx2`: regular transaction with a single input and a single output. It uses up the entire input, leading to 0 miner fees, so this greedy one might (will?) never get mined.
- `tx3`: regular transaction with two inputs and one output. The total input is 2.3, and the output is 1.8, so the miner fee will be 0.5

<a id="code-sample-bitcoin-transaction-graph"></a>
```
                   tx1                     tx3
  tx0            +---------------+       +---------------+
+----------+     | in0           |       | in0           |
| out0     |<------out: tx0 out0 |  +------out: tx1 out1 |
| value: 1 |     +---------------+  |    +---------------+
+----------+     | out0          |  |    | in1           |
| out1     |<-+  | value: 0.5    |  | +----out: tx2 out0 |
| value: 2 |  |  +---------------+  | |  +---------------+
+----------+  |  | out1          |<-+ |  | out1          |
              |  | value: 0.3    |    |  | value: 1.8    |
              |  +---------------+    |  +---------------+
              |                       |
              |                       |
              |                       |
              |    tx2                |
              |  +---------------+    |
              |  | in0           |    |
              +----out: tx0 out1 |    |
                 +---------------+    |
                 | out0          |<---+
                 | value: 2      |
                 +---------------+
```

Since every input must come from a previous output, there must be some magic way of generating new coins from scratch to bootstrap the system. This mechanism is that when the miner mines successfully, they get a mining fee, which is a magic transaction without any valid inputs and a pre-agreed value, and an incentive to use their power/compute resources to mine. This magic transaction is called a "[coinbase transaction](https://en.bitcoin.it/wiki/Coinbase)".

The key innovation of Bitcoin is how to prevent double spending, i.e. use a single output as the input of two different transactions, via mining.

For example, what prevents me from very quickly using a single output to pay two different people in quick succession?

The solution are the blocks. Blocks [discretize](discretization.md) transactions into chunks in a way that prevents double spending.

A block contains:
- a list of transactions that are valid amongst themselves. Notably, there can't be double spending within a block.

  People making transactions send them to the network, and miners select which ones they want to add to their block. Miners prefer to pick transactions that are:
  - small, as less bytes means less hashing costs. Small generally means "doesn't have a gazillion inputs/outputs".
  - have higher transaction fees, for obvious reasons
- the ID of its parent block. Blocks therefore form a linear linked list of blocks, except for temporary ties that are soon resolved. The longest known list block is considered to be the valid one.
- a nonce, which is an integer chosen "arbitrarily by the miner"

For a block to be valid, besides not containing easy to check stuff like double spending, the miner must also select a nonce such that the hash of the block starts with N zeroes.

For example, considering the transactions from [Code 1. "Sample Bitcoin transaction graph"](#code-sample-bitcoin-transaction-graph), the block structure shown at [Code 2. "Sample Bitcoin blockchain"](#code-sample-bitcoin-blockchain) would be valid. In it `block0` contains two transactions: `tx0` and `tx1`, and `block1` also contains two transactions: `tx2` and `tx3`.

<a id="code-sample-bitcoin-blockchain"></a>

```
 block0           block1             block2
+------------+   +--------------+   +--------------+
| prev:      |<----prev: block0 |<----prev: block1 |
+------------+   +--------------+   +--------------+
| txs:       |   | txs:         |   | txs:         |
| - tx0      |   | - tx2        |   | - tx4        |
| - tx1      |   | - tx3        |   | - tx5        |
+------------+   +--------------+   +--------------+
| nonce: 944 |   | nonce: 832   |   | nonce: 734   |
+------------+   +--------------+   +--------------+
```
The `nonce`s are on this example arbitrary chosen numbers that would lead to a desired hash for the block.

`block0` is the [Genesis block](genesis-block.md), which is magic and does not have a previous block, because we have to start from somewhere. The network is hardcoded to accept that as a valid starting point.

Now suppose that the person who created `tx2` had tried to double spend and also created another transaction `tx2'` at the same time that looks like this:
```
  tx2'
+---------------+
| in0           |
| out: tx0 out1 |
+---------------+
| out0          |
| value: 2      |
+---------------+
```
Clearly, this transaction would try to spend `tx0 out1` one more time in addition to `tx2`, and should not be allowed! If this were attempted, only the following outcomes are possible:
- `block1` contains `tx2`. Then when `block2` gets made, it cannot contain `tx2'`, because `tx0 out1` was already spent by `tx2`
- `block1` contains `tx2'`. `tx2` cannot be spent anymore
Notably, it is not possible that `block1` contains both `tx2` and `tx2'`, as that would make the block invalid, and the network would not accept that block even if a miner found a `nonce`.

Since hashes are basically random, miners just have to try a bunch of nonces randomly until they find one that works.

The more zeroes, the harder it is to find the hash. For example, on the extreme case where N is all the bits of the hash output, we are trying to find a hash of exactly 0, which is statistically impossible. But if e.g. N=1, you will in average have to try only two nonces, N=2 four nonces, and so on.

The value N is updated every 2 weeks, and aims to make blocks to take 10 minutes to mine on average. N has to be increased with time, as more advanced hashing hardware has become available.

Once a miner finds a nonce that works, they send their block to the network. Other miners then verify the block, and once they do, they are highly incentivized to stop their hashing attempts, and make the new valid block be the new parent, and start over. This is because the length of the chain has already increased: they would need to mine two blocks instead of one if they didn't update to the newest block!

Therefore if you try to double spend, some random miner is going to select only one of your transactions and add it to the block.

They can't pick both, otherwise their block would be invalid, and other miners wouldn't accept is as the new longest one.

Then sooner or later, the transaction will be mined and added to the longest chain. At this point, the network will move to that newer header, and your second transaction will not be valid for any miner at all anymore, since it uses a spent output from the first one that went in. All miners will therefore drop that transaction, and it will never go in.

The goal of having this mandatory 10 minutes block interval is to make it very unlikely that two miners will mine at the exact same time, and therefore possibly each one mine one of the two double spending transactions. When ties to happen, miners randomly choose one of the valid blocks and work on top of it. The first one that does, now has a block of length L + 2 rather than L + 1, and therefore when that is propagated, everyone drops what they are doing and move to that new longest one.

Bibliography:
- [https://arstechnica.com/tech-policy/2020/12/how-bitcoin-works/](https://arstechnica.com/tech-policy/2020/12/how-bitcoin-works/)

**Table of contents**

- [Bitcoin script](bitcoin-script.md)
  - [Bitcoin script debugger](bitcoin-script-debugger.md)
    - [btcdeb](btcdeb.md)
  - [Puzzle script](puzzle-script.md)
    - [Bitcoin hash puzzle script](bitcoin-hash-puzzle-script.md)
    - [Finding unspent puzzle scripts](finding-unspent-puzzle-scripts.md)
      - [BSHUNTER: Detecting and Tracing Defects of Bitcoin Scripts](bshunter-detecting-and-tracing-defects-of-bitcoin-scripts.md)
  - [Bitcoin script type](bitcoin-script-type.md)
    - [Multisig](multisig.md)
    - [P2PKH](p2pkh.md)
    - [P2SH](p2sh.md)
    - [Bitcoin non-standard transaction](bitcoin-non-standard-transaction.md)
      - [An overview of recent non-standard Bitcoin transactions by 0xB10C](an-overview-of-recent-non-standard-bitcoin-transactions-by-0xb10c.md)
      - [Invalid Bitcoin transaction script](invalid-bitcoin-transaction-script.md)
        - [OP\_INVALIDOPCODE](op-invalidopcode.md)
          - [77822fd6663c665104119cb7635352756dfc50da76a92d417ec1a12c518fad69](77822fd6663c665104119cb7635352756dfc50da76a92d417ec1a12c518fad69.md)
      - [Peter Todd's hash collision puzzles](peter-todd-s-hash-collision-puzzles.md)
        - [Peter Todd](peter-todd.md)
      - [Bitcoin script that terminates with multiple values on the stack](bitcoin-script-that-terminates-with-multiple-values-on-the-stack.md)
        - [3ad6677303fb6f700a4f2f977fe86e5324e0ddb0d3b33a649e513d7e88904e85](3ad6677303fb6f700a4f2f977fe86e5324e0ddb0d3b33a649e513d7e88904e85.md)
      - [Provably unspendable Bitcoin output script](provably-unspendable-bitcoin-output-script.md)
        - [4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af](4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af.md)
          - [a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24](a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24.md)
        - [5660d06bd69326c18ec63127b37fb3b32ea763c3846b3334c51beb6a800c57d3](5660d06bd69326c18ec63127b37fb3b32ea763c3846b3334c51beb6a800c57d3.md)
    - [Invalid Bitcoin script](invalid-bitcoin-script.md)
  - [Bitcoin script operator](bitcoin-script-operator.md)
    - [OP\_RETURN](op-return.md)
  - [Bitcoin input script](bitcoin-input-script.md)
  - [Bitcoin output script](bitcoin-output-script.md)
- [Change (Bitcoin)](change-bitcoin.md)
- [Bitcoin mining reward](bitcoin-mining-reward.md)
  - [Bitcoin halving](bitcoin-halving.md)

## ↑ Ancestors (9)

1. [Bitcoin](bitcoin.md)
2. [List of cryptocurrencies](list-of-cryptocurrencies.md)
3. [Cryptocurrency](cryptocurrency-split.md)
4. [Blockchain](blockchain.md)
5. [Money](money.md)
6. [Social technology](social-technology-split.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Bitcoin](bitcoin.md)
- [Digital signature](digital-signature.md)
