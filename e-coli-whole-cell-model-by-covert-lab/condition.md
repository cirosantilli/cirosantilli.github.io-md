# Condition

↑ **Parent:** [Source code overview](source-code-overview.md)

- `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` contains the nutrients in a minimal environment in which the cell survives:
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
  If we compare that to `reconstruction/ecoli/flat/condition/nutrient/minimal_plus_amino_acids.tsv`, we see that it adds the 20 [amino acids](../amino-acid.md) on top of the minimal condition:
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

  We can try to understand the less obvious ones:
  - `ADP`: TODO
  - `PI`: TODO
  - `PROTON[c]`: presumably a measure of [pH](../ph.md)
  - `GLC[p]`: [glucose](../glucose.md), this can be seen by comparing `minimal.tsv` with `minimal_no_glucose.tsv`
  - `AMMONIUM`: [ammonium](../ammonium.md). This appears to be the primary source of [nitrogen](../nitrogen.md) [atoms](../atom.md) for producing [amino acids](../amino-acid.md).
  - `CYTOSINE[c]`: hmmm, why is external [cytosine](../cytosine.md) needed? Weird.
- `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/` contains sequences of conditions for each time. For example:
  - `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/000000_basal.tsv` contains:
    ```
    "time (units.s)" "nutrients"
    0 "minimal"
    ```

    which means just using `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` until infinity. That is the default one used by `runSim.py`, as can be seen from `./out/manual/wildtype_000000/000000/generation_000000/000000/simOut/Environment/attributes/nutrientTimeSeriesLabel` which contains just `000000_basal`.
  - `reconstruction/ecoli/flat/reconstruction/ecoli/flat/condition/timeseries/000001_cut_glucose.tsv` is more interesting and contains:
    ```
    "time (units.s)" "nutrients"
    0 "minimal"
    1200 "minimal_no_glucose"
    ```

    so we see that this will shift the conditions half-way to a condition that will eventually kill the bacteria because it will run out of [glucose](../glucose.md) and thus energy!

  Timeseries can be selected with `--variant nutrientTimeSeries X Y`, see also: [run variants](run-variants.md).

  We can use that variant with:
  ```
  VARIANT="condition" FIRST_VARIANT_INDEX=1 LAST_VARIANT_INDEX=1 python runscripts/manual/runSim.py
  ```
- `reconstruction/ecoli/flat/condition/condition_defs.tsv` contains lines of form:
  ```
  "condition" "nutrients"                "genotype perturbations" "doubling time (units.min)" "active TFs"
  "basal"     "minimal"                  {}                       44.0                        []
  "no_oxygen" "minimal_minus_oxygen"     {}                       100.0                       []
  "with_aa"   "minimal_plus_amino_acids" {}                       25.0                        ["CPLX-125", "MONOMER0-162", "CPLX0-7671", "CPLX0-228", "MONOMER0-155"]
  ```


  - `condition` refers to entries in `reconstruction/ecoli/flat/condition/condition_defs.tsv`
  - `nutrients` refers to entries under `reconstruction/ecoli/flat/condition/nutrient/`, e.g. `reconstruction/ecoli/flat/condition/nutrient/minimal.tsv` or `reconstruction/ecoli/flat/condition/nutrient/minimal_plus_amino_acids.tsv`
  - `genotype perturbations`: there aren't any in the file, but this suggests that genotype modifications can also be incorporated here
  - `doubling time`: TODO experimental data? Because this should be a simulation output, right? Or do they cheat and fix doubling by time?
  - `active TFs`: this suggests that they are cheating [transcription factors](../transcription-factor.md) here, as those would ideally be functions of other more basic inputs

## ↑ Ancestors (12)

1. [Source code overview](source-code-overview.md)
2. [E. Coli Whole Cell Model by Covert Lab](../e-coli-whole-cell-model-by-covert-lab-split.md)
3. [E. Coli whole cell simulation](../e-coli-whole-cell-simulation.md)
4. [Escherichia coli](../escherichia-coli.md)
5. [List of bacteria](../list-of-bacteria.md)
6. [Bacteria](../bacteria.md)
7. [Species](../species.md)
8. [Taxonomy](../taxonomy-split.md)
9. [Biology](../biology-split.md)
10. [Natural science](../natural-science.md)
11. [Science](../science-split.md)
12. [Ciro Santilli's Homepage](../split.md)

## ← Incoming links (1)

- [Default run variant](default-run-variant.md)
