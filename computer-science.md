# Computer science

↑ **Parent:** [Computer](computer.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computer_science)

A branch of [mathematics](mathematics.md) that attempts to prove stuff about [computers](computer.md).

Unfortunately, all [software engineers](software.md#software-engineer) already know the answer to the useful theorems though (except perhaps notably for [cryptography](cryptography.md)), e.g. all programmers obviously know that iehter [P != NP](#p-versus-np-problem) or that this is [unprovable or some other "for all practical purposes practice P != NP"](formalization-of-mathematics.md#independence-mathematical-logic), even though they don't have proof.

And 99% of their time, software engineers are not dealing with mathematically formulatable problems anyways, which is sad.

The only useful "computer science" subset every programmer ever needs to know is:
- for arrays: [dynamic array](#dynamic-array) vs [linked list](#linked-list)
- for [associative array](#associative-array): [binary search tree](#binary-search-tree) vs [hash table](#hash-table). See also [Heap vs Binary Search Tree (BST)](https://stackoverflow.com/questions/6147242/heap-vs-binary-search-tree-bst/29548834#29548834). No need to understand the algorithmic details of the hash function, the [NSA](science.md#national-security-agency) has already done that for you.
- don't use [Bubble sort](https://en.wikipedia.org/wiki/Bubble_sort) for sorting
- you can't parse HTML with regular expressions: [https://stackoverflow.com/questions/1732348/regex-match-open-tags-except-xhtml-self-contained-tags/1732454#1732454](https://stackoverflow.com/questions/1732348/regex-match-open-tags-except-xhtml-self-contained-tags/1732454#1732454) because of [formal language theory](#formal-language-theory)

Funnily, due to the [formalization of mathematics](formalization-of-mathematics.md), [mathematics](mathematics.md) can be seen as a branch of computer science, just like computer science can be seen as a branch of Mathematics!

**Table of contents**

- [Turing machine](#turing-machine)
  - [Universal Turing machine](#universal-turing-machine)
  - [Turing complete](#turing-complete)
- [Formal language theory](#formal-language-theory)
  - [Formal language](#formal-language)
    - [Abstract syntax tree](#abstract-syntax-tree)
  - [Chomsky hierarchy](#chomsky-hierarchy)
    - [Recursively enumerable language](#recursively-enumerable-language)
      - [RE (complexity)](#re-complexity)
      - [Recursive language](#recursive-language)
        - [R (complexity)](#r-complexity)
        - [Undecidable problem](#undecidable-problem)
          - [Undecidability requires infinitely many inputs](#undecidability-requires-infinitely-many-inputs)
          - [Mortal matrix problem](#mortal-matrix-problem)
          - [Computable problem](#computable-problem)
          - [Computable function](#computable-function)
            - [Uncomputable function](#uncomputable-function)
          - [Computable number](#computable-number)
        - [Difference between recursive language and recursively enumerable language](#difference-between-recursive-language-and-recursively-enumerable-language)
        - [Recursive set](#recursive-set)
        - [Context-free language](#context-free-language)
          - [Regular language](#regular-language)
            - [Regular expression](#regular-expression)
- [Computational problem](#computational-problem)
  - [Decision problem](#decision-problem)
    - [Halting problem](#halting-problem)
      - [Turing machine decider](#turing-machine-decider)
        - [Turing machine regex tape notation](#turing-machine-regex-tape-notation)
        - [Cycler Turing machine](#cycler-turing-machine)
        - [Translated cycler Turing machine](#translated-cycler-turing-machine)
        - [Closed Tape Language decider](#closed-tape-language-decider)
      - [Busy beaver](#busy-beaver)
        - [Step busy beaver](#step-busy-beaver)
        - [Busy beaver function](#busy-beaver-function)
          - [Specific values of the Busy beaver function](#specific-values-of-the-busy-beaver-function)
            - [Turing machine acceleration](#turing-machine-acceleration)
            - [Busy Beaver Challenge](#busy-beaver-challenge)
            - [BB(5)](#bb-5)
              - [Marxen-Buntrock machine](#marxen-buntrock-machine)
              - [Skelet’s machines](#skelet’s-machines)
                - [Skelet machine \#1](#skelet-machine-1)
                  - [Skelet machine \#1 is infinite](#skelet-machine-1-is-infinite)
            - [BB(6)](#bb-6)
              - [BB(6) is hard](#bb-6-is-hard)
                - [Antihydra](#antihydra)
                  - [Antihydra in Magic: The Gathering](#antihydra-in-magic-the-gathering)
                  - [Antihydra GMP implementation](#antihydra-gmp-implementation)
                  - [gmp/antihydra.c](#_file/gmp/antihydra.c)
        - [Busy beaver scale](#busy-beaver-scale)
          - [Turing machine compiler](#turing-machine-compiler)
          - [Automated theorem proving by halting problem reduction](#automated-theorem-proving-by-halting-problem-reduction)
            - [Conjecture reduction to a halting problem](#conjecture-reduction-to-a-halting-problem)
              - [Turing machine that halts if and only if the Goldbach conjecture is false](#turing-machine-that-halts-if-and-only-if-the-goldbach-conjecture-is-false)
              - [Turing machine that halts if and only if Collatz conjecture is false](#turing-machine-that-halts-if-and-only-if-collatz-conjecture-is-false)
  - [Function problem](#function-problem)
    - [Inverse problem](#inverse-problem)
    - [Integer algorithm](#integer-algorithm)
      - [Integer multiplication](#integer-multiplication)
      - [Integer factorization](#integer-factorization)
        - [Integer factorization algorithm](#integer-factorization-algorithm)
        - [NP-hard cryptosystem](#np-hard-cryptosystem)
    - [Discrete logarithm](#discrete-logarithm)
      - [Discrete logarithm of the cyclic group](#discrete-logarithm-of-the-cyclic-group)
    - [Functional problem with array as input](#functional-problem-with-array-as-input)
      - [Largest element in an array](#largest-element-in-an-array)
      - [K-th largest element in an array](#k-th-largest-element-in-an-array)
      - [Longest common subsequence](#longest-common-subsequence)
      - [Subset sum problem](#subset-sum-problem)
        - [3SUM](#3sum)
          - [Two sum problem](#two-sum-problem)
  - [Algorithm](#algorithm)
    - [Algorithm cheatsheet](#algorithm-cheatsheet)
    - [Data structure](#data-structure)
      - [Associative array](#associative-array)
        - [Binary search tree](#binary-search-tree)
          - [B-tree](#b-tree)
        - [Hash table](#hash-table)
      - [Dynamic array](#dynamic-array)
      - [Linked list](#linked-list)
      - [Trie](#trie)
    - [Recursion (computer science)](#recursion-computer-science)
      - [Iteration](#iteration)
        - [Iterative algorithm](#iterative-algorithm)
    - [Sorting algorithm](#sorting-algorithm)
      - [String-sorting algorithm](#string-sorting-algorithm)
        - [Natural sort order](#natural-sort-order)
    - [String-search algorithm](#string-search-algorithm)
    - [Class of algorithm](#class-of-algorithm)
      - [Greedy algorithm](#greedy-algorithm)
      - [Dynamic programming](#dynamic-programming)
  - [Complexity class](#complexity-class)
    - [Time complexity](#time-complexity)
      - [Quasilinear time](#quasilinear-time)
    - [Big O notation family](#big-o-notation-family)
      - [Big O notation](#big-o-notation)
      - [Little-o notation](#little-o-notation)
    - [Primitive recursive function](#primitive-recursive-function)
      - [Non-primitive total recursive function](#non-primitive-total-recursive-function)
        - [Ackermann function](#ackermann-function)
    - [Galactic algorithm](#galactic-algorithm)
    - [ELEMENTARY (complexity)](#elementary-complexity)
      - [EXPTIME](#exptime)
        - [PSPACE](#pspace)
          - [NP (complexity)](#np-complexity)
            - [P (complexity)](#p-complexity)
              - [NC (complexity)](#nc-complexity)
              - [Polynomial time algorithm](#polynomial-time-algorithm)
            - [NP-complete](#np-complete)
              - [Cook-Levin theorem](#cook-levin-theorem)
              - [P versus NP problem](#p-versus-np-problem)
                - [Ladner's Theorem](#ladner-s-theorem)
            - [NP-hard](#np-hard)
            - [NP-intermediate](#np-intermediate)
              - [BQP](#bqp)
            - [Co-NP](#co-np)
  - [Constraint satisfaction problem](#constraint-satisfaction-problem)
  - [Optimization problem](#optimization-problem)
    - [Linear programming](#linear-programming)
    - [Logistics](#logistics)
      - [Last mile problem](#last-mile-problem)
    - [Optimization software](#optimization-software)
      - [CPLEX](#cplex)
    - [Limiting factor](#limiting-factor)
      - [Critical path method](#critical-path-method)
        - [Critical path](#critical-path)
        - [Dependency graph](#dependency-graph)
    - [Value function](#value-function)
  - [List of computational problems](#list-of-computational-problems)
- [Computer scientist](#computer-scientist)
  - [Alan Turing](#alan-turing)
  - [Noam Chomsky](#noam-chomsky)
  - [Scott Aaronson](#scott-aaronson)
- [Cryptography](cryptography.md)
  - [Cryptosystem](cryptography.md#cryptosystem)
  - [Random number generation](cryptography.md#random-number-generation)
    - [Hardware random number generation](cryptography.md#hardware-random-number-generation)
  - [Symmetric and public-key cryptography](cryptography.md#symmetric-and-public-key-cryptography)
    - [Symmetric encryption](cryptography.md#symmetric-encryption)
      - [Provably secure symmetric-key algorithm](cryptography.md#provably-secure-symmetric-key-algorithm)
      - [One-time pad](cryptography.md#one-time-pad)
      - [Symmetric-key algorithm](cryptography.md#symmetric-key-algorithm)
        - [Advanced Encryption Standard](cryptography.md#advanced-encryption-standard)
          - [Is AES quantum resistant?](cryptography.md#is-aes-quantum-resistant)
    - [Public-key cryptography](cryptography.md#public-key-cryptography)
      - [Digital signature](cryptography.md#digital-signature)
      - [Ring signature](cryptography.md#ring-signature)
      - [Public-key cryptosystem](cryptography.md#public-key-cryptosystem)
        - [RSA (cryptosystem)](cryptography.md#rsa-cryptosystem)
          - [How large primes are found for RSA](cryptography.md#how-large-primes-are-found-for-rsa)
          - [RSA vs Diffie-Hellman](cryptography.md#rsa-vs-diffie-hellman)
      - [Diffie-Hellman key exchange](cryptography.md#diffie-hellman-key-exchange)
        - [Key exchange](cryptography.md#key-exchange)
      - [Elliptic curve cryptography](cryptography.md#elliptic-curve-cryptography)
        - [Elliptic-curve Diffie-Hellman](cryptography.md#elliptic-curve-diffie-hellman)
          - [Diffie-Hellman vs ECDH](cryptography.md#diffie-hellman-vs-ecdh)
  - [Encryption](cryptography.md#encryption)
    - [Encryption software](cryptography.md#encryption-software)
      - [OpenSSL](cryptography.md#openssl)
    - [Steganography](cryptography.md#steganography)
    - [Deniable authentication](cryptography.md#deniable-authentication)
    - [End-to-end encryption](cryptography.md#end-to-end-encryption)
    - [Forward secrecy](cryptography.md#forward-secrecy)
    - [Disk encryption](cryptography.md#disk-encryption)
      - [Can a smartphone's PIN or password be brute-forced in an offline attack?](cryptography.md#can-a-smartphone-s-pin-or-password-be-brute-forced-in-an-offline-attack)
      - [Linux Unified Key Setup](cryptography.md#linux-unified-key-setup)
      - [Disk encryption password handover plausible deniability](cryptography.md#disk-encryption-password-handover-plausible-deniability)
  - [GNU Privacy Guard](cryptography.md#gnu-privacy-guard)
  - [Internet privacy](cryptography.md#internet-privacy)
    - [Anonymity](cryptography.md#anonymity)
      - [Receiving an anonymous donation](cryptography.md#receiving-an-anonymous-donation)
        - [Receiving an anonymous donation in the UK](cryptography.md#receiving-an-anonymous-donation-in-the-uk)
    - [Internet privacy organizations](cryptography.md#internet-privacy-organizations)
      - [Riseup](cryptography.md#riseup)
    - [Operations security](cryptography.md#operations-security)
    - [Internet privacy technology](cryptography.md#internet-privacy-technology)
      - [I2P](cryptography.md#i2p)
        - [I2P on Ubuntu](cryptography.md#i2p-on-ubuntu)
          - [I2P on Ubuntu browser setup](cryptography.md#i2p-on-ubuntu-browser-setup)
          - [I2P Ubuntu via PPA](cryptography.md#i2p-ubuntu-via-ppa)
      - [Tor (anonymity network)](cryptography.md#tor-anonymity-network)
        - [Tor Browser](cryptography.md#tor-browser)
        - [Onion service](cryptography.md#onion-service)
          - [Dark web](cryptography.md#dark-web)
          - [Hidden Answers](cryptography.md#hidden-answers)
          - [Onion service search engine](cryptography.md#onion-service-search-engine)
            - [Uncensored Onion service search engine](cryptography.md#uncensored-onion-service-search-engine)
              - [Tor.link](cryptography.md#tor-link)
        - [The Hidden Wiki](cryptography.md#the-hidden-wiki)
        - [Can ISPs deanonymize Tor users based on timestamps of public posts?](cryptography.md#can-isps-deanonymize-tor-users-based-on-timestamps-of-public-posts)
  - [Ciphertext, plaintext, key and salt](cryptography.md#ciphertext-plaintext-key-and-salt)
    - [Ciphertext](cryptography.md#ciphertext)
    - [Key (cryptography)](cryptography.md#key-cryptography)
      - [Pre-shared key](cryptography.md#pre-shared-key)
        - [Message authentication code](cryptography.md#message-authentication-code)
  - [Man-in-the-middle attack](cryptography.md#man-in-the-middle-attack)
    - [Authentication (cryptography)](cryptography.md#authentication-cryptography)
  - [Zero-knowledge proof](cryptography.md#zero-knowledge-proof)
    - [Zero-knowledge proof vs digital signature](cryptography.md#zero-knowledge-proof-vs-digital-signature)
- [Hash function](#hash-function)
  - [Secure Hash Algorithms](#secure-hash-algorithms)
    - [SHA-1](#sha-1)
    - [SHA-2](#sha-2)
      - [SHA-256](#sha-256)
  - [Merkle tree](#merkle-tree)
- [Computer science bibliography](#computer-science-bibliography)
  - [Computer science YouTube channel](#computer-science-youtube-channel)
    - [Computerphile](#computerphile)
      - [Brady Haran](#brady-haran)
        - [Brady Haran production](#brady-haran-production)

## Turing machine

↑ **Parent:** [Computer science](computer-science.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Turing_machine)

The dominating model of a computer.

The model is extremely simple, but has been proven to be able to solve all the problems that any reasonable computer model can solve, thus its adoption as the "default model".

The smallest known Turing machine that cannot be proven to halt or not as of 2019 is 7,918-states: [https://www.scottaaronson.com/blog/?p=2725](https://www.scottaaronson.com/blog/?p=2725). [Shtetl-Optimized](https://www.scottaaronson.com/) by Scott Aaronson is just the best website.

A bunch of non-reasonable-looking computers have also been proven to be Turing complete for fun, e.g. [Magic: The Gathering](magic-the-gathering.md).

### Universal Turing machine

↑ **Parent:** [Turing machine](#turing-machine)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Universal_Turing_machine)

A Turing machine that simulates another Turing machine/input pair that has been encoded as a string.

In other words: an [emulator](systems-programming.md#emulator)!

The concept is fundamental to state several key results in [computer science](computer-science.md), notably the [halting problem](#halting-problem).

### Turing complete

↑ **Parent:** [Turing machine](#turing-machine)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Turing_completeness)

A computer model that is as powerful as the most powerful computer model we have: [Turing machine](#turing-machine)!

## Formal language theory

↑ **Parent:** [Computer science](computer-science.md)

### Formal language

↑ **Parent:** [Formal language theory](#formal-language-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Formal_language)

#### Abstract syntax tree

↑ **Parent:** [Formal language](#formal-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Abstract_syntax_tree)

### Chomsky hierarchy

↑ **Parent:** [Formal language theory](#formal-language-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chomsky_hierarchy)

This is the classic result of [formal language theory](#formal-language-theory), but there is too much slack between context free and context sensitive, which is [PSPACE](#pspace) (larger than [NP](#np-complexity)!).

By [Noam Chomsky](#noam-chomsky).

A good summary table that opens up each category much more can be seen e.g. at the bottom of [https://en.wikipedia.org/wiki/Automata_theory](https://en.wikipedia.org/wiki/Automata_theory) under the summary thingy at the bottom entitled "Automata theory: formal languages and formal grammars".

#### Recursively enumerable language

↑ **Parent:** [Chomsky hierarchy](#chomsky-hierarchy)  
🏷️ **Tags:** [Chomsky hierarchy](#chomsky-hierarchy)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Recursively_enumerable_language)

There is a [Turing machine](#turing-machine) that halts for every member of the language with the answer yes, but does not necessarily halt for non-members.

Non-examples: [https://cs.stackexchange.com/questions/52503/non-recursively-enumerable-languages](https://cs.stackexchange.com/questions/52503/non-recursively-enumerable-languages)

##### RE (complexity)

↑ **Parent:** [Recursively enumerable language](#recursively-enumerable-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RE_(complexity))

##### Recursive language

↑ **Parent:** [Recursively enumerable language](#recursively-enumerable-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Recursive_language)

Subset of [recursively enumerable language](#recursively-enumerable-language) as explained at: [difference between recursive language and recursively enumerable language](#difference-between-recursive-language-and-recursively-enumerable-language).

###### R (complexity)

↑ **Parent:** [Recursive language](#recursive-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/R_(complexity))

Set of all [decision problems](#decision-problem) solvable by a [Turing machine](#turing-machine), i.e. that decide if a string belongs to a [recursive language](#recursive-language).

###### Undecidable problem

↑ **Parent:** [Recursive language](#recursive-language)  
🏷️ **Tags:** [Decision problem](#decision-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Undecidable_problem)

Is a [decision problem](#decision-problem) of determining if something belongs to a non-[recursive language](#recursive-language).

Or in other words: there is no [Turing machine](#turing-machine) that always halts for every input with the yes/no output.

Every undecidable problem must obviously have an infinite number of "possibilities of stuff you can try": if there is only a finite number, then you can brute-force it.

Some undecidable problems are of [recursively enumerable language](#recursively-enumerable-language), e.g. the [halting problem](#halting-problem).

Lists of undecidable problems.
- [https://mathoverflow.net/questions/11540/what-are-the-most-attractive-turing-undecidable-problems-in-mathematics](https://mathoverflow.net/questions/11540/what-are-the-most-attractive-turing-undecidable-problems-in-mathematics)
- [https://en.wikipedia.org/wiki/List_of_undecidable_problems](https://en.wikipedia.org/wiki/List_of_undecidable_problems)

Coolest ones besides the obvious boring [halting problem](#halting-problem):
- [mortal matrix problem](#mortal-matrix-problem)
- [Diophantine equation](formalization-of-mathematics.md#diophantine-equation) existence of solutions: [undecidable Diophantine equation problems](formalization-of-mathematics.md#undecidable-diophantine-equation-example)

###### Undecidability requires infinitely many inputs

↑ **Parent:** [Undecidable problem](#undecidable-problem)

If there are infinitely many inputs, we can always construct a (potentially exponentially huge) [Turing machine](#turing-machine) that hardcodes the outcome for every possible input, so the problem is never [undecidable](#undecidable-problem).

The problem is of course deciding and proving the outcome for each possible input, notably as it is possible that calculation for some of the inputs may be [independent](formalization-of-mathematics.md#independence-mathematical-logic) from [ZFC](formalization-of-mathematics.md#zermelo-fraenkel-axioms-with-the-axiom-of-choice).

###### Mortal matrix problem

↑ **Parent:** [Undecidable problem](#undecidable-problem)

[https://en.wikipedia.org/wiki/Zero_matrix#Occurrences](https://en.wikipedia.org/wiki/Zero_matrix#Occurrences)

One of the most simple to state [undecidable problems](#undecidable-problem).

The reason that it is undecidable is that you can repeat each matrix any number of times, so there isn't a finite number of possibilities to check.

###### Computable problem

↑ **Parent:** [Undecidable problem](#undecidable-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computable_problem)

A:
- [decidable problem](#undecidable-problem) is to a [decision problem](#decision-problem)
- like a computable problem is to a [function problem](#function-problem)

###### Computable function

↑ **Parent:** [Undecidable problem](#undecidable-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computable_function)

###### Uncomputable function

↑ **Parent:** [Computable function](#computable-function)

The prototypical example is the [Busy beaver function](#busy-beaver-function), which is the easiest example to reach from the [halting problem](#halting-problem).

###### Computable number

↑ **Parent:** [Undecidable problem](#undecidable-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computable_number)

[https://math.stackexchange.com/questions/462790/are-there-any-examples-of-non-computable-real-numbers](https://math.stackexchange.com/questions/462790/are-there-any-examples-of-non-computable-real-numbers)

There are only boring examples of taking an uncomputable language and converting it into a number?

###### Difference between recursive language and recursively enumerable language

↑ **Parent:** [Recursive language](#recursive-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Difference_between_recursive_language_and_recursively_enumerable_language)

[https://stackoverflow.com/questions/33467040/what-is-the-difference-between-recursive-and-recursively-enumerable-languages/65455863#65455863](https://stackoverflow.com/questions/33467040/what-is-the-difference-between-recursive-and-recursively-enumerable-languages/65455863#65455863)

###### Recursive set

↑ **Parent:** [Recursive language](#recursive-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Recursive_set)

Same as [recursive language](#recursive-language) but in the context of the [integers](formalization-of-mathematics.md#integer).

###### Context-free language

↑ **Parent:** [Recursive language](#recursive-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Context-free_language)

###### Regular language

↑ **Parent:** [Context-free language](#context-free-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Regular_language)

###### Regular expression

↑ **Parent:** [Regular language](#regular-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Regular_expression)

## Computational problem

↑ **Parent:** [Computer science](computer-science.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computational_problem)

The list: [https://complexityzoo.uwaterloo.ca/Complexity_Zoo](https://complexityzoo.uwaterloo.ca/Complexity_Zoo)

### Decision problem

↑ **Parent:** [Computational problem](#computational-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Decision_problem)

[Computational problem](#computational-problem) where the solution is either yes or no.

When there are more than two possible answers, it is called a [function problem](#function-problem).

Decision problems come up often in [computer science](computer-science.md) because many important problems are often stated in terms of "decide if a given string belongs to given [formal language](#formal-language)".

#### Halting problem

↑ **Parent:** [Decision problem](#decision-problem)  
🏷️ **Tags:** [Undecidable problem](#undecidable-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Halting_problem)

The canonical [undecidable problem](#undecidable-problem).

##### Turing machine decider

↑ **Parent:** [Halting problem](#halting-problem)

A [Turing machine](#turing-machine) decider is a program that decides if one or more [Turing machines](#turing-machine) halts of not.

Of course, because what we know about the [halting problem](#halting-problem), there cannot exist a single decider that decides all [Turing machines](#turing-machine).

E.g. [The Busy Beaver Challenge](#busy-beaver-challenge) has a set of deciders clearly published, which decide a large part of [BB(5)](#bb-5). Their proposed deciders are listed at: [https://discuss.bbchallenge.org/c/deciders/5](https://discuss.bbchallenge.org/c/deciders/5) and actually applied ones at: [https://bbchallenge.org](https://bbchallenge.org).

But there are deciders that can decide large classes of turing machines.

Many (all/most?) deciders are based on simulation of machines with arbitrary cutoff [hyperparameters](machine-learning.md#hyperparameter), e.g. the cutoff space/time of a [Turing machine cycler decider](#cycler-turing-machine).

The simplest and most obvious example is the [Turing machine cycler decider](#cycler-turing-machine)

###### Turing machine regex tape notation

↑ **Parent:** [Turing machine decider](#turing-machine-decider)

[Turing machine regex tape notation](#turing-machine-regex-tape-notation) is [Ciro Santilli](ciro-santilli.md)'s made up name for the notation used e.g. at:
- [https://www.sligocki.com/2023/02/02/skelet-34.html](https://www.sligocki.com/2023/02/02/skelet-34.html)
- [https://www.sligocki.com/2022/06/10/ctl.html](https://www.sligocki.com/2022/06/10/ctl.html)
Most of it is just regular [regular expression](#regular-expression) notation, with a few differences:
- $0^{\inf}$ denotes the right or left edge of the (zero initialized) tape. It is often omitted as we always just assume it is always present on both sides of every regex
- `A`, `B`, `C`, `D` and `E` denotes the current machine state. This is especially common notation in the context of the [BB(5)](#bb-5) problem
- `<` and `>` next to the state indicate if the head is on top of the left or right element. E.g.:
  ```
  11 (01)^n <A 00 (0011)^{n+2}
  ```

  indicates that the head `A` is on top of the last `1` of the last sequence of n `01`s to the left of the head.

This notation is very useful, as it helps compress long repeated sequences of [Turing machine](#turing-machine) tape and extract higher level patterns from them, which is how you go about understanding a Turing machine in order to apply [Turing machine acceleration](#turing-machine-acceleration).

###### Cycler Turing machine

↑ **Parent:** [Turing machine decider](#turing-machine-decider)

Bibliography: [https://discuss.bbchallenge.org/t/decider-cyclers/33](https://discuss.bbchallenge.org/t/decider-cyclers/33)

Example: [https://bbchallenge.org/279081](https://bbchallenge.org/279081).

These are very simple, they just check for exact state repetitions, which obviously imply that they will run forever.

Unfortunately, cyclers may need to run through an initial setup phase before reaching the initial cycle point, which is not very elegant.

Also, we have no way of knowing the initial setup length of the actual cycle length, so we just need an arbitrary cutoff value.

And unfortunately, this can lead to misses, e.g. [Skelet machine \#1](#skelet-machine-1), a 5 state machine, has a (translated) cycle that starts at around 50-200M steps, and takes 8 trillion steps to repeat.

###### Translated cycler Turing machine

↑ **Parent:** [Turing machine decider](#turing-machine-decider)

Bibliography: [https://discuss.bbchallenge.org/t/decider-translated-cyclers/34](https://discuss.bbchallenge.org/t/decider-translated-cyclers/34)

Like a cycler, but the cycle starts at an offset.

To see infinity, we check that if the machine only goes left N squares until reaching the repetition, then repetition must only be N squares long.

###### Closed Tape Language decider

↑ **Parent:** [Turing machine decider](#turing-machine-decider)

Described at: [https://www.sligocki.com/2022/06/10/ctl.html](https://www.sligocki.com/2022/06/10/ctl.html)

##### Busy beaver

↑ **Parent:** [Halting problem](#halting-problem)  
🏷️ **Tags:** [Function problem](#function-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Busy_beaver)

The busy beaver game consists in finding, for a given $n$, the turing machine with $n$ states that writes the largest possible number of 1's on a tape initially filled with 0's. In other words, computing the [busy beaver function](#busy-beaver-function) for a given $n$.

There are only finitely many Turing machines with $n$ states, so we are certain that there exists such a maximum. Computing the [Busy beaver function](#busy-beaver-function) for a given $n$ then comes down to solving the halting problem for every single machine with $n$ states.

Some variant definitions define it as the number of time steps taken by the machine instead. Wikipedia talks about their relationship, but no patience right now.

The Busy Beaver problem is cool because it puts the [halting problem](#halting-problem) in a more precise numerical light, e.g.:
- the [Busy beaver function](#busy-beaver-function) is the most obvious [uncomputable function](#uncomputable-function) one can come up with starting from the [halting problem](#halting-problem)
- the [Busy beaver scale](#busy-beaver-scale) allows us to gauge the difficulty of proving certain (yet unproven!) mathematical [conjectures](formalization-of-mathematics.md#conjecture)

Bibliography:
- [https://www.scottaaronson.com/blog/?p=4916](https://www.scottaaronson.com/blog/?p=4916)
- [https://www.quantamagazine.org/the-busy-beaver-game-illuminates-the-fundamental-limits-of-math-20201210](https://www.quantamagazine.org/the-busy-beaver-game-illuminates-the-fundamental-limits-of-math-20201210)

###### Step busy beaver

↑ **Parent:** [Busy beaver](#busy-beaver)

The [step busy beaver](#step-busy-beaver) is a variant of the [busy beaver game](#busy-beaver) counts the number of steps before halt, instead of the number of 1's written to the tape.

As of 2023, it appears that [BB(5)](#bb-5) the same machine, , will win both for 5 states. But this is not always necessarily the case.

###### Busy beaver function

↑ **Parent:** [Busy beaver](#busy-beaver)  
🏷️ **Tags:** [Uncomputable function](#uncomputable-function)

$BB(n)$ is the largest number of 1's written by a [halting](#halting-problem) $n$-state [Turing machine](#turing-machine) on a tape initially filled with 0's.

<a id="video-the-boundary-of-computation-by-mutual-information-2023"></a>
**[Video 1](#video-the-boundary-of-computation-by-mutual-information-2023). The Boundary of Computation by Mutual Information (2023)** [Source](https://www.youtube.com/watch?v=kmAc1nDizu0).

###### Specific values of the Busy beaver function

↑ **Parent:** [Busy beaver function](#busy-beaver-function)

The following things come to mind when you look into research in this area, especially the search for [BB(5)](#bb-5) which was hard but doable:
- it is largely [recreational mathematics](mathematics.md#recreational-mathematics), i.e. done by non-professionals, a bit like the [aperiodic tiling](geometry.md#aperiodic-tiling). Humbly, they tend to call their results [lemmas](formalization-of-mathematics.md#lemma-mathematics)
- complex structure emerges from simple rules, leading to a complex [classification](mathematics.md#classification-mathematics) with a few edge cases, much like the [classification of finite simple groups](group.md#classification-of-finite-simple-groups)

Bibliography:
- [https://cs.stackexchange.com/questions/59344/what-are-very-short-programs-with-unknown-halting-status](https://cs.stackexchange.com/questions/59344/what-are-very-short-programs-with-unknown-halting-status)
  - [https://cs.stackexchange.com/questions/44869/what-are-the-simplest-examples-of-programs-that-we-do-not-know-whether-they-term](https://cs.stackexchange.com/questions/44869/what-are-the-simplest-examples-of-programs-that-we-do-not-know-whether-they-term) imprecise duplicate
- [https://cstheory.stackexchange.com/questions/20978/what-is-the-smallest-turing-machine-where-it-is-unknown-if-it-halts-or-not](https://cstheory.stackexchange.com/questions/20978/what-is-the-smallest-turing-machine-where-it-is-unknown-if-it-halts-or-not)

###### Turing machine acceleration

↑ **Parent:** [Specific values of the Busy beaver function](#specific-values-of-the-busy-beaver-function)

[Turing machine acceleration](#turing-machine-acceleration) refers to using high level understanding of specific properties of specific Turing machines to be able to simulate them much fatser than naively running the simulation as usual.

Acceleration allows one to use simulation to find infinite loops that might be very long, and would not be otherwise spotted without acceleration.

This is for example the case of [https://www.sligocki.com/2023/03/13/skelet-1-infinite.html](https://www.sligocki.com/2023/03/13/skelet-1-infinite.html) proof of [Skelet machine \#1](#skelet-machine-1).

###### Busy Beaver Challenge

↑ **Parent:** [Specific values of the Busy beaver function](#specific-values-of-the-busy-beaver-function)

[https://bbchallenge.org/story](https://bbchallenge.org/story)

Project trying to compute [BB(5)](#bb-5) once and for all. Notably it has better presentation and organization than any other previous effort, and appears to have grouped everyone who cares about the topic as of the early 2020s.

Very cool initiative!

By 2023, they had basically decided every machine: [https://discuss.bbchallenge.org/t/the-30-to-34-ctl-holdouts-from-bb-5/141](https://discuss.bbchallenge.org/t/the-30-to-34-ctl-holdouts-from-bb-5/141)

In June 2024 they felt that they had verified the result after a full [Coq](formalization-of-mathematics.md#coq-software) proof was published: 
- [https://www.quantamagazine.org/amateur-mathematicians-find-fifth-busy-beaver-turing-machine-20240702/](https://www.quantamagazine.org/amateur-mathematicians-find-fifth-busy-beaver-turing-machine-20240702/)
- [https://discuss.bbchallenge.org/t/july-2nd-2024-we-have-proved-bb-5-47-176-870/237](https://discuss.bbchallenge.org/t/july-2nd-2024-we-have-proved-bb-5-47-176-870/237)
So now onto [BB(6)](#bb-6) I guess.

<h6 id="bb-5">BB(5)</h6>

↑ **Parent:** [Specific values of the Busy beaver function](#specific-values-of-the-busy-beaver-function)

The last value we will likely every know for the [busy beaver function](#busy-beaver-function)! [BB(6)](#bb-6) is likely completely out of reach forever.

By 2023, it had basically been decided by the [The Busy Beaver Challenge](#busy-beaver-challenge) as mentioned at: [https://discuss.bbchallenge.org/t/the-30-to-34-ctl-holdouts-from-bb-5/141](https://discuss.bbchallenge.org/t/the-30-to-34-ctl-holdouts-from-bb-5/141), pending only further verification. It is going to be one of those highly computational proofs that will be needed to be [formally verified](software.md#formal-verification) for people to finally settle.

As that project beautifully puts it, as of 2023 prior to full resolution, this can be considered the:

> simplest open problem in mathematics

on the [Busy beaver scale](#busy-beaver-scale).

###### Marxen-Buntrock machine

↑ **Parent:** [BB(5)](#bb-5)

Best [busy beaver](#busy-beaver) machine known since 1989 as of 2023, before a full proof of all 5 state machines had been carried out.

Entry on [The Busy Beaver Challenge](#busy-beaver-challenge): [https://bbchallenge.org/1RB1LC_1RC1RB_1RD0LE_1LA1LD_1RZ0LA](https://bbchallenge.org/1RB1LC_1RC1RB_1RD0LE_1LA1LD_1RZ0LA)

Paper extracted to HTML by Heiner Marxen: [http://turbotm.de/~heiner/BB/mabu90.html](http://turbotm.de/~heiner/BB/mabu90.html)

###### Skelet’s machines

↑ **Parent:** [BB(5)](#bb-5)

List on [The Busy Beaver Challenge](#busy-beaver-challenge): [https://bbchallenge.org/skelet](https://bbchallenge.org/skelet)

Bibliography:
- [https://bbchallenge.org/story#skelets-43-undecided-machines](https://bbchallenge.org/story#skelets-43-undecided-machines)
- [https://skelet.ludost.net/bb/nreg.html](https://skelet.ludost.net/bb/nreg.html)

###### Skelet machine \#1

↑ **Parent:** [Skelet’s machines](#skelet’s-machines)  
🏷️ **Tags:** [Translated cycler Turing machine](#translated-cycler-turing-machine)

On [The Busy Beaver Challenge](#busy-beaver-challenge): [https://bbchallenge.org/68329601](https://bbchallenge.org/68329601)

###### Skelet machine \#1 is infinite

↑ **Parent:** [Skelet machine \#1](#skelet-machine-1)

Non formal proof with a program March 2023: [https://www.sligocki.com/2023/03/13/skelet-1-infinite.html](https://www.sligocki.com/2023/03/13/skelet-1-infinite.html) Awesome article that describes the proof procedure.

[Formal proof](formalization-of-mathematics.md#formal-proof) August 2023: [https://discuss.bbchallenge.org/t/skelet-1-is-a-translated-cycler-coq-agrees/166](https://discuss.bbchallenge.org/t/skelet-1-is-a-translated-cycler-coq-agrees/166)

The proof uses [Turing machine acceleration](#turing-machine-acceleration) to show that [Skelet machine \#1](#skelet-machine-1) is a [Translated cycler Turing machine](#translated-cycler-turing-machine) with humongous cycle paramters:
- start between 50-200 M steps, not calculated precisely on the original post
- period: ~8 billion steps

<h6 id="bb-6">BB(6)</h6>

↑ **Parent:** [Specific values of the Busy beaver function](#specific-values-of-the-busy-beaver-function)

<h6 id="bb-6-is-hard">BB(6) is hard</h6>

↑ **Parent:** [BB(6)](#bb-6)

A hard problem ha been found for it, and it was called the "[antihydra](#antihydra)":
- [https://news.ycombinator.com/item?id=40864949](https://news.ycombinator.com/item?id=40864949) BB(6), The 6th Busy Beaver Number, is harder than a Collatz-like math problem 
- [https://www.reddit.com/r/math/comments/1dubva0/finding_the_6th_busy_beaver_number_%CF%836_aka_bb6_is/](https://www.reddit.com/r/math/comments/1dubva0/finding_the_6th_busy_beaver_number_%CF%836_aka_bb6_is/) "Finding the 6th busy beaver number (Σ(6), AKA BB(6)) is at least as hard as a hard Collatz-like math problem called Antihydra":
- [https://www.reddit.com/r/compsci/comments/1duc62e/finding_the_6th_busy_beaver_number_%CF%836_aka_bb6_is/](https://www.reddit.com/r/compsci/comments/1duc62e/finding_the_6th_busy_beaver_number_%CF%836_aka_bb6_is/)

###### Antihydra

↑ **Parent:** [BB(6) is hard](#bb-6-is-hard)

The [Antihydra](#antihydra) is the first hard-looking problem for [BB(6)](#bb-6), what some would classify as a [Collatz-like problem](formalization-of-mathematics.md#collatz-like-problem).

It is documented on the [Busy Beaver Challenge](#busy-beaver-challenge) wiki at: [https://wiki.bbchallenge.org/wiki/Antihydra](https://wiki.bbchallenge.org/wiki/Antihydra)

###### Antihydra in Magic: The Gathering

↑ **Parent:** [Antihydra](#antihydra)

Some dude recreated the [antihydra](#antihydra) on [Magic: The Gathering](magic-the-gathering.md) at: [https://aesort.com/antihydra](https://aesort.com/antihydra), probably: [https://x.com/IsaacKing314/status/1870637729375219740](https://x.com/IsaacKing314/status/1870637729375219740).

It is known that [Magic: The Gathering is Turing complete](magic-the-gathering.md#magic-the-gathering-is-turing-complete), but it is cool to have a concrete specific example of an [open problem in mathematics](formalization-of-mathematics.md#open-problem-in-mathematics) coded in it.

<a id="image-screenshot-of-the-antihydra-in-magic-the-gathering-construction"></a>
<img src="https://web.archive.org/web/20241222020126im_/https://aesort.com/static/img/antihydra.png" alt="" height="800">

**[Figure 1](#image-screenshot-of-the-antihydra-in-magic-the-gathering-construction). Screenshot of the Antihydra in Magic: The Gathering construction**.

###### Antihydra GMP implementation

↑ **Parent:** [Antihydra](#antihydra)  
🏷️ **Tags:** [GNU Multiple Precision Arithmetic Library](software.md#gnu-multiple-precision-arithmetic-library)

<h6 id="_file/gmp/antihydra.c">gmp/antihydra.c</h6>

↑ **Parent:** [Antihydra](#antihydra)  
🏷️ **Tags:** [GMP example](software.md#gmp-example)

Also posted at:
- [https://wiki.bbchallenge.org/w/index.php?title=Antihydra&oldid=958](https://wiki.bbchallenge.org/w/index.php?title=Antihydra&oldid=958) But [obviously it got deleted](website.md#deletionism-on-wikipedia), not even a tiny shitpage maintained by 5 people is immune to [deletionism](website.md#deletionism)
- [https://cstheory.stackexchange.com/questions/20978/what-is-the-smallest-turing-machine-where-it-is-unknown-if-it-halts-or-not/53326#53326](https://cstheory.stackexchange.com/questions/20978/what-is-the-smallest-turing-machine-where-it-is-unknown-if-it-halts-or-not/53326#53326)
- [https://cs.stackexchange.com/questions/59344/what-are-very-short-programs-with-unknown-halting-status/162108#162108](https://cs.stackexchange.com/questions/59344/what-are-very-short-programs-with-unknown-halting-status/162108#162108)

###### Busy beaver scale

↑ **Parent:** [Busy beaver](#busy-beaver)

The [Busy beaver scale](#busy-beaver-scale) allows us to gauge the difficulty of proving certain (yet unproven!) mathematical [conjectures](formalization-of-mathematics.md#conjecture)!

To to this, people have reduced certain mathematical problems to deciding the [halting problem](#halting-problem) of a specific [Turing machine](#turing-machine).

A good example is perhaps the [Goldbach's conjecture](mathematics.md#goldbach-s-conjecture). We just make a [Turing machine](#turing-machine) that successively checks for each even number of it is a sum of two primes by naively looping down and trying every possible pair. Let the machine halt if the check fails. So this machine halts [iff](formalization-of-mathematics.md#if-and-only-if) the [Goldbach's conjecture](mathematics.md#goldbach-s-conjecture) is false! See also [Conjecture reduction to a halting problem](#conjecture-reduction-to-a-halting-problem).

Therefore, if we were able to compute $BB(n)$, we would be able to prove those conjectures automatically, by letting the machine run up to $BB(n)$, and if it hadn't halted by then, we would know that it would never halt.

Of course, in practice, $BB$ is generally [uncomputable](#computable-problem), so we will never know it. And furthermore, even if it were computable, it would take a lot longer than the age of the universe to compute any of it, so it would be useless.

However, philosophically speaking at least, the number of states of the equivalent [Turing machine](#turing-machine) gives us a philosophical idea of the complexity of the problem.

The [busy beaver scale](#busy-beaver-scale) is likely mostly useless, since we are able to prove that many non-trivial [Turing machines](#turing-machine) do halt, often by reducing problems to simpler known cases. But still, it is cute.

But maybe, just maybe, reduction to Turing machine form could be useful. E.g. [The Busy Beaver Challenge](#busy-beaver-challenge) and other attempts to solve [BB(5)](#bb-5) have come up with large number of automated (usually parametrized up to a certain threshold) [Turing machine decider](#turing-machine-decider) programs that automatically determine if certain (often large numbers of) Turing machines run forever.

So it it not impossible that after some reduction to a standard [Turing machine](#turing-machine) form, some conjecture just gets automatically brute-forced by one of the deciders, this is a path to

###### Turing machine compiler

↑ **Parent:** [Busy beaver scale](#busy-beaver-scale)

[https://cs.stackexchange.com/questions/50815/compiler-that-compiles-to-a-turing-machine/161872#161872](https://cs.stackexchange.com/questions/50815/compiler-that-compiles-to-a-turing-machine/161872#161872)

###### Automated theorem proving by halting problem reduction

↑ **Parent:** [Busy beaver scale](#busy-beaver-scale)  
🏷️ **Tags:** [Automated theorem proving](artificial-intelligence.md#automated-theorem-proving)

If you can reduce a mathematical problem to the [Halting problem](#halting-problem) of a specific turing machine, as in the case of a few machines of the [Busy beaver scale](#busy-beaver-scale), then using [Turing machine deciders](#turing-machine-decider) could serve as a method of [automated theorem proving](artificial-intelligence.md#automated-theorem-proving).

That feels like it could be an elegant proof method, as you reduce your problem to one of the most well studied representations that exists: a [Turing machine](#turing-machine).

However it also appears that certain problems cannot be reduced to a [halting problem](#halting-problem)... OMG life sucks (or is awesome?): [Section "Turing machine that halts if and only if Collatz conjecture is false"](#turing-machine-that-halts-if-and-only-if-collatz-conjecture-is-false).

###### Conjecture reduction to a halting problem

↑ **Parent:** [Automated theorem proving by halting problem reduction](#automated-theorem-proving-by-halting-problem-reduction)

[https://bbchallenge.org/story#what-is-known-about-bb](https://bbchallenge.org/story#what-is-known-about-bb) lists some (all?) cool examples, 
- BB(15): [Erdős' conjecture on powers of 2](formalization-of-mathematics.md#erdos-conjecture-on-powers-of-2), which has some relation to [Collatz conjecture](formalization-of-mathematics.md#collatz-conjecture)
- BB(27): [Goldbach's conjecture](mathematics.md#goldbach-s-conjecture)
- BB(744): [Riemann hypothesis](calculus.md#riemann-hypothesis)
- BB(748): [independent](formalization-of-mathematics.md#independence-mathematical-logic) from the [Zermelo-Fraenkel axioms](formalization-of-mathematics.md#zermelo-fraenkel-axioms)
- BB(7910): [independent](formalization-of-mathematics.md#independence-mathematical-logic) from the [ZFC](formalization-of-mathematics.md#zermelo-fraenkel-axioms-with-the-axiom-of-choice)

[https://wiki.bbchallenge.org/wiki/Cryptids](https://wiki.bbchallenge.org/wiki/Cryptids) contains a larger list. In June 2024 it was discovered that [BB(6) is hard](#bb-6-is-hard).

###### Turing machine that halts if and only if the Goldbach conjecture is false

↑ **Parent:** [Conjecture reduction to a halting problem](#conjecture-reduction-to-a-halting-problem)  
🏷️ **Tags:** [Goldbach conjecture](mathematics.md#goldbach-s-conjecture)

[https://www.scottaaronson.com/papers/bb.pdf](https://www.scottaaronson.com/papers/bb.pdf)

###### Turing machine that halts if and only if Collatz conjecture is false

↑ **Parent:** [Conjecture reduction to a halting problem](#conjecture-reduction-to-a-halting-problem)  
🏷️ **Tags:** [Collatz conjecture](formalization-of-mathematics.md#collatz-conjecture)

[https://mathoverflow.net/questions/309044/is-there-a-known-turing-machine-which-halts-if-and-only-if-the-collatz-conjectur](https://mathoverflow.net/questions/309044/is-there-a-known-turing-machine-which-halts-if-and-only-if-the-collatz-conjectur) suggests one does not exist. Amazing.

Intuitively we see that the situation is fundamentally different from the [Turing machine that halts if and only if the Goldbach conjecture is false](#turing-machine-that-halts-if-and-only-if-the-goldbach-conjecture-is-false) because for Collatz the counter example must go off into infinity, while in Goldbach conjecture we can finitely check any failures.

Amazing.

### Function problem

↑ **Parent:** [Computational problem](#computational-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Function_problem)

A problem that has more than two possible yes/no outputs.

It is therefore a generalization of a [decision problem](#decision-problem).

#### Inverse problem

↑ **Parent:** [Function problem](#function-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inverse_problem)

#### Integer algorithm

↑ **Parent:** [Function problem](#function-problem)

We define an "integer algorithm" as an algorithm that takes [integer](formalization-of-mathematics.md#integer) inputs and produces [integer](formalization-of-mathematics.md#integer) outputs.

##### Integer multiplication

↑ **Parent:** [Integer algorithm](#integer-algorithm)

[https://cs.stackexchange.com/questions/16226/what-is-the-fastest-algorithm-for-multiplication-of-two-n-digit-numbers](https://cs.stackexchange.com/questions/16226/what-is-the-fastest-algorithm-for-multiplication-of-two-n-digit-numbers)

##### Integer factorization

↑ **Parent:** [Integer algorithm](#integer-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Integer_factorization)

Complexity: [NP-intermediate](#np-intermediate) as of 2020:
- expected not to be [NP-complete](#np-complete) because it would imply NP != [Co-NP](#co-np): [https://cstheory.stackexchange.com/questions/167/what-are-the-consequences-of-factoring-being-np-complete#comment104849_169](https://cstheory.stackexchange.com/questions/167/what-are-the-consequences-of-factoring-being-np-complete#comment104849_169)
- expected not to be in [P](#p-complexity) because "could we be that dumb that we haven't found a solution after having tried for that long?

The basis of RSA: [RSA](cryptography.md#rsa-cryptosystem). But not proved [NP-complete](#np-complete), which leads to:

###### Integer factorization algorithm

↑ **Parent:** [Integer factorization](#integer-factorization)

###### NP-hard cryptosystem

↑ **Parent:** [Integer factorization](#integer-factorization)

This is natural question because both [integer factorization](#integer-factorization) and [discrete logarithm](#discrete-logarithm) are the basis for the most popular [public-key cryptography](cryptography.md#public-key-cryptography) systems as of 2020 ([RSA](cryptography.md#rsa-cryptosystem) and [Diffie-Hellman key exchange](cryptography.md#diffie-hellman-key-exchange) respectively), and both are [NP-intermediate](#np-intermediate). Why not use something more provenly hard?
- [https://cs.stackexchange.com/questions/356/why-hasnt-there-been-an-encryption-algorithm-that-is-based-on-the-known-np-hard](https://cs.stackexchange.com/questions/356/why-hasnt-there-been-an-encryption-algorithm-that-is-based-on-the-known-np-hard) "Why hasn't there been an encryption algorithm that is based on the known NP-Hard problems?"

#### Discrete logarithm

↑ **Parent:** [Function problem](#function-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Discrete_logarithm)

[Logarithm](formalization-of-mathematics.md#logarithm) of a [discrete](calculus.md#discrete) [groups](group.md).

[NP-intermediate](#np-intermediate) as of 2020 for similar reasons as [integer factorization](#integer-factorization).

An important case is the [discrete logarithm of the cyclic group](#discrete-logarithm-of-the-cyclic-group) in which the group is a [cyclic group](group.md#cyclic-group).

##### Discrete logarithm of the cyclic group

↑ **Parent:** [Discrete logarithm](#discrete-logarithm)

This is the [discrete logarithm](#discrete-logarithm) problem where the group is a [cyclic group](group.md#cyclic-group).

In this case, the problem becomes equivalent to reversing [modular exponentiation](mathematics.md#modular-exponentiation).

This computational problem forms the basis for [Diffie-Hellman key exchange](cryptography.md#diffie-hellman-key-exchange), because [modular exponentiation](mathematics.md#modular-exponentiation) can be efficiently computed, but no known way exists to efficiently compute the reverse function.

#### Functional problem with array as input

↑ **Parent:** [Function problem](#function-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Functional_problem_with_array_as_input)

##### Largest element in an array

↑ **Parent:** [Functional problem with array as input](#functional-problem-with-array-as-input)

[https://www.geeksforgeeks.org/program-to-find-largest-element-in-an-array/](https://www.geeksforgeeks.org/program-to-find-largest-element-in-an-array/)

##### K-th largest element in an array

↑ **Parent:** [Functional problem with array as input](#functional-problem-with-array-as-input)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/K-th_largest_element_in_an_array)

Simple interview problem!
- [https://leetcode.com/problems/kth-largest-element-in-an-array/solutions/60309](https://leetcode.com/problems/kth-largest-element-in-an-array/solutions/60309)
- [https://www.geeksforgeeks.org/kth-largest-element-in-an-array/](https://www.geeksforgeeks.org/kth-largest-element-in-an-array/)

##### Longest common subsequence

↑ **Parent:** [Functional problem with array as input](#functional-problem-with-array-as-input)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Longest_common_subsequence)

Note that the subsequences do not need to be contiguous.

Implementations:
- [cpp/longest_common_subsequence.cpp](cpp/longest_common_subsequence.cpp)

On [coding challenge websites](website.md#programming-problem-collection-website):
- [https://leetcode.com/problems/longest-common-subsequence/description/](https://leetcode.com/problems/longest-common-subsequence/description/)
- [https://www.geeksforgeeks.org/longest-common-subsequence-dp-4/](https://www.geeksforgeeks.org/longest-common-subsequence-dp-4/)

##### Subset sum problem

↑ **Parent:** [Functional problem with array as input](#functional-problem-with-array-as-input)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Subset_sum_problem)

Sample implementation:
- [cpp/subset_sum.cpp](cpp/subset_sum.cpp)

On [coding challenge websites](website.md#programming-problem-collection-website):
- [https://www.hackerrank.com/challenges/subset-sum/problem](https://www.hackerrank.com/challenges/subset-sum/problem)
- [https://leetcode.com/problems/partition-equal-subset-sum/](https://leetcode.com/problems/partition-equal-subset-sum/)
- [https://www.geeksforgeeks.org/subset-sum-problem-dp-25/](https://www.geeksforgeeks.org/subset-sum-problem-dp-25/)

###### 3SUM

↑ **Parent:** [Subset sum problem](#subset-sum-problem)  
🏷️ **Tags:** [Simple to state but hard to prove](mathematics.md#simple-to-state-but-hard-to-prove)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/3SUM)

It is cool how even for such a "simple looking" problem, we were still unable to prove optimality as of 2020!

###### Two sum problem

↑ **Parent:** [3SUM](#3sum)

### Algorithm

↑ **Parent:** [Computational problem](#computational-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algorithm)

A solution to a [computational problem](#computational-problem)!

#### Algorithm cheatsheet

↑ **Parent:** [Algorithm](#algorithm)

Draft by [Ciro Santilli](ciro-santilli.md) with cross language input/output test cases: [https://github.com/cirosantilli/algorithm-cheat](https://github.com/cirosantilli/algorithm-cheat)

By others:
- [https://github.com/TheAlgorithms/Python](https://github.com/TheAlgorithms/Python)

#### Data structure

↑ **Parent:** [Algorithm](#algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Data_structure)

##### Associative array

↑ **Parent:** [Data structure](#data-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Associative_array)

More commonly known as a map or dictionary.

###### Binary search tree

↑ **Parent:** [Associative array](#associative-array)  
🏷️ **Tags:** [Binary tree](mathematics.md#binary-tree), [Ordered tree](mathematics.md#ordered-tree)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Binary_search_tree)

###### B-tree

↑ **Parent:** [Binary search tree](#binary-search-tree)

Like [Binary search tree](#binary-search-tree), but each node can have multiple objects and more than two children.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/65/B-tree.svg/960px-B-tree.svg.png)

**[Figure 2](#_253)** [Source](https://commons.wikimedia.org/wiki/File:B-tree.svg.png).

###### Hash table

↑ **Parent:** [Associative array](#associative-array)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hash_table)

##### Dynamic array

↑ **Parent:** [Data structure](#data-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dynamic_array)

##### Linked list

↑ **Parent:** [Data structure](#data-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linked_list)

##### Trie

↑ **Parent:** [Data structure](#data-structure)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Trie)

Sample implementations:
- [C++](programming-language.md#c-plus-plus): [cpp/trie.cpp](cpp/trie.cpp)

#### Recursion (computer science)

↑ **Parent:** [Algorithm](#algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Recursion_(computer_science))

##### Iteration

↑ **Parent:** [Recursion (computer science)](#recursion-computer-science)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Iteration)

###### Iterative algorithm

↑ **Parent:** [Iteration](#iteration)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Iterative_algorithm)

#### Sorting algorithm

↑ **Parent:** [Algorithm](#algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sorting_algorithm)

##### String-sorting algorithm

↑ **Parent:** [Sorting algorithm](#sorting-algorithm)

###### Natural sort order

↑ **Parent:** [String-sorting algorithm](#string-sorting-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Natural_sort_order)

#### String-search algorithm

↑ **Parent:** [Algorithm](#algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/String-search_algorithm)

#### Class of algorithm

↑ **Parent:** [Algorithm](#algorithm)

##### Greedy algorithm

↑ **Parent:** [Class of algorithm](#class-of-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Greedy_algorithm)

##### Dynamic programming

↑ **Parent:** [Class of algorithm](#class-of-algorithm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dynamic_programming)

### Complexity class

↑ **Parent:** [Computational problem](#computational-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Complexity_class)

#### Time complexity

↑ **Parent:** [Complexity class](#complexity-class)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Time_complexity)

##### Quasilinear time

↑ **Parent:** [Time complexity](#time-complexity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quasilinear_time)

#### Big O notation family

↑ **Parent:** [Complexity class](#complexity-class)

This is a family of notations related to the [big O notation](#big-o-notation). A good mnemonic summary of all notations would be:
- [big O notation](#big-o-notation): $|f| \le g$
- [little-o notation](#little-o-notation): $|f| \lt g$

##### Big O notation

↑ **Parent:** [Big O notation family](#big-o-notation-family)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Big_O_notation)

Module bound above, possibly multiplied by a constant:

$$
f(x) = O(g(x))
$$

is defined as:

$$
\exists M > 0 \exists x_0  \forall x > x_0 \colon |f(x)| \leq M g(x)
$$

E.g.:
- $\forall c \in \R x + c = O(x)$. For $c < 0$, $M = 1$ is enough. Otherwise, any $M > 1$ will do, the bottom line will always catch up to the top one eventually.

##### Little-o notation

↑ **Parent:** [Big O notation family](#big-o-notation-family)

Stronger version of the [big O notation](#big-o-notation), basically means that ratio goes to zero. In [big O notation](#big-o-notation), the ratio does not need to go to zero.

So in informal terms, [big O notation](#big-o-notation) means $\leq$, and [little-o notation](#little-o-notation) means $<$.

E.g.:
- $x = O(x)$
- $x \ne o(x)$K does not tend to zero
- $x = O(x^2)$
- $x = o(x^2)$

#### Primitive recursive function

↑ **Parent:** [Complexity class](#complexity-class)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Primitive_recursive_function)

In intuitive terms it consists of all integer functions, possibly with multiple input arguments, that can be written only with a sequence of:
- variable assignments
- addition and subtraction
- integer comparisons and if/else
- [for loops](programming-language.md#for-loop)

```
for (i = 0; i < n; i++)
```
and such that `n` does not change inside the loop body, i.e. no [while loops](programming-language.md#while-loop) with arbitrary conditions.

`n` does not have to be a constant, it may come from previous calculations. But it must not change inside the loop body.

[Primitive recursive functions](#primitive-recursive-function) basically include every integer function that comes up in practice. Primitive recursive functions can have huge complexity, and it strictly contains [EXPTIME](#exptime). As such, they mostly only come up in [foundation of mathematics](formalization-of-mathematics.md) contexts.

The cool thing about [primitive recursive functions](#primitive-recursive-function) is that the number of iterations is always bound, so we are certain that they terminate and are therefore [computable](#computable-problem).

This also means that there are necessarily functions which are not [primitive recursive](#primitive-recursive-function), as we know that there must exist [uncomputable](#computable-problem) functions, e.g. the [busy beaver function](#busy-beaver-function).

Adding unbounded [while loops](programming-language.md#while-loop) of course enables us to simulate arbitrary [Turing machines](#turing-machine), and therefore increases the [complexity class](#complexity-class).

More finely, there are [non-primitive total recursive functions](#non-primitive-total-recursive-function), e.g. most famously the [Ackermann function](#ackermann-function).

##### Non-primitive total recursive function

↑ **Parent:** [Primitive recursive function](#primitive-recursive-function)

###### Ackermann function

↑ **Parent:** [Non-primitive total recursive function](#non-primitive-total-recursive-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ackermann_function)

To get an intuition for it, see the sample computation at: [https://en.wikipedia.org/w/index.php?title=Ackermann_function&oldid=1170238965#TRS,_based_on_2-ary_function](https://en.wikipedia.org/w/index.php?title=Ackermann_function&oldid=1170238965#TRS,_based_on_2-ary_function) where $S(n) = n + 1$ in this context. From this, we immediately get the intuition that these functions are recursive somehow.

#### Galactic algorithm

↑ **Parent:** [Complexity class](#complexity-class)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Galactic_algorithm)

#### ELEMENTARY (complexity)

↑ **Parent:** [Complexity class](#complexity-class)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/EXPTIME)

##### EXPTIME

↑ **Parent:** [ELEMENTARY (complexity)](#elementary-complexity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/EXPTIME)

###### PSPACE

↑ **Parent:** [EXPTIME](#exptime)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PSPACE)

###### NP (complexity)

↑ **Parent:** [PSPACE](#pspace)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NP_(complexity))

Strictly speaking, only defined for decision problems: [https://cs.stackexchange.com/questions/9664/is-it-necessary-for-np-problems-to-be-decision-problems/128702#128702](https://cs.stackexchange.com/questions/9664/is-it-necessary-for-np-problems-to-be-decision-problems/128702#128702)

###### P (complexity)

↑ **Parent:** [NP (complexity)](#np-complexity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/P_(complexity))

###### NC (complexity)

↑ **Parent:** [P (complexity)](#p-complexity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NC_(complexity))

###### Polynomial time algorithm

↑ **Parent:** [P (complexity)](#p-complexity)

###### NP-complete

↑ **Parent:** [NP (complexity)](#np-complexity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NP-completeness)

A problem that is both [NP](#np-complexity) and [NP-hard](#np-hard).

###### Cook-Levin theorem

↑ **Parent:** [NP-complete](#np-complete)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cook–Levin_theorem)

###### P versus NP problem

↑ **Parent:** [NP-complete](#np-complete)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/P_versus_NP_problem)

Interesting because of the [Cook-Levin theorem](#cook-levin-theorem): if only a single [NP-complete](#np-complete) problem were in [P](#p-complexity), then all NP-complete problems would also be P!

We all know the answer for this: either false or [independent](formalization-of-mathematics.md#independence-mathematical-logic).

<h6 id="ladner-s-theorem">Ladner's Theorem</h6>

↑ **Parent:** [P versus NP problem](#p-versus-np-problem)

###### NP-hard

↑ **Parent:** [NP (complexity)](#np-complexity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NP-hardness)

A problem such that all NP problems can be reduced in polynomial time to it.

###### NP-intermediate

↑ **Parent:** [NP (complexity)](#np-complexity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NP-intermediate)

This is the most interesting class of problems for [BQP](#bqp) as we haven't proven that they are neither:
- [P](#p-complexity): would be boring on quantum computer
- [NP-complete](#np-complete): would likely be impossible on a quantum computer

Big list: [https://cstheory.stackexchange.com/questions/79/problems-between-p-and-npc/460#460](https://cstheory.stackexchange.com/questions/79/problems-between-p-and-npc/460#460)

###### BQP

↑ **Parent:** [NP-intermediate](#np-intermediate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/BQP)

[P](#p-complexity) for [quantum computing](quantum-computing.md)!

Heck, we know nothing about this class yet related to non quantum classes!
- conjectured not to intersect with [NP-complete](#np-complete), because if it were, all NP-complete problems could be solved efficiently on quantum computers, and none has been found so far as of 2020.
- conjectured to be larger than [P](#p-complexity), but we don't have a single algorithm provenly there:
  - it is believed that the NP complete ones can't be solved
  - if they were neither NP-complete nor P, it would imply [P != NP](#p-versus-np-problem)
- we just don't know if it is even contained inside [NP](#np-complexity)!

###### Co-NP

↑ **Parent:** [NP (complexity)](#np-complexity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Co-NP)

- [https://math.stackexchange.com/questions/361422/why-isnt-np-conp](https://math.stackexchange.com/questions/361422/why-isnt-np-conp) "Why isn't NP = coNP?"
- [https://stackoverflow.com/questions/17046440/whats-the-difference-between-np-and-co-np](https://stackoverflow.com/questions/17046440/whats-the-difference-between-np-and-co-np)
- [https://cs.stackexchange.com/questions/9795/is-the-open-question-np-co-np-the-same-as-p-np](https://cs.stackexchange.com/questions/9795/is-the-open-question-np-co-np-the-same-as-p-np)
- [https://mathoverflow.net/questions/31821/problems-known-to-be-in-both-np-and-conp-but-not-known-to-be-in-p](https://mathoverflow.net/questions/31821/problems-known-to-be-in-both-np-and-conp-but-not-known-to-be-in-p)

### Constraint satisfaction problem

↑ **Parent:** [Computational problem](#computational-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem)

### Optimization problem

↑ **Parent:** [Computational problem](#computational-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Optimization_problem)

#### Linear programming

↑ **Parent:** [Optimization problem](#optimization-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Linear_programming)

#### Logistics

↑ **Parent:** [Optimization problem](#optimization-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Logistics)

##### Last mile problem

↑ **Parent:** [Logistics](#logistics)

The exact same problem appears over and over, e.g.:
- [transportaion](https://en.wikipedia.org/wiki/Last_mile_(transportation)): the last mile of the trip when everyone leaves the train and goes to their different respective offices is the most expensive
- [telecommunications](https://en.wikipedia.org/wiki/Last_mile_(telecommunications)): the last mile of wire linking local hubs to actual homes is the most expensive
- electrical grid: same as telecommunications

[Ciro Santilli](ciro-santilli.md) also identified knowledge version of this problem: [the missing link between basic and advanced](ciro-santilli.md#the-missing-link-between-basic-and-advanced).

#### Optimization software

↑ **Parent:** [Optimization problem](#optimization-problem)  
🏷️ **Tags:** [Software](software.md)

- [https://en.wikipedia.org/wiki/List_of_optimization_software](https://en.wikipedia.org/wiki/List_of_optimization_software)
- [https://en.wikipedia.org/wiki/Comparison_of_optimization_software](https://en.wikipedia.org/wiki/Comparison_of_optimization_software)

##### CPLEX

↑ **Parent:** [Optimization software](#optimization-software)

#### Limiting factor

↑ **Parent:** [Optimization problem](#optimization-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Limiting_factor)

##### Critical path method

↑ **Parent:** [Limiting factor](#limiting-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Critical_path_method)

###### Critical path

↑ **Parent:** [Critical path method](#critical-path-method)

###### Dependency graph

↑ **Parent:** [Critical path method](#critical-path-method)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dependency_graph)

#### Value function

↑ **Parent:** [Optimization problem](#optimization-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Value_function)

The function being maximized in a [optimization problem](#optimization-problem).

### List of computational problems

↑ **Parent:** [Computational problem](#computational-problem)

## Computer scientist

↑ **Parent:** [Computer science](computer-science.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computer_scientist)

### Alan Turing

↑ **Parent:** [Computer scientist](#computer-scientist)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Alan_Turing)

### Noam Chomsky

↑ **Parent:** [Computer scientist](#computer-scientist)  
🏷️ **Tags:** [Cool person](cirism.md#cool-person)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Noam_Chomsky)

### Scott Aaronson

↑ **Parent:** [Computer scientist](#computer-scientist)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Scott_Aaronson)

## Cryptography

↑ **Parent:** [Computer science](computer-science.md)

[This section is present in another page, follow this link to view it.](cryptography.md)

## Hash function

↑ **Parent:** [Computer science](computer-science.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hash_function)

Applications:
- [hash map](https://en.wikipedia.org/wiki/Hash_table) which is a O(1) amortized implementation of a map
- creating unbreakable chains of data, e.g. for [Git commits](https://stackoverflow.com/questions/22968856/what-is-the-file-format-of-a-git-commit-object-data-structure/37438460#37438460) or [Bitcoin](cryptocurrency.md#bitcoin). 
- storing passwords on a server in a way that if the password database is stolen, attackers can't reuse them on other websites where the user used the same password: [https://security.blogoverflow.com/2013/09/about-secure-password-hashing/](https://security.blogoverflow.com/2013/09/about-secure-password-hashing/)

### Secure Hash Algorithms

↑ **Parent:** [Hash function](#hash-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Secure_Hash_Algorithms)

#### SHA-1

↑ **Parent:** [Secure Hash Algorithms](#secure-hash-algorithms)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SHA-1)

#### SHA-2

↑ **Parent:** [Secure Hash Algorithms](#secure-hash-algorithms)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SHA-2)

##### SHA-256

↑ **Parent:** [SHA-2](#sha-2)

### Merkle tree

↑ **Parent:** [Hash function](#hash-function)

## Computer science bibliography

↑ **Parent:** [Computer science](computer-science.md)

### Computer science YouTube channel

↑ **Parent:** [Computer science bibliography](#computer-science-bibliography)  
🏷️ **Tags:** [YouTube channel](website.md#youtube-channel)

#### Computerphile

↑ **Parent:** [Computer science YouTube channel](#computer-science-youtube-channel)  
🏷️ **Tags:** [Brady Haran production](#brady-haran-production)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computerphile)

##### Brady Haran

↑ **Parent:** [Computerphile](#computerphile)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Brady_Haran)

###### Brady Haran production

↑ **Parent:** [Brady Haran](#brady-haran)  
🏷️ **Tags:** [Science communicator](science.md#science-communicator)

## ↑ Ancestors (5)

1. [Computer](computer.md)
2. [Information technology](technology.md#information-technology)
3. [Area of technology](technology.md#area-of-technology)
4. [Technology](technology.md)
5. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (7)

- [The best articles by Ciro Santilli](articles.md)
- [Collatz conjecture](formalization-of-mathematics.md#collatz-conjecture)
- [Decision problem](#decision-problem)
- [Human brain](brain.md#human-brain)
- [Project Euler problem style](project-euler.md#project-euler-problem-style)
- [Qxir](website.md#qxir)
- [Universal Turing machine](#universal-turing-machine)
