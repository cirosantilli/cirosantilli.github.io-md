# Link to an image or video in another file that has an `\x` on title from another file

↑ **Parent:** [Make `\Include` headers show on table of contents work for cirosantilli.com](make-include-headers-show-on-table-of-contents-work-for-cirosantilli-com.md)

Issue report at:  [https://github.com/ourbigbook/ourbigbook/issues/198](https://github.com/ourbigbook/ourbigbook/issues/198) Suppose you had:

programming-language.ciro

```
= Programming language

\Image[https://raw.githubusercontent.com/cirosantilli/media/master/python-logo.jpg]
{title=The \x[python-programming-language] logo}

== Python
{c}
{disambiguate=programming-language}
```

logos-i-like.ciro

```
= Logos I like

\x[image-the-python-logo]
```

Now, when rendering `\x[image-the-python-logo]`, we would need to fetch two IDs:
- `image-the-python-logo` for the `The ` and ` logo` part
- `python-programming-language` itself, to know that `\x[python-programming-language]` should render as `Python`

But after [group all SQL queries together](../4/group-all-sql-queries-together.md) was done, there was no way to know that rendering `image-the-python-logo` would imply also fetching `python-programming-language`.

This was solved by adding a new database entry type, `REFS_TABLE_X_TITLE_TITLE` to the existing References table, which tracks dependencies between IDs.

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
