# Other run variants

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](../e-coli-whole-cell-model-by-covert-lab-split.md)

<a id="_105"></a>
Besides [time series run variants](time-series-run-variant.md), conditions can also be selected directly without a time series as in:<a id="_106"></a>

```
python runscripts/manual/runSim.py --variant condition 1 1
```
which select row indices from `reconstruction/ecoli/flat/condition/condition_defs.tsv`. The above `1 1` would mean the second line of that file which starts with:<a id="_107"></a>

```
"condition" "nutrients" "genotype perturbations" "doubling time (units.min)" "active TFs"
"basal" "minimal" {} 44.0 []
"no_oxygen" "minimal_minus_oxygen" {} 100.0 []
"with_aa" "minimal_plus_amino_acids" {} 25.0 ["CPLX-125", "MONOMER0-162", "CPLX0-7671", "CPLX0-228", "MONOMER0-155"]
```
so `1` means `no_oxygen`.

## ↑ Ancestors (11)

1. [E. Coli Whole Cell Model by Covert Lab](../e-coli-whole-cell-model-by-covert-lab-split.md)
2. [E. Coli whole cell simulation](../e-coli-whole-cell-simulation.md)
3. [Escherichia coli](../escherichia-coli.md)
4. [List of bacteria](../list-of-bacteria.md)
5. [Bacteria](../bacteria.md)
6. [Species](../species.md)
7. [Taxonomy](../taxonomy-split.md)
8. [Biology](../biology-split.md)
9. [Natural science](../natural-science.md)
10. [Science](../science-split.md)
11. [Ciro Santilli's Homepage](../split.md)
