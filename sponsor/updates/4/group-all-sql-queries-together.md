# Group all SQL queries together

↑ **Parent:** [Advances](advances.md)

<a id="_14"></a>
And do 5 big queries instead of hundreds of smaller ones.

<a id="_15"></a>
For example, a README.ciro document that references another document saying:<a id="_16"></a>

```
The \x[speed-of-light] is fast.
```
needs to fetch "speed-of-light" from the ID database (previously populated e.g. by preparsing light.ciro:<a id="_17"></a>

```
= Light

== Speed of light
```
to decide that it should display as "Speed of light" (the title rather than the ID).

<a id="_18"></a>
Previously, I was doing a separate fetch for each `\x[]` as they were needed, leading to hundreds of them at different times.

<a id="_19"></a>
Now I refactored things so that I do very few database queries, but large ones that fetch everything during parsing. And then at render time they are all ready in cache.

<a id="_20"></a>
This will be fundamental for the live preview on the browser, where the roundtrip to server would make it impossible

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
- [Link to an image or video in another file that has an `\x` on title from another file](../5/link-to-an-image-or-video-in-another-file-that-has-an-x-on-title-from-another-file.md)
