# E. Coli K-12 MG1655

↑ **Parent:** [E. Coli K-12](e-coli-k-12.md)

[NCBI](national-center-for-biotechnology-information.md) taxonomy entry: [https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=511145](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=511145) This links to:
- [genome](genome.md): [https://www.ncbi.nlm.nih.gov/genome/?term=txid511145](https://www.ncbi.nlm.nih.gov/genome/?term=txid511145) From there there are links to either:
  - Download the [FASTA](fasta-format.md): "Download sequences in FASTA format for genome, protein"

    For the genome, you get a compressed [FASTA](fasta-format.md) file with extension `.fna` called `GCF_000005845.2_ASM584v2_genomic.fna` that starts with:
    ```
    >NC_000913.3 Escherichia coli str. K-12 substr. MG1655, complete genome
    AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGCTTCTGAACTG
    ```

    Using [`wc`](wc-unix.md) as in `wc GCF_000005845.2_ASM584v2_genomic.fna` gives 58022 lines, in [Vim](vim.md) we see that each line is 80 characters, except for the final one which is 52. So we have 58020 \* 80 + 52 = 4641652 =~ 4.6 Mbp


  - Interactively browse the sequence on the browser viewer: "Reference genome: Escherichia coli str. K-12 substr. MG1655" which eventually leads to: [https://www.ncbi.nlm.nih.gov/nuccore/556503834?report=graph](https://www.ncbi.nlm.nih.gov/nuccore/556503834?report=graph)

    If we zoom into the start, we hover over the very first [gene](gene.md)/[protein](protein-split.md): the famous (just kidding) [e. Coli K-12 MG1655 gene thrL](e-coli-k-12-mg1655-gene-thrl.md), at position 190-255.

    The second one is the much more interesting [e. Coli K-12 MG1655 gene thrA](e-coli-k-12-mg1655-gene-thra.md).
  - Gene list, with a total of 4,629 as of 2021: [https://www.ncbi.nlm.nih.gov/gene/?term=txid511145](https://www.ncbi.nlm.nih.gov/gene/?term=txid511145)

[KEGG](kegg.md) entry: [https://www.genome.jp/pathway/eco01100+M00022](https://www.genome.jp/pathway/eco01100+M00022)

[BioCyc promoter database](biocyc-promoter-database.md) query URL: [https://biocyc.org/group?id=:ALL-PROMOTERS&orgid=ECOLI](https://biocyc.org/group?id=:ALL-PROMOTERS&orgid=ECOLI)

**Table of contents**

- [E. Coli K-12 MG1655 origin of replication](e-coli-k-12-mg1655-origin-of-replication.md)
- [E. Coli K-12 MG1655 gene](e-coli-k-12-mg1655-gene.md)
  - [E. Coli K-12 MG1655 gene thrL](e-coli-k-12-mg1655-gene-thrl.md)
  - [E. Coli K-12 MG1655 gene thrA](e-coli-k-12-mg1655-gene-thra.md)
  - [E. Coli K-12 MG1655 gene thrB](e-coli-k-12-mg1655-gene-thrb.md)
  - [E. Coli K-12 MG1655 gene thrC](e-coli-k-12-mg1655-gene-thrc.md)
  - [E. Coli K-12 MG1655 gene yaaX](e-coli-k-12-mg1655-gene-yaax.md)
  - [E. Coli K-12 MG1655 gene dksA](e-coli-k-12-mg1655-gene-dksa.md)
  - [E. Coli K-12 MG1655 gene lrp](e-coli-k-12-mg1655-gene-lrp.md)
  - [E. Coli K-12 MG1655 gene fnr](e-coli-k-12-mg1655-gene-fnr.md)
  - [E. Coli K-12 MG1655 gene arcA](e-coli-k-12-mg1655-gene-arca.md)
  - [E. Coli K-12 MG1655 gene ytdX](e-coli-k-12-mg1655-gene-ytdx.md)
- [E. Coli K-12 MG1655 gene of unknown function](e-coli-k-12-mg1655-gene-of-unknown-function.md)
- [E. Coli K-12 MG1655 promoter](e-coli-k-12-mg1655-promoter.md)
  - [E. Coli K-12 MG1655 promoter thrLp](e-coli-k-12-mg1655-promoter-thrlp.md)
    - [E. Coli K-12 MG1655 operon thrLABC](e-coli-k-12-mg1655-operon-thrlabc.md)
    - [E. Coli K-12 MG1655 transcription unit thrL](e-coli-k-12-mg1655-transcription-unit-thrl.md)
    - [E. Coli K-12 MG1655 transcription unit thrLABC](e-coli-k-12-mg1655-transcription-unit-thrlabc.md)

## ↑ Ancestors (11)

1. [E. Coli K-12](e-coli-k-12.md)
2. [E. Coli strain](e-coli-strain.md)
3. [Escherichia coli](escherichia-coli.md)
4. [List of bacteria](list-of-bacteria.md)
5. [Bacteria](bacteria.md)
6. [Species](species.md)
7. [Taxonomy](taxonomy-split.md)
8. [Biology](biology-split.md)
9. [Natural science](natural-science.md)
10. [Science](science-split.md)
11. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (7)

- [BioCyc promoter database](biocyc-promoter-database.md)
- [E. Coli K-12 MG1655 gene thrA](e-coli-k-12-mg1655-gene-thra.md)
- [E. Coli K-12 MG1655 gene thrL](e-coli-k-12-mg1655-gene-thrl.md)
- [E. Coli strain](e-coli-strain.md)
- [Escherichia coli](escherichia-coli.md)
- [National Center for Biotechnology Information](national-center-for-biotechnology-information.md)
- [UniProt](uniprot.md)
