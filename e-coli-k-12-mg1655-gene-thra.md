# E. Coli K-12 MG1655 gene thrA

↑ **Parent:** [E. Coli K-12 MG1655 gene](e-coli-k-12-mg1655-gene.md)  
🏷️ **Tags:** [Enzyme](enzyme.md)

[UniProt](uniprot.md) entry: [https://www.uniprot.org/uniprot/P00561](https://www.uniprot.org/uniprot/P00561).

[NCBI](national-center-for-biotechnology-information.md) entry: [https://www.ncbi.nlm.nih.gov/gene/945803](https://www.ncbi.nlm.nih.gov/gene/945803).

The second [gene](gene.md) in the [E. Coli K-12 MG1655](e-coli-k-12-mg1655.md) genome. Part of the [E. Coli K-12 MG1655 operon thrLABC](e-coli-k-12-mg1655-operon-thrlabc.md).

Part of a reaction that produces [threonine](threonine.md).

This [protein](protein-split.md) is an [enzyme](enzyme.md). The [UniProt](uniprot.md) entry clearly shows the [chemical reactions](chemical-reaction.md) that it [catalyses](catalysis.md). In this case, there are actually two! It can either transforming the [metabolite](metabolite.md):
- "L-homoserine" into "L-aspartate 4-semialdehyde"
- "L-aspartate" into "4-phospho-L-aspartate"
Also interestingly, we see that both of those reaction require some extra energy to catalyse, one needing [adenosine triphosphate](adenosine-triphosphate.md) and the other [nADP+](nadp-plus.md).

TODO: any mention of how much faster it makes the reaction, numerically?

Since this is an [enzyme](enzyme.md), it would also be interesting to have a quick search for it in the [KEGG](kegg.md) entry starting from the organism: [https://www.genome.jp/pathway/eco01100+M00022](https://www.genome.jp/pathway/eco01100+M00022) We type in the search bar "thrA", it gives a long list, but the last entry is our "thrA". Selecting it highlights two pathways in the large [graph](graph-discrete-mathematics.md), so we understand that it catalyzes two different reactions, as suggested by the protein name itself (fused blah blah). We can now hover over:
- the [edge](edge-graph.md): it shows all the enzymes that catalyze the given reaction. Both edges actually have multiple enzymes, e.g. the L-Homoserine path is also catalyzed by another enzyme called metL.
- the [node](edge-graph.md): they are the [metabolites](metabolite.md), e.g. one of the paths contains "L-homoserine" on one node and "L-aspartate 4-semialdehyde"
Note that common [cofactor](cofactor-biochemistry.md) are omitted, since we've learnt from the UniProt entry that this reaction uses ATP.

If we can now click on the L-Homoserine edge, it takes us to: [https://www.genome.jp/entry/eco:b0002+eco:b3940](https://www.genome.jp/entry/eco:b0002+eco:b3940). Under "Pathway" we see an interesting looking pathway "Glycine, serine and threonine metabolism": [https://www.genome.jp/pathway/eco00260+b0002](https://www.genome.jp/pathway/eco00260+b0002) which contains a small manually selected and extremely clearly named subset of the larger graph!

But looking at the bottom of this subgraph (the UI is not great, can't Ctrl+F and enzyme names not shown, but the selected enzyme is slightly highlighted in red because it is in the URL [https://www.genome.jp/pathway/eco00260+b0002](https://www.genome.jp/pathway/eco00260+b0002) vs [https://www.genome.jp/pathway/eco00260](https://www.genome.jp/pathway/eco00260)) we clearly see that thrA, thrB and thrC for a sequence that directly transforms "L-aspartate 4-semialdehyde" into "Homoserine" to "O-Phospho-L-homoserine" and finally to[threonine](threonine.md). This makes it crystal clear that they are not just located adjacently in the genome by chance: they are actually functionally related, and likely controlled by the same transcription factor: when you want one of them, you basically always want the three, because you must be are lacking [threonine](threonine.md). TODO find transcription factor!

The UniProt entry also shows an interactive browser of the [tertiary structure](tertiary-structure.md) of the protein. We note that there are currently two sources available: [X-ray crystallography](x-ray-crystallography.md) and [AlphaFold](alphafold.md). To be honest, the [AlphaFold](alphafold.md) one looks quite off!!!

By inspecting the [FASTA](fasta-format.md) for the entire genome, or by using the [NCBI open reading frame tool](ncbi-open-reading-frame-tool.md), we see that this gene lies entirely in its own [open reading frame](open-reading-frame.md), so it is quite boring

From the [FASTA](fasta-format.md) we see that the very first three [Codons](codon.md) at position 337 are
```
ATG CGA GTG
```
where `ATG` is the [start codon](start-codon.md), and CGA GTG should be the first two that actually go into the protein:
- CGA: [arginine](arginine.md)
- GTG: [valine](valine.md)

[https://ecocyc.org/gene?orgid=ECOLI&id=ASPKINIHOMOSERDEHYDROGI-MONOMER](https://ecocyc.org/gene?orgid=ECOLI&id=ASPKINIHOMOSERDEHYDROGI-MONOMER) mentions that the enzime is most active as [protein complex](protein-complex.md) with four copies of the same protein:

> Aspartate kinase I / homoserine dehydrogenase I comprises a [dimer](protein-dimer.md) of ThrA dimers. Although the dimeric form is catalytically active, the binding equilibrium dramatically favors the tetrameric form. The aspartate kinase and homoserine dehydrogenase activities of each ThrA monomer are catalyzed by independent domains connected by a linker region.

TODO image?

## ↑ Ancestors (13)

1. [E. Coli K-12 MG1655 gene](e-coli-k-12-mg1655-gene.md)
2. [E. Coli K-12 MG1655](e-coli-k-12-mg1655.md)
3. [E. Coli K-12](e-coli-k-12.md)
4. [E. Coli strain](e-coli-strain.md)
5. [Escherichia coli](escherichia-coli.md)
6. [List of bacteria](list-of-bacteria.md)
7. [Bacteria](bacteria.md)
8. [Species](species.md)
9. [Taxonomy](taxonomy-split.md)
10. [Biology](biology-split.md)
11. [Natural science](natural-science.md)
12. [Science](science-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (11)

- [BioCyc promoter database](biocyc-promoter-database.md)
- [E. Coli K-12 MG1655](e-coli-k-12-mg1655.md)
- [E. Coli K-12 MG1655 gene thrB](e-coli-k-12-mg1655-gene-thrb.md)
- [E. Coli K-12 MG1655 gene thrL](e-coli-k-12-mg1655-gene-thrl.md)
- [E. Coli K-12 MG1655 operon thrLABC](e-coli-k-12-mg1655-operon-thrlabc.md)
- [E. Coli K-12 MG1655 transcription unit thrLABC](e-coli-k-12-mg1655-transcription-unit-thrlabc.md)
- [Source code overview](e-coli-whole-cell-model-by-covert-lab/source-code-overview.md)
- [Enzyme](enzyme.md)
- [KEGG](kegg.md)
- [Polycistronic mRNA](polycistronic-mrna.md)
- [UniProt](uniprot.md)
