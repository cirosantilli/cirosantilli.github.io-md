<h1 id="make-include-headers-show-on-table-of-contents-work-for-cirosantilli-com">Make <code>\Include</code> headers show on table of contents work for cirosantilli.com</h1>

↑ **Parent:** [Advances](advances.md)

<a id="_30"></a>
One of the [key advances of the previous update](../4/the-table-of-contents-shows-across-different-files-via-include.md) was to show include headers on the table of contents.

<a id="_31"></a>
This was to allow splitting source files freely.

<a id="_32"></a>
While that goal was in principle achieved in that commit, when I went ahead to split the huge index of cirosantilli.com into multiple files, I notice several bugs that took a week to fix.

<a id="_33"></a>
After all of these were solved, I finally managed to split the [README](https://github.com/cirosantilli/cirosantilli.github.io/blob/84c8a6e7fdbe252041accfb7a06d9b7462287131/README.ciro) at: [https://github.com/cirosantilli/cirosantilli.github.io/commit/84c8a6e7fdbe252041accfb7a06d9b7462287131](https://github.com/cirosantilli/cirosantilli.github.io/commit/84c8a6e7fdbe252041accfb7a06d9b7462287131) and keep the previous desired output. You can now see that the README contains just:<a id="_34"></a>

```
\Include[ciro-santilli]
\Include[science]
\Include[mathematics]
\Include[technology]
\Include[art]
```

<a id="_35"></a>
This split led to a small positive modification of the output as follows. Previously, a section such as "Quantum Electrodynamics" would have been present in the monolithic README.ciro as:<a id="_36"></a>

```
= Quantum electrodynamics
```
If you visited [https://cirosantilli.com/quantum-electrodynamics](https://cirosantilli.com/quantum-electrodynamics), you would see see a link to the "nosplit" version, which would link you back to [https://cirosantilli.com#quantum-electrodynamics](https://cirosantilli.com#quantum-electrodynamics), but that is not great, since this is was a humongous page with all of the README.ciro, and took long to display.

<a id="_37"></a>
After the split, `= Quantum electrodynamics` is present under `science.ciro`, and the nosplit version is the more manageable [https://cirosantilli.com/science#quantum-electrodynamics](https://cirosantilli.com/science#quantum-electrodynamics).

<a id="_38"></a>
The key changes that were missing for that to happen were:<a id="_39"></a>

<a id="_40"></a>
- [link to an image or video in another file that has an `\x` on title from another file](link-to-an-image-or-video-in-another-file-that-has-an-x-on-title-from-another-file.md)

**Table of contents**

- [Link to an image or video in another file that has an `\x` on title from another file](link-to-an-image-or-video-in-another-file-that-has-an-x-on-title-from-another-file.md)

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#5](../5-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)
