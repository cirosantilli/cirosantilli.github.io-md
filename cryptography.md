# Cryptography

↑ **Parent:** [Computer science](computer-science.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cryptography)

**Table of contents**

- [Cryptosystem](#cryptosystem)
- [Random number generation](#random-number-generation)
  - [Hardware random number generation](#hardware-random-number-generation)
- [Symmetric and public-key cryptography](#symmetric-and-public-key-cryptography)
  - [Symmetric encryption](#symmetric-encryption)
    - [Provably secure symmetric-key algorithm](#provably-secure-symmetric-key-algorithm)
    - [One-time pad](#one-time-pad)
    - [Symmetric-key algorithm](#symmetric-key-algorithm)
      - [Advanced Encryption Standard](#advanced-encryption-standard)
        - [Is AES quantum resistant?](#is-aes-quantum-resistant)
  - [Public-key cryptography](#public-key-cryptography)
    - [Digital signature](#digital-signature)
    - [Ring signature](#ring-signature)
    - [Public-key cryptosystem](#public-key-cryptosystem)
      - [RSA (cryptosystem)](#rsa-cryptosystem)
        - [How large primes are found for RSA](#how-large-primes-are-found-for-rsa)
        - [RSA vs Diffie-Hellman](#rsa-vs-diffie-hellman)
    - [Diffie-Hellman key exchange](#diffie-hellman-key-exchange)
      - [Key exchange](#key-exchange)
    - [Elliptic curve cryptography](#elliptic-curve-cryptography)
      - [Elliptic-curve Diffie-Hellman](#elliptic-curve-diffie-hellman)
        - [Diffie-Hellman vs ECDH](#diffie-hellman-vs-ecdh)
- [Encryption](#encryption)
  - [Encryption software](#encryption-software)
    - [OpenSSL](#openssl)
  - [Steganography](#steganography)
  - [Deniable authentication](#deniable-authentication)
  - [End-to-end encryption](#end-to-end-encryption)
  - [Forward secrecy](#forward-secrecy)
  - [Disk encryption](#disk-encryption)
    - [Can a smartphone's PIN or password be brute-forced in an offline attack?](#can-a-smartphone-s-pin-or-password-be-brute-forced-in-an-offline-attack)
    - [Linux Unified Key Setup](#linux-unified-key-setup)
    - [Disk encryption password handover plausible deniability](#disk-encryption-password-handover-plausible-deniability)
- [GNU Privacy Guard](#gnu-privacy-guard)
- [Internet privacy](#internet-privacy)
  - [Anonymity](#anonymity)
    - [Receiving an anonymous donation](#receiving-an-anonymous-donation)
      - [Receiving an anonymous donation in the UK](#receiving-an-anonymous-donation-in-the-uk)
  - [Internet privacy organizations](#internet-privacy-organizations)
    - [Riseup](#riseup)
  - [Operations security](#operations-security)
  - [Internet privacy technology](#internet-privacy-technology)
    - [I2P](#i2p)
      - [I2P on Ubuntu](#i2p-on-ubuntu)
        - [I2P on Ubuntu browser setup](#i2p-on-ubuntu-browser-setup)
        - [I2P Ubuntu via PPA](#i2p-ubuntu-via-ppa)
    - [Tor (anonymity network)](#tor-anonymity-network)
      - [Tor Browser](#tor-browser)
      - [Onion service](#onion-service)
        - [Dark web](#dark-web)
        - [Hidden Answers](#hidden-answers)
        - [Onion service search engine](#onion-service-search-engine)
          - [Uncensored Onion service search engine](#uncensored-onion-service-search-engine)
            - [Tor.link](#tor-link)
      - [The Hidden Wiki](#the-hidden-wiki)
      - [Can ISPs deanonymize Tor users based on timestamps of public posts?](#can-isps-deanonymize-tor-users-based-on-timestamps-of-public-posts)
- [Ciphertext, plaintext, key and salt](#ciphertext-plaintext-key-and-salt)
  - [Ciphertext](#ciphertext)
  - [Key (cryptography)](#key-cryptography)
    - [Pre-shared key](#pre-shared-key)
      - [Message authentication code](#message-authentication-code)
- [Man-in-the-middle attack](#man-in-the-middle-attack)
  - [Authentication (cryptography)](#authentication-cryptography)
- [Zero-knowledge proof](#zero-knowledge-proof)
  - [Zero-knowledge proof vs digital signature](#zero-knowledge-proof-vs-digital-signature)

## Cryptosystem

↑ **Parent:** [Cryptography](cryptography.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cryptosystem)

## Random number generation

↑ **Parent:** [Cryptography](cryptography.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Random_number_generation)

### Hardware random number generation

↑ **Parent:** [Random number generation](#random-number-generation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hardware_random_number_generation)

## Symmetric and public-key cryptography

↑ **Parent:** [Cryptography](cryptography.md)

### Symmetric encryption

↑ **Parent:** [Symmetric and public-key cryptography](#symmetric-and-public-key-cryptography)

Symmetric encryption is a type of [encryption](#encryption) where you use a password (also known as a "key") to encrypt your data, and then the same password to decrypt the data.

For example, this is the type of encryption that is used for encrypting the data in our [smartphones](computer-hardware.md#smartphone) and [laptops](computer-hardware.md#laptop) with [disk encryption](#disk-encryption).

This way, if your laptop gets stolen, the thief is not able to see your private photos without knowing your password, even though they are able to read every byte of your disk.

The downside is that that you have to type your password every time you want to login. This leads people to want to use shorter passwords, which in turn are more prone to [password cracking](software.md#password-cracking).

The other main type of encryption is [public-key cryptography](#public-key-cryptography).

The advantage of [public-key cryptography](#public-key-cryptography) is that it allows you to send secret messages to other people even an the attacker is able to capture the encrypted messages. This is for example what you want to do when sending a personal message to a friend over the [Internet](computer.md#internet). Such [encryption](#encryption) is especially crucial when using [wireless communication](telecommunication.md#wireless) such as [Wi-Fi](computer.md#wi-fi), where anyone nearby can capture the signals you send and receive, and would be able to read all your data if it weren't encrypted.

Easily sending encrypted messages over the [Internet](computer.md#internet) is not possible with [symmetric encryption](#symmetric-encryption) because for your friend to decrypt the message in that system, you'd need to send them the password, which the attacker would also be able to eavesdrop and then decrypt the message that follows using it. The problem of sharing a password with another person online is called [key exchange](#key-exchange).

[Advanced Encryption Standard](#advanced-encryption-standard) (AES) is one of the most popular families of [symmetric encryption](#symmetric-encryption) algorithms.

[OpenSSL](#openssl) is a popular [open source](software.md#open-source-software) implementation of [symmetric and public-key cryptography](#symmetric-and-public-key-cryptography). A simple example of using [OpenSSL](#openssl) for [symmetric encryption](#symmetric-encryption) from the [command-line](software.md#command-line-interface) is:
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
This was tested on [Ubuntu 24.04](systems-programming.md#ubuntu-24-04), OpenSSL 3.0.13. See also: [How to use OpenSSL to encrypt/decrypt files? on Stack Overflow](https://stackoverflow.com/questions/16056135/how-to-use-openssl-to-encrypt-decrypt-files).

There is no [provably secure symmetric-key algorithm](#provably-secure-symmetric-key-algorithm) besides the [one-time pad](#one-time-pad), which has the serious drawback of requiring the key to be as long as the message. This means that we believe that most encryption algorithms are secure because it is a hugely valuable target and no one has managed to crack them yet. But we don't have a mathematical proof that they are actually secure, so they could in theory be broken by new algorithms one day.

#### Provably secure symmetric-key algorithm

↑ **Parent:** [Symmetric encryption](#symmetric-encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Provably_secure_symmetric-key_algorithm)

There aren't any 2020, except in the trivial [one-time pad](#one-time-pad) case where the key is as large as the message: [https://crypto.stackexchange.com/questions/10815/how-do-we-prove-that-aes-des-etc-are-secure](https://crypto.stackexchange.com/questions/10815/how-do-we-prove-that-aes-des-etc-are-secure)

#### One-time pad

↑ **Parent:** [Symmetric encryption](#symmetric-encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/One-time_pad)

The only perfect cryptosystem!

The problem is that you need a shared [key](#key-cryptography) as large as the message.

Systems like [advanced Encryption Standard](#advanced-encryption-standard) allow us to encrypt things larger than the key, but the tradeoff is that they could be possibly broken, as don't have any [provably secure symmetric-key algorithms](#provably-secure-symmetric-key-algorithm) as of 2020.

#### Symmetric-key algorithm

↑ **Parent:** [Symmetric encryption](#symmetric-encryption)

Symmetric-key algorithm is al algorithm implementing [symmetric encryption](#symmetric-encryption).

##### Advanced Encryption Standard

↑ **Parent:** [Symmetric-key algorithm](#symmetric-key-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard)

###### Is AES quantum resistant?

↑ **Parent:** [Advanced Encryption Standard](#advanced-encryption-standard)  
🏷️ **Tags:** [Quantum resistant cryptosystem](quantum-computing.md#quantum-resistant-cryptosystem)

2020-so-far yes, [Grover's algorithm](quantum-computing.md#grover-s-algorithm) would only effectively reduce key sizes by half:
- [https://crypto.stackexchange.com/questions/6712/is-aes-256-a-post-quantum-secure-cipher-or-not](https://crypto.stackexchange.com/questions/6712/is-aes-256-a-post-quantum-secure-cipher-or-not)
- [https://qvault.io/cryptography/is-aes-256-quantum-resistant/](https://qvault.io/cryptography/is-aes-256-quantum-resistant/)
but there isn't a mathematical proof either.

### Public-key cryptography

↑ **Parent:** [Symmetric and public-key cryptography](#symmetric-and-public-key-cryptography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Public-key_cryptography)

It allows you to do two things:
- [encryption](#encryption)
- [digital signature](#digital-signature)

#### Digital signature

↑ **Parent:** [Public-key cryptography](#public-key-cryptography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Digital_signature)

One notable application: [cryptocurrency](cryptocurrency.md), see e.g. [how Bitcoin works](cryptocurrency.md#how-bitcoin-works).

#### Ring signature

↑ **Parent:** [Public-key cryptography](#public-key-cryptography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ring_signature)

Used for example:
- by [Monero](cryptocurrency.md#monero) to hide the input of a transaction
- anonymous [electronic voting](social-technology.md#electronic-voting)

#### Public-key cryptosystem

↑ **Parent:** [Public-key cryptography](#public-key-cryptography)  
🏷️ **Tags:** [Cryptosystem](#cryptosystem)

##### RSA (cryptosystem)

↑ **Parent:** [Public-key cryptosystem](#public-key-cryptosystem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RSA_(cryptosystem))

Based on the fact that we don't have a [P](computer-science.md#p-complexity) algorithm for [integer factorization](computer-science.md#integer-factorization) as of 2020. But nor proof that one does not exist!

The private key is made of two randomly generated prime numbers: $p$ and $q$. How such large primes are found: [how large primes are found for RSA](#how-large-primes-are-found-for-rsa).

The public key is made of:
- `n = p*q`
- a randomly chosen integer exponent $e$ between `1` and `e_max = lcm(p -1, q -1)`, where `lcm` is the [Least common multiple](mathematics.md#least-common-multiple)

Given a plaintext message `m`, the encrypted [ciphertext](#ciphertext) version is:
```
c = m^e mod n
```
This operation is called [modular exponentiation](mathematics.md#modular-exponentiation) can be calculated efficiently with the [Extended Euclidean algorithm](mathematics.md#extended-euclidean-algorithm).

The inverse operation of finding the private `m` from the public `c`, `e` and $n$ is however believed to be a hard problem without knowing the factors of `n`.

However, if we know the private `p` and `q`, we can solve the problem. As follows.

First we calculate the [modular multiplicative inverse](mathematics.md#modular-multiplicative-inverse). TODO continue.

Bibliography:
- [https://www.comparitech.com/blog/information-security/rsa-encryption/](https://www.comparitech.com/blog/information-security/rsa-encryption/) has a numeric example

###### How large primes are found for RSA

↑ **Parent:** [RSA (cryptosystem)](#rsa-cryptosystem)

- [https://crypto.stackexchange.com/questions/1970/how-are-primes-generated-for-rsa](https://crypto.stackexchange.com/questions/1970/how-are-primes-generated-for-rsa)
- [https://crypto.stackexchange.com/questions/690/can-i-select-a-large-random-prime-using-this-procedure/693#693](https://crypto.stackexchange.com/questions/690/can-i-select-a-large-random-prime-using-this-procedure/693#693)

Answers suggest hat you basically pick a random large odd number, and add 2 to it until your selected [primality test](mathematics.md#primality-test) passes.

The [prime number theorem](mathematics.md#prime-number-theorem) tells us that the probability that a number between 1 and $N$ is a prime number is $1/log(N)$.

Therefore, for an N-bit integer, we only have to run the test N times on average to find a prime.

Since say, A 512-bit integer is already humongous and sufficiently large, we would only need to search 512 times on average even for such sizes, and therefore the procedure scales well.

###### RSA vs Diffie-Hellman

↑ **Parent:** [RSA (cryptosystem)](#rsa-cryptosystem)

[RSA](#rsa-cryptosystem) vs [Diffie-Hellman key exchange](#diffie-hellman-key-exchange) are the dominant [public-key cryptography](#public-key-cryptography) systems as of 2020, so it is natural to ask how they compare:
- [https://security.stackexchange.com/questions/35471/is-there-any-particular-reason-to-use-diffie-hellman-over-rsa-for-key-exchange](https://security.stackexchange.com/questions/35471/is-there-any-particular-reason-to-use-diffie-hellman-over-rsa-for-key-exchange)
- [https://crypto.stackexchange.com/questions/2867/whats-the-fundamental-difference-between-diffie-hellman-and-rsa](https://crypto.stackexchange.com/questions/2867/whats-the-fundamental-difference-between-diffie-hellman-and-rsa)
- [https://crypto.stackexchange.com/questions/797/is-diffie-hellman-mathematically-the-same-as-rsa](https://crypto.stackexchange.com/questions/797/is-diffie-hellman-mathematically-the-same-as-rsa)

As its name indicates, [Diffie-Hellman key exchange](#diffie-hellman-key-exchange) is a [key exchange](#key-exchange) algorithm. TODO verify: this means that in order to transmit a message, both parties must first send data to one another to reach a shared secret key. For RSA on the other hand, you can just take the public key of the other party and send encrypted data to them, the receiver does not need to send you any data at any point.

#### Diffie-Hellman key exchange

↑ **Parent:** [Public-key cryptography](#public-key-cryptography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Diffie–Hellman_key_exchange)

Based on the fact that we don't have a [P](computer-science.md#p-complexity) algorithm for the [discrete logarithm of the cyclic group](computer-science.md#discrete-logarithm-of-the-cyclic-group) as of 2020, but we do have an efficient algorithm for [modular exponentiation](mathematics.md#modular-exponentiation). But nor do we have proof that one does not exist! Living on the edge as usual for [public-key cryptography](#public-key-cryptography).

##### Key exchange

↑ **Parent:** [Diffie-Hellman key exchange](#diffie-hellman-key-exchange)

#### Elliptic curve cryptography

↑ **Parent:** [Public-key cryptography](#public-key-cryptography)  
🏷️ **Tags:** [Discrete logarithm](computer-science.md#discrete-logarithm), [Elliptic curve](algebra.md#elliptic-curve)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Elliptic_curve_cryptography)

##### Elliptic-curve Diffie-Hellman

↑ **Parent:** [Elliptic curve cryptography](#elliptic-curve-cryptography)  
🏷️ **Tags:** [Diffie-Hellman key exchange](#diffie-hellman-key-exchange)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Elliptic-curve_Diffie-Hellman)

The algorithm is completely analogous to [Diffie-Hellman key exchange](#diffie-hellman-key-exchange) in that you efficiently raise a number to a power $n$ times and send the result over while keeping $n$ as private key.

The only difference is that a different group is used: instead of using the [cyclic group](group.md#cyclic-group), we use the [elliptic curve group](algebra.md#elliptic-curve-group) of an [elliptic curve over a finite field](algebra.md#elliptic-curve-over-a-finite-field).

<a id="video-elliptic-curves-by-computerphile-2018"></a>
**[Video 1](#video-elliptic-curves-by-computerphile-2018). Elliptic curves by Computerphile (2018)** [Source](https://www.youtube.com/watch?v=NF1pwjL9-DE). [https://youtu.be/NF1pwjL9-DE?t=143](https://youtu.be/NF1pwjL9-DE?t=143) shows the continuous group well, but then fails to explain the discrete part.

Variant of [Diffie-Hellman key exchange](#diffie-hellman-key-exchange) based on [elliptic curve cryptography](#elliptic-curve-cryptography).

###### Diffie-Hellman vs ECDH

↑ **Parent:** [Elliptic-curve Diffie-Hellman](#elliptic-curve-diffie-hellman)

[https://crypto.stackexchange.com/questions/29906/how-does-diffie-hellman-differ-from-elliptic-curve-diffie-hellman](https://crypto.stackexchange.com/questions/29906/how-does-diffie-hellman-differ-from-elliptic-curve-diffie-hellman)

[ECDH](#elliptic-curve-diffie-hellman) has smaller keys. [https://youtu.be/gAtBM06xwaw?t=634](https://youtu.be/gAtBM06xwaw?t=634) mentions some interesting downsides:
- bad curves exist, while in modular, any number seems to work well. TODO why?
- TODO can't find this mentioned anywher else: [Diffie-Hellman key exchange](#diffie-hellman-key-exchange) has a proof that there is no algorithm, [ECDH](#elliptic-curve-diffie-hellman) doesn't. Which proof?

## Encryption

↑ **Parent:** [Cryptography](cryptography.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Encryption)

### Encryption software

↑ **Parent:** [Encryption](#encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Encryption_software)

#### OpenSSL

↑ **Parent:** [Encryption software](#encryption-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/OpenSSL)

### Steganography

↑ **Parent:** [Encryption](#encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Steganography)

### Deniable authentication

↑ **Parent:** [Encryption](#encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Deniable_authentication)

### End-to-end encryption

↑ **Parent:** [Encryption](#encryption)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/End-to-end_encryption)

### Forward secrecy

↑ **Parent:** [Encryption](#encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Forward_secrecy)

[https://stackoverflow.com/questions/20505942/how-does-perfect-forward-secrecy-pfs-work/66118134#66118134](https://stackoverflow.com/questions/20505942/how-does-perfect-forward-secrecy-pfs-work/66118134#66118134)

### Disk encryption

↑ **Parent:** [Encryption](#encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Disk_encryption)

<h4 id="can-a-smartphone-s-pin-or-password-be-brute-forced-in-an-offline-attack">Can a smartphone's PIN or password be brute-forced in an offline attack?</h4>

↑ **Parent:** [Disk encryption](#disk-encryption)

[https://security.stackexchange.com/questions/202174/can-a-smartphones-pin-or-password-be-brute-forced-in-an-offline-attack](https://security.stackexchange.com/questions/202174/can-a-smartphones-pin-or-password-be-brute-forced-in-an-offline-attack)

[Ciro Santilli](ciro-santilli.md) has a hard time understanding why this is possible, e.g. many people use short 4 digit pins, or a short swipe pattern. Why can't this be cracked easily offline?

#### Linux Unified Key Setup

↑ **Parent:** [Disk encryption](#disk-encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup)

#### Disk encryption password handover plausible deniability

↑ **Parent:** [Disk encryption](#disk-encryption)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Disk_encryption_password_handover_plausible_deniability)

- [https://security.stackexchange.com/questions/135846/is-plausible-deniability-actually-feasible-for-encrypted-volumes-disks](https://security.stackexchange.com/questions/135846/is-plausible-deniability-actually-feasible-for-encrypted-volumes-disks)
- [https://security.stackexchange.com/questions/87153/linux-plausibly-deniable-file-system](https://security.stackexchange.com/questions/87153/linux-plausibly-deniable-file-system)

Can we do better than "wrong password implies random bytes"?

Can the last disk access times be checked via forensic methods?

## GNU Privacy Guard

↑ **Parent:** [Cryptography](cryptography.md)  
🏷️ **Tags:** [GNU package](software.md#gnu-package)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GNU_Privacy_Guard)

Generate public private key, test encrypt and test decrypt:
```
# Create your pubkey.
gpg --gen-key
gpg --armor --output pubkey.gpg --export <myemail>

# Encrypt using someone's pubkey.
gpg --import pubkey2.gpg
echo 'hello world' > hello.txt
gpg --output hello.txt.gpg --encrypt --recipient <other-email> hello.txt

# Double check it is not plaintext in the encrypted message.
grep hello hello.txt.gpg

# Decrypt.
gpg --output hello.decrypt.txt --decrypt --recipient <myemail> hello.txt.gpg
diff -u hello.decrypt.txt hello.txt
```

## Internet privacy

↑ **Parent:** [Cryptography](cryptography.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Internet_privacy)

### Anonymity

↑ **Parent:** [Internet privacy](#internet-privacy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Anonymity)

#### Receiving an anonymous donation

↑ **Parent:** [Anonymity](#anonymity)

Closely related:
- [De-banking](economy.md#de-banking)

Bibliography:
- [https://www.quora.com/Is-it-legal-for-billionaires-to-make-anonymous-charitable-donations-How-can-it-be-determined-if-a-large-sum-of-money-was-donated-anonymously-or-not](https://www.quora.com/Is-it-legal-for-billionaires-to-make-anonymous-charitable-donations-How-can-it-be-determined-if-a-large-sum-of-money-was-donated-anonymously-or-not)

##### Receiving an anonymous donation in the UK

↑ **Parent:** [Receiving an anonymous donation](#receiving-an-anonymous-donation)

[Ciro Santilli](ciro-santilli.md)'s experience: [https://www.quora.com/Is-it-legal-for-billionaires-to-make-anonymous-charitable-donations-How-can-it-be-determined-if-a-large-sum-of-money-was-donated-anonymously-or-not/answer/Ciro-Santilli](https://www.quora.com/Is-it-legal-for-billionaires-to-make-anonymous-charitable-donations-How-can-it-be-determined-if-a-large-sum-of-money-was-donated-anonymously-or-not/answer/Ciro-Santilli)

### Internet privacy organizations

↑ **Parent:** [Internet privacy](#internet-privacy)

#### Riseup

↑ **Parent:** [Internet privacy organizations](#internet-privacy-organizations)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Riseup)

### Operations security

↑ **Parent:** [Internet privacy](#internet-privacy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Operations_security)

### Internet privacy technology

↑ **Parent:** [Internet privacy](#internet-privacy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Internet_privacy_technology)

#### I2P

↑ **Parent:** [Internet privacy technology](#internet-privacy-technology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/I2P)

[https://en.wikipedia.org/wiki/I2P](https://en.wikipedia.org/wiki/I2P)

Seems very similar to [Tor](#tor-anonymity-network), but also supports anonymous sharing of large files, notably via [BitTorrent](software.md#bittorrent), which [Tor](#tor-anonymity-network) does not support well. Shame.

##### I2P on [Ubuntu](systems-programming.md#ubuntu)

↑ **Parent:** [I2P](#i2p)

On [Ubuntu 26.04](systems-programming.md#ubuntu-26-04), visiting [https://i2p.net/en/downloads/](https://i2p.net/en/downloads/) recommended me to download [https://files.i2p.net/2.12.0/i2pinstall_2.12.0.jar](https://files.i2p.net/2.12.0/i2pinstall_2.12.0.jar) so I did:
```
cd ~
wget https://files.i2p.net/2.12.0/i2pinstall_2.12.0.jar
sudo apt install openjdk-17-jre
JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64 PATH="$JAVA_HOME/bin:$PATH" java -jar ./i2pinstall_2.12.0.jar -console
```
Then after some clicking faff
```
cd ~/i2p
JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64 PATH="$JAVA_HOME/bin:$PATH" ./i2prouter start
```
and it told me:
```
Starting I2P Service...
Waiting for I2P Service....
running: PID:423806
```
and it automatically opened up a Chrome tab at: [http://127.0.0.1:7657/welcome](http://127.0.0.1:7657/welcome)

The default Java 8 installed on my machine is too old, needed 17 or above. Very annoying.

To make things more bearable I added this to my `.bashrc`:

```
i2p() (
  cd ~/i2p
  JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64 PATH="$JAVA_HOME/bin:$PATH" ./i2prouter "$@"
)
```

so I can just:

```
i2p start
i2p stop
```

###### I2P on [Ubuntu](systems-programming.md#ubuntu) browser setup

↑ **Parent:** [I2P on Ubuntu](#i2p-on-ubuntu)

It does not come with a default browser... A popular option seems to be to install a praivate browser such as LibreWolf (Firefox based) to be your I2P thing [https://www.youtube.com/watch?v=qFE1J9YhhWg](https://www.youtube.com/watch?v=qFE1J9YhhWg) Setting it up as such makes it not work as a regular clearnet browser. Instructions at: [https://librewolf.net/installation/debian/](https://librewolf.net/installation/debian/)

```
sudo apt update && sudo apt install extrepo -y
sudo extrepo enable librewolf && sudo extrepo update librewolf
sudo apt update && sudo apt install librewolf -y
```

Then go to Proxy settings and set Manual proxy configuration:

- HTTP Proxy: 127.0.0.1:4444
- SOCKS Host: 127.0.0.1:4447

Another setting you really want in LibreWolf is:

> Don't enable HTTPS-Only Mode

otherwise it keeps complaining every time that pages are not https, because they are all http, because the security is happening at a lower layer of the protocol already. 

Then I can visit the sample website [http://tracker2.postman.i2p.](http://tracker2.postman.i2p.) It complains that it's not https, but I say, OK, I think I'm already mega encrypted figers crossed. It is a simple oldschool forum like phpBB where people announce their I2P compatible Torrents. From the posts I can copy a Magnet link and add it to [http://127.0.0.1:7657/i2psnark/,](http://127.0.0.1:7657/i2psnark/,) the built-in Torrent thing, the only convenient thing they have pre-setup for you :-)

Shame setting up this project is so difficult, it can never reach mainstream like this. Tor Browser and centralized VPN are so much more streamlined. But if it were mainstream, it would be boring? Early 200ss vibes come to mind.

###### I2P [Ubuntu](systems-programming.md#ubuntu) via PPA

↑ **Parent:** [I2P on Ubuntu](#i2p-on-ubuntu)

[https://i2p.net/en/docs/guides/installing-i2p-on-debian-and-ubuntu/](https://i2p.net/en/docs/guides/installing-i2p-on-debian-and-ubuntu/) documents the experimental PPA method:

```
sudo apt-add-repository ppa:i2p-maintainers/i2p
sudo apt-get update
sudo apt-get install i2p
```

but then when I ran:

```
i2prouter start
```

it fails with:

```
Starting I2P Service...
Removed stale pid file: /home/ciro/.i2p/i2p.pid
Waiting for I2P Service.....
WARNING: I2P Service may have failed to start.
```

Meh?

#### Tor (anonymity network)

↑ **Parent:** [Internet privacy technology](#internet-privacy-technology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tor_(anonymity_network))

##### Tor Browser

↑ **Parent:** [Tor (anonymity network)](#tor-anonymity-network)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tor_Browser)

##### Onion service

↑ **Parent:** [Tor (anonymity network)](#tor-anonymity-network)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/en.wikipedia.org/wiki/Tor_(network)#Onion_services)

This is a way to host a server that actually hide the [IP](computer.md#ip-address) of the server from the client, just like [Tor](#tor-anonymity-network) hides the [IP](computer.md#ip-address) of the client from the server. Amazing tecnology!

This is why it enables hosting [illegal](law.md) things like the [Silk Road](computer.md#silk-road-marketplace): [law enforcement](law.md#law-enforcement) is not able find where the server is hosted, and take it down or identify the owner.

Bibliography:
- [https://security.stackexchange.com/questions/38194/how-can-i-get-the-ip-address-for-a-tor-hidden-service-hs-with-a-onion-address](https://security.stackexchange.com/questions/38194/how-can-i-get-the-ip-address-for-a-tor-hidden-service-hs-with-a-onion-address)

###### Dark web

↑ **Parent:** [Onion service](#onion-service)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dark_web)

###### Hidden Answers

↑ **Parent:** [Onion service](#onion-service)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hidden_Answers)

[https://www.reddit.com/r/onions/comments/sfquss/hidden_answers_is_back/](https://www.reddit.com/r/onions/comments/sfquss/hidden_answers_is_back/) gives pbqttnffb5sh6ckgnz4f5by55w25gd6tuw5f5qcctmnyk62eyhgx6rad.onion which is Dead Janary 2024

###### Onion service search engine

↑ **Parent:** [Onion service](#onion-service)

###### Uncensored Onion service search engine

↑ **Parent:** [Onion service search engine](#onion-service-search-engine)

This is where "fun" stuff is likely to be.

<h6 id="tor-link">Tor.link</h6>

↑ **Parent:** [Uncensored Onion service search engine](#uncensored-onion-service-search-engine)

[https://tor.link/](https://tor.link/)

Live January 2024.

##### The Hidden Wiki

↑ **Parent:** [Tor (anonymity network)](#tor-anonymity-network)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/The_Hidden_Wiki)

##### Can ISPs deanonymize Tor users based on timestamps of public posts?

↑ **Parent:** [Tor (anonymity network)](#tor-anonymity-network)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Can_ISPs_deanonymize_Tor_users_based_on_timestamps_of_public_posts?)

[https://security.stackexchange.com/questions/237632/can-isp-deanonymize-telegram-public-channel-creators](https://security.stackexchange.com/questions/237632/can-isp-deanonymize-telegram-public-channel-creators)

## Ciphertext, plaintext, key and salt

↑ **Parent:** [Cryptography](cryptography.md)

### Ciphertext

↑ **Parent:** [Ciphertext, plaintext, key and salt](#ciphertext-plaintext-key-and-salt)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ciphertext)

### Key (cryptography)

↑ **Parent:** [Ciphertext, plaintext, key and salt](#ciphertext-plaintext-key-and-salt)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Key_(cryptography))

#### Pre-shared key

↑ **Parent:** [Key (cryptography)](#key-cryptography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pre-shared_key)

An overview of what you can do with a pre-shared key with tradeoffs can be found at: [https://quantumcomputing.stackexchange.com/questions/142/advantage-of-quantum-key-distribution-over-post-quantum-cryptography/25727#25727](https://quantumcomputing.stackexchange.com/questions/142/advantage-of-quantum-key-distribution-over-post-quantum-cryptography/25727#25727) The options are:
- [one-time pad](#one-time-pad)
- [symmetric encryption](#symmetric-encryption)
- authentication with some [message authentication code](#message-authentication-code) protocol

##### Message authentication code

↑ **Parent:** [Pre-shared key](#pre-shared-key)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Message_authentication_code)

Bibliography:
- [https://crypto.stackexchange.com/questions/59958/is-it-safe-to-hash-a-packet-with-a-shared-secret-to-prove-authenticity](https://crypto.stackexchange.com/questions/59958/is-it-safe-to-hash-a-packet-with-a-shared-secret-to-prove-authenticity)

## Man-in-the-middle attack

↑ **Parent:** [Cryptography](cryptography.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Man-in-the-middle_attack)

### Authentication (cryptography)

↑ **Parent:** [Man-in-the-middle attack](#man-in-the-middle-attack)

In the context of cryptography, authentication means "ensuring that the message you got comes from who you think it did".

Authentication is how we prevent the [man-in-the-middle attack](#man-in-the-middle-attack).

Authentication is one of the hardest parts of cryptography, because the only truly secure way to do it is by driving to the other party yourself to establish a [pre-shared key](#pre-shared-key) so you can do [message authentication code](#message-authentication-code). Or to share your [public key](#public-key-cryptography) with them if you are satisfied with the safety of [post-quantum cryptography](quantum-computing.md#post-quantum-cryptography).

## Zero-knowledge proof

↑ **Parent:** [Cryptography](cryptography.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Zero-knowledge_proof)

<a id="video-i-can-prove-i-ve-solved-this-sudoku-without-revealing-it-by-polylog"></a>
**[Video 2](#video-i-can-prove-i-ve-solved-this-sudoku-without-revealing-it-by-polylog). I can prove I've solved this Sudoku without revealing it by Polylog.** [Source](https://www.youtube.com/watch?v=Otvcbw6k4eo).

### Zero-knowledge proof vs digital signature

↑ **Parent:** [Zero-knowledge proof](#zero-knowledge-proof)  
🏷️ **Tags:** [Digital signature](#digital-signature)

- [https://crypto.stackexchange.com/questions/35177/is-using-digital-signatures-to-prove-identity-a-zero-knowledge-proof](https://crypto.stackexchange.com/questions/35177/is-using-digital-signatures-to-prove-identity-a-zero-knowledge-proof)
- [https://www.reddit.com/r/crypto/comments/stspyl/is_digital_signature_a_form_of_zero_knowledge/](https://www.reddit.com/r/crypto/comments/stspyl/is_digital_signature_a_form_of_zero_knowledge/)

## 🏷️ Tagged (2)

- [Post-quantum cryptography](quantum-computing.md#post-quantum-cryptography)
- [Quantum key distribution](technology.md#quantum-key-distribution)

## ↑ Ancestors (6)

1. [Computer science](computer-science.md)
2. [Computer](computer.md)
3. [Information technology](technology.md#information-technology)
4. [Area of technology](technology.md#area-of-technology)
5. [Technology](technology.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (5)

- [Computer science](computer-science.md)
- [Kerckhoffs's principle](software.md#kerckhoffs-s-principle)
- [Lattice-based cryptography](quantum-computing.md#lattice-based-cryptography)
- [Millennium Prize Problems](mathematics.md#millennium-prize-problems)
- [Quantum algorithm](quantum-computing.md#quantum-algorithm)
