# Install and first run

↑ **Parent:** [E. Coli Whole Cell Model by Covert Lab](../e-coli-whole-cell-model-by-covert-lab-split.md)

<a id="_14"></a>
At [7e4cc9e57de76752df0f4e32eca95fb653ea64e4](https://github.com/CovertLab/WholeCellEcoliRelease/tree/7e4cc9e57de76752df0f4e32eca95fb653ea64e4) you basically need to use the [Docker](../docker-software.md) image on [Ubuntu](../ubuntu.md) 21.04 due to [pip](../pip-package-manager.md) breaking changes... (not their fault). Perhaps [pyenv](../pyenv.md) would solve things, but who has the patience for that?!?!

<a id="_15"></a>
The Docker setup from README does just work. The image download is a bit tedius, as it requires you to create a GitHub API key as described in the README, but there must be reasons for that.

<a id="_16"></a>
Once the image is downloaded, you really want to run is from the root of the source tree:<a id="_17"></a>

```
sudo docker run --name=wcm -it -v "$(pwd):/wcEcoli" docker.pkg.github.com/covertlab/wholecellecolirelease/wcm-full
```
This mounts the host source under `/wcEcoli`, so you can easily edit and view output images from your host. Once inside Docker we can compile, run the simulation, and analyze results with:<a id="_18"></a>

```
make clean compile &&
python runscripts/manual/runFitter.py &&
python runscripts/manual/runSim.py &&
python runscripts/manual/analysisVariant.py &&
python runscripts/manual/analysisCohort.py &&
python runscripts/manual/analysisMultigen.py &&
python runscripts/manual/analysisSingle.py
```
The meaning of each of the analysis commands is described at [Section "Output overview"](output-overview.md).

<a id="_19"></a>
As a [Docker](../docker-software.md) refresher, after you stop the container, e.g. by restarting your computer or running `sudo docker stop wcm`, you can get back into it with:<a id="_20"></a>

```
sudo docker start wcm
sudo docker run -it wcm bash
```

<a id="_21"></a>
`runscripts/manual/runFitter.py` takes about 15 minutes, and it generates files such as `reconstruction/ecoli/dataclasses/process/two_component_system.py` ([related](https://github.com/CovertLab/WholeCellEcoliRelease/issues/20)) which is required to run the simulation, it is basically a part of the build.

<a id="_22"></a>
`runSim.py` does the main simulation, progress output contains lines of type:<a id="_23"></a>

```
Time (s)  Dry mass     Dry mass      Protein          RNA    Small mol     Expected
              (fg)  fold change  fold change  fold change  fold change  fold change
========  ========  ===========  ===========  ===========  ===========  ===========
    0.00    403.09        1.000        1.000        1.000        1.000        1.000
    0.20    403.18        1.000        1.000        1.000        1.000        1.000
```
and then it ended on the [Lenovo ThinkPad P51 (2017)](../ciro-santilli-s-hardware/lenovo-thinkpad-p51-2017.md) at:<a id="_24"></a>

```
 2569.18    783.09        1.943        1.910        2.005        1.950        1.963

Simulation finished:
 - Length: 0:42:49
 - Runtime: 0:09:13
```
when the cell had almost doubled, and presumably divided in 42 minutes of simulated time, which could make sense compared to the 20 under optimal conditions.

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

## ← Incoming links (1)

- [Time series run variant](time-series-run-variant.md)
