# Post-quantum cryptography

↑ **Parent:** [Quantum computing](quantum-computing-split.md)  
🏷️ **Tags:** [Cryptography](cryptography-split.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Post-quantum_cryptography)

[Encryption algorithms](cryptosystem.md) that run on [classical computers](classical-computer.md) that are expected to be resistant to [quantum computers](quantum-computing-split.md).

This is notably not the case of the dominant 2020 algorithms, [RSA](rsa-cryptosystem.md) and [elliptic curve cryptography](elliptic-curve-cryptography.md), which are provably broken by [Grover's algorithm](grover-s-algorithm.md).

However, as of 2020, we [don't have any proof that any symmetric or public key algorithm is quantum resistant](provably-quantum-secure-encryption-algorithm.md).

Post-quantum cryptography is the very first quantum computing thing at which people have to put money into.

The reason is that attackers would be able to store captured [ciphertext](ciphertext.md), and then retroactively break them once and if [quantum computing](quantum-computing-split.md) power becomes available in the future.

There isn't a shade of a doubt that [intelligence agencies](intelligence-agency.md) are actively doing this as of 2020. They must have a database of how interesting a given source is, and then store as much as they can given some ammount of storage budget they have available.

A good way to explain this to [quantum computing skeptics](quantum-computing-skepticism.md) is to ask them:

> If I told you there is a 5% chance that I will be able to decrypt everything you write online starting today in 10 years. Would you give me a dollar to reduce that chance to 0.5%?

Post-quantum cryptography is simply not a choice. It must be done now. Even if the risk is low, the cost would be way too great.

**Table of contents**

- [Post-quantum cryptography company](post-quantum-cryptography-company.md)
  - [CryptoNext](cryptonext.md)
  - [PQShield](pqshield.md)
- [NIST Post-Quantum Cryptography Standardization](nist-post-quantum-cryptography-standardization.md)
- [Provably quantum secure encryption algorithm](provably-quantum-secure-encryption-algorithm.md)
- [Quantum resistant cryptosystem](quantum-resistant-cryptosystem.md)
  - [Lattice-based cryptography](lattice-based-cryptography.md)

## ↑ Ancestors (7)

1. [Quantum computing](quantum-computing-split.md)
2. [Quantum information](quantum-information.md)
3. [Information](information.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Authentication (cryptography)](authentication-cryptography.md)
- [NIST Post-Quantum Cryptography Standardization](nist-post-quantum-cryptography-standardization.md)
- [PQShield](pqshield.md)
- [Quantum algorithm](quantum-algorithm.md)
