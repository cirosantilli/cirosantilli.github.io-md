# Website front-end for a mathematical formal proof system

↑ **Parent:** [The most important projects Ciro Santilli wants to do](todo-split.md)  
🏷️ **Tags:** [Proof assistant](proof-assistant.md)

When [Ciro Santilli](ciro-santilli-split.md) first learnt the old [Zermelo-Fraenkel set theory](zermelo-fraenkel-set-theory.md) and the idea of [formal proofs](formal-proof.md), his teenager [mind was completely blown](mind-blown.md).

Finally, there it was: a proper and precise definition of [mathematics](mathematics-split.md), including [a definition of integers](https://en.wikipedia.org/wiki/Set-theoretic_definition_of_natural_numbers), reals and limits!

Theorems are strings, proofs are string manipulations, and axioms are the initial strings that you can use.

Once proved, press a button on your computer, and the proof is automatically verified. No messy complicated "group of savants" reading it for 4 years and looking for flaws!

There are a few [proof assistant](proof-assistant.md) systems with several theorems in their [Git](git.md) tracked standard library. The hottest ones circa 2020 are:
- [https://github.com/HOL-Theorem-Prover/HOL](https://github.com/HOL-Theorem-Prover/HOL)
- [https://github.com/seL4/isabelle](https://github.com/seL4/isabelle). Rumours have it that this is "uncompilable" from source without [blobs](evil.md). It does however offer a very rich [IDE](integrated-development-environment.md).
- [https://github.com/coq/coq](https://github.com/coq/coq)
- [Metamath](metamath.md) this one is likely an older and less powerful system, but the web presentation and tutorial are very good! Source: [https://github.com/metamath/metamath-exe](https://github.com/metamath/metamath-exe) Here is a proof that 2 + 2 equals 4: [http://us.metamath.org/mpeuni/2p2e4.html](http://us.metamath.org/mpeuni/2p2e4.html)
- [Lean](lean-proof-assistant.md)
- [https://www.bookofproofs.org/branches/fpl-formal-proving-language/](https://www.bookofproofs.org/branches/fpl-formal-proving-language/) from [BookofProofs](bookofproofs.md)

And here are some more interesting links:
- [https://github.com/awesomo4000/awesome-provable](https://github.com/awesomo4000/awesome-provable) an awesome list of formal stuff
- [https://devel.isa-afp.org/](https://devel.isa-afp.org/) Isabelle Archive of Formal Proofs. A curated list of Isabelle proofs, with minimal web UI. This is almost what we need, but without the manual curation, and with a better web UI.
- [http://www.cs.ru.nl/~freek/100/](http://www.cs.ru.nl/~freek/100/) list of how many of the "arbitrarily" selected [the Hundred Greatest Theorems by Paul and Jack Abad (1999)](the-hundred-greatest-theorems-by-paul-and-jack-abad-1999.md) had been proved in several formal systems, serving therefore as a [benchmark](benchmark.md) of sorts

However, as expressed by the [QED manifesto](qed-manifesto.md), is unbelievable that there isn't one awesome and dominating website, that hosts all those proofs, possibly an on the browser editor, and which all mathematicians in the world use as the one golden reference of mathematics to rule them all!

Just imagine the impact.

Standard library maintainers don't have to deal with the impossible question of what is "beautiful" or "useful" enough mathematics to deserve merged: users just push content to the online database, and star what they like!

We then just use [GitHub](github.md)-like namespaces for each person's theorem, e.g. "cirosantilli/fundmaental-theorem-of-calculus" or "johndoe/fundmaental-theorem-of-calculus" so that each person owns their own preferred definition IDs, which others can reuse.

No more endless [bikeshedding](law-of-triviality.md) over what insane level of generality do your [analysis](mathematical-analysis.md) theorems need to be ([Ciro Santilli](ciro-santilli-split.md) attended at talk about [Lean](lean-proof-assistant.md) where the speaker mentioned this was a problem)!

This would move things more out of the "pull request and Git tracked code" approach, into a more "database with entries" version of things.

Furthermore, it is just a matter of time until the "single standard library" approach starts to break down, as the git clone becomes impossibly large. At this point, people have to start publishing separate packages. And when this happens, you would need to retest every package that you add to your project. This is why a centralized database is just inevitable at some point, it just scales better.

Interested in a conjecture? No problem: just subscribe to its formal statement + all known equivalents, and get an email on your inbox when it gets proved!

Are you a garage mathematician and have managed to prove a hard theorem, but no "real" mathematician will read your proof because your unknown? [Fuck](sexual-intercourse.md) that, just publish it on the system and let it get auto verified. Overnight fame awaits.

Notation incompatibility hell? A thing of the past, just automatically convert to your preferred representation.

Such a system would be the perfect companion to [OurBigBook.com](ourbigbook-com-split.md). Just like computer code offers the backbone of [Linux Kernel Module Cheat](linux-kernel-module-cheat-split.md) Linux kernel tutorials, a formal proof system website would be the backbone of mathematics tutorials! You know what, if [OurBigBook.com](ourbigbook-com-split.md) becomes insanely successful, Ciro is going to add this to it later on.

Furthermore, it would not be too hard to achieve this system!

All we would need would be something analogous to a package registry like [PyPI](python-package-index.md) or [NodeJS' registry](https://www.npmjs.com/).

Then, each person can publish packages containing proofs.

Packages can rely on other packages that contain pre-requisites definition or theorem.

Packages are just regular git repos, with some metadata. One notable metadata would be a human readable description of the theorems the package provides.

The package registry would then in addition to most package registries have a [CI](continuous-integration.md) [server](server-computing.md) in it, that checks the correctness of all proofs, generates a web-page showing each theorem.

All proofs can be conditional: the package registry simply shows clearly what axiom set a theorem is based on.

This is a close as we can get to [Erdős' book](https://en.wikipedia.org/wiki/Proofs_from_THE_BOOK).

Maybe Ciro will just stuff this into [OurBigBook.com](ourbigbook-com-split.md) once that takes over the world.

This project could be seen as a more automated/less moderated version of [ProofWiki](proofwiki.md).

This would be a bit like [erdosproblems.com](erdosproblems-com.md), but with formal proofs. Note for example that [Formal Conjectures](formal-conjectures.md) has formalized these specific problems at: [https://github.com/google-deepmind/formal-conjectures/tree/main/FormalConjectures/ErdosProblems](https://github.com/google-deepmind/formal-conjectures/tree/main/FormalConjectures/ErdosProblems)

Bibliography:
- [The Math Genome Project](the-math-genome-project.md) has very similar end goals. Apparently it will run proofs on server against the stdlib, but not allow one proof to depend on another, so in the end you still have to pull request everything back. Also there may be moderation forever, unclear. Ciro tried to create a dummy lolol theorem without any correct syntax and it just became private. Also apparently every single proof needs corresponding LaTeX manually written to be accepted. Cowards!
- [https://math.stackexchange.com/questions/1767070/what-is-the-current-state-of-formalized-mathematics/3297536#3297536](https://math.stackexchange.com/questions/1767070/what-is-the-current-state-of-formalized-mathematics/3297536#3297536)
- [https://math.stackexchange.com/questions/2747661/why-is-there-not-a-system-for-computer-checking-mathematical-proofs-yet-2018](https://math.stackexchange.com/questions/2747661/why-is-there-not-a-system-for-computer-checking-mathematical-proofs-yet-2018)
- [https://stackoverflow.com/questions/19421234/how-do-i-generate-latex-from-isabelle-hol](https://stackoverflow.com/questions/19421234/how-do-i-generate-latex-from-isabelle-hol)
- [https://stackoverflow.com/questions/30152139/what-are-the-strengths-and-weaknesses-of-the-isabelle-proof-assistant-compared-t](https://stackoverflow.com/questions/30152139/what-are-the-strengths-and-weaknesses-of-the-isabelle-proof-assistant-compared-t)
- [https://arxiv.org/abs/2102.03044](https://arxiv.org/abs/2102.03044) SPIRG, a [decentralized](decentralized.md) version of this
- [https://proofnet.org/](https://proofnet.org/): [ChatGPT](chatgpt.md) pointed [Ciro Santilli](ciro-santilli-split.md) to this, but it has like 4 broken archives? [https://web.archive.org/web/20220523140733/http://www.proofnet.org/](https://web.archive.org/web/20220523140733/http://www.proofnet.org/) Does it really exist or is it just hallucination? There is a [AI Math benchmark](math-ai-benchmark.md) with that name though: [https://arxiv.org/abs/2302.12433](https://arxiv.org/abs/2302.12433)
- [https://formalabstracts.github.io/](https://formalabstracts.github.io/) is an idea without implementation. By mathematician [Thomas Callister Hales](https://ourbigbook.com/go/topic/thomas-callister-hales).
- [https://x.com/_Mira___Mira_/status/2003302921476378713](https://x.com/_Mira___Mira_/status/2003302921476378713)

  > I want the world's biggest proof database.
  > 
  > Pose any theorem and bots will try to prove it. If they fail, then it's an open question.  
  > People can collaborate to prove it or make partial progress, generalize it, use it as an axiom.
  > 
  > As AI improves, we become the "Google of math".

  Registered domain `proofoverflow.com`.
- [https://www.newton.ac.uk/event/bprw03/](https://www.newton.ac.uk/event/bprw03/) 2025 Big Proof workshop at the [University of Cambridge](university-of-cambridge.md)

[Ciro Santilli](ciro-santilli-split.md) pinging people:
- [https://mastodon.social/@cirosantilli/114201226569666331](https://mastodon.social/@cirosantilli/114201226569666331) [Terence Tao](terence-tao.md), why not, he's interested in formal!

## ↑ Ancestors (3)

1. [The most important projects Ciro Santilli wants to do](todo-split.md)
2. [Ciro Santilli](ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (5)

- [BookofProofs](bookofproofs.md)
- [Formalization of mathematics](formalization-of-mathematics-split.md)
- [Proof assistant](proof-assistant.md)
- [QED manifesto](qed-manifesto.md)
- [Web-based proof assistant](web-based-proof-assistant.md)
