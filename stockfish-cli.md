# Stockfish CLI

↑ **Parent:** [Stockfish (chess)](stockfish-chess.md)

[https://www.maketecheasier.com/use-stockfish-cli-master-chess](https://www.maketecheasier.com/use-stockfish-cli-master-chess) is a good source.

Most of what follows is part of the [Universal Chess Interface](universal-chess-interface.md). Tested on [Ubuntu 22.10](ubuntu-22-10.md), [Stockfish](stockfish-chess.md) 14.1.

After starting `stockfish` on the command line, `d` (presumably display) contains:
```
 +---+---+---+---+---+---+---+---+
 | r | n | b | q | k | b | n | r | 8
 +---+---+---+---+---+---+---+---+
 | p | p | p | p | p | p | p | p | 7
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 6
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 5
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 4
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 3
 +---+---+---+---+---+---+---+---+
 | P | P | P | P | P | P | P | P | 2
 +---+---+---+---+---+---+---+---+
 | R | N | B | Q | K | B | N | R | 1
 +---+---+---+---+---+---+---+---+
   a   b   c   d   e   f   g   h

Fen: rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1
Key: 8F8F01D4562F59FB
```
Sweet [ASCII art](ascii-art.md). where:
- `Fen`: [FEN notation](forsyth-edwards-notation.md)
- `Key`: TODO

Move white king's pawn from e2 to e4:
```
position startpos moves e2e4
```
Then display again:
```
d
```
gives:
```
 +---+---+---+---+---+---+---+---+
 | r | n | b | q | k | b | n | r | 8
 +---+---+---+---+---+---+---+---+
 | p | p | p | p | p | p | p | p | 7
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 6
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 5
 +---+---+---+---+---+---+---+---+
 |   |   |   |   | P |   |   |   | 4
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 3
 +---+---+---+---+---+---+---+---+
 | P | P | P | P |   | P | P | P | 2
 +---+---+---+---+---+---+---+---+
 | R | N | B | Q | K | B | N | R | 1
 +---+---+---+---+---+---+---+---+
   a   b   c   d   e   f   g   h

Fen: rnbqkbnr/pppppppp/8/8/4P3/8/PPPP1PPP/RNBQKBNR b KQkq - 0 1
Key: B46022469E3DD31B
```
so we see that the pawn moved.

Now let's make Stockfish think for one second what is the next best move for black:
```
go movetime 1000
```
gives as the last line:
```
bestmove c7c5 ponder g1f3
```
TODO:
- what is ponder? Something to do with thinking on the opponent's turn: [permanent brain](permanent-brain.md).
- understand the previous lines

To make the move it as suggested for black, we have to either repeat the entire sequence of movements:
```
position startpos moves e2e4 c7c5
```
`d`:
```
 +---+---+---+---+---+---+---+---+
 | r | n | b | q | k | b | n | r | 8
 +---+---+---+---+---+---+---+---+
 | p | p |   | p | p | p | p | p | 7
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 6
 +---+---+---+---+---+---+---+---+
 |   |   | p |   |   |   |   |   | 5
 +---+---+---+---+---+---+---+---+
 |   |   |   |   | P |   |   |   | 4
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   | 3
 +---+---+---+---+---+---+---+---+
 | P | P | P | P |   | P | P | P | 2
 +---+---+---+---+---+---+---+---+
 | R | N | B | Q | K | B | N | R | 1
 +---+---+---+---+---+---+---+---+
   a   b   c   d   e   f   g   h

Fen: rnbqkbnr/pp1ppppp/8/2p5/4P3/8/PPPP1PPP/RNBQKBNR w KQkq - 0 2
Key: 4CA78BCE9C2980B0
```
or alternatively we could also use the previous [FEN notation](forsyth-edwards-notation.md) as a starting point;
```
position fen rnbqkbnr/pppppppp/8/8/4P3/8/PPPP1PPP/RNBQKBNR b KQkq - 0 1 moves c7c5
```
Note how the [Universal Chess Interface](universal-chess-interface.md) interface is very simple: we just load a state and then decide what to do next for that one state. The engine holds only one and exactly one state at a time, and you can't even modify it differentially without loading new one from scratch.

Let's move white again with our brain with either:
```
position startpos moves e2e4 c7c5 d2d3
position fen rnbqkbnr/pp1ppppp/8/2p5/4P3/8/PPPP1PPP/RNBQKBNR w KQkq - 0 2 moves d2d3
```

Set a specific position from `fen`:
```
position fen rnbqkbnr/pppppppp/8/8/4P3/8/PPPP1PPP/RNBQKBNR b KQkq - 0 1
```

## ↑ Ancestors (9)

1. [Stockfish (chess)](stockfish-chess.md)
2. [Chess engine](chess-engine.md)
3. [Computer chess](computer-chess.md)
4. [Chess](chess.md)
5. [Deterministic perfect information board game](deterministic-perfect-information-board-game.md)
6. [Board game](board-game.md)
7. [Game](game.md)
8. [Art](art-split.md)
9. [Ciro Santilli's Homepage](split.md)
