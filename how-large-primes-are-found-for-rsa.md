# How large primes are found for RSA

↑ **Parent:** [RSA (cryptosystem)](rsa-cryptosystem.md)

- [https://crypto.stackexchange.com/questions/1970/how-are-primes-generated-for-rsa](https://crypto.stackexchange.com/questions/1970/how-are-primes-generated-for-rsa)
- [https://crypto.stackexchange.com/questions/690/can-i-select-a-large-random-prime-using-this-procedure/693#693](https://crypto.stackexchange.com/questions/690/can-i-select-a-large-random-prime-using-this-procedure/693#693)

Answers suggest hat you basically pick a random large odd number, and add 2 to it until your selected [primality test](primality-test.md) passes.

The [prime number theorem](prime-number-theorem.md) tells us that the probability that a number between 1 and $N$ is a prime number is $1/log(N)$.

Therefore, for an N-bit integer, we only have to run the test N times on average to find a prime.

Since say, A 512-bit integer is already humongous and sufficiently large, we would only need to search 512 times on average even for such sizes, and therefore the procedure scales well.

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

## ← Incoming links (1)

- [RSA (cryptosystem)](rsa-cryptosystem.md)
