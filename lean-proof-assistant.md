# Lean (proof assistant)

↑ **Parent:** [List of proof assistants](list-of-proof-assistants.md)  
🏷️ **Tags:** [Microsoft product](microsoft-product.md), [Open source software](open-source-software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lean_(proof_assistant))

[Source code](source-code.md):
- [https://github.com/leanprover/lean4](https://github.com/leanprover/lean4) why a separate repo per version... but it is what it is.
- [https://github.com/leanprover/lean](https://github.com/leanprover/lean)

The way [Lean](lean-proof-assistant.md) and [Coq](coq-software.md) mix programming and mathematics is a thing of great beauty. This is especially notable in lean as you start to play with with things such as:

- `partial`env lean functions, and using `terminates_by` to prove that certain functions terminate. Lean requires explicitly known if functions terminate or not to be able to use them in proofs.
- `noncomputable` functions. Lean allows you to define mathematical functions which you can't actually execute, and it tracks that explicitly

They are huge fans of [Unicode](unicode.md) characters! Check this out from a [formal proof of the prime number theorem](formal-proof-of-the-prime-number-theorem.md): [https://github.com/AlexKontorovich/PrimeNumberTheoremAnd/blob/fbdbb5310d036d33b9797b35f3b04b08f2447a6e/PrimeNumberTheoremAnd/ZetaBounds.lean](https://github.com/AlexKontorovich/PrimeNumberTheoremAnd/blob/fbdbb5310d036d33b9797b35f3b04b08f2447a6e/PrimeNumberTheoremAnd/ZetaBounds.lean) Here's map to Ascii: [https://proofassistants.stackexchange.com/questions/954/does-lean-have-a-standard-ascii-representation/5289#5289](https://proofassistants.stackexchange.com/questions/954/does-lean-have-a-standard-ascii-representation/5289#5289)

Their dependency graph thingy is just beautiful however: [https://alexkontorovich.github.io/PrimeNumberTheoremAnd/web/dep_graph_document.html](https://alexkontorovich.github.io/PrimeNumberTheoremAnd/web/dep_graph_document.html)

Their 2025 current installation method is bullshit, recommends [VS Code](visual-studio-code.md) extension on Ubuntu. Lol.

From CLI:
```
curl https://elan.lean-lang.org/elan-init.sh -sSf | sh
source $HOME/.elan/env
```
Then when you run:
```
lean
```
it downloads the `lean` executable for you. Insane shit, could only come from a [Microsoft](microsoft-split.md) mindset.

**Table of contents**

- [Lean utility](lean-utility.md)
  - [elan](elan.md)
  - [Lean autoformatter](lean-autoformatter.md)
- [Lean vs Coq](lean-vs-coq.md)
- [Lean Zulip](lean-zulip.md)
- [Lean bibliography](lean-bibliography.md)
  - [How To Prove It with Lean ](how-to-prove-it-with-lean.md)
  - [Logic and Proof (Lean book)](logic-and-proof-lean-book.md)
- [Lean library](lean-library.md)
  - [Lean Mathlib](lean-mathlib.md)
    - [mathlib4](mathlib4.md)
  - [Formal Conjectures](formal-conjectures.md)

## ↑ Ancestors (6)

1. [List of proof assistants](list-of-proof-assistants.md)
2. [Proof assistant](proof-assistant.md)
3. [Formalization of mathematics](formalization-of-mathematics-split.md)
4. [Area of mathematics](area-of-mathematics.md)
5. [Mathematics](mathematics-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (3)

- [Microsoft](microsoft-split.md)
- [The Math Genome Project](the-math-genome-project.md)
- [Website front-end for a mathematical formal proof system](website-front-end-for-a-mathematical-formal-proof-system.md)
