# HumanEval

↑ **Parent:** [AI code generation benchmark](ai-code-generation-benchmark.md)  
🏷️ **Tags:** [OpenAI project](openai-project.md)

- [https://github.com/openai/human-eval](https://github.com/openai/human-eval)
- [https://arxiv.org/abs/2107.03374](https://arxiv.org/abs/2107.03374)

The tests are present in a gzip inside the Git repo: [https://github.com/openai/human-eval/blob/master/data/HumanEval.jsonl.gz](https://github.com/openai/human-eval/blob/master/data/HumanEval.jsonl.gz) These researchers.

To get a quick overview of the problems with [jq](jq.md):
```
jq -r '"==== \(.task_id) \(.entry_point)\n\(.prompt)"' <HumanEval.jsonl 
```

The first two problems are:
```
==== HumanEval/0 has_close_elements
from typing import List


def has_close_elements(numbers: List[float], threshold: float) -> bool:
    """ Check if in given list of numbers, are any two numbers closer to each other than
    given threshold.
    >>> has_close_elements([1.0, 2.0, 3.0], 0.5)
    False
    >>> has_close_elements([1.0, 2.8, 3.0, 4.0, 5.0, 2.0], 0.3)
    True
    """

==== HumanEval/1 separate_paren_groups
from typing import List


def separate_paren_groups(paren_string: str) -> List[str]:
    """ Input to this function is a string containing multiple groups of nested parentheses. Your goal is to
    separate those group into separate strings and return the list of those.
    Separate groups are balanced (each open brace is properly closed) and not nested within each other
    Ignore any spaces in the input string.
    >>> separate_paren_groups('( ) (( )) (( )( ))')
    ['()', '(())', '(()())']
    """
```
so we understand that it takes as input an empty function with a docstring and you have to fill the function body.

The paper also shows that there can be other defined functions besides the one you have to implement.

## ↑ Ancestors (9)

1. [AI code generation benchmark](ai-code-generation-benchmark.md)
2. [Automatic programming](automatic-programming.md)
3. [Compiler](compiler.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
