# The table of contents shows across different files via `\Include`

↑ **Parent:** [Advances](advances.md)

<a id="_21"></a>
E.g.:

<a id="_22"></a>
README.ciro<a id="_23"></a>

```
= My website

== h2

\Include[not-readme]
```
not-readme.ciro<a id="_24"></a>

```
= Not readme

== Not readme h2
```
the table of contents for `index.html` also contains the headers for `not-readme.ciro` producing:<a id="_25"></a>

<a id="_26"></a>
- My website<a id="_27"></a>

  <a id="_28"></a>
  - h2<a id="_29"></a>

    <a id="_30"></a>
    - Not readme<a id="_31"></a>

      <a id="_32"></a>
      - Not readme h2

<a id="_33"></a>
This feature means that you can split large input files if rendering starts to slow you down, and things will still render exactly the same, with the larger table of contents.

<a id="_34"></a>
This will be especially important for the website because initially I want users to be able to edit one header at a time, and join all headers with `\Include`. But I still want the ToC to show those children.

<a id="_35"></a>
This was a bit hard because it required doing RECURSIVE SQL queries, something I hadn't done before: [https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree/192462#192462 +](https://stackoverflow.com/questions/192220/what-is-the-most-efficient-elegant-way-to-parse-a-flat-table-into-a-tree/192462#192462 +) of course the usual refactor a bunch of stuff and fix tests until you go mad.

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#4](../4-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)

## ← Incoming links (2)

- [Ourbigbook.com](ourbigbook-com.md)
- [Make `\Include` headers show on table of contents work for cirosantilli.com](../5/make-include-headers-show-on-table-of-contents-work-for-cirosantilli-com.md)
