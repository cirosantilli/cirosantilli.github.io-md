# CSS flex

↑ **Parent:** [Cascading Style Sheets](cascading-style-sheets.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CSS_Flexible_Box_Layout)

- [css/flex.html](css/flex.html): illustrates basic flex usage, including:
- `flex-grow`: if there's space left, this determines how much extra space will be given to each.
- `flex-basis`: the size the items want to be. But if there isnt' enough space, this can be cut up.

  Note that the minimal space required by children of the flex children cannot be necessarily cut up, and might lead things to overflow out of the container.
- `flex-shrink`: if there's space missing, this determines how much extra space will be removed from each `flex-basis`

Other examples include:
- [css/flex-fill-vertical.html](css/flex-fill-vertical.html): minimal setup for a editor: [https://docs.ourbigbook.com/editor](https://docs.ourbigbook.com/editor)

That example calculates and displays the final widths via [JavaScript](javascript.md), making it easier to understand the calculations being done.

Answers: [https://stackoverflow.com/questions/28473807/how-does-flex-grow0-get-interpreted/69995712#69995712](https://stackoverflow.com/questions/28473807/how-does-flex-grow0-get-interpreted/69995712#69995712)

Bibliography:
- [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)

## ↑ Ancestors (8)

1. [Cascading Style Sheets](cascading-style-sheets.md)
2. [Web technology](web-technology-split.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
