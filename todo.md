# The most important projects Ciro Santilli wants to do

↑ **Parent:** [Ciro Santilli](ciro-santilli.md)

They are sorted in order of "most likely to get done first".

Top one: [OurBigBook.com](ourbigbook-com.md).

**Table of contents**

- [OurBigBook.com is number one](#ourbigbook-com-is-number-one)
- [Ciro's 2D reinforcement learning games](#ciro-s-2d-reinforcement-learning-games)
- [Videos of all key physics experiments](#videos-of-all-key-physics-experiments)
- [Website front-end for a mathematical formal proof system](#website-front-end-for-a-mathematical-formal-proof-system)

<h2 id="ourbigbook-com-is-number-one">OurBigBook.com is number one</h2>

↑ **Parent:** [The most important projects Ciro Santilli wants to do](todo.md)

Actual section at: [Section "OurBigBook.com"](ourbigbook-com.md)

<h2 id="ciro-s-2d-reinforcement-learning-games">Ciro's 2D reinforcement learning games</h2>

↑ **Parent:** [The most important projects Ciro Santilli wants to do](todo.md)  
🏷️ **Tags:** [AI training game](artificial-intelligence.md#ai-game)

Prototype: [https://github.com/cirosantilli/Urho3D-cheat](https://github.com/cirosantilli/Urho3D-cheat)

Prior art research: [https://github.com/cirosantilli/awesome-reinforcement-learning-games](https://github.com/cirosantilli/awesome-reinforcement-learning-games)

<a id="video-top-down-2d-continuous-game-with-urho3d-c-plus-plus-sdl-and-box2d-for-reinforcement-learning-by-ciro-santilli-2018"></a>
**[Video 1](#video-top-down-2d-continuous-game-with-urho3d-c-plus-plus-sdl-and-box2d-for-reinforcement-learning-by-ciro-santilli-2018). Top Down 2D Continuous Game with Urho3D C++ SDL and Box2D for Reinforcement learning by Ciro Santilli (2018)** [Source](https://youtube.com/watch?v=j_fl4xoGTKU). Source code at: [https://github.com/cirosantilli/Urho3D-cheat](https://github.com/cirosantilli/Urho3D-cheat).

<a id="image-screenshot-of-the-basketball-stage-of-ciro-s-2d-continuous-game"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/Basketball_stage_of_Ciro_Santilli&#039;s_2D_continuous_AI_game.png)

**[Figure 1](#image-screenshot-of-the-basketball-stage-of-ciro-s-2d-continuous-game). Screenshot of the basketball stage of Ciro's 2D continuous game**. Source code at: [https://github.com/cirosantilli/rl-game-2d-grid](https://github.com/cirosantilli/rl-game-2d-grid). Big kudos to [game-icons.net](video-game.md#game-icons-net) for the sprites.

Less good [discrete](calculus.md#discrete) prototype: [https://github.com/cirosantilli/rl-game-2d-grid](https://github.com/cirosantilli/rl-game-2d-grid) [YouTube](website.md#youtube) demo: [Video 1. "Top Down 2D Continuous Game with Urho3D C++ SDL and Box2D for Reinforcement learning by Ciro Santilli (2018)"](#video-top-down-2d-continuous-game-with-urho3d-c-plus-plus-sdl-and-box2d-for-reinforcement-learning-by-ciro-santilli-2018).

<a id="video-top-down-2d-discrete-tile-based-game-with-c-plus-plus-sdl-and-boost-r-tree-for-reinforcement-learning-by-ciro-santilli-2017"></a>
**[Video 2](#video-top-down-2d-discrete-tile-based-game-with-c-plus-plus-sdl-and-boost-r-tree-for-reinforcement-learning-by-ciro-santilli-2017). Top Down 2D Discrete Tile Based Game with C++ SDL and Boost R-Tree for Reinforcement Learning by Ciro Santilli (2017)** [Source](https://youtube.com/watch?v=TQ5k2u25eI8).

The goal of this project is to reach [artificial general intelligence](artificial-intelligence.md#artificial-general-intelligence).

A few initiatives have created reasonable sets of robotics-like games for the purposes of AI development, most notably: [OpenAI](artificial-intelligence.md#openai) and [DeepMind](artificial-intelligence.md#deepmind).

However, all projects so far have only created sets of unrelated games, or worse: focused on closed games designed for humans!

What is really needed is to create a single cohesive game world, designed specifically for this purpose, and with a very large number of game mechanics.

Notably, by "game mechanic" is meant "a magic aspect of the game world, which cannot be explained by object's location and inertia alone" in order to test the [the missing link between continuous and discrete AI](artificial-intelligence.md#the-missing-link-between-continuous-and-discrete-ai).

Much in the spirit of [gvgai](artificial-intelligence.md#gvgai), we have to do the following loop:
- create an initial game that a human can solve
- find an AI that beats it well
- study the AI, and add a new mechanic that breaks the AI, but does not break a human!

The question then becomes: do we have enough computational power to simulation a game worlds that is analogous enough to the real world, so that our AI algorithms will also apply to the real world?

To reduce computation requirements, it is better to focus on a 2D world at first. Such world with the right mechanics can break any AI, while still being faster to simulate than a 3D world.

The initial prototype uses the Urho3D open source [game engine](software.md#game-engine), and that is a reasonable project, but a raw [Simple DirectMedia Layer](video-game.md#simple-directmedia-layer) + Box2D + [OpenGL](software.md#opengl) solution from scratch would be faster to develop for this use case, since Urho3D has a lot of human-gaming features that are not needed, and because 2019 Urho3D lead developers [disagree with the China censored keyword attack](https://github.com/cirosantilli/china-dictatorship/blob/23c5bd936361f78a8dd6bd1f412286808714d2da/communities-that-censor-politics.md).

Simulations such as these can be viewed as a form of [synthetic data generation procedure](https://en.wikipedia.org/wiki/Synthetic_data#Synthetic_data_in_machine_learning), where the goal is to use computer worlds to reduce the costs of experiments and to improve reproducibility.

Ciro has always had a feeling that AI research in the 2020's is too unambitious. How many teams are actually aiming for [AGI](artificial-intelligence.md#artificial-general-intelligence)? When he then read [Superintelligence by Nick Bostrom (2014)](artificial-intelligence.md#superintelligence-by-nick-bostrom-2014) it said the same. [AGI research has become a taboo in the early 21st century](artificial-intelligence.md#agi-research-has-become-a-taboo-in-the-early-21st-century).

Related projects:
- [https://github.com/deepmind/lab2d](https://github.com/deepmind/lab2d): 2D [gridworld](video-game.md#gridworld) games, [C++](programming-language.md#c-plus-plus) with Lua bindings

Related ideas:
- [https://www.youtube.com/watch?v=MHFrhIAj0ME?t=4183](https://www.youtube.com/watch?v=MHFrhIAj0ME?t=4183) [Can't get you out of my head by Adam Curtis (2021)](film.md#can-t-get-you-out-of-my-head-by-adam-curtis-2021) Part 1: Bloodshed on Wolf Mountain :)
- [https://www.youtube.com/watch?v=EUjc1WuyPT8](https://www.youtube.com/watch?v=EUjc1WuyPT8) [AI alignment](artificial-intelligence.md#ai-alignment): Why It's Hard, and Where to Start by [Eliezer Yudkowsky](website.md#eliezer-yudkowsky) (2016)

Bibliograpy:
- [https://agents.inf.ed.ac.uk/blog/multiagent-learning-environments/](https://agents.inf.ed.ac.uk/blog/multiagent-learning-environments/) Multi-Agent Learning Environments (2021) by Lukas Schäfer from the [Autonomous agents research group of the University of Edinburgh](university.md#autonomous-agents-research-group-of-the-university-of-edinburgh). One of their games actually uses apples as visual represntation of rewards, exactly like Ciro's game. So funny. They also have a 2d continuous game: [https://agents.inf.ed.ac.uk/blog/multiagent-learning-environments/#mpe](https://agents.inf.ed.ac.uk/blog/multiagent-learning-environments/#mpe)
- humanoid robot simulation
  - 2022 MoCapAct by [Microsoft Research](microsoft.md#microsoft-research): [https://www.microsoft.com/en-us/research/blog/mocapact-training-humanoid-robots-to-move-like-jagger](https://www.microsoft.com/en-us/research/blog/mocapact-training-humanoid-robots-to-move-like-jagger)
- [Section "AI training game"](artificial-intelligence.md#ai-game)
- [Section "Software-based artificial life"](biology.md#software-based-artificial-life)

<a id="video-deepmind-has-a-superhuman-level-quake-3-ai-team-by-two-minute-papers-2018"></a>
**[Video 3](#video-deepmind-has-a-superhuman-level-quake-3-ai-team-by-two-minute-papers-2018). DeepMind Has A Superhuman Level Quake 3 AI Team by Two Minute Papers (2018)** [Source](https://youtube.com/watch?v=MvFABFWPBrw). Commentary of [DeepMind](artificial-intelligence.md#deepmind)'s 2019 [Capture the Flag paper](https://deepmind.com/blog/article/capture-the-flag-science). DeepMind does some similar simulations to what Ciro wants, but TODO do they publish source code for all of them? If not Ciro calls [bullshit](molecular-biology.md#bullshit) on non-reproducible research. Does [this repo](https://github.com/deepmind/lab) contain everything?

<a id="video-openai-plays-hide-and-seek-and-breaks-the-game-by-two-minute-papers-2019"></a>
**[Video 4](#video-openai-plays-hide-and-seek-and-breaks-the-game-by-two-minute-papers-2019). OpenAI Plays Hide and Seek... and Breaks The Game! by Two Minute Papers (2019)** [Source](https://youtube.com/watch?v=Lu56xVlZ40M). Commentary of [OpenAi](artificial-intelligence.md#openai)'s 2019 [hide and seek](https://openai.com/blog/emergent-tool-use/) paper. OpenAI does some similar simulations to what Ciro wants, but TODO do they publish source code for all of them? If not Ciro calls bullshit on non-reproducible research, and even worse due to the fake "Open" in the name. Does [this repo](https://github.com/openai/multi-agent-emergence-environments) contain everything?

<a id="video-much-bigger-simulation-ais-learn-phalanx-by-pezzza-s-work-2022"></a>
**[Video 5](#video-much-bigger-simulation-ais-learn-phalanx-by-pezzza-s-work-2022). Much bigger simulation, AIs learn Phalanx by Pezzza's Work (2022)** [Source](https://www.youtube.com/watch?v=tVNoetVLuQg). 2d agents with vision. Simple prey/predator scenario.

## Videos of all key physics experiments

↑ **Parent:** [The most important projects Ciro Santilli wants to do](todo.md)

It is unbelievable that you can't find easily on YouTube recreations of many of the key [physics](physics.md)/[chemistry](chemistry.md) experiments and of common laboratory techniques.

Experiments, the techniques required to to them, and the history of how they were first achieved, are the heart of the natural sciences. Without them, there is no motivation, no beauty, no nothing.

[School](education.md#school) gives too much emphasis on the formulas. This is bad. Much more important is to understand how the experiments are done in greater detail.

The videos must be completely reproducible, indicating the exact model of every experimental element used, and how the experiment is setup.

A bit like what [Ciro Santilli](ciro-santilli.md) does in his [Stack Overflow contributions](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-stack-overflow-contributions) but with computers, by indicating precise versions of his operating system, software stack, and hardware whenever they may matter.

It is understandable that some experiments are just to complex and expensive to re-create. As an extreme example, say, a precise description of the [Large Hadron Collider](particle-physics.md#large-hadron-collider) anyone? But experiments up to the mid-20th century before "[big science](https://en.wikipedia.org/wiki/Big_Science)"? We should have all of those nailed down.

We should strive to achieve the cheapest most reproducible setup possible with currently available materials: recreating the original historic setup is [cute](art.md), but not a priority.

Furthermore, it is also desirable to reproduce the original setups whenever possible in addition to having the most convenient modern setup.

Lists of good experiments to cover be found at: [the most important physics experiments](physics.md#the-most-important-physics-experiments).

This project is to a large extent a political endeavour.

Someone with enough access to labs has to step up and make a name for themselves through the huge effort of creating a baseline of amazing content without yet being famous.

Until it reaches a point that this person is actively sought to create new material for others, and things snowball out of control. Maybe, if the Gods allow it, that person could be Ciro.

Tutorials with a gazillion photos and short videos are also equally good or even better than videos, see for example Ciro's [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in bacteria](oxford-nanopore-river-bacteria.md) for an example that goes toward that level of perfection.

The [Applied Science](technology.md#applied-science-youtube-channel) does well in that direction.

This project is one step that could be taken towards improving the [replication crisis](science.md#replication-crisis) of [science](science.md). It's a bit what [Hackster.io](website.md#hackster-io) wants to do really. But that website is useless, just use [OurBigBook.com](ourbigbook-com.md) and create videos instead :-)

We're maintaining a list of experiments for which we could not find decent videos at: [Section "Physics experiment without a decent modern video"](physics.md#physics-experiment-without-a-decent-modern-video).

[Ciro Santilli](ciro-santilli.md) visited the teaching labs of a large European university in the early 2020's. They had a few large rooms filled with mostly ready to run versions of several key experiments, many/most from "modern physics", e.g. [Stern-Gerlach experiment](relativistic-quantum-mechanics.md#stern-gerlach-experiment), [Quantum Hall effect](quantum-mechanics.md#quantum-hall-effect), etc.. These included booklets with detailed descriptions of how to operate the apparatus, what you'd expect to see, and the theory behind them. With a fat copyright notice at the bottom. If only such universities aimed to actually serve the public for free rather than hoarding resources to get more tuition fees, university level education would already have been solved a long time ago!

One thing we can more or less easily do is to search for existing freely licensed videos and add them to the corresponding [Wikipedia](website.md#wikipedia) page where missing. This requires knowing how to search for freely licensed videos:
- [Wikimedia Commons](website.md#wikimedia-commons) video search, e.g.: [https://commons.wikimedia.org/w/index.php?search=spectophotometry&title=Special:MediaSearch&go=Go&type=video](https://commons.wikimedia.org/w/index.php?search=spectophotometry&title=Special:MediaSearch&go=Go&type=video)
- [YouTube](website.md#youtube) creative commons video search

Related:
- relevant University [YouTube](website.md#youtube) channels:
  - [UCSB Physics Lecture Demonstrations](physics.md#ucsb-physics-lecture-demonstrations) he's the cutest
  - [UNSW Physics YouTube channel](physics.md#unsw-physics-youtube-channel): [https://www.youtube.com/@UNSWPhysics](https://www.youtube.com/@UNSWPhysics)
  - [https://www.youtube.com/c/HarvardNaturalSciencesLectureDemonstrations/videos](https://www.youtube.com/c/HarvardNaturalSciencesLectureDemonstrations/videos)
- [K-12](education.md#k-12) demo projects:
  - [https://www.communityscienceworkshops.org/](https://www.communityscienceworkshops.org/)
  - [https://twitter.com/Physicsbus](https://twitter.com/Physicsbus)
  - [https://www.littlehouseofscience.com/](https://www.littlehouseofscience.com/)
- books:
- Practical approach series by [Oxford University Press](university-of-oxford.md#oxford-university-press): [https://global.oup.com/academic/content/series/p/practical-approach-series-pas](https://global.oup.com/academic/content/series/p/practical-approach-series-pas)

## Website front-end for a mathematical formal proof system

↑ **Parent:** [The most important projects Ciro Santilli wants to do](todo.md)  
🏷️ **Tags:** [Proof assistant](formalization-of-mathematics.md#proof-assistant)

When [Ciro Santilli](ciro-santilli.md) first learnt the old [Zermelo-Fraenkel set theory](formalization-of-mathematics.md#zermelo-fraenkel-set-theory) and the idea of [formal proofs](formalization-of-mathematics.md#formal-proof), his teenager [mind was completely blown](brain.md#mind-blown).

Finally, there it was: a proper and precise definition of [mathematics](mathematics.md), including [a definition of integers](https://en.wikipedia.org/wiki/Set-theoretic_definition_of_natural_numbers), reals and limits!

Theorems are strings, proofs are string manipulations, and axioms are the initial strings that you can use.

Once proved, press a button on your computer, and the proof is automatically verified. No messy complicated "group of savants" reading it for 4 years and looking for flaws!

There are a few [proof assistant](formalization-of-mathematics.md#proof-assistant) systems with several theorems in their [Git](software.md#git) tracked standard library. The hottest ones circa 2020 are:
- [https://github.com/HOL-Theorem-Prover/HOL](https://github.com/HOL-Theorem-Prover/HOL)
- [https://github.com/seL4/isabelle](https://github.com/seL4/isabelle). Rumours have it that this is "uncompilable" from source without [blobs](cirism.md#evil). It does however offer a very rich [IDE](software.md#integrated-development-environment).
- [https://github.com/coq/coq](https://github.com/coq/coq)
- [Metamath](formalization-of-mathematics.md#metamath) this one is likely an older and less powerful system, but the web presentation and tutorial are very good! Source: [https://github.com/metamath/metamath-exe](https://github.com/metamath/metamath-exe) Here is a proof that 2 + 2 equals 4: [http://us.metamath.org/mpeuni/2p2e4.html](http://us.metamath.org/mpeuni/2p2e4.html)
- [Lean](formalization-of-mathematics.md#lean-proof-assistant)
- [https://www.bookofproofs.org/branches/fpl-formal-proving-language/](https://www.bookofproofs.org/branches/fpl-formal-proving-language/) from [BookofProofs](website.md#bookofproofs)

And here are some more interesting links:
- [https://github.com/awesomo4000/awesome-provable](https://github.com/awesomo4000/awesome-provable) an awesome list of formal stuff
- [https://devel.isa-afp.org/](https://devel.isa-afp.org/) Isabelle Archive of Formal Proofs. A curated list of Isabelle proofs, with minimal web UI. This is almost what we need, but without the manual curation, and with a better web UI.
- [http://www.cs.ru.nl/~freek/100/](http://www.cs.ru.nl/~freek/100/) list of how many of the "arbitrarily" selected [the Hundred Greatest Theorems by Paul and Jack Abad (1999)](mathematics.md#the-hundred-greatest-theorems-by-paul-and-jack-abad-1999) had been proved in several formal systems, serving therefore as a [benchmark](software.md#benchmark) of sorts

However, as expressed by the [QED manifesto](formalization-of-mathematics.md#qed-manifesto), is unbelievable that there isn't one awesome and dominating website, that hosts all those proofs, possibly an on the browser editor, and which all mathematicians in the world use as the one golden reference of mathematics to rule them all!

Just imagine the impact.

Standard library maintainers don't have to deal with the impossible question of what is "beautiful" or "useful" enough mathematics to deserve merged: users just push content to the online database, and star what they like!

We then just use [GitHub](software.md#github)-like namespaces for each person's theorem, e.g. "cirosantilli/fundmaental-theorem-of-calculus" or "johndoe/fundmaental-theorem-of-calculus" so that each person owns their own preferred definition IDs, which others can reuse.

No more endless [bikeshedding](brain.md#law-of-triviality) over what insane level of generality do your [analysis](calculus.md#mathematical-analysis) theorems need to be ([Ciro Santilli](ciro-santilli.md) attended at talk about [Lean](formalization-of-mathematics.md#lean-proof-assistant) where the speaker mentioned this was a problem)!

This would move things more out of the "pull request and Git tracked code" approach, into a more "database with entries" version of things.

Furthermore, it is just a matter of time until the "single standard library" approach starts to break down, as the git clone becomes impossibly large. At this point, people have to start publishing separate packages. And when this happens, you would need to retest every package that you add to your project. This is why a centralized database is just inevitable at some point, it just scales better.

Interested in a conjecture? No problem: just subscribe to its formal statement + all known equivalents, and get an email on your inbox when it gets proved!

Are you a garage mathematician and have managed to prove a hard theorem, but no "real" mathematician will read your proof because your unknown? [Fuck](biology.md#sexual-intercourse) that, just publish it on the system and let it get auto verified. Overnight fame awaits.

Notation incompatibility hell? A thing of the past, just automatically convert to your preferred representation.

Such a system would be the perfect companion to [OurBigBook.com](ourbigbook-com.md). Just like computer code offers the backbone of [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat) Linux kernel tutorials, a formal proof system website would be the backbone of mathematics tutorials! You know what, if [OurBigBook.com](ourbigbook-com.md) becomes insanely successful, Ciro is going to add this to it later on.

Furthermore, it would not be too hard to achieve this system!

All we would need would be something analogous to a package registry like [PyPI](programming-language.md#python-package-index) or [NodeJS' registry](https://www.npmjs.com/).

Then, each person can publish packages containing proofs.

Packages can rely on other packages that contain pre-requisites definition or theorem.

Packages are just regular git repos, with some metadata. One notable metadata would be a human readable description of the theorems the package provides.

The package registry would then in addition to most package registries have a [CI](software.md#continuous-integration) [server](computer.md#server-computing) in it, that checks the correctness of all proofs, generates a web-page showing each theorem.

All proofs can be conditional: the package registry simply shows clearly what axiom set a theorem is based on.

This is a close as we can get to [Erdős' book](https://en.wikipedia.org/wiki/Proofs_from_THE_BOOK).

Maybe Ciro will just stuff this into [OurBigBook.com](ourbigbook-com.md) once that takes over the world.

This project could be seen as a more automated/less moderated version of [ProofWiki](website.md#proofwiki).

This would be a bit like [erdosproblems.com](mathematics.md#erdosproblems-com), but with formal proofs. Note for example that [Formal Conjectures](formalization-of-mathematics.md#formal-conjectures) has formalized these specific problems at: [https://github.com/google-deepmind/formal-conjectures/tree/main/FormalConjectures/ErdosProblems](https://github.com/google-deepmind/formal-conjectures/tree/main/FormalConjectures/ErdosProblems)

Bibliography:
- [The Math Genome Project](formalization-of-mathematics.md#the-math-genome-project) has very similar end goals. Apparently it will run proofs on server against the stdlib, but not allow one proof to depend on another, so in the end you still have to pull request everything back. Also there may be moderation forever, unclear. Ciro tried to create a dummy lolol theorem without any correct syntax and it just became private. Also apparently every single proof needs corresponding LaTeX manually written to be accepted. Cowards!
- [https://math.stackexchange.com/questions/1767070/what-is-the-current-state-of-formalized-mathematics/3297536#3297536](https://math.stackexchange.com/questions/1767070/what-is-the-current-state-of-formalized-mathematics/3297536#3297536)
- [https://math.stackexchange.com/questions/2747661/why-is-there-not-a-system-for-computer-checking-mathematical-proofs-yet-2018](https://math.stackexchange.com/questions/2747661/why-is-there-not-a-system-for-computer-checking-mathematical-proofs-yet-2018)
- [https://stackoverflow.com/questions/19421234/how-do-i-generate-latex-from-isabelle-hol](https://stackoverflow.com/questions/19421234/how-do-i-generate-latex-from-isabelle-hol)
- [https://stackoverflow.com/questions/30152139/what-are-the-strengths-and-weaknesses-of-the-isabelle-proof-assistant-compared-t](https://stackoverflow.com/questions/30152139/what-are-the-strengths-and-weaknesses-of-the-isabelle-proof-assistant-compared-t)
- [https://arxiv.org/abs/2102.03044](https://arxiv.org/abs/2102.03044) SPIRG, a [decentralized](technology.md#decentralized) version of this
- [https://proofnet.org/](https://proofnet.org/): [ChatGPT](artificial-intelligence.md#chatgpt) pointed [Ciro Santilli](ciro-santilli.md) to this, but it has like 4 broken archives? [https://web.archive.org/web/20220523140733/http://www.proofnet.org/](https://web.archive.org/web/20220523140733/http://www.proofnet.org/) Does it really exist or is it just hallucination? There is a [AI Math benchmark](artificial-intelligence.md#math-ai-benchmark) with that name though: [https://arxiv.org/abs/2302.12433](https://arxiv.org/abs/2302.12433)
- [https://formalabstracts.github.io/](https://formalabstracts.github.io/) is an idea without implementation. By mathematician [Thomas Callister Hales](https://ourbigbook.com/go/topic/thomas-callister-hales).
- [https://x.com/_Mira___Mira_/status/2003302921476378713](https://x.com/_Mira___Mira_/status/2003302921476378713)

  > I want the world's biggest proof database.
  > 
  > Pose any theorem and bots will try to prove it. If they fail, then it's an open question.  
  > People can collaborate to prove it or make partial progress, generalize it, use it as an axiom.
  > 
  > As AI improves, we become the "Google of math".

  Registered domain `proofoverflow.com`.
- [https://www.newton.ac.uk/event/bprw03/](https://www.newton.ac.uk/event/bprw03/) 2025 Big Proof workshop at the [University of Cambridge](university.md#university-of-cambridge)

[Ciro Santilli](ciro-santilli.md) pinging people:
- [https://mastodon.social/@cirosantilli/114201226569666331](https://mastodon.social/@cirosantilli/114201226569666331) [Terence Tao](mathematics.md#terence-tao), why not, he's interested in formal!

## 🏷️ Tagged (1)

- [OurBigBook.com](ourbigbook-com.md)

## ↑ Ancestors (2)

1. [Ciro Santilli](ciro-santilli.md)
2. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (1)

- [Ciro Santilli's Homepage](README.md)
