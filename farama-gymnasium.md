# Farama Gymnasium

↑ **Parent:** [OpenAI Gym](openai-gym.md)

[https://github.com/Farama-Foundation/Gymnasium](https://github.com/Farama-Foundation/Gymnasium)

[OpenAI Gym](openai-gym.md) development by [OpenAI](openai.md) ceased in 2021, and the [Farama Foundation](farama-foundation.md) not for profit took up maintenance of it.

gymnasium==1.1.1 just worked on [Ubuntu 24.10](ubuntu-24-10.md) testing with the [hello world](hello-world-program.md) [gym/random_control.py](gym/random_control.py):
```
sudo apt install swig
cd gym
virtualenv -p python3
. .venv/bin/activate
pip install -r requirements-python-3-12.txt
./random_control.py
```
just works and opens a game window on my desktop.

<a id="image-lunar-lander-environment-of-farama-gymnasium-with-random-controls"></a>
![](https://web.archive.org/web/20250225114240im_/https://gymnasium.farama.org/_images/lunar_lander.gif)

**[Figure 7](#image-lunar-lander-environment-of-farama-gymnasium-with-random-controls). Lunar Lander environment of Farama Gymnasium with random controls**.

This example just passes random commands to the ship so don't expect wonders. The cool thing about it though is that you can open any environment with it e.g.
```
./random_control.py CarRacing-v3
```

To manually control it we can use [gym/moon_play.py](gym/moon_play.py):
```
cd gym
./moon_play.py
```

Manual control is extremely useful to get an intuition about the problem. You will notice immediately that controlling the ship is extremely difficult.

<a id="image-lunar-lander-environment-of-farama-gymnasium-with-manual-control"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/Gymnasium_LunarLander-v3_manual_control.gif)

**[Figure 8](#image-lunar-lander-environment-of-farama-gymnasium-with-manual-control). Lunar Lander environment of Farama Gymnasium with manual control**.

We slow it down to 10 FPS to give us some fighting chance.

We don't know if it is realistic, but what is certain is that this is definitely not designed to be a fun video game!
- the legs of the lander are short and soft, and you're not supposed to hit the body on ground, so you have to go very slow
- the thrusters are quite weak and inertia management is super important
- the ground is very slippery
A good strategy is to land anywhere very slowly and then inch yourself towards the landing pad.

The documentation for it is available at: [https://gymnasium.farama.org/environments/box2d/lunar_lander/](https://gymnasium.farama.org/environments/box2d/lunar_lander/) The agent input is described as:

> The state is an 8-dimensional vector: the coordinates of the lander in x & y, its linear velocities in x & y, its angle, its angular velocity, and two booleans that represent whether each leg is in contact with the ground or not.

so it is a fundamentally flawed robot training example as global x and y coordinates are precisely known.

Variation in the scenario comes from:
- initial speed of vehicle
- shape of lunar surface, but TODO can the ship observe the lunar surface shape in any way? If not, once again, this is a deeply flawed example.

The actions are documented at:
- 0: do nothing
- 1: fire left orientation engine
- 2: fire main engine
- 3: fire right orientation engine
so we can make it spin like mad counter clockwise with:
```
action = 1
```

To actually play the games manually with keyboard, you need to define your own keybindings with [gymnasium.utils.play.play](https://gymnasium.farama.org/api/utils/#gymnasium.utils.play.play). Feature request for default keybindings: [https://github.com/Farama-Foundation/Gymnasium/discussions/1330](https://github.com/Farama-Foundation/Gymnasium/discussions/1330)

There is no [C](c-programming-language.md) API, you have to go through [Python](python-programming-language.md): [https://github.com/Farama-Foundation/Gymnasium/discussions/1181](https://github.com/Farama-Foundation/Gymnasium/discussions/1181). Shame.

They have video recording support, minimal ex [https://stackoverflow.com/questions/77042526/how-to-record-and-save-video-of-gym-environment/79514542#79514542](https://stackoverflow.com/questions/77042526/how-to-record-and-save-video-of-gym-environment/79514542#79514542)

Announced at:
- [https://mastodon.social/@cirosantilli/114177836474854152](https://mastodon.social/@cirosantilli/114177836474854152)
- [https://x.com/cirosantilli/status/1901617258482352552](https://x.com/cirosantilli/status/1901617258482352552)
- [https://www.facebook.com/cirosantilli/videos/1315866553003785/](https://www.facebook.com/cirosantilli/videos/1315866553003785/)

**Table of contents**

- [Farama Gymnasium solutions](farama-gymnasium-solutions.md)
- [Farama Foundation](farama-foundation.md)

## ↑ Ancestors (13)

1. [OpenAI Gym](openai-gym.md)
2. [OpenAI project](openai-project.md)
3. [OpenAI](openai.md)
4. [Entity creating AI games](entity-creating-ai-games.md)
5. [AI game](ai-game.md)
6. [Path to AGI](path-to-agi.md)
7. [Artificial intelligence](artificial-intelligence-split.md)
8. [Machine learning](machine-learning-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Farama Gymnasium](farama-gymnasium.md)
- [OpenAI Gym](openai-gym.md)
