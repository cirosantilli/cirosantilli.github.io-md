# How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it

↑ **Parent:** [Oxford Nanopore MinION](dna.md#oxford-nanopore-minion)  
🏷️ **Tags:** [The best articles by Ciro Santilli](articles.md), [DNA sequencing](dna.md#dna-sequencing), [Metagenomics](dna.md#metagenomics), [Polymerase chain reaction](dna.md#polymerase-chain-reaction)

<a id="_5"></a>
This article gives an idea of how this kind of biological experiment feels like to a [software engineer](software.md#software-engineer) who has never done any [biology](biology.md) like [Ciro Santilli](ciro-santilli.md).

**Table of contents**

- [Experiment background](#experiment-background)
- [Overview of the experiment](#overview-of-the-experiment)
  - [Why Oxford Nanopore was used instead of Illumina for the sequencing](#why-oxford-nanopore-was-used-instead-of-illumina-for-the-sequencing)
- [Sample collection](#sample-collection)
- [DNA extraction](#dna-extraction)
  - [Filtration with vacuum pump](#filtration-with-vacuum-pump)
  - [Post filtration purification](#post-filtration-purification)
- [PCR](#pcr)
  - [PCR verification with gel electrophoresis](#pcr-verification-with-gel-electrophoresis)
- [Sequencing](#sequencing)
  - [Pre-sequencing preparation](#pre-sequencing-preparation)
  - [Using the Oxford Nanopore](#using-the-oxford-nanopore)
- [Bioinformatics](#bioinformatics)
- [Conclusions](#conclusions)
- [Protocols used](#protocols-used)
  - [Qiagen DNeasy PowerWater Kit](#qiagen-dneasy-powerwater-kit)
  - [Qiagen QIAquick PCR Purification Kit](#qiagen-qiaquick-pcr-purification-kit)
  - [Oxford Nanopore SQK-LSK109 Ligation Sequencing Kit](#oxford-nanopore-sqk-lsk109-ligation-sequencing-kit)
- [Equipment used](#equipment-used)
  - [Thermo Scientific Nalgene Polysulfone Reusable Bottle Top Filters](#thermo-scientific-nalgene-polysulfone-reusable-bottle-top-filters)
  - [KNF Laboport series laboratory vacuum pump](#knf-laboport-series-laboratory-vacuum-pump)
  - [Scientific Industries Inc. Vortex-Genie 2](#scientific-industries-inc-vortex-genie-2)
  - [VWR Micro Star 17 microcentrifuge](#vwr-micro-star-17-microcentrifuge)
  - [VELP Scientifica WIZARD IR Infrared Vortex Mixer](#velp-scientifica-wizard-ir-infrared-vortex-mixer)
  - [Marshal Scientific MJ Research PTC-200 Thermal Cycler](#marshal-scientific-mj-research-ptc-200-thermal-cycler)
  - [GE MagRack 6](#ge-magrack-6)
  - [BTLab Systems Mini Centrifuge](#btlab-systems-mini-centrifuge)
  - [Fisher Scientific UVP LM-26E Benchtop 2UV Transilluminator](#fisher-scientific-uvp-lm-26e-benchtop-2uv-transilluminator)
  - [Biochrom SimpliNano spectrophotometer](#biochrom-simplinano-spectrophotometer)
- [External links to this page](#external-links-to-this-page)

## Experiment background

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_6"></a>
[PuntSeq](https://www.puntseq.co.uk/) is a side project led by a few [University of Cambridge](university.md#university-of-cambridge) [PhDs](education.md#doctor-of-philosophy) that aims to determine which [bacteria](taxonomy.md#bacteria) are present in the [River Cam](https://en.wikipedia.org/wiki/River_Cam).

<a id="_7"></a>
In July 2019, the PuntSeq team got together with the awesome [Cambridge Biomakespace](https://biomake.space), an awesome biology makerspace open to all, to create a two day science outreach activity showing their procedures.

<a id="_8"></a>
The data collected in this experiment, together with other collection sessions done by the organizers actually led to a publication on [eLife](education.md#elife): [https://elifesciences.org/articles/61504](https://elifesciences.org/articles/61504) "Freshwater monitoring by nanopore sequencing" by Lara Urban et al. (2021), so it is awesome to see that were are actual being part of "real science".

<a id="_9"></a>
Ciro knows nothing about biology, but since he is [very curious about it](ciro-santilli.md#molecular-biology-technologies), he jumped at this opportunity, and decided to document things as well as his limited knowledge would allow.

<a id="_10"></a>
All participants chipped in some money to help cover the experiment's costs. Ciro suspects that this activity was done partially to help crowdfund the experiment, but it was a worthy investment!

<a id="_11"></a>
The impressions you get from the experiment as a software engineer will be:<a id="_12"></a>

<a id="_13"></a>
- OMG, this is so labour intensive, why haven't they automated this
<a id="_14"></a>
- OMG, this is frightening, all the 8 hours of work I've just done are present in that tiny plastic tube
<a id="_15"></a>
- Amazing! Look at that apparatus! And the bio people are like: I've used this a million times, it's cheap and every lab has one, just work faster and don't break you piece of junk!

## Overview of the experiment

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_16"></a>
For those that know biology and just want to do the thing, see: [Section 9. "Protocols used"](#protocols-used).

<a id="_17"></a>
The PuntSeq team uses an [Oxford Nanopore MinION](dna.md#oxford-nanopore-minion) [DNA sequencer](dna.md#dna-sequencing) made by [Oxford Nanopore Technologies](dna.md#oxford-nanopore-technologies) to sequence the [16S](cell.md#16s-ribosomal-rna) region of bacterial [DNA](dna.md), which is about 1500 nucleotides long.

<a id="_18"></a>
This kind of "decode everything from the sample to see what species are present approach" is called "[metagenomics](dna.md#metagenomics)".

<a id="_19"></a>
This is how the MinION looks like: [Figure 1. "Oxford Nanopore MinION top"](#image-oxford-nanopore-minion-top).

<a id="image-oxford-nanopore-minion-top"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/Oxford_Nanopore_MinION_top_cropped.jpg/330px-Oxford_Nanopore_MinION_top_cropped.jpg)

**[Figure 1](#image-oxford-nanopore-minion-top). Oxford Nanopore MinION top**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_top_cropped.jpg).

<a id="image-oxford-nanopore-minion-side"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Oxford_Nanopore_MinION_side_cropped.jpg/250px-Oxford_Nanopore_MinION_side_cropped.jpg)

**[Figure 2](#image-oxford-nanopore-minion-side). Oxford Nanopore MinION side**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_side_cropped.jpg).

<a id="image-oxford-nanopore-minion-top-open"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0a/Oxford_Nanopore_MinION_top_open_cropped.jpg/120px-Oxford_Nanopore_MinION_top_open_cropped.jpg" alt="" height="500">

**[Figure 3](#image-oxford-nanopore-minion-top-open). Oxford Nanopore MinION top open**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_top_open_cropped.jpg).

<a id="image-oxford-nanopore-minion-side-usb"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Oxford_Nanopore_MinION_side_USB_cropped.jpg/500px-Oxford_Nanopore_MinION_side_USB_cropped.jpg)

**[Figure 4](#image-oxford-nanopore-minion-side-usb). Oxford Nanopore MinION side USB**. [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_side_USB_cropped.jpg).

<a id="_20"></a>
The 16S region codes for one of the [RNA](dna.md#rna) pieces that makes the [bacterial ribosome](https://en.wikipedia.org/w/index.php?title=Ribosome&oldid=912600990#Bacterial_ribosomes).

<a id="_21"></a>
Before [sequencing the DNA](#sequencing), we will do a [PCR](#pcr) with primers that fit just before and just after the 16S DNA, in well conserved regions expected to be present in all bacteria.

<a id="_22"></a>
The PCR replicates only the DNA region between our two selected primers a gazillion times so that only those regions will actually get picked up by the sequencing step in practice.

<a id="_23"></a>
[Eukaryotes](taxonomy.md#eukaryote) also have an analogous ribosome part, the 18S region, but the PCR primers are selected for targets around the 16S region which are only present in prokaryotes.

<a id="_24"></a>
This way, we amplify only the 16S region of bacteria, excluding other parts of bacterial genome, and excluding eukaryotes entirely.

<a id="_25"></a>
Despite coding such a fundamental piece of RNA, there is still surprisingly variability in the 16S region across different bacteria, and it is those differences will allow us to identify which bacteria are present in the river.

<a id="_26"></a>
The variability exists because certain base pairs are not fundamental for the function of the 16S region. This variability happens mostly on [RNA loops as opposed to stems](https://en.wikipedia.org/wiki/Stem-loop), i.e. parts of the RNA that don't base pair with other RNA in the [RNA secondary structure](https://en.wikipedia.org/wiki/Nucleic_acid_secondary_structure) as shown at: [Code 1. "RNA stem-loop structure"](#code-rna-stem-loop-structure).

<a id="code-rna-stem-loop-structure"></a>
```
                A-U
               /   \
A-U-C-G-A-U-C-G     C
| | | | | | | |     |
U-A-G-C-U-A-G-C     G
               \   /
                U-A
|             ||    |
+-------------++----+
    stem        loop
```

<a id="_27"></a>
This is how the 16S RNA secondary structure looks like in its full glory: [Figure 5. "16S RNA secondary structure"](#image-16s-rna-secondary-structure).

<a id="image-16s-rna-secondary-structure"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/a/a6/16S.svg" alt="height=800" height="500">

**[Figure 5](#image-16s-rna-secondary-structure). 16S RNA secondary structure**. [Source](https://commons.wikimedia.org/wiki/File:16S.svg).

<a id="_28"></a>
Since loops don't base pair, they are less crucial in the determination of the secondary structure of the RNA.

<a id="_29"></a>
The variability is such that it is possible to identify individual species apart if full sequences are known with certainty.

<a id="_30"></a>
With the experimental limitations of experiment however, we would only be able to obtain [family](https://en.wikipedia.org/wiki/Family_(biology)) or [genus](https://en.wikipedia.org/wiki/Genus) level breakdowns.

### Why Oxford Nanopore was used instead of Illumina for the sequencing

↑ **Parent:** [Overview of the experiment](#overview-of-the-experiment)

<a id="_31"></a>
At the time of the experiment, [Illumina](dna.md#illumina) equipment was cheaper per base pair and dominates the [human genome](human.md#human-genome) sequencing market, but it required a much higher initial investment for the equipment (TODO how much).

<a id="_32"></a>
The reusable Nanopore device costs just [about 500 dollars](https://web.archive.org/web/20190717141155/https://store.nanoporetech.com/starter-packs/), and [about 500 dollars (50 unit volume)](https://web.archive.org/web/20190911092809/https://store.nanoporetech.com/flowcells.html) for the single usage flow cell which can decode up to 30 billion base pairs, which is about 10 human genomes 1x! Note that 1x is basically useless for one of the most important of all applications of sequencing: detection of [single-nucleotide polymorphisms](dna.md#single-nucleotide-polymorphism), since the error rate would be too high to base clinical decisions on.

<a id="_33"></a>
Compare that to Illumina which is currently doing about an 1000 dollar human genome at 30x, and a bit less errors per base pair (TODO how much).

<a id="_34"></a>
Other advantages of the MinION over Illumina which didn't really matter to this particular experiment are:<a id="_35"></a>

<a id="_36"></a>
- <a id="_37"></a>
  portability for e.g. to do analysis on the field near infections outbreaks. Compare that to the smallest Illumina sequencer currently available in 2019, the iSeq 100: [Figure 6. "Illumina iSeq 100 DNA sequencer"](#image-illumina-iseq-100-dna-sequencer).

  <a id="image-illumina-iseq-100-dna-sequencer"></a>
  ![](https://web.archive.org/web/20190922113448if_/https://www.illumina.com/content/dam/illumina-marketing/images/systems/v2/web-graphic/iseq-100-demo-video-thumbnail-web-graphic.jpg)

  **[Figure 6](#image-illumina-iseq-100-dna-sequencer). Illumina iSeq 100 DNA sequencer**. [Source](https://www.illumina.com/systems/sequencing-platforms/iseq.html).
<a id="_38"></a>
- long reads which can be necessary for long repetitive regions, see also: [Section "Sequence alignment"](biology.md#sequence-alignment)

## Sample collection

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_39"></a>
As you would expect, not much secret here, we just dumped a 1 liter glass bottle with a rope attached around the neck in a few different locations of the river, and pulled it out with the rope.

<a id="_40"></a>
And, in the name of science, we even wore gloves to not contaminate the samples!

<a id="image-swans-swimming-in-the-river-when-during-sample-collection"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/River_water_sample_collection_swans.jpg/960px-River_water_sample_collection_swans.jpg)

**[Figure 7](#image-swans-swimming-in-the-river-when-during-sample-collection). Swans swimming in the river when during sample collection**. [Source](https://commons.wikimedia.org/wiki/File:River_water_sample_collection_swans.jpg). Swam poo bacteria?

<a id="image-tying-rope-to-bootle-for-river-water-sample-collection"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a9/River_water_sample_collection_tie_rope_to_bottle.jpg/330px-River_water_sample_collection_tie_rope_to_bottle.jpg" alt="" height="400">

**[Figure 8](#image-tying-rope-to-bootle-for-river-water-sample-collection). Tying rope to bootle for river water sample collection**. [Source](https://commons.wikimedia.org/wiki/File:River_water_sample_collection_tie_rope_to_bottle.jpg).

<a id="image-dumping-the-bottle-into-the-river-to-collect-the-water-sample"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9b/River_water_sample_collection_get_sample.jpg/330px-River_water_sample_collection_get_sample.jpg" alt="" height="400">

**[Figure 9](#image-dumping-the-bottle-into-the-river-to-collect-the-water-sample). Dumping the bottle into the river to collect the water sample**. [Source](https://commons.wikimedia.org/wiki/File:River_water_sample_collection_get_sample.jpg).

<a id="image-measuring-the-river-water-sample-temperature-with-a-mercury-thermometer"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/River_water_sample_collection_measure_temperature.jpg/330px-River_water_sample_collection_measure_temperature.jpg" alt="" height="400">

**[Figure 10](#image-measuring-the-river-water-sample-temperature-with-a-mercury-thermometer). Measuring the river water sample temperature with a mercury thermometer**. [Source](https://commons.wikimedia.org/wiki/File:River_water_sample_collection_measure_temperature.jpg).

<a id="image-measuring-the-river-water-sample-ph-with-a-ph-strip"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/River_water_sample_collection_read_PH_strip.jpg/330px-River_water_sample_collection_read_PH_strip.jpg" alt="" height="400">

**[Figure 11](#image-measuring-the-river-water-sample-ph-with-a-ph-strip). Measuring the river water sample pH with a pH strip**. [Source](https://commons.wikimedia.org/wiki/File:River_water_sample_collection_read_PH_strip.jpg). The strip is compared with the color of a [mobile app](computer-hardware.md#mobile-app) that gives the pH for a given strip color.

<a id="image-noting-sample-collection-location-on-the-water-bottle"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0a/River_water_sample_collection_identify_bottle.jpg/330px-River_water_sample_collection_identify_bottle.jpg" alt="" height="400">

**[Figure 12](#image-noting-sample-collection-location-on-the-water-bottle). Noting sample collection location on the water bottle**. [Source](https://commons.wikimedia.org/wiki/File:River_water_sample_collection_identify_bottle.jpg).

<a id="video-dumping-the-bottle-into-the-river-to-collect-the-water-sample"></a>
**[Video 1](#video-dumping-the-bottle-into-the-river-to-collect-the-water-sample). Dumping the bottle into the river to collect the water sample.** [Source](https://commons.wikimedia.org/wiki/File:River_water_sample_collection_with_a_bottle_and_string.ogv). That was fun.

## DNA extraction

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_41"></a>
The first thing we had to do with the sample was to extract the DNA present in the water in a pure form for the PCR.

<a id="_42"></a>
We did that with a [Qiagen DNeasy PowerWater Kit](#qiagen-dneasy-powerwater-kit).

<a id="_43"></a>
As you would expect, this consists of a purification procedure with several steps.

<a id="_44"></a>
In each step we take a physical or chemical action on the sample, which splits it into two parts: the one with the DNA and the one without.

<a id="_45"></a>
We then take the part with the DNA, and throw away the one without the DNA.

<a id="_46"></a>
The first steps are coarser, and finer and finer splits are done as we move forward.

### Filtration with vacuum pump

↑ **Parent:** [DNA extraction](#dna-extraction)

<a id="_47"></a>
The first thing we did was to filter the water samples with a membrane filter that is so fine that not even bacteria can pass through, but water can.

<a id="_48"></a>
Therefore, after filtration, we would have all particles such as bacteria and larger dirt pieces in the filter.

<a id="_49"></a>
From the 1 liter in each bottle, we only used 400 ml because previous experiments showed that filtering the remaining 600 ml is very time consuming because the membrane filter gets clogged up.

<a id="_50"></a>
Therefore, the filtration step allows us to reduce those 400 ml volumes to more manageable [Eppendorf tube](molecular-biology.md#eppendorf-tube) volumes: [Figure 13. "An Eppendorf tube"](#image-an-eppendorf-tube). Reagents are expensive, and lab bench centrifuges are small!

<a id="image-an-eppendorf-tube"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Microcentrifuge_tube_in_hand.jpg/500px-Microcentrifuge_tube_in_hand.jpg)

**[Figure 13](#image-an-eppendorf-tube). An Eppendorf tube**. [Source](https://commons.wikimedia.org/wiki/File:Microcentrifuge_tube_in_hand.jpg). They are small, convenient and disposable.

<a id="image-labelled-eppendorf-tubes-on-a-rack"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Labelled_Eppendorf_microcentrifuge_tubes_on_rack.jpg/500px-Labelled_Eppendorf_microcentrifuge_tubes_on_rack.jpg)

**[Figure 14](#image-labelled-eppendorf-tubes-on-a-rack). Labelled Eppendorf tubes on a rack**. [Source](https://commons.wikimedia.org/wiki/File:Labelled_Eppendorf_microcentrifuge_tubes_on_rack.jpg).

<a id="_51"></a>
Since the filter is so fine, filtering by gravity alone would take forever, and so we used a vacuum pump to speed thing up!

<a id="_52"></a>
For that we used:<a id="_53"></a>

<a id="_54"></a>
- [Thermo Scientific Nalgene Polysulfone Reusable Bottle Top Filters](#thermo-scientific-nalgene-polysulfone-reusable-bottle-top-filters)
<a id="_55"></a>
- [KNF Laboport series laboratory vacuum pump](#knf-laboport-series-laboratory-vacuum-pump)

<a id="image-peeling-the-vacuum-pump-filter-protection-peel-before-usage"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/6/6e/Vacuum_pump_filter_peel_filter.png" alt="" height="400">

**[Figure 15](#image-peeling-the-vacuum-pump-filter-protection-peel-before-usage). Peeling the vacuum pump filter protection peel before usage**. [Source](https://commons.wikimedia.org/wiki/File:Vacuum_pump_filter_peel_filter.png).

<a id="image-placing-the-vacuum-pump-filter"></a>
![](https://upload.wikimedia.org/wikipedia/commons/7/78/Vacuum_pump_filter_place_filter.png)

**[Figure 16](#image-placing-the-vacuum-pump-filter). Placing the vacuum pump filter**. [Source](https://commons.wikimedia.org/wiki/File:Vacuum_pump_filter_place_filter.png).

<a id="video-pouring-the-water-sample-into-the-vacuum-tube-and-turning-on-the-vacuum-pump"></a>
**[Video 2](#video-pouring-the-water-sample-into-the-vacuum-tube-and-turning-on-the-vacuum-pump). Pouring the water sample into the vacuum tube and turning on the vacuum pump.** [Source](https://commons.wikimedia.org/wiki/File:Vacuum_pump_filter_pour_sample_and_turn_on.webm).

### Post filtration purification

↑ **Parent:** [DNA extraction](#dna-extraction)

<a id="_56"></a>
After filtration, all DNA should present in the filter, so we cut the paper up with scissors and put the pieces into an Eppendorf: [Video 3. "Cutting vacuum pump filter and placing it in Eppendorf"](#video-cutting-vacuum-pump-filter-and-placing-it-in-eppendorf).

<a id="video-cutting-vacuum-pump-filter-and-placing-it-in-eppendorf"></a>
**[Video 3](#video-cutting-vacuum-pump-filter-and-placing-it-in-eppendorf). Cutting vacuum pump filter and placing it in Eppendorf.** [Source](https://commons.wikimedia.org/wiki/File:Vacuum_pump_filter_cut_and_place_in_eppendorf.webm).

<a id="_57"></a>
Now that we had the DNA in Eppendorfs, we were ready to continue the purification in a simpler and more standardized lab pipeline fashion.

<a id="_58"></a>
First we added some small specialized beads and chemicals to the water and shook them Eppendorfs hard in a [Scientific Industries Inc. Vortex-Genie 2](#scientific-industries-inc-vortex-genie-2) machine to break the [cell](cell.md) and free the DNA.

<a id="_59"></a>
**[Video 4](#_59)** [Source](https://commons.wikimedia.org/wiki/File:Scientific_Industries_Inc_Vortex-Genie_2_loading.webm).

<a id="_60"></a>
**[Video 5](#_60)** [Source](https://commons.wikimedia.org/wiki/File:Scientific_Industries_Inc_Vortex-Genie_2_running.ogv).

<a id="_61"></a>
Once that was done, we added several reagents which split the solution into two phases: one containing the DNA and the other not. We would then pipette the phase with the DNA out to the next Eppendorf, and continue the process.

<a id="_62"></a>
In one step for example, the DNA was present as a white precipitate at the bottom of the tube, and we threw away the supernatant liquid: [Figure 17. "White precipitate formed with Qiagen DNeasy PowerWater Kit"](#image-white-precipitate-formed-with-qiagen-dneasy-powerwater-kit).

<a id="image-white-precipitate-formed-with-qiagen-dneasy-powerwater-kit"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Qiagen_DNeasy_PowerWater_Kit_White_Precipitate.jpg/500px-Qiagen_DNeasy_PowerWater_Kit_White_Precipitate.jpg)

**[Figure 17](#image-white-precipitate-formed-with-qiagen-dneasy-powerwater-kit). White precipitate formed with Qiagen DNeasy PowerWater Kit**. [Source](https://commons.wikimedia.org/wiki/File:Qiagen_DNeasy_PowerWater_Kit_White_Precipitate.jpg).

<a id="_63"></a>
At various stages, centrifuging was also necessary. Much like the previous vacuum pump step, this adds extra gravity to speed up the separation of phases with different molecular masses.

<a id="_64"></a>
In our case, we used a [VWR Micro Star 17 microcentrifuge](#vwr-micro-star-17-microcentrifuge) for those steps:

<a id="image-vwr-micro-star-17-microcentrifuge"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/VWR_Micro_Star_17_microcentrifuge.jpg/330px-VWR_Micro_Star_17_microcentrifuge.jpg" alt="" height="400">

**[Figure 18](#image-vwr-micro-star-17-microcentrifuge). VWR Micro Star 17 microcentrifuge.** [Source](https://commons.wikimedia.org/wiki/File:VWR_Micro_Star_17_microcentrifuge.jpg).

<a id="image-vwr-micro-star-17-microcentrifuge-loading"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/65/VWR_Micro_Star_17_microcentrifuge_loading.png/330px-VWR_Micro_Star_17_microcentrifuge_loading.png)

**[Figure 19](#image-vwr-micro-star-17-microcentrifuge-loading). VWR Micro Star 17 microcentrifuge loading.** [Source](https://commons.wikimedia.org/wiki/File:VWR_Micro_Star_17_microcentrifuge_loading.png).

<a id="_65"></a>
Then, when we had finally finished all the purification steps, we measured the quantity of DNA with a [Biochrom SimpliNano spectrophotometer](#biochrom-simplinano-spectrophotometer) to check that the purification went well:

<a id="image-biochrom-simplinano-spectrophotometer-loading-sample"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/Biochrom_SimpliNano_spectrophotometer_loading_sample.jpg/250px-Biochrom_SimpliNano_spectrophotometer_loading_sample.jpg" alt="" height="400">

**[Figure 20](#image-biochrom-simplinano-spectrophotometer-loading-sample). Biochrom SimpliNano spectrophotometer loading sample.** [Source](https://commons.wikimedia.org/wiki/File:Biochrom_SimpliNano_spectrophotometer_loading_sample.jpg).

<a id="image-biochrom-simplinano-spectrophotometer-result-readout"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f4/Biochrom_SimpliNano_spectrophotometer_result_readout.jpg/330px-Biochrom_SimpliNano_spectrophotometer_result_readout.jpg)

**[Figure 21](#image-biochrom-simplinano-spectrophotometer-result-readout). Biochrom SimpliNano spectrophotometer result readout.** [Source](https://commons.wikimedia.org/wiki/File:Biochrom_SimpliNano_spectrophotometer_result_readout.jpg).

<a id="_66"></a>
And because the readings were good, we put it in our -20 C fridge to preserve it until the second day of the workshop and called it a day:

<a id="image-minus-20-fridge-storing-samples"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/Minus_20_fridge_storing_samples.jpg/120px-Minus_20_fridge_storing_samples.jpg" alt="" height="400">

**[Figure 22](#image-minus-20-fridge-storing-samples). Minus 20 fridge storing samples.** [Source](https://commons.wikimedia.org/wiki/File:Minus_20_fridge_storing_samples.jpg).

## PCR

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)  
🏷️ **Tags:** [Polymerase chain reaction](dna.md#polymerase-chain-reaction)

<a id="_68"></a>
More generic PCR information at: [Section "Polymerase chain reaction"](dna.md#polymerase-chain-reaction).

<a id="_69"></a>
Because it is considered the less interesting step, and because it takes quite some time, this step was done by the event organizers between the two event days, so participants did not get to take many photos.

<a id="_70"></a>
PCR protocols are very standard it seems, all that biologists need to know to reproduce is the time and temperature of each step.

<a id="_71"></a>
We did 35 cycles of:<a id="_72"></a>

<a id="_73"></a>
- 94˚C for 30 seconds
<a id="_74"></a>
- 60˚C for 30 seconds
<a id="_75"></a>
- 72˚C for 45 seconds

<a id="_76"></a>
This process used a [Marshal Scientific MJ Research PTC-200 Thermal Cycler](#marshal-scientific-mj-research-ptc-200-thermal-cycler):

<a id="image-marshal-scientific-mj-research-ptc-200-thermal-cycler"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/Marshal_Scientific_MJ_Research_PTC-200_Thermal_Cycler.jpg/330px-Marshal_Scientific_MJ_Research_PTC-200_Thermal_Cycler.jpg)

**[Figure 23](#image-marshal-scientific-mj-research-ptc-200-thermal-cycler). Marshal Scientific MJ Research PTC-200 Thermal Cycler.** [Source](https://commons.wikimedia.org/wiki/File:Marshal_Scientific_MJ_Research_PTC-200_Thermal_Cycler.jpg).

<a id="_77"></a>
We added PCR primers for regions that surround the 16S DNA. The primers are just bought from a vendor, and we used well known regions are called 27F and 1492R. Here is a paper that analyzes other choices: [https://academic.oup.com/femsle/article/221/2/299/630719](https://academic.oup.com/femsle/article/221/2/299/630719) ([archive](https://web.archive.org/web/20190911091818/https://academic.oup.com/femsle/article/221/2/299/630719)) "Evaluation of primers and PCR conditions for the analysis of 16S rRNA genes from a natural environment" by Yuichi Hongoh, Hiroe Yuzawa, Moriya Ohkuma, Toshiaki Kudo (2003)

<a id="_78"></a>
One cool thing about the PCR is that we can also add a known barcode at the end of each primer as shown at [Code 2. "PCR diagram"](#code-pcr-diagram).

<a id="_79"></a>
This means that we bought a few different versions of our 27F/1492R primers, each with a different small DNA tag attached directly to them in addition to the matching sequence.

<a id="_80"></a>
This way, we were able to:<a id="_81"></a>

<a id="_82"></a>
- use a different barcode for samples collected from different locations. This means we<a id="_83"></a>

  <a id="_84"></a>
  - did PCR separately for each one of them
  <a id="_85"></a>
  - for each PCR run, used a different set of primers, each with a different tag
  <a id="_86"></a>
  - the primer is still able to attach, and then the tag just gets amplified with the rest of everything!
<a id="_87"></a>
- sequence them all in one go
<a id="_88"></a>
- then just from the sequencing output the barcode to determine where each sequence came from!

<a id="code-pcr-diagram"></a>
```
Input: Bacterial DNA (a little bit)
... --- 27S --- 16S --- 1492R --- ...

|||
|||
vvv

Output: PCR output (a lot of)
Barcode --- 27S --- 16S --- 1492R
```

<a id="_89"></a>
Finally, after purification, we used the [Qiagen QIAquick PCR Purification Kit](#qiagen-qiaquick-pcr-purification-kit) protocol to purify the generated from unwanted PCR byproducts.

### PCR verification with gel electrophoresis

↑ **Parent:** [PCR](#pcr)

<a id="_90"></a>
Biology experiments are hard, and so they go wrong, a lot.

<a id="_91"></a>
For this reason, it is wise to verify that certain steps are correct whenever possible.

<a id="_92"></a>
And so this is the first thing we did on the second day!

<a id="_93"></a>
[Gel electrophoresis](molecular-biology.md#gel-electrophoresis) separates molecules by their charge-to-mass ratio. It is one of those ultra common lab procedures!

<a id="_94"></a>
This allows us to determine how long are the DNA fragments present in our solution.

<a id="_95"></a>
Since we know that we amplified the 16S regions which we know the rough size of (there might be a bit of variability across species, but not that much), we were expecting to see a big band at that size.

<a id="_96"></a>
And that is exactly what we saw!

<a id="_97"></a>
First we had to prepare the gel, put the gel comb, and pipette the samples into wells present in the gel:

<a id="image-gel-electrophoresis-insert-comb"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Gel_electrophoresis_insert_comb.jpg/330px-Gel_electrophoresis_insert_comb.jpg)

**[Figure 24](#image-gel-electrophoresis-insert-comb). Gel electrophoresis insert comb.** [Source](https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_insert_comb.jpg).

<a id="image-gel-electrophoresis-top-view-with-wells-visible"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cb/Gel_electrophoresis_top_view_with_wells_visible.jpg/330px-Gel_electrophoresis_top_view_with_wells_visible.jpg)

**[Figure 25](#image-gel-electrophoresis-top-view-with-wells-visible). Gel electrophoresis top view with wells visible.** [Source](https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_top_view_with_wells_visible.jpg).

<a id="image-gel-electrophoresis-pipette-sample-into-wells"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/Gel_electrophoresis_pipette_sample_into_wells.jpg/330px-Gel_electrophoresis_pipette_sample_into_wells.jpg)

**[Figure 26](#image-gel-electrophoresis-pipette-sample-into-wells). Gel electrophoresis pipette sample into wells.** [Source](https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_pipette_sample_into_wells.jpg).

<a id="_98"></a>
To see the DNA, we added [ethidium bromide](chemistry.md#ethidium-bromide) to the samples, which is a substance that that both binds to DNA and is fluorescent.

<a id="_99"></a>
Because it interacts heavily with DNA, ethidium bromide is a [mutagen](dna.md#mutagen), and the biology people sure did treat the dedicated electrophoresis bench area with respect! [Figure 27. "Gel electrophoresis dedicated bench area to prevent ethidium bromide contamination."](#image-gel-electrophoresis-dedicated-bench-area-to-prevent-ethidium-bromide-contamination).

<a id="image-gel-electrophoresis-dedicated-bench-area-to-prevent-ethidium-bromide-contamination"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Gel_electrophoresis_dedicated_bench_area_to_prevent_ethidium_bromide_contamination.jpg/330px-Gel_electrophoresis_dedicated_bench_area_to_prevent_ethidium_bromide_contamination.jpg)

**[Figure 27](#image-gel-electrophoresis-dedicated-bench-area-to-prevent-ethidium-bromide-contamination). Gel electrophoresis dedicated bench area to prevent ethidium bromide contamination.** [Source](https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_dedicated_bench_area_to_prevent_ethidium_bromide_contamination.jpg).

<a id="image-gel-electrophoresis-dedicated-waste-bin-for-centrifuge-tubes-and-pipette-tips-contaminated-with-ethidium-bromide"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Gel_electrophoresis_dedicated_waste_bin_for_centrifuge_tubes_and_pipette_tips_contaminated_with_ethidium_bromide.jpg/330px-Gel_electrophoresis_dedicated_waste_bin_for_centrifuge_tubes_and_pipette_tips_contaminated_with_ethidium_bromide.jpg)

**[Figure 28](#image-gel-electrophoresis-dedicated-waste-bin-for-centrifuge-tubes-and-pipette-tips-contaminated-with-ethidium-bromide). Gel electrophoresis dedicated waste bin for centrifuge tubes and pipette tips contaminated with ethidium bromide.** [Source](https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_dedicated_waste_bin_for_centrifuge_tubes_and_pipette_tips_contaminated_with_ethidium_bromide.jpg).

<a id="_100"></a>
The UV transilluminator we used to shoot [UV light](photon.md#ultraviolet) into the gel was the [Fisher Scientific UVP LM-26E Benchtop 2UV Transilluminator](#fisher-scientific-uvp-lm-26e-benchtop-2uv-transilluminator). The fluorescent substance then emitted a light we can see.

<a id="_101"></a>
As barely seen at [Figure 31. "Fischer Scientific UVP LM-26E Benchtop 2UV Transilluminator illuminated gel."](#image-fischer-scientific-uvp-lm-26e-benchtop-2uv-transilluminator-illuminated-gel) due to bad photo quality due to lack of light, there is one strong green line, which compared to the ladder matches our expected 16S length. What we saw it with the naked eyes was very clear however.

<a id="image-fischer-scientific-uvp-lm-26e-benchtop-2uv-transilluminator"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator.jpg/500px-Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator.jpg)

**[Figure 29](#image-fischer-scientific-uvp-lm-26e-benchtop-2uv-transilluminator). Fischer Scientific UVP LM-26E Benchtop 2UV Transilluminator**. [Source](https://commons.wikimedia.org/wiki/File:Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator.jpg).

<a id="image-fischer-scientific-uvp-lm-26e-benchtop-2uv-transilluminator-loading-gel"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/85/Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator_loading_gel.jpg/330px-Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator_loading_gel.jpg)

**[Figure 30](#image-fischer-scientific-uvp-lm-26e-benchtop-2uv-transilluminator-loading-gel). Fischer Scientific UVP LM-26E Benchtop 2UV Transilluminator loading gel.** [Source](https://commons.wikimedia.org/wiki/File:Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator_loading_gel.jpg).

<a id="image-fischer-scientific-uvp-lm-26e-benchtop-2uv-transilluminator-illuminated-gel"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator_illuminated_gel.jpg/330px-Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator_illuminated_gel.jpg)

**[Figure 31](#image-fischer-scientific-uvp-lm-26e-benchtop-2uv-transilluminator-illuminated-gel). Fischer Scientific UVP LM-26E Benchtop 2UV Transilluminator illuminated gel.** [Source](https://commons.wikimedia.org/wiki/File:Fischer_Scientific_UVP_LM-26E_Benchtop_2UV_Transilluminator_illuminated_gel.jpg).

## Sequencing

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_102"></a>
Once we had the amplified 16S DNA, we were almost ready to start sequencing!

### Pre-sequencing preparation

↑ **Parent:** [Sequencing](#sequencing)

<a id="_103"></a>
One cool thing we did in this procedure was to use [magnetic separation](https://en.wikipedia.org/wiki/Magnetic_separation) with magnetic beads to further concentrate the DNA: [Figure 32. "GE MagRack 6 pipetting."](#image-ge-magrack-6-pipetting).

<a id="_104"></a>
The beads are coated to stick to the DNA, which allows us to easily extract the DNA from the rest of the solution. This is cool, but bio people are borderline obsessed by those beads! Go figure!

<a id="image-ge-magrack-6-pipetting"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/GE_MagRack_6_pipetting.jpg/330px-GE_MagRack_6_pipetting.jpg" alt="" height="400">

**[Figure 32](#image-ge-magrack-6-pipetting). GE MagRack 6 pipetting.** [Source](https://commons.wikimedia.org/wiki/File:GE_MagRack_6_pipetting.jpg).

<a id="image-ge-magrack-6-eppendorf-with-magnetic-beads-mounted"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cc/GE_MagRack_6_eppendorf_with_magnetic_beads_mounted.jpg/500px-GE_MagRack_6_eppendorf_with_magnetic_beads_mounted.jpg)

**[Figure 33](#image-ge-magrack-6-eppendorf-with-magnetic-beads-mounted). GE MagRack 6 eppendorf with magnetic beads mounted.** [Source](https://commons.wikimedia.org/wiki/File:GE_MagRack_6_eppendorf_with_magnetic_beads_mounted.jpg).

<a id="_105"></a>
Then we prepared the DNA for sequencing with the Oxford Nanopore specific part: [Oxford Nanopore SQK-LSK109 Ligation Sequencing Kit](#oxford-nanopore-sqk-lsk109-ligation-sequencing-kit).

<a id="_106"></a>
Here some of the steps required a bit more of vortexing for mixing the reagents, and for this we used the [VELP Scientifica WIZARD IR Infrared Vortex Mixer](#velp-scientifica-wizard-ir-infrared-vortex-mixer) which appears to be quicker to use and not as strong as the Vortex Genie 2 previously used to break up the cells:

<a id="image-velp-scientifica-wizard-ir-infrared-vortex-mixer-running"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/VELP_Scientifica_WIZARD_IR_Infrared_Vortex_Mixer_running.jpg/330px-VELP_Scientifica_WIZARD_IR_Infrared_Vortex_Mixer_running.jpg" alt="" height="400">

**[Figure 34](#image-velp-scientifica-wizard-ir-infrared-vortex-mixer-running). VELP Scientifica WIZARD IR Infrared Vortex Mixer running.** [Source](https://commons.wikimedia.org/wiki/File:VELP_Scientifica_WIZARD_IR_Infrared_Vortex_Mixer_running.jpg).

<a id="_107"></a>
After all that was done, the DNA of the several 400 ml water bottles and hours of hard purification labour were contained in one single Eppendorf!

### Using the Oxford Nanopore

↑ **Parent:** [Sequencing](#sequencing)

<a id="_108"></a>
With all this ready, we opened the Nanopore flow cell, which is the 500 dollar consumable piece that goes in the sequencer.

<a id="_109"></a>
We then had to pipette the final golden Eppendorf into the flow cell. My anxiety levels were going through the roof: [Figure 38. "Oxford nanopore MinION flow cell pipette loading."](#image-oxford-nanopore-minion-flow-cell-pipette-loading).

<a id="image-oxford-nanopore-minion-flow-cell-package"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/81/Oxford_nanopore_MinION_flow_cell_package.jpg/330px-Oxford_nanopore_MinION_flow_cell_package.jpg" alt="" height="400">

**[Figure 35](#image-oxford-nanopore-minion-flow-cell-package). Oxford nanopore MinION flow cell package.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_nanopore_MinION_flow_cell_package.jpg).

<a id="image-oxford-nanopore-minion-flow-cell-front"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/00/Oxford_nanopore_MinION_flow_cell_front.jpg/500px-Oxford_nanopore_MinION_flow_cell_front.jpg)

**[Figure 36](#image-oxford-nanopore-minion-flow-cell-front). Oxford nanopore MinION flow cell front.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_nanopore_MinION_flow_cell_front.jpg).

<a id="image-oxford-nanopore-minion-flow-cell-back"></a>
![](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/Oxford_nanopore_MinION_flow_cell_back.jpg/960px-Oxford_nanopore_MinION_flow_cell_back.jpg)

**[Figure 37](#image-oxford-nanopore-minion-flow-cell-back). Oxford nanopore MinION flow cell back.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_nanopore_MinION_flow_cell_back.jpg).

<a id="image-oxford-nanopore-minion-flow-cell-pipette-loading"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Oxford_nanopore_MinION_flow_cell_pipette_loading.jpg/250px-Oxford_nanopore_MinION_flow_cell_pipette_loading.jpg" alt="" height="400">

**[Figure 38](#image-oxford-nanopore-minion-flow-cell-pipette-loading). Oxford nanopore MinION flow cell pipette loading.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_nanopore_MinION_flow_cell_pipette_loading.jpg).

<a id="_110"></a>
At this point bio people start telling lab horror stories of expensive solutions being spilled and people having to recover them from fridge walls, or of how people threw away golden Eppendorfs and had to pick them out of trash bins with hundreds of others looking exactly the same etc. (but also how some discoveries were made like this). This reminded Ciro of: [https://youtu.be/89UNPdNtOoE?t=919](https://youtu.be/89UNPdNtOoE?t=919) [Alfred Maddock's plutonium spill horror story](https://en.wikipedia.org/wiki/Alfred_Maddock).

<a id="_111"></a>
Luckily this time, it worked out!

<a id="_112"></a>
We then just had to connect the MinION to the computer, and wait for 2 days.

<a id="_113"></a>
During this time, the DNA would be sucked through the pores.

<a id="_114"></a>
As can be seen from [Video 6. "Oxford Nanopore MinION software channels pannel on Mac."](#video-oxford-nanopore-minion-software-channels-pannel-on-mac) the software tells us which pores are still working.

<a id="image-oxford-nanopore-minion-connected-to-a-mac-via-usb"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/Oxford_Nanopore_MinION_connected_to_a_Mac_via_USB.jpg/330px-Oxford_Nanopore_MinION_connected_to_a_Mac_via_USB.jpg" alt="" height="400">

**[Figure 39](#image-oxford-nanopore-minion-connected-to-a-mac-via-usb). Oxford Nanopore MinION connected to a Mac via USB.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_connected_to_a_Mac_via_USB.jpg).

<a id="video-oxford-nanopore-minion-software-channels-pannel-on-mac"></a>
**[Video 6](#video-oxford-nanopore-minion-software-channels-pannel-on-mac). Oxford Nanopore MinION software channels pannel on Mac.** [Source](https://commons.wikimedia.org/wiki/File:Oxford_Nanopore_MinION_software_channels_pannel_on_Mac.webm).

<a id="_115"></a>
Pores go bad sooner or later randomly, until there are none left, at which point we can stop the process and throw the flow cell away.

<a id="_116"></a>
48 hours was expected to be a reasonable time until all pores went bad, and so we called it a day, and waited for an email from the PuntSeq team telling us how things went.

<a id="_117"></a>
We reached a yield of 16 billion base pairs out of the 30Gbp nominal maximum, which the bio people said was not bad.

## Bioinformatics

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_118"></a>
Because Ciro's a software engineer, and he's done enough staring in computers for a lifetime already, and he believes in the power of [Git](software.md#git), he didn't pay much attention to this part ;-)

<a id="_119"></a>
According to the eLife paper, the code appears to have been uploaded to: [https://github.com/d-j-k/puntseq](https://github.com/d-j-k/puntseq). TODO at least mention the key algorithms used more precisely.

<a id="_120"></a>
Ciro can however see that it does present interesting problems!

<a id="_121"></a>
Because it was necessary to wait for 2 days to get our data, the workshop first reused sample data from previous collections done earlier in the year to illustrate the software.

<a id="_122"></a>
First there is some signal processing/machine learning required to do the [base calling](dna.md#base-calling), which is not trivial in the Oxford Nanopore, since neighbouring bases can affect the signal of each other. This is mostly handled by Oxford Nanopore itself, or by hardcore programmers in the field however.

<a id="_123"></a>
After the base calling was done, the data was analyzed using computer programs that match the sequenced 16S sequences to a database of known sequenced species.

<a id="_124"></a>
This is of course not just a simple direct string matching problem, since like any in experiment, the DNA reads have some errors, so the program has to find the best match even though it is not exact.

<a id="_125"></a>
The PuntSeq team would later upload the data to well known open databases so that it will be preserved forever! When ready, a link to the data would be uploaded to: [https://www.puntseq.co.uk/data](https://www.puntseq.co.uk/data)

## Conclusions

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_126"></a>
<a id="_127"></a>
- against all odds, the experiment worked and we got DNA out of the water, despite a bunch of non-bio newbs actively messing with random parts of the experiment
<a id="_128"></a>
- PuntSeq and Biomakespace people, and all those tho do scientific outreach, are awesome!
<a id="_129"></a>
- biology is hard
<a id="_130"></a>
- creating insanely media rich articles like this is also hard, but the following helped enormously:<a id="_131"></a>

  <a id="_132"></a>
  - [Wikimedia Commons](cirosantilli-com.md#media-rationale-of-ciro-santilli-s-website) to store large media files out of Git
  <a id="_133"></a>
  - [Asciidoctor](markdown-style-guide) extensions to easily include those media files. The lessons learnt in this article were then an important motivation for Ciro's [OurBigBook Markup](ciro-santilli-s-projects.md#ourbigbook-markup), to which this article was later migrated.
  <a id="_134"></a>
  - [Nomacs](https://unix.stackexchange.com/questions/25978/image-viewer-for-multiple-images/539333#539333) to give [Google Photos](google.md#google-photos) photos meaningful names and to edit people's faces out of pictures ;-)
<a id="_135"></a>
- some scientific Wikipedia pages may or may not have been edited with better pictures during the course of writing this article

## Protocols used

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_136"></a>
Protocols are the biologist term for "recipe".

<a id="_137"></a>
I found that a lot of biology comes down to this: get the right recipe, follow it well even though you don't understand all the proprietary details, and pray.

### Qiagen DNeasy PowerWater Kit

↑ **Parent:** [Protocols used](#protocols-used)

<a id="_138"></a>
[https://www.qiagen.com/gb/products/discovery-and-translational-research/dna-rna-purification/dna-purification/microbial-dna/dneasy-powerwater-kit](https://www.qiagen.com/gb/products/discovery-and-translational-research/dna-rna-purification/dna-purification/microbial-dna/dneasy-powerwater-kit) ([archive](https://web.archive.org/web/20190905084344/https://www.qiagen.com/gb/products/discovery-and-translational-research/dna-rna-purification/dna-purification/microbial-dna/dneasy-powerwater-kit/)) Here is its documentation: [https://www.qiagen.com/gb/resources/download.aspx?id=bb731482-874b-4241-8cf4-c15054e3a4bf&lang=en](https://www.qiagen.com/gb/resources/download.aspx?id=bb731482-874b-4241-8cf4-c15054e3a4bf&lang=en) ([archive](https://web.archive.org/web/20190905084623/https://www.qiagen.com/gb/resources/download.aspx?id=bb731482-874b-4241-8cf4-c15054e3a4bf&lang=en)).

<a id="_139"></a>
Manual archive: [https://web.archive.org/web/20190911111136/https://www.qiagen.com/gb/resources/download.aspx?id=bb731482-874b-4241-8cf4-c15054e3a4bf&lang=en](https://web.archive.org/web/20190911111136/https://www.qiagen.com/gb/resources/download.aspx?id=bb731482-874b-4241-8cf4-c15054e3a4bf&lang=en)

<a id="_140"></a>
Kit to extract clean DNA from water.

<a id="image-qiagen-dneasy-powerwater-kit-open-box"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2b/Qiagen_DNeasy_PowerWater_Kit_open_box.jpg/330px-Qiagen_DNeasy_PowerWater_Kit_open_box.jpg" alt="" height="400">

**[Figure 40](#image-qiagen-dneasy-powerwater-kit-open-box). Qiagen DNeasy PowerWater Kit open box.** [Source](https://commons.wikimedia.org/wiki/File:Qiagen_DNeasy_PowerWater_Kit_open_box.jpg).

### Qiagen QIAquick PCR Purification Kit

↑ **Parent:** [Protocols used](#protocols-used)

<a id="_141"></a>
[https://www.qiagen.com/us/products/discovery-translational-research/dna-rn-a-purification/dna-purification/dna-clean-up/qiaquick-pcr-purification-kit/#orderinginformation](https://www.qiagen.com/us/products/discovery-translational-research/dna-rn-a-purification/dna-purification/dna-clean-up/qiaquick-pcr-purification-kit/#orderinginformation) ([archive](https://web.archive.org/web/20190911092647/https://www.qiagen.com/us/products/discovery-translational-research/dna-rn-a-purification/dna-purification/dna-clean-up/qiaquick-pcr-purification-kit/))

<a id="_142"></a>
Manual archive: [https://web.archive.org/web/20190911100243/https://www.qiagen.com/us/resources/download.aspx?id=e0fab087-ea52-4c16-b79f-c224bf760c39&lang=en](https://web.archive.org/web/20190911100243/https://www.qiagen.com/us/resources/download.aspx?id=e0fab087-ea52-4c16-b79f-c224bf760c39&lang=en)

<a id="_143"></a>
Removes PCR byproducts from purified DNA.

### Oxford Nanopore SQK-LSK109 Ligation Sequencing Kit

↑ **Parent:** [Protocols used](#protocols-used)

<a id="_144"></a>
[https://store.nanoporetech.com/ligation-sequencing-kit.html](https://store.nanoporetech.com/ligation-sequencing-kit.html) ([archive](https://web.archive.org/web/20190911092756/https://store.nanoporetech.com/ligation-sequencing-kit.html))

<a id="_145"></a>
Repairs the ends of DNA, and also attaches an adapter protein to the DNA that makes them go through the pores of e.g. an [Oxford Nanopore MinION](dna.md#oxford-nanopore-minion).

## Equipment used

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

### Thermo Scientific Nalgene Polysulfone Reusable Bottle Top Filters

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_146"></a>
[https://www.fishersci.no/shop/products/nalgene-polysulfone-reusable-bottle%20-top-filters/10465781](https://www.fishersci.no/shop/products/nalgene-polysulfone-reusable-bottle%20-top-filters/10465781) ([archive](https://web.archive.org/web/20190907131756/https://www.fishersci.no/shop/products/nalgene-polysulfone-reusable-bottle%20-top-filters/10465781))

<a id="_147"></a>
This is where we poured the water. It was not large enough for the entire 1L sample, so we had to do it a few times.

### KNF Laboport series laboratory vacuum pump

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_148"></a>
[https://www.knfusa.com/en/laboport/](https://www.knfusa.com/en/laboport/) ([archive](https://web.archive.org/web/20190907132036/https://www.knfusa.com/en/laboport/)).

### Scientific Industries Inc. Vortex-Genie 2

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_150"></a>
[https://www.scientificindustries.com/vortex-genie-2.html](https://www.scientificindustries.com/vortex-genie-2.html) ([archive](https://web.archive.org/web/20190908034549/https://www.scientificind.ustries.com/vortex-genie-2.html))

<a id="_151"></a>
[https://en.wikipedia.org/wiki/Vortex_mixer](https://en.wikipedia.org/wiki/Vortex_mixer)

### VWR Micro Star 17 microcentrifuge

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_153"></a>
[https://uk.vwr.com/store/product/8306728/microcentrifuges-ventilated-refrigerated-micro-star-17-17r](https://uk.vwr.com/store/product/8306728/microcentrifuges-ventilated-refrigerated-micro-star-17-17r) ([archive](https://web.archive.org/web/20190908040119/https://uk.vwr.com/store/product/8306728/microcentrifuges-ventilated-refrigerated-micro-star-17-17r)).

### VELP Scientifica WIZARD IR Infrared Vortex Mixer

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_155"></a>
[https://www.velp.com/en/products/lines/3/family/44/vortex_mixers/65/wizard_ir_infrared_vortex_mixer](https://www.velp.com/en/products/lines/3/family/44/vortex_mixers/65/wizard_ir_infrared_vortex_mixer) ([archive](https://web.archive.org/web/20190908091343/https://www.velp.com/en/products/lines/3/family/44/vortex_mixers/65/wizard_ir_infrared_vortex_mixer)).

### Marshal Scientific MJ Research PTC-200 Thermal Cycler

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_157"></a>
[https://www.marshallscientific.com/MJ-Research-PTC-200-Thermal-Cycler-p/mj-200.htm](https://www.marshallscientific.com/MJ-Research-PTC-200-Thermal-Cycler-p/mj-200.htm) ([archive](https://web.archive.org/web/20190908091629/https://www.marshallscientific.com/MJ-Research-PTC-200-Thermal-Cycler-p/mj-200.htm)).

### GE MagRack 6

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_159"></a>
[https://www.gelifesciences.com/en/us/shop/protein-analysis/protein-sample-preparation/protein-enrichment/magrack-6-p-05761](https://www.gelifesciences.com/en/us/shop/protein-analysis/protein-sample-preparation/protein-enrichment/magrack-6-p-05761) ([archive](https://web.archive.org/web/20190908091852/https://www.gelifesciences.com/en/us/shop/protein-analysis/protein-sample-preparation/protein-enrichment/magrack-6-p-05761)).

### BTLab Systems Mini Centrifuge

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_161"></a>
[https://www.btlabsystems.com/Centrifuges/Mini_Centrifuge_Fixed_7K](https://www.btlabsystems.com/Centrifuges/Mini_Centrifuge_Fixed_7K) ([archive](https://web.archive.org/web/20190908094324/https://www.btlabsystems.com/Centrifuges/Mini_Centrifuge_Fixed_7K)).

<a id="_162"></a>
Manual: [https://web.archive.org/web/20190908094334/https://www.btlabsystems.com/downloads/BT602_Mini_Centrifuge_7K_Fixed.pdf](https://web.archive.org/web/20190908094334/https://www.btlabsystems.com/downloads/BT602_Mini_Centrifuge_7K_Fixed.pdf)

### Fisher Scientific UVP LM-26E Benchtop 2UV Transilluminator

↑ **Parent:** [Equipment used](#equipment-used)  
🏷️ **Tags:** [Fisher Scientific product](science.md#fisher-scientific-product)

<a id="_165"></a>
[https://www.bidspotter.com/en-us/auction-catalogues/bscsur/catalogue-id-bscsur10011/lot-c6605b41-1a14-40e5-a255-a5c5000866e0](https://www.bidspotter.com/en-us/auction-catalogues/bscsur/catalogue-id-bscsur10011/lot-c6605b41-1a14-40e5-a255-a5c5000866e0) ([archive](https://web.archive.org/web/20190908094721/https://www.bidspotter.com/en-us/auction-catalogues/bscsur/catalogue-id-bscsur10011/lot-c6605b41-1a14-40e5-a255-a5c5000866e0)) Cannot exact same product on official website, but here is a similar one: [https://www.fishersci.co.uk/shop/products/lm-26-2uv-transilluminator/12382038](https://www.fishersci.co.uk/shop/products/lm-26-2uv-transilluminator/12382038) ([archive](https://web.archive.org/web/20190908094903/https://www.fishersci.co.uk/shop/products/lm-26-2uv-transilluminator/12382038)).

### Biochrom SimpliNano spectrophotometer

↑ **Parent:** [Equipment used](#equipment-used)

<a id="_167"></a>
[https://biochromspectros.com/spectrophotometers/simplinano-cat/simplinano-spectrophotometer.html](https://biochromspectros.com/spectrophotometers/simplinano-cat/simplinano-spectrophotometer.html) ([archive](https://web.archive.org/web/20190920214435/https://biochromspectros.com/spectrophotometers/simplinano-cat/simplinano-spectrophotometer.html))

<a id="_168"></a>
Manual: [https://biochromspectros.com/media/wysiwyg/support_page/support-simplinano/Simplinano-UM.pdf](https://biochromspectros.com/media/wysiwyg/support_page/support-simplinano/Simplinano-UM.pdf) ([archive](https://web.archive.org/web/20190920214755/https://biochromspectros.com/media/wysiwyg/support_page/support-simplinano/Simplinano-UM.pdf))

## External links to this page

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](oxford-nanopore-river-bacteria.md)

<a id="_170"></a>
<a id="_171"></a>
- 2021-03-25: [Oxford Nanopore Technologies](dna.md#oxford-nanopore-technologies) [retweeted](https://twitter.com/cirosantilli/status/1177856415068823552/retweets) this article, that's awesome!
<a id="_172"></a>
- 2021: [https://hackaday.com/author/wd5gnr1/](https://hackaday.com/author/wd5gnr1/) "SEQUENCING DNA FOR METAGENOMICS" by Al Williams (2021). This came after [Ciro Santilli](ciro-santilli.md) self promoted at: [https://stackoverflow.blog/2021/02/03/sequencing-your-dna-with-a-usb-dongle-and-open-source-code/#comment-1411921](https://stackoverflow.blog/2021/02/03/sequencing-your-dna-with-a-usb-dongle-and-open-source-code/#comment-1411921)

## ↑ Ancestors (12)

1. [Oxford Nanopore MinION](dna.md#oxford-nanopore-minion)
2. [Oxford Nanopore Technologies product](dna.md#oxford-nanopore-technologies-product)
3. [Oxford Nanopore Technologies](dna.md#oxford-nanopore-technologies)
4. [DNA sequencing company](dna.md#dna-sequencing-company)
5. [DNA sequencing](dna.md#dna-sequencing)
6. [DNA](dna.md)
7. [Molecular biology](molecular-biology.md)
8. [Level of organization of bodies](biology.md#level-of-organization-of-bodies)
9. [Biology](biology.md)
10. [Natural science](science.md#natural-science)
11. [Science](science.md)
12. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (9)

- [Ciro Santilli's Homepage](README.md)
- [The best articles by Ciro Santilli](articles.md)
- [Ciro Santilli](ciro-santilli.md)
- [Exams and homework are useless, only projects matter](how-to-teach.md#exams-and-homework-are-useless-only-projects-matter)
- [Metagenomics](dna.md#metagenomics)
- [Oxford Nanopore MinION](dna.md#oxford-nanopore-minion)
- [Polymerase chain reaction](dna.md#polymerase-chain-reaction)
- [Sponsor Ciro Santilli's work on OurBigBook.com](sponsor.md)
- [Videos of all key physics experiments](todo.md#videos-of-all-key-physics-experiments)
