# WebGL

↑ **Parent:** [HTML canvas](html-canvas.md)  
🏷️ **Tags:** [OpenGL](opengl.md)

[https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/By_example](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/By_example)

new class extends OurbigbookCanvasDemo {
  init() {
    super.init('webgl', {context\_type: 'webgl'});
    this.ctx.viewport(0, 0, this.ctx.drawingBufferWidth, this.ctx.drawingBufferHeight);
    this.ctx.clearColor(0.0, 0.0, 0.0, 1.0);
    this.vertexShaderSource = \`
\#version 100
precision highp float;
attribute float position;
void main() {
  gl\_Position = vec4(position, 0.0, 0.0, 1.0);
  gl\_PointSize = 64.0;
}
\`;

    this.fragmentShaderSource = \`
\#version 100
precision mediump float;
void main() {
  gl\_FragColor = vec4(0.18, 0.0, 0.34, 1.0);
}
\`;
    this.vertexShader = this.ctx.createShader(this.ctx.VERTEX\_SHADER);
    this.ctx.shaderSource(this.vertexShader, this.vertexShaderSource);
    this.ctx.compileShader(this.vertexShader);
    this.fragmentShader = this.ctx.createShader(this.ctx.FRAGMENT\_SHADER);
    this.ctx.shaderSource(this.fragmentShader, this.fragmentShaderSource);
    this.ctx.compileShader(this.fragmentShader);
    this.program = this.ctx.createProgram();
    this.ctx.attachShader(this.program, this.vertexShader);
    this.ctx.attachShader(this.program, this.fragmentShader);
    this.ctx.linkProgram(this.program);
    this.ctx.detachShader(this.program, this.vertexShader);
    this.ctx.detachShader(this.program, this.fragmentShader);
    this.ctx.deleteShader(this.vertexShader);
    this.ctx.deleteShader(this.fragmentShader);
    if (!this.ctx.getProgramParameter(this.program, this.ctx.LINK\_STATUS)) {
      console.log('error ' + this.ctx.getProgramInfoLog(this.program));
      return;
    }
    this.ctx.enableVertexAttribArray(0);
    var buffer = this.ctx.createBuffer();
    this.ctx.bindBuffer(this.ctx.ARRAY\_BUFFER, buffer);
    this.ctx.vertexAttribPointer(0, 1, this.ctx.FLOAT, false, 0, 0);
    this.ctx.useProgram(this.program);
  }
  draw() {
    this.ctx.clear(this.ctx.COLOR\_BUFFER\_BIT);
    this.ctx.bufferData(this.ctx.ARRAY\_BUFFER, new Float32Array(\[Math.sin(this.time / 60.0)\]), this.ctx.STATIC\_DRAW);
    this.ctx.drawArrays(this.ctx.POINTS, 0, 1);
  }
}**Table of contents**

- [three.js](three-js.md)

## ↑ Ancestors (10)

1. [HTML canvas](html-canvas.md)
2. [HTML element](html-element.md)
3. [HTML](html.md)
4. [Web technology](web-technology-split.md)
5. [Software](software-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Wave equation solver](wave-equation-solver.md)
