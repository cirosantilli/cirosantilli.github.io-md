# Semidirect product

↑ **Parent:** [Direct product of groups](direct-product-of-groups.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Semidirect_product)

As per [https://en.wikipedia.org/w/index.php?title=Semidirect_product&oldid=1040813965#Properties](https://en.wikipedia.org/w/index.php?title=Semidirect_product&oldid=1040813965#Properties), unlike the [Direct product](direct-product.md), the semidirect product of two goups is neither [unique](uniqueness.md), nor does it always [exist](existence.md), and there is no known algorithmic way way to tell if one exists or not.

This is because reaching the "output" of the semidirect produt of two groups requires extra non-obvious information that might not exist. This is because the semi-direct product is based on the [product of group subsets](product-of-group-subsets.md). So you start with two small and completely independent groups, and it is not obvious how to join them up, i.e. how to define the group operation of the product group that is compatible with that of the two smaller input groups. Contrast this with the [Direct product](direct-product.md), where the composition is simple: just use the group operation of each group on either side.

Product of group subsets

So in other words, it is not a [function](function-mathematics.md) like the [Direct product](direct-product.md). The semidiret product is therefore more like a property of three groups. 

The semidirect product is more general than the [direct product of groups](direct-product-of-groups.md) when thinking about the [group extension problem](group-extension-problem.md), because with the [direct product of groups](direct-product-of-groups.md), both subgroups of the larger group are necessarily also normal (trivial projection [group homomorphism](group-homomorphism.md) on either side), while for the semidirect product, only one of them does.

Conversely, [https://en.wikipedia.org/w/index.php?title=Semidirect_product&oldid=1040813965](https://en.wikipedia.org/w/index.php?title=Semidirect_product&oldid=1040813965) explains that if $G = N \rtimes H$, and besides the implied requirement that N is normal, H is also normal, then $G = N \times H$.

Smallest example: $D_6 = C_3 \rtimes C_2$ where $D$ is a [dihedral group](dihedral-group.md) and $C$ are [cyclic groups](cyclic-group.md). $C_3$ (the rotation) is a normal subgroup of $D_6$, but $C_2$ (the flip) is not.

Note that with the [Direct product](direct-product.md) instead we get $C_6$ and not $D_6$, i.e. $C_3 \times C_2 = C_6$ as per [the direct product of two cyclic groups of coprime order is another cyclic group](the-direct-product-of-two-cyclic-groups-of-coprime-order-is-another-cyclic-group.md).

TODO:
- why does one of the groups have to be normal in the definition?
- what is the smallest example of a non-[simple group](simple-group.md) that is neither a direct nor a semi-direct product of any two other groups?

Bibliography: [https://math.stackexchange.com/questions/1726939/is-this-intuition-for-the-semidirect-product-of-groups-correct](https://math.stackexchange.com/questions/1726939/is-this-intuition-for-the-semidirect-product-of-groups-correct)

## ↑ Ancestors (6)

1. [Direct product of groups](direct-product-of-groups.md)
2. [Group](group-split.md)
3. [Algebra](algebra-split.md)
4. [Area of mathematics](area-of-mathematics.md)
5. [Mathematics](mathematics-split.md)
6. [Ciro Santilli's Homepage](split.md)
