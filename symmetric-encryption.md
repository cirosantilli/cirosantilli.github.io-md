# Symmetric encryption

↑ **Parent:** [Symmetric and public-key cryptography](symmetric-and-public-key-cryptography.md)

Symmetric encryption is a type of [encryption](encryption.md) where you use a password (also known as a "key") to encrypt your data, and then the same password to decrypt the data.

For example, this is the type of encryption that is used for encrypting the data in our [smartphones](smartphone.md) and [laptops](laptop.md) with [disk encryption](disk-encryption.md).

This way, if your laptop gets stolen, the thief is not able to see your private photos without knowing your password, even though they are able to read every byte of your disk.

The downside is that that you have to type your password every time you want to login. This leads people to want to use shorter passwords, which in turn are more prone to [password cracking](password-cracking.md).

The other main type of encryption is [public-key cryptography](public-key-cryptography.md).

The advantage of [public-key cryptography](public-key-cryptography.md) is that it allows you to send secret messages to other people even an the attacker is able to capture the encrypted messages. This is for example what you want to do when sending a personal message to a friend over the [Internet](internet.md). Such [encryption](encryption.md) is especially crucial when using [wireless communication](wireless.md) such as [Wi-Fi](wi-fi.md), where anyone nearby can capture the signals you send and receive, and would be able to read all your data if it weren't encrypted.

Easily sending encrypted messages over the [Internet](internet.md) is not possible with [symmetric encryption](symmetric-encryption.md) because for your friend to decrypt the message in that system, you'd need to send them the password, which the attacker would also be able to eavesdrop and then decrypt the message that follows using it. The problem of sharing a password with another person online is called [key exchange](key-exchange.md).

[Advanced Encryption Standard](advanced-encryption-standard.md) (AES) is one of the most popular families of [symmetric encryption](symmetric-encryption.md) algorithms.

[OpenSSL](openssl.md) is a popular [open source](open-source-software.md) implementation of [symmetric and public-key cryptography](symmetric-and-public-key-cryptography.md). A simple example of using [OpenSSL](openssl.md) for [symmetric encryption](symmetric-encryption.md) from the [command-line](command-line-interface.md) is:
```
echo 'Hello World!' > message.txt
openssl aes-256-cbc -a -salt -pbkdf2 -in message.txt -out message.txt.enc
```
This asks for a password, which we set as `asdfqwer`, and then produces a file `message.txt.enc` containing garbled text such that:
```
hd message.txt.enc
```
contains:
```
00000000  55 32 46 73 64 47 56 6b  58 31 38 58 48 65 2f 30  |U2FsdGVkX18XHe/0|
00000010  70 56 42 2b 70 45 6c 55  59 38 2b 54 38 7a 4e 34  |pVB+pElUY8+T8zN4|
00000020  4e 37 6d 52 2f 73 6d 4d  62 64 30 3d 0a           |N7mR/smMbd0=.|
0000002d
```
Then to decrypt:
```
openssl aes-256-cbc -d -a -pbkdf2 -in message.txt.enc -out message.new.txt
```
once again asks for your password and given the correct password produces a file `message.new.txt` containing the original message:
```
Hello World!
```
This was tested on [Ubuntu 24.04](ubuntu-24-04.md), OpenSSL 3.0.13. See also: [How to use OpenSSL to encrypt/decrypt files? on Stack Overflow](https://stackoverflow.com/questions/16056135/how-to-use-openssl-to-encrypt-decrypt-files).

There is no [provably secure symmetric-key algorithm](provably-secure-symmetric-key-algorithm.md) besides the [one-time pad](one-time-pad.md), which has the serious drawback of requiring the key to be as long as the message. This means that we believe that most encryption algorithms are secure because it is a hugely valuable target and no one has managed to crack them yet. But we don't have a mathematical proof that they are actually secure, so they could in theory be broken by new algorithms one day.

**Table of contents**

- [Provably secure symmetric-key algorithm](provably-secure-symmetric-key-algorithm.md)
- [One-time pad](one-time-pad.md)
- [Symmetric-key algorithm](symmetric-key-algorithm.md)
  - [Advanced Encryption Standard](advanced-encryption-standard.md)
    - [Is AES quantum resistant?](is-aes-quantum-resistant.md)

## ↑ Ancestors (8)

1. [Symmetric and public-key cryptography](symmetric-and-public-key-cryptography.md)
2. [Cryptography](cryptography-split.md)
3. [Computer science](computer-science-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (4)

- [Pre-shared key](pre-shared-key.md)
- [Quantum key distribution](quantum-key-distribution.md)
- [Symmetric encryption](symmetric-encryption.md)
- [Symmetric-key algorithm](symmetric-key-algorithm.md)
