# E. Coli Whole Cell Model by Covert Lab

↑ **Parent:** [E. Coli whole cell simulation](taxonomy.md#e-coli-whole-cell-simulation)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles.md)

[https://github.com/CovertLab/WholeCellEcoliRelease](https://github.com/CovertLab/WholeCellEcoliRelease) is a [whole cell simulation](cell.md#whole-cell-simulation) model created by [Covert Lab](university.md#covert-lab) and other collaborators.

The project is written in [Python](programming-language.md#python-programming-language), hurray!

But according to te [README](software.md#readme), it seems to be the use a [code drop](software.md#code-drop) model with on-request access to master. [Ciro Santilli](ciro-santilli.md) asked at [rationale on GitHub discussion](https://github.com/CovertLab/WholeCellEcoliRelease/discussions/23), and they confirmed as expected that it is to:
- to prevent their [publication](education.md#academic-publishing) ideas from being stolen. Who would steal publication ideas with public proof in an issue tracker without crediting original authors? [Academia is broken](education.md#academia-is-broken). Academia should be the most open form of knowledge sharing. But instead we get this silly competition for publication points.
- to prevent noise from non-collaborators. But they only get like 2 issues as year on such a meganiche subject... Did you know that you can ignore people, and even block them if they are particularly annoying? Much more likely is that no one will every hear about your project and that it will die with its last graduate student slave.

The project is a followup to the earlier [M. genitalium whole cell model by Covert lab](taxonomy.md#m-genitalium-whole-cell-model-by-covert-lab) which modelled [Mycoplasma genitalium](taxonomy.md#mycoplasma-genitalium). [E. Coli](taxonomy.md#escherichia-coli) has 8x more genes (500 vs 4k), but it the undisputed [bacterial](taxonomy.md#bacteria) [model organism](biology.md#model-organism) and as such has been studied much more thoroughly. It also reproduces faster than Mycoplasma (20 minutes vs a few hours), which is a huge advantages for validation/exploratory [experiments](science.md#experiment).

The project has a partial dependency on the [proprietary](law.md#proprietary-software) [optimization software](computer-science.md#optimization-software) [CPLEX](computer-science.md#cplex) which is [freeware](law.md#freeware), for students, not sure what it is used for exactly, from the comment in the `requirements.txt` the dependency is only partial.

This project makes [Ciro Santilli](ciro-santilli.md) think of the [E. Coli](taxonomy.md#escherichia-coli) as an [optimization problem](computer-science.md#optimization-problem). Given such external nutrient/temperature condition, which [DNA](dna.md) sequence makes the cell grow the fastest? Balancing [metabolites](molecular-biology.md#metabolite) feels like designing a [Factorio](video-game.md#factorio) speedrun.

There is one major thing missing thing in the current model: [promoters](dna.md#promoter-genetics)/[transcription factor](dna.md#transcription-factor) interactions are not modelled due to lack/low quality of experimental data: [https://github.com/CovertLab/WholeCellEcoliRelease/issues/21](https://github.com/CovertLab/WholeCellEcoliRelease/issues/21). They just have a magic direct "[transcription factor](dna.md#transcription-factor) to [gene](dna.md#gene)" relationship, encoded at [reconstruction/ecoli/flat/foldChanges.tsv](https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/reconstruction/ecoli/flat/foldChanges.tsv) in terms of type "if this is present, such protein is expressed 10x more". [Transcription units](dna.md#transcription-unit) are not implemented at all it appears.

Everything in this section refers to version [7e4cc9e57de76752df0f4e32eca95fb653ea64e4](https://github.com/CovertLab/WholeCellEcoliRelease/tree/7e4cc9e57de76752df0f4e32eca95fb653ea64e4), the code drop from November 2020, and was tested on [Ubuntu](systems-programming.md#ubuntu) 21.04 with a docker install of `docker.pkg.github.com/covertlab/wholecellecolirelease/wcm-full` with image id 502c3e604265, unless otherwise noted.

**Table of contents**

- [Install and first run](#install-and-first-run)
- [Output overview](#output-overview)
  - [Mass fraction summary plot analysis](#mass-fraction-summary-plot-analysis)
- [Run variants](#run-variants)
  - [Default run variant](#default-run-variant)
  - [Time series run variant](#time-series-run-variant)
- [Other run variants](#other-run-variants)
- [Source code overview](#source-code-overview)
  - [Condition](#condition)
- [Model validation](#model-validation)
- [Publications](#publications)

## Install and first run

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

At [7e4cc9e57de76752df0f4e32eca95fb653ea64e4](https://github.com/CovertLab/WholeCellEcoliRelease/tree/7e4cc9e57de76752df0f4e32eca95fb653ea64e4) you basically need to use the [Docker](systems-programming.md#docker-software) image on [Ubuntu](systems-programming.md#ubuntu) 21.04 due to [pip](programming-language.md#pip-package-manager) breaking changes... (not their fault). Perhaps [pyenv](programming-language.md#pyenv) would solve things, but who has the patience for that?!?!

The Docker setup from README does just work. The image download is a bit tedius, as it requires you to create a GitHub API key as described in the README, but there must be reasons for that.

Once the image is downloaded, you really want to run is from the root of the source tree:
```
sudo docker run --name=wcm -it -v "$(pwd):/wcEcoli" docker.pkg.github.com/covertlab/wholecellecolirelease/wcm-full
```
This mounts the host source under `/wcEcoli`, so you can easily edit and view output images from your host. Once inside Docker we can compile, run the simulation, and analyze results with:
```
make clean compile &&
python runscripts/manual/runFitter.py &&
python runscripts/manual/runSim.py &&
python runscripts/manual/analysisVariant.py &&
python runscripts/manual/analysisCohort.py &&
python runscripts/manual/analysisMultigen.py &&
python runscripts/manual/analysisSingle.py
```
The meaning of each of the analysis commands is described at [Section 2. "Output overview"](#output-overview).

As a [Docker](systems-programming.md#docker-software) refresher, after you stop the container, e.g. by restarting your computer or running `sudo docker stop wcm`, you can get back into it with:
```
sudo docker start wcm
sudo docker run -it wcm bash
```

`runscripts/manual/runFitter.py` takes about 15 minutes, and it generates files such as `reconstruction/ecoli/dataclasses/process/two_component_system.py` ([related](https://github.com/CovertLab/WholeCellEcoliRelease/issues/20)) which is required to run the simulation, it is basically a part of the build.

`runSim.py` does the main simulation, progress output contains lines of type:
```
Time (s)  Dry mass     Dry mass      Protein          RNA    Small mol     Expected
              (fg)  fold change  fold change  fold change  fold change  fold change
========  ========  ===========  ===========  ===========  ===========  ===========
    0.00    403.09        1.000        1.000        1.000        1.000        1.000
    0.20    403.18        1.000        1.000        1.000        1.000        1.000
```
and then it ended on the [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017) at:
```
 2569.18    783.09        1.943        1.910        2.005        1.950        1.963

Simulation finished:
 - Length: 0:42:49
 - Runtime: 0:09:13
```
when the cell had almost doubled, and presumably divided in 42 minutes of simulated time, which could make sense compared to the 20 under optimal conditions.

## Output overview

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

Run output is placed under `out/`:

Some of the output data is stored as `.cpickle` files. To observe those files, you need the original Python classes, and therefore you have to be inside Docker, from the host it won't work.

We can list all the plots that have been produced under `out/` with
```
find -name '*.png'
```
Plots are also available in [SVG](computer.md#scalable-vector-graphics) and [PDF](computer.md#pdf) formats, e.g.:
- [PNG](computer.md#portable-network-graphics): `./out/manual/plotOut/low_res_plots/massFractionSummary.png`
- [SVG](computer.md#scalable-vector-graphics): `./out/manual/plotOut/svg_plots/massFractionSummary.svg` The SVGs write text as polygons, see also: [SVG fonts](computer.md#svg-fonts).
- [PDF](computer.md#pdf): `./out/manual/plotOut/massFractionSummary.pdf`

The output directory has a hierarchical structure of type:
```
./out/manual/wildtype_000000/000000/generation_000000/000000/
```
where:
- `wildtype_000000`: variant conditions. `wildtype` is a human readable label, and `000000` is an index amongst the possible `wildtype` conditions. For example, we can have different simulations with different nutrients, or different [DNA](dna.md) sequences. An example of this is shown at [run variants](#run-variants).
- `000000`: initial random seed for the initial cell, likely fed to [NumPy](programming-language.md#numpy)'s `np.random.seed`
- `genereation_000000`: this will increase with generations if we simulate multiple cells, which is supported by the model
- `000000`: this will presumably contain the cell index within a generation

We also understand that some of the top level directories contain summaries over all cells, e.g. the `massFractionSummary.pdf` plot exists at several levels of the hierarchy:
```
./out/manual/plotOut/massFractionSummary.pdf
./out/manual/wildtype_000000/plotOut/massFractionSummary.pdf
./out/manual/wildtype_000000/000000/plotOut/massFractionSummary.pdf
./out/manual/wildtype_000000/000000/generation_000000/000000/plotOut/massFractionSummary.pdf
```

Each of thoes four levels of `plotOut` is generated by a different one of the analysis scripts:
- `./out/manual/plotOut`: generated by `python runscripts/manual/analysisVariant.py`. Contains comparisons of different variant conditions. We confirm this by looking at the results of [run variants](#run-variants).
- `./out/manual/wildtype_000000/plotOut`: generated by `python runscripts/manual/analysisCohort.py --variant_index 0`. TODO not sure how to differentiate between two different labels e.g. `wildtype_000000` and `somethingElse_000000`. If `-v` is not given, a it just picks the first one alphabetically. TODO not sure how to automatically generate all of those plots without inspecting the directories.
- `./out/manual/wildtype_000000/000000/plotOut`: generated by `python runscripts/manual/analysisMultigen.py --variant_index 0 --seed 0`
- `./out/manual/wildtype_000000/000000/generation_000000/000000/plotOut`: generated by `python runscripts/manual/analysisSingle.py --variant_index 0 --seed 0 --generation 0 --daughter 0`. Contains information about a single specific cell.

### Mass fraction summary plot analysis

↑ **Parent:** [Output overview](#output-overview)

Let's look into a sample plot, `out/manual/plotOut/svg_plots/massFractionSummary.svg`, and try to understand as much as we can about what it means and how it was generated.

This plot contains how much of each type of mass is present in all cells. Since we simulated just one cell, it will be the same as the results for that cell.

We can see that all of them grow more or less [linearly](linear-algebra.md#linear-function), perhaps as the start of an exponential. We can see that all of them grow more or less linearly, perhaps as the start of an exponential. We can see that all of them grow more or less linearly, perhaps as the start of an exponential.
- total dry mass (mass excluding [water](chemistry.md#water))
- [protein](protein.md) mass
- [rRNA](cell.md#ribosomal-rna) mass
- [mRNA](dna.md#messenger-rna) mass
- [DNA](dna.md) mass. The last label is not very visible on the plots, but we can deduce it from the source code.
By grepping the title "Cell mass fractions" in the source code, we see the files:
```
models/ecoli/analysis/cohort/massFractionSummary.py
models/ecoli/analysis/multigen/massFractionSummary.py
models/ecoli/analysis/variant/massFractionSummary.py
```
which must correspond to the different `massFractionSummary` plots throughout different levels of the hierarchy.

By reading `models/ecoli/analysis/variant/massFractionSummary.py` a little bit, we see that:
- the plotting is done with [Matplotlib](software.md#matplotlib), hurray
- it is reading its data from files under `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/`, more precisely `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/columns/<column-name>/data`. They are binary files however.

  Looking at the source for `wholecell/io/tablereader.py` shows that those are just a standard [NumPy](programming-language.md#numpy) serialization mechanism. Maybe they should have used the [Hierarchical Data Format](computer.md#hierarchical-data-format) instead.

  We can also take this opportunity to try and find where the data is coming from. `Mass` from the `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/` looks like an ID, so we [`grep`](systems-programming.md#grep) that and we reach `models/ecoli/listeners/mass.py`.

  From this we understand that all data that is to be saved from a simulation must be coming from listeners: likely nothing, or not much, is dumped by default, because otherwise it would take up too much disk space. You have to explicitly say what it is that you want to save via a listener that acts on each time step.

<a id="image-minimal-condition-mass-fraction-plot"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/9/94/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_mass_fraction_summary.svg" alt="" height="600">

**[Figure 1](#image-minimal-condition-mass-fraction-plot). Minimal condition mass fraction plot**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_mass_fraction_summary.svg). File name: `out/manual/plotOut/svg_plots/massFractionSummary.svg`

More plot types will be explored at [time series run variant](#time-series-run-variant), where we will contrast two runs with different [growth mediums](cell.md#growth-medium).

## Run variants

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

It would be boring if we could only simulate the same condition all the time, so let's have a look at the different [boundary conditions](calculus.md#boundary-condition) that we can apply to the cell!

We are able to alter things like the composition of the external medium, and the genome of the bacteria, which will make the bacteria behave differently.

The variant selection is a bit cumbersome as we have to use indexes instead of names, but one you know what you are doing, it is fine.

Of course, genetic modification is limited only to experimentally known protein interactions due to the intractability of [computational protein folding](protein.md#computational-protein-folding) and [computational chemistry](physics.md#computational-chemistry) in general, solving those would bsai.

### Default run variant

↑ **Parent:** [Run variants](#run-variants)

The default run variant, if you don't pass any options, just has the minimal growth conditions set. What this means can be seen at [condition](#condition).

Notably, this implies a [growth medium](cell.md#growth-medium) that includes [glucose](chemistry.md#glucose) and [salt](chemistry.md#salt-chemistry). It also includes [oxygen](chemistry.md#oxygen), which is not strictly required, but greatly benefits cell growth, and is of course easier to have than not have as it is part of the atmosphere!

But the medium does not include [amino acids](protein.md#amino-acid), which the bacteria will have to produce by itself.

### Time series run variant

↑ **Parent:** [Run variants](#run-variants)

To modify the nutrients as a function of time, with To select a time series we can use something like:
```
python runscripts/manual/runSim.py --variant nutrientTimeSeries 25 25
```
As mentioned in `python runscripts/manual/runSim.py --help`, `nutrientTimeSeries` is one of the choices from [https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/models/ecoli/sim/variants/__init__.py#L57](https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/models/ecoli/sim/variants/__init__.py#L57)

`25 25` means to start from index 25 and also end at 25, so running just one simulation. `25 27` would run 25 then 26 and then 27 for example.

The timeseries with index 25 is `reconstruction/ecoli/flat/condition/timeseries/000025_cut_aa.tsv` and contains
```
"time (units.s)" "nutrients"
0 "minimal_plus_amino_acids"
1200 "minimal"
```
so we understand that it starts with extra [amino acids](protein.md#amino-acid) in the medium, which benefit the cell, and half way through those are removed at time 1200s = 20 minutes. We would therefore expect the cell to start expressing amino acid production genes exactly at that point.

`nutrients` likely means `condition` in that file however, see bug report with `1 1` failing:  [https://github.com/CovertLab/WholeCellEcoliRelease/issues/24](https://github.com/CovertLab/WholeCellEcoliRelease/issues/24)

When we do this the simulation ends in:
```
Simulation finished:
 - Length: 0:34:23
 - Runtime: 0:08:03
```
so we see that the doubling time was faster than the one with minimal conditions of `0:42:49`, which makes sense, since during the first 20 minutes the cell had extra [amino acid](protein.md#amino-acid) nutrients at its disposal.

The output directory now contains simulation output data under `out/manual/nutrientTimeSeries_000025/`. Let's run analysis and plots for that:
```
python runscripts/manual/analysisVariant.py &&
python runscripts/manual/analysisCohort.py --variant 25 &&
python runscripts/manual/analysisMultigen.py --variant 25 &&
python runscripts/manual/analysisSingle.py --variant 25
```

We can now compare the outputs of this run to the default `wildtype_000000` run from [Section 1. "Install and first run"](#install-and-first-run).

- `out/manual/plotOut/svg_plots/massFractionSummary.svg`: because we now have two variants in the same `out/` folder, `wildtype_000000` and `nutrientTimeSeries_000025`, we now see a side by side comparision of both on the same graph!

  The run variant where we started with amino acids initially grows faster as expected, because the cell didn't have to make it's own amino acids, so growth is a bit more efficient.

  Then, at 20 minutes, which is about 0.3 hours, we see that the cell starts growing a bit less fast as the slope of the curve decreases a bit, because we removed that free amino acid supply.

  <a id="image-minimal-condition-vs-amino-acid-cut-mass-fraction-plot"></a>
  <img src="https://upload.wikimedia.org/wikipedia/commons/5/5f/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_mass_fraction_summary.svg" alt="" height="600">

  **[Figure 2](#image-minimal-condition-vs-amino-acid-cut-mass-fraction-plot). Minimal condition vs amino acid cut mass fraction plot**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_mass_fraction_summary.svg). From file `out/manual/plotOut/svg_plots/massFractionSummary.svg`.

The following plots from under `out/manual/wildtype_000000/000000/{generation_000000,nutrientTimeSeries_000025}/000000/plotOut/svg_plots` have been manually joined side-by-side with:
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

**[Figure 3](#image-amino-acid-counts). Amino acid counts**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_acids_amino_acid_counts.svg). `aaCounts.svg`:
- default: quantities just increase
- amino acid cut: there is an abrupt fall at 20 minutes when we cut off external supply, presumably because it takes some time for the cell to start producing its own

---

<a id="image-external-exchange-fluxes-of-amino-acids"></a>


<img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes_of_amino_acids.svg" alt="" height="800">

**[Figure 4](#image-external-exchange-fluxes-of-amino-acids). External exchange fluxes of amino acids**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes_of_amino_acids.svg). `aaExchangeFluxes.svg`:
- default: no exchanges
- amino acid cut: for all graphs except [phenylalanine](protein.md#phenylalanine) (PHE), either the cell was intaking the AA (negative flux), and that intake goes to 0 when the supply is cut, or the flux is always 0.

  For PHE however, the flux is at all times, except shortly after the cut. Why? And why there was no excretion on the default conditions?

---

<a id="image-evaluation-time"></a>


![](https://upload.wikimedia.org/wikipedia/commons/d/d6/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_evaluation_time.svg)

**[Figure 5](#image-evaluation-time). Evaluation time**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_evaluation_time.svg). `evaluationTime.svg`: this has nothing to do with biology, but it is rather a [profile](software.md#profiling-computer-programming) of the program runtime. We can see that the simulation gets slower and slower as time passes, presumably because there are more and more molecules to simulate.

<a id="image-mrna-count-of-highly-expressed-mrnas"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_mrna_count_of_highly_expressed_mRNAs.svg" alt="" height="800">

**[Figure 6](#image-mrna-count-of-highly-expressed-mrnas). mRNA count of highly expressed mRNAs**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_mrna_count_of_highly_expressed_mRNAs.svg). From file `expression_rna_03_high.svg`. Each of the entries is a [gene](dna.md#gene) using the conventional gene naming convention of `xyzW`, e.g. here's the [BioCyc](biology.md#biocyc) for the first entry, `tufA`: [https://biocyc.org/gene?orgid=ECOLI&id=EG11036](https://biocyc.org/gene?orgid=ECOLI&id=EG11036), which comments > Elongation factor Tu (EF-Tu) is the most abundant protein in E. coli.

 and > In E. coli, EF-Tu is encoded by two genes, tufA and tufB

. What they seem to mean is that tufA and tufB are two similar molecules, either of which can make up the [EF-Tu](cell.md#ef-tu) of the [E. Coli](taxonomy.md#escherichia-coli), which is an important part of [translation](cell.md#translation-biology).

---

<a id="image-external-exchange-fluxes"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/4/49/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes.svg" alt="" height="1000">

**[Figure 7](#image-external-exchange-fluxes). External exchange fluxes**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes.svg). `mediaExcange.svg`: this one is similar to `aaExchangeFluxes.svg`, but it also tracks other substances. The color version makes it easier to squeeze more substances in a given space, but you lose the shape of curves a bit. The title seems reversed: red must be excretion, since that's where [glucose](chemistry.md#glucose) (GLC) is.

The substances are different between the default and amino acid cut graphs, they seem to be the most exchanged substances. On the amino cut graph, first we see the cell intaking most (except [phenylalanine](protein.md#phenylalanine), which is excreted for some reason). When we cut amino acids, the uptake of course stops.

---

## Other run variants

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

Besides [time series run variants](#time-series-run-variant), conditions can also be selected directly without a time series as in:
```
python runscripts/manual/runSim.py --variant condition 1 1
```
which select row indices from `reconstruction/ecoli/flat/condition/condition_defs.tsv`. The above `1 1` would mean the second line of that file which starts with:
```
"condition" "nutrients" "genotype perturbations" "doubling time (units.min)" "active TFs"
"basal" "minimal" {} 44.0 []
"no_oxygen" "minimal_minus_oxygen" {} 100.0 []
"with_aa" "minimal_plus_amino_acids" {} 25.0 ["CPLX-125", "MONOMER0-162", "CPLX0-7671", "CPLX0-228", "MONOMER0-155"]
```
so `1` means `no_oxygen`.

## Source code overview

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

The key model database is located in the source code at `reconstruction/ecoli/flat`.

Let's try to understand some interesting looking, with a special focus on our understanding of the tiny [E. Coli K-12 MG1655 operon thrLABC](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc) part of the metabolism, which we have well understood at [Section "E. Coli K-12 MG1655 operon thrLABC"](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc).

We'll realize that a lot of data and IDs come from/match [BioCyc](biology.md#biocyc) quite closely.

- `reconstruction/ecoli/flat/compartments.tsv` contains [cellular compartment](cell.md#cellular-compartment) information:
  ```
  "abbrev" "id"
  "n" "CCO-BAC-NUCLEOID"
  "j" "CCO-CELL-PROJECTION"
  "w" "CCO-CW-BAC-NEG"
  "c" "CCO-CYTOSOL"
  "e" "CCO-EXTRACELLULAR"
  "m" "CCO-MEMBRANE"
  "o" "CCO-OUTER-MEM"
  "p" "CCO-PERI-BAC"
  "l" "CCO-PILUS"
  "i" "CCO-PM-BAC-NEG"
  ```


  - `CCO`: "Celular COmpartment"
  - `BAC-NUCLEOID`: [nucleoid](cell.md#nucleoid)
  - `CELL-PROJECTION`: [cell projection](cell.md#cell-projection)
  - `CW-BAC-NEG`: TODO confirm: [cell wall](cell.md#cell-wall) (of a [Gram-negative bacteria](taxonomy.md#gram-negative-bacteria))
  - `CYTOSOL`: [cytosol](cell.md#cytosol)
  - `EXTRACELLULAR`: outside the cell
  - `MEMBRANE`: [cell membrane](cell.md#cell-membrane)
  - `OUTER-MEM`: [bacterial outer membrane](taxonomy.md#bacterial-outer-membrane)
  - `PERI-BAC`: [periplasm](taxonomy.md#periplasm)
  - `PILUS`: [pilus](cell.md#pilus)
  - `PM-BAC-NEG`: TODO: [plasma membrane](cell.md#organelle), but that is the same as [cell membrane](cell.md#cell-membrane) no?
- `reconstruction/ecoli/flat/promoters.tsv` contains [promoter](dna.md#promoter-genetics) information. Simple file, sample lines:
  ```
  "position" "direction" "id" "name"
  148 "+" "PM00249" "thrLp"
  ```

  corresponds to [E. Coli K-12 MG1655 promoter thrLp](taxonomy.md#e-coli-k-12-mg1655-promoter-thrlp), which starts as position 148.
- `reconstruction/ecoli/flat/proteins.tsv` contains [protein](protein.md) information. Sample line corresponding to [e. Coli K-12 MG1655 gene thrA](taxonomy.md#e-coli-k-12-mg1655-gene-thra):
  ```
  "aaCount" "name" "seq" "comments" "codingRnaSeq" "mw" "location" "rnaId" "id" "geneId"
  [91, 46, 38, 44, 12, 53, 30, 63, 14, 46, 89, 34, 23, 30, 29, 51, 34, 4, 20, 0, 69] "ThrA" "MRVL..." "Location information from Ecocyc dump." "AUGCGAGUGUUG..." [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 89103.51099999998, 0.0, 0.0, 0.0, 0.0] ["c"] "EG10998_RNA" "ASPKINIHOMOSERDEHYDROGI-MONOMER" "EG10998"
  ```

  so we understand that:
  - `aaCount`: [amino acid](protein.md#amino-acid) count, how many of each of the 20 [proteinogenic amino acid](protein.md#proteinogenic-amino-acid) are there
  - `seq`: full sequence, using the single letter abbreviation of the [proteinogenic amino acids](protein.md#proteinogenic-amino-acid)
  - `mw`; molecular weight? The 11 components appear to be given at `reconstruction/ecoli/flat/scripts/unifyBulkFiles.py`:
    ```
    molecular_weight_keys = [
      '23srRNA',
      '16srRNA',
      '5srRNA',
      'tRNA',
      'mRNA',
      'miscRNA',
      'protein',
      'metabolite',
      'water',
      'DNA',
      'RNA' # nonspecific RNA
      ]
    ```

    so they simply classify the weight? Presumably this exists for complexes that have multiple classes?
    - `23srRNA`, `16srRNA`, `5srRNA` are the three structural [RNAs](dna.md#rna) present in the [ribosome](cell.md#ribosome): [23S ribosomal RNA](cell.md#23s-ribosomal-rna), [16S ribosomal RNA](cell.md#16s-ribosomal-rna), [5S ribosomal RNA](cell.md#5s-ribosomal-rna), all others are obvious:
    - [tRNA](cell.md#transfer-rna)
    - [mRNA](dna.md#messenger-rna)
    - [protein](protein.md). This is the seventh class, and this enzyme only contains mass in this class as expected.
    - [metabolite](molecular-biology.md#metabolite)
    - [water](chemistry.md#water)
    - [DNA](dna.md)
    - [RNA](dna.md#rna): TODO `rna` vs `miscRNA`
  - `location`: [cell compartment](cell.md#cellular-compartment) where the protein is present, `c` defined at `reconstruction/ecoli/flat/compartments.tsv` as [cytoplasm](cell.md#cytoplasm), as expected for something that will make an [amino acid](protein.md#amino-acid)
- `reconstruction/ecoli/flat/rnas.tsv`: TODO vs `transcriptionUnits.tsv`. Sample lines:
  ```
  "halfLife" "name" "seq" "type" "modifiedForms" "monomerId" "comments" "mw" "location" "ntCount" "id" "geneId" "microarray expression"
  174.0 "ThrA [RNA]" "AUGCGAGUGUUG..." "mRNA" [] "ASPKINIHOMOSERDEHYDROGI-MONOMER" "" [0.0, 0.0, 0.0, 0.0, 790935.00399999996, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0] ["c"] [553, 615, 692, 603] "EG10998_RNA" "EG10998" 0.0005264904
  ```


  - `halfLife`: [half-life](particle-physics.md#half-life)
  - `mw`: molecular weight, same as in `reconstruction/ecoli/flat/proteins.tsv`. This [molecule](quantum-mechanics.md#molecule) only have weight in the `mRNA` class, as expected, as it just codes for a protein
  - `location`: same as in `reconstruction/ecoli/flat/proteins.tsv`
  - `ntCount`: [nucleotide](dna.md#nucleotide) count for each of the ATGC
  - `microarray expression`: presumably refers to [DNA microarray](dna.md#dna-microarray) for [gene expression profiling](dna.md#gene-expression-profiling), but what measure exactly?
- `reconstruction/ecoli/flat/sequence.fasta`: [FASTA](biology.md#fasta-format) [DNA](dna.md) sequence, first two lines:
  ```
  >E. coli K-12 MG1655 U00096.2 (1 to 4639675 = 4639675 bp)
  AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGCTTCTG
  ```
- `reconstruction/ecoli/flat/transcriptionUnits.tsv`: [transcription units](dna.md#transcription-unit). We can observe for example the two different transcription units of the [E. Coli K-12 MG1655 operon thrLABC](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc) in the lines:
  ```
  "expression_rate" "direction" "right" "terminator_id"  "name"    "promoter_id" "degradation_rate" "id"       "gene_id"                                   "left"
  0.0               "f"         310     ["TERM0-1059"]   "thrL"    "PM00249"     0.198905992329492 "TU0-42486" ["EG11277"]                                  148
  657.057317358791  "f"         5022    ["TERM_WC-2174"] "thrLABC" "PM00249"     0.231049060186648 "TU00178"   ["EG10998", "EG10999", "EG11000", "EG11277"] 148
  ```


  - `promoter_id`: matches promoter id in `reconstruction/ecoli/flat/promoters.tsv`
  - `gene_id`: matches id in `reconstruction/ecoli/flat/genes.tsv`
  - `id`: matches exactly those used in [BioCyc](biology.md#biocyc), which is quite nice, might be more or less standardized:
    - [https://biocyc.org/ECOLI/NEW-IMAGE?object=TU0-42486](https://biocyc.org/ECOLI/NEW-IMAGE?object=TU0-42486)
    - [https://biocyc.org/ECOLI/NEW-IMAGE?type=OPERON&object=TU00178](https://biocyc.org/ECOLI/NEW-IMAGE?type=OPERON&object=TU00178)
- `reconstruction/ecoli/flat/genes.tsv`
  ```
  "length" "name"                      "seq"             "rnaId"      "coordinate" "direction" "symbol" "type" "id"      "monomerId"
  66       "thr operon leader peptide" "ATGAAACGCATT..." "EG11277_RNA" 189         "+"         "thrL"   "mRNA" "EG11277" "EG11277-MONOMER"
  2463     "ThrA"                      "ATGCGAGTGTTG"    "EG10998_RNA" 336         "+"         "thrA"   "mRNA" "EG10998" "ASPKINIHOMOSERDEHYDROGI-MONOMER"
  ```
- `reconstruction/ecoli/flat/metabolites.tsv` contains [metabolite](molecular-biology.md#metabolite) information. Sample lines:
  ```
  "id"                       "mw7.2" "location"
  "HOMO-SER"                 119.12  ["n", "j", "w", "c", "e", "m", "o", "p", "l", "i"]
  "L-ASPARTATE-SEMIALDEHYDE" 117.104 ["n", "j", "w", "c", "e", "m", "o", "p", "l", "i"]
  ```
  In the case of the enzyme thrA, one of the two reactions it catalyzes is "L-aspartate 4-semialdehyde" into "Homoserine".

  Starting from the enzyme page: [https://biocyc.org/gene?orgid=ECOLI&id=EG10998](https://biocyc.org/gene?orgid=ECOLI&id=EG10998) we reach the reaction page: [https://biocyc.org/ECOLI/NEW-IMAGE?type=REACTION&object=HOMOSERDEHYDROG-RXN](https://biocyc.org/ECOLI/NEW-IMAGE?type=REACTION&object=HOMOSERDEHYDROG-RXN) which has reaction ID `HOMOSERDEHYDROG-RXN`, and that page which clarifies the IDs:
  - [https://biocyc.org/compound?orgid=ECOLI&id=L-ASPARTATE-SEMIALDEHYDE:](https://biocyc.org/compound?orgid=ECOLI&id=L-ASPARTATE-SEMIALDEHYDE:) "L-aspartate 4-semialdehyde" has ID `L-ASPARTATE-SEMIALDEHYDE`
  - [https://biocyc.org/compound?orgid=ECOLI&id=HOMO-SER:](https://biocyc.org/compound?orgid=ECOLI&id=HOMO-SER:) "Homoserine" has ID `HOMO-SER`
  so these are the compounds that we care about.
- `reconstruction/ecoli/flat/reactions.tsv` contains [chemical reaction](chemistry.md#chemical-reaction) information. Sample lines:
  ```
  "reaction id" "stoichiometry" "is reversible" "catalyzed by"

  "HOMOSERDEHYDROG-RXN-HOMO-SER/NAD//L-ASPARTATE-SEMIALDEHYDE/NADH/PROTON.51."
    {"NADH[c]": -1, "PROTON[c]": -1, "HOMO-SER[c]": 1, "L-ASPARTATE-SEMIALDEHYDE[c]": -1, "NAD[c]": 1}
    false
    ["ASPKINIIHOMOSERDEHYDROGII-CPLX", "ASPKINIHOMOSERDEHYDROGI-CPLX"]

  "HOMOSERDEHYDROG-RXN-HOMO-SER/NADP//L-ASPARTATE-SEMIALDEHYDE/NADPH/PROTON.53."
    {"NADPH[c]": -1, "NADP[c]": 1, "PROTON[c]": -1, "L-ASPARTATE-SEMIALDEHYDE[c]": -1, "HOMO-SER[c]": 1
    false
    ["ASPKINIIHOMOSERDEHYDROGII-CPLX", "ASPKINIHOMOSERDEHYDROGI-CPLX"]
  ```


  - `catalized by`: here we see `ASPKINIHOMOSERDEHYDROGI-CPLX`, which we can guess is a [protein complex](protein.md#protein-complex) made out of `ASPKINIHOMOSERDEHYDROGI-MONOMER`, which is the ID for the `thrA` we care about! This is confirmed in `complexationReactions.tsv`.
- `reconstruction/ecoli/flat/complexationReactions.tsv` contains information about [chemical reactions](chemistry.md#chemical-reaction) that produce [protein complexes](protein.md#protein-complex):
  ```
  "process" "stoichiometry" "id" "dir"
  "complexation"
    [
      {
        "molecule": "ASPKINIHOMOSERDEHYDROGI-CPLX",
        "coeff": 1,
        "type": "proteincomplex",
        "location": "c",
        "form": "mature"
      },
      {
        "molecule": "ASPKINIHOMOSERDEHYDROGI-MONOMER",
        "coeff": -4,
        "type": "proteinmonomer",
        "location": "c",
        "form": "mature"
      }
    ]
  "ASPKINIHOMOSERDEHYDROGI-CPLX_RXN"
  1
  ```

  The `coeff` is how many monomers need to get together for form the final complex. This can be seen from the Summary section of [https://ecocyc.org/gene?orgid=ECOLI&id=ASPKINIHOMOSERDEHYDROGI-MONOMER](https://ecocyc.org/gene?orgid=ECOLI&id=ASPKINIHOMOSERDEHYDROGI-MONOMER):> Aspartate kinase I / homoserine dehydrogenase I comprises a dimer of ThrA dimers. Although the dimeric form is catalytically active, the binding equilibrium dramatically favors the tetrameric form. The aspartate kinase and homoserine dehydrogenase activities of each ThrA monomer are catalyzed by independent domains connected by a linker region.

  Fantastic literature summary! Can't find that in database form there however.
- `reconstruction/ecoli/flat/proteinComplexes.tsv` contains [protein complex](protein.md#protein-complex) information:
  ```
  "name" "comments" "mw" "location" "reactionId" "id"
  "aspartate kinase / homoserine dehydrogenase"
  ""
  [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 356414.04399999994, 0.0, 0.0, 0.0, 0.0]
  ["c"]
  "ASPKINIHOMOSERDEHYDROGI-CPLX_RXN"
  "ASPKINIHOMOSERDEHYDROGI-CPLX"
  ```
- `reconstruction/ecoli/flat/protein_half_lives.tsv` contains the [half-life](particle-physics.md#half-life) of [proteins](protein.md). Very few proteins are listed however for some reason.
- `reconstruction/ecoli/flat/tfIds.csv`: [transcription factors](dna.md#transcription-factor) information:
  ```
  "TF"   "geneId"  "oneComponentId"  "twoComponentId" "nonMetaboliteBindingId" "activeId" "notes"
  "arcA" "EG10061" "PHOSPHO-ARCA"    "PHOSPHO-ARCA"
  "fnr"  "EG10325" "FNR-4FE-4S-CPLX" "FNR-4FE-4S-CPLX"
  "dksA" "EG10230"
  ```

### Condition

↑ **Parent:** [Source code overview](#source-code-overview)

- `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` contains the nutrients in a minimal environment in which the cell survives:
  ```
  "molecule id" "lower bound (units.mmol / units.g / units.h)" "upper bound (units.mmol / units.g / units.h)"
  "ADP[c]" 3.15 3.15
  "PI[c]" 3.15 3.15
  "PROTON[c]" 3.15 3.15
  "GLC[p]" NaN 20
  "OXYGEN-MOLECULE[p]" NaN NaN
  "AMMONIUM[c]" NaN NaN
  "PI[p]" NaN NaN
  "K+[p]" NaN NaN
  "SULFATE[p]" NaN NaN
  "FE+2[p]" NaN NaN
  "CA+2[p]" NaN NaN
  "CL-[p]" NaN NaN
  "CO+2[p]" NaN NaN
  "MG+2[p]" NaN NaN
  "MN+2[p]" NaN NaN
  "NI+2[p]" NaN NaN
  "ZN+2[p]" NaN NaN
  "WATER[p]" NaN NaN
  "CARBON-DIOXIDE[p]" NaN NaN
  "CPD0-1958[p]" NaN NaN
  "L-SELENOCYSTEINE[c]" NaN NaN
  "GLC-D-LACTONE[c]" NaN NaN
  "CYTOSINE[c]" NaN NaN
  ```
  If we compare that to `reconstruction/ecoli/flat/condition/nutrient/minimal_plus_amino_acids.tsv`, we see that it adds the 20 [amino acids](protein.md#amino-acid) on top of the minimal condition:
  ```
  "L-ALPHA-ALANINE[p]" NaN NaN
  "ARG[p]" NaN NaN
  "ASN[p]" NaN NaN
  "L-ASPARTATE[p]" NaN NaN
  "CYS[p]" NaN NaN
  "GLT[p]" NaN NaN
  "GLN[p]" NaN NaN
  "GLY[p]" NaN NaN
  "HIS[p]" NaN NaN
  "ILE[p]" NaN NaN
  "LEU[p]" NaN NaN
  "LYS[p]" NaN NaN
  "MET[p]" NaN NaN
  "PHE[p]" NaN NaN
  "PRO[p]" NaN NaN
  "SER[p]" NaN NaN
  "THR[p]" NaN NaN
  "TRP[p]" NaN NaN
  "TYR[p]" NaN NaN
  "L-SELENOCYSTEINE[c]" NaN NaN
  "VAL[p]" NaN NaN
  ```
  so we guess that `NaN` in the `upper mound` likely means infinite.

  We can try to understand the less obvious ones:
  - `ADP`: TODO
  - `PI`: TODO
  - `PROTON[c]`: presumably a measure of [pH](chemistry.md#ph)
  - `GLC[p]`: [glucose](chemistry.md#glucose), this can be seen by comparing `minimal.tsv` with `minimal_no_glucose.tsv`
  - `AMMONIUM`: [ammonium](chemistry.md#ammonium). This appears to be the primary source of [nitrogen](chemistry.md#nitrogen) [atoms](chemistry.md#atom) for producing [amino acids](protein.md#amino-acid).
  - `CYTOSINE[c]`: hmmm, why is external [cytosine](dna.md#cytosine) needed? Weird.
- `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/` contains sequences of conditions for each time. For example:
  - `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/000000_basal.tsv` contains:
    ```
    "time (units.s)" "nutrients"
    0 "minimal"
    ```

    which means just using `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` until infinity. That is the default one used by `runSim.py`, as can be seen from `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Environment/attributes/nutrientTimeSeriesLabel` which contains just `000000_basal`.
  - `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/000001_cut_glucose.tsv` is more interesting and contains:
    ```
    "time (units.s)" "nutrients"
    0 "minimal"
    1200 "minimal_no_glucose"
    ```

    so we see that this will shift the conditions half-way to a condition that will eventually kill the bacteria because it will run out of [glucose](chemistry.md#glucose) and thus energy!

  Timeseries can be selected with `--variant nutrientTimeSeries X Y`, see also: [run variants](#run-variants).

  We can use that variant with:
  ```
  VARIANT="condition" FIRST_VARIANT_INDEX=1 LAST_VARIANT_INDEX=1 python runscripts/manual/runSim.py
  ```
- `reconstruction/ecoli/flat/condition/condition_defs.tsv` contains lines of form:
  ```
  "condition" "nutrients"                "genotype perturbations" "doubling time (units.min)" "active TFs"
  "basal"     "minimal"                  {}                       44.0                        []
  "no_oxygen" "minimal_minus_oxygen"     {}                       100.0                       []
  "with_aa"   "minimal_plus_amino_acids" {}                       25.0                        ["CPLX-125", "MONOMER0-162", "CPLX0-7671", "CPLX0-228", "MONOMER0-155"]
  ```


  - `condition` refers to entries in `reconstruction/ecoli/flat/condition/condition_defs.tsv`
  - `nutrients` refers to entries under `reconstruction/ecoli/flat/condition/nutrient/`, e.g. `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` or `reconstruction/ecoli/flat/condition/nutrient/minimal_plus_amino_acids.tsv`
  - `genotype perturbations`: there aren't any in the file, but this suggests that genotype modifications can also be incorporated here
  - `doubling time`: TODO experimental data? Because this should be a simulation output, right? Or do they cheat and fix doubling by time?
  - `active TFs`: this suggests that they are cheating [transcription factors](dna.md#transcription-factor) here, as those would ideally be functions of other more basic inputs

## Model validation

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

TODO compare with actual datasetes.

## Publications

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

Unfortunately, due to lack of [one page to rule them all](cirosantilli-com.md#one-page-to-rule-them-all), the [on-Git tree publication list is meager](https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/docs/README.md#relevant-papers), some of the most relevant ones seems to be:
- 2021 [open access](education.md#open-access) [review paper](education.md#review-article): [https://journals.asm.org/doi/full/10.1128/ecosalplus.ESP-0001-2020](https://journals.asm.org/doi/full/10.1128/ecosalplus.ESP-0001-2020) "The E. coli Whole-Cell Modeling Project". They should just past that stuff in a [README](software.md#readme) :-) The article mentions that it is a follow up to the previous [M. genitalium whole cell model by Covert lab](taxonomy.md#m-genitalium-whole-cell-model-by-covert-lab). Only 43% of known genes modelled at this point however, a shame.
- 2020 under [Science](education.md#science-journal) [paywall](education.md#paywall): [https://www.science.org/doi/10.1126/science.aav3751](https://www.science.org/doi/10.1126/science.aav3751) "Simultaneous cross-evaluation of heterogeneous E. coli datasets via mechanistic simulation"

## ↑ Ancestors (10)

1. [E. Coli whole cell simulation](taxonomy.md#e-coli-whole-cell-simulation)
2. [Escherichia coli](taxonomy.md#escherichia-coli)
3. [List of bacteria](taxonomy.md#list-of-bacteria)
4. [Bacteria](taxonomy.md#bacteria)
5. [Species](taxonomy.md#species)
6. [Taxonomy](taxonomy.md)
7. [Biology](biology.md)
8. [Natural science](science.md#natural-science)
9. [Science](science.md)
10. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (6)

- [The best articles by Ciro Santilli](articles.md)
- [Covert Lab](university.md#covert-lab)
- [Half-life](particle-physics.md#half-life)
- [Exams and homework are useless, only projects matter](how-to-teach.md#exams-and-homework-are-useless-only-projects-matter)
- [M. genitalium whole cell model by Covert lab](taxonomy.md#m-genitalium-whole-cell-model-by-covert-lab)
- [Molecular biology feels like systems programming](systems-programming.md#molecular-biology-feels-like-systems-programming)
