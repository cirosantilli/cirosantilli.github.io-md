<h1 id="aviad12g-arc-agi-solution">aviad12g/ARC-AGI-solution </h1>

↑ **Parent:** [Local CPU ARC-AGI without LLM](local-cpu-arc-agi-without-llm.md)

[https://github.com/aviad12g/ARC-AGI-solution](https://github.com/aviad12g/ARC-AGI-solution)

Interesting looking repo with optional [GPU](graphics-processing-unit.md) and optional [LLM](large-language-model.md).

It seems to have been tested on something older than [Ubuntu 24.04](ubuntu-24-04.md), as 24.04 install requires some porting, started process at: [https://github.com/cirosantilli/ARC-AGI-solution/tree/ubuntu-24-04](https://github.com/cirosantilli/ARC-AGI-solution/tree/ubuntu-24-04) but gave up to try [Ubuntu 22.04](ubuntu-22-04.md) instead.

[Ubuntu 22.04](ubuntu-22-04.md) [Docker](docker-software.md) install worked without patches, after installing [Poetry](poetry-python-package-manager.md) e.g. to try and solve [1ae2feb7](arc-agi-2-problem/list/1ae2feb7.md):
```
git clone https://github.com/aviad12g/ARC-AGI-solution
cd ARC-AGI-solution
git checkout f3283f727488ad98fe575ea6a5ac981e4a188e49
poetry install
git clone https://github.com/arcprize/ARC-AGI-2
`poetry env activate`
export PYTHONPATH="$PWD/src:$PYTHONPATH"
python3 -m arc_solver.cli.main solve ARC-AGI-2/data/evaluation/1ae2feb7.json
```
but towards the end we have:
```
{
  "success": false,
  "error": "Search failed: no_multi_example_solution",
  "search_stats": {
    "nodes_expanded": 21,
    "nodes_generated": 903,
    "termination_reason": "no_multi_example_solution",
    "candidates_generated": 25,
    "examples_validated": 3,
    "validation_success_rate": 0.0,
    "multi_example_used": true
  },
  "predictions": [
    null,
    null,
    null
  ],
  "computation_time": 30.234344280001096,
  "task_id": "1ae2feb7",
  "task_file": "ARC-AGI-2/data/evaluation/1ae2feb7.json",
  "solver_version": "0.1.0",
  "total_time": 30.24239572100123,
  "timestamp": 1760353369.9701269
}

Task: 1ae2feb7.json
Success: False
Error: Search failed: no_multi_example_solution
Multi-example validation: ENABLED
Training examples validated: 3
Candidates generated: 25
Validation success rate: 0.0%
Computation time: 30.23s
Total time: 30.24s
```
so it failed.

Let's see if any of them work at all as advertised:
```
ls ARC-AGI-2/data/evaluation/ | xargs -I'{}' python3 -m arc_solver.cli.main solve 'ARC-AGI-2/data/evaluation/{}' |& tee tmp.txt
```
and at the end:
```
grep 'Success: True' tmp.txt | wc
```
has only 7 successes.

Also weirdly 
```
grep 'Success: True' tmp.txt | wc
```
only has 102 hits, but there were 120 JSON tasks in that folder. I search for the missing executions:
```
diff -u <(grep Task: tmp.txt | cut -d' ' -f2) <(ls ARC-AGI-2/data/evaluation)
```
The first missing one is 135a2760, it blows up with:
```
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
```
and grepping ERROR gives us:
```
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type SizePredicate is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type ndarray is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type ndarray is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type ndarray is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type ndarray is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
```
Reported at: [https://github.com/aviad12g/ARC-AGI-solution/issues/1](https://github.com/aviad12g/ARC-AGI-solution/issues/1)

## ↑ Ancestors (14)

1. [Local CPU ARC-AGI without LLM](local-cpu-arc-agi-without-llm.md)
2. [ARC-AGI without LLM](arc-agi-without-llm.md)
3. [ARC-AGI implementation](arc-agi-implementation.md)
4. [ARC-AGI](arc-agi.md)
5. [AGI test](agi-test.md)
6. [Artificial general intelligence](artificial-general-intelligence.md)
7. [AI by capability](ai-by-capability.md)
8. [Artificial intelligence](artificial-intelligence-split.md)
9. [Machine learning](machine-learning-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)
