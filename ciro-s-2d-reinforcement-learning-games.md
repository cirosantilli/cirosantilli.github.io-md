<h1 id="ciro-s-2d-reinforcement-learning-games">Ciro's 2D reinforcement learning games</h1>

↑ **Parent:** [The most important projects Ciro Santilli wants to do](todo-split.md)  
🏷️ **Tags:** [AI training game](ai-game.md)

Prototype: [https://github.com/cirosantilli/Urho3D-cheat](https://github.com/cirosantilli/Urho3D-cheat)

Prior art research: [https://github.com/cirosantilli/awesome-reinforcement-learning-games](https://github.com/cirosantilli/awesome-reinforcement-learning-games)

<a id="video-top-down-2d-continuous-game-with-urho3d-c-plus-plus-sdl-and-box2d-for-reinforcement-learning-by-ciro-santilli-2018"></a>
**[Video 1](#video-top-down-2d-continuous-game-with-urho3d-c-plus-plus-sdl-and-box2d-for-reinforcement-learning-by-ciro-santilli-2018). Top Down 2D Continuous Game with Urho3D C++ SDL and Box2D for Reinforcement learning by Ciro Santilli (2018)** [Source](https://youtube.com/watch?v=j_fl4xoGTKU). Source code at: [https://github.com/cirosantilli/Urho3D-cheat](https://github.com/cirosantilli/Urho3D-cheat).

<a id="image-screenshot-of-the-basketball-stage-of-ciro-s-2d-continuous-game"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/Basketball_stage_of_Ciro_Santilli&#039;s_2D_continuous_AI_game.png)

**[Figure 1](#image-screenshot-of-the-basketball-stage-of-ciro-s-2d-continuous-game). Screenshot of the basketball stage of Ciro's 2D continuous game**. Source code at: [https://github.com/cirosantilli/rl-game-2d-grid](https://github.com/cirosantilli/rl-game-2d-grid). Big kudos to [game-icons.net](game-icons-net.md) for the sprites.

Less good [discrete](discrete.md) prototype: [https://github.com/cirosantilli/rl-game-2d-grid](https://github.com/cirosantilli/rl-game-2d-grid) [YouTube](youtube.md) demo: [Video 1. "Top Down 2D Continuous Game with Urho3D C++ SDL and Box2D for Reinforcement learning by Ciro Santilli (2018)"](#video-top-down-2d-continuous-game-with-urho3d-c-plus-plus-sdl-and-box2d-for-reinforcement-learning-by-ciro-santilli-2018).

<a id="video-top-down-2d-discrete-tile-based-game-with-c-plus-plus-sdl-and-boost-r-tree-for-reinforcement-learning-by-ciro-santilli-2017"></a>
**[Video 2](#video-top-down-2d-discrete-tile-based-game-with-c-plus-plus-sdl-and-boost-r-tree-for-reinforcement-learning-by-ciro-santilli-2017). Top Down 2D Discrete Tile Based Game with C++ SDL and Boost R-Tree for Reinforcement Learning by Ciro Santilli (2017)** [Source](https://youtube.com/watch?v=TQ5k2u25eI8).

The goal of this project is to reach [artificial general intelligence](artificial-general-intelligence.md).

A few initiatives have created reasonable sets of robotics-like games for the purposes of AI development, most notably: [OpenAI](openai.md) and [DeepMind](deepmind.md).

However, all projects so far have only created sets of unrelated games, or worse: focused on closed games designed for humans!

What is really needed is to create a single cohesive game world, designed specifically for this purpose, and with a very large number of game mechanics.

Notably, by "game mechanic" is meant "a magic aspect of the game world, which cannot be explained by object's location and inertia alone" in order to test the [the missing link between continuous and discrete AI](the-missing-link-between-continuous-and-discrete-ai.md).

Much in the spirit of [gvgai](gvgai.md), we have to do the following loop:
- create an initial game that a human can solve
- find an AI that beats it well
- study the AI, and add a new mechanic that breaks the AI, but does not break a human!

The question then becomes: do we have enough computational power to simulation a game worlds that is analogous enough to the real world, so that our AI algorithms will also apply to the real world?

To reduce computation requirements, it is better to focus on a 2D world at first. Such world with the right mechanics can break any AI, while still being faster to simulate than a 3D world.

The initial prototype uses the Urho3D open source [game engine](game-engine.md), and that is a reasonable project, but a raw [Simple DirectMedia Layer](simple-directmedia-layer.md) + Box2D + [OpenGL](opengl.md) solution from scratch would be faster to develop for this use case, since Urho3D has a lot of human-gaming features that are not needed, and because 2019 Urho3D lead developers [disagree with the China censored keyword attack](https://github.com/cirosantilli/china-dictatorship/blob/23c5bd936361f78a8dd6bd1f412286808714d2da/communities-that-censor-politics.md).

Simulations such as these can be viewed as a form of [synthetic data generation procedure](https://en.wikipedia.org/wiki/Synthetic_data#Synthetic_data_in_machine_learning), where the goal is to use computer worlds to reduce the costs of experiments and to improve reproducibility.

Ciro has always had a feeling that AI research in the 2020's is too unambitious. How many teams are actually aiming for [AGI](artificial-general-intelligence.md)? When he then read [Superintelligence by Nick Bostrom (2014)](superintelligence-by-nick-bostrom-2014.md) it said the same. [AGI research has become a taboo in the early 21st century](agi-research-has-become-a-taboo-in-the-early-21st-century.md).

Related projects:
- [https://github.com/deepmind/lab2d](https://github.com/deepmind/lab2d): 2D [gridworld](gridworld.md) games, [C++](c-plus-plus.md) with Lua bindings

Related ideas:
- [https://www.youtube.com/watch?v=MHFrhIAj0ME?t=4183](https://www.youtube.com/watch?v=MHFrhIAj0ME?t=4183) [Can't get you out of my head by Adam Curtis (2021)](can-t-get-you-out-of-my-head-by-adam-curtis-2021.md) Part 1: Bloodshed on Wolf Mountain :)
- [https://www.youtube.com/watch?v=EUjc1WuyPT8](https://www.youtube.com/watch?v=EUjc1WuyPT8) [AI alignment](ai-alignment.md): Why It's Hard, and Where to Start by [Eliezer Yudkowsky](eliezer-yudkowsky.md) (2016)

Bibliograpy:
- [https://agents.inf.ed.ac.uk/blog/multiagent-learning-environments/](https://agents.inf.ed.ac.uk/blog/multiagent-learning-environments/) Multi-Agent Learning Environments (2021) by Lukas Schäfer from the [Autonomous agents research group of the University of Edinburgh](autonomous-agents-research-group-of-the-university-of-edinburgh.md). One of their games actually uses apples as visual represntation of rewards, exactly like Ciro's game. So funny. They also have a 2d continuous game: [https://agents.inf.ed.ac.uk/blog/multiagent-learning-environments/#mpe](https://agents.inf.ed.ac.uk/blog/multiagent-learning-environments/#mpe)
- humanoid robot simulation
  - 2022 MoCapAct by [Microsoft Research](microsoft-research.md): [https://www.microsoft.com/en-us/research/blog/mocapact-training-humanoid-robots-to-move-like-jagger](https://www.microsoft.com/en-us/research/blog/mocapact-training-humanoid-robots-to-move-like-jagger)
- [Section "AI training game"](ai-game.md)
- [Section "Software-based artificial life"](software-based-artificial-life.md)

<a id="video-deepmind-has-a-superhuman-level-quake-3-ai-team-by-two-minute-papers-2018"></a>
**[Video 3](#video-deepmind-has-a-superhuman-level-quake-3-ai-team-by-two-minute-papers-2018). DeepMind Has A Superhuman Level Quake 3 AI Team by Two Minute Papers (2018)** [Source](https://youtube.com/watch?v=MvFABFWPBrw). Commentary of [DeepMind](deepmind.md)'s 2019 [Capture the Flag paper](https://deepmind.com/blog/article/capture-the-flag-science). DeepMind does some similar simulations to what Ciro wants, but TODO do they publish source code for all of them? If not Ciro calls [bullshit](bullshit.md) on non-reproducible research. Does [this repo](https://github.com/deepmind/lab) contain everything?

<a id="video-openai-plays-hide-and-seek-and-breaks-the-game-by-two-minute-papers-2019"></a>
**[Video 4](#video-openai-plays-hide-and-seek-and-breaks-the-game-by-two-minute-papers-2019). OpenAI Plays Hide and Seek... and Breaks The Game! by Two Minute Papers (2019)** [Source](https://youtube.com/watch?v=Lu56xVlZ40M). Commentary of [OpenAi](openai.md)'s 2019 [hide and seek](https://openai.com/blog/emergent-tool-use/) paper. OpenAI does some similar simulations to what Ciro wants, but TODO do they publish source code for all of them? If not Ciro calls bullshit on non-reproducible research, and even worse due to the fake "Open" in the name. Does [this repo](https://github.com/openai/multi-agent-emergence-environments) contain everything?

<a id="video-much-bigger-simulation-ais-learn-phalanx-by-pezzza-s-work-2022"></a>
**[Video 5](#video-much-bigger-simulation-ais-learn-phalanx-by-pezzza-s-work-2022). Much bigger simulation, AIs learn Phalanx by Pezzza's Work (2022)** [Source](https://www.youtube.com/watch?v=tVNoetVLuQg). 2d agents with vision. Simple prey/predator scenario.

## ↑ Ancestors (3)

1. [The most important projects Ciro Santilli wants to do](todo-split.md)
2. [Ciro Santilli](ciro-santilli-split.md)
3. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (17)

- [Ciro Santilli's Homepage](split.md)
- [AI game](ai-game.md)
- [Artificial general intelligence](artificial-general-intelligence.md)
- [Can AGI be trained in simulations?](can-agi-be-trained-in-simulations.md)
- [Cocos2d](cocos2d.md)
- [DeepMind Lab](deepmind-lab.md)
- [game-icons.net](game-icons-net.md)
- [gvgai](gvgai.md)
- [Human brain](human-brain.md)
- [Machine learning](machine-learning-split.md)
- [Neuro-symbolic AI](neuro-symbolic-ai.md)
- [Phaser.js](phaser-js.md)
- [Questions for Ciro Santilli's future self](questions-for-ciro-santilli-s-future-self.md)
- [Real-time attack speedrun](real-time-attack-speedrun.md)
- [The missing link between continuous and discrete AI](the-missing-link-between-continuous-and-discrete-ai.md)
- [Universal basic income](universal-basic-income.md)
- [When the École Polytechnique mathematics department didn't let Ciro Santilli do his internship of choice due to grades](when-the-ecole-polytechnique-mathematics-department-didn-t-let-ciro-santilli-do-his-internship-of-choice-due-to-grades.md)
