# Formalization of mathematics

↑ **Parent:** [Area of mathematics](mathematics.md#area-of-mathematics)

Mathematics is a [beautiful game](art.md) played on [strings](https://en.wikipedia.org/wiki/String_(computer_science), which [mathematicians](mathematics.md#mathematician) call ["theorems"](https://en.wikipedia.org/wiki/Theorem).

Here is a more understandable description of the semi-satire that follows: [https://math.stackexchange.com/questions/53969/what-does-formal-mean/3297537#3297537](https://math.stackexchange.com/questions/53969/what-does-formal-mean/3297537#3297537)

You start with a very small list of:
- certain arbitrarily chosen initial strings, which mathematicians call "[axioms](#axiom)"
- rules of how to obtain new strings from old strings, called ["rules of inference"](https://en.wikipedia.org/wiki/Rule_of_inference) Every transformation rule is very simple, and can be verified by a computer.

Using those rules, you choose a target string that you want to reach, and then try to reach it. Before the target string is reached, mathematicians call it a ["conjecture"](https://en.wikipedia.org/wiki/Conjecture).

Mathematicians call the list of transformation rules used to reach a string a ["proof"](https://en.wikipedia.org/wiki/Mathematical_proof).

Since every step of the proof is very simple and can be verified by a computer automatically, the entire proof can also be automatically verified by a computer very easily.

Finding proofs however is undoubtedly an [uncomputable problem](computer-science.md#computable-problem).

Most mathematicians can't code or deal with the real world in general however, so they haven't created the obviously necessary: [website front-end for a mathematical formal proof system](todo.md#website-front-end-for-a-mathematical-formal-proof-system).

The fact that Mathematics happens to be the best way to describe [physics](physics.md) and that humans can use physical intuition heuristics to reach the NP-hard proofs of mathematics is one of the great miracles of the universe.

Once we have mathematics formally modelled, one of the coolest results is [Gödel's incompleteness theorems](https://en.wikipedia.org/wiki/G%C3%B6del%27s_incompleteness_theorems), which states that for any reasonable proof system, there are necessarily theorems that cannot be proven neither true nor false starting from any given set of axioms: those theorems are independent from those axioms. Therefore, there are three possible outcomes for any hypothesis: true, false or independent!

Some famous theorems have even been proven to be independent of some famous [axioms](#axiom). One of the most notable is that the [Continuum Hypothesis](http://en.wikipedia.org/wiki/Continuum_hypothesis) is [independent](#independence-mathematical-logic) from [Zermelo-Fraenkel set theory](#zermelo-fraenkel-set-theory)! Such independence proofs rely on modelling the proof system inside another proof system, and [forcing](https://en.wikipedia.org/wiki/Forcing_(mathematics)) is one of the main techniques used for this.

<a id="image-the-landscape-of-modern-mathematics-comic-by-abstruse-goose"></a>
![](https://web.archive.org/web/20190430151331im_/http://abstrusegoose.com/strips/i_dont_give_a_shit_about_your_mountain.png)

**[Figure 1](#image-the-landscape-of-modern-mathematics-comic-by-abstruse-goose). The landscape of modern Mathematics comic by Abstruse Goose**. [Source](https://abstrusegoose.com/211). This comic shows that Mathematics is one of the most diversified areas of [useless](art.md) human knowledge.

**Table of contents**

- [Formal proof systems and LLMs are a match made in heaven](#formal-proof-systems-and-llms-are-a-match-made-in-heaven)
- [Proof assistant](#proof-assistant)
  - [QED manifesto](#qed-manifesto)
  - [Web-based proof assistant](#web-based-proof-assistant)
    - [The Math Genome Project](#the-math-genome-project)
  - [Comparison of proof assistants](#comparison-of-proof-assistants)
  - [List of proof assistants](#list-of-proof-assistants)
    - [Lean (proof assistant)](#lean-proof-assistant)
      - [Lean utility](#lean-utility)
        - [elan](#elan)
        - [Lean autoformatter](#lean-autoformatter)
      - [Lean vs Coq](#lean-vs-coq)
      - [Lean Zulip](#lean-zulip)
      - [Lean bibliography](#lean-bibliography)
        - [How To Prove It with Lean ](#how-to-prove-it-with-lean)
        - [Logic and Proof (Lean book)](#logic-and-proof-lean-book)
      - [Lean library](#lean-library)
        - [Lean Mathlib](#lean-mathlib)
          - [mathlib4](#mathlib4)
        - [Formal Conjectures](#formal-conjectures)
    - [Coq (software)](#coq-software)
    - [Mathematical Intelligence (Proof assistant)](#mathematical-intelligence-proof-assistant)
    - [Metamath](#metamath)
- [Formal proof](#formal-proof)
  - [Formal proof is useless](#formal-proof-is-useless)
  - [Mathematical proof](#mathematical-proof)
  - [Formal system](#formal-system)
    - [Set theory](#set-theory)
      - [Zermelo-Fraenkel set theory](#zermelo-fraenkel-set-theory)
        - [Zermelo-Fraenkel axioms](#zermelo-fraenkel-axioms)
          - [Zermelo-Fraenkel axioms with the axiom of choice](#zermelo-fraenkel-axioms-with-the-axiom-of-choice)
    - [Type theory](#type-theory)
  - [Axiom](#axiom)
    - [Consistency](#consistency)
    - [Independence (mathematical logic)](#independence-mathematical-logic)
  - [Open problem in mathematics](#open-problem-in-mathematics)
    - [Conjecture](#conjecture)
      - [Famous conjecture](#famous-conjecture)
        - [Collatz conjecture](#collatz-conjecture)
          - [Collatz function](#collatz-function)
            - [Shortcut Collatz function](#shortcut-collatz-function)
          - [Collatz conjecture failure mode](#collatz-conjecture-failure-mode)
            - [Collatz cycle](#collatz-cycle)
              - [Collatz n-cycle](#collatz-n-cycle)
                - [Collatz 1-cycle](#collatz-1-cycle)
                - [Collatz cycle length lower bound](#collatz-cycle-length-lower-bound)
            - [Unbounded Collatz trajectory](#unbounded-collatz-trajectory)
          - [Collatz-like problem](#collatz-like-problem)
          - [The Busy Beaver Competition: a historical survey by Pascal Michel](#the-busy-beaver-competition-a-historical-survey-by-pascal-michel)
          - [Erdős' conjecture on powers of 2](#erdos-conjecture-on-powers-of-2)
  - [Theorem](#theorem)
    - [Corollary](#corollary)
- [Lemma (mathematics)](#lemma-mathematics)
- [Set (mathematics)](#set-mathematics)
  - [Union (set theory)](#union-set-theory)
  - [Cardinality](#cardinality)
- [Function (mathematics)](#function-mathematics)
  - [Domain, codomain and image](#domain-codomain-and-image)
    - [Bijection](#bijection)
      - [Injective function](#injective-function)
      - [Surjective function](#surjective-function)
    - [Domain of a function](#domain-of-a-function)
    - [Codomain](#codomain)
      - [Endofunction](#endofunction)
    - [Image (mathematics)](#image-mathematics)
  - [Periodic function](#periodic-function)
    - [Square wave](#square-wave)
      - [Rectangular wave](#rectangular-wave)
  - [Function by signature](#function-by-signature)
    - [Functional function](#functional-function)
      - [Convolution](#convolution)
    - [Set function](#set-function)
      - [Cartesian product](#cartesian-product)
      - [Direct product](#direct-product)
    - [Numeric function](#numeric-function)
      - [Addition](#addition)
      - [Subtraction](#subtraction)
      - [Multiplication](#multiplication)
      - [Division](#division)
      - [Exponentiation](#exponentiation)
        - [Exponentiation grows really fast](#exponentiation-grows-really-fast)
          - [Wheat and chessboard problem](#wheat-and-chessboard-problem)
        - [nth root](#nth-root)
          - [Square root](#square-root)
        - [Exponentiation functional equation](#exponentiation-functional-equation)
        - [Exponential function](#exponential-function)
          - [Exponential function differential equation](#exponential-function-differential-equation)
          - [Definition of the exponential function](#definition-of-the-exponential-function)
            - [Taylor expansion definition of the exponential function](#taylor-expansion-definition-of-the-exponential-function)
            - [Product definition of the exponential function](#product-definition-of-the-exponential-function)
          - [Gaussian function](#gaussian-function)
          - [Logarithm](#logarithm)
          - [Matrix exponential](#matrix-exponential)
            - [Logarithm of a matrix](#logarithm-of-a-matrix)
              - [Existence of the matrix logarithm](#existence-of-the-matrix-logarithm)
      - [Polynomial](#polynomial)
        - [Degree of a polynomial](#degree-of-a-polynomial)
        - [Algebraic equation](#algebraic-equation)
          - [Named algebraic equation](#named-algebraic-equation)
            - [Quadratic equation](#quadratic-equation)
              - [Quadratic equation modulo n](#quadratic-equation-modulo-n)
              - [Quadratic formula](#quadratic-formula)
            - [Cubic equation](#cubic-equation)
            - [Quartic equation](#quartic-equation)
            - [Quintic equation](#quintic-equation)
              - [Abel-Ruffini theorem](#abel-ruffini-theorem)
          - [Algebraic equation over a field](#algebraic-equation-over-a-field)
          - [Algebraic equation modulo n](#algebraic-equation-modulo-n)
          - [Algebraic number](#algebraic-number)
            - [Algebraic number field](#algebraic-number-field)
            - [Algebraic function](#algebraic-function)
            - [Transcendental number](#transcendental-number)
              - [Transcendental number conjecture](#transcendental-number-conjecture)
        - [Diophantine equation](#diophantine-equation)
          - [Pythagorean triple](#pythagorean-triple)
            - [Euclid's formula](#euclid-s-formula)
              - [There are infinitely many Pythagorean triples](#there-are-infinitely-many-pythagorean-triples)
              - [Euclid's formula generates all Pythagorean triples](#euclid-s-formula-generates-all-pythagorean-triples)
            - [Classification of Pythagorean triples](#classification-of-pythagorean-triples)
            - [Taxicab number](#taxicab-number)
            - [Fermat's last theorem](#fermat-s-last-theorem)
              - [Formalization of Fermat's last theorem](#formalization-of-fermat-s-last-theorem)
              - [Andrew Wiles](#andrew-wiles)
          - [Hilbert's tenth problem](#hilbert-s-tenth-problem)
            - [Hilbert's tenth problem variant](#hilbert-s-tenth-problem-variant)
              - [Decidability of Hilbert's tenth problem in modular arithmetic](#decidability-of-hilbert-s-tenth-problem-in-modular-arithmetic)
              - [Decidability of Hilbert's tenth problem of a given degree and number of variables](#decidability-of-hilbert-s-tenth-problem-of-a-given-degree-and-number-of-variables)
                - [Quadratic Diophantine equation](#quadratic-diophantine-equation)
                - [Hilbert's tenth problem is decidable for quadratic equations](#hilbert-s-tenth-problem-is-decidable-for-quadratic-equations)
                - [Undecidable Diophantine equation example](#undecidable-diophantine-equation-example)
              - [Hilbert's tenth problem over other rings](#hilbert-s-tenth-problem-over-other-rings)
          - [Additive number theory](#additive-number-theory)
            - [Additive basis](#additive-basis)
              - [Additive basis theorem](#additive-basis-theorem)
                - [Waring's problem](#waring-s-problem)
                  - [Waring's problem for squares](#waring-s-problem-for-squares)
                    - [Lagrange's four-square theorem](#lagrange-s-four-square-theorem)
                    - [Legendre's three-square theorem](#legendre-s-three-square-theorem)
                    - [Sum of two squares theorem](#sum-of-two-squares-theorem)
                  - [Waring problem variant](#waring-problem-variant)
                    - [Waring problem with negative numbers allowed](#waring-problem-with-negative-numbers-allowed)
                      - [Sum of three cubes](#sum-of-three-cubes)
                    - [Waring-Goldbach problem](#waring-goldbach-problem)
        - [Named small order polynomial](#named-small-order-polynomial)
          - [Linear polynomial](#linear-polynomial)
        - [Galois theory](#galois-theory)
        - [Irreducible polynomial](#irreducible-polynomial)
        - [Multivariate polynomial](#multivariate-polynomial)
        - [Domain of a polynomial](#domain-of-a-polynomial)
          - [Polynomial over a field](#polynomial-over-a-field)
          - [Polynomial over a ring](#polynomial-over-a-ring)
          - [Polynomial over a commutative ring](#polynomial-over-a-commutative-ring)
        - [Polynomial ring](#polynomial-ring)
      - [Step function](#step-function)
        - [Heavyside step function](#heavyside-step-function)
      - [Integer sequence](#integer-sequence)
        - [Fibonacci sequence](#fibonacci-sequence)
        - [Tribonacci](#tribonacci)
        - [Kolakoski sequence](#kolakoski-sequence)
          - [Generalized Kolakoski sequence](#generalized-kolakoski-sequence)
          - [Nilsson algorithm for the Kolakoski sequence](#nilsson-algorithm-for-the-kolakoski-sequence)
          - [Nilsson algorithm for the generalized Kolakoski sequence](#nilsson-algorithm-for-the-generalized-kolakoski-sequence)
- [Function space](#function-space)
- [Number](#number)
  - [Scientific notation](#scientific-notation)
    - [E notation](#e-notation)
  - [Natural number](#natural-number)
  - [Integer](#integer)
  - [Rational number](#rational-number)
    - [Irrational number](#irrational-number)
      - [Number of unknown rationality](#number-of-unknown-rationality)
    - [Fraction](#fraction)
      - [Reduced fraction](#reduced-fraction)
        - [Farey sequence](#farey-sequence)
          - [Farey sunburst](#farey-sunburst)
        - [Number of elements in a Farey sequence](#number-of-elements-in-a-farey-sequence)
      - [Numerator](#numerator)
      - [Denominator](#denominator)
  - [Real number](#real-number)
    - [Dedekind cut](#dedekind-cut)
    - [Cardinality of the continuum](#cardinality-of-the-continuum)
      - [Countable set](#countable-set)
      - [Cantor's diagonal argument](#cantor-s-diagonal-argument)
    - [Mathematical constant](#mathematical-constant)
      - [Pi](#pi)
- [Complex number](#complex-number)
  - [Complex conjugate](#complex-conjugate)
  - [Imaginary number](#imaginary-number)
  - [Imaginary unit](#imaginary-unit)
  - [Cayley-Dickson construction](#cayley-dickson-construction)
    - [Quaternion](#quaternion)
    - [Octonion](#octonion)
    - [Sedenion](#sedenion)
- [Ordered pair](#ordered-pair)
- [Logic](#logic)
  - [Propositional logic](#propositional-logic)
    - [Modus ponens](#modus-ponens)
    - [If and only if](#if-and-only-if)
  - [First-order logic](#first-order-logic)
    - [Existential quantification](#existential-quantification)
      - [Existence and uniqueness](#existence-and-uniqueness)
        - [Existence](#existence)
        - [Uniqueness](#uniqueness)
    - [Universal quantification](#universal-quantification)
- [Entity formalizing mathematics](#entity-formalizing-mathematics)
  - [expMath](#expmath)
- [Formalization of X](#formalization-of-x)
  - [Formalization of physics](#formalization-of-physics)
    - [Formalization of physics project](#formalization-of-physics-project)
      - [PhysLean](#physlean)
      - [Physics Derivation Graph](#physics-derivation-graph)

## [Formal proof systems](#formal-system) and [LLMs](artificial-intelligence.md#large-language-model) are a match made in heaven

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)

On one hand, [formal proof systems](#formal-system) prevent [hallucinations](artificial-intelligence.md#hallucination-artificial-intelligence).

On the other hand, [LLMs](artificial-intelligence.md#large-language-model) can handle the mega verbosity and learning curve of [formal proof systems](#formal-system) which few humans are willing to undertake.

The human only needs to understand the bare minium of the formal proof system to know that statements are what they say they are. LLMs can then take care of the proof entirely.

It's really a killer combo.

## Proof assistant

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Proof_assistant)

Much of this section will be dumped at [Section "Website front-end for a mathematical formal proof system"](todo.md#website-front-end-for-a-mathematical-formal-proof-system) instead.

### QED manifesto

↑ **Parent:** [Proof assistant](#proof-assistant)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/QED_manifesto)

If [Ciro Santilli](ciro-santilli.md) ever becomes rich, he's going to solve this with: [website front-end for a mathematical formal proof system](todo.md#website-front-end-for-a-mathematical-formal-proof-system), promise.

### Web-based proof assistant

↑ **Parent:** [Proof assistant](#proof-assistant)

A more verbose description of this at: [Section "Website front-end for a mathematical formal proof system"](todo.md#website-front-end-for-a-mathematical-formal-proof-system).

#### The Math Genome Project

↑ **Parent:** [Web-based proof assistant](#web-based-proof-assistant)  
🏷️ **Tags:** [Closed source software](software.md#closed-source-software)

[https://www.themathgenome.com/](https://www.themathgenome.com/)

The website was dead as of February 2025. Last archive: [https://web.archive.org/web/20240418004442/http://www.themathgenome.com/](https://web.archive.org/web/20240418004442/http://www.themathgenome.com/) Pings:
- [https://x.com/cirosantilli/status/1890873216551313861](https://x.com/cirosantilli/status/1890873216551313861)
They were seeking help on May 2024:
- [https://x.com/TheMathGenome/status/1792963871193608593](https://x.com/TheMathGenome/status/1792963871193608593)
- [https://www.linkedin.com/feed/update/urn:li:activity:7198688750355259393/](https://www.linkedin.com/feed/update/urn:li:activity:7198688750355259393/)
so its likely the followup death. LinkedIn post gives basic stack: MERN stack, [Heroku](computer-hardware.md#heroku), Supabase/[MongoDB](software.md#mongodb) Atlas.

Appears to support multiple [proof assistant](#proof-assistant) backends including [Lean](#lean-proof-assistant), Hol and [Coq](#coq-software).

A discussion on the [Lean](#lean-proof-assistant) Zulip: [https://leanprover.zulipchat.com/#narrow/stream/113488-general/topic/The.20Math.20Genome.20Project/near/352639129](https://leanprover.zulipchat.com/#narrow/stream/113488-general/topic/The.20Math.20Genome.20Project/near/352639129). Lean people are not convinced about the model in general it seems however.

TODO [closed source](software.md#closed-source-software)? Really? [https://www.themathgenome.com/pricing](https://www.themathgenome.com/pricing)

TODO not viewable without login?

Has [conjectures](#conjecture) feature.

Built by this dude John Mercer:
- [https://www.linkedin.com/in/johnmercer/](https://www.linkedin.com/in/johnmercer/)
- [https://x.com/john_d_mercer](https://x.com/john_d_mercer)
He must be [independently wealthy](economy.md#independently-wealthy) or something to do such a project? What a hero. But he seems to have jobs. On the side? Hardcore.

A failed [Hacker News](website.md#hacker-news) self post: [https://news.ycombinator.com/item?id=35775071](https://news.ycombinator.com/item?id=35775071) 

[Ciro Santilli](ciro-santilli.md) asked: [https://discord.com/channels/1096393420408360989/1096393420408360996/1137047842159079474](https://discord.com/channels/1096393420408360989/1096393420408360996/1137047842159079474)

> Does the website actually automatically check the formal proofs, or is this intended to be implemented at some point? And if yes, is it intended to allow proofs to depend on other proofs of the website (possibly by other people)

Owner:

> Hi Ciro, yes we will be releasing in-browser proof assistant environments/checkers (e.g. Lean). Our goal is not to replace the underlying open-source repos (e.g. Mathlib) so the main dependency will be on the current repos; then when statement formalizations and proofs come in and are certified they can be PR'd to the respective repos. So we will be the source of truth for the informal latex code but only a stepping stone and orchestration layer on the way to the respective formal libraries.

So apparently there will be proof checking, but no dependencies between proofs, you still have to pull request everything back and face the pain.

Bibliography:
- [https://www.reddit.com/r/mathematics/comments/1cpm5kb/math_genome_project/](https://www.reddit.com/r/mathematics/comments/1cpm5kb/math_genome_project/)
- [https://news.ycombinator.com/item?id=35775071](https://news.ycombinator.com/item?id=35775071) by the creator

### Comparison of proof assistants

↑ **Parent:** [Proof assistant](#proof-assistant)

- [https://ntietz.com/blog/first-impressions-of-lean-and-coq/](https://ntietz.com/blog/first-impressions-of-lean-and-coq/) My first impressions from a few weeks with [Lean](#lean-proof-assistant) and [Coq](#coq-software)

### List of proof assistants

↑ **Parent:** [Proof assistant](#proof-assistant)

#### Lean (proof assistant)

↑ **Parent:** [List of proof assistants](#list-of-proof-assistants)  
🏷️ **Tags:** [Microsoft product](microsoft.md#microsoft-product), [Open source software](software.md#open-source-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lean_(proof_assistant))

[Source code](software.md#source-code):
- [https://github.com/leanprover/lean4](https://github.com/leanprover/lean4) why a separate repo per version... but it is what it is.
- [https://github.com/leanprover/lean](https://github.com/leanprover/lean)

The way [Lean](#lean-proof-assistant) and [Coq](#coq-software) mix programming and mathematics is a thing of great beauty. This is especially notable in lean as you start to play with with things such as:

- `partial`env lean functions, and using `terminates_by` to prove that certain functions terminate. Lean requires explicitly known if functions terminate or not to be able to use them in proofs.
- `noncomputable` functions. Lean allows you to define mathematical functions which you can't actually execute, and it tracks that explicitly

They are huge fans of [Unicode](telecommunication.md#unicode) characters! Check this out from a [formal proof of the prime number theorem](mathematics.md#formal-proof-of-the-prime-number-theorem): [https://github.com/AlexKontorovich/PrimeNumberTheoremAnd/blob/fbdbb5310d036d33b9797b35f3b04b08f2447a6e/PrimeNumberTheoremAnd/ZetaBounds.lean](https://github.com/AlexKontorovich/PrimeNumberTheoremAnd/blob/fbdbb5310d036d33b9797b35f3b04b08f2447a6e/PrimeNumberTheoremAnd/ZetaBounds.lean) Here's map to Ascii: [https://proofassistants.stackexchange.com/questions/954/does-lean-have-a-standard-ascii-representation/5289#5289](https://proofassistants.stackexchange.com/questions/954/does-lean-have-a-standard-ascii-representation/5289#5289)

Their dependency graph thingy is just beautiful however: [https://alexkontorovich.github.io/PrimeNumberTheoremAnd/web/dep_graph_document.html](https://alexkontorovich.github.io/PrimeNumberTheoremAnd/web/dep_graph_document.html)

Their 2025 current installation method is bullshit, recommends [VS Code](software.md#visual-studio-code) extension on Ubuntu. Lol.

From CLI:
```
curl https://elan.lean-lang.org/elan-init.sh -sSf | sh
source $HOME/.elan/env
```
Then when you run:
```
lean
```
it downloads the `lean` executable for you. Insane shit, could only come from a [Microsoft](microsoft.md) mindset.

##### Lean utility

↑ **Parent:** [Lean (proof assistant)](#lean-proof-assistant)

###### elan

↑ **Parent:** [Lean utility](#lean-utility)

[https://github.com/leanprover/elan](https://github.com/leanprover/elan)

###### Lean autoformatter

↑ **Parent:** [Lean utility](#lean-utility)

TODO none? Seriously?

##### Lean vs [Coq](#coq-software)

↑ **Parent:** [Lean (proof assistant)](#lean-proof-assistant)

- [https://proofassistants.stackexchange.com/questions/153/what-are-the-main-differences-between-coq-and-lean](https://proofassistants.stackexchange.com/questions/153/what-are-the-main-differences-between-coq-and-lean)
- [https://news.ycombinator.com/item?id=22171305](https://news.ycombinator.com/item?id=22171305)

##### Lean Zulip

↑ **Parent:** [Lean (proof assistant)](#lean-proof-assistant)

[https://leanprover.zulipchat.com](https://leanprover.zulipchat.com)

##### Lean bibliography

↑ **Parent:** [Lean (proof assistant)](#lean-proof-assistant)

###### How To Prove It with Lean 

↑ **Parent:** [Lean bibliography](#lean-bibliography)

[https://djvelleman.github.io/HTPIwL](https://djvelleman.github.io/HTPIwL)

This tutorial has the merit of actually trying you to do some meaningful mathematics before teaching you a billion items of syntax and dependent type theory nuances.

###### Logic and Proof (Lean book)

↑ **Parent:** [Lean bibliography](#lean-bibliography)

[https://leanprover-community.github.io/logic_and_proof/index.html](https://leanprover-community.github.io/logic_and_proof/index.html)

##### Lean library

↑ **Parent:** [Lean (proof assistant)](#lean-proof-assistant)

###### Lean Mathlib

↑ **Parent:** [Lean library](#lean-library)

###### mathlib4

↑ **Parent:** [Lean Mathlib](#lean-mathlib)

[https://github.com/leanprover-community/mathlib4](https://github.com/leanprover-community/mathlib4)

Here is a specific minimal example of how to use mathlib4: [https://proofassistants.stackexchange.com/questions/2526/how-to-run-lean4-with-mathlib-manually/5299#5299](https://proofassistants.stackexchange.com/questions/2526/how-to-run-lean4-with-mathlib-manually/5299#5299)

###### Formal Conjectures

↑ **Parent:** [Lean library](#lean-library)

[https://github.com/google-deepmind/formal-conjectures](https://github.com/google-deepmind/formal-conjectures)

#### Coq (software)

↑ **Parent:** [List of proof assistants](#list-of-proof-assistants)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Coq_(software))

This used to have the best name ever allowing you to say:

> I love Coq

to English speakers and watch their faces drop.

But in 2023 the bastards renamed it to "[Rocq](#coq-software)", presumably pronounced "rock". Why, God, why.

#### Mathematical Intelligence (Proof assistant)

↑ **Parent:** [List of proof assistants](#list-of-proof-assistants)

[https://github.com/wenitte/mathematical-intelligence](https://github.com/wenitte/mathematical-intelligence)

This will never work but OK. New custom language after [Lean](#lean-proof-assistant).

#### Metamath

↑ **Parent:** [List of proof assistants](#list-of-proof-assistants)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Metamath)

[http://metamath.org/](http://metamath.org/)

It seems to implement [Zermelo-Fraenkel set theory](#zermelo-fraenkel-set-theory).

## Formal proof

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Formal_proof)

A proof in some system for the [formalization of mathematics](formalization-of-mathematics.md).

### Formal proof is useless

↑ **Parent:** [Formal proof](#formal-proof)

The only cases where formal proof of [theorems](#theorem) seem to have had actual mathematical value is for theorems that require checking a very large number of case, so much so that no human can be fully certain that no mistakes were made. Some examples:
- [Four color theorem](https://en.wikipedia.org/wiki/Four_color_theorem)
- [BB(5)](computer-science.md#bb-5)
- [classification of finite simple groups](group.md#classification-of-finite-simple-groups)

### Mathematical proof

↑ **Parent:** [Formal proof](#formal-proof)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mathematical_proof)

### Formal system

↑ **Parent:** [Formal proof](#formal-proof)

#### Set theory

↑ **Parent:** [Formal system](#formal-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Set_theory)

When [Ciro Santilli](ciro-santilli.md) says [set theory](#set-theory), he basically means. [Zermelo-Fraenkel set theory](#zermelo-fraenkel-set-theory).

##### Zermelo-Fraenkel set theory

↑ **Parent:** [Set theory](#set-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Zermelo–Fraenkel_set_theory)

One of the first [formal proof systems](#formal-system). This is actually understandable!

This is [Ciro Santilli](ciro-santilli.md)-2020 definition of the [foundation of mathematics](formalization-of-mathematics.md) (and the only one he had any patience to study at all).

TODO what are its limitations? Why were other systems created?

###### Zermelo-Fraenkel axioms

↑ **Parent:** [Zermelo-Fraenkel set theory](#zermelo-fraenkel-set-theory)

###### Zermelo-Fraenkel axioms with the axiom of choice

↑ **Parent:** [Zermelo-Fraenkel axioms](#zermelo-fraenkel-axioms)

#### Type theory

↑ **Parent:** [Formal system](#formal-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Type_theory)

Alternative to [set theory](#set-theory), and some say it is better for [proof assistants](#proof-assistant), and many of the most popular proof assistants of the 2020s use it e.g. [Lean](#lean-proof-assistant) and [Coq](#coq-software).

<a id="video-why-should-you-learn-type-theory-by-dapper-mink"></a>
**[Video 1](#video-why-should-you-learn-type-theory-by-dapper-mink). Why should you learn Type Theory? by Dapper Mink.** [Source](https://www.youtube.com/watch?v=QRrcwahx-3s). Uses [Lean](#lean-proof-assistant) syntax largely.

### Axiom

↑ **Parent:** [Formal proof](#formal-proof)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Axiom)

#### Consistency

↑ **Parent:** [Axiom](#axiom)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Consistency)

A set of [axioms](#axiom) is consistent if they don't lead to any contradictions.

When a set of axioms is not consistent, false can be proven, and then everything is true, making the set of axioms useless.

#### Independence (mathematical logic)

↑ **Parent:** [Axiom](#axiom)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Independence_(mathematical_logic))

A [theorem](#theorem) is said to be independent from a set of [axioms](#axiom) if it cannot be proven neither true nor false from those axioms.

It or its negation could therefore be arbitrarily added to the set of axioms.

### Open problem in mathematics

↑ **Parent:** [Formal proof](#formal-proof)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/List_of_unsolved_problems_in_mathematics)

#### Conjecture

↑ **Parent:** [Open problem in mathematics](#open-problem-in-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Conjecture)

A [conjecture](#conjecture) is an [open problem in mathematics](#open-problem-in-mathematics) for which some famous dude gave heuristic arguments which indicate if the [theorem](#theorem) is true or false.

##### Famous conjecture

↑ **Parent:** [Conjecture](#conjecture)

This section groups conjectures that are famous, solved or unsolved.

They are usually conjectures that have a strong intuitive reasoning, but took a very long time to prove, despite great efforts.

The list: [https://en.wikipedia.org/wiki/List_of_unsolved_problems_in_mathematics](https://en.wikipedia.org/wiki/List_of_unsolved_problems_in_mathematics)

###### Collatz conjecture

↑ **Parent:** [Famous conjecture](#famous-conjecture)  
🏷️ **Tags:** [Simple to state but hard to prove](mathematics.md#simple-to-state-but-hard-to-prove)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Collatz_conjecture)

Given stuff like [https://arxiv.org/pdf/2107.12475.pdf](https://arxiv.org/pdf/2107.12475.pdf) on [Erdős' conjecture on powers of 2](#erdos-conjecture-on-powers-of-2), it feels like this one will be somewhere close to [computer science](computer-science.md)/[Halting problem](computer-science.md#halting-problem) issues than [number theory](mathematics.md#number-theory). Who knows. This is suggested e.g. at [The Busy Beaver Competition: a historical survey by Pascal Michel](#the-busy-beaver-competition-a-historical-survey-by-pascal-michel).

###### Collatz function

↑ **Parent:** [Collatz conjecture](#collatz-conjecture)

###### Shortcut Collatz function

↑ **Parent:** [Collatz function](#collatz-function)

The [Collatz function](#collatz-function) is not very elegant in that the odd $3n + 1$ case is always even because $n$ is odd, so it is always predictably followed by a division by two. This is not the case for the even case, where the result can be either even or odd.

A much more elegant formulation is to immediately also divide by two when the number is odd:

$$
\frac{3n + 1}{2}
$$

###### Collatz conjecture failure mode

↑ **Parent:** [Collatz conjecture](#collatz-conjecture)

There are to ways in which the [Collatz conjecture](#collatz-conjecture) can fail:
- [Collatz cycle](#collatz-cycle): there is a cycle that loops forever and never reaches 1
- [Unbounded Collatz trajectory](#unbounded-collatz-trajectory): there is a sequence that grows without bound without looping
These are the only two options because if any sequence has an upper bound, it must sooner or later repeat an element, leading to a cycle.

###### Collatz cycle

↑ **Parent:** [Collatz conjecture failure mode](#collatz-conjecture-failure-mode)

###### Collatz n-cycle

↑ **Parent:** [Collatz cycle](#collatz-cycle)

###### Collatz 1-cycle

↑ **Parent:** [Collatz n-cycle](#collatz-n-cycle)

###### Collatz cycle length lower bound

↑ **Parent:** [Collatz n-cycle](#collatz-n-cycle)

- [https://www.sciencedirect.com/science/article/pii/0012365X9390052U?via%3Dihub](https://www.sciencedirect.com/science/article/pii/0012365X9390052U?via%3Dihub)

###### Unbounded Collatz trajectory

↑ **Parent:** [Collatz conjecture failure mode](#collatz-conjecture-failure-mode)

###### Collatz-like problem

↑ **Parent:** [Collatz conjecture](#collatz-conjecture)

We ust use the if mod notation definition as mentioned at: [https://math.stackexchange.com/questions/4305972/what-exactly-is-a-collatz-like-problem/4773230#4773230](https://math.stackexchange.com/questions/4305972/what-exactly-is-a-collatz-like-problem/4773230#4773230)

###### The Busy Beaver Competition: a historical survey by Pascal Michel

↑ **Parent:** [Collatz conjecture](#collatz-conjecture)

[https://arxiv.org/abs/0906.3749](https://arxiv.org/abs/0906.3749)

<h6 id="erdos-conjecture-on-powers-of-2">Erdős' conjecture on powers of 2</h6>

↑ **Parent:** [Collatz conjecture](#collatz-conjecture)  
🏷️ **Tags:** [Conjecture by Erdős](mathematics.md#conjecture-by-erdos)

Described at: [https://arxiv.org/pdf/2107.12475.pdf](https://arxiv.org/pdf/2107.12475.pdf) where a relation to the [Busy beaver scale](computer-science.md#busy-beaver-scale) is proven, and the intuitive relation to the [Collatz conjecture](#collatz-conjecture) described. Perhaps more directly: [https://demonstrations.wolfram.com/CollatzSequenceComputedByATuringMachine/](https://demonstrations.wolfram.com/CollatzSequenceComputedByATuringMachine/)

### Theorem

↑ **Parent:** [Formal proof](#formal-proof)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Theorem)

#### Corollary

↑ **Parent:** [Theorem](#theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Corollary)

An easy to prove [theorem](#theorem) that follows from a harder to prove theorem.

## Lemma (mathematics)

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)

A [theorem](#theorem) that is not very important on its own, often an intermediate step to proving something that the author feels deserves the name "[theorem](#theorem)".

## Set (mathematics)

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)

Intuitively: unordered container where all the values are unique, just like C++ `std::set`.

More precisely for set theory [formalization of mathematics](formalization-of-mathematics.md):
- everything is a set, including the elements of sets
- string manipulation wise:
  - `{}` is an empty set. The natural number `0` is defined as `{}` as well.
  - `{{}}` is a set that contains an empty set
  - `{{}, {{}}}` is a set that contains two sets: `{}` and `{{}}`
  - `{{}, {}}` is not well formed, because it contains `{}` twice

### Union (set theory)

↑ **Parent:** [Set (mathematics)](#set-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Union_(set_theory))

### Cardinality

↑ **Parent:** [Set (mathematics)](#set-mathematics)

The size of a set.

For [finite](calculus.md#infinity) sizes, the definition is simple, and the intuitive name "size" matches well.

But for infinity, things are messier, e.g. the size of the [real numbers](#real-number) is strictly larger than the size of the [integers](#integer) as shown by [Cantor's diagonal argument](#cantor-s-diagonal-argument), which is kind of what justifies a fancier word "cardinality" to distinguish it from the more normal word "size".

The key idea is to compare set sizes with [bijections](#bijection).

## Function (mathematics)

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Function_(mathematics))

[Set](#set-mathematics) of [ordered pairs](#ordered-pair). That's it! This is illustrated at: [https://math.stackexchange.com/questions/1480651/is-fx-x-1-x-2-a-function/1481099#1481099](https://math.stackexchange.com/questions/1480651/is-fx-x-1-x-2-a-function/1481099#1481099)

### Domain, codomain and image

↑ **Parent:** [Function (mathematics)](#function-mathematics)

#### Bijection

↑ **Parent:** [Domain, codomain and image](#domain-codomain-and-image)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bijection)

##### Injective function

↑ **Parent:** [Bijection](#bijection)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Injective_function)

Mnemonic: in means into. So we are going into a [codomain](#codomain) that is large enough so that we can have a different image for every input.

##### Surjective function

↑ **Parent:** [Bijection](#bijection)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Surjective_function)

Mnemonic: sur means over. So we are going over the [codomain](#codomain), and covering it entirely.

#### Domain of a function

↑ **Parent:** [Domain, codomain and image](#domain-codomain-and-image)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Domain_of_a_function)

#### Codomain

↑ **Parent:** [Domain, codomain and image](#domain-codomain-and-image)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Codomain)

Vs: [image](#image-mathematics): the codomain is the set that the function might reach.

The [image](#image-mathematics) is the exact set that it actually reaches.

E.g. the function:

$$
f(x) = x^2
$$

could have:
- codomain $\R$
- image $\R_{+}$

Note that the definition of the codomain is somewhat arbitrary, e.g. $x^2$ could as well technically have codomain:

$$
\R \bigcup \R^2
$$

even though it will obviously never reach any value in $\R^2$.

The exact image is in general therefore harder to characterize.

##### Endofunction

↑ **Parent:** [Codomain](#codomain)

A [function](#function-mathematics) where the [domain](#domain-of-a-function) is the same as the [codomain](#codomain).

#### Image (mathematics)

↑ **Parent:** [Domain, codomain and image](#domain-codomain-and-image)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Image_(mathematics))

### Periodic function

↑ **Parent:** [Function (mathematics)](#function-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Periodic_function)

#### Square wave

↑ **Parent:** [Periodic function](#periodic-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Square_wave)

##### Rectangular wave

↑ **Parent:** [Square wave](#square-wave)

### Function by signature

↑ **Parent:** [Function (mathematics)](#function-mathematics)

In this section we classify some functions by the type of inputs and outputs they take and produce.

#### Functional function

↑ **Parent:** [Function by signature](#function-by-signature)

This is about functions that take functions as input or output.

##### Convolution

↑ **Parent:** [Functional function](#functional-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Convolution)

#### Set function

↑ **Parent:** [Function by signature](#function-by-signature)

This section is about functions that operates on arbitrary [sets](#set-mathematics).

##### Cartesian product

↑ **Parent:** [Set function](#set-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cartesian_product)

A function that maps two [sets](#set-mathematics) to a third set.

##### Direct product

↑ **Parent:** [Set function](#set-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Direct_product)

A [Cartesian product](#cartesian-product) that carries over some extra structure of the input groups.

E.g. the [direct product of groups](group.md#direct-product-of-groups) carries over [group](group.md) structure on both sides.

#### Numeric function

↑ **Parent:** [Function by signature](#function-by-signature)

This section is about functions that operate on numbers such as the [integers](#integer) or [real numbers](#real-number).

##### Addition

↑ **Parent:** [Numeric function](#numeric-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Addition)

##### Subtraction

↑ **Parent:** [Numeric function](#numeric-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Subtraction)

##### Multiplication

↑ **Parent:** [Numeric function](#numeric-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Multiplication)

##### Division

↑ **Parent:** [Numeric function](#numeric-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Division)

##### Exponentiation

↑ **Parent:** [Numeric function](#numeric-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Exponentiation)

###### Exponentiation grows really fast

↑ **Parent:** [Exponentiation](#exponentiation)

It is quite [the beauty of mathematics](mathematics.md#the-beauty-of-mathematics) beautiful that with exponentiation, even if you take relatively small numbers of the order of 100 then:

$$
2^{265}
$$

is already equal to the number of atoms in the universe.

###### Wheat and chessboard problem

↑ **Parent:** [Exponentiation grows really fast](#exponentiation-grows-really-fast)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Wheat_and_chessboard_problem)

![](https://upload.wikimedia.org/wikipedia/commons/c/cd/Wheat_and_chessboard_problem.jpg)

**[Figure 2](#_166)** [Source](https://commons.wikimedia.org/wiki/File:Wheat_and_chessboard_problem.jpg).

###### nth root

↑ **Parent:** [Exponentiation](#exponentiation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/nth_root)

###### Square root

↑ **Parent:** [Nth root](#nth-root)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Square_root)

###### Exponentiation functional equation

↑ **Parent:** [Exponentiation](#exponentiation)  
🏷️ **Tags:** [Functional equation](mathematics.md#functional-equation)

We define this as the [functional equation](mathematics.md#functional-equation):

$$
f(x, y) = f(x)f(y)
$$

It is a bit like [cauchy's functional equation](mathematics.md#cauchy-s-functional-equation) but with [multiplication](#multiplication) instead of [addition](#addition).

###### Exponential function

↑ **Parent:** [Exponentiation](#exponentiation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Exponential_function)

###### Exponential function differential equation

↑ **Parent:** [Exponential function](#exponential-function)

The [differential equation](calculus.md#differential-equation) that is solved by the [exponential function](#exponential-function):

$$
y'(x) = y(x)
$$

with [initial condition](calculus.md#initial-condition):

$$
y(0) = 1
$$

TODO find better name for it, "[linear](calculus.md#linear-differential-equation) homogenous differential equation of degree one" almost fully constrainst it except for the exponent constant and initial value.

###### Definition of the exponential function

↑ **Parent:** [Exponential function](#exponential-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Characterizations_of_the_exponential_function)

###### Taylor expansion definition of the exponential function

↑ **Parent:** [Definition of the exponential function](#definition-of-the-exponential-function)

The [Taylor series](calculus.md#taylor-series) expansion is the most direct definition of the expontial as it obviously satisfies the [exponential function differential equation](#exponential-function-differential-equation):
- the first constant term dies
- each other term gets converted to the one before
- because we have [infinite](calculus.md#infinity) many terms, we get what we started with!


$$
e^x = \sum_{n=0}^\infty \frac{x^n}{n!} = 1 + \frac{x}{1} + \frac{x^2}{2} + \frac{x^3}{2 \times 3} + \frac{x^4}{2 \times 3 \times 4} + \ldots
$$

###### Product definition of the exponential function

↑ **Parent:** [Definition of the exponential function](#definition-of-the-exponential-function)

$$
e^x = \lim_{n\to\infty} \left(1+\frac x n \right)^n
$$

The basic intuition for this is to start from the origin and make small changes to the function based on its known derivative at the origin.

More precisely, we know that for any base b, [exponentiation](#exponentiation) satisfies:
- $b^{x + y} = b^x b^y$.
- $b^{0} = 1$.
And we also know that for $b = e$ in particular that we satisfy the [exponential function differential equation](#exponential-function-differential-equation) and so:

$$
\dv{e^x}{x}(0) = 1
$$

One interesting fact is that the only thing we use from the [exponential function differential equation](#exponential-function-differential-equation) is the value around $x = 0$, which is quite little information! This idea is basically what is behind the importance of the ralationship between [Lie group-Lie algebra correspondence](geometry.md#lie-group-lie-algebra-correspondence) via the [exponential map](geometry.md#exponential-map). In the more general settings of groups and [manifolds](calculus.md#manifold), restricting ourselves to be near the origin is a huge advantage.

Now suppose that we want to calculate $e^1$. The idea is to start from $e^0$ and then then to use the first order of the [Taylor series](calculus.md#taylor-series) to extend the known value of $e^0$ to $e^1$.

E.g., if we split into 2 parts, we know that:

$$
e^1 = e^{1/2}e^{1/2}
$$

or in three parts:

$$
e^1 = e^{1/3}e^{1/3}e^{1/3}
$$

so we can just use arbitrarily many parts $e^{1/n}$ that are arbitrarily close to $x = 0$:

$$
e^1 = (e^{1/n})^n
$$

and more generally for any $x$ we have:

$$
e^x = (e^{x/n})^n
$$

Let's see what happens with the Taylor series. We have near $y = 0$ in [little-o notation](computer-science.md#little-o-notation):

$$
e^y = 1 + y + o(y)
$$

Therefore, for $y = x/n$, which is near $y = 0$ for any fixed $x$:

$$
e^{x/n} = 1 + x/n + o(1/n)
$$

and therefore:

$$
e^x = (e^{x/n})^n = (1 + x/n + o(1/n))^n
$$

which is basically the formula tha we wanted. We just have to convince ourselves that at $\lim_{n \to \infty}$, the $o(1/n)$ disappears, i.e.:

$$
(1 + x/n + o(1/n))^n = (1 + x/n)^n
$$

To do that, let's multiply $e^y$ by itself once:

$$
e^y e^y = (1 + y + o(y))(1 + y + o(y)) = 1 + 2y + o(y)
$$

and multiplying a third time:

$$
e^y e^y e^y = (1 + 2y + o(y))(1 + y + o(y)) = 1 + 3y + o(y)
$$

TODO conclude.

###### Gaussian function

↑ **Parent:** [Exponential function](#exponential-function)

###### Logarithm

↑ **Parent:** [Exponential function](#exponential-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Logarithm)

###### Matrix exponential

↑ **Parent:** [Exponential function](#exponential-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Matrix_exponential)

Is the solution to a [system of linear ordinary differential equations](calculus.md#system-of-linear-ordinary-differential-equations), the [exponential function](#exponential-function) is just a 1-dimensional subcase.

Note that more generally, the [matrix exponential](#matrix-exponential) can be defined on any [ring](group.md#ring-mathematics).

The matrix exponential is of particular interest in the study of [Lie groups](geometry.md#lie-group), because in the case of the [Lie algebra of a matrix Lie group](geometry.md#lie-algebra-of-a-matrix-lie-group), it provides the correct [exponential map](geometry.md#exponential-map).

<a id="video-how-and-why-to-raise-e-to-the-power-of-a-matrix-by-3blue1brown-2021"></a>
**[Video 2](#video-how-and-why-to-raise-e-to-the-power-of-a-matrix-by-3blue1brown-2021). How (and why) to raise e to the power of a matrix by 3Blue1Brown (2021)** [Source](https://www.youtube.com/watch?v=O85OWBJ2ayo).

###### Logarithm of a matrix

↑ **Parent:** [Matrix exponential](#matrix-exponential)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Logarithm_of_a_matrix)

###### Existence of the matrix logarithm

↑ **Parent:** [Logarithm of a matrix](#logarithm-of-a-matrix)

[https://en.wikipedia.org/wiki/Logarithm_of_a_matrix#Existence](https://en.wikipedia.org/wiki/Logarithm_of_a_matrix#Existence) mentions it always exists for all [invertible](algebra.md#invertible) [complex](#complex-number) matrices. But the [real](#real-number) condition is more complicated. Notable counter example: -1 cannot be reached by any real $e^{tk}$.

The [Lie algebra exponential covering problem](geometry.md#lie-algebra-exponential-covering-problem) can be seen as a generalized version of this problem, because
- [Lie algebra](geometry.md#lie-algebra) of [$GL(n)$](geometry.md#general-linear-group) is just the entire [$M_n$](linear-algebra.md#matrix-ring)
- we can immediately exclude non-invertible matrices from being the result of the exponential, because $e^{tM}$ has inverse $e^{-tM}$, so we already know that non-invertible matrices are not reachable

##### Polynomial

↑ **Parent:** [Numeric function](#numeric-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polynomial)

###### Degree of a polynomial

↑ **Parent:** [Polynomial](#polynomial)

###### Algebraic equation

↑ **Parent:** [Polynomial](#polynomial)  
🏷️ **Tags:** [Functional equation](mathematics.md#functional-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algebraic_equation)

###### Named algebraic equation

↑ **Parent:** [Algebraic equation](#algebraic-equation)

###### Quadratic equation

↑ **Parent:** [Named algebraic equation](#named-algebraic-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quadratic_equation)

###### Quadratic equation modulo n

↑ **Parent:** [Quadratic equation](#quadratic-equation)

- [https://math.stackexchange.com/questions/229218/modulo-version-of-the-quadratic-formula-and-eulers-criterion](https://math.stackexchange.com/questions/229218/modulo-version-of-the-quadratic-formula-and-eulers-criterion)

###### Quadratic formula

↑ **Parent:** [Quadratic equation](#quadratic-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quadratic_formula)

###### Cubic equation

↑ **Parent:** [Named algebraic equation](#named-algebraic-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cubic_equation)

###### Quartic equation

↑ **Parent:** [Named algebraic equation](#named-algebraic-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quartic_equation)

###### Quintic equation

↑ **Parent:** [Named algebraic equation](#named-algebraic-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quintic_equation)

###### Abel-Ruffini theorem

↑ **Parent:** [Quintic equation](#quintic-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Abel-Ruffini_theorem)

<a id="video-but-why-is-there-no-quintic-formula-by-mathkiwi"></a>
**[Video 3](#video-but-why-is-there-no-quintic-formula-by-mathkiwi). But why is there no quintic formula? by MathKiwi.** [Source](https://www.youtube.com/watch?v=1EWUsef0iFs). 10 minutes, that's about the right length, well done.

###### Algebraic equation over a field

↑ **Parent:** [Algebraic equation](#algebraic-equation)

In this section we collect results about [algebraic equations](#algebraic-equation) over more "exotic" [fields](group.md#field-mathematics)

###### Algebraic equation modulo n

↑ **Parent:** [Algebraic equation](#algebraic-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algebraic_equation_modulo_n)

###### Algebraic number

↑ **Parent:** [Algebraic equation](#algebraic-equation)  
🏷️ **Tags:** [Number](#number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algebraic_number)

###### Algebraic number field

↑ **Parent:** [Algebraic number](#algebraic-number)  
🏷️ **Tags:** [Quadratically closed field](group.md#quadratically-closed-field)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/en.wikipedia.org/w/index.php?title=Algebraic_number&oldid=1168427661#Field)

The set of all [algebraic numbers](#algebraic-number) forms a [field](group.md#field-mathematics).

This field contains all of the [rational numbers](#rational-number), but it is a [quadratically closed field](group.md#quadratically-closed-field).

Like the [rationals](#rational-number), this field also has the same [cardinality](#cardinality) as the [natural numbers](#natural-number), because we can specify and enumerate each of its members by a fixed number of integers from the [polynomial equation](#algebraic-equation) that defines them. So it is a bit like the [rationals](#rational-number), but we use potentially arbitrary numbers of integers to specify each number (polynomial coefficients + index of which root we are talking about) instead of just always two as for the rationals.

Each [algebraic number](#algebraic-number) also has a degree associated to it, i.e. the [degree of the polynomial](#degree-of-a-polynomial) used to define it.

###### Algebraic function

↑ **Parent:** [Algebraic number](#algebraic-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Algebraic_function)

TODO understand.

###### Transcendental number

↑ **Parent:** [Algebraic number](#algebraic-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transcendental_number)

Sometimes [mathematicians](mathematics.md#mathematician) go a little overboard with their naming.

Bibliography:
- [https://www.quantamagazine.org/recounting-the-history-of-maths-transcendental-numbers-20230627/](https://www.quantamagazine.org/recounting-the-history-of-maths-transcendental-numbers-20230627/)

###### Transcendental number conjecture

↑ **Parent:** [Transcendental number](#transcendental-number)  
🏷️ **Tags:** [Simple to state but hard to prove](mathematics.md#simple-to-state-but-hard-to-prove)

[https://en.wikipedia.org/wiki/Transcendental_number#Conjectured_transcendental_numbers](https://en.wikipedia.org/wiki/Transcendental_number#Conjectured_transcendental_numbers)

There's a billion simple looking expressions which are not known to be transcendental numbers or not. It's cute [simple to state but hard to prove](mathematics.md#simple-to-state-but-hard-to-prove) at its best.

Open as of 2020:
- $e + \pi$

Bibliography:
- [https://www.quantamagazine.org/recounting-the-history-of-maths-transcendental-numbers-20230627/](https://www.quantamagazine.org/recounting-the-history-of-maths-transcendental-numbers-20230627/) How Math Achieved Transcendence by David S. Richeson (2023).

<a id="video-why-pi-pi-pi-pi-could-be-an-integer-by-stand-up-maths-2021"></a>
**[Video 4](#video-why-pi-pi-pi-pi-could-be-an-integer-by-stand-up-maths-2021). Why π^π^π^π could be an integer by Stand-up Maths (2021)** [Source](https://www.youtube.com/watch?v=BdHFLfv-ThQ). Sponsored by Jane Street. [Shame](economy.md#finance-is-a-cancer-of-society).

###### Diophantine equation

↑ **Parent:** [Polynomial](#polynomial)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Diophantine_equation)

[Polynomial](#polynomial) (possibly a [multivariate polynomial](#multivariate-polynomial)) with [integer](#integer) coefficients.

Sometimes systems of [Diophantine equations](#diophantine-equation) are considered.

Problems generally involve finding integer solutions to the equations, notably determining if any solution exists, and if infinitely solutions exist.

The general problem is known to be [undecidable](computer-science.md#undecidable-problem): [Hilbert's tenth problem](#hilbert-s-tenth-problem).

The [Pythagorean triples](#pythagorean-triple), and its generalization [Fermat's last theorem](#fermat-s-last-theorem), are the quintessential examples.

###### Pythagorean triple

↑ **Parent:** [Diophantine equation](#diophantine-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pythagorean_triple)

![](https://web.archive.org/web/20220528162407im_/https://upload.wikimedia.org/wikipedia/commons/4/4c/Pythagorean_theorem_-_Ani.gif)

**[Figure 3](#_246)** [Source](https://en.wikipedia.org/wiki/File:Pythagorean\_theorem\_-\_Ani.gif).

<h6 id="euclid-s-formula">Euclid's formula</h6>

↑ **Parent:** [Pythagorean triple](#pythagorean-triple)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pythagorean_triple#Generating_a_triple)

###### There are infinitely many Pythagorean triples

↑ **Parent:** [Euclid's formula](#euclid-s-formula)

Direct consequence of [Euclid's formula](#euclid-s-formula).

<h6 id="euclid-s-formula-generates-all-pythagorean-triples">Euclid's formula generates all Pythagorean triples</h6>

↑ **Parent:** [Euclid's formula](#euclid-s-formula)

###### Classification of Pythagorean triples

↑ **Parent:** [Pythagorean triple](#pythagorean-triple)  
🏷️ **Tags:** [Classification (mathematics)](mathematics.md#classification-mathematics)

[https://en.wikipedia.org/wiki/Pythagorean_triple#Generating_a_triple](https://en.wikipedia.org/wiki/Pythagorean_triple#Generating_a_triple)

###### Taxicab number

↑ **Parent:** [Pythagorean triple](#pythagorean-triple)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Taxicab_number)

<h6 id="fermat-s-last-theorem">Fermat's last theorem</h6>

↑ **Parent:** [Pythagorean triple](#pythagorean-triple)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fermat's_last_theorem)

A generalization of the [Pythagorean triple](#pythagorean-triple) infinity question.

<h6 id="formalization-of-fermat-s-last-theorem">Formalization of Fermat's last theorem</h6>

↑ **Parent:** [Fermat's last theorem](#fermat-s-last-theorem)  
🏷️ **Tags:** [Formalization of X](#formalization-of-x)

[https://github.com/ImperialCollegeLondon/FLT](https://github.com/ImperialCollegeLondon/FLT)

###### Andrew Wiles

↑ **Parent:** [Fermat's last theorem](#fermat-s-last-theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Andrew_Wiles)

<a id="video-beauty-is-suffering"></a>
**[Video 5](#video-beauty-is-suffering). Beauty Is Suffering.** [Source](https://www.youtube.com/watch?v=i0UTeQfnzfM).

<h6 id="hilbert-s-tenth-problem">Hilbert's tenth problem</h6>

↑ **Parent:** [Diophantine equation](#diophantine-equation)  
🏷️ **Tags:** [Hilbert's problems](mathematics.md#hilbert-s-problems), [Undecidable problem](computer-science.md#undecidable-problem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hilbert's_tenth_problem)

Once you hear about the [uncomputability](computer-science.md#computable-problem) of such problems, it makes you see that all [Diophantine equation](#diophantine-equation) questions risk being [undecidable](computer-science.md#undecidable-problem), though in some simpler cases we manage to come up with answers. The feeling is similar to watching people trying to solve the [Halting problem](computer-science.md#halting-problem), e.g. in the effort to determine [BB(5)](computer-science.md#bb-5).

<h6 id="hilbert-s-tenth-problem-variant">Hilbert's tenth problem variant</h6>

↑ **Parent:** [Hilbert's tenth problem](#hilbert-s-tenth-problem)

[https://mathoverflow.net/questions/51987/which-types-of-diophantine-equations-are-solvable](https://mathoverflow.net/questions/51987/which-types-of-diophantine-equations-are-solvable)

<h6 id="decidability-of-hilbert-s-tenth-problem-in-modular-arithmetic">Decidability of Hilbert's tenth problem in modular arithmetic</h6>

↑ **Parent:** [Hilbert's tenth problem variant](#hilbert-s-tenth-problem-variant)

[https://www.jstor.org/stable/1970438](https://www.jstor.org/stable/1970438) says for [prime](mathematics.md#prime-number) modulo there is an algorithm.

Question for non-prime modulo: [https://math.stackexchange.com/questions/4944623/are-diophantine-equations-decidable-in-modular-arithmetic](https://math.stackexchange.com/questions/4944623/are-diophantine-equations-decidable-in-modular-arithmetic)

<h6 id="decidability-of-hilbert-s-tenth-problem-of-a-given-degree-and-number-of-variables">Decidability of Hilbert's tenth problem of a given degree and number of variables</h6>

↑ **Parent:** [Hilbert's tenth problem variant](#hilbert-s-tenth-problem-variant)

- [https://mathoverflow.net/questions/207482/algorithmic-un-solvability-of-diophantine-equations-of-given-degree-with-given](https://mathoverflow.net/questions/207482/algorithmic-un-solvability-of-diophantine-equations-of-given-degree-with-given)
- [https://mathoverflow.net/questions/51987/which-types-of-diophantine-equations-are-solvable](https://mathoverflow.net/questions/51987/which-types-of-diophantine-equations-are-solvable)

###### Quadratic Diophantine equation

↑ **Parent:** [Decidability of Hilbert's tenth problem of a given degree and number of variables](#decidability-of-hilbert-s-tenth-problem-of-a-given-degree-and-number-of-variables)

<h6 id="hilbert-s-tenth-problem-is-decidable-for-quadratic-equations">Hilbert's tenth problem is decidable for quadratic equations</h6>

↑ **Parent:** [Decidability of Hilbert's tenth problem of a given degree and number of variables](#decidability-of-hilbert-s-tenth-problem-of-a-given-degree-and-number-of-variables)  
🏷️ **Tags:** [Quadratic Diophantine equation](#quadratic-diophantine-equation)

TODO is it or is not:
- [https://mathoverflow.net/questions/207482/algorithmic-un-solvability-of-diophantine-equations-of-given-degree-with-given](https://mathoverflow.net/questions/207482/algorithmic-un-solvability-of-diophantine-equations-of-given-degree-with-given)
- [https://math.stackexchange.com/questions/181380/second-degree-diophantine-equations](https://math.stackexchange.com/questions/181380/second-degree-diophantine-equations)
- [https://mathoverflow.net/questions/142938/is-there-an-algorithm-to-solve-quadratic-diophantine-equations](https://mathoverflow.net/questions/142938/is-there-an-algorithm-to-solve-quadratic-diophantine-equations)
- [https://math.stackexchange.com/questions/798609/is-there-any-solution-to-this-quadratic-diophantine-equation](https://math.stackexchange.com/questions/798609/is-there-any-solution-to-this-quadratic-diophantine-equation)

###### Undecidable Diophantine equation example

↑ **Parent:** [Decidability of Hilbert's tenth problem of a given degree and number of variables](#decidability-of-hilbert-s-tenth-problem-of-a-given-degree-and-number-of-variables)  
🏷️ **Tags:** [Undecidable problem](computer-science.md#undecidable-problem)

[https://mathoverflow.net/questions/11540/what-are-the-most-attractive-turing-undecidable-problems-in-mathematics/103415#103415](https://mathoverflow.net/questions/11540/what-are-the-most-attractive-turing-undecidable-problems-in-mathematics/103415#103415) provides a specific single undecidable [Diophantine equation](#diophantine-equation).

<h6 id="hilbert-s-tenth-problem-over-other-rings">Hilbert's tenth problem over other rings</h6>

↑ **Parent:** [Hilbert's tenth problem variant](#hilbert-s-tenth-problem-variant)

[https://mathoverflow.net/questions/11540/what-are-the-most-attractive-turing-undecidable-problems-in-mathematics/11557#11557](https://mathoverflow.net/questions/11540/what-are-the-most-attractive-turing-undecidable-problems-in-mathematics/11557#11557) contains a good overview of the decidability status of variants over [rings](group.md#ring-mathematics) other than the [integers](#integer).

###### Additive number theory

↑ **Parent:** [Diophantine equation](#diophantine-equation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Additive_number_theory)

###### Additive basis

↑ **Parent:** [Additive number theory](#additive-number-theory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Additive_basis)

###### Additive basis theorem

↑ **Parent:** [Additive basis](#additive-basis)

<h6 id="waring-s-problem">Waring's problem</h6>

↑ **Parent:** [Additive basis theorem](#additive-basis-theorem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Waring's_problem)

And when it can't, attempt to classify which subset of the [integers](#integer) can be reached. E.g. [Legendre's three-square theorem](#legendre-s-three-square-theorem).

<h6 id="waring-s-problem-for-squares">Waring's problem for squares</h6>

↑ **Parent:** [Waring's problem](#waring-s-problem)

4 squares are sufficient by [Lagrange's four-square theorem](#lagrange-s-four-square-theorem).

3 is not enough by [Legendre's three-square theorem](#legendre-s-three-square-theorem).

The subsets reachable with 2 and 3 squares are fully characterized by [Legendre's three-square theorem](#legendre-s-three-square-theorem).

<h6 id="lagrange-s-four-square-theorem">Lagrange's four-square theorem</h6>

↑ **Parent:** [Waring's problem for squares](#waring-s-problem-for-squares)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lagrange's_four-square_theorem)

<h6 id="legendre-s-three-square-theorem">Legendre's three-square theorem</h6>

↑ **Parent:** [Waring's problem for squares](#waring-s-problem-for-squares)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Legendre's_three-square_theorem)

###### Sum of two squares theorem

↑ **Parent:** [Waring's problem for squares](#waring-s-problem-for-squares)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sum_of_two_squares_theorem)

###### Waring problem variant

↑ **Parent:** [Waring's problem](#waring-s-problem)

###### Waring problem with negative numbers allowed

↑ **Parent:** [Waring problem variant](#waring-problem-variant)

###### Sum of three cubes

↑ **Parent:** [Waring problem with negative numbers allowed](#waring-problem-with-negative-numbers-allowed)  
🏷️ **Tags:** [Open problem in mathematics](#open-problem-in-mathematics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sum_of_three_cubes)

Compared to [Waring's problem](#waring-s-problem), this is potentially much harder, as we can go infinitely negative in our attempts, there isn't a bound on how many tries we can have for each number.

In other words, it is unlikely to have a [Conjecture reduction to a halting problem](computer-science.md#conjecture-reduction-to-a-halting-problem).

<a id="video-3-as-the-sum-of-the-3-cubes-by-numberphile-2019"></a>
**[Video 6](#video-3-as-the-sum-of-the-3-cubes-by-numberphile-2019). 3 as the sum of the 3 cubes by Numberphile (2019)** [Source](https://www.youtube.com/watch?v=GXhzZAem7k0).

###### Waring-Goldbach problem

↑ **Parent:** [Waring problem variant](#waring-problem-variant)  
🏷️ **Tags:** [Goldbach's conjecture](mathematics.md#goldbach-s-conjecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Waring-Goldbach_problem)

It is exactly what you'd expect from the name, Waring was [watching Netflix](computer.md#netflix-and-chill) with Goldbach, when they suddenly came up with this.

###### Named small order polynomial

↑ **Parent:** [Polynomial](#polynomial)

###### Linear polynomial

↑ **Parent:** [Named small order polynomial](#named-small-order-polynomial)

A [polynomial](#polynomial) of degree 1, i.e. of form $ax + b$.

###### Galois theory

↑ **Parent:** [Polynomial](#polynomial)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Galois_theory)

###### Irreducible polynomial

↑ **Parent:** [Polynomial](#polynomial)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Irreducible_polynomial)

###### Multivariate polynomial

↑ **Parent:** [Polynomial](#polynomial)

A [polynomial](#polynomial) with multiple input arguments, e.g. with two inputs $x$ and $y$:

$$
f(x, y) = x^2 + 2x + y^3 + 1
$$

as opposed to a [polynomial](#polynomial) with a single argument e.g. one with just $x$:

$$
f(x) = x^2 + 2x + 1
$$

###### Domain of a polynomial

↑ **Parent:** [Polynomial](#polynomial)

###### Polynomial over a field

↑ **Parent:** [Domain of a polynomial](#domain-of-a-polynomial)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polynomial_over_a_field)

By default, we think of polynomials over the [real numbers](#real-number) or [complex numbers](#complex-number).

However, a polynomial can be defined over any other field just as well, the most notable example being that of a polynomial over a [finite field](group.md#finite-field).

For example, given the finite field of [order](algebra.md#order-algebra) 9, $GP(3)$ and with elements $\{0, 1, 2\}$, we can denote polynomials over that ring as

$$
GP(3)[x]
$$

where $x$ is the variable name.

For example, one such polynomial could be:

$$
P(x) = 2x^4 + x^2 + 2
$$

and another one:

$$
Q(X) = x^3 + 2x^2 + 2
$$

Note how all the coefficients are members of the finite field we chose.

Given this, we could evaluate the polynomial for any element of the field, e.g.:

$$
P(0) = 2 (0 \times 0 \times 0 \times 0) + (0 \times 0) + 2 = 2
P(1) = 2 (1 \times 1 \times 1 \times 1) + (1 \times 1) + 2 = 2 (1) + 1 + 2 = 2
P(2) = 2 (2 \times 2 \times 2 \times 2) + (2 \times 2) + 2 = 2 (16 % 3) + (4 % 3) + 2 = 2 + 1 + 2 = 2
$$

and so on.

We can also add polynomials as usual over the field:

$$
P(x) + Q(x) = 2x^4 + x^3 + (1+2)x^2 + (2 + 2) = 2x^4 + x^3 + (0)x^2 + 1 = 2x^4 + x^3 + 1
$$

and multiplication works analogously.

###### Polynomial over a ring

↑ **Parent:** [Domain of a polynomial](#domain-of-a-polynomial)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polynomial_over_a_ring)

The usual definition of a [polynomial](#polynomial) is over a [field](group.md#field-mathematics) as shown at [polynomial over a field](#polynomial-over-a-field).

However, there is nothing in the immediate definition that prevents us from having a [ring](group.md#ring-mathematics) instead, i.e. a [field](group.md#field-mathematics) but without the [commutative property](group.md#commutative-property) and [inverse elements](algebra.md#inverse-element).

The only thing is that then we would need to differentiate between different orderings of the terms of [multivariate polynomial](#multivariate-polynomial), e.g. the following would all be potentially different terms:

$$
2xxy + 2xyx + 2yxx +
x2xy + x2yx + y2xx +
xx2y + xy2x + yx2x +
xxy2 + xyx2 + yxx2
$$

while for a field they would all go into a single term:

$$
12x^2y
$$

so when considering a polynomial over a [ring](group.md#ring-mathematics) we end up with a lot more more possible terms.

If the [ring](group.md#ring-mathematics) is a [commutative ring](group.md#commutative-ring) however, polynomials do look like proper polynomials: [Section "Polynomial over a commutative ring"](#polynomial-over-a-commutative-ring).

###### Polynomial over a commutative ring

↑ **Parent:** [Domain of a polynomial](#domain-of-a-polynomial)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polynomial_over_a_commutative_ring)

Unlike [over non-commutative rings](#polynomial-over-a-ring), polynomials do look like proper [polynomials](#polynomial) over [commutative ring](group.md#commutative-ring).

In particular, [Hilbert's tenth problem](#hilbert-s-tenth-problem) is about [polynomials](#polynomial) over the [integers](#integer), which is a [commutative ring](group.md#commutative-ring), and therefore brings mindshare to this definition.

###### Polynomial ring

↑ **Parent:** [Polynomial](#polynomial)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polynomial_ring)

The polynomials together with polynomial addition and multiplication form a [commutative](group.md#commutative-property) [ring](group.md#ring-mathematics).

##### Step function

↑ **Parent:** [Numeric function](#numeric-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Step_function)

###### Heavyside step function

↑ **Parent:** [Step function](#step-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Heavyside_step_function)

##### Integer sequence

↑ **Parent:** [Numeric function](#numeric-function)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Integer_sequence)

###### Fibonacci sequence

↑ **Parent:** [Integer sequence](#integer-sequence)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fibonacci_sequence)

###### Tribonacci

↑ **Parent:** [Integer sequence](#integer-sequence)

Interview problem!

Solutions:
- [cpp/tribonacci.cpp](cpp/tribonacci.cpp)

[Coding challenge websites](website.md#programming-problem-collection-website):
- [https://leetcode.com/problems/n-th-tribonacci-number](https://leetcode.com/problems/n-th-tribonacci-number)
- [https://www.geeksforgeeks.org/tribonacci-numbers/](https://www.geeksforgeeks.org/tribonacci-numbers/)

###### Kolakoski sequence

↑ **Parent:** [Integer sequence](#integer-sequence)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Kolakoski_sequence)

###### Generalized Kolakoski sequence

↑ **Parent:** [Kolakoski sequence](#kolakoski-sequence)

The generalized Kolakoski sequence is the generalization of the [Kolakoski sequence](#kolakoski-sequence) where you don't need to restrict yourself to 1,2 but can instead use any a,b pair.

###### Nilsson algorithm for the Kolakoski sequence

↑ **Parent:** [Kolakoski sequence](#kolakoski-sequence)

This algorithm is more efficient in space, using only $log(n)$, as it recursively compresses the state required to keep track of what to do next.

Time is still $O(n)$.

The table at [https://maths-people.anu.edu.au/~brent/pd/Kolakoski-UNSW.pdf](https://maths-people.anu.edu.au/~brent/pd/Kolakoski-UNSW.pdf) page 20 has a summary image, but it is hard to understand.

Let's do a step by step version now.

The notation we use is as follows:
```
1 2 (1) 1 (1)
```
means that:
- this is number 2
- there is 1 occurrence count left

Note that column 1 does not need to keep a count so we use notation such as:

```
1 2(0) 1(1)
```

The starting state is:
```
2 | 2 2(1) 2(1) 2(1) 2(1) ...
```
which means that it implicitly contains infinitely many `2(1)` at the end which we abbreviate just as:
```
2 | 2 2(1) ...
```
The actual algorithm will of course omit as many trailing `2(1)` as it can.

The update rules are:
- go left to right:
  - flip:
    ```
    x(0)       y(0)
    !x((!x)-1) unchanged
    ```

    continue going left to right.
  - repeat:
    ```
    x(0)   y(n > 0)
    x(x-1) y(n - 1)
    ```

    and then stop further updates.
Note that both rules don't overlap so that each update is always determined by only one of them at a time.

Also the first column is always implicitly `(0)`.

Use column 2 up once to repeat column 1:

```
2 | 2 2(1) ...
3 | 2 2(0) 2(1) ...
```

Here we:
- switch column 1 because column 2 reached 0 on previous step
- use column 3 up once to repeat column 2

```
2 | 2 2(1) ...
3 | 2 2(0) 2(1) ...
4 | 1 2(1) 2(0) 2(1) ...
```

- use column 2 up once to repeat 1

```
2 | 2 2(1) ...
3 | 2 2(0) 2(1) ...
4 | 1 2(1) 2(0) 2(1) ...
5 | 1 2(0) 2(1) 2(0) 2(1) ...
```

```
 2 | 2 2(1) ...
 3 | 2 2(0) 2(1) ...
 4 | 1 2(1) 2(0) 2(1) ...
 5 | 1 2(0) 2(0) 2(1) ...
 6 | 2 1(0) 2(1) 2(0) 2(1) ...
 7 | 1 1(0) 2(0) 2(0) 2(1) ...
 8 | 2 2(1) 1(0) 2(1) 2(0) 2(1) ...
 9 | 2 2(0) 1(0) 2(1) 2(0) 2(1) ...
10 | 1 1(0) 1(0) 2(0) 2(0) 2(1) ...
11 | 2 2(1) 2(1) 1(0) 2(1) 2(0) 2(1) ...
12 | 2 2(0) 2(1) 1(0) 2(1) 2(0) 2(1) ...
13 | 1 2(1) 2(0) 1(0) 2(1) 2(0) 2(1) ...
14 | 1 2(0) 2(0) 1(0) 2(1) 2(0) 2(1) ...
15 | 2 1(0) 1(0) 1(0) 2(0) 2(0) 2(1) ...
16 | 1 2(1) 2(1) 2(1) 1(0) 2(1) 2(0) 2(1) ...
```

###### Nilsson algorithm for the generalized Kolakoski sequence

↑ **Parent:** [Kolakoski sequence](#kolakoski-sequence)

Here's an execution for 2, 3. When `a != 1` we use `a` as the extra numbers instead of `b`:
```
 1 | 2 2(1) ...
 2 | 2 2(0) 2(1) ...
 3 | 3 2(1) 2(0) 2(1) ...
 4 | 3 2(0) 2(0) 2(1) ...
 5 | 2 3(2) 2(1) 2(0) 2(0) ...
 6 | 2 3(1) 2(1) 2(0) 2(1) ...
 7 | 2 3(0) 2(1) 2(0) 2(1) ...
 8 | 3 3(2) 2(0) 2(0) 2(1) ...
 9 | 3 3(1) 2(0) 2(0) 2(1) ...
10 | 3 3(0) 2(0) 2(0) 2(1) ...
11 | 2 2(1) 3(2) 2(1) 2(0) 2(1) ...
12 | 2 2(0) 3(2) 2(1) 2(0) 2(1) ...
13 | 3 2(1) 3(1) 2(1) 2(0) 2(1) ...
14 | 3 2(0) 3(1) 2(1) 2(0) 2(1) ...
15 | 2 2(1) 3(0) 2(1) 2(0) 2(1) ...
16 | 2 2(0) 3(0) 2(1) 2(0) 2(1) ...
17 | 3 3(2) 3(2) 2(0) 2(0) 2(1) ...
```
Furthermore, note that if `a = 1`, then the `a, b` sequence is a subset of the `b, a` sequence e.g.:
```
1, 2 = [1, 2, 2, 1, 1, 2, 1, ...]
2, 1 = [   2, 2, 1, 1, 2, 1, ...]
```
therefore we can always make `a` not be 1 by switching the pair and then using the generalized algorithm with `a != 1`.

## Function space

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Function_space)

Most notable example: [$\LTwo$](calculus.md#l2).

## Number

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Number)

### Scientific notation

↑ **Parent:** [Number](#number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Scientific_notation)

#### E notation

↑ **Parent:** [Scientific notation](#scientific-notation)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Scientific_notation#E_notation)

What do you prefer, `1 \times 10^{10}` or `1E10`.

### Natural number

↑ **Parent:** [Number](#number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Natural_number)

### Integer

↑ **Parent:** [Number](#number)  
🏷️ **Tags:** [Commutative ring](group.md#commutative-ring)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Integer)

### Rational number

↑ **Parent:** [Number](#number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rational_number)

#### Irrational number

↑ **Parent:** [Rational number](#rational-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Irrational_number)

##### Number of unknown rationality

↑ **Parent:** [Irrational number](#irrational-number)

This section is about numbers that we don't know if they are rational or not.

Bibliography:
- [https://www.quantamagazine.org/rational-or-not-this-basic-math-question-took-decades-to-answer-20250108/](https://www.quantamagazine.org/rational-or-not-this-basic-math-question-took-decades-to-answer-20250108/) Rational or Not? This Basic Math Question Took Decades to Answer (2025)

#### Fraction

↑ **Parent:** [Rational number](#rational-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fraction)

##### Reduced fraction

↑ **Parent:** [Fraction](#fraction)

A "reduced fraction" is a fraction that has the smallest possible [integer](#integer) [numerator](#numerator) and [denominator](#denominator) for its value.

For example:

$$
\frac{3}{6}
$$

is not a reduced fraction, because there is another fraction equal to it but with smaller [numerator](#numerator) and [denominator](#denominator):

$$
\frac{1}{2}
$$

###### Farey sequence

↑ **Parent:** [Reduced fraction](#reduced-fraction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Farey_sequence)

###### Farey sunburst

↑ **Parent:** [Farey sequence](#farey-sequence)

[https://en.wikipedia.org/w/index.php?title=Farey_sequence&oldid=1223364653#Farey_sunburst](https://en.wikipedia.org/w/index.php?title=Farey_sequence&oldid=1223364653#Farey_sunburst)

###### Number of elements in a Farey sequence

↑ **Parent:** [Reduced fraction](#reduced-fraction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Number_of_elements_in_a_Farey_sequence)

[https://en.wikipedia.org/w/index.php?title=Farey_sequence&oldid=1223364653#Sequence_length_and_index_of_a_fraction](https://en.wikipedia.org/w/index.php?title=Farey_sequence&oldid=1223364653#Sequence_length_and_index_of_a_fraction)

$$
|F_n| = 1 + \Phi(n)
$$

where $\Phi(n)$ is the [totient summatory function](mathematics.md#totient-summatory-function).

##### Numerator

↑ **Parent:** [Fraction](#fraction)

##### Denominator

↑ **Parent:** [Fraction](#fraction)

### Real number

↑ **Parent:** [Number](#number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Real_number)

A good definition is by using [Dedekind cuts](#dedekind-cut).

#### Dedekind cut

↑ **Parent:** [Real number](#real-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dedekind_cut)

#### Cardinality of the continuum

↑ **Parent:** [Real number](#real-number)

##### Countable set

↑ **Parent:** [Cardinality of the continuum](#cardinality-of-the-continuum)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Countable_set)

<h5 id="cantor-s-diagonal-argument">Cantor's diagonal argument</h5>

↑ **Parent:** [Cardinality of the continuum](#cardinality-of-the-continuum)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cantor's_diagonal_argument)

#### Mathematical constant

↑ **Parent:** [Real number](#real-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mathematical_constant)

##### Pi

↑ **Parent:** [Mathematical constant](#mathematical-constant)  
🏷️ **Tags:** [Transcendental number](#transcendental-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pi)

## Complex number

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Complex_number)

An [ordered pair](#ordered-pair) of two [real numbers](#real-number) with the complex addition and multiplication defined.

Forms both a:
- [division algebra](group.md#division-algebra) if thought of [$\R^2$](calculus.md#real-plane) with complex multiplication as the bilinear map of the [algebra](group.md#algebra-over-a-field)
- [field](group.md#field-mathematics)

### Complex conjugate

↑ **Parent:** [Complex number](#complex-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Complex_conjugate)

### Imaginary number

↑ **Parent:** [Complex number](#complex-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Imaginary_number)

### Imaginary unit

↑ **Parent:** [Complex number](#complex-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Imaginary_unit)

### Cayley-Dickson construction

↑ **Parent:** [Complex number](#complex-number)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cayley–Dickson construction)

Constructs the [quaternions](#quaternion) from [complex numbers](#complex-number), [octonions](#octonion) from [quaternions](#quaternion), and keeps doubling like this indefinitely.

#### Quaternion

↑ **Parent:** [Cayley-Dickson construction](#cayley-dickson-construction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Quaternion)

Kind of extends the [complex numbers](#complex-number).

Some facts that make them stand out:
- one of the only three real [associative](algebra.md#associative-property) [division algebras](group.md#division-algebra) in addition to the [real numbers](#real-number) and [complex numbers](#complex-number), according to the [classification of associative real division algebras](group.md#frobenius-theorem-real-division-algebras)
- the simplest non-[commutative](group.md#commutative-property) [division algebra](group.md#division-algebra). Contrast for example with [complex numbers](#complex-number) where multiplication is [commutative](group.md#commutative-property)

#### Octonion

↑ **Parent:** [Cayley-Dickson construction](#cayley-dickson-construction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Octonion)

Unlike the [quaternions](#quaternion), it is non-[associative](algebra.md#associative-property).

#### Sedenion

↑ **Parent:** [Cayley-Dickson construction](#cayley-dickson-construction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sedenion)

## Ordered pair

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ordered_pair)

[Sets](#set-mathematics) are unordered, but we can use them to create ordered objects, which are of fundamental importance. Notably, they are used in the definition of [functions](#function-mathematics).

## Logic

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Logic)

### Propositional logic

↑ **Parent:** [Logic](#logic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Propositional_logic)

This is the part of the [formalization of mathematics](formalization-of-mathematics.md) that deals only with the propositions.

In some systems, e.g. including [Metamath](#metamath), [modus ponens](#modus-ponens) alone tends to be enough, everything else can be defined based on it.

#### Modus ponens

↑ **Parent:** [Propositional logic](#propositional-logic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Modus_ponens)

#### If and only if

↑ **Parent:** [Propositional logic](#propositional-logic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/If_and_only_if)

### First-order logic

↑ **Parent:** [Logic](#logic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/First-order_logic)

Builds on top of [propositional logic](#propositional-logic), adding notably [existential quantification](#existential-quantification).

#### Existential quantification

↑ **Parent:** [First-order logic](#first-order-logic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Existential_quantification)

Models [existence](#existence) in the context of the [formalization of mathematics](formalization-of-mathematics.md).

##### Existence and uniqueness

↑ **Parent:** [Existential quantification](#existential-quantification)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Existence_and_uniqueness)

Existence and uniqueness results are fundamental in [mathematics](mathematics.md) because we often define objects by their properties, and then start calling them "the object", which is fantastically convenient.

But calling something "the object" only makes sense if there exists exactly one, and only one, object that satisfies the properties.

One particular context where these come up very explicitly is in solutions to [differential equations](calculus.md#differential-equation), e.g. [existence and uniqueness of solutions of partial differential equations](calculus.md#existence-and-uniqueness-of-solutions-of-partial-differential-equations).

###### Existence

↑ **Parent:** [Existence and uniqueness](#existence-and-uniqueness)

###### Uniqueness

↑ **Parent:** [Existence and uniqueness](#existence-and-uniqueness)

#### Universal quantification

↑ **Parent:** [First-order logic](#first-order-logic)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Universal_quantification)

## Entity formalizing mathematics

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)

### expMath

↑ **Parent:** [Entity formalizing mathematics](#entity-formalizing-mathematics)  
🏷️ **Tags:** [DARPA project](united-states.md#darpa-project)

[https://www.darpa.mil/research/programs/expmath-exponential-mathematics](https://www.darpa.mil/research/programs/expmath-exponential-mathematics)

Funded for example [Math, Inc](artificial-intelligence.md#math-inc) as mentioned at: [https://www.math.inc/gauss](https://www.math.inc/gauss).

## Formalization of X

↑ **Parent:** [Formalization of mathematics](formalization-of-mathematics.md)

This section is about formalization efforts of specific fields of [mathematics](mathematics.md).

### Formalization of [physics](physics.md)

↑ **Parent:** [Formalization of X](#formalization-of-x)

#### Formalization of physics project

↑ **Parent:** [Formalization of physics](#formalization-of-physics)

##### PhysLean

↑ **Parent:** [Formalization of physics project](#formalization-of-physics-project)  
🏷️ **Tags:** [Lean library](#lean-library)

[https://physlean.com/](https://physlean.com/)

##### Physics Derivation Graph

↑ **Parent:** [Formalization of physics project](#formalization-of-physics-project)

- [https://www.youtube.com/channel/UCBSInUAbtBkYDYKNc_iauVQ](https://www.youtube.com/channel/UCBSInUAbtBkYDYKNc_iauVQ)
- [https://derivationmap.net](https://derivationmap.net)
- [https://github.com/allofphysicsgraph/proofofconcept](https://github.com/allofphysicsgraph/proofofconcept)

## ↑ Ancestors (3)

1. [Area of mathematics](mathematics.md#area-of-mathematics)
2. [Mathematics](mathematics.md)
3. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (11)

- [The best articles by Ciro Santilli](articles.md)
- [Ciro Santilli's bad old event memory](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-bad-old-event-memory)
- [Computer science](computer-science.md)
- [Existential quantification](#existential-quantification)
- [Formal proof](#formal-proof)
- [Limit (mathematics)](calculus.md#limit-mathematics)
- [Mathematics](mathematics.md)
- [Propositional logic](#propositional-logic)
- [Set (mathematics)](#set-mathematics)
- [Settheory.net](physicist.md#settheory-net)
- [The art of programming](software.md#the-art-of-programming)
