# How to mine Monero

↑ **Parent:** [Monero](monero.md)

[Ubuntu](ubuntu.md) 20.10 as per [https://xmrig.com/docs/miner/build/ubuntu](https://xmrig.com/docs/miner/build/ubuntu):
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

Benchmark on [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md) as per [https://xmrig.com/docs/miner/benchmark](https://xmrig.com/docs/miner/benchmark):
```
./xmrig --bench=1M
```
gives:
```
948.1 h/s
```
which according to the [https://minexmr.com](https://minexmr.com) [mining pool](mining-pool.md) would generate 0.0005 XMR/day, which at the February 2021 rate of 140 USD/XMR is 0.07 USD/day. The minimum payout in that pool is 0.004 XMR so it would take 8 days to reach that.

So clearly, [application-specific integrated circuit](application-specific-integrated-circuit.md) mining is the only viable way of doing this.

Some people considering [Raspberry Pis](raspberry-pi.md) also conclude obviously that it is useless at a 10H/s rate:
- [https://monero.stackexchange.com/questions/6862/could-i-use-a-raspberry-pi-to-mine-monero](https://monero.stackexchange.com/questions/6862/could-i-use-a-raspberry-pi-to-mine-monero)
- [https://raspberrypi.stackexchange.com/questions/49552/the-hashrate-of-the-raspberry-pi-2-and-3/87252#87252](https://raspberrypi.stackexchange.com/questions/49552/the-hashrate-of-the-raspberry-pi-2-and-3/87252#87252)

[https://www.makeuseof.com/cryptos-you-can-mine-at-home/](https://www.makeuseof.com/cryptos-you-can-mine-at-home/) is a completely full of bullshit article that says otherwise. How can someone publish that!

## ↑ Ancestors (9)

1. [Monero](monero.md)
2. [List of cryptocurrencies](list-of-cryptocurrencies.md)
3. [Cryptocurrency](cryptocurrency-split.md)
4. [Blockchain](blockchain.md)
5. [Money](money.md)
6. [Social technology](social-technology-split.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
