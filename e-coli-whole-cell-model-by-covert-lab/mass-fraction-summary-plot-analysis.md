# Mass fraction summary plot analysis

↑ **Parent:** [Output overview](output-overview.md)

<a id="_48"></a>
Let's look into a sample plot, `out/manual/plotOut/svg_plots/massFractionSummary.svg`, and try to understand as much as we can about what it means and how it was generated.

<a id="_49"></a>
This plot contains how much of each type of mass is present in all cells. Since we simulated just one cell, it will be the same as the results for that cell.

<a id="_50"></a>
We can see that all of them grow more or less [linearly](../linear-function.md), perhaps as the start of an exponential. We can see that all of them grow more or less linearly, perhaps as the start of an exponential. We can see that all of them grow more or less linearly, perhaps as the start of an exponential.<a id="_51"></a>

<a id="_52"></a>
- total dry mass (mass excluding [water](../water.md))
<a id="_53"></a>
- [protein](../protein-split.md) mass
<a id="_54"></a>
- [rRNA](../ribosomal-rna.md) mass
<a id="_55"></a>
- [mRNA](../messenger-rna.md) mass
<a id="_56"></a>
- [DNA](../dna-split.md) mass. The last label is not very visible on the plots, but we can deduce it from the source code.
By grepping the title "Cell mass fractions" in the source code, we see the files:<a id="_57"></a>

```
models/ecoli/analysis/cohort/massFractionSummary.py
models/ecoli/analysis/multigen/massFractionSummary.py
models/ecoli/analysis/variant/massFractionSummary.py
```
which must correspond to the different `massFractionSummary` plots throughout different levels of the hierarchy.

<a id="_58"></a>
By reading `models/ecoli/analysis/variant/massFractionSummary.py` a little bit, we see that:<a id="_59"></a>

<a id="_60"></a>
- the plotting is done with [Matplotlib](../matplotlib.md), hurray
<a id="_61"></a>
- <a id="_62"></a>
  it is reading its data from files under `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/`, more precisely `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/columns/<column-name>/data`. They are binary files however.

  <a id="_63"></a>
  Looking at the source for `wholecell/io/tablereader.py` shows that those are just a standard [NumPy](../numpy.md) serialization mechanism. Maybe they should have used the [Hierarchical Data Format](../hierarchical-data-format.md) instead.

  <a id="_64"></a>
  We can also take this opportunity to try and find where the data is coming from. `Mass` from the `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/` looks like an ID, so we [`grep`](../grep.md) that and we reach `models/ecoli/listeners/mass.py`.

  <a id="_65"></a>
  From this we understand that all data that is to be saved from a simulation must be coming from listeners: likely nothing, or not much, is dumped by default, because otherwise it would take up too much disk space. You have to explicitly say what it is that you want to save via a listener that acts on each time step.

<a id="image-minimal-condition-mass-fraction-plot"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/9/94/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_mass_fraction_summary.svg" alt="" height="600">

**[Figure 1](#image-minimal-condition-mass-fraction-plot). Minimal condition mass fraction plot**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_mass_fraction_summary.svg). File name: `out/manual/plotOut/svg_plots/massFractionSummary.svg`

<a id="_66"></a>
More plot types will be explored at [time series run variant](time-series-run-variant.md), where we will contrast two runs with different [growth mediums](../growth-medium.md).

## ↑ Ancestors (12)

1. [Output overview](output-overview.md)
2. [E. Coli Whole Cell Model by Covert Lab](../e-coli-whole-cell-model-by-covert-lab-split.md)
3. [E. Coli whole cell simulation](../e-coli-whole-cell-simulation.md)
4. [Escherichia coli](../escherichia-coli.md)
5. [List of bacteria](../list-of-bacteria.md)
6. [Bacteria](../bacteria.md)
7. [Species](../species.md)
8. [Taxonomy](../taxonomy-split.md)
9. [Biology](../biology-split.md)
10. [Natural science](../natural-science.md)
11. [Science](../science-split.md)
12. [Ciro Santilli's Homepage](../split.md)
