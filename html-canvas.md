# HTML canvas

↑ **Parent:** [HTML element](html-element.md)

[https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

Allows us to draw with JavaScript pixel by pixel! Great way to create [computational physics](computational-physics.md) demos!

Here is an animation demo with some useful controls:new class extends OurbigbookCanvasDemo {
  init() {
    super.init('hello');
    this.pixel\_size\_input = this.addInputAfterEnable(
      'Pixel size',
      {
        'min': 1,
        'type': 'number',
        'value': 1,
      }
    );
  }
  draw() {
    var pixel\_size = parseInt(this.pixel\_size\_input.value);
    for (var x = 0; x \< this.width; x += pixel\_size) {
      for (var y = 0; y \< this.height; y += pixel\_size) {
        var b = ((1.0 + Math.sin(this.time \* Math.PI / 16)) / 2.0);
        this.ctx.fillStyle =
          'rgba(' +
          (x / this.width) \* 255 + ',' +
          (y / this.height) \* 255 + ',' +
          b \* 255 +
          ',255)'
        ;
        this.ctx.fillRect(x, y, pixel\_size, pixel\_size);
      }
    }
  }
}

Bibliography: [https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_animations">https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_animations](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_animations">https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_animations)

**Table of contents**

- [WebGL](webgl.md)
  - [three.js](three-js.md)

## ↑ Ancestors (9)

1. [HTML element](html-element.md)
2. [HTML](html.md)
3. [Web technology](web-technology-split.md)
4. [Software](software-split.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
