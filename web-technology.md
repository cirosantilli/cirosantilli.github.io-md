# Web technology

↑ **Parent:** [Software](software.md)

Cheatsheet on [HTML](#html), [Cascading Style Sheets](#cascading-style-sheets) and [JavaScript](programming-language.md#javascript).

Old cheat on separate repo: [web](web).

Now moving to either:
- separate files under: [web-cheat/](web-cheat/) for the boring stuff
- subsections under this section for the more exciting stuff!

Examples under:
- [Section "HTML"](#html)
- [Section "JavaScript browser example"](#javascript-browser-example)

**Table of contents**

- [World Wide Web](#world-wide-web)
  - [World Wide Web Consortium](#world-wide-web-consortium)
  - [History of the World Wide Web](#history-of-the-world-wide-web)
- [Webdev's Creed](#webdev-s-creed)
- [HTML](#html)
  - [HTML element](#html-element)
    - [HTML canvas](#html-canvas)
      - [WebGL](#webgl)
        - [three.js](#three-js)
    - [HTML `details` tag](#html-details-tag)
      - [html/details-toc.html](#_file/html/details-toc.html)
      - [HTML `summary` tag](#html-summary-tag)
- [Cascading Style Sheets](#cascading-style-sheets)
  - [CSS flex](#css-flex)
  - [Sass (stylesheet language)](#sass-stylesheet-language)
- [JavaScript browser example](#javascript-browser-example)
- [Website stack](#website-stack)
- [Asset bundler](#asset-bundler)
  - [webpack](webpack.md)
    - [webpack/template](webpack.md#_file/webpack/template)
    - [webpack/sass](webpack.md#_file/webpack/sass)
    - [webpack/no-js-inject](webpack.md#_file/webpack/no-js-inject)
    - [webpack Sass import](webpack.md#webpack-sass-import)
    - [webpack CSS ignore font format](webpack.md#webpack-css-ignore-font-format)
- [Push technology](#push-technology)
- [Web browser](#web-browser)
  - [Chromium (web browser)](#chromium-web-browser)
    - [Chromium bug](#chromium-bug)
      - [Chromium sometimes freezes due to autofill on omnibox ](#chromium-sometimes-freezes-due-to-autofill-on-omnibox)
    - [Electron (software framework)](#electron-software-framework)
      - [Software that uses Electron](#software-that-uses-electron)
    - [Disable JavaScript on Chromium](#disable-javascript-on-chromium)
  - [Firefox](#firefox)
  - [Google Chrome](#google-chrome)
    - [Chrome Android extension](#chrome-android-extension)
- [Web development](#web-development)
- [Web framework](#web-framework)
  - [Hello world website](#hello-world-website)
    - [A blog in every web framework](#a-blog-in-every-web-framework)
      - [gothinkster/realworld](#gothinkster-realworld)
        - [gothinkster/realworld implementation](#gothinkster-realworld-implementation)
    - [TodoMVC](#todomvc)
  - [Front-end web framework](#front-end-web-framework)
    - [Single page application](#single-page-application)
      - [Isomorphic JavaScript](#isomorphic-javascript)
        - [Server-side rendering](#server-side-rendering)
    - [List of front-end web frameworks](#list-of-front-end-web-frameworks)
      - [Angular.js](#angular-js)
      - [React](react.md)
        - [React JSX](react.md#react-jsx)
        - [React error](react.md#react-error)
          - [Cannot update a component while rendering a different component warning in React](react.md#cannot-update-a-component-while-rendering-a-different-component-warning-in-react)
        - [React example](react.md#react-example)
          - [react/hello.html](react.md#_file/react/hello.html)
          - [react/ref-twice.html](react.md#_file/react/ref-twice.html)
        - [React DOM manipulation](react.md#react-dom-manipulation)
          - [react/ref-click-counter.html](react.md#_file/react/ref-click-counter.html)
          - [react/ref-click-counter-func.html](react.md#_file/react/ref-click-counter-func.html)
        - [React class vs function component](react.md#react-class-vs-function-component)
          - [React class component](react.md#react-class-component)
          - [React function component](react.md#react-function-component)
            - [React hook](react.md#react-hook)
              - [`useEffect`](react.md#useeffect)
              - [`useRef`](react.md#useref)
              - [`useCallback`](react.md#usecallback)
        - [Next.js](react.md#next-js)
          - [Next.js example](react.md#next-js-example)
            - [nodejs/next/posts](react.md#_file/nodejs/next/posts)
            - [nodejs/next/ref-twice](react.md#_file/nodejs/next/ref-twice)
            - [nodejs/next/inject-into-static](react.md#_file/nodejs/next/inject-into-static)
          - [Node Express Sequelize Next.js realworld example app](react.md#node-express-sequelize-next-js-realworld-example-app)
      - [Vue.js](#vue-js)
        - [Nuxt.js](#nuxt-js)

## World Wide Web

↑ **Parent:** [Web technology](web-technology.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/World_Wide_Web)

### World Wide Web Consortium

↑ **Parent:** [World Wide Web](#world-wide-web)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium)

### History of the World Wide Web

↑ **Parent:** [World Wide Web](#world-wide-web)

<a id="video-why-web-tech-is-like-this-by-steve-sanderson-2022"></a>
**[Video 1](#video-why-web-tech-is-like-this-by-steve-sanderson-2022). Why web tech is like this by Steve Sanderson (2022)** [Source](https://www.youtube.com/watch?v=3QEoJRjxnxQ).

<h2 id="webdev-s-creed">Webdev's Creed</h2>

↑ **Parent:** [Web technology](web-technology.md)  
🏷️ **Tags:** [Essays by Ciro Santilli](ciro-santilli.md#essays-by-ciro-santilli), [Website stack](#website-stack)

> This is my [stack](#website-stack). There are many like it, but this one is mine.
> 
> My stack is my best friend. It is my life. I must master it as I must master my life.
> 
> Without me, my stack is useless. Without my stack, I am useless. I must fire my requests true. I must shoot straighter than my hackers who are trying to kill me. I must shoot him before he shoots me. I will ...
> 
> My stack is human, even as I am human, because it is my life. Thus, I will learn it as a brother. I will learn its weaknesses, its strength, its parts, its accessories, its [ORMs](software.md#object-relational-mapping) and its [asset bundlers](#asset-bundler). I will keep my stack clean and ready, even as I am clean and ready. We will become part of each other. We will ...
> 
> Before [God](religion.md#god), I swear this creed. My stack and I are the defenders of my website. We are the masters of our enemy. We are the saviors of my life.
> 
> So be it, until victory is mine and there is no enemy, but peace!

Explanation: this is an allusion to the [Rifleman's Creed](united-states.md#rifleman-s-creed). This particular version talks about the [website stack](#website-stack) chosen for a website, i.e. the libraries used.

[Ciro Santilli](ciro-santilli.md) has always felt that choosing a stack is an almost religious choice. It is perhaps part of why the prayer style of the original [Rifleman's Creed](united-states.md#rifleman-s-creed) resonates with the web stack choice.

It is very hard to know how things are going go, the ups and downs, before putting big hours into it.

And once you start, it is hard, though not impossible, to move away.

The same allusion would make sense with any complex library choice, but it is particularly apparent in web development since there are so many different web stacks to choose from. A bit like rifles, they are all somewhat [fungible](economy.md#fungibility), though of course not as much.

## HTML

↑ **Parent:** [Web technology](web-technology.md)  
🏷️ **Tags:** [Markup language](computer.md#markup-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/HTML)

Examples:
- [html/min.html](html/min.html): minimal valid HTML document. It is insane however.
- [html/min-sane.html](html/min-sane.html): minimal sane HTML document. There are smaller valid ones, but they are insane.
- [html/img.html](html/img.html)
- [html/img-broken.html](html/img-broken.html): [https://stackoverflow.com/questions/22051573/how-to-hide-image-broken-icon-using-only-css-html](https://stackoverflow.com/questions/22051573/how-to-hide-image-broken-icon-using-only-css-html)
- [html/img-load-lazy.html](html/img-load-lazy.html): [https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-lazily-only-when-they-are-in-the-viewport/57389607#57389607](https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-lazily-only-when-they-are-in-the-viewport/57389607#57389607)
- [html/iframe.html](html/iframe.html). Uses: [html/iframe2.html](html/iframe2.html), [html/hello.txt](html/hello.txt) and [html/hello](html/hello)
- forms
  - [html/form-password.html](html/form-password.html)
- [YouTube](website.md#youtube) embeds
  - [html/youtube-embed.html](html/youtube-embed.html)
  - [html/youtube-embed-lazy.html](html/youtube-embed-lazy.html): [https://stackoverflow.com/questions/7154958/lazy-load-iframe-delay-src-http-call-with-jquery/62523325#62523325](https://stackoverflow.com/questions/7154958/lazy-load-iframe-delay-src-http-call-with-jquery/62523325#62523325)

### HTML element

↑ **Parent:** [HTML](#html)

#### HTML canvas

↑ **Parent:** [HTML element](#html-element)

[https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

Allows us to draw with JavaScript pixel by pixel! Great way to create [computational physics](physics.md#computational-physics) demos!

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

##### WebGL

↑ **Parent:** [HTML canvas](#html-canvas)  
🏷️ **Tags:** [OpenGL](software.md#opengl)

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
}<h6 id="three-js">three.js</h6>

↑ **Parent:** [WebGL](#webgl)  
🏷️ **Tags:** [Graphics library](software.md#graphics-library)

#### HTML `details` tag

↑ **Parent:** [HTML element](#html-element)

<h5 id="_file/html/details-toc.html">html/details-toc.html</h5>

↑ **Parent:** [HTML `details` tag](#html-details-tag)

##### HTML `summary` tag

↑ **Parent:** [HTML `details` tag](#html-details-tag)

## Cascading Style Sheets

↑ **Parent:** [Web technology](web-technology.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cascading_Style_Sheets)

- [css/code-block.html](css/code-block.html)
- [css/img-table-vertical-center.html](css/img-table-vertical-center.html)
- [css/viewport-height.html](css/viewport-height.html): a div that is a tall as the viewport, and does not generate a toplevel scrollbar
- [css/responsive-image-max-height.html](css/responsive-image-max-height.html): here we try to create an image that is never wider than the screen. If the screen is less wide than the image, then the image scales down proportionally. Otherwise, the image has a user determined fixed by the CSS or the HTML `height` property. Related:
  - [https://stackoverflow.com/questions/13632985/limit-the-height-of-a-responsive-image-with-css](https://stackoverflow.com/questions/13632985/limit-the-height-of-a-responsive-image-with-css)
  - [https://stackoverflow.com/questions/50193946/responsive-image-with-max-height-max-width/50194061](https://stackoverflow.com/questions/50193946/responsive-image-with-max-height-max-width/50194061)

  TODO I'm unable to do this....... [https://stackoverflow.com/questions/69964332/how-to-set-the-default-height-of-responsive-images-when-screen-is-wide-and-have](https://stackoverflow.com/questions/69964332/how-to-set-the-default-height-of-responsive-images-when-screen-is-wide-and-have) The objective was to implement: [https://github.com/ourbigbook/ourbigbook/issues/168](https://github.com/ourbigbook/ourbigbook/issues/168)
- [css/top-navigation.html](css/top-navigation.html)

### CSS flex

↑ **Parent:** [Cascading Style Sheets](#cascading-style-sheets)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CSS_Flexible_Box_Layout)

- [css/flex.html](css/flex.html): illustrates basic flex usage, including:
- `flex-grow`: if there's space left, this determines how much extra space will be given to each.
- `flex-basis`: the size the items want to be. But if there isnt' enough space, this can be cut up.

  Note that the minimal space required by children of the flex children cannot be necessarily cut up, and might lead things to overflow out of the container.
- `flex-shrink`: if there's space missing, this determines how much extra space will be removed from each `flex-basis`

Other examples include:
- [css/flex-fill-vertical.html](css/flex-fill-vertical.html): minimal setup for a editor: [https://docs.ourbigbook.com/editor](https://docs.ourbigbook.com/editor)

That example calculates and displays the final widths via [JavaScript](programming-language.md#javascript), making it easier to understand the calculations being done.

Answers: [https://stackoverflow.com/questions/28473807/how-does-flex-grow0-get-interpreted/69995712#69995712](https://stackoverflow.com/questions/28473807/how-does-flex-grow0-get-interpreted/69995712#69995712)

Bibliography:
- [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)

### Sass (stylesheet language)

↑ **Parent:** [Cascading Style Sheets](#cascading-style-sheets)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))

The more of their syntax gets merged into mainline [Cascading Style Sheets](#cascading-style-sheets), the better the world will be.

## JavaScript browser example

↑ **Parent:** [Web technology](web-technology.md)  
🏷️ **Tags:** [JavaScript](programming-language.md#javascript)

- [js/confirm-close.html](js/confirm-close.html): [https://stackoverflow.com/questions/7317273/warn-user-before-leaving-web-page-with-unsaved-changes](https://stackoverflow.com/questions/7317273/warn-user-before-leaving-web-page-with-unsaved-changes)
- [web-cheat/js-image-load.html](web-cheat/js-image-load.html): load an image from JavaScript dynamically: [https://stackoverflow.com/questions/226847/what-is-the-best-javascript-code-to-create-an-img-element](https://stackoverflow.com/questions/226847/what-is-the-best-javascript-code-to-create-an-img-element)
- [web-cheat/js-image-load-viewport.html](web-cheat/js-image-load-viewport.html): load an image from JavaScript dynamically when it would become visible on the viewport: [https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-only-when-they-are-in-the-viewport](https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-only-when-they-are-in-the-viewport)
- [html/img-load-lazy.html](html/img-load-lazy.html): [https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-lazily-only-when-they-are-in-the-viewport/57389607#57389607](https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-lazily-only-when-they-are-in-the-viewport/57389607#57389607)
- [web-cheat/esm.html](web-cheat/esm.html): ESM modules
  - [web-cheat/esm1.js](web-cheat/esm1.js)
  - [web-cheat/esm2.js](web-cheat/esm2.js)
- [js/keydown.html](js/keydown.html): [https://stackoverflow.com/questions/16006583/capturing-ctrlz-key-combination-in-javascript](https://stackoverflow.com/questions/16006583/capturing-ctrlz-key-combination-in-javascript)

External libraries
- Text editors
  - [web-cheat/monaco-editor.html](web-cheat/monaco-editor.html):
    - [https://github.com/microsoft/monaco-editor](https://github.com/microsoft/monaco-editor)
    - [https://stackoverflow.com/questions/63179813/how-to-run-the-monaco-editor-from-a-cdn-like-cdnjs/63179814#63179814](https://stackoverflow.com/questions/63179813/how-to-run-the-monaco-editor-from-a-cdn-like-cdnjs/63179814#63179814)
- Interactive HTML table sorting
  - [web-cheat/tablesort.html](web-cheat/tablesort.html): [https://github.com/tristen/tablesort](https://github.com/tristen/tablesort)
  - [web-cheat/sortable.html](web-cheat/sortable.html): [https://github.com/HubSpot/sortable](https://github.com/HubSpot/sortable)

## Website stack

↑ **Parent:** [Web technology](web-technology.md)

## Asset bundler

↑ **Parent:** [Web technology](web-technology.md)

In order to make websites efficient and portable, a lot of [transpilation](software.md#source-to-source-compiler) is needed.

### webpack

↑ **Parent:** [Asset bundler](#asset-bundler)

[This section is present in another page, follow this link to view it.](webpack.md)

## Push technology

↑ **Parent:** [Web technology](web-technology.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Push_technology)

## Web browser

↑ **Parent:** [Web technology](web-technology.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Web_browser)

### Chromium (web browser)

↑ **Parent:** [Web browser](#web-browser)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chromium_(web_browser))

[Google](google.md) is trying to kill it as of 2021: [https://www.omgubuntu.co.uk/2021/01/chromium-sync-google-api-removed](https://www.omgubuntu.co.uk/2021/01/chromium-sync-google-api-removed) The lack of sync is a major major blow. So selfish. Google makes billions, and it won't give in a little bit of settings storage...

#### Chromium bug

↑ **Parent:** [Chromium (web browser)](#chromium-web-browser)

##### Chromium sometimes freezes due to autofill on omnibox 

↑ **Parent:** [Chromium bug](#chromium-bug)

This has happened a few times a day on [Ubuntu 24.10](systems-programming.md#ubuntu-24-10) and [Chromium](chemistry.md#chromium) 133. It has also been happening in previous versions of Ubuntu and Chromium.

As [Ciro Santilli](ciro-santilli.md) starts typing on the omnibox, sometimes the window freezes and the dreaded "is not responding" window shows up.

The only somewhat similar reports that [Ciro Santilli](ciro-santilli.md) could find as of 2025:
- [https://askubuntu.com/questions/474270/typing-freezes-in-chromium-omnibox-and-enigmatic-letter-a-in-bar-since-ubuntu](https://askubuntu.com/questions/474270/typing-freezes-in-chromium-omnibox-and-enigmatic-letter-a-in-bar-since-ubuntu)
- [https://superuser.com/questions/454737/debugging-freeze-in-chromium](https://superuser.com/questions/454737/debugging-freeze-in-chromium)
- [https://unix.stackexchange.com/questions/51905/typing-in-chromiums-chromes-omnibox-crashes-browser](https://unix.stackexchange.com/questions/51905/typing-in-chromiums-chromes-omnibox-crashes-browser)

Opened one at: [https://askubuntu.com/questions/1544448/chome-chromium-ui-sometimes-freezes-for-several-seconds-when-i-start-typing-on-t](https://askubuntu.com/questions/1544448/chome-chromium-ui-sometimes-freezes-for-several-seconds-when-i-start-typing-on-t)

#### Electron (software framework)

↑ **Parent:** [Chromium (web browser)](#chromium-web-browser)

##### Software that uses Electron

↑ **Parent:** [Electron (software framework)](#electron-software-framework)

#### Disable JavaScript on Chromium

↑ **Parent:** [Chromium (web browser)](#chromium-web-browser)

[https://stackoverflow.com/questions/13405383/how-to-disable-javascript-in-chrome-developer-tools](https://stackoverflow.com/questions/13405383/how-to-disable-javascript-in-chrome-developer-tools)

### Firefox

↑ **Parent:** [Web browser](#web-browser)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Firefox)

### Google Chrome

↑ **Parent:** [Web browser](#web-browser)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Google_Chrome)

#### Chrome Android extension

↑ **Parent:** [Google Chrome](#google-chrome)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chrome_Android_extension)

Lol it is note possible what a joke. Notably this makes it harder to have of a superior third party [password manager](software.md#password-manager)  like [Proton Pass](messaging-software.md#proton-pass) (though there seems to be an autocomplete app as an alternative path), and an [ad blocker](social-technology.md#ad-blocking). Fuck [Google](google.md).

Also, [Chromium](chemistry.md#chromium) is not available on [Google Play](https://ourbigbook.com/go/topic/google-play) by default, you can install the [apk](https://ourbigbook.com/go/topic/apk), but you will miss updates:
- [https://www.quora.com/Is-it-possible-to-install-Chromium-on-my-Android-11-smartphone-If-not-why](https://www.quora.com/Is-it-possible-to-install-Chromium-on-my-Android-11-smartphone-If-not-why)

## Web development

↑ **Parent:** [Web technology](web-technology.md)

## Web framework

↑ **Parent:** [Web technology](web-technology.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Web_framework)

By [programming language](programming-language.md):
- [Node.js web frameworks](node-js.md#node-js-web-framework)
- [Python web frameworks](programming-language.md#python-web-framework)

How to select one:
- [https://insights.stackoverflow.com/trends?tags=django%2Cruby-on-rails%2Cexpress%2Csails.js%2Cflask%2Cnestjs](https://insights.stackoverflow.com/trends?tags=django%2Cruby-on-rails%2Cexpress%2Csails.js%2Cflask%2Cnestjs)
- [gothinkster/realworld](#gothinkster-realworld)

### Hello world website

↑ **Parent:** [Web framework](#web-framework)

#### A blog in every web framework

↑ **Parent:** [Hello world website](#hello-world-website)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/A_blog_in_every_web_framework)

A (multi-user) [blog](website.md#blog) is the [hello world](software.md#hello-world-program) of the web, so creating one of those is the best way to quickly evaluate web technology, i.e. [time to Hello World](software.md#time-to-hello-world).

Some new frameworks like [FeathersJS](node-js.md#feathersjs) are making a chat app instead, as that highlights the push notifications a bit better.

<h5 id="gothinkster-realworld">gothinkster/realworld</h5>

↑ **Parent:** [A blog in every web framework](#a-blog-in-every-web-framework)

[https://github.com/gothinkster/realworld](https://github.com/gothinkster/realworld)

[Ciro Santilli](ciro-santilli.md)'s implementation: [node Express Sequelize Next.js realworld example app](react.md#node-express-sequelize-next-js-realworld-example-app).

Ahh, you [can't have new ideas anymore](#a-blog-in-every-web-framework)!

Basically puts together every backend with [Front-end web framework](#front-end-web-framework) to create the exact same website.

The reference live demo can be found at: [https://demo.realworld.io/#/](https://demo.realworld.io/#/) It is based on [Angular.js](#angular-js) as it links to: [https://github.com/gothinkster/angularjs-realworld-example-app](https://github.com/gothinkster/angularjs-realworld-example-app) TODO backend?

There are however also live demos of other frontends, e.g.:
- [React](react.md): [https://react-redux.realworld.io](https://react-redux.realworld.io). But note that tag addition at post creation is broken there as of March 2021, but not on master: [https://github.com/gothinkster/react-redux-realworld-example-app/issues/151#issuecomment-808417846](https://github.com/gothinkster/react-redux-realworld-example-app/issues/151#issuecomment-808417846) so they forgot to update the live [server](computer.md#server-computing).
- [Vue.js](#vue-js): [https://vue-vuex-realworld.netlify.app](https://vue-vuex-realworld.netlify.app)
Note that all those frontends communicate with the same backend.

As of 2021 Devs are seemed a bit too focused on monetizing the project through their "how to use this project" premium tutorial, and documentation could be better: just getting the [hello world](software.md#hello-world-program) of the most popular backend with the most popular frontend is not easy... come on.

[https://github.com/gothinkster/realworld/issues/578](https://github.com/gothinkster/realworld/issues/578) asks for community support, as devs have moved on since unfortunately.

Remember:
- by default, the frontends hardcode the upstream public data [API](software.md#application-programming-interface): `https://conduit.productionready.io/api` so you have to hack their code to match the port of the backend. And each backend can have a different port.
- when you switch between backends, you must first manually [clear client-side storage](programming-language.md#clear-client-side-storage) cookies/local new run will fail due to authentication issues!

Important missing things from the minimum base app:
- [server-side rendering](#server-side-rendering):
  - [https://github.com/arrlancore/nextjs-ssr-real-world-app-example](https://github.com/arrlancore/nextjs-ssr-real-world-app-example). As advertised, that global instance does render with [JavaScript](programming-language.md#javascript) disabled! Proposed for upstream at: [https://github.com/gothinkster/realworld/issues/423](https://github.com/gothinkster/realworld/issues/423)
  - [https://github.com/gothinkster/realworld/issues/266](https://github.com/gothinkster/realworld/issues/266)
- no [javaScript bi-directional communication library](programming-language.md#javascript-bi-directional-communication-library) built-in... come on: [https://github.com/gothinkster/realworld/issues/107](https://github.com/gothinkster/realworld/issues/107)
- [email](messaging-software.md#email) notifications however as tested on the live demo: [https://demo.realworld.io/#/](https://demo.realworld.io/#/)
- error handling is broken/missing/inconsistent across apps

First you should the most popular backend/frontend combination running, which is the most likely to be working. We managed to run on [Ubuntu](systems-programming.md#ubuntu) 20.10, [React](react.md) + [Node.js](node-js.md) [Express.js](node-js.md#express-js) as described at [https://github.com/gothinkster/node-express-realworld-example-app/pull/116](https://github.com/gothinkster/node-express-realworld-example-app/pull/116):
- [https://github.com/cirosantilli/node-express-realworld-example-app/tree/mongo4](https://github.com/cirosantilli/node-express-realworld-example-app/tree/mongo4) which has a simple patch on top of [https://github.com/gothinkster/node-express-realworld-example-app/tree/ba04b70c31af81ca7935096740a6e083563b3a4a](https://github.com/gothinkster/node-express-realworld-example-app/tree/ba04b70c31af81ca7935096740a6e083563b3a4a) for MongoDB 4 support

  This requires you to first [install MongoDB on Ubuntu](software.md#install-mongodb-on-ubuntu) and ensure you can login to it from the command line.
- [https://github.com/gothinkster/react-redux-realworld-example-app/tree/9186292054dc37567e707602a15a0884d6bdae35](https://github.com/gothinkster/react-redux-realworld-example-app/tree/9186292054dc37567e707602a15a0884d6bdae35) patched to use the correct server host/port `localhost:3000`:
  ```
  diff --git a/src/agent.js b/src/agent.js
  index adfbd72..e3cdc7f 100644
  --- a/src/agent.js
  +++ b/src/agent.js
  @@ -3,7 +3,7 @@ import _superagent from 'superagent';

   const superagent = superagentPromise(_superagent, global.Promise);

  -const API_ROOT = 'https://conduit.productionready.io/api';
  +const API_ROOT = 'http://localhost:3030/api';

   const encode = encodeURIComponent;
   const responseBody = res => res.body;
  ```
Then just:
```
npm install
npm start
```
on both [server](computer.md#server-computing) and [client](computer.md#client-computing), and then visit the client URL: [http://localhost:4100/](http://localhost:4100/)

You have to hit the Enter key to add tags, it's terrible: [https://github.com/gothinkster/react-redux-realworld-example-app/issues/151#issuecomment-808417846](https://github.com/gothinkster/react-redux-realworld-example-app/issues/151#issuecomment-808417846)

One cool thing is that the main repo has unified backend API tests:
```
git clone https://github.com/gothinkster/realworld
cd realworld
git checkout e7adc6b06b459e578d7d4a6738c1c050598ba431
cd api
APIURL=http://localhost:3000/api USERNAME="u$(date +%s)" ./run-api-tests.sh
```
so the per-repository tests are basically useless, and that single test can test everything for any backend! There is no frontend testing however: [https://github.com/gothinkster/realworld/issues/269](https://github.com/gothinkster/realworld/issues/269) so newb.

<h6 id="gothinkster-realworld-implementation">gothinkster/realworld implementation</h6>

↑ **Parent:** [Gothinkster/realworld](#gothinkster-realworld)

Setups we've tried:
- backend:
  - [randyscotsmithey/feathers-realworld-example-app](node-js.md#randyscotsmithey-feathers-realworld-example-app) worked with [React](react.md) and [Vue.js](#vue-js)
  - the [React](react.md) setup failed as shown at: [https://github.com/gothinkster/react-redux-realworld-example-app/issues/187](https://github.com/gothinkster/react-redux-realworld-example-app/issues/187)
  - [gothinkster/django-realworld-example-app](programming-language.md#gothinkster-django-realworld-example-app)
  - the [Nest.js](node-js.md#nest-js) failed on Ubuntu 20.10 as per [https://github.com/lujakob/nestjs-realworld-example-app/issues/19](https://github.com/lujakob/nestjs-realworld-example-app/issues/19)
- frontend:

#### TodoMVC

↑ **Parent:** [Hello world website](#hello-world-website)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/TodoMVC)

[https://todomvc.com/](https://todomvc.com/)

[Front-end](#front-end-web-framework) only, so infinitely simpler, and generally much less useful than [gothinkster/realworld](#gothinkster-realworld).

### Front-end web framework

↑ **Parent:** [Web framework](#web-framework)

You need those because it is hard to do the following:
- client [JavaScript](programming-language.md#javascript) sends a request to [server](computer.md#server-computing)
- server sends back data
- client updates what the user sees

This is hard to do notably because when the update happens, several things might need to change on the webpage at the same time.

Notably, new elements might need to be added to the webpage, which in turn means that new bindings such as button clicks have to be added to those, in a way that keeps the page working.

The only way to do this basically is to have a functional dependency graph that keeps everything in the page in working state as updates come.

#### Single page application

↑ **Parent:** [Front-end web framework](#front-end-web-framework)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Single_page_application)

##### Isomorphic JavaScript

↑ **Parent:** [Single page application](#single-page-application)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Isomorphic_JavaScript)

###### Server-side rendering

↑ **Parent:** [Isomorphic JavaScript](#isomorphic-javascript)

#### List of front-end web frameworks

↑ **Parent:** [Front-end web framework](#front-end-web-framework)

<h5 id="angular-js">Angular.js</h5>

↑ **Parent:** [List of front-end web frameworks](#list-of-front-end-web-frameworks)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Angular.js)

[React.js](react.md)

##### React

↑ **Parent:** [List of front-end web frameworks](#list-of-front-end-web-frameworks)

[This section is present in another page, follow this link to view it.](react.md)

<h5 id="vue-js">Vue.js</h5>

↑ **Parent:** [List of front-end web frameworks](#list-of-front-end-web-frameworks)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Vue.js)

<h6 id="nuxt-js">Nuxt.js</h6>

↑ **Parent:** [Vue.js](#vue-js)

## 🏷️ Tagged (1)

- [JavaScript](programming-language.md#javascript)

## ↑ Ancestors (6)

1. [Software](software.md)
2. [Computer](computer.md)
3. [Information technology](technology.md#information-technology)
4. [Area of technology](technology.md#area-of-technology)
5. [Technology](technology.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (2)

- [The best articles by Ciro Santilli](articles.md)
- [Programming languages](skills.md#programming-languages)
