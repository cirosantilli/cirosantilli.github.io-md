# E. Coli Whole Cell Model by Covert Lab

↑ **Parent:** [E. Coli whole cell simulation](taxonomy.md#e-coli-whole-cell-simulation)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles.md)

<a id="_3"></a>
[https://github.com/CovertLab/WholeCellEcoliRelease](https://github.com/CovertLab/WholeCellEcoliRelease) is a [whole cell simulation](cell.md#whole-cell-simulation) model created by [Covert Lab](university.md#covert-lab) and other collaborators.

<a id="_4"></a>
The project is written in [Python](programming-language.md#python-programming-language), hurray!

<a id="_5"></a>
But according to te [README](software.md#readme), it seems to be the use a [code drop](software.md#code-drop) model with on-request access to master. [Ciro Santilli](ciro-santilli.md) asked at [rationale on GitHub discussion](https://github.com/CovertLab/WholeCellEcoliRelease/discussions/23), and they confirmed as expected that it is to:<a id="_6"></a>

<a id="_7"></a>
- to prevent their [publication](education.md#academic-publishing) ideas from being stolen. Who would steal publication ideas with public proof in an issue tracker without crediting original authors? [Academia is broken](education.md#academia-is-broken). Academia should be the most open form of knowledge sharing. But instead we get this silly competition for publication points.
<a id="_8"></a>
- to prevent noise from non-collaborators. But they only get like 2 issues as year on such a meganiche subject... Did you know that you can ignore people, and even block them if they are particularly annoying? Much more likely is that no one will every hear about your project and that it will die with its last graduate student slave.

<a id="_9"></a>
The project is a followup to the earlier [M. genitalium whole cell model by Covert lab](taxonomy.md#m-genitalium-whole-cell-model-by-covert-lab) which modelled [Mycoplasma genitalium](taxonomy.md#mycoplasma-genitalium). [E. Coli](taxonomy.md#escherichia-coli) has 8x more genes (500 vs 4k), but it the undisputed [bacterial](taxonomy.md#bacteria) [model organism](biology.md#model-organism) and as such has been studied much more thoroughly. It also reproduces faster than Mycoplasma (20 minutes vs a few hours), which is a huge advantages for validation/exploratory [experiments](science.md#experiment).

<a id="_10"></a>
The project has a partial dependency on the [proprietary](law.md#proprietary-software) [optimization software](computer-science.md#optimization-software) [CPLEX](computer-science.md#cplex) which is [freeware](law.md#freeware), for students, not sure what it is used for exactly, from the comment in the `requirements.txt` the dependency is only partial.

<a id="_11"></a>
This project makes [Ciro Santilli](ciro-santilli.md) think of the [E. Coli](taxonomy.md#escherichia-coli) as an [optimization problem](computer-science.md#optimization-problem). Given such external nutrient/temperature condition, which [DNA](dna.md) sequence makes the cell grow the fastest? Balancing [metabolites](molecular-biology.md#metabolite) feels like designing a [Factorio](video-game.md#factorio) speedrun.

<a id="_12"></a>
There is one major thing missing thing in the current model: [promoters](dna.md#promoter-genetics)/[transcription factor](dna.md#transcription-factor) interactions are not modelled due to lack/low quality of experimental data: [https://github.com/CovertLab/WholeCellEcoliRelease/issues/21](https://github.com/CovertLab/WholeCellEcoliRelease/issues/21). They just have a magic direct "[transcription factor](dna.md#transcription-factor) to [gene](dna.md#gene)" relationship, encoded at [reconstruction/ecoli/flat/foldChanges.tsv](https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/reconstruction/ecoli/flat/foldChanges.tsv) in terms of type "if this is present, such protein is expressed 10x more". [Transcription units](dna.md#transcription-unit) are not implemented at all it appears.

<a id="_13"></a>
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

<a id="_14"></a>
At [7e4cc9e57de76752df0f4e32eca95fb653ea64e4](https://github.com/CovertLab/WholeCellEcoliRelease/tree/7e4cc9e57de76752df0f4e32eca95fb653ea64e4) you basically need to use the [Docker](systems-programming.md#docker-software) image on [Ubuntu](systems-programming.md#ubuntu) 21.04 due to [pip](programming-language.md#pip-package-manager) breaking changes... (not their fault). Perhaps [pyenv](programming-language.md#pyenv) would solve things, but who has the patience for that?!?!

<a id="_15"></a>
The Docker setup from README does just work. The image download is a bit tedius, as it requires you to create a GitHub API key as described in the README, but there must be reasons for that.

<a id="_16"></a>
Once the image is downloaded, you really want to run is from the root of the source tree:<a id="_17"></a>

```
sudo docker run --name=wcm -it -v "$(pwd):/wcEcoli" docker.pkg.github.com/covertlab/wholecellecolirelease/wcm-full
```
This mounts the host source under `/wcEcoli`, so you can easily edit and view output images from your host. Once inside Docker we can compile, run the simulation, and analyze results with:<a id="_18"></a>

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

<a id="_19"></a>
As a [Docker](systems-programming.md#docker-software) refresher, after you stop the container, e.g. by restarting your computer or running `sudo docker stop wcm`, you can get back into it with:<a id="_20"></a>

```
sudo docker start wcm
sudo docker run -it wcm bash
```

<a id="_21"></a>
`runscripts/manual/runFitter.py` takes about 15 minutes, and it generates files such as `reconstruction/ecoli/dataclasses/process/two_component_system.py` ([related](https://github.com/CovertLab/WholeCellEcoliRelease/issues/20)) which is required to run the simulation, it is basically a part of the build.

<a id="_22"></a>
`runSim.py` does the main simulation, progress output contains lines of type:<a id="_23"></a>

```
Time (s)  Dry mass     Dry mass      Protein          RNA    Small mol     Expected
              (fg)  fold change  fold change  fold change  fold change  fold change
========  ========  ===========  ===========  ===========  ===========  ===========
    0.00    403.09        1.000        1.000        1.000        1.000        1.000
    0.20    403.18        1.000        1.000        1.000        1.000        1.000
```
and then it ended on the [Lenovo ThinkPad P51 (2017)](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017) at:<a id="_24"></a>

```
 2569.18    783.09        1.943        1.910        2.005        1.950        1.963

Simulation finished:
 - Length: 0:42:49
 - Runtime: 0:09:13
```
when the cell had almost doubled, and presumably divided in 42 minutes of simulated time, which could make sense compared to the 20 under optimal conditions.

## Output overview

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

<a id="_25"></a>
Run output is placed under `out/`:

<a id="_26"></a>
Some of the output data is stored as `.cpickle` files. To observe those files, you need the original Python classes, and therefore you have to be inside Docker, from the host it won't work.

<a id="_27"></a>
We can list all the plots that have been produced under `out/` with<a id="_28"></a>

```
find -name '*.png'
```
Plots are also available in [SVG](computer.md#scalable-vector-graphics) and [PDF](computer.md#pdf) formats, e.g.:<a id="_29"></a>

<a id="_30"></a>
- [PNG](computer.md#portable-network-graphics): `./out/manual/plotOut/low_res_plots/massFractionSummary.png`
<a id="_31"></a>
- [SVG](computer.md#scalable-vector-graphics): `./out/manual/plotOut/svg_plots/massFractionSummary.svg` The SVGs write text as polygons, see also: [SVG fonts](computer.md#svg-fonts).
<a id="_32"></a>
- [PDF](computer.md#pdf): `./out/manual/plotOut/massFractionSummary.pdf`

<a id="_33"></a>
The output directory has a hierarchical structure of type:<a id="_34"></a>

```
./out/manual/wildtype_000000/000000/generation_000000/000000/
```
where:<a id="_35"></a>

<a id="_36"></a>
- `wildtype_000000`: variant conditions. `wildtype` is a human readable label, and `000000` is an index amongst the possible `wildtype` conditions. For example, we can have different simulations with different nutrients, or different [DNA](dna.md) sequences. An example of this is shown at [run variants](#run-variants).
<a id="_37"></a>
- `000000`: initial random seed for the initial cell, likely fed to [NumPy](programming-language.md#numpy)'s `np.random.seed`
<a id="_38"></a>
- `genereation_000000`: this will increase with generations if we simulate multiple cells, which is supported by the model
<a id="_39"></a>
- `000000`: this will presumably contain the cell index within a generation

<a id="_40"></a>
We also understand that some of the top level directories contain summaries over all cells, e.g. the `massFractionSummary.pdf` plot exists at several levels of the hierarchy:<a id="_41"></a>

```
./out/manual/plotOut/massFractionSummary.pdf
./out/manual/wildtype_000000/plotOut/massFractionSummary.pdf
./out/manual/wildtype_000000/000000/plotOut/massFractionSummary.pdf
./out/manual/wildtype_000000/000000/generation_000000/000000/plotOut/massFractionSummary.pdf
```

<a id="_42"></a>
Each of thoes four levels of `plotOut` is generated by a different one of the analysis scripts:<a id="_43"></a>

<a id="_44"></a>
- `./out/manual/plotOut`: generated by `python runscripts/manual/analysisVariant.py`. Contains comparisons of different variant conditions. We confirm this by looking at the results of [run variants](#run-variants).
<a id="_45"></a>
- `./out/manual/wildtype_000000/plotOut`: generated by `python runscripts/manual/analysisCohort.py --variant_index 0`. TODO not sure how to differentiate between two different labels e.g. `wildtype_000000` and `somethingElse_000000`. If `-v` is not given, a it just picks the first one alphabetically. TODO not sure how to automatically generate all of those plots without inspecting the directories.
<a id="_46"></a>
- `./out/manual/wildtype_000000/000000/plotOut`: generated by `python runscripts/manual/analysisMultigen.py --variant_index 0 --seed 0`
<a id="_47"></a>
- `./out/manual/wildtype_000000/000000/generation_000000/000000/plotOut`: generated by `python runscripts/manual/analysisSingle.py --variant_index 0 --seed 0 --generation 0 --daughter 0`. Contains information about a single specific cell.

### Mass fraction summary plot analysis

↑ **Parent:** [Output overview](#output-overview)

<a id="_48"></a>
Let's look into a sample plot, `out/manual/plotOut/svg_plots/massFractionSummary.svg`, and try to understand as much as we can about what it means and how it was generated.

<a id="_49"></a>
This plot contains how much of each type of mass is present in all cells. Since we simulated just one cell, it will be the same as the results for that cell.

<a id="_50"></a>
We can see that all of them grow more or less [linearly](linear-algebra.md#linear-function), perhaps as the start of an exponential. We can see that all of them grow more or less linearly, perhaps as the start of an exponential. We can see that all of them grow more or less linearly, perhaps as the start of an exponential.<a id="_51"></a>

<a id="_52"></a>
- total dry mass (mass excluding [water](chemistry.md#water))
<a id="_53"></a>
- [protein](protein.md) mass
<a id="_54"></a>
- [rRNA](cell.md#ribosomal-rna) mass
<a id="_55"></a>
- [mRNA](dna.md#messenger-rna) mass
<a id="_56"></a>
- [DNA](dna.md) mass. The last label is not very visible on the plots, but we can deduce it from the source code.
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
- the plotting is done with [Matplotlib](software.md#matplotlib), hurray
<a id="_61"></a>
- <a id="_62"></a>
  it is reading its data from files under `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/`, more precisely `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/columns/<column-name>/data`. They are binary files however.

  <a id="_63"></a>
  Looking at the source for `wholecell/io/tablereader.py` shows that those are just a standard [NumPy](programming-language.md#numpy) serialization mechanism. Maybe they should have used the [Hierarchical Data Format](computer.md#hierarchical-data-format) instead.

  <a id="_64"></a>
  We can also take this opportunity to try and find where the data is coming from. `Mass` from the `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Mass/` looks like an ID, so we [`grep`](systems-programming.md#grep) that and we reach `models/ecoli/listeners/mass.py`.

  <a id="_65"></a>
  From this we understand that all data that is to be saved from a simulation must be coming from listeners: likely nothing, or not much, is dumped by default, because otherwise it would take up too much disk space. You have to explicitly say what it is that you want to save via a listener that acts on each time step.

<a id="image-minimal-condition-mass-fraction-plot"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/9/94/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_mass_fraction_summary.svg" alt="" height="600">

**[Figure 1](#image-minimal-condition-mass-fraction-plot). Minimal condition mass fraction plot**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_mass_fraction_summary.svg). File name: `out/manual/plotOut/svg_plots/massFractionSummary.svg`

<a id="_66"></a>
More plot types will be explored at [time series run variant](#time-series-run-variant), where we will contrast two runs with different [growth mediums](cell.md#growth-medium).

## Run variants

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

<a id="_67"></a>
It would be boring if we could only simulate the same condition all the time, so let's have a look at the different [boundary conditions](calculus.md#boundary-condition) that we can apply to the cell!

<a id="_68"></a>
We are able to alter things like the composition of the external medium, and the genome of the bacteria, which will make the bacteria behave differently.

<a id="_69"></a>
The variant selection is a bit cumbersome as we have to use indexes instead of names, but one you know what you are doing, it is fine.

<a id="_70"></a>
Of course, genetic modification is limited only to experimentally known protein interactions due to the intractability of [computational protein folding](protein.md#computational-protein-folding) and [computational chemistry](physics.md#computational-chemistry) in general, solving those would bsai.

### Default run variant

↑ **Parent:** [Run variants](#run-variants)

<a id="_71"></a>
The default run variant, if you don't pass any options, just has the minimal growth conditions set. What this means can be seen at [condition](#condition).

<a id="_72"></a>
Notably, this implies a [growth medium](cell.md#growth-medium) that includes [glucose](chemistry.md#glucose) and [salt](chemistry.md#salt-chemistry). It also includes [oxygen](chemistry.md#oxygen), which is not strictly required, but greatly benefits cell growth, and is of course easier to have than not have as it is part of the atmosphere!

<a id="_73"></a>
But the medium does not include [amino acids](protein.md#amino-acid), which the bacteria will have to produce by itself.

### Time series run variant

↑ **Parent:** [Run variants](#run-variants)

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
so we understand that it starts with extra [amino acids](protein.md#amino-acid) in the medium, which benefit the cell, and half way through those are removed at time 1200s = 20 minutes. We would therefore expect the cell to start expressing amino acid production genes exactly at that point.

<a id="_79"></a>
`nutrients` likely means `condition` in that file however, see bug report with `1 1` failing:  [https://github.com/CovertLab/WholeCellEcoliRelease/issues/24](https://github.com/CovertLab/WholeCellEcoliRelease/issues/24)

<a id="_80"></a>
When we do this the simulation ends in:<a id="_81"></a>

```
Simulation finished:
 - Length: 0:34:23
 - Runtime: 0:08:03
```
so we see that the doubling time was faster than the one with minimal conditions of `0:42:49`, which makes sense, since during the first 20 minutes the cell had extra [amino acid](protein.md#amino-acid) nutrients at its disposal.

<a id="_82"></a>
The output directory now contains simulation output data under `out/manual/nutrientTimeSeries_000025/`. Let's run analysis and plots for that:<a id="_83"></a>

```
python runscripts/manual/analysisVariant.py &&
python runscripts/manual/analysisCohort.py --variant 25 &&
python runscripts/manual/analysisMultigen.py --variant 25 &&
python runscripts/manual/analysisSingle.py --variant 25
```

<a id="_84"></a>
We can now compare the outputs of this run to the default `wildtype_000000` run from [Section 1. "Install and first run"](#install-and-first-run).

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
  amino acid cut: for all graphs except [phenylalanine](protein.md#phenylalanine) (PHE), either the cell was intaking the AA (negative flux), and that intake goes to 0 when the supply is cut, or the flux is always 0.

  <a id="_100"></a>
  For PHE however, the flux is at all times, except shortly after the cut. Why? And why there was no excretion on the default conditions?

---

<a id="image-evaluation-time"></a>


![](https://upload.wikimedia.org/wikipedia/commons/d/d6/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_evaluation_time.svg)

**[Figure 5](#image-evaluation-time). Evaluation time**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_evaluation_time.svg). `evaluationTime.svg`: this has nothing to do with biology, but it is rather a [profile](software.md#profiling-computer-programming) of the program runtime. We can see that the simulation gets slower and slower as time passes, presumably because there are more and more molecules to simulate.

<a id="image-mrna-count-of-highly-expressed-mrnas"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_mrna_count_of_highly_expressed_mRNAs.svg" alt="" height="800">

**[Figure 6](#image-mrna-count-of-highly-expressed-mrnas). mRNA count of highly expressed mRNAs**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_mrna_count_of_highly_expressed_mRNAs.svg). From file `expression_rna_03_high.svg`. Each of the entries is a [gene](dna.md#gene) using the conventional gene naming convention of `xyzW`, e.g. here's the [BioCyc](biology.md#biocyc) for the first entry, `tufA`: [https://biocyc.org/gene?orgid=ECOLI&id=EG11036](https://biocyc.org/gene?orgid=ECOLI&id=EG11036), which comments <a id="_101"></a>
> Elongation factor Tu (EF-Tu) is the most abundant protein in E. coli.

 and <a id="_102"></a>
> In E. coli, EF-Tu is encoded by two genes, tufA and tufB

. What they seem to mean is that tufA and tufB are two similar molecules, either of which can make up the [EF-Tu](cell.md#ef-tu) of the [E. Coli](taxonomy.md#escherichia-coli), which is an important part of [translation](cell.md#translation-biology).

---

<a id="image-external-exchange-fluxes"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/4/49/E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes.svg" alt="" height="1000">

**[Figure 7](#image-external-exchange-fluxes). External exchange fluxes**. [Source](https://commons.wikimedia.org/wiki/File:E._Coli_Whole_Cell_model_by_Covert_Lab_minimal_nutrients_vs_cut_amino_external_exchange_fluxes.svg). <a id="_103"></a>
`mediaExcange.svg`: this one is similar to `aaExchangeFluxes.svg`, but it also tracks other substances. The color version makes it easier to squeeze more substances in a given space, but you lose the shape of curves a bit. The title seems reversed: red must be excretion, since that's where [glucose](chemistry.md#glucose) (GLC) is.

<a id="_104"></a>
The substances are different between the default and amino acid cut graphs, they seem to be the most exchanged substances. On the amino cut graph, first we see the cell intaking most (except [phenylalanine](protein.md#phenylalanine), which is excreted for some reason). When we cut amino acids, the uptake of course stops.

---

## Other run variants

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

<a id="_105"></a>
Besides [time series run variants](#time-series-run-variant), conditions can also be selected directly without a time series as in:<a id="_106"></a>

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

## Source code overview

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

<a id="_108"></a>
The key model database is located in the source code at `reconstruction/ecoli/flat`.

<a id="_109"></a>
Let's try to understand some interesting looking, with a special focus on our understanding of the tiny [E. Coli K-12 MG1655 operon thrLABC](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc) part of the metabolism, which we have well understood at [Section "E. Coli K-12 MG1655 operon thrLABC"](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc).

<a id="_110"></a>
We'll realize that a lot of data and IDs come from/match [BioCyc](biology.md#biocyc) quite closely.

<a id="_111"></a>
<a id="_112"></a>
- <a id="_113"></a>
  `reconstruction/ecoli/flat/compartments.tsv` contains [cellular compartment](cell.md#cellular-compartment) information:<a id="_114"></a>

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

  <a id="_115"></a>

  <a id="_116"></a>
  - `CCO`: "Celular COmpartment"
  <a id="_117"></a>
  - `BAC-NUCLEOID`: [nucleoid](cell.md#nucleoid)
  <a id="_118"></a>
  - `CELL-PROJECTION`: [cell projection](cell.md#cell-projection)
  <a id="_119"></a>
  - `CW-BAC-NEG`: TODO confirm: [cell wall](cell.md#cell-wall) (of a [Gram-negative bacteria](taxonomy.md#gram-negative-bacteria))
  <a id="_120"></a>
  - `CYTOSOL`: [cytosol](cell.md#cytosol)
  <a id="_121"></a>
  - `EXTRACELLULAR`: outside the cell
  <a id="_122"></a>
  - `MEMBRANE`: [cell membrane](cell.md#cell-membrane)
  <a id="_123"></a>
  - `OUTER-MEM`: [bacterial outer membrane](taxonomy.md#bacterial-outer-membrane)
  <a id="_124"></a>
  - `PERI-BAC`: [periplasm](taxonomy.md#periplasm)
  <a id="_125"></a>
  - `PILUS`: [pilus](cell.md#pilus)
  <a id="_126"></a>
  - `PM-BAC-NEG`: TODO: [plasma membrane](cell.md#organelle), but that is the same as [cell membrane](cell.md#cell-membrane) no?
<a id="_127"></a>
- `reconstruction/ecoli/flat/promoters.tsv` contains [promoter](dna.md#promoter-genetics) information. Simple file, sample lines:<a id="_128"></a>

  ```
  "position" "direction" "id" "name"
  148 "+" "PM00249" "thrLp"
  ```

  corresponds to [E. Coli K-12 MG1655 promoter thrLp](taxonomy.md#e-coli-k-12-mg1655-promoter-thrlp), which starts as position 148.
<a id="_129"></a>
- `reconstruction/ecoli/flat/proteins.tsv` contains [protein](protein.md) information. Sample line corresponding to [e. Coli K-12 MG1655 gene thrA](taxonomy.md#e-coli-k-12-mg1655-gene-thra):<a id="_130"></a>

  ```
  "aaCount" "name" "seq" "comments" "codingRnaSeq" "mw" "location" "rnaId" "id" "geneId"
  [91, 46, 38, 44, 12, 53, 30, 63, 14, 46, 89, 34, 23, 30, 29, 51, 34, 4, 20, 0, 69] "ThrA" "MRVL..." "Location information from Ecocyc dump." "AUGCGAGUGUUG..." [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 89103.51099999998, 0.0, 0.0, 0.0, 0.0] ["c"] "EG10998_RNA" "ASPKINIHOMOSERDEHYDROGI-MONOMER" "EG10998"
  ```

  so we understand that:<a id="_131"></a>

  <a id="_132"></a>
  - `aaCount`: [amino acid](protein.md#amino-acid) count, how many of each of the 20 [proteinogenic amino acid](protein.md#proteinogenic-amino-acid) are there
  <a id="_133"></a>
  - `seq`: full sequence, using the single letter abbreviation of the [proteinogenic amino acids](protein.md#proteinogenic-amino-acid)
  <a id="_134"></a>
  - `mw`; molecular weight? The 11 components appear to be given at `reconstruction/ecoli/flat/scripts/unifyBulkFiles.py`:<a id="_135"></a>

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

    so they simply classify the weight? Presumably this exists for complexes that have multiple classes?<a id="_136"></a>

    <a id="_137"></a>
    - `23srRNA`, `16srRNA`, `5srRNA` are the three structural [RNAs](dna.md#rna) present in the [ribosome](cell.md#ribosome): [23S ribosomal RNA](cell.md#23s-ribosomal-rna), [16S ribosomal RNA](cell.md#16s-ribosomal-rna), [5S ribosomal RNA](cell.md#5s-ribosomal-rna), all others are obvious:
    <a id="_138"></a>
    - [tRNA](cell.md#transfer-rna)
    <a id="_139"></a>
    - [mRNA](dna.md#messenger-rna)
    <a id="_140"></a>
    - [protein](protein.md). This is the seventh class, and this enzyme only contains mass in this class as expected.
    <a id="_141"></a>
    - [metabolite](molecular-biology.md#metabolite)
    <a id="_142"></a>
    - [water](chemistry.md#water)
    <a id="_143"></a>
    - [DNA](dna.md)
    <a id="_144"></a>
    - [RNA](dna.md#rna): TODO `rna` vs `miscRNA`
  <a id="_145"></a>
  - `location`: [cell compartment](cell.md#cellular-compartment) where the protein is present, `c` defined at `reconstruction/ecoli/flat/compartments.tsv` as [cytoplasm](cell.md#cytoplasm), as expected for something that will make an [amino acid](protein.md#amino-acid)
<a id="_146"></a>
- <a id="_147"></a>
  `reconstruction/ecoli/flat/rnas.tsv`: TODO vs `transcriptionUnits.tsv`. Sample lines:<a id="_148"></a>

  ```
  "halfLife" "name" "seq" "type" "modifiedForms" "monomerId" "comments" "mw" "location" "ntCount" "id" "geneId" "microarray expression"
  174.0 "ThrA [RNA]" "AUGCGAGUGUUG..." "mRNA" [] "ASPKINIHOMOSERDEHYDROGI-MONOMER" "" [0.0, 0.0, 0.0, 0.0, 790935.00399999996, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0] ["c"] [553, 615, 692, 603] "EG10998_RNA" "EG10998" 0.0005264904
  ```

  <a id="_149"></a>

  <a id="_150"></a>
  - `halfLife`: [half-life](particle-physics.md#half-life)
  <a id="_151"></a>
  - `mw`: molecular weight, same as in `reconstruction/ecoli/flat/proteins.tsv`. This [molecule](quantum-mechanics.md#molecule) only have weight in the `mRNA` class, as expected, as it just codes for a protein
  <a id="_152"></a>
  - `location`: same as in `reconstruction/ecoli/flat/proteins.tsv`
  <a id="_153"></a>
  - `ntCount`: [nucleotide](dna.md#nucleotide) count for each of the ATGC
  <a id="_154"></a>
  - `microarray expression`: presumably refers to [DNA microarray](dna.md#dna-microarray) for [gene expression profiling](dna.md#gene-expression-profiling), but what measure exactly?
<a id="_155"></a>
- `reconstruction/ecoli/flat/sequence.fasta`: [FASTA](biology.md#fasta-format) [DNA](dna.md) sequence, first two lines:<a id="_156"></a>

  ```
  >E. coli K-12 MG1655 U00096.2 (1 to 4639675 = 4639675 bp)
  AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGCTTCTG
  ```
<a id="_157"></a>
- <a id="_158"></a>
  `reconstruction/ecoli/flat/transcriptionUnits.tsv`: [transcription units](dna.md#transcription-unit). We can observe for example the two different transcription units of the [E. Coli K-12 MG1655 operon thrLABC](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc) in the lines:<a id="_159"></a>

  ```
  "expression_rate" "direction" "right" "terminator_id"  "name"    "promoter_id" "degradation_rate" "id"       "gene_id"                                   "left"
  0.0               "f"         310     ["TERM0-1059"]   "thrL"    "PM00249"     0.198905992329492 "TU0-42486" ["EG11277"]                                  148
  657.057317358791  "f"         5022    ["TERM_WC-2174"] "thrLABC" "PM00249"     0.231049060186648 "TU00178"   ["EG10998", "EG10999", "EG11000", "EG11277"] 148
  ```

  <a id="_160"></a>

  <a id="_161"></a>
  - `promoter_id`: matches promoter id in `reconstruction/ecoli/flat/promoters.tsv`
  <a id="_162"></a>
  - `gene_id`: matches id in `reconstruction/ecoli/flat/genes.tsv`
  <a id="_163"></a>
  - `id`: matches exactly those used in [BioCyc](biology.md#biocyc), which is quite nice, might be more or less standardized:<a id="_164"></a>

    <a id="_165"></a>
    - [https://biocyc.org/ECOLI/NEW-IMAGE?object=TU0-42486](https://biocyc.org/ECOLI/NEW-IMAGE?object=TU0-42486)
    <a id="_166"></a>
    - [https://biocyc.org/ECOLI/NEW-IMAGE?type=OPERON&object=TU00178](https://biocyc.org/ECOLI/NEW-IMAGE?type=OPERON&object=TU00178)
<a id="_167"></a>
- `reconstruction/ecoli/flat/genes.tsv`<a id="_168"></a>

  ```
  "length" "name"                      "seq"             "rnaId"      "coordinate" "direction" "symbol" "type" "id"      "monomerId"
  66       "thr operon leader peptide" "ATGAAACGCATT..." "EG11277_RNA" 189         "+"         "thrL"   "mRNA" "EG11277" "EG11277-MONOMER"
  2463     "ThrA"                      "ATGCGAGTGTTG"    "EG10998_RNA" 336         "+"         "thrA"   "mRNA" "EG10998" "ASPKINIHOMOSERDEHYDROGI-MONOMER"
  ```
<a id="_169"></a>
- <a id="_170"></a>
  `reconstruction/ecoli/flat/metabolites.tsv` contains [metabolite](molecular-biology.md#metabolite) information. Sample lines:<a id="_171"></a>

  ```
  "id"                       "mw7.2" "location"
  "HOMO-SER"                 119.12  ["n", "j", "w", "c", "e", "m", "o", "p", "l", "i"]
  "L-ASPARTATE-SEMIALDEHYDE" 117.104 ["n", "j", "w", "c", "e", "m", "o", "p", "l", "i"]
  ```
  In the case of the enzyme thrA, one of the two reactions it catalyzes is "L-aspartate 4-semialdehyde" into "Homoserine".

  <a id="_172"></a>
  Starting from the enzyme page: [https://biocyc.org/gene?orgid=ECOLI&id=EG10998](https://biocyc.org/gene?orgid=ECOLI&id=EG10998) we reach the reaction page: [https://biocyc.org/ECOLI/NEW-IMAGE?type=REACTION&object=HOMOSERDEHYDROG-RXN](https://biocyc.org/ECOLI/NEW-IMAGE?type=REACTION&object=HOMOSERDEHYDROG-RXN) which has reaction ID `HOMOSERDEHYDROG-RXN`, and that page which clarifies the IDs:<a id="_173"></a>

  <a id="_174"></a>
  - [https://biocyc.org/compound?orgid=ECOLI&id=L-ASPARTATE-SEMIALDEHYDE:](https://biocyc.org/compound?orgid=ECOLI&id=L-ASPARTATE-SEMIALDEHYDE:) "L-aspartate 4-semialdehyde" has ID `L-ASPARTATE-SEMIALDEHYDE`
  <a id="_175"></a>
  - [https://biocyc.org/compound?orgid=ECOLI&id=HOMO-SER:](https://biocyc.org/compound?orgid=ECOLI&id=HOMO-SER:) "Homoserine" has ID `HOMO-SER`
  so these are the compounds that we care about.
<a id="_176"></a>
- <a id="_177"></a>
  `reconstruction/ecoli/flat/reactions.tsv` contains [chemical reaction](chemistry.md#chemical-reaction) information. Sample lines:<a id="_178"></a>

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

  <a id="_179"></a>

  <a id="_180"></a>
  - `catalized by`: here we see `ASPKINIHOMOSERDEHYDROGI-CPLX`, which we can guess is a [protein complex](protein.md#protein-complex) made out of `ASPKINIHOMOSERDEHYDROGI-MONOMER`, which is the ID for the `thrA` we care about! This is confirmed in `complexationReactions.tsv`.
<a id="_181"></a>
- `reconstruction/ecoli/flat/complexationReactions.tsv` contains information about [chemical reactions](chemistry.md#chemical-reaction) that produce [protein complexes](protein.md#protein-complex):<a id="_182"></a>

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

  The `coeff` is how many monomers need to get together for form the final complex. This can be seen from the Summary section of [https://ecocyc.org/gene?orgid=ECOLI&id=ASPKINIHOMOSERDEHYDROGI-MONOMER](https://ecocyc.org/gene?orgid=ECOLI&id=ASPKINIHOMOSERDEHYDROGI-MONOMER):<a id="_183"></a>
  > Aspartate kinase I / homoserine dehydrogenase I comprises a dimer of ThrA dimers. Although the dimeric form is catalytically active, the binding equilibrium dramatically favors the tetrameric form. The aspartate kinase and homoserine dehydrogenase activities of each ThrA monomer are catalyzed by independent domains connected by a linker region.

  Fantastic literature summary! Can't find that in database form there however.
<a id="_184"></a>
- `reconstruction/ecoli/flat/proteinComplexes.tsv` contains [protein complex](protein.md#protein-complex) information:<a id="_185"></a>

  ```
  "name" "comments" "mw" "location" "reactionId" "id"
  "aspartate kinase / homoserine dehydrogenase"
  ""
  [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 356414.04399999994, 0.0, 0.0, 0.0, 0.0]
  ["c"]
  "ASPKINIHOMOSERDEHYDROGI-CPLX_RXN"
  "ASPKINIHOMOSERDEHYDROGI-CPLX"
  ```
<a id="_186"></a>
- `reconstruction/ecoli/flat/protein_half_lives.tsv` contains the [half-life](particle-physics.md#half-life) of [proteins](protein.md). Very few proteins are listed however for some reason.
<a id="_187"></a>
- `reconstruction/ecoli/flat/tfIds.csv`: [transcription factors](dna.md#transcription-factor) information:<a id="_188"></a>

  ```
  "TF"   "geneId"  "oneComponentId"  "twoComponentId" "nonMetaboliteBindingId" "activeId" "notes"
  "arcA" "EG10061" "PHOSPHO-ARCA"    "PHOSPHO-ARCA"
  "fnr"  "EG10325" "FNR-4FE-4S-CPLX" "FNR-4FE-4S-CPLX"
  "dksA" "EG10230"
  ```

### Condition

↑ **Parent:** [Source code overview](#source-code-overview)

<a id="_189"></a>
<a id="_190"></a>
- <a id="_191"></a>
  `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` contains the nutrients in a minimal environment in which the cell survives:<a id="_192"></a>

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
  If we compare that to `reconstruction/ecoli/flat/condition/nutrient/minimal_plus_amino_acids.tsv`, we see that it adds the 20 [amino acids](protein.md#amino-acid) on top of the minimal condition:<a id="_193"></a>

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

  <a id="_194"></a>
  We can try to understand the less obvious ones:<a id="_195"></a>

  <a id="_196"></a>
  - `ADP`: TODO
  <a id="_197"></a>
  - `PI`: TODO
  <a id="_198"></a>
  - `PROTON[c]`: presumably a measure of [pH](chemistry.md#ph)
  <a id="_199"></a>
  - `GLC[p]`: [glucose](chemistry.md#glucose), this can be seen by comparing `minimal.tsv` with `minimal_no_glucose.tsv`
  <a id="_200"></a>
  - `AMMONIUM`: [ammonium](chemistry.md#ammonium). This appears to be the primary source of [nitrogen](chemistry.md#nitrogen) [atoms](chemistry.md#atom) for producing [amino acids](protein.md#amino-acid).
  <a id="_201"></a>
  - `CYTOSINE[c]`: hmmm, why is external [cytosine](dna.md#cytosine) needed? Weird.
<a id="_202"></a>
- <a id="_203"></a>
  `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/` contains sequences of conditions for each time. For example:<a id="_204"></a>

  <a id="_205"></a>
  - `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/000000_basal.tsv` contains:<a id="_206"></a>

    ```
    "time (units.s)" "nutrients"
    0 "minimal"
    ```

    which means just using `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` until infinity. That is the default one used by `runSim.py`, as can be seen from `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Environment/attributes/nutrientTimeSeriesLabel` which contains just `000000_basal`.
  <a id="_207"></a>
  - `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/000001_cut_glucose.tsv` is more interesting and contains:<a id="_208"></a>

    ```
    "time (units.s)" "nutrients"
    0 "minimal"
    1200 "minimal_no_glucose"
    ```

    so we see that this will shift the conditions half-way to a condition that will eventually kill the bacteria because it will run out of [glucose](chemistry.md#glucose) and thus energy!

  <a id="_209"></a>
  Timeseries can be selected with `--variant nutrientTimeSeries X Y`, see also: [run variants](#run-variants).

  <a id="_210"></a>
  We can use that variant with:<a id="_211"></a>

  ```
  VARIANT="condition" FIRST_VARIANT_INDEX=1 LAST_VARIANT_INDEX=1 python runscripts/manual/runSim.py
  ```
<a id="_212"></a>
- <a id="_213"></a>
  `reconstruction/ecoli/flat/condition/condition_defs.tsv` contains lines of form:<a id="_214"></a>

  ```
  "condition" "nutrients"                "genotype perturbations" "doubling time (units.min)" "active TFs"
  "basal"     "minimal"                  {}                       44.0                        []
  "no_oxygen" "minimal_minus_oxygen"     {}                       100.0                       []
  "with_aa"   "minimal_plus_amino_acids" {}                       25.0                        ["CPLX-125", "MONOMER0-162", "CPLX0-7671", "CPLX0-228", "MONOMER0-155"]
  ```

  <a id="_215"></a>

  <a id="_216"></a>
  - `condition` refers to entries in `reconstruction/ecoli/flat/condition/condition_defs.tsv`
  <a id="_217"></a>
  - `nutrients` refers to entries under `reconstruction/ecoli/flat/condition/nutrient/`, e.g. `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` or `reconstruction/ecoli/flat/condition/nutrient/minimal_plus_amino_acids.tsv`
  <a id="_218"></a>
  - `genotype perturbations`: there aren't any in the file, but this suggests that genotype modifications can also be incorporated here
  <a id="_219"></a>
  - `doubling time`: TODO experimental data? Because this should be a simulation output, right? Or do they cheat and fix doubling by time?
  <a id="_220"></a>
  - `active TFs`: this suggests that they are cheating [transcription factors](dna.md#transcription-factor) here, as those would ideally be functions of other more basic inputs

## Model validation

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

<a id="_221"></a>
TODO compare with actual datasetes.

## Publications

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)

<a id="_222"></a>
Unfortunately, due to lack of [one page to rule them all](cirosantilli-com.md#one-page-to-rule-them-all), the [on-Git tree publication list is meager](https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/docs/README.md#relevant-papers), some of the most relevant ones seems to be:<a id="_223"></a>

<a id="_224"></a>
- 2021 [open access](education.md#open-access) [review paper](education.md#review-article): [https://journals.asm.org/doi/full/10.1128/ecosalplus.ESP-0001-2020](https://journals.asm.org/doi/full/10.1128/ecosalplus.ESP-0001-2020) "The E. coli Whole-Cell Modeling Project". They should just past that stuff in a [README](software.md#readme) :-) The article mentions that it is a follow up to the previous [M. genitalium whole cell model by Covert lab](taxonomy.md#m-genitalium-whole-cell-model-by-covert-lab). Only 43% of known genes modelled at this point however, a shame.
<a id="_225"></a>
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
