# DNA

↑ **Parent:** [Molecular biology](molecular-biology.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA)

Since DNA is the centerpiece of life, [Ciro Santilli](ciro-santilli.md) is extremely excited about DNA-related technologies, see also: [molecular biology technologies](ciro-santilli.md#molecular-biology-technologies).

**Table of contents**

- [Structure of DNA](#structure-of-dna)
  - [Nucleic acid double helix](#nucleic-acid-double-helix)
  - [Chromosome](#chromosome)
    - [Chromosome by species](#chromosome-by-species)
    - [Chromosomal crossover](#chromosomal-crossover)
    - [Circular chromosome](#circular-chromosome)
    - [X chromosome](#x-chromosome)
      - [X-inactivation](#x-inactivation)
      - [Sex determination system](#sex-determination-system)
        - [XY sex-determination system](#xy-sex-determination-system)
    - [Nucleosome](#nucleosome)
      - [Histone](#histone)
    - [Plasmid](#plasmid)
    - [Telomere](#telomere)
      - [Hayflick limit](#hayflick-limit)
- [DNA detection](#dna-detection)
- [DNA amplification](#dna-amplification)
  - [Polymerase chain reaction](#polymerase-chain-reaction)
    - [Real-time polymerase chain reaction](#real-time-polymerase-chain-reaction)
    - [Isothermal DNA amplification techniques](#isothermal-dna-amplification-techniques)
      - [Loop-mediated isothermal amplification](#loop-mediated-isothermal-amplification)
- [DNA profiling](#dna-profiling)
  - [Variable number tandem repeat](#variable-number-tandem-repeat)
- [DNA replication](#dna-replication)
  - [Origin of replication](#origin-of-replication)
- [DNA repair](#dna-repair)
- [DNA sequencing](#dna-sequencing)
  - [DNA sequencing milestone](#dna-sequencing-milestone)
  - [Base calling](#base-calling)
  - [DNA microarray](#dna-microarray)
  - [Metagenomics](#metagenomics)
  - [Short-read DNA sequencing](#short-read-dna-sequencing)
    - [Long-read DNA sequencing](#long-read-dna-sequencing)
  - [RNA-Seq](#rna-seq)
    - [Gene expression profiling](#gene-expression-profiling)
  - [Whole-genome sequencing](#whole-genome-sequencing)
  - [Application of DNA sequencing](#application-of-dna-sequencing)
    - [DNA paternity testing](#dna-paternity-testing)
  - [DNA sequencing method](#dna-sequencing-method)
    - [Sanger method](#sanger-method)
  - [DNA sequencing company](#dna-sequencing-company)
    - [Illumina](#illumina)
      - [Bridge amplification](#bridge-amplification)
      - [Solexa](#solexa)
    - [Oxford Nanopore Technologies](#oxford-nanopore-technologies)
      - [Oxford Nanopore Technologies product](#oxford-nanopore-technologies-product)
        - [PromethION](#promethion)
        - [Oxford Nanopore MinION](#oxford-nanopore-minion)
          - [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)
            - [Experiment background](oxford-nanopore-river-bacteria.md#experiment-background)
            - [Overview of the experiment](oxford-nanopore-river-bacteria.md#overview-of-the-experiment)
              - [Why Oxford Nanopore was used instead of Illumina for the sequencing](oxford-nanopore-river-bacteria.md#why-oxford-nanopore-was-used-instead-of-illumina-for-the-sequencing)
            - [Sample collection](oxford-nanopore-river-bacteria.md#sample-collection)
            - [DNA extraction](oxford-nanopore-river-bacteria.md#dna-extraction)
              - [Filtration with vacuum pump](oxford-nanopore-river-bacteria.md#filtration-with-vacuum-pump)
              - [Post filtration purification](oxford-nanopore-river-bacteria.md#post-filtration-purification)
            - [PCR](oxford-nanopore-river-bacteria.md#pcr)
              - [PCR verification with gel electrophoresis](oxford-nanopore-river-bacteria.md#pcr-verification-with-gel-electrophoresis)
            - [Sequencing](oxford-nanopore-river-bacteria.md#sequencing)
              - [Pre-sequencing preparation](oxford-nanopore-river-bacteria.md#pre-sequencing-preparation)
              - [Using the Oxford Nanopore](oxford-nanopore-river-bacteria.md#using-the-oxford-nanopore)
            - [Bioinformatics](oxford-nanopore-river-bacteria.md#bioinformatics)
            - [Conclusions](oxford-nanopore-river-bacteria.md#conclusions)
            - [Protocols used](oxford-nanopore-river-bacteria.md#protocols-used)
              - [Qiagen DNeasy PowerWater Kit](oxford-nanopore-river-bacteria.md#qiagen-dneasy-powerwater-kit)
              - [Qiagen QIAquick PCR Purification Kit](oxford-nanopore-river-bacteria.md#qiagen-qiaquick-pcr-purification-kit)
              - [Oxford Nanopore SQK-LSK109 Ligation Sequencing Kit](oxford-nanopore-river-bacteria.md#oxford-nanopore-sqk-lsk109-ligation-sequencing-kit)
            - [Equipment used](oxford-nanopore-river-bacteria.md#equipment-used)
              - [Thermo Scientific Nalgene Polysulfone Reusable Bottle Top Filters](oxford-nanopore-river-bacteria.md#thermo-scientific-nalgene-polysulfone-reusable-bottle-top-filters)
              - [KNF Laboport series laboratory vacuum pump](oxford-nanopore-river-bacteria.md#knf-laboport-series-laboratory-vacuum-pump)
              - [Scientific Industries Inc. Vortex-Genie 2](oxford-nanopore-river-bacteria.md#scientific-industries-inc-vortex-genie-2)
              - [VWR Micro Star 17 microcentrifuge](oxford-nanopore-river-bacteria.md#vwr-micro-star-17-microcentrifuge)
              - [VELP Scientifica WIZARD IR Infrared Vortex Mixer](oxford-nanopore-river-bacteria.md#velp-scientifica-wizard-ir-infrared-vortex-mixer)
              - [Marshal Scientific MJ Research PTC-200 Thermal Cycler](oxford-nanopore-river-bacteria.md#marshal-scientific-mj-research-ptc-200-thermal-cycler)
              - [GE MagRack 6](oxford-nanopore-river-bacteria.md#ge-magrack-6)
              - [BTLab Systems Mini Centrifuge](oxford-nanopore-river-bacteria.md#btlab-systems-mini-centrifuge)
              - [Fisher Scientific UVP LM-26E Benchtop 2UV Transilluminator](oxford-nanopore-river-bacteria.md#fisher-scientific-uvp-lm-26e-benchtop-2uv-transilluminator)
              - [Biochrom SimpliNano spectrophotometer](oxford-nanopore-river-bacteria.md#biochrom-simplinano-spectrophotometer)
            - [External links to this page](oxford-nanopore-river-bacteria.md#external-links-to-this-page)
- [De novo DNA synthesis](#de-novo-dna-synthesis)
  - [De novo DNA synthesis company](#de-novo-dna-synthesis-company)
    - [AnsaBio](#ansabio)
    - [Camena Bioscience](#camena-bioscience)
    - [DNAScript](#dnascript)
    - [Touchlight Genetics](#touchlight-genetics)
  - [Artificial gene synthesis](#artificial-gene-synthesis)
    - [Artificial chromosome](#artificial-chromosome)
  - [Species bootstrapping from DNA](#species-bootstrapping-from-dna)
    - [Synthetic chromosome](#synthetic-chromosome)
    - [Synthetic virus](#synthetic-virus)
      - [DIY gun](#diy-gun)
        - [3D-printed firearm](#3d-printed-firearm)
    - [Genome Project-Write](#genome-project-write)
    - [Yeast artificial chromosome](#yeast-artificial-chromosome)
- [Epigenetics](#epigenetics)
  - [DNA methylation](#dna-methylation)
    - [History of DNA methylation research](#history-of-dna-methylation-research)
    - [Adenine methylation](#adenine-methylation)
    - [Bisulfite sequencing](#bisulfite-sequencing)
  - [Transgenerational epigenetic inheritance](#transgenerational-epigenetic-inheritance)
- [RNA](#rna)
  - [Messenger RNA](#messenger-rna)
    - [Alternative splicing](#alternative-splicing)
  - [RNA secondary structure](#rna-secondary-structure)
    - [RNA half-life prediction](#rna-half-life-prediction)
  - [Transcription (biology)](#transcription-biology)
    - [Post-transcriptional modification](#post-transcriptional-modification)
    - [Promoter (genetics)](#promoter-genetics)
      - [Transcriptional regulation](#transcriptional-regulation)
    - [RNA polymerase](#rna-polymerase)
      - [RNA-dependent RNA polymerase](#rna-dependent-rna-polymerase)
    - [Operon](#operon)
      - [Transcription unit](#transcription-unit)
      - [Operon vs transcription unit](#operon-vs-transcription-unit)
      - [Polycistronic mRNA](#polycistronic-mrna)
    - [Transcription factor](#transcription-factor)
      - [Intrinsic termination](#intrinsic-termination)
  - [Type of RNA](#type-of-rna)
- [Nucleotide](#nucleotide)
  - [Nucleobase](#nucleobase)
    - [Adenine](#adenine)
    - [Cytosine](#cytosine)
    - [Thymine](#thymine)
    - [Uracil](#uracil)
      - [Uracil vs thymine](#uracil-vs-thymine)
- [Base pair](#base-pair)
- [Genetic code](#genetic-code)
  - [Reading frame](#reading-frame)
    - [Open reading frame](#open-reading-frame)
      - [NCBI open reading frame tool](#ncbi-open-reading-frame-tool)
  - [Codon](#codon)
    - [Start codon](#start-codon)
    - [Stop codon](#stop-codon)
- [Genetics](#genetics)
  - [Genetics company](#genetics-company)
    - [23andMe](#23andme)
  - [Population genetics](#population-genetics)
  - [Evolutionary genetics](#evolutionary-genetics)
    - [DNA replication is a key limiting factor of bacterial replication time](#dna-replication-is-a-key-limiting-factor-of-bacterial-replication-time)
      - [It is hard for complex organisms to evolve because longer DNA means longer replication time](#it-is-hard-for-complex-organisms-to-evolve-because-longer-dna-means-longer-replication-time)
  - [Comparative genomics](#comparative-genomics)
    - [Parasites tend to have smaller DNAs](#parasites-tend-to-have-smaller-dnas)
    - [Homology (biology)](#homology-biology)
      - [Ortholog](#ortholog)
      - [Paralog](#paralog)
  - [Phenotype](#phenotype)
  - [Transposable element](#transposable-element)
- [Gene](#gene)
  - [Genome](#genome)
    - [Genomics](#genomics)
  - [Non-coding DNA](#non-coding-dna)
- [Mutation](#mutation)
  - [Mutagen](#mutagen)
  - [DNA mutation type](#dna-mutation-type)
    - [Indel](#indel)
    - [Single-nucleotide polymorphism](#single-nucleotide-polymorphism)
  - [Slipped strand mispairing](#slipped-strand-mispairing)
- [Horizontal gene transfer](#horizontal-gene-transfer)
  - [Transduction (genetics)](#transduction-genetics)
  - [Transformation (genetics)](#transformation-genetics)
    - [Avery-MacLeod-McCarty experiment](#avery-macleod-mccarty-experiment)
    - [Transfection](#transfection)

## Structure of DNA

↑ **Parent:** [DNA](dna.md)

### Nucleic acid double helix

↑ **Parent:** [Structure of DNA](#structure-of-dna)

### Chromosome

↑ **Parent:** [Structure of DNA](#structure-of-dna)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chromosome)

#### Chromosome by species

↑ **Parent:** [Chromosome](#chromosome)

#### Chromosomal crossover

↑ **Parent:** [Chromosome](#chromosome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chromosomal_crossover)

#### Circular chromosome

↑ **Parent:** [Chromosome](#chromosome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Circular_chromosome)

#### X chromosome

↑ **Parent:** [Chromosome](#chromosome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/X_chromosome)

##### X-inactivation

↑ **Parent:** [X chromosome](#x-chromosome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/X-inactivation)

[epigenetics](#epigenetics) mechanism.

<a id="video-x-inactivation-and-epigenetics-by-wehimovies-2012"></a>
**[Video 1](#video-x-inactivation-and-epigenetics-by-wehimovies-2012). X-Inactivation and Epigenetics by WEHImovies (2012)** [Source](https://www.youtube.com/watch?v=mHak9EZjySs). Shows how this makes every [female](biology.md#female) [mammal](taxonomy.md#mammal) a [chimera](taxonomy.md#chimera-genetics).

##### Sex determination system

↑ **Parent:** [X chromosome](#x-chromosome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sex_determination_system)

###### XY sex-determination system

↑ **Parent:** [Sex determination system](#sex-determination-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/XY_sex-determination_system)

#### Nucleosome

↑ **Parent:** [Chromosome](#chromosome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nucleosome)

##### Histone

↑ **Parent:** [Nucleosome](#nucleosome)  
🏷️ **Tags:** [Protein](protein.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Histone)

These are apparenty an important part of [transcriptional regulation](#transcriptional-regulation) given the number of modifications they can undergo! Quite exciting.

#### Plasmid

↑ **Parent:** [Chromosome](#chromosome)  
🏷️ **Tags:** [Horizontal gene transfer](#horizontal-gene-transfer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Plasmid)

#### Telomere

↑ **Parent:** [Chromosome](#chromosome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Telomere)

##### Hayflick limit

↑ **Parent:** [Telomere](#telomere)  
🏷️ **Tags:** [Anti-cancer mechanism](biology.md#anti-cancer-mechanism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hayflick_limit)

## DNA detection

↑ **Parent:** [DNA](dna.md)

DNA detection means determining if a specific DNA sequence is present in a sample.

This can be used to detect if a given species of microorganism is present in a sample, and is therefore a widely used diagnostics technique to see if someone is infected with a virus.

You could of course do full [DNA Sequencing](#dna-sequencing) to see everything that is there, but since it is as a more generic procedure, sequencing is more expensive and slow.

The alternative is to use a [DNA amplification](#dna-amplification) technique.

## DNA amplification

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_amplification)

DNA amplification is one of the key DNA technologies:
- it is one of the main ways in which [DNA detection](#dna-detection) can be done.
- it is the first step of [Illumina sequencing](#illumina), since you need multiple copies of several parts of the genome for the method to work

### Polymerase chain reaction

↑ **Parent:** [DNA amplification](#dna-amplification)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Polymerase_chain_reaction)

This is an extremely widely used technique as of 2020 and much earlier.

If allows you to amplify "any" sequence of choice (TODO length limitations) between a start and end sequences of interest which you synthesize.

If the sequence of interest is present, it gets amplified exponentially, and you end up with a bunch of DNA at the end.

You can then measure the DNA concentration based on simple light refraction methods to see if there is a lot of DNA or not in the post-processed sample.

Even [Ciro Santilli](ciro-santilli.md) had some contact with it at: [Section "How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it"](oxford-nanopore-river-bacteria.md), see: [PCR](oxford-nanopore-river-bacteria.md#pcr)!

One common problem that happens with PCR if you don't design your primers right is: [https://en.wikipedia.org/wiki/Primer_dimer](https://en.wikipedia.org/wiki/Primer_dimer)

Sometime it fails: [https://www.reddit.com/r/molecularbiology/comments/1kouomw/when_your_pcr_fails_again_and_you_start/](https://www.reddit.com/r/molecularbiology/comments/1kouomw/when_your_pcr_fails_again_and_you_start/)

> Nothing humbles you faster than a bandless gel. One minute you’re a scientist, the next you’re just a pipette-wielding wizard casting spells that don’t work. Meanwhile, physicists are out there acting like gravity always behaves. Smash that upvote if your reagents have ever gaslit you.

and a comment:

> PCR = Pray, Cry, Repeat

#### Real-time polymerase chain reaction

↑ **Parent:** [Polymerase chain reaction](#polymerase-chain-reaction)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Real-time_polymerase_chain_reaction)

Also known as: Quantitative PCR (qPCR).

Like PCR, but the amplification machine measures the concentration of DNA at each step.

This describes one possible concentration detection method with [fluorescent](condensed-matter-physics.md#fluorescence) molecules that only become fluorescent when the DNA is double stranded ([SYBR Green](https://en.wikipedia.org/wiki/SYBR_Green_I))

<a id="video-polymerase-chain-reaction-pcr-quantitative-pcr-qpcr-by-applied-biological-materials-2016"></a>
**[Video 2](#video-polymerase-chain-reaction-pcr-quantitative-pcr-qpcr-by-applied-biological-materials-2016). Polymerase Chain Reaction (PCR) - Quantitative PCR (qPCR) by Applied Biological Materials (2016)** [Source](http://youtube.com/watch?v=YhXj5Yy4ksQ).

This allows you to predict the exact initial concentration by extrapolating the exponential curve backwards.

TODO: vs non-real-time PCR. Why can't you just divide by 2 for every heating step to reach back the original concentration? Likely the reaction reach saturation at an unknown step.

TODO: vs non-real-time PCR in medical diagnostics: do you really need to know concentration for diagnostics? Isn't it enough to know if the virus is present or not?

#### Isothermal DNA amplification techniques

↑ **Parent:** [Polymerase chain reaction](#polymerase-chain-reaction)

Isothermal means "at fixed temperature".

This is to contrast with the more well established [polymerase chain reaction](#polymerase-chain-reaction), which requires heating and cooling the sample several times.

The obvious advantage of isothermal methods is that their machinery can be simpler and cheaper, and the process can happen faster, since you don't have to do through heating and cooling cycles.

##### Loop-mediated isothermal amplification

↑ **Parent:** [Isothermal DNA amplification techniques](#isothermal-dna-amplification-techniques)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Loop-mediated_isothermal_amplification)

Like PCR, but does not require thermal cycling. Thus the "isothermal" in the name: iso means same, so "same temperature".

Not needing the thermo cycling means that the equipment needed is much smaller and cheaper it seems.

Trade-offs question: [https://biology.stackexchange.com/questions/92172/what-are-the-trade-offs-between-polymerase-chain-reaction-pcr-vs-loop-mediated](https://biology.stackexchange.com/questions/92172/what-are-the-trade-offs-between-polymerase-chain-reaction-pcr-vs-loop-mediated)

<a id="video-loop-mediated-isothermal-amplification-lamp-tutorial-by-new-england-biolabs-2015"></a>
**[Video 3](#video-loop-mediated-isothermal-amplification-lamp-tutorial-by-new-england-biolabs-2015). Loop Mediated Isothermal Amplification (LAMP) Tutorial by New England Biolabs (2015)** [Source](https://www.youtube.com/watch?v=L5zi2P4lggw). Explains the basic LAMP concept well.

## DNA profiling

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_profiling)

### Variable number tandem repeat

↑ **Parent:** [DNA profiling](#dna-profiling)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Variable_number_tandem_repeat)

Caused by [slipped strand mispairing](#slipped-strand-mispairing).

## DNA replication

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_replication)

### Origin of replication

↑ **Parent:** [DNA replication](#dna-replication)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Origin_of_replication)

oriC = Origin of [Chromosomal](#chromosome) replication.

## DNA repair

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_repair)

## DNA sequencing

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_sequencing)

Big excitement picture at: [molecular biology technologies](ciro-santilli.md#molecular-biology-technologies).

A concrete experiment has been done at [Section 6. "Sequencing"](oxford-nanopore-river-bacteria.md#sequencing) on section [sequencing](oxford-nanopore-river-bacteria.md#sequencing).

### DNA sequencing milestone

↑ **Parent:** [DNA sequencing](#dna-sequencing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_sequencing_milestone)

Most of these are going to be [Whole-genome sequencing](#whole-genome-sequencing) of some [model organism](biology.md#model-organism):
- 1975 by [Sanger](chemistry.md#frederick-sanger) et al.: 5 kbp of the single-stranded [bacteriophage ΦX174](taxonomy.md#phi-x-174) using Sanger's radiolabelling method
- 1981 by [Sanger](chemistry.md#frederick-sanger) et al.: 17 kbp of human mitochondrial DNA via [Sanger method](#sanger-method), known as the [Cambridge Reference Sequence](human.md#cambridge-reference-sequence)
- 2003: [Human Genome Project](human.md#human-genome-project) (3 [Gbp](#base-pair))
[https://en.wikipedia.org/wiki/Whole_genome_sequencing#History](https://en.wikipedia.org/wiki/Whole_genome_sequencing#History) lists them all. Basically th big "firsts" all happened in the 1990s and early 2000s.

### Base calling

↑ **Parent:** [DNA sequencing](#dna-sequencing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Base_calling)

### [DNA](dna.md) microarray

↑ **Parent:** [DNA sequencing](#dna-sequencing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_microarray)

Can be seen as a cheap form of [DNA sequencing](#dna-sequencing) that only test for a few hits. Some major applications:
- [gene expression profiling](#gene-expression-profiling)
- [single-nucleotide polymorphism](#single-nucleotide-polymorphism): specificity is high enough to detect snips

### Metagenomics

↑ **Parent:** [DNA sequencing](#dna-sequencing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Metagenomics)

Experiments that involve sequencing bulk DNA found in a sample to determine what species are present, as opposed to sequencing just a single specific specimen. Examples of samples that are often used:
- river water to determine which bacteria are present, notably to determine if the water is free of dangerous bacteria. A concrete example is shown at: [Section "How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it"](oxford-nanopore-river-bacteria.md).
- sea water biodiversity: [http://ocean-microbiome.embl.de/companion.html](http://ocean-microbiome.embl.de/companion.html)
- [food](art.md#food), including searching for desirable microorganisms such as in cheese or bread [yeast](taxonomy.md#yeast)
- [poo](molecular-biology.md#feces), e.g. to study how the human microbiome influences health. There are companies actively working on this, e.g.: [https://www.microbiotica.com/](https://www.microbiotica.com/)

One related application which most people would not consider metagenomics, is that of finding [circulating tumor DNA](https://en.wikipedia.org/wiki/Circulating_tumor_DNA) in blood to detect tumors.

### Short-read DNA sequencing

↑ **Parent:** [DNA sequencing](#dna-sequencing)

#### Long-read DNA sequencing

↑ **Parent:** [Short-read DNA sequencing](#short-read-dna-sequencing)

### RNA-Seq

↑ **Parent:** [DNA sequencing](#dna-sequencing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RNA-Seq)

Sequencing the [DNA](dna.md) tells us what the organism can do. Sequencing the [RNA](#rna) tells us what the organism is actually doing at a given point in time. The problem is not killing the cell while doing that. Is it possible to just take a chunk of the cell to sequence without killing it maybe?

#### Gene expression profiling

↑ **Parent:** [RNA-Seq](#rna-seq)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gene_expression_profiling)

### Whole-genome sequencing

↑ **Parent:** [DNA sequencing](#dna-sequencing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Whole-genome_sequencing)

### Application of DNA sequencing

↑ **Parent:** [DNA sequencing](#dna-sequencing)

#### DNA paternity testing

↑ **Parent:** [Application of DNA sequencing](#application-of-dna-sequencing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_paternity_testing)

### DNA sequencing method

↑ **Parent:** [DNA sequencing](#dna-sequencing)

#### [Sanger](chemistry.md#frederick-sanger) method

↑ **Parent:** [DNA sequencing method](#dna-sequencing-method)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sanger_method)

### DNA sequencing company

↑ **Parent:** [DNA sequencing](#dna-sequencing)

- [https://techcrunch.com/2022/05/31/ultima-genomics-claims-100-full-genome-sequencing-after-stealth-600m-raise/](https://techcrunch.com/2022/05/31/ultima-genomics-claims-100-full-genome-sequencing-after-stealth-600m-raise/) Ultima genomics TODO technology? Promises 100 USD genome, 600M funding out of stealth...

#### Illumina

↑ **Parent:** [DNA sequencing company](#dna-sequencing-company)  
🏷️ **Tags:** [American company](company.md#american-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Illumina,_Inc.)

The by far dominating DNA sequencing company of the late 2000's and 2010's due to having the smallest cost per base pair.

Illumina actually bought their 2010's dominating technology from a [Cambridge](united-kingdom.md#cambridge) company called [Solexa](#solexa).

To understand how Illumina's technology works basically, watch this video: [Video 4. "Illumina Sequencing by Synthesis by Illumina (2016)"](#video-illumina-sequencing-by-synthesis).

<a id="video-illumina-sequencing-by-synthesis"></a>
**[Video 4](#video-illumina-sequencing-by-synthesis). Illumina Sequencing by Synthesis by Illumina (2016)** [Source](http://youtube.com/watch?v=fCd6B5HRaZ8).

The key innovation of this method is the [Bridge amplification](#bridge-amplification) step, which produces a large amount of identical DNA strands.

##### Bridge amplification

↑ **Parent:** [Illumina](#illumina)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Illumina_dye_sequencing#Bridge_amplification)

This is one of the the key innovations of the [Illumina](#illumina) (originally [Solexa](#solexa)) sequencing.

This step is genius because sequencing is basically a [signal-to-noise](technology.md#signal-to-noise-ratio) problem, as you are trying to observe individual tiny nucleotides mixed with billions of other tiny nucleotides.

With bridge amplification, we group some of the nucleotides together, and multiply the signal millions of times for that part of the DNA.

<a id="image-illustration-of-the-bridge-amplification-step-of-illumina-sequencing"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/65/Cluster_Generation.png/960px-Cluster_Generation.png)

**[Figure 1](#image-illustration-of-the-bridge-amplification-step-of-illumina-sequencing). Illustration of the bridge amplification step of Illumina sequencing**. [Source](https://commons.wikimedia.org/wiki/File:Cluster_Generation.png).

##### Solexa

↑ **Parent:** [Illumina](#illumina)

Bought by [Illumina](#illumina) [for 600 million in 2007 for 600 million dollars](https://www.reuters.com/article/us-illumina-solexa/illumina-to-buy-genome-firm-solexa-for-600-mln-idUSN1348062320061113).

This is one of the prime examples of [Europe](continent.md#europe)'s decline.

Instead of trying to dominate the sequencing market and gain trillions of dollars from it, they local British early stage investors were more than happy to get a 20x return on their small initial investments, and sold out to the Americans who will then make the real profit.

And now Solexa doesn't even have its own [Wikipedia](website.md#wikipedia) page, while Illumina is set out to be the next [Microsoft](microsoft.md). What a disgrace.

Here are some good articles about the company:
- [http://www.bio-itworld.com/2010/issues/sept-oct/solexa.html](http://www.bio-itworld.com/2010/issues/sept-oct/solexa.html) ([archive](https://web.archive.org/web/20190411005034/http://www.bio-itworld.com/2010/issues/sept-oct/solexa.html)).

Cambridge visitors can still visit the [Panton Arms pub](https://pantonarms.co.uk/), which was the location of the legendary "hey we should talk" founders meeting, chosen due to its proximity to the chemistry department of the [University of Cambridge](university.md#university-of-cambridge).

In 2021 the founders were awarded the [Breakthrough Prize](social-technology.md#breakthrough-prize). The third person awarded was Pascal Mayer. He was apparently at Serono Pharmaceutical Research Institute at the time of development. They do have a wiki page unlike Solexa: [https://en.wikipedia.org/wiki/Serono](https://en.wikipedia.org/wiki/Serono). They paid a 700 million fine in 2005 in the [United States](united-states.md), and sold out in 2006 to [Merck](biology.md#merck-group) for 10 billion USD.

Bibliography:
- [https://medium.com/@nick.mccooke/how-we-pioneered-next-generation-dna-sequencing-at-solexa-61bac41aedd2](https://medium.com/@nick.mccooke/how-we-pioneered-next-generation-dna-sequencing-at-solexa-61bac41aedd2) How We Pioneered Next Generation DNA Sequencing At Solexal by Nick McCooke 2025. This article series could be very interesting.

#### Oxford Nanopore Technologies

↑ **Parent:** [DNA sequencing company](#dna-sequencing-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Oxford_Nanopore_Technologies)

They put a lot of emphasis into [base calling](#base-calling). E.g.:
- they have used [FPGAs](computer-hardware.md#field-programmable-gate-array) to accelerate it on certain models: [https://twitter.com/nanopore/status/841671404588302338](https://twitter.com/nanopore/status/841671404588302338), sampe engineer: [https://www.linkedin.com/in/balaji-renganathan-31b98415/](https://www.linkedin.com/in/balaji-renganathan-31b98415/)

##### Oxford Nanopore Technologies product

↑ **Parent:** [Oxford Nanopore Technologies](#oxford-nanopore-technologies)

###### PromethION

↑ **Parent:** [Oxford Nanopore Technologies product](#oxford-nanopore-technologies-product)

###### Oxford Nanopore MinION

↑ **Parent:** [Oxford Nanopore Technologies product](#oxford-nanopore-technologies-product)

One of the sequencers made by [Oxford Nanopore Technologies](#oxford-nanopore-technologies).

The device has had several updates since however, notably of the pore proteins which are present in the critical flow cell consumable.

Official documentation: [https://nanoporetech.com/products/minion](https://nanoporetech.com/products/minion) ([archive](https://web.archive.org/web/20190825022606/https://nanoporetech.com/products/minion))

The following images of the device and its peripherals were taken during the experiment: [Section "How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it"](oxford-nanopore-river-bacteria.md).

<a id="image-top-view-of-a-closed-oxford-nanopore-minion"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/Oxford_Nanopore_MinION_top_cropped.jpg/330px-Oxford_Nanopore_MinION_top_cropped.jpg)

**[Figure 2](#image-top-view-of-a-closed-oxford-nanopore-minion). Top view of a closed Oxford Nanopore MinION**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_top_cropped.jpg).

<a id="image-side-view-of-an-oxford-nanopore-minion"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Oxford_Nanopore_MinION_side_cropped.jpg/250px-Oxford_Nanopore_MinION_side_cropped.jpg)

**[Figure 3](#image-side-view-of-an-oxford-nanopore-minion). Side view of an Oxford Nanopore MinION**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_side_cropped.jpg).

<a id="image-top-view-of-an-open-oxford-nanopore-minion"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0a/Oxford_Nanopore_MinION_top_open_cropped.jpg/120px-Oxford_Nanopore_MinION_top_open_cropped.jpg)

**[Figure 4](#image-top-view-of-an-open-oxford-nanopore-minion). Top view of an open Oxford Nanopore MinION**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_top_open_cropped.jpg).

<a id="image-oxford-nanopore-minion-side-usb"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Oxford_Nanopore_MinION_side_USB_cropped.jpg/500px-Oxford_Nanopore_MinION_side_USB_cropped.jpg)

**[Figure 5](#image-oxford-nanopore-minion-side-usb). Oxford Nanopore MinION side USB**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_side_USB_cropped.jpg).

<a id="image-oxford-nanopore-minion-flow-cell-package"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/81/Oxford_nanopore_MinION_flow_cell_package.jpg/330px-Oxford_nanopore_MinION_flow_cell_package.jpg)

**[Figure 6](#image-oxford-nanopore-minion-flow-cell-package). Oxford nanopore MinION flow cell package.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_nanopore_MinION_flow_cell_package.jpg).

<a id="image-oxford-nanopore-minion-flow-cell-front"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/00/Oxford_nanopore_MinION_flow_cell_front.jpg/500px-Oxford_nanopore_MinION_flow_cell_front.jpg)

**[Figure 7](#image-oxford-nanopore-minion-flow-cell-front). Oxford nanopore MinION flow cell front.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_nanopore_MinION_flow_cell_front.jpg).

<a id="image-oxford-nanopore-minion-flow-cell-back"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/Oxford_nanopore_MinION_flow_cell_back.jpg/960px-Oxford_nanopore_MinION_flow_cell_back.jpg)

**[Figure 8](#image-oxford-nanopore-minion-flow-cell-back). Oxford nanopore MinION flow cell back.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_nanopore_MinION_flow_cell_back.jpg).

<a id="image-oxford-nanopore-minion-flow-cell-pipette-loading"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Oxford_nanopore_MinION_flow_cell_pipette_loading.jpg/250px-Oxford_nanopore_MinION_flow_cell_pipette_loading.jpg)

**[Figure 9](#image-oxford-nanopore-minion-flow-cell-pipette-loading). Oxford nanopore MinION flow cell pipette loading.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_nanopore_MinION_flow_cell_pipette_loading.jpg).

<a id="image-oxford-nanopore-minion-connected-to-a-mac-via-usb"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/Oxford_Nanopore_MinION_connected_to_a_Mac_via_USB.jpg/330px-Oxford_Nanopore_MinION_connected_to_a_Mac_via_USB.jpg)

**[Figure 10](#image-oxford-nanopore-minion-connected-to-a-mac-via-usb). Oxford Nanopore MinION connected to a Mac via USB.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_connected_to_a_Mac_via_USB.jpg).

<a id="video-oxford-nanopore-minion-software-channels-pannel-on-mac"></a>
**[Video 5](#video-oxford-nanopore-minion-software-channels-pannel-on-mac). Oxford Nanopore MinION software channels pannel on Mac.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_software_channels_pannel_on_Mac.webm).

<h6 id="oxford-nanopore-river-bacteria">How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it</h6>

↑ **Parent:** [Oxford Nanopore MinION](#oxford-nanopore-minion)

[This section is present in another page, follow this link to view it.](oxford-nanopore-river-bacteria.md)

## De novo DNA synthesis

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/De_novo_synthesis)

As of 2018, [Ciro Santilli](ciro-santilli.md) believes that this could be [the next big thing](ciro-santilli.md#the-next-big-thing) in [biology](biology.md) technology.

"De novo" means "starting from scratch", that is: you type the desired sequence into a computer, and the synthesize it.

The "de novo" part is important, because it distinguishes this from the already well solved problem of duplicating DNA from an existing DNA template, which is what all our cells do daily, and which can already be done very efficiently [in vitro](linguistics.md#in-vitro) with [polymerase chain reaction](#polymerase-chain-reaction).

Many [companies are attempting to create more efficient de novo synthesis methods](#de-novo-dna-synthesis-company):
- [https://twistbioscience.com/](https://twistbioscience.com/)
- [https://www.evonetix.com/technology/](https://www.evonetix.com/technology/)
- [DNAScript](#dnascript)
- [https://www.ansabio.com/](https://www.ansabio.com/)
- [https://www.nuclera.com/](https://www.nuclera.com/)

Notably, the dream of most of those companies is to have a machine that sits on a lab bench, which synthesises whatever you want.

TODO current de novo synthesis costs/time to delivery after ordering a custom sequence.

The initial main applications are likely going to be:
- [polymerase chain reaction](#polymerase-chain-reaction) primers (determine which region will be amplified
- creating a custom sequence to be inserted in a [plasmid](#plasmid), i.e. [artificial gene synthesis](#artificial-gene-synthesis)
but the real pipe dream is building and bootstraping entire [artificial chromosomes](#artificial-chromosome)

News coverage:
- 2023-03 [https://twitter.com/sethbannon/status/1633848116154880001](https://twitter.com/sethbannon/status/1633848116154880001)> [AnsaBio](#ansabio) created the world's longest DNA oligo produced using de novo synthesis! 1,005 bases! 99.9% stepwise yield
- 2020-10-05 [https://www.nature.com/articles/s41587-020-0695-9](https://www.nature.com/articles/s41587-020-0695-9) "Enzymatic DNA synthesis enters new phase"

<a id="video-nuclera-edna-enzymatic-de-novo-dna-synthesis-explanatory-animation-2021"></a>
**[Video 6](#video-nuclera-edna-enzymatic-de-novo-dna-synthesis-explanatory-animation-2021). Nuclera eDNA enzymatic de novo DNA synthesis explanatory animation (2021)** [Source](https://vimeo.com/535484548). The video shows nicely how Nuclera's enzymatic DNA synthesis works:
- they provide blocked [nucleotides](#nucleotide) of a single type
- add them with the enzyme. They use a werid [DNA polymerase](protein.md#dna-polymerase) called [terminal deoxynucleotidyl transferase](protein.md#terminal-deoxynucleotidyl-transferase) that adds a base at a time to a single stranded DNA strand rather than copying from a template
- wash everything
- do deblocking reaction
- and then repeat until done

---

### De novo DNA synthesis company

↑ **Parent:** [De novo DNA synthesis](#de-novo-dna-synthesis)

#### AnsaBio

↑ **Parent:** [De novo DNA synthesis company](#de-novo-dna-synthesis-company)

- [https://ansabio.com/](https://ansabio.com/)
- [https://www.crunchbase.com/organization/ansa-biotechnologies](https://www.crunchbase.com/organization/ansa-biotechnologies)

#### Camena Bioscience

↑ **Parent:** [De novo DNA synthesis company](#de-novo-dna-synthesis-company)  
🏷️ **Tags:** [University of Cambridge spinout company](university.md#university-of-cambridge-spinout-company)

[https://www.camenabio.com/](https://www.camenabio.com/)

The third one from [Cambridge](united-kingdom.md#cambridge) after:
- [https://www.nuclera.com/](https://www.nuclera.com/)
- [https://www.evonetix.com/technology/](https://www.evonetix.com/technology/)

#### DNAScript

↑ **Parent:** [De novo DNA synthesis company](#de-novo-dna-synthesis-company)  
🏷️ **Tags:** [French company](company.md#french-company)

[http://dnascript.co/](http://dnascript.co/)

#### Touchlight Genetics

↑ **Parent:** [De novo DNA synthesis company](#de-novo-dna-synthesis-company)  
🏷️ **Tags:** [British company](company.md#british-company)

### Artificial gene synthesis

↑ **Parent:** [De novo DNA synthesis](#de-novo-dna-synthesis)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Artificial_gene_synthesis)

Using [de novo DNA synthesis](#de-novo-dna-synthesis) to synthesize a [genes](#gene) to later insert somewhere.

Note that this is a specific application of [de novo DNA synthesis](#de-novo-dna-synthesis), e.g. [polymerase chain reaction](#polymerase-chain-reaction) primers is another major application that does not imply creating genes.

#### Artificial chromosome

↑ **Parent:** [Artificial gene synthesis](#artificial-gene-synthesis)

Using [de novo DNA synthesis](#de-novo-dna-synthesis) to synthesize entire [Chromosomes](#chromosome).

### Species bootstrapping from DNA

↑ **Parent:** [De novo DNA synthesis](#de-novo-dna-synthesis)

Synthesizing the DNA itself is not the only problem however.

You then have to get that DNA into a working living form state so that normal cell processes can continue:
- for [viri](taxonomy.md#virus) see: [synthetic virus](#synthetic-virus)
- for bacteria, you have to inject it into a cell
- for placental animals, you also have to somehow simulate a compatible placenta. It is likely easier for eggs.

Multicellular questions:
- [https://biology.stackexchange.com/questions/8590/can-extinct-animals-be-cloned](https://biology.stackexchange.com/questions/8590/can-extinct-animals-be-cloned)

Apparently achieved for the first time in 2021: [https://www.jcvi.org/research/first-self-replicating-synthetic-bacterial-cell](https://www.jcvi.org/research/first-self-replicating-synthetic-bacterial-cell) by the [J. Craig Venter Institute](research-institute.md#j-craig-venter-institute).

#### Synthetic chromosome

↑ **Parent:** [Species bootstrapping from DNA](#species-bootstrapping-from-dna)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Synthetic_chromosome)

Basically a synonym for doing a large chunk of [de novo DNA synthesis](#de-novo-dna-synthesis).

#### Synthetic virus

↑ **Parent:** [Species bootstrapping from DNA](#species-bootstrapping-from-dna)  
🏷️ **Tags:** [Virus](taxonomy.md#virus)

Man-made [virus](taxonomy.md#virus)!

- [https://en.wikipedia.org/wiki/Synthetic_virology](https://en.wikipedia.org/wiki/Synthetic_virology)
- [https://en.wikipedia.org/wiki/Genetically_modified_virus](https://en.wikipedia.org/wiki/Genetically_modified_virus)
- [https://www.scientificamerican.com/article/is-it-possible-to-enginee/](https://www.scientificamerican.com/article/is-it-possible-to-enginee/)
- [https://www.npr.org/sections/health-shots/2019/05/22/723582726/scientists-modify-viruses-with-crispr-to-create-new-weapon-against-superbugs](https://www.npr.org/sections/health-shots/2019/05/22/723582726/scientists-modify-viruses-with-crispr-to-create-new-weapon-against-superbugs)

TODO: if we had cheap [de novo DNA synthesis](#de-novo-dna-synthesis), how hard would it be to bootstrap a virus culture from that? [https://github.com/cirosantilli/cirosantilli.github.io/issues/60](https://github.com/cirosantilli/cirosantilli.github.io/issues/60)

Is it easy to [transfect](#transfection) a cell with the synthesized DNA, and get it to generate full infectious viral particles?

If so, then [de novo DNA synthesis](#de-novo-dna-synthesis) would be very similar to 3D printed guns: [https://en.wikipedia.org/wiki/3D_printed_firearms](https://en.wikipedia.org/wiki/3D_printed_firearms).

It might already be possible to order dissimulated sequences online:
- [https://www.theguardian.com/world/2006/jun/14/terrorism.topstories3](https://www.theguardian.com/world/2006/jun/14/terrorism.topstories3)

##### DIY gun

↑ **Parent:** [Synthetic virus](#synthetic-virus)

<a id="video-the-unhinged-world-of-diy-guns-by-qxir"></a>
**[Video 7](#video-the-unhinged-world-of-diy-guns-by-qxir). The Unhinged World of DIY Guns by Qxir.** [Source](https://www.youtube.com/watch?v=Fu1NvEcjB4Q).

###### 3D-printed firearm

↑ **Parent:** [DIY gun](#diy-gun)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/3D-printed_firearm)

<a id="video-3d-printed-guns-are-easy-to-make-and-impossible-to-stop-by-vice-news-2018"></a>
**[Video 8](#video-3d-printed-guns-are-easy-to-make-and-impossible-to-stop-by-vice-news-2018). 3D Printed Guns Are Easy To Make And Impossible To Stop by VICE News (2018)** [Source](http://youtube.com/watch?v=dB25H7pD2jg).

#### Genome Project-Write

↑ **Parent:** [Species bootstrapping from DNA](#species-bootstrapping-from-dna)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genome_Project-Write)

#### Yeast artificial chromosome

↑ **Parent:** [Species bootstrapping from DNA](#species-bootstrapping-from-dna)  
🏷️ **Tags:** [Artificial chromosome](#artificial-chromosome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Yeast_artificial_chromosome)

## Epigenetics

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Epigenetics)

### DNA methylation

↑ **Parent:** [Epigenetics](#epigenetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DNA_methylation)

The first found and most important known [epigenetic](#epigenetics) marker.

Happens only on [adenine](#adenine) and [cytosine](#cytosine). [Adenine methylation](#adenine-methylation) is much less common in [mammal](taxonomy.md#mammal) than [cytosine](#cytosine) methylation, when people say "methylation" they often mean just cytosine methylation.

It often happens on [promoters](#promoter-genetics), where it inhibits [transcription](#transcription-biology).

#### History of DNA methylation research

↑ **Parent:** [DNA methylation](#dna-methylation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/History_of_DNA_methylation_research)

Incredible that there hasn't been a [Nobel Prize](nobel-prize.md) for it as of 2022, e.g. as mentioned at: [https://theconversation.com/no-nobel-but-epigenetics-finally-gets-the-recognition-it-deserves-18970](https://theconversation.com/no-nobel-but-epigenetics-finally-gets-the-recognition-it-deserves-18970)

Some old dudes getting another prize in 2016: [https://www.cuimc.columbia.edu/news/pioneers-epigenetics-awarded-horwitz-prize](https://www.cuimc.columbia.edu/news/pioneers-epigenetics-awarded-horwitz-prize)

#### Adenine methylation

↑ **Parent:** [DNA methylation](#dna-methylation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Adenine_methylation)

#### Bisulfite sequencing

↑ **Parent:** [DNA methylation](#dna-methylation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bisulfite_sequencing)

The main way to sequence [DNA methylation](#dna-methylation). Converts methylated [cytosine](#cytosine) to [uracil](#uracil), and then we can sequence those.

<a id="video-bisulfite-sequencing-by-henrik-s-lab-2020"></a>
**[Video 9](#video-bisulfite-sequencing-by-henrik-s-lab-2020). Bisulfite Sequencing by Henrik's Lab (2020)** [Source](https://www.youtube.com/watch?v=OcIazFGQv0g). Nothing much new that we don't understand from a single sentence in the animation. But hey, animations!

### Transgenerational epigenetic inheritance

↑ **Parent:** [Epigenetics](#epigenetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transgenerational_epigenetic_inheritance)

They are actually inheritable! But [alleles](biology.md#allele) are rare: [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5559844](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5559844)

<a id="image-to-rats-with-the-same-genome-differing-only-in-dna-methylation-with-a-different-tail-phenotype"></a>
![](https://upload.wikimedia.org/wikipedia/commons/b/b3/Cloned_mice_with_different_DNA_methylation.png)

**[Figure 11](#image-to-rats-with-the-same-genome-differing-only-in-dna-methylation-with-a-different-tail-phenotype). To rats with the same genome differing only in DNA methylation with a different tail phenotype.** [Source](https://commons.wikimedia.org/wiki/File:Cloned_mice_with_different_DNA_methylation.png).

## RNA

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RNA)

### Messenger RNA

↑ **Parent:** [RNA](#rna)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Messenger_RNA)

#### Alternative splicing

↑ **Parent:** [Messenger RNA](#messenger-rna)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Alternative_splicing)

### RNA secondary structure

↑ **Parent:** [RNA](#rna)

Analogous problem to the [secondary structure](protein.md#secondary-structure) of [proteins](protein.md). Likely a bit simpler due to the strong tendency for complementary pairs to bind.

#### RNA half-life prediction

↑ **Parent:** [RNA secondary structure](#rna-secondary-structure)

### Transcription (biology)

↑ **Parent:** [RNA](#rna)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transcription_(biology))

#### Post-transcriptional modification

↑ **Parent:** [Transcription (biology)](#transcription-biology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Post-transcriptional_modification)

#### Promoter (genetics)

↑ **Parent:** [Transcription (biology)](#transcription-biology)

A [DNA](dna.md) sequence that marks the start of a [transcription](#transcription-biology) area.

##### Transcriptional regulation

↑ **Parent:** [Promoter (genetics)](#promoter-genetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transcriptional_regulation)

#### RNA polymerase

↑ **Parent:** [Transcription (biology)](#transcription-biology)  
🏷️ **Tags:** [Enzyme](protein.md#enzyme)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RNA_polymerase)

Converts [DNA](dna.md) to [RNA](#rna).

##### RNA-dependent RNA polymerase

↑ **Parent:** [RNA polymerase](#rna-polymerase)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RNA-dependent_RNA_polymerase)

Makes [RNA](#rna) from [RNA](#rna).

Used in [Positive-strand RNA virus](taxonomy.md#positive-strand-rna-virus) to replicate.

I don't think it's present outside viruses. Well regulated organisms just [transcribe](#transcription-biology) more [DNA](dna.md) instead.

#### Operon

↑ **Parent:** [Transcription (biology)](#transcription-biology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Operon)

Sequence of genes under a single [promoter](#promoter-genetics). For an example, see [E. Coli K-12 MG1655 operon thrLABC](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc).

A single [operon](#operon) may produce multiple different [transcription units](#transcription-unit) depending on certain conditions, see: [operon vs transcription unit](#operon-vs-transcription-unit).

##### Transcription unit

↑ **Parent:** [Operon](#operon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transcription_unit)

A sequence of [mRNA](#messenger-rna) that can actually be [transcribed](#transcription-biology).

For an example, see [E. Coli K-12 MG1655 operon thrLABC](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc).

Multiple different transcription units can be produced by a single [operon](#operon), see: [operon vs transcription unit](#operon-vs-transcription-unit).

##### Operon vs transcription unit

↑ **Parent:** [Operon](#operon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Operon_vs_transcription_unit)

Consider the [E. Coli K-12 MG1655 operon thrLABC](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc).

That single [operon](#operon) can produce two different [mRNA](#messenger-rna) [transcription units](#transcription-unit):
- thrL only, the transcription unit is also called thrL: [https://biocyc.org/ECOLI/NEW-IMAGE?object=TU0-42486](https://biocyc.org/ECOLI/NEW-IMAGE?object=TU0-42486)
- thrL + thrA + thrB + thrC all together, the transcription unit is called thrLABC: [https://biocyc.org/ECOLI/NEW-IMAGE?type=OPERON&object=TU00178](https://biocyc.org/ECOLI/NEW-IMAGE?type=OPERON&object=TU00178)

The reason for this appears to be that there is a [rho-independent termination](#intrinsic-termination) region after thrL. But then under certain conditions, that must get innactivated, and then the thrLABC is produced instead.

##### Polycistronic mRNA

↑ **Parent:** [Operon](#operon)

Multiple [genes](#gene) coding for multiple [proteins](protein.md) in one [transcription unit](#transcription-unit), e.g. [e. Coli K-12 MG1655 gene thrL](taxonomy.md#e-coli-k-12-mg1655-gene-thrl) and [e. Coli K-12 MG1655 gene thrA](taxonomy.md#e-coli-k-12-mg1655-gene-thra) are both prat of the [E. Coli K-12 MG1655 operon thrLABC](taxonomy.md#e-coli-k-12-mg1655-operon-thrlabc).

#### Transcription factor

↑ **Parent:** [Transcription (biology)](#transcription-biology)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transcription_factor)

##### Intrinsic termination

↑ **Parent:** [Transcription factor](#transcription-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Intrinsic_termination)

### Type of RNA

↑ **Parent:** [RNA](#rna)

The most important ones are:
- [mRNA](#messenger-rna)
- [tRNA](cell.md#transfer-rna)
- [rRNA](cell.md#ribosomal-rna)

## Nucleotide

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nucleotide)

### Nucleobase

↑ **Parent:** [Nucleotide](#nucleotide)

#### Adenine

↑ **Parent:** [Nucleobase](#nucleobase)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Adenine)

#### Cytosine

↑ **Parent:** [Nucleobase](#nucleobase)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cytosine)

#### Thymine

↑ **Parent:** [Nucleobase](#nucleobase)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Thymine)

#### Uracil

↑ **Parent:** [Nucleobase](#nucleobase)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Uracil)

Replaces [Thymine](#thymine) in [RNA](#rna).

##### Uracil vs thymine

↑ **Parent:** [Uracil](#uracil)

- [https://byjus.com/neet-questions/why-does-dna-contain-thymine-and-rna-uracil](https://byjus.com/neet-questions/why-does-dna-contain-thymine-and-rna-uracil) says [Uracil](#uracil) cannot be repaired by [DNA repair](#dna-repair) mechanisms. But it is also requires less energy to synthesize with.

## Base pair

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Base_pair)

## Genetic code

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genetic_code)

### Reading frame

↑ **Parent:** [Genetic code](#genetic-code)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Reading_frame)

There are six, three in each sense, depending on where you start [modulo](mathematics.md#modulo-operation)-3.

#### Open reading frame

↑ **Parent:** [Reading frame](#reading-frame)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Open_reading_frame)

Area between a [start codon](#start-codon) and an [stop codon](#stop-codon).

This term is useful because:
- there are some crazy constructs, notably in viruses, in which there's more than one gene in a single orf
- [post-transcriptional modifications](#post-transcriptional-modification) can throw out parts of the sequence

##### NCBI open reading frame tool

↑ **Parent:** [Open reading frame](#open-reading-frame)

[NCBI](biology.md#national-center-for-biotechnology-information) online tool to find and view all [open reading frames](#open-reading-frame) in a given [FASTA](biology.md#fasta-format): [https://www.ncbi.nlm.nih.gov/orffinder/](https://www.ncbi.nlm.nih.gov/orffinder/)

### Codon

↑ **Parent:** [Genetic code](#genetic-code)

#### Start codon

↑ **Parent:** [Codon](#codon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Start_codon)

#### Stop codon

↑ **Parent:** [Codon](#codon)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Stop_codon)

## Genetics

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genetics)

High level [DNA](dna.md) studies? :-)

### Genetics company

↑ **Parent:** [Genetics](#genetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genetics_company)

#### 23andMe

↑ **Parent:** [Genetics company](#genetics-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/23andMe)

### Population genetics

↑ **Parent:** [Genetics](#genetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Population_genetics)

### Evolutionary genetics

↑ **Parent:** [Genetics](#genetics)

#### DNA replication is a key limiting factor of bacterial replication time

↑ **Parent:** [Evolutionary genetics](#evolutionary-genetics)

TODO confirm, but looks like it, e.g. [E. Coli starts DNA replication before the previous one finished](taxonomy.md#e-coli-starts-dna-replication-before-the-previous-one-finished).

##### It is hard for complex organisms to evolve because longer DNA means longer replication time

↑ **Parent:** [DNA replication is a key limiting factor of bacterial replication time](#dna-replication-is-a-key-limiting-factor-of-bacterial-replication-time)

Because [DNA replication is a key limiting factor of bacterial replication time](#dna-replication-is-a-key-limiting-factor-of-bacterial-replication-time), such organisms are therefore strongly incentivized to have very minimal DNAs.

[Power, Sex, Suicide by Nick Lane (2006)](cell.md#power-sex-suicide-by-nick-lane-2006) 7 "Why bacteria are simple" page 169 puts this nicely:

> Bacteria replicate at colossal speed. \[...\] In two days, the mass of exponentially doubling E. coli would be 2664 times larger than the mass of the [Earth](astronomy.md#earth).
> 
> Luckily this does not happen, and the reason is that bacteria are normally half starved. They swiftly consume all available food, whereupon their growth is limited once again by the lack of nutrients. Most bacteria spend most of their lives in stasis, waiting for a meal. Nonetheless, the speed at which bacteria do mobilize themselves to replicate upon feeding illustrates the overwhelming strength of the selection pressures at work.

### Comparative genomics

↑ **Parent:** [Genetics](#genetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Comparative_genomics)

#### Parasites tend to have smaller DNAs

↑ **Parent:** [Comparative genomics](#comparative-genomics)

If you live in the relatively food abundant environment of another cell, then you don't have to be able to digest every single food source in existence, of defend against a wide range of predators.

So because [DNA replication is a key limiting factor of bacterial replication time](#dna-replication-is-a-key-limiting-factor-of-bacterial-replication-time), you just reduce your genome to a minimum.

And likely you also want to be as small as possible to evade the host's [immune system](biology.md#immune-system).

[Power, Sex, Suicide by Nick Lane (2006)](cell.md#power-sex-suicide-by-nick-lane-2006) section "Gene loss as an evolutionary trajectory" puts it well:

> One of the most extreme examples of gene loss is Rickettsia prowazekii, the cause of typhus. \[...\] Over evolutionary time Rickettsia has lost most of its genes, and now has a mere  protein-coding genes left. \[...\] Rickettsia is a tiny bacterium, almost as small as a virus, which lives as a parasite inside other cells. It is so well adapted to this lifestyle that it can no longer survive outside its host cells. \[...\] It was able to lose most of its genes in this way simply because they were not needed: life inside other cells, if you can survive there at all, is a spoonfed existence.

and also section "How to lose the cell wall without dying" page 184 has some related mentions:

> While many types of bacteria do lose their cell wall during parts of their life cycle only two groups of prokaryotes have succeeded in losing their cell walls permanently, yet lived to tell the tale. It's interesting to consider the extenuating circumstances that permitted them to do so.
> 
> \[...\]
> 
> One group, the Mycoplasma, comprises mostly parasites, many of which live inside other cells. Mycoplasma cells are tiny, with very small genomes. M. genitalium, discovered in 1981, has the smallest known genome of any bacterial cell, encoding fewer than 500 genes. [M. genitalium](taxonomy.md#mycoplasma-genitalium), discovered in 1981, has the smallest known genome of any bacterial cell, encoding fewer than 500 genes. \[...\] Like Rickettsia, Mycoplasma have lost virtually all the genes required for making nucleotides, [amino acids](protein.md#amino-acid), and so forth.

#### Homology (biology)

↑ **Parent:** [Comparative genomics](#comparative-genomics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Homology_(biology))

##### Ortholog

↑ **Parent:** [Homology (biology)](#homology-biology)

A gene that was inherited from the same ancestor in two different species, and which has maintained the same function in both species.

##### Paralog

↑ **Parent:** [Homology (biology)](#homology-biology)

A [gene](#gene) that got duplicated withing the same species. The copies may diverge in function from the original.

Important example: [hox genes](taxonomy.md#hox-gene).

### Phenotype

↑ **Parent:** [Genetics](#genetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phenotype)

### Transposable element

↑ **Parent:** [Genetics](#genetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transposable_element)

## Gene

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gene)

### Genome

↑ **Parent:** [Gene](#gene)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genome)

#### Genomics

↑ **Parent:** [Genome](#genome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Genomics)

Study of the [genome](#genome), one of the [omics](biology.md#omics).

### Non-coding DNA

↑ **Parent:** [Gene](#gene)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Non-coding_DNA)

## Mutation

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mutation)

### Mutagen

↑ **Parent:** [Mutation](#mutation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mutagen)

### DNA mutation type

↑ **Parent:** [Mutation](#mutation)

#### Indel

↑ **Parent:** [DNA mutation type](#dna-mutation-type)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Indel)

#### Single-nucleotide polymorphism

↑ **Parent:** [DNA mutation type](#dna-mutation-type)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Single-nucleotide_polymorphism)

### Slipped strand mispairing

↑ **Parent:** [Mutation](#mutation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Slipped_strand_mispairing)

The cause of [variable number tandem repeat](#variable-number-tandem-repeat).

## Horizontal gene transfer

↑ **Parent:** [DNA](dna.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Horizontal_gene_transfer)

Ways in which it can happen:
- [bacterial conjugation](taxonomy.md#bacterial-conjugation)

<a id="image-graph-of-life"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Tree_Of_Life_%28with_horizontal_gene_transfer%29.svg" alt="" height="600">

**[Figure 12](#image-graph-of-life). Graph of life**. [Source](https://commons.wikimedia.org/wiki/File:Tree_Of_Life_%28with_horizontal_gene_transfer%29.svg). [horizontal gene transfer](#horizontal-gene-transfer) transforms the [tree of life](taxonomy.md#phylogenetic-tree) into the graph of life! Fuck my life.

### Transduction (genetics)

↑ **Parent:** [Horizontal gene transfer](#horizontal-gene-transfer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transduction_(genetics))

### Transformation (genetics)

↑ **Parent:** [Horizontal gene transfer](#horizontal-gene-transfer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transformation_(genetics))

[Current Wikipedia](https://en.wikipedia.org/w/index.php?title=Horizontal_gene_transfer&oldid=1078227723) seems to say that this refers specifically to cells taking up DNA from other dead cells as in the [Avery-MacLeod-McCarty experiment](#avery-macleod-mccarty-experiment), excluding other types of [horizontal gene transfer](#horizontal-gene-transfer) like [bacterial conjugation](taxonomy.md#bacterial-conjugation)

The term is sometimes just used a synonym for [horizontal gene transfer](#horizontal-gene-transfer) in general it seems however.

#### Avery-MacLeod-McCarty experiment

↑ **Parent:** [Transformation (genetics)](#transformation-genetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Avery–MacLeod–McCarty_experiment)

#### Transfection

↑ **Parent:** [Transformation (genetics)](#transformation-genetics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transfection)

## ↑ Ancestors (6)

1. [Molecular biology](molecular-biology.md)
2. [Level of organization of bodies](biology.md#level-of-organization-of-bodies)
3. [Biology](biology.md)
4. [Natural science](science.md#natural-science)
5. [Science](science.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (23)

- [100 Greatest Discoveries by the Discovery Channel (2004-2005)](science.md#100-greatest-discoveries-by-the-discovery-channel-2004-2005)
- [A Structure for Deoxyribose Nucleic Acid](brain.md#a-structure-for-deoxyribose-nucleic-acid)
- [Animation of molecular biology processes](science.md#animation-of-molecular-biology-processes)
- [DNA microarray](#dna-microarray)
- [E. Coli Whole Cell Model by Covert Lab](e-coli-whole-cell-model-by-covert-lab.md)
- [Mass fraction summary plot analysis](e-coli-whole-cell-model-by-covert-lab.md#mass-fraction-summary-plot-analysis)
- [Output overview](e-coli-whole-cell-model-by-covert-lab.md#output-overview)
- [Source code overview](e-coli-whole-cell-model-by-covert-lab.md#source-code-overview)
- [Genetics](#genetics)
- [Human mitochondrion](cell.md#human-mitochondrion)
- [Molecular biology feels like systems programming](systems-programming.md#molecular-biology-feels-like-systems-programming)
- [Molecular biology technologies](ciro-santilli.md#molecular-biology-technologies)
- [OpenWorm](taxonomy.md#openworm)
- [Overview of the experiment](oxford-nanopore-river-bacteria.md#overview-of-the-experiment)
- [Physics and the illusion of life](science.md#physics-and-the-illusion-of-life)
- [Promoter (genetics)](#promoter-genetics)
- [Protein tag](molecular-biology.md#protein-tag)
- [Reverse transcriptase](taxonomy.md#reverse-transcriptase)
- [RNA-dependent RNA polymerase](#rna-dependent-rna-polymerase)
- [RNA polymerase](#rna-polymerase)
- [RNA-Seq](#rna-seq)
- [Sequence alignment](biology.md#sequence-alignment)
- [Sonicator](molecular-biology.md#sonicator)
