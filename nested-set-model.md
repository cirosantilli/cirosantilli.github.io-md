# Nested set model

↑ **Parent:** [Tree representation](tree-representation.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nested_set_model)

This is particularly important in [SQL](sql-split.md): [Nested set model in SQL](nested-set-model-in-sql.md), as it is an efficient way to transverse trees there, since querying parents every time would require multiple disk accesses.

The [ASCII art](ascii-art.md) visualizations from [https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree/194031#194031](https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree/194031#194031) are worth reproducing.

As a tree:
- Root 1
  - Child 1.1
    - Child 1.1.1
    - Child 1.1.2
  - Child 1.2
    - Child 1.2.1
    - Child 1.2.2

As the sets:
```
 __________________________________________________________________________
|  Root 1                                                                  |
|   ________________________________    ________________________________   |
|  |  Child 1.1                     |  |  Child 1.2                     |  |
|  |   ___________    ___________   |  |   ___________    ___________   |  |
|  |  |  C 1.1.1  |  |  C 1.1.2  |  |  |  |  C 1.2.1  |  |  C 1.2.2  |  |  |
1  2  3___________4  5___________6  7  8  9___________10 11__________12 13 14
|  |________________________________|  |________________________________|  |
|__________________________________________________________________________|
```

Consider the following nested set:
```
0, 8, root
  1, 7, mathematics
    2, 3, geometry
      3, 6, calculus
        4, 5, derivative
        5, 6, integral
      6, 7, algebra
  7, 8, physics
```

When we want to insert one element, e.g. `limit`, normally under `calculus`, we have to specify:
- parent
- index within parent
so we have a method:
```
insert(parent, previousSibling)
```

## ↑ Ancestors (8)

1. [Tree representation](tree-representation.md)
2. [Tree (data structure)](tree-data-structure.md)
3. [Type of graph](type-of-graph.md)
4. [Graph (discrete mathematics)](graph-discrete-mathematics.md)
5. [Discrete mathematics](discrete-mathematics.md)
6. [Area of mathematics](area-of-mathematics.md)
7. [Mathematics](mathematics-split.md)
8. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Nested set model in SQL](nested-set-model-in-sql.md)
