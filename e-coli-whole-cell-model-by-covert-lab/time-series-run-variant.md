# Time series run variant

↑ **Parent:** [Run variants](run-variants.md)

<a id="_74"></a>
To modify the nutrients as a function of time, with To select a time series we can use something like:<a id="_75"></a>

```
python runscripts/manual/runSim.py --variant nutrientTimeSeries 25 25
```
As mentioned in `python runscripts/manual/runSim.py --help`, `nutrientTimeSeries` is one of the choices from [https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/models/ecoli/sim/variants/__init__.py#L57](https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/models/ecoli/sim/variants/__init__.py#L57)

<a id="_76"></a>
`25 25` means to start from index 25 and also end at 25, so running just one simulation. `25 27` would run 25 then 26 and then 27 for example.

<a id="_77"></a>
The timeseries with index 25 is `reconstruction/ecoli/flat/condition/timeseries/000025_cut_aa.tsv` and contains<a id="_78"></a>

```
"time (units.s)" "nutrients"
0 "minimal_plus_amino_acids"
1200 "minimal"
```
so we understand that it starts with extra [amino acids](../amino-acid.md) in the medium, which benefit the cell, and half way through those are removed at time 1200s = 20 minutes. We would therefore expect the cell to start expressing amino acid production genes exactly at that point.

<a id="_79"></a>
`nutrients` likely means `condition` in that file however, see bug report with `1 1` failing:  [https://github.com/CovertLab/WholeCellEcoliRelease/issues/24](https://github.com/CovertLab/WholeCellEcoliRelease/issues/24)

<a id="_80"></a>
When we do this the simulation ends in:<a id="_81"></a>

```
Simulation finished:
 - Length: 0:34:23
 - Runtime: 0:08:03
```
so we see that the doubling time was faster than the one with minimal conditions of `0:42:49`, which makes sense, since during the first 20 minutes the cell had extra [amino acid](../amino-acid.md) nutrients at its disposal.

<a id="_82"></a>
The output directory now contains simulation output data under `out/manual/nutrientTimeSeries_000025/`. Let's run analysis and plots for that:<a id="_83"></a>

```
python runscripts/manual/analysisVariant.py &&
python runscripts/manual/analysisCohort.py --variant 25 &&
python runscripts/manual/analysisMultigen.py --variant 25 &&
python runscripts/manual/analysisSingle.py --variant 25
```

<a id="_84"></a>
We can now compare the outputs of this run to the default `wildtype_000000` run from [Section "Install and first run"](install-and-first-run.md).

<a id="_85"></a>
<a id="_86"></a>
- <a id="_87"></a>
  `out/manual/plotOut/svg_plots/massFractionSummary.svg`: because we now have two variants in the same `out/` folder, `wildtype_000000` and `nutrientTimeSeries_000025`, we now see a side by side comparision of both on the same graph!

  <a id="_88"></a>
  The run variant where we started with amino acids initially grows faster as expected, because the cell didn't have to make it's own amino acids, so growth is a bit more efficient.

  <a id="_89"></a>
  Then, at 20 minutes, which is about 0.3 hours, we see that the cell starts growing a bit less fast as the slope of the curve decreases a bit, because we removed that free amino acid supply.

  <a id="image-minimal-condition-vs-amino-acid-cut-mass-fraction-plot"></a>
  <img src="https://upload.wikimedia.org/wikipedia/commons/5/5f/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_mass_fraction_summary.svg" alt="" height="600">

  **[Figure 2](#image-minimal-condition-vs-amino-acid-cut-mass-fraction-plot). Minimal condition vs amino acid cut mass fraction plot**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_mass_fraction_summary.svg). From file `out/manual/plotOut/svg_plots/massFractionSummary.svg`.

<a id="_90"></a>
The following plots from under `out/manual/wildtype_000000/000000/{generation_000000,nutrientTimeSeries_000025}/000000/plotOut/svg_plots` have been manually joined side-by-side with:<a id="_91"></a>

```
for f in out/manual/wildtype_000000/000000/generation_000000/000000/plotOut/svg_plots/*; do
  echo $f
  svg_stack.py \
    --direction h \
    out/manual/wildtype_000000/000000/generation_000000/000000/plotOut/svg_plots/$(basename $f) \
    out/manual/nutrientTimeSeries_000025/000000/generation_000000/000000/plotOut/svg_plots/$(basename $f) \
    > tmp/$(basename $f)
done
```

<a id="image-amino-acid-counts"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/e/e1/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_amino_acid_counts.svg" alt="" height="800">

**[Figure 3](#image-amino-acid-counts). Amino acid counts**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_amino_acid_counts.svg). `aaCounts.svg`:<a id="_92"></a>

<a id="_93"></a>
- default: quantities just increase
<a id="_94"></a>
- amino acid cut: there is an abrupt fall at 20 minutes when we cut off external supply, presumably because it takes some time for the cell to start producing its own

---

<a id="_95"></a>
<a id="image-external-exchange-fluxes-of-amino-acids"></a>


<img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes_of_amino_acids.svg" alt="" height="800">

**[Figure 4](#image-external-exchange-fluxes-of-amino-acids). External exchange fluxes of amino acids**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes_of_amino_acids.svg). `aaExchangeFluxes.svg`:<a id="_96"></a>

<a id="_97"></a>
- default: no exchanges
<a id="_98"></a>
- <a id="_99"></a>
  amino acid cut: for all graphs except [phenylalanine](../phenylalanine.md) (PHE), either the cell was intaking the AA (negative flux), and that intake goes to 0 when the supply is cut, or the flux is always 0.

  <a id="_100"></a>
  For PHE however, the flux is at all times, except shortly after the cut. Why? And why there was no excretion on the default conditions?

---

<a id="image-evaluation-time"></a>


![](https://upload.wikimedia.org/wikipedia/commons/d/d6/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_evaluation_time.svg)

**[Figure 5](#image-evaluation-time). Evaluation time**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_evaluation_time.svg). `evaluationTime.svg`: this has nothing to do with biology, but it is rather a [profile](../profiling-computer-programming.md) of the program runtime. We can see that the simulation gets slower and slower as time passes, presumably because there are more and more molecules to simulate.

<a id="image-mrna-count-of-highly-expressed-mrnas"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_mrna_count_of_highly_expressed_mRNAs.svg" alt="" height="800">

**[Figure 6](#image-mrna-count-of-highly-expressed-mrnas). mRNA count of highly expressed mRNAs**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_mrna_count_of_highly_expressed_mRNAs.svg). From file `expression_rna_03_high.svg`. Each of the entries is a [gene](../gene.md) using the conventional gene naming convention of `xyzW`, e.g. here's the [BioCyc](../biocyc.md) for the first entry, `tufA`: [https://biocyc.org/gene?orgid=ECOLI&id=EG11036](https://biocyc.org/gene?orgid=ECOLI&id=EG11036), which comments <a id="_101"></a>
> Elongation factor Tu (EF-Tu) is the most abundant protein in E. coli.

 and <a id="_102"></a>
> In E. coli, EF-Tu is encoded by two genes, tufA and tufB

. What they seem to mean is that tufA and tufB are two similar molecules, either of which can make up the [EF-Tu](../ef-tu.md) of the [E. Coli](../escherichia-coli.md), which is an important part of [translation](../translation-biology.md).

---

<a id="image-external-exchange-fluxes"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/4/49/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes.svg" alt="" height="1000">

**[Figure 7](#image-external-exchange-fluxes). External exchange fluxes**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes.svg). <a id="_103"></a>
`mediaExcange.svg`: this one is similar to `aaExchangeFluxes.svg`, but it also tracks other substances. The color version makes it easier to squeeze more substances in a given space, but you lose the shape of curves a bit. The title seems reversed: red must be excretion, since that's where [glucose](../glucose.md) (GLC) is.

<a id="_104"></a>
The substances are different between the default and amino acid cut graphs, they seem to be the most exchanged substances. On the amino cut graph, first we see the cell intaking most (except [phenylalanine](../phenylalanine.md), which is excreted for some reason). When we cut amino acids, the uptake of course stops.

---

## ↑ Ancestors (12)

1. [Run variants](run-variants.md)
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

## ← Incoming links (2)

- [Mass fraction summary plot analysis](mass-fraction-summary-plot-analysis.md)
- [Other run variants](other-run-variants.md)
