# Link to an image or video in another file that has an `\x` on title from another file

↑ **Parent:** [Make `\Include` headers show on table of contents work for cirosantilli.com](make-include-headers-show-on-table-of-contents-work-for-cirosantilli-com.md)

<a id="_41"></a>
Issue report at:  [https://github.com/ourbigbook/ourbigbook/issues/198](https://github.com/ourbigbook/ourbigbook/issues/198) Suppose you had:

<a id="_42"></a>
programming-language.ciro

<a id="_43"></a>
```
= Programming language

\Image[https://raw.githubusercontent.com/cirosantilli/media/master/python-logo.jpg]
{title=The \x[python-programming-language] logo}

== Python
{c}
{disambiguate=programming-language}
```

<a id="_44"></a>
logos-i-like.ciro

<a id="_45"></a>
```
= Logos I like

\x[image-the-python-logo]
```

<a id="_46"></a>
Now, when rendering `\x[image-the-python-logo]`, we would need to fetch two IDs:<a id="_47"></a>

<a id="_48"></a>
- `image-the-python-logo` for the `The ` and ` logo` part
<a id="_49"></a>
- `python-programming-language` itself, to know that `\x[python-programming-language]` should render as `Python`

<a id="_50"></a>
But after [group all SQL queries together](../4/group-all-sql-queries-together.md) was done, there was no way to know that rendering `image-the-python-logo` would imply also fetching `python-programming-language`.

<a id="_51"></a>
This was solved by adding a new database entry type, `REFS_TABLE_X_TITLE_TITLE` to the existing References table, which tracks dependencies between IDs.

<a id="_52"></a>
After this was setup, we can now know that `image-the-python-logo` depends on `image-the-python-logo`, and then fetch both of them together in a single [JOIN](../../../join-sql.md).

## ↑ Ancestors (8)

1. [Make `\Include` headers show on table of contents work for cirosantilli.com](make-include-headers-show-on-table-of-contents-work-for-cirosantilli-com.md)
2. [Advances](advances.md)
3. [Ourbigbook.com](ourbigbook-com.md)
4. [Ciro's Edict \#5](../5-split.md)
5. [Sponsor updates](../../../sponsor-updates.md)
6. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
7. [Ciro Santilli](../../../ciro-santilli-split.md)
8. [Ciro Santilli's Homepage](../../../split.md)

## ← Incoming links (1)

- [Make `\Include` headers show on table of contents work for cirosantilli.com](make-include-headers-show-on-table-of-contents-work-for-cirosantilli-com.md)
