# In-order depth-first search

↑ **Parent:** [Depth-first search](depth-first-search.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/In-order_depth-first_search)

This is the order in which a [binary search tree](binary-search-tree.md) should be traversed for ordered output, i.e.:
- everything to the left is smaller than parent
- everything to the right is larger than parent

This ordering makes sense for [binary trees](binary-tree.md) and not [k-ary trees](k-ary-tree.md) in general because if there are more than two nodes it is not clear what the top node should go in the middle of.

This is unlike [pre-order depth-first search](pre-order-depth-first-search.md) and [post-order depth-first search](post-order-depth-first-search.md) which generalize obviously to general trees.

**Table of contents**

- [Iterative in-order](iterative-in-order.md)

## ↑ Ancestors (9)

1. [Depth-first search](depth-first-search.md)
2. [Tree traversal](tree-traversal.md)
3. [Tree (data structure)](tree-data-structure.md)
4. [Type of graph](type-of-graph.md)
5. [Graph (discrete mathematics)](graph-discrete-mathematics.md)
6. [Discrete mathematics](discrete-mathematics.md)
7. [Area of mathematics](area-of-mathematics.md)
8. [Mathematics](mathematics-split.md)
9. [Ciro Santilli's Homepage](split.md)
