# Bioinformatics

↑ **Parent:** [How to use an Oxford Nanopore MinION to extract DNA from river water and determine which bacteria live in it](../oxford-nanopore-river-bacteria-split.md)

<a id="_118"></a>
Because Ciro's a software engineer, and he's done enough staring in computers for a lifetime already, and he believes in the power of [Git](../git.md), he didn't pay much attention to this part ;-)

<a id="_119"></a>
According to the eLife paper, the code appears to have been uploaded to: [https://github.com/d-j-k/puntseq](https://github.com/d-j-k/puntseq). TODO at least mention the key algorithms used more precisely.

<a id="_120"></a>
Ciro can however see that it does present interesting problems!

<a id="_121"></a>
Because it was necessary to wait for 2 days to get our data, the workshop first reused sample data from previous collections done earlier in the year to illustrate the software.

<a id="_122"></a>
First there is some signal processing/machine learning required to do the [base calling](../base-calling.md), which is not trivial in the Oxford Nanopore, since neighbouring bases can affect the signal of each other. This is mostly handled by Oxford Nanopore itself, or by hardcore programmers in the field however.

<a id="_123"></a>
After the base calling was done, the data was analyzed using computer programs that match the sequenced 16S sequences to a database of known sequenced species.

<a id="_124"></a>
This is of course not just a simple direct string matching problem, since like any in experiment, the DNA reads have some errors, so the program has to find the best match even though it is not exact.

<a id="_125"></a>
The PuntSeq team would later upload the data to well known open databases so that it will be preserved forever! When ready, a link to the data would be uploaded to: [https://www.puntseq.co.uk/data](https://www.puntseq.co.uk/data)

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
