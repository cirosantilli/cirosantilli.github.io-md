# Iterative in-order

↑ **Parent:** [In-order depth-first search](in-order-depth-first-search.md)

This is a bit harder than [iterative pre-order](iterative-pre-order.md): now we have to check if there is a left or right element or not:
- (START) push current
- if there is left:
  - move left
- else:
  - (ELSE) pop
  - visit
  - if there is right
    - move right
    - GOTO START
  - else:
    - GOTO ELSE

The control flow can be slightly simplified if we allow NULLs: [https://www.geeksforgeeks.org/inorder-tree-traversal-without-recursion/](https://www.geeksforgeeks.org/inorder-tree-traversal-without-recursion/)

## ↑ Ancestors (10)

1. [In-order depth-first search](in-order-depth-first-search.md)
2. [Depth-first search](depth-first-search.md)
3. [Tree traversal](tree-traversal.md)
4. [Tree (data structure)](tree-data-structure.md)
5. [Type of graph](type-of-graph.md)
6. [Graph (discrete mathematics)](graph-discrete-mathematics.md)
7. [Discrete mathematics](discrete-mathematics.md)
8. [Area of mathematics](area-of-mathematics.md)
9. [Mathematics](mathematics-split.md)
10. [Ciro Santilli's Homepage](split.md)
