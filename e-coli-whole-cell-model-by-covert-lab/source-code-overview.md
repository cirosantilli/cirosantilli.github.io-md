# Source code overview

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](../e-coli-whole-cell-model-by-covert-lab-split.md)

<a id="_108"></a>
The key model database is located in the source code at `reconstruction/ecoli/flat`.

<a id="_109"></a>
Let's try to understand some interesting looking, with a special focus on our understanding of the tiny [E. Coli K-12 MG1655 operon thrLABC](../e-coli-k-12-mg1655-operon-thrlabc.md) part of the metabolism, which we have well understood at [Section "E. Coli K-12 MG1655 operon thrLABC"](../e-coli-k-12-mg1655-operon-thrlabc.md).

<a id="_110"></a>
We'll realize that a lot of data and IDs come from/match [BioCyc](../biocyc.md) quite closely.

<a id="_111"></a>
<a id="_112"></a>
- <a id="_113"></a>
  `reconstruction/ecoli/flat/compartments.tsv` contains [cellular compartment](../cellular-compartment.md) information:<a id="_114"></a>

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
  - `BAC-NUCLEOID`: [nucleoid](../nucleoid.md)
  <a id="_118"></a>
  - `CELL-PROJECTION`: [cell projection](../cell-projection.md)
  <a id="_119"></a>
  - `CW-BAC-NEG`: TODO confirm: [cell wall](../cell-wall.md) (of a [Gram-negative bacteria](../gram-negative-bacteria.md))
  <a id="_120"></a>
  - `CYTOSOL`: [cytosol](../cytosol.md)
  <a id="_121"></a>
  - `EXTRACELLULAR`: outside the cell
  <a id="_122"></a>
  - `MEMBRANE`: [cell membrane](../cell-membrane.md)
  <a id="_123"></a>
  - `OUTER-MEM`: [bacterial outer membrane](../bacterial-outer-membrane.md)
  <a id="_124"></a>
  - `PERI-BAC`: [periplasm](../periplasm.md)
  <a id="_125"></a>
  - `PILUS`: [pilus](../pilus.md)
  <a id="_126"></a>
  - `PM-BAC-NEG`: TODO: [plasma membrane](../organelle.md), but that is the same as [cell membrane](../cell-membrane.md) no?
<a id="_127"></a>
- `reconstruction/ecoli/flat/promoters.tsv` contains [promoter](../promoter-genetics.md) information. Simple file, sample lines:<a id="_128"></a>

  ```
  "position" "direction" "id" "name"
  148 "+" "PM00249" "thrLp"
  ```

  corresponds to [E. Coli K-12 MG1655 promoter thrLp](../e-coli-k-12-mg1655-promoter-thrlp.md), which starts as position 148.
<a id="_129"></a>
- `reconstruction/ecoli/flat/proteins.tsv` contains [protein](../protein-split.md) information. Sample line corresponding to [e. Coli K-12 MG1655 gene thrA](../e-coli-k-12-mg1655-gene-thra.md):<a id="_130"></a>

  ```
  "aaCount" "name" "seq" "comments" "codingRnaSeq" "mw" "location" "rnaId" "id" "geneId"
  [91, 46, 38, 44, 12, 53, 30, 63, 14, 46, 89, 34, 23, 30, 29, 51, 34, 4, 20, 0, 69] "ThrA" "MRVL..." "Location information from Ecocyc dump." "AUGCGAGUGUUG..." [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 89103.51099999998, 0.0, 0.0, 0.0, 0.0] ["c"] "EG10998_RNA" "ASPKINIHOMOSERDEHYDROGI-MONOMER" "EG10998"
  ```

  so we understand that:<a id="_131"></a>

  <a id="_132"></a>
  - `aaCount`: [amino acid](../amino-acid.md) count, how many of each of the 20 [proteinogenic amino acid](../proteinogenic-amino-acid.md) are there
  <a id="_133"></a>
  - `seq`: full sequence, using the single letter abbreviation of the [proteinogenic amino acids](../proteinogenic-amino-acid.md)
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
    - `23srRNA`, `16srRNA`, `5srRNA` are the three structural [RNAs](../rna.md) present in the [ribosome](../ribosome.md): [23S ribosomal RNA](../23s-ribosomal-rna.md), [16S ribosomal RNA](../16s-ribosomal-rna.md), [5S ribosomal RNA](../5s-ribosomal-rna.md), all others are obvious:
    <a id="_138"></a>
    - [tRNA](../transfer-rna.md)
    <a id="_139"></a>
    - [mRNA](../messenger-rna.md)
    <a id="_140"></a>
    - [protein](../protein-split.md). This is the seventh class, and this enzyme only contains mass in this class as expected.
    <a id="_141"></a>
    - [metabolite](../metabolite.md)
    <a id="_142"></a>
    - [water](../water.md)
    <a id="_143"></a>
    - [DNA](../dna-split.md)
    <a id="_144"></a>
    - [RNA](../rna.md): TODO `rna` vs `miscRNA`
  <a id="_145"></a>
  - `location`: [cell compartment](../cellular-compartment.md) where the protein is present, `c` defined at `reconstruction/ecoli/flat/compartments.tsv` as [cytoplasm](../cytoplasm.md), as expected for something that will make an [amino acid](../amino-acid.md)
<a id="_146"></a>
- <a id="_147"></a>
  `reconstruction/ecoli/flat/rnas.tsv`: TODO vs `transcriptionUnits.tsv`. Sample lines:<a id="_148"></a>

  ```
  "halfLife" "name" "seq" "type" "modifiedForms" "monomerId" "comments" "mw" "location" "ntCount" "id" "geneId" "microarray expression"
  174.0 "ThrA [RNA]" "AUGCGAGUGUUG..." "mRNA" [] "ASPKINIHOMOSERDEHYDROGI-MONOMER" "" [0.0, 0.0, 0.0, 0.0, 790935.00399999996, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0] ["c"] [553, 615, 692, 603] "EG10998_RNA" "EG10998" 0.0005264904
  ```

  <a id="_149"></a>

  <a id="_150"></a>
  - `halfLife`: [half-life](../half-life.md)
  <a id="_151"></a>
  - `mw`: molecular weight, same as in `reconstruction/ecoli/flat/proteins.tsv`. This [molecule](../molecule.md) only have weight in the `mRNA` class, as expected, as it just codes for a protein
  <a id="_152"></a>
  - `location`: same as in `reconstruction/ecoli/flat/proteins.tsv`
  <a id="_153"></a>
  - `ntCount`: [nucleotide](../nucleotide.md) count for each of the ATGC
  <a id="_154"></a>
  - `microarray expression`: presumably refers to [DNA microarray](../dna-microarray.md) for [gene expression profiling](../gene-expression-profiling.md), but what measure exactly?
<a id="_155"></a>
- `reconstruction/ecoli/flat/sequence.fasta`: [FASTA](../fasta-format.md) [DNA](../dna-split.md) sequence, first two lines:<a id="_156"></a>

  ```
  >E. coli K-12 MG1655 U00096.2 (1 to 4639675 = 4639675 bp)
  AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGCTTCTG
  ```
<a id="_157"></a>
- <a id="_158"></a>
  `reconstruction/ecoli/flat/transcriptionUnits.tsv`: [transcription units](../transcription-unit.md). We can observe for example the two different transcription units of the [E. Coli K-12 MG1655 operon thrLABC](../e-coli-k-12-mg1655-operon-thrlabc.md) in the lines:<a id="_159"></a>

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
  - `id`: matches exactly those used in [BioCyc](../biocyc.md), which is quite nice, might be more or less standardized:<a id="_164"></a>

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
  `reconstruction/ecoli/flat/metabolites.tsv` contains [metabolite](../metabolite.md) information. Sample lines:<a id="_171"></a>

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
  `reconstruction/ecoli/flat/reactions.tsv` contains [chemical reaction](../chemical-reaction.md) information. Sample lines:<a id="_178"></a>

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
  - `catalized by`: here we see `ASPKINIHOMOSERDEHYDROGI-CPLX`, which we can guess is a [protein complex](../protein-complex.md) made out of `ASPKINIHOMOSERDEHYDROGI-MONOMER`, which is the ID for the `thrA` we care about! This is confirmed in `complexationReactions.tsv`.
<a id="_181"></a>
- `reconstruction/ecoli/flat/complexationReactions.tsv` contains information about [chemical reactions](../chemical-reaction.md) that produce [protein complexes](../protein-complex.md):<a id="_182"></a>

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
- `reconstruction/ecoli/flat/proteinComplexes.tsv` contains [protein complex](../protein-complex.md) information:<a id="_185"></a>

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
- `reconstruction/ecoli/flat/protein_half_lives.tsv` contains the [half-life](../half-life.md) of [proteins](../protein-split.md). Very few proteins are listed however for some reason.
<a id="_187"></a>
- `reconstruction/ecoli/flat/tfIds.csv`: [transcription factors](../transcription-factor.md) information:<a id="_188"></a>

  ```
  "TF"   "geneId"  "oneComponentId"  "twoComponentId" "nonMetaboliteBindingId" "activeId" "notes"
  "arcA" "EG10061" "PHOSPHO-ARCA"    "PHOSPHO-ARCA"
  "fnr"  "EG10325" "FNR-4FE-4S-CPLX" "FNR-4FE-4S-CPLX"
  "dksA" "EG10230"
  ```

**Table of contents**

- [Condition](condition.md)

## ↑ Ancestors (11)

1. [E. Coli Whole Cell Model by Covert Lab](../e-coli-whole-cell-model-by-covert-lab-split.md)
2. [E. Coli whole cell simulation](../e-coli-whole-cell-simulation.md)
3. [Escherichia coli](../escherichia-coli.md)
4. [List of bacteria](../list-of-bacteria.md)
5. [Bacteria](../bacteria.md)
6. [Species](../species.md)
7. [Taxonomy](../taxonomy-split.md)
8. [Biology](../biology-split.md)
9. [Natural science](../natural-science.md)
10. [Science](../science-split.md)
11. [Ciro Santilli's Homepage](../split.md)
