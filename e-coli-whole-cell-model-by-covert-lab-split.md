# E. Coli Whole Cell Model by Covert Lab

↑ **Parent:** [E. Coli whole cell simulation](e-coli-whole-cell-simulation.md)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles-split.md)

<a id="_3"></a>
[https://github.com/CovertLab/WholeCellEcoliRelease](https://github.com/CovertLab/WholeCellEcoliRelease) is a [whole cell simulation](whole-cell-simulation.md) model created by [Covert Lab](covert-lab.md) and other collaborators.

<a id="_4"></a>
The project is written in [Python](python-programming-language.md), hurray!

<a id="_5"></a>
But according to te [README](readme.md), it seems to be the use a [code drop](code-drop.md) model with on-request access to master. [Ciro Santilli](ciro-santilli-split.md) asked at [rationale on GitHub discussion](https://github.com/CovertLab/WholeCellEcoliRelease/discussions/23), and they confirmed as expected that it is to:<a id="_6"></a>

<a id="_7"></a>
- to prevent their [publication](academic-publishing.md) ideas from being stolen. Who would steal publication ideas with public proof in an issue tracker without crediting original authors? [Academia is broken](academia-is-broken.md). Academia should be the most open form of knowledge sharing. But instead we get this silly competition for publication points.
<a id="_8"></a>
- to prevent noise from non-collaborators. But they only get like 2 issues as year on such a meganiche subject... Did you know that you can ignore people, and even block them if they are particularly annoying? Much more likely is that no one will every hear about your project and that it will die with its last graduate student slave.

<a id="_9"></a>
The project is a followup to the earlier [M. genitalium whole cell model by Covert lab](m-genitalium-whole-cell-model-by-covert-lab.md) which modelled [Mycoplasma genitalium](mycoplasma-genitalium.md). [E. Coli](escherichia-coli.md) has 8x more genes (500 vs 4k), but it the undisputed [bacterial](bacteria.md) [model organism](model-organism.md) and as such has been studied much more thoroughly. It also reproduces faster than Mycoplasma (20 minutes vs a few hours), which is a huge advantages for validation/exploratory [experiments](experiment.md).

<a id="_10"></a>
The project has a partial dependency on the [proprietary](proprietary-software.md) [optimization software](optimization-software.md) [CPLEX](cplex.md) which is [freeware](freeware.md), for students, not sure what it is used for exactly, from the comment in the `requirements.txt` the dependency is only partial.

<a id="_11"></a>
This project makes [Ciro Santilli](ciro-santilli-split.md) think of the [E. Coli](escherichia-coli.md) as an [optimization problem](optimization-problem.md). Given such external nutrient/temperature condition, which [DNA](dna-split.md) sequence makes the cell grow the fastest? Balancing [metabolites](metabolite.md) feels like designing a [Factorio](factorio.md) speedrun.

<a id="_12"></a>
There is one major thing missing thing in the current model: [promoters](promoter-genetics.md)/[transcription factor](transcription-factor.md) interactions are not modelled due to lack/low quality of experimental data: [https://github.com/CovertLab/WholeCellEcoliRelease/issues/21](https://github.com/CovertLab/WholeCellEcoliRelease/issues/21). They just have a magic direct "[transcription factor](transcription-factor.md) to [gene](gene.md)" relationship, encoded at [reconstruction/ecoli/flat/foldChanges.tsv](https://github.com/CovertLab/WholeCellEcoliRelease/blob/7e4cc9e57de76752df0f4e32eca95fb653ea64e4/reconstruction/ecoli/flat/foldChanges.tsv) in terms of type "if this is present, such protein is expressed 10x more". [Transcription units](transcription-unit.md) are not implemented at all it appears.

<a id="_13"></a>
Everything in this section refers to version [7e4cc9e57de76752df0f4e32eca95fb653ea64e4](https://github.com/CovertLab/WholeCellEcoliRelease/tree/7e4cc9e57de76752df0f4e32eca95fb653ea64e4), the code drop from November 2020, and was tested on [Ubuntu](ubuntu.md) 21.04 with a docker install of `docker.pkg.github.com/covertlab/wholecellecolirelease/wcm-full` with image id 502c3e604265, unless otherwise noted.

**Table of contents**

- [Install and first run](e-coli-whole-cell-model-by-covert-lab/install-and-first-run.md)
- [Output overview](e-coli-whole-cell-model-by-covert-lab/output-overview.md)
  - [Mass fraction summary plot analysis](e-coli-whole-cell-model-by-covert-lab/mass-fraction-summary-plot-analysis.md)
- [Run variants](e-coli-whole-cell-model-by-covert-lab/run-variants.md)
  - [Default run variant](e-coli-whole-cell-model-by-covert-lab/default-run-variant.md)
  - [Time series run variant](e-coli-whole-cell-model-by-covert-lab/time-series-run-variant.md)
- [Other run variants](e-coli-whole-cell-model-by-covert-lab/other-run-variants.md)
- [Source code overview](e-coli-whole-cell-model-by-covert-lab/source-code-overview.md)
  - [Condition](e-coli-whole-cell-model-by-covert-lab/condition.md)
- [Model validation](e-coli-whole-cell-model-by-covert-lab/model-validation.md)
- [Publications](e-coli-whole-cell-model-by-covert-lab/publications.md)

## ↑ Ancestors (10)

1. [E. Coli whole cell simulation](e-coli-whole-cell-simulation.md)
2. [Escherichia coli](escherichia-coli.md)
3. [List of bacteria](list-of-bacteria.md)
4. [Bacteria](bacteria.md)
5. [Species](species.md)
6. [Taxonomy](taxonomy-split.md)
7. [Biology](biology-split.md)
8. [Natural science](natural-science.md)
9. [Science](science-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [The best articles by Ciro Santilli](articles-split.md)
- [Covert Lab](covert-lab.md)
- [Half-life](half-life.md)
- [Exams and homework are useless, only projects matter](how-to-teach/exams-and-homework-are-useless-only-projects-matter.md)
- [M. genitalium whole cell model by Covert lab](m-genitalium-whole-cell-model-by-covert-lab.md)
- [Molecular biology feels like systems programming](molecular-biology-feels-like-systems-programming.md)
