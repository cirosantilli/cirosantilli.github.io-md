# Gridworld

↑ **Parent:** [2D game](2d-game.md)

A discrete 2D game on a rectangular grid: [https://towardsdatascience.com/reinforcement-learning-implement-grid-world-from-scratch-c5963765ebff](https://towardsdatascience.com/reinforcement-learning-implement-grid-world-from-scratch-c5963765ebff)

This is analogous to many traditional [board games](board-game.md) such as [chess](chess.md), the concept is very natural and maps well into computer.

The downsides of gridworld games are:
- it is hard to model speed in discrete worlds. When you 10x faster, when do you collide with something else that is also crossing your path?
- they tend to not use vector representations of objects. So to have an object be 10x longer than another one, the naive implementation has to add 10 smaller objects. This becomes untenable as the number of objects increases.

## 🏷️ Tagged (4)

- [Battlecode](battlecode.md)
- [DeepMind Lab2D](deepmind-lab2d.md)
- [Gridworld AI game](gridworld-ai-game.md)
- [gvgai](gvgai.md)

## ↑ Ancestors (6)

1. [2D game](2d-game.md)
2. [Video game graphics](video-game-graphics.md)
3. [Video game](video-game-split.md)
4. [Game](game.md)
5. [Art](art-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (2)

- [Ciro's 2D reinforcement learning games](ciro-s-2d-reinforcement-learning-games.md)
- [DeepMind Lab2D](deepmind-lab2d.md)
