# `\Include` and `\x` and working on dynamic website

↑ **Parent:** [Advances](advances.md)

<a id="_3"></a>
This was the major final step of fully integrating the [OurBigBook CLI](../../../ourbigbook-cli.md) into the dynamic website (besides fixing some nasty bugs that escaped passed by me from the previous newsletter).

<a id="_4"></a>
The implementation was done by "simply" reusing [scopes](https://cirosantilli.com/ourbigbook/h-scope-argument), e.g.: `cirosantilli`'s article about `mathematics` has scope `cirosantilli` and full ID `cirosantilli/mathematics`.

<a id="_5"></a>
That on the website is equivalent to a local file structure of:<a id="_6"></a>

```
cirodown/mathematics.bigb
```

<a id="_7"></a>
The problem is that a bunch of subdirectory scope operations were broken locally as well, as it simply wasn't a major use case. But now they became a major use case for , so I fixed them.

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#5](../5-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)
