<h1 id="arc-agi-1-problem/007bbfb">007bbfb</h1>

↑ **Parent:** [Train](train.md)

<a id="arc-agi-1-problem/_219"></a>
[https://arcprize.org/play?task=007bbfb7](https://arcprize.org/play?task=007bbfb7)

<a id="arc-agi-1-problem/_220"></a>
Hard input constraints:<a id="arc-agi-1-problem/_221"></a>

<a id="arc-agi-1-problem/_222"></a>
- inputs are 3x3
<a id="arc-agi-1-problem/_223"></a>
- inputs contain only 2 colors monocolored: black and another

<a id="arc-agi-1-problem/_224"></a>
Hard output constraints:<a id="arc-agi-1-problem/_225"></a>

<a id="arc-agi-1-problem/_226"></a>
- output is 3x input width and height. Suggests that the output is a 3x3 grid based on the input.<a id="arc-agi-1-problem/_227"></a>

  <a id="arc-agi-1-problem/_228"></a>
  - stronger: if output is split as a 3x3 grid, then each 3x3 block is either black or a copy as input. Which is which?<a id="arc-agi-1-problem/_229"></a>

    <a id="arc-agi-1-problem/_230"></a>
    - stronger: each pixel of the input determines if block is black or copy (final solution)
<a id="arc-agi-1-problem/_231"></a>
- output contains only two colors: black and another<a id="arc-agi-1-problem/_232"></a>

  <a id="arc-agi-1-problem/_233"></a>
  - stronger: the same two colors as input

<a id="arc-agi-1-problem/_234"></a>
Input output comparison:<a id="arc-agi-1-problem/_235"></a>

<a id="arc-agi-1-problem/_236"></a>
- input appears pasted on output multiple times: suggests it is being copy pasted

<a id="arc-agi-1-problem/_237"></a>
Hard output constraints:<a id="arc-agi-1-problem/_238"></a>

<a id="arc-agi-1-problem/_239"></a>
- <a id="arc-agi-1-problem/_240"></a>
  output is 3x input width and height: suggests that the output is a 3x3 grid based on the input

  <a id="arc-agi-1-problem/_241"></a>
  If that is the case, let's try to figure out what is placed on each output grid.

  <a id="arc-agi-1-problem/_242"></a>
  Notice: each grid element is either blank or the input.

  <a id="arc-agi-1-problem/_243"></a>
  OK so let's determine what in the input determines each output grid.

  <a id="arc-agi-1-problem/_244"></a>
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
