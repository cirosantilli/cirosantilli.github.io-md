# RSA (cryptosystem)

↑ **Parent:** [Public-key cryptosystem](public-key-cryptosystem.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RSA_(cryptosystem))

Based on the fact that we don't have a [P](p-complexity.md) algorithm for [integer factorization](integer-factorization.md) as of 2020. But nor proof that one does not exist!

The private key is made of two randomly generated prime numbers: $p$ and $q$. How such large primes are found: [how large primes are found for RSA](how-large-primes-are-found-for-rsa.md).

The public key is made of:
- `n = p*q`
- a randomly chosen integer exponent $e$ between `1` and `e_max = lcm(p -1, q -1)`, where `lcm` is the [Least common multiple](least-common-multiple.md)

Given a plaintext message `m`, the encrypted [ciphertext](ciphertext.md) version is:
```
c = m^e mod n
```
This operation is called [modular exponentiation](modular-exponentiation.md) can be calculated efficiently with the [Extended Euclidean algorithm](extended-euclidean-algorithm.md).

The inverse operation of finding the private `m` from the public `c`, `e` and $n$ is however believed to be a hard problem without knowing the factors of `n`.

However, if we know the private `p` and `q`, we can solve the problem. As follows.

First we calculate the [modular multiplicative inverse](modular-multiplicative-inverse.md). TODO continue.

Bibliography:
- [https://www.comparitech.com/blog/information-security/rsa-encryption/](https://www.comparitech.com/blog/information-security/rsa-encryption/) has a numeric example

**Table of contents**

- [How large primes are found for RSA](how-large-primes-are-found-for-rsa.md)
- [RSA vs Diffie-Hellman](rsa-vs-diffie-hellman.md)

## ↑ Ancestors (10)

1. [Public-key cryptosystem](public-key-cryptosystem.md)
2. [Public-key cryptography](public-key-cryptography.md)
3. [Symmetric and public-key cryptography](symmetric-and-public-key-cryptography.md)
4. [Cryptography](cryptography-split.md)
5. [Computer science](computer-science-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Integer factorization](integer-factorization.md)
- [NP-hard cryptosystem](np-hard-cryptosystem.md)
- [Post-quantum cryptography](post-quantum-cryptography.md)
- [RSA vs Diffie-Hellman](rsa-vs-diffie-hellman.md)
