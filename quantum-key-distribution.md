# Quantum key distribution

↑ **Parent:** [Quantum information](quantum-information.md)  
🏷️ **Tags:** [Cryptography](cryptography-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quantum_key_distribution)

Man-in-the-middle attack

[https://quantumcomputing.stackexchange.com/questions/142/advantage-of-quantum-key-distribution-over-post-quantum-cryptography/25727#25727](https://quantumcomputing.stackexchange.com/questions/142/advantage-of-quantum-key-distribution-over-post-quantum-cryptography/25727#25727) Advantage of quantum key distribution over post-quantum cryptography has [Ciro Santilli](ciro-santilli-split.md)'s comparison to classical encryption.

[BB84](bb84.md) is a good first algorithm to look into.

Long story short:
- QKD allows you to generate shared keys without [public-key cryptography](public-key-cryptography.md). You can then use thses shared keys
- QKD requires authentication on a classical channel, exactly like a classical [public-key cryptography](public-key-cryptography.md) [forward secrecy](forward-secrecy.md) would. The simplest way to do this is a with a [pre-shared key](pre-shared-key.md), just like in classical public key cryptography. If that key is compromised at any point, your future messages can get [man-in-the-middle](man-in-the-middle-attack.md)'d, exactly like in classical cryptography.

QKD uses [quantum mechanics](quantum-mechanics-split.md) stuff to allow sharing unsnoopable keys: you can detect any snooping and abort communication. Unsnoopability is guaranteed by the known [laws of physics](law-of-physics.md), up only to engineering imperfections.

Furthermore, it allows this [key](key-cryptography.md) distribution without having to physically take a box by car somewhere: once the channel is established, e.g. [optical fiber](optical-fiber.md), you can just keep generating perfect keys from it. Otherwise it would be pointless, as you could just drive your [one-time pad](one-time-pad.md) key every time.

However, the keys likely have a limited rate of generation, so you can't just [one-time pad](one-time-pad.md) the entire message, except for small text messages. What you would then do is to use the shared key with [symmetric encryption](symmetric-encryption.md).

Therefore, this setup usually ultimately relies on the idea that we believe that [symmetric encryption](symmetric-encryption.md) is safer than , even though there aren't mathematical safety proofs of either as of 2020.

**Table of contents**

- [Quantum key distribution protocol](quantum-key-distribution-protocol.md)
  - [BB84](bb84.md)
    - [BB86 vs E91](bb86-vs-e91.md)
  - [E91](e91.md)

## ↑ Ancestors (6)

1. [Quantum information](quantum-information.md)
2. [Information](information.md)
3. [Information technology](information-technology.md)
4. [Area of technology](area-of-technology.md)
5. [Technology](technology-split.md)
6. [Ciro Santilli's Homepage](split.md)
