# Overview of the experiment

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](../oxford-nanopore-river-bacteria-split.md)

<a id="_16"></a>
For those that know biology and just want to do the thing, see: [Section "Protocols used"](protocols-used.md).

<a id="_17"></a>
The PuntSeq team uses an [Oxford Nanopore MinION](../oxford-nanopore-minion.md) [DNA sequencer](../dna-sequencing.md) made by [Oxford Nanopore Technologies](../oxford-nanopore-technologies.md) to sequence the [16S](../16s-ribosomal-rna.md) region of bacterial [DNA](../dna-split.md), which is about 1500 nucleotides long.

<a id="_18"></a>
This kind of "decode everything from the sample to see what species are present approach" is called "[metagenomics](../metagenomics.md)".

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
The 16S region codes for one of the [RNA](../rna.md) pieces that makes the [bacterial ribosome](https://en.wikipedia.org/w/index.php?title=Ribosome&oldid=912600990#Bacterial_ribosomes).

<a id="_21"></a>
Before [sequencing the DNA](sequencing.md), we will do a [PCR](pcr.md) with primers that fit just before and just after the 16S DNA, in well conserved regions expected to be present in all bacteria.

<a id="_22"></a>
The PCR replicates only the DNA region between our two selected primers a gazillion times so that only those regions will actually get picked up by the sequencing step in practice.

<a id="_23"></a>
[Eukaryotes](../eukaryote.md) also have an analogous ribosome part, the 18S region, but the PCR primers are selected for targets around the 16S region which are only present in prokaryotes.

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

**Table of contents**

- [Why Oxford Nanopore was used instead of Illumina for the sequencing](why-oxford-nanopore-was-used-instead-of-illumina-for-the-sequencing.md)

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
