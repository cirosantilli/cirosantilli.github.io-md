# RSA vs Diffie-Hellman

↑ **Parent:** [RSA (cryptosystem)](rsa-cryptosystem.md)

[RSA](rsa-cryptosystem.md) vs [Diffie-Hellman key exchange](diffie-hellman-key-exchange.md) are the dominant [public-key cryptography](public-key-cryptography.md) systems as of 2020, so it is natural to ask how they compare:
- [https://security.stackexchange.com/questions/35471/is-there-any-particular-reason-to-use-diffie-hellman-over-rsa-for-key-exchange](https://security.stackexchange.com/questions/35471/is-there-any-particular-reason-to-use-diffie-hellman-over-rsa-for-key-exchange)
- [https://crypto.stackexchange.com/questions/2867/whats-the-fundamental-difference-between-diffie-hellman-and-rsa](https://crypto.stackexchange.com/questions/2867/whats-the-fundamental-difference-between-diffie-hellman-and-rsa)
- [https://crypto.stackexchange.com/questions/797/is-diffie-hellman-mathematically-the-same-as-rsa](https://crypto.stackexchange.com/questions/797/is-diffie-hellman-mathematically-the-same-as-rsa)

As its name indicates, [Diffie-Hellman key exchange](diffie-hellman-key-exchange.md) is a [key exchange](key-exchange.md) algorithm. TODO verify: this means that in order to transmit a message, both parties must first send data to one another to reach a shared secret key. For RSA on the other hand, you can just take the public key of the other party and send encrypted data to them, the receiver does not need to send you any data at any point.

## ↑ Ancestors (11)

1. [RSA (cryptosystem)](rsa-cryptosystem.md)
2. [Public-key cryptosystem](public-key-cryptosystem.md)
3. [Public-key cryptography](public-key-cryptography.md)
4. [Symmetric and public-key cryptography](symmetric-and-public-key-cryptography.md)
5. [Cryptography](cryptography-split.md)
6. [Computer science](computer-science-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
