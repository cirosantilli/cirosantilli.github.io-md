# PCR

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](../oxford-nanopore-river-bacteria-split.md)  
🏷️ **Tags:** [Polymerase chain reaction](../polymerase-chain-reaction.md)

<a id="_68"></a>
More generic PCR information at: [Section "Polymerase chain reaction"](../polymerase-chain-reaction.md).

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
This process used a [Marshal Scientific MJ Research PTC-200 Thermal Cycler](marshal-scientific-mj-research-ptc-200-thermal-cycler.md):

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
Finally, after purification, we used the [Qiagen QIAquick PCR Purification Kit](qiagen-qiaquick-pcr-purification-kit.md) protocol to purify the generated from unwanted PCR byproducts.

**Table of contents**

- [PCR verification with gel electrophoresis](pcr-verification-with-gel-electrophoresis.md)

## ↑ Ancestors (13)

1. [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](../oxford-nanopore-river-bacteria-split.md)
2. [Oxford Nanopore MinION](../oxford-nanopore-minion.md)
3. [Oxford Nanopore Technologies product](../oxford-nanopore-technologies-product.md)
4. [Oxford Nanopore Technologies](../oxford-nanopore-technologies.md)
5. [DNA sequencing company](../dna-sequencing-company.md)
6. [DNA sequencing](../dna-sequencing.md)
7. [DNA](../dna-split.md)
8. [Molecular biology](../molecular-biology-split.md)
9. [Level of organization of bodies](../level-of-organization-of-bodies.md)
10. [Biology](../biology-split.md)
11. [Natural science](../natural-science.md)
12. [Science](../science-split.md)
13. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (2)

- [Overview of the experiment](overview-of-the-experiment.md)
- [Polymerase chain reaction](../polymerase-chain-reaction.md)
