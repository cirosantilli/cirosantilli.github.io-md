<h1 id="arc-agi-1-problem/007bbfb">007bbfb</h1>

↑ **Parent:** [Train](train.md)

[https://arcprize.org/play?task=007bbfb7](https://arcprize.org/play?task=007bbfb7)

Hard input constraints:
- inputs are 3x3
- inputs contain only 2 colors monocolored: black and another

Hard output constraints:
- output is 3x input width and height. Suggests that the output is a 3x3 grid based on the input.
  - stronger: if output is split as a 3x3 grid, then each 3x3 block is either black or a copy as input. Which is which?
    - stronger: each pixel of the input determines if block is black or copy (final solution)
- output contains only two colors: black and another
  - stronger: the same two colors as input

Input output comparison:
- input appears pasted on output multiple times: suggests it is being copy pasted

Hard output constraints:
- output is 3x input width and height: suggests that the output is a 3x3 grid based on the input

  If that is the case, let's try to figure out what is placed on each output grid.

  Notice: each grid element is either blank or the input.

  OK so let's determine what in the input determines each output grid.

  Because input in 3x3 maybe there's a direct mapping.

## ↑ Ancestors (16)

1. [Train](train.md)
2. [ARC-AGI-1 problem](../arc-agi-1-problem.md)
3. [ARC-AGI-1](../arc-agi-1.md)
4. [Official ARC-AGI problem set](../official-arc-agi-problem-set.md)
5. [ARC-AGI problem set](../arc-agi-problem-set.md)
6. [ARC-AGI](../arc-agi.md)
7. [AGI test](../agi-test.md)
8. [Artificial general intelligence](../artificial-general-intelligence.md)
9. [AI by capability](../ai-by-capability.md)
10. [Artificial intelligence](../artificial-intelligence-split.md)
11. [Machine learning](../machine-learning-split.md)
12. [Computer](../computer-split.md)
13. [Information technology](../information-technology.md)
14. [Area of technology](../area-of-technology.md)
15. [Technology](../technology-split.md)
16. [Ciro Santilli's Homepage](../split.md)
