# Programming language

↑ **Parent:** [Software](software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Programming_language)

A language that allows you to talk to and command a [computer](computer.md).

There is only space for two languages at most in the world: the [compiled](#compiled-programming-language) one, and the [interpreted](#interpreted-programming-language) one.

For 2020 now, when you have a choice, you must go for:
- [Python](#python-programming-language) as the interpreted one
- [C++](#c-plus-plus) for compiled

Those two are languages not by any means perfect from a language design point of view, and there are likely already better alternatives, they are only chosen due to a pragmatic tradeoff between ecosystem and familiarity.

Ciro predicts that Python will become like [Fortran](#fortran) in the future: a legacy hated by most who have moved to [JavaScript](#javascript) long ago (which is slightly inferior, but too similar, and with too much web dominance to be replaced), but with too much dominance in certain applications like machine learning to be worth replacing, like Fortran dominates certain HPC applications. We'll see. Maybe non performance critical scripting languages are easier to replace.

[C++](#c-plus-plus) however is decent, and is evolving in very good directions in the 2010's, and will remain relevant in the foreseeable future.

[Bash](#bash-unix-shell) can also be used when you're lazy. But if the project goes on, you will sooner or later regret that choice.

The language syntax in itself does not matter. All that matters is how many useful libraries and tooling it has.

This is how other languages compare:
- [C](#c-programming-language): but cannot make a large codebase [DRY](software.md#yet-another) without insanity
- [Ruby](#ruby-programming-language): the exact same as Python, and only strong in one domain: [web development](web-technology.md#web-development), while Python rules everything else, and is not bad on web either. So just kill Ruby, please.
- [JavaScript](#javascript): it is totally fine if [Node.js](node-js.md) destroys [Python](#python-programming-language) and becomes the ONE scripting language to rule them all since Python and JavaScript are almost equally crappy (although JavaScript is a bit more of course).

  One thing must be said tough: `someobject.not_defined_property` silently returning `undefined` rather than blowing up is [bullshit](molecular-biology.md#bullshit).
- [Go](#go-programming-language): likely a good replacement for [Python](#python-programming-language). If the ecosystem gets there, will gladly use it more.
- [Java](#java-programming-language): good language, but has an ugly enterprisey ecosystem, Oracle has made/kept the development process too closed, and [API patenting madness on Android just kills if off completely](https://en.wikipedia.org/wiki/Google_v._Oracle_America)
- [Haskell](#haskell): many have tried to learn some functional stuff, but too hard. Sounds really cool though.
- Rust: sounds cool, you will gladly replace C and C++ with it if the ecosystem ramps up.
- [C](linguistics.md#c): [Microsoft](microsoft.md) is [evil](cirism.md#evil)
- [Tcl](#tcl), [Perl](#perl-programming-language): Python killed them way back and is less insane
- [R](#r-programming-language), GNU Octave and any other "[numerical computing language](mathematics.md#numerical-computing-language)": all of this is a waste of society's time as explained at: [Section "Numerical computing language"](mathematics.md#numerical-computing-language)
- Swift: Ciro would rather stay away from [Apple](apple-inc.md) dominated projects if possible since they sell a [closed source](software.md#closed-source-software) [operating system](systems-programming.md#operating-system)

**Table of contents**

- [Type of programming language](#type-of-programming-language)
  - [Type system](#type-system)
  - [Programming language feature](#programming-language-feature)
    - [Inline assembly](#inline-assembly)
  - [Programming paradigm](#programming-paradigm)
    - [Imperative programming](#imperative-programming)
    - [Functional programming](#functional-programming)
      - [Unnecessary state is the source of much evil](#unnecessary-state-is-the-source-of-much-evil)
      - [Functional programming is a subset of imperative programming](#functional-programming-is-a-subset-of-imperative-programming)
  - [Compiled and interpreted programming language](#compiled-and-interpreted-programming-language)
    - [Compiled programming language](#compiled-programming-language)
    - [Interpreted programming language](#interpreted-programming-language)
  - [Programming languages without a decent dominating package system](#programming-languages-without-a-decent-dominating-package-system)
- [Programming language construct](#programming-language-construct)
  - [for loop](#for-loop)
  - [while loop](#while-loop)
- [List of programming languages](#list-of-programming-languages)
  - [Adobe Flash](#adobe-flash)
  - [awk](#awk)
  - [Bash (Unix shell)](#bash-unix-shell)
    - [Bash HOWTO](#bash-howto)
  - [C (programming language)](#c-programming-language)
    - [C example](#c-example)
    - [ANSI C](#ansi-c)
    - [C library](#c-library)
      - [C standard library](#c-standard-library)
      - [C POSIX library](#c-posix-library)
  - [C++](#c-plus-plus)
    - [C++ library](#c-plus-plus-library)
    - [C++ standard library](#c-plus-plus-standard-library)
      - [C++ format](#c-plus-plus-format)
        - [C++ format print containers](#c-plus-plus-format-print-containers)
  - [C\#](#c-sharp)
  - [Fortran](#fortran)
  - [Go (programming language)](#go-programming-language)
  - [Haskell](#haskell)
  - [Java (programming language)](#java-programming-language)
    - [`JAVA_HOME`](#java-home)
    - [Java library](#java-library)
    - [JAR (file format)](#jar-file-format)
    - [Google LLC v. Oracle America, Inc.](#google-llc-v-oracle-america-inc)
    - [Java program](#java-program)
  - [JavaScript](#javascript)
    - [Client-side storage](#client-side-storage)
      - [Clear client-side storage](#clear-client-side-storage)
        - [Clear client-side storage on Chromium](#clear-client-side-storage-on-chromium)
    - [Emscripten](#emscripten)
    - [JavaScript software](#javascript-software)
      - [JavaScript library](#javascript-library)
        - [Babel (transcompiler)](#babel-transcompiler)
        - [JavaScript game engine](#javascript-game-engine)
          - [Phaser.js](#phaser-js)
            - [Phaser hello world](#phaser-hello-world)
            - [Bundle assets into a single file in Phaser](#bundle-assets-into-a-single-file-in-phaser)
        - [JavaScript physics engine](#javascript-physics-engine)
          - [Matter.js](#matter-js)
            - [js/matterjs/hello.html](#_file/js/matterjs/hello.html)
            - [js/matterjs/examples.html](#_file/js/matterjs/examples.html)
        - [JavaScript bi-directional communication library](#javascript-bi-directional-communication-library)
        - [Socket.IO](#socket-io)
    - [JavaScript tooling](#javascript-tooling)
      - [JavaScript linter](#javascript-linter)
        - [ESLint](#eslint)
    - [JavaScript language](#javascript-language)
      - [JavaScript is single threaded](#javascript-is-single-threaded)
      - [`async` (JavaScript)](#async-javascript)
        - [How to convert `async` to sync in JavaScript](#how-to-convert-async-to-sync-in-javascript)
    - [Node.js](node-js.md)
      - [Node.js example](node-js.md#node-js-example)
        - [nodejs/count.js](node-js.md#_file/nodejs/count.js)
        - [nodejs/read\_child\_process\_lines.js](node-js.md#_file/nodejs/read_child_process_lines.js)
        - [JavaScript memory usage benchmark](node-js.md#javascript-memory-usage-benchmark)
      - [npm](node-js.md#npm)
        - [package.json](node-js.md#package-json)
      - [Node.js library](node-js.md#node-js-library)
        - [Node.js standard library](node-js.md#node-js-standard-library)
          - [Node.js `worker_threads`](node-js.md#node-js-worker-threads)
        - [Node.js database bindings](node-js.md#node-js-database-bindings)
        - [Node.js ORM library](node-js.md#node-js-orm-library)
          - [Sequelize](sequelize.md)
            - [The horrors of Sequelize](sequelize.md#the-horrors-of-sequelize)
            - [Sequelize example](sequelize.md#sequelize-example)
              - [Sequelize raw query](sequelize.md#sequelize-raw-query)
              - [UPDATE with JOIN in Sequelize](sequelize.md#update-with-join-in-sequelize)
              - [Sequelize parallel example](sequelize.md#sequelize-parallel-example)
                - [nodejs/sequelize/parallel\_select\_and\_update.js](sequelize.md#_file/nodejs/sequelize/parallel_select_and_update.js)
            - [Sequelize transaction retry](sequelize.md#sequelize-transaction-retry)
            - [SQL TRIGGER in Sequelize](sequelize.md#sql-trigger-in-sequelize)
      - [Node.js web framework](node-js.md#node-js-web-framework)
        - [Express.js](node-js.md#express-js)
          - [Realworld app written in Express](node-js.md#realworld-app-written-in-express)
            - [gothinkster/node-express-realworld-example-app](node-js.md#gothinkster-node-express-realworld-example-app)
            - [sigoden/node-express-realworld-example-app](node-js.md#sigoden-node-express-realworld-example-app)
            - [Varun-Hegde/Conduit\_NodeJS](node-js.md#varun-hegde-conduit-nodejs)
        - [FeathersJS](node-js.md#feathersjs)
          - [FeatherJS demo apps](node-js.md#featherjs-demo-apps)
            - [feathersjs/feathers-chat](node-js.md#feathersjs-feathers-chat)
              - [feathers-chat PostgreSQL](node-js.md#feathers-chat-postgresql)
              - [feathers-chat-react](node-js.md#feathers-chat-react)
            - [Codaisseur/feathersjs-react-redux-ssr](node-js.md#codaisseur-feathersjs-react-redux-ssr)
            - [randyscotsmithey/feathers-realworld-example-app](node-js.md#randyscotsmithey-feathers-realworld-example-app)
          - [FeathersJS Heroku deployment](node-js.md#feathersjs-heroku-deployment)
          - [FeathersJS signup email verification](node-js.md#feathersjs-signup-email-verification)
        - [Meteor (web framework)](node-js.md#meteor-web-framework)
        - [Nest.js](node-js.md#nest-js)
          - [lujakob/nestjs-realworld-example-app](node-js.md#lujakob-nestjs-realworld-example-app)
            - [lujakob/nestjs-realworld-example-app SQLite port](node-js.md#lujakob-nestjs-realworld-example-app-sqlite-port)
        - [Sails.js](node-js.md#sails-js)
      - [NVM](node-js.md#nvm)
    - [TypeScript](typescript.md)
    - [Universal Module Definition](#universal-module-definition)
  - [Perl (programming language)](#perl-programming-language)
    - [Perl HOWTO](#perl-howto)
      - [Print only the matching group in Perl](#print-only-the-matching-group-in-perl)
  - [PHP](#php)
  - [Pseudocode](#pseudocode)
  - [Python (programming language)](#python-programming-language)
    - [Python language feature](#python-language-feature)
      - [Python classes](#python-classes)
        - [Python special method](#python-special-method)
          - [Python `__getitem__`](#python-getitem)
            - [python/getitem.py](#_file/python/getitem.py)
            - [python/getitem\_complex.py](#_file/python/getitem_complex.py)
    - [Python standard library](#python-standard-library)
      - [Python `abc`](#python-abc)
        - [python/abc\_cheat.py](#_file/python/abc_cheat.py)
      - [Python `ast`](#python-ast)
        - [python/ast\_cheat.py](#_file/python/ast_cheat.py)
      - [Python `dataclass`](#python-dataclass)
        - [python/infer.py](#python-infer-py)
        - [python/dataclass\_cheat.py](#python-dataclass-cheat-py)
        - [python/dataclass\_hash.py](#python-dataclass-hash-py)
      - [Python `tkinter`](#python-tkinter)
        - [Python `tkinter` image editor](#python-tkinter-image-editor)
          - [Python `tkinter` image editor with image recognition](#python-tkinter-image-editor-with-image-recognition)
      - [Python `typing`](#python-typing)
        - [python/typing\_cheat/hello.py](#_file/python/typing_cheat/hello.py)
        - [python/typing\_cheat/infer.py](#_file/python/typing_cheat/infer.py)
        - [python/typing\_cheat/union.py](#_file/python/typing_cheat/union.py)
        - [Python `Protocol`](#python-protocol)
          - [python/typing\_cheat/protocol.py](#_file/python/typing_cheat/protocol.py)
          - [python/typing\_cheat/protocol\_empty.py](#_file/python/typing_cheat/protocol_empty.py)
    - [Zen of Python](#zen-of-python)
    - [Python version](#python-version)
      - [Python 3.12](#python-3-12)
    - [Python implementation](#python-implementation)
      - [CPython](#cpython)
        - [CPython feature](#cpython-feature)
        - [Global Interpreter Lock](#global-interpreter-lock)
        - [CPython JIT](#cpython-jit)
        - [CPython version](#cpython-version)
          - [CPython 3.13](#cpython-3-13)
      - [Cython](#cython)
      - [Jython](#jython)
      - [Numba](#numba)
      - [PyPy](#pypy)
    - [Python package manager](#python-package-manager)
      - [pip (package manager)](#pip-package-manager)
      - [Conda](#conda)
        - [Install Conda on Ubuntu](#install-conda-on-ubuntu)
      - [Poetry (Python package manager)](#poetry-python-package-manager)
    - [Python Package Index](#python-package-index)
    - [Python virtualization](#python-virtualization)
      - [Python version virtualization](#python-version-virtualization)
        - [pyenv](#pyenv)
      - [virtualenv](#virtualenv)
    - [Python documentation generator](#python-documentation-generator)
      - [Sphinx (documentation generator)](#sphinx-documentation-generator)
        - [python/sphinx](#_file/python/sphinx)
        - [python/sphinx/hello](#_file/python/sphinx/hello)
        - [python/sphinx/union](#_file/python/sphinx/union)
        - [python/sphinx/class](#_file/python/sphinx/class)
        - [python/sphinx/virtual\_method](#_file/python/sphinx/virtual_method)
    - [Python library](#python-library)
      - [Python scientific library](#python-scientific-library)
        - [Jupyter Notebook](#jupyter-notebook)
          - [python/jupyter/hello.ipynb](#_file/python/jupyter/hello.ipynb)
        - [NumPy](#numpy)
          - [numpy.fft](#numpy-fft)
            - [numpy/fft\_plot.py](#_file/numpy/fft_plot.py)
            - [numpy/fft.py](#_file/numpy/fft.py)
        - [SageMath](#sagemath)
        - [Scikit-learn](#scikit-learn)
      - [Python web framework](#python-web-framework)
        - [Django (web-framework)](#django-web-framework)
          - [gothinkster/django-realworld-example-app](#gothinkster-django-realworld-example-app)
  - [R (programming language)](#r-programming-language)
  - [Ruby (programming language)](#ruby-programming-language)
    - [Ruby on Rails](#ruby-on-rails)
      - [Ruby on Rails React integration](#ruby-on-rails-react-integration)
        - [shakacode/react\_on\_rails](#shakacode-react-on-rails)
  - [Rust (programming language)](#rust-programming-language)
    - [Rust library](#rust-library)
  - [Short Code (programming-language)](#short-code-programming-language)
  - [Tcl](#tcl)

## Type of programming language

↑ **Parent:** [Programming language](programming-language.md)

### Type system

↑ **Parent:** [Type of programming language](#type-of-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Type_system)

### Programming language feature

↑ **Parent:** [Type of programming language](#type-of-programming-language)

#### Inline assembly

↑ **Parent:** [Programming language feature](#programming-language-feature)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Inline_assembler)

### Programming paradigm

↑ **Parent:** [Type of programming language](#type-of-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Programming_paradigm)

#### Imperative programming

↑ **Parent:** [Programming paradigm](#programming-paradigm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Imperative_programming)

#### Functional programming

↑ **Parent:** [Programming paradigm](#programming-paradigm)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Functional_programming)

[Good](cirism.md#good) because [unnecessary state is the source of much evil](#unnecessary-state-is-the-source-of-much-evil).

Even if we cannot do everything in functional, we should at least strive to clearly extract functional substes in what we do.

##### Unnecessary state is the source of much evil

↑ **Parent:** [Functional programming](#functional-programming)  
🏷️ **Tags:** [Ciro Santilli's software engineering wisdom](software.md#ciro-santilli-s-software-engineering-wisdom)

##### Functional programming is a subset of imperative programming

↑ **Parent:** [Functional programming](#functional-programming)

[Ciro Santilli](ciro-santilli.md) thinks [imperative programming](#imperative-programming) is just a superset of [functional programming](#functional-programming) where you can have state.

[C](#c-programming-language) and [C++](#c-plus-plus): OK, you're old before the Internet and compiled, forgiven.

[Python](#python-programming-language): OMG, please, just make it work!!! Your are interpreted!!! You are a hot web technology!!! [Node.js](node-js.md) and [Ruby](#ruby-programming-language) are doing just fine, and Ruby is not newer than you!!! See also: [pip](#pip-package-manager).

### Compiled and interpreted programming language

↑ **Parent:** [Type of programming language](#type-of-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Compiled_and_interpreted_programming_language)

#### Compiled programming language

↑ **Parent:** [Compiled and interpreted programming language](#compiled-and-interpreted-programming-language)

#### Interpreted programming language

↑ **Parent:** [Compiled and interpreted programming language](#compiled-and-interpreted-programming-language)

Interestingly, the very first programming language with an actual implementation was interpreted: [Short Code](#short-code-programming-language) in 1950.

This is not surprising, as interpreters are easier to write than compilers.

And just like modern scripting languages, it reduced execution speed by about 50x.

### Programming languages without a decent dominating package system

↑ **Parent:** [Type of programming language](#type-of-programming-language)  
🏷️ **Tags:** [Evil](cirism.md#evil)

## Programming language construct

↑ **Parent:** [Programming language](programming-language.md)

### for loop

↑ **Parent:** [Programming language construct](#programming-language-construct)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/for_loop)

The [for loop](#for-loop) is a subcase of the [while loop](#while-loop).

One theoretical motivation for its existence is that it has the fundamental property that we are immediately certain it will terminate, unlike [while loops](#while-loop) with arbitrary conditions.

[Primitive recursive functions](computer-science.md#primitive-recursive-function) are the [complexity](computer-science.md#complexity-class) class that divides those two.

### while loop

↑ **Parent:** [Programming language construct](#programming-language-construct)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/while_loop)

## List of programming languages

↑ **Parent:** [Programming language](programming-language.md)

### Adobe Flash

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Adobe_Flash)

### awk

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/awk)

Largest programs ever written:
- [https://www.quora.com/What-is-the-most-complex-software-written-in-Awk](https://www.quora.com/What-is-the-most-complex-software-written-in-Awk)
- [https://github.com/greencardamom/Wikiget/blob/master/wikiget.awk](https://github.com/greencardamom/Wikiget/blob/master/wikiget.awk) is 2690 lines long. Mentioned at: [https://webapps.stackexchange.com/questions/16359/is-there-a-way-to-download-a-list-of-all-wikipedia-categories](https://webapps.stackexchange.com/questions/16359/is-there-a-way-to-download-a-list-of-all-wikipedia-categories)

### Bash (Unix shell)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)

The more heavily a project relies on it, the more you start to regret it.

#### Bash HOWTO

↑ **Parent:** [Bash (Unix shell)](#bash-unix-shell)

### C (programming language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/C++)

It gets the job done, but cannot make a large codebase DRY without insanity.

As of 2020, C is like [Latin](linguistics.md#latin), and we are in the [Middle Ages](science.md#middle-ages), where it has become a [lingua franca](linguistics.md#lingua-franca).

It is interesting to note how late C appeared: 1972, compared e.g. to [Fortran](#fortran) which is from 1957. This is basically because C was a "systems programming language", i.e. with focus on pointer manipulation, and because early computers were so weak, there was no operating system or many software layers in the early days. Fortran however was a numerical language, and it ran directly on bare metal, an application that existed before systems programming.

Examples under [c](c).

#### C example

↑ **Parent:** [C (programming language)](#c-programming-language)

#### ANSI C

↑ **Parent:** [C (programming language)](#c-programming-language)  
🏷️ **Tags:** [Closed standard](software.md#closed-standard)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ANSI_C)

A [closed standard](software.md#closed-standard): [https://stackoverflow.com/questions/81656/where-do-i-find-the-current-c-or-c-standard-documents](https://stackoverflow.com/questions/81656/where-do-i-find-the-current-c-or-c-standard-documents). Nice.

#### C library

↑ **Parent:** [C (programming language)](#c-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/C_library)

##### C standard library

↑ **Parent:** [C library](#c-library)  
🏷️ **Tags:** [ANSI C](#ansi-c)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/C_standard_library)

##### C POSIX library

↑ **Parent:** [C library](#c-library)  
🏷️ **Tags:** [POSIX](systems-programming.md#posix)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/C_POSIX_library)

Quick overview at [https://stackoverflow.com/questions/1780599/what-is-the-meaning-of-posix/31865755#31865755](https://stackoverflow.com/questions/1780599/what-is-the-meaning-of-posix/31865755#31865755)

Exmples under [c/posix](c/posix):
- [c/posix/signal_return.c](c/posix/signal_return.c): [https://stackoverflow.com/questions/37063212/where-does-signal-handler-return-back-to](https://stackoverflow.com/questions/37063212/where-does-signal-handler-return-back-to)
- [c/posix/inet/pton.c](c/posix/inet/pton.c): `inet_pton` demo. Adapted from `man inet_pton` on [Ubuntu 23.04](systems-programming.md#ubuntu-23-04). Usage:
  ```
  ./pton.out 192.187.1.42
  ```

  Output:
  ```
  0xc0bb012a
  ```

  So we see that the strings was converted to an integer, e.g.:
  - 0xc0 = 192
  - 0xbb = 187
  - 0x01 = 1
  - 0x2a = 42

  See also: [https://stackoverflow.com/questions/1680622/ip-address-to-integer-c/76520978#76520978](https://stackoverflow.com/questions/1680622/ip-address-to-integer-c/76520978#76520978)
- [c/posix/inet/ntop.c](c/posix/inet/ntop.c): `inet_ntop` demo. Adapted from `man inet_pton` on [Ubuntu 23.04](systems-programming.md#ubuntu-23-04). Usage:
  ```
  ./ntop.out 0x01021AA0
  ```

  Output:
  ```
  ./ntop.out 0x01021AA0
  ```

<h3 id="c-plus-plus">C++</h3>

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/C++)

C plus plus is what you get when you want to have all of:
- ability to write DRY code, which is e.g. impossible in the [C](#c-programming-language)
- low level control, notably not having [garbage collection](software.md#garbage-collection-computer-science), as possible in the [C](#c-programming-language)
- somewhat backwards compatibility with [C](#c-programming-language)

<h4 id="c-plus-plus-library">C++ library</h4>

↑ **Parent:** [C++](#c-plus-plus)

<h4 id="c-plus-plus-standard-library">C++ standard library</h4>

↑ **Parent:** [C++](#c-plus-plus)

<h5 id="c-plus-plus-format">C++ format</h5>

↑ **Parent:** [C++ standard library](#c-plus-plus-standard-library)

<h6 id="c-plus-plus-format-print-containers">C++ format print containers</h6>

↑ **Parent:** [C++ format](#c-plus-plus-format)

By [Ciro Santilli](ciro-santilli.md):
- [https://stackoverflow.com/questions/1430757/convert-a-vectorint-to-a-string/79637760#79637760](https://stackoverflow.com/questions/1430757/convert-a-vectorint-to-a-string/79637760#79637760)
- [https://stackoverflow.com/questions/14070940/how-can-i-print-out-c-map-values/79637777#79637777](https://stackoverflow.com/questions/14070940/how-can-i-print-out-c-map-values/79637777#79637777)
- [https://stackoverflow.com/questions/2793232/c-print-out-objects-from-set/79637784#79637784](https://stackoverflow.com/questions/2793232/c-print-out-objects-from-set/79637784#79637784)
- [https://stackoverflow.com/questions/61338240/how-to-print-the-content-of-a-nested-stdunordered-map/79637792#79637792](https://stackoverflow.com/questions/61338240/how-to-print-the-content-of-a-nested-stdunordered-map/79637792#79637792)
By others:
- [https://stackoverflow.com/questions/10750057/how-do-i-print-out-the-contents-of-a-vector/55270925#55270925](https://stackoverflow.com/questions/10750057/how-do-i-print-out-the-contents-of-a-vector/55270925#55270925)
- [https://stackoverflow.com/questions/3496982/how-can-i-print-a-list-of-elements-separated-by-commas/75762963#75762963](https://stackoverflow.com/questions/3496982/how-can-i-print-a-list-of-elements-separated-by-commas/75762963#75762963)

<h3 id="c-sharp">C#</h3>

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/C_Sharp_(programming_language))

### Fortran

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fortran)

### Go (programming language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Go_(programming_language))

Likely a good replacement for [Python](#python-programming-language). If the ecosystem gets there, [Ciro Santilli](ciro-santilli.md) would gladly use it more.

### Haskell

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Haskell)

There are only two pre-requisites to using Haskell in 2020. You have to be an [idealist](science.md#idealist). And you have to be a genius:
- [https://youtu.be/d8nzFqoEOvE?list=PLAJnaovHtaFTK9E1xHnBWZeKtAOhonqH5&t=558](https://youtu.be/d8nzFqoEOvE?list=PLAJnaovHtaFTK9E1xHnBWZeKtAOhonqH5&t=558) [Ben Goertzel](artificial-intelligence.md#ben-goertzel)

<a id="image-xkcd-1312-haskell"></a>
![](https://web.archive.org/web/20230127135616im_/https://imgs.xkcd.com/comics/haskell.png)

**[Figure 1](#image-xkcd-1312-haskell). xkcd 1312: Haskell**. [Source](https://xkcd.com/1312/).

### Java (programming language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Java_(programming_language))

Java is good.

Its boilerplate requirement is a pain, but the design is otherwise very clean.

But its ecosystem sucks.

The development process is rather closed, the issue tracker obscure.

And above all, [Google LLC v. Oracle America, Inc.](#google-llc-v-oracle-america-inc) killed everybody's trust in it once and for all. Thanks [Oracle](software.md#oracle-corporation).

<a id="video-java-for-the-haters-in-100-seconds-by-fireship-2022"></a>
**[Video 1](#video-java-for-the-haters-in-100-seconds-by-fireship-2022). Java for the Haters in 100 Seconds by Fireship (2022)** [Source](https://www.youtube.com/watch?v=m4-HM_sCvtQ).

<h4 id="java-home"><code>JAVA_HOME</code></h4>

↑ **Parent:** [Java (programming language)](#java-programming-language)

This ultimately determines which Java is used by a bunch of tools.

TODO is there a way to update it sanely in [Ubuntu](systems-programming.md#ubuntu): [https://askubuntu.com/questions/175514/how-to-set-java-home-for-java](https://askubuntu.com/questions/175514/how-to-set-java-home-for-java) to always match the default `java` executable?

#### Java library

↑ **Parent:** [Java (programming language)](#java-programming-language)

#### JAR (file format)

↑ **Parent:** [Java (programming language)](#java-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/JAR_(file_format))

#### Google LLC v. Oracle America, Inc.

↑ **Parent:** [Java (programming language)](#java-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Google_LLC_v._Oracle_America,_Inc.)

#### Java program

↑ **Parent:** [Java (programming language)](#java-programming-language)

### JavaScript

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
🏷️ **Tags:** [Web technology](web-technology.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/JavaScript)

The language all browsers converted to as of 2019, and therefore the easiest one to distribute and most widely implemented programming language.

Hopefully will be killed by [WebAssembly](https://en.wikipedia.org/wiki/WebAssembly) one day.

Because JavaScript is a relatively crap/ad-hoc language, it ended up some decent tooling to make up for that, e.g. stuff like linting via ESLint and reformatting through Prettier is much more widespread than in other languages.

JavaScript data structure are also quite a bit anemic, which makes libraries such as lodash incredibly popular. But most of that stuff should be in the stdlib.

Our JavaScript examples can be found at:
- [Node.js example](node-js.md#node-js-example): examples that don't interact with any browser feature. We are just testing those on the CLI which is much more convenient.
- [JavaScript browser example](web-technology.md#javascript-browser-example): examples that interact with browser-specific features, notably the DOM

#### Client-side storage

↑ **Parent:** [JavaScript](#javascript)

[https://www.google.com/search?q=client-side+storage&oq=Client-side+storage&aqs=chrome.0.0l3j0i22i30l4j69i60.88j0j7&client=ubuntu&sourceid=chrome&ie=UTF-8](https://www.google.com/search?q=client-side+storage&oq=Client-side+storage&aqs=chrome.0.0l3j0i22i30l4j69i60.88j0j7&client=ubuntu&sourceid=chrome&ie=UTF-8)

##### Clear client-side storage

↑ **Parent:** [Client-side storage](#client-side-storage)

###### Clear client-side storage on Chromium

↑ **Parent:** [Clear client-side storage](#clear-client-side-storage)

- [https://superuser.com/questions/366483/how-to-delete-cookies-for-a-specific-site](https://superuser.com/questions/366483/how-to-delete-cookies-for-a-specific-site)
- [https://superuser.com/questions/722498/what-is-the-fastest-way-to-clear-cache-and-cookies-in-google-chrome](https://superuser.com/questions/722498/what-is-the-fastest-way-to-clear-cache-and-cookies-in-google-chrome)

#### Emscripten

↑ **Parent:** [JavaScript](#javascript)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Emscripten)

#### JavaScript software

↑ **Parent:** [JavaScript](#javascript)

##### JavaScript library

↑ **Parent:** [JavaScript software](#javascript-software)

###### Babel (transcompiler)

↑ **Parent:** [JavaScript library](#javascript-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Babel_(transcompiler))

###### JavaScript game engine

↑ **Parent:** [JavaScript library](#javascript-library)  
🏷️ **Tags:** [Game engine](software.md#game-engine)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/JavaScript_game_engine)

<h6 id="phaser-js">Phaser.js</h6>

↑ **Parent:** [JavaScript game engine](#javascript-game-engine)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Phaser_(game_framework))

Likely the best [JavaScript](#javascript) [2D](calculus.md#real-plane) game engine as of 2023.
- [https://github.com/photonstorm/phaser](https://github.com/photonstorm/phaser)
- [https://phaser.io/](https://phaser.io/)
- [https://phaser.io/examples/v3.85.0/games](https://phaser.io/examples/v3.85.0/games) contains the demo games
Uses [Matter.js](#matter-js) as a [physics engine](science.md#physics-engine) if enabled. There's also an alternative (in-house?) "arcade" engine: [https://photonstorm.github.io/phaser3-docs/Phaser.Physics.Arcade.ArcadePhysics.html](https://photonstorm.github.io/phaser3-docs/Phaser.Physics.Arcade.ArcadePhysics.html) but it appears to be simpler/less robust (but also possibly faster).

TODO any 2D first person examples a bit like [Ciro's 2D reinforcement learning games](todo.md#ciro-s-2d-reinforcement-learning-games)?

The examples are present under:
```
git clone https://github.com/photonstorm/phaser3-examples
```
but note that that repo is huge, about 4.5 GiB on local disk, as is has tons of assets.

The demos also include a [Monaco](software.md#monaco-editor)-editor based sandbox mode where you can edit code directly on the web and see the game update which is a really sweet addition.

###### Phaser hello world

↑ **Parent:** [Phaser.js](#phaser-js)  
🏷️ **Tags:** [Hello world](software.md#hello-world-program)

- [phaser/hello.html](phaser/hello.html): a minimal hello world adapted from [https://web.archive.org/web/20230323212804/https://phaser.io/tutorials/getting-started-phaser3/part5](https://web.archive.org/web/20230323212804/https://phaser.io/tutorials/getting-started-phaser3/part5). Not an actual game strictly speaking though, just shows the phaser logo bouncing around the screen.

  Fully contained in a single HTML file, except that it loads the phaser library and image assets from the web.
- [phaser/hello-game.html](phaser/hello-game.html): an actually hello world game where you have to collect stars and avoid bombs.

  Based on [https://labs.phaser.io/index.html?dir=games/firstgame/&q=](https://labs.phaser.io/index.html?dir=games/firstgame/&q=):
  - finished version: [https://labs.phaser.io/view.html?src=src/games/firstgame/part10.js](https://labs.phaser.io/view.html?src=src/games/firstgame/part10.js)
  - corresponding tutorial: [https://web.archive.org/web/20230323210501/https://phaser.io/tutorials/making-your-first-phaser-3-game/part10](https://web.archive.org/web/20230323210501/https://phaser.io/tutorials/making-your-first-phaser-3-game/part10).

A web server is mandatory for assets, unless you embed them in data URLs, `file://` access is not possible:
- [https://web.archive.org/web/20230323212818/https://phaser.io/tutorials/getting-started-phaser3](https://web.archive.org/web/20230323212818/https://phaser.io/tutorials/getting-started-phaser3)
- [https://stackoverflow.com/questions/39565296/cors-issue-with-html5-canvas-javascript](https://stackoverflow.com/questions/39565296/cors-issue-with-html5-canvas-javascript)
- [https://stackoverflow.com/questions/59362232/i-cannot-load-images-from-my-pc-in-phaser-3](https://stackoverflow.com/questions/59362232/i-cannot-load-images-from-my-pc-in-phaser-3)
- [https://github.com/photonstorm/phaser/issues/3464](https://github.com/photonstorm/phaser/issues/3464)

###### Bundle assets into a single file in Phaser

↑ **Parent:** [Phaser.js](#phaser-js)

- [https://stackoverflow.com/questions/46576811/is-there-a-way-to-have-phaser-read-assets-from-a-zip-file](https://stackoverflow.com/questions/46576811/is-there-a-way-to-have-phaser-read-assets-from-a-zip-file)
- [https://phaser.discourse.group/t/is-there-a-way-to-have-phaser-read-assets-from-a-zip-file/8521](https://phaser.discourse.group/t/is-there-a-way-to-have-phaser-read-assets-from-a-zip-file/8521)

###### JavaScript physics engine

↑ **Parent:** [JavaScript library](#javascript-library)

<h6 id="matter-js">Matter.js</h6>

↑ **Parent:** [JavaScript physics engine](#javascript-physics-engine)  
🏷️ **Tags:** [2D physics engine](mechanics.md#2d-rigid-body-dynamics-simulator), [JavaScript library](#javascript-library)

To run the demos locally, tested on [Ubuntu 22.10](systems-programming.md#ubuntu-22-10):
```
git clone https://github.com/liabru/matter-js
cd matter-js
git checkout 0.19.0
npm install
npm run dev
```
and this opens up the demos on the browser.

<h6 id="_file/js/matterjs/hello.html">js/matterjs/hello.html</h6>

↑ **Parent:** [Matter.js](#matter-js)

Hello world adapted from: [https://github.com/liabru/matter-js/wiki/Getting-started/1d138998f05766dc4de0e44ae2e35d03121bb7f2](https://github.com/liabru/matter-js/wiki/Getting-started/1d138998f05766dc4de0e44ae2e35d03121bb7f2)

Also asked at: [https://stackoverflow.com/questions/28079138/how-to-make-minimal-example-of-matter-js-work/76203103#76203103](https://stackoverflow.com/questions/28079138/how-to-make-minimal-example-of-matter-js-work/76203103#76203103)

Renderer questions:
- follow object on viewport: [https://codepen.io/csims314/pen/goZQvG](https://codepen.io/csims314/pen/goZQvG)
- draw text: [https://github.com/liabru/matter-js/issues/321](https://github.com/liabru/matter-js/issues/321)

![](https://i.stack.imgur.com/VhFcj.png)

**[Figure 2](#_151)** [Source](https://stackoverflow.com/questions/28079138/how-to-make-minimal-example-of-matter-js-work/76203103\#76203103).

<h6 id="_file/js/matterjs/examples.html">js/matterjs/examples.html</h6>

↑ **Parent:** [Matter.js](#matter-js)

A multi-scenario demo.

###### JavaScript bi-directional communication library

↑ **Parent:** [JavaScript library](#javascript-library)  
🏷️ **Tags:** [Push technology](web-technology.md#push-technology)

- [https://stackoverflow.com/questions/30419455/server-side-data-push-for-web-services](https://stackoverflow.com/questions/30419455/server-side-data-push-for-web-services)
- [https://stackoverflow.com/questions/52146670/bi-directional-communication-between-server-and-client](https://stackoverflow.com/questions/52146670/bi-directional-communication-between-server-and-client)

<h6 id="socket-io">Socket.IO</h6>

↑ **Parent:** [JavaScript library](#javascript-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Socket.IO)

#### JavaScript tooling

↑ **Parent:** [JavaScript](#javascript)

##### JavaScript linter

↑ **Parent:** [JavaScript tooling](#javascript-tooling)

###### ESLint

↑ **Parent:** [JavaScript linter](#javascript-linter)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ESLint)

#### JavaScript language

↑ **Parent:** [JavaScript](#javascript)

##### JavaScript is single threaded

↑ **Parent:** [JavaScript language](#javascript-language)

[Node.js](node-js.md) does have [Node.js `worker_threads`](node-js.md#node-js-worker-threads) however.

##### `async` (JavaScript)

↑ **Parent:** [JavaScript language](#javascript-language)

[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)

`async` is all present in [JavaScript](#javascript) for two reasons:
- you make network requests all the time
- JavaScript is single threaded, so if you are waiting for a network request, the UI freezes, see remarks on the deprecation of synchronous HTTP request at: [https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Synchronous_and_Asynchronous_Requests](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Synchronous_and_Asynchronous_Requests)

However, it is also [Hell](religion.md#hell): [how to convert `async` to sync in JavaScript](#how-to-convert-async-to-sync-in-javascript).

###### How to convert `async` to sync in JavaScript

↑ **Parent:** [`Async` (JavaScript)](#async-javascript)

[God](religion.md#god), it's impossible! You just have to convert the entire fucking call stack all the way up to async functions. It could mean refactoring hundreds of functions.

To be fair, there is a logic to this, if you put yourself within the crappiness of the [JavaScript](#javascript) threading model. And [Python](#python-programming-language) is not that much better with its [Global Interpreter Lock](#global-interpreter-lock).

The problem is that async was introduced relatively late, previously we just had to use infinitely deep callback [trees](mathematics.md#tree-data-structure), which was worse:
```
myAsync().then(ret => myAsync2(ret).then(ret2 => myAsync3(re3)))
```
compared to the new infinitely more readable:
```
ret = await myAsync()
ret2 = await myAsync2(ret)
ret3 = await myAsync3(ret3)
```
But now we are in an endless period of transition between both worlds.

It is also worth mentioning that callbacks are still inescapable if you really want to fan out into a non-linear dependency graph, usually with `Promise.all`:
```
await Promise.all([
  myAsync(1).then(ret => myAsync2(ret)),
  myAsync(2).then(ret => myAsync2(ret)),
])
```

Bibliography:
- [https://stackoverflow.com/questions/21819858/how-to-wrap-async-function-calls-into-a-sync-function-in-node-js-or-javascript](https://stackoverflow.com/questions/21819858/how-to-wrap-async-function-calls-into-a-sync-function-in-node-js-or-javascript)
- [https://stackoverflow.com/questions/9121902/call-an-asynchronous-javascript-function-synchronously](https://stackoverflow.com/questions/9121902/call-an-asynchronous-javascript-function-synchronously)
- [https://stackoverflow.com/questions/47227550/using-await-inside-non-async-function](https://stackoverflow.com/questions/47227550/using-await-inside-non-async-function)
- [https://stackoverflow.com/questions/43832490/is-it-possible-to-use-await-without-async-in-js](https://stackoverflow.com/questions/43832490/is-it-possible-to-use-await-without-async-in-js)
- [https://stackoverflow.com/questions/6921895/synchronous-delay-in-code-execution](https://stackoverflow.com/questions/6921895/synchronous-delay-in-code-execution)

And then, after many many hours of this work, you might notice that the new code is way, way way slower than before, because making small functions `async` has a large performance impact: [https://madelinemiller.dev/blog/javascript-promise-overhead/](https://madelinemiller.dev/blog/javascript-promise-overhead/). Real world case with a 4x slowdown: [https://github.com/ourbigbook/ourbigbook/tree/async-slow](https://github.com/ourbigbook/ourbigbook/tree/async-slow).

Anyways, since you Googled here, you might as well learn the standard pattern to convert callbacks functions into async functions using a promise: [https://stackoverflow.com/questions/4708787/get-password-from-input-using-node-js/71868483#71868483](https://stackoverflow.com/questions/4708787/get-password-from-input-using-node-js/71868483#71868483)

<a id="image-async-function-teletubbies-meme"></a>
<img src="https://web.archive.org/web/20241129001302im_/https://miro.medium.com/v2/resize:fit:828/format:webp/0*-sXUj7txIyw9LX_F" alt="" height="800">

**[Figure 3](#image-async-function-teletubbies-meme). async function Teletubbies meme**. [Source](https://andrewzuo.com/async-await-is-the-worst-thing-to-happen-to-programming-9b8f5150ba74). TODO find original source.

<h4 id="node-js">Node.js</h4>

↑ **Parent:** [JavaScript](#javascript)

[This section is present in another page, follow this link to view it.](node-js.md)

#### TypeScript

↑ **Parent:** [JavaScript](#javascript)

[This section is present in another page, follow this link to view it.](typescript.md)

#### Universal Module Definition

↑ **Parent:** [JavaScript](#javascript)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Universal_Module_Definition)

Since [JavaScript](#javascript) devs are incapable of defining an unified import standard, this design pattern emerged where you just check every magic global one by one. Here's a demo where a Js library works on both the [browser](web-technology.md#web-browser) and from [Node.js](node-js.md):
- [web-cheat/umd_my_lib.js](web-cheat/umd_my_lib.js): the library
- [web-cheat/umd.js](web-cheat/umd.js): [Node.js](node-js.md) user
- [web-cheat/umd.html](web-cheat/umd.html): [browser](web-technology.md#web-browser) user

### Perl (programming language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Perl_(programming_language))

TODO why did [Python](#python-programming-language) kill it? They are very similar and existed at similar times, and possibly Perl was more popular early on.
- [https://www.quora.com/Why-is-Perl-no-longer-a-popular-programming-language](https://www.quora.com/Why-is-Perl-no-longer-a-popular-programming-language) on [Quora](website.md#quora)

Perl likely killed [Tcl](#tcl).

#### Perl HOWTO

↑ **Parent:** [Perl (programming language)](#perl-programming-language)

##### Print only the matching group in Perl

↑ **Parent:** [Perl HOWTO](#perl-howto)

[https://stackoverflow.com/questions/5617314/perl-regex-print-the-matched-value/5617355#5617355](https://stackoverflow.com/questions/5617314/perl-regex-print-the-matched-value/5617355#5617355)
```
perl -lne 'print for /mykey=(\d+)/'
```

### PHP

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PHP)

### Pseudocode

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pseudocode)

### Python (programming language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Python_(programming_language))

Examples under [python](python).

[Ciro Santilli's wife](ciro-santilli.md#ciro-santilli-s-wife) was studying a bit of basic Python for some job interviews, when she noticed:

> Wow, `in` is so powerful! You can do `for x in list`, `for x in dict` and `if x in dict` all with that single word!

Damn right, girl, damn right.

Ciro remembers hearing about [Python](#python-programming-language) online briefly. It seemed like a distant thing from the [Java](#java-programming-language)/[C](#c-programming-language) dominated (and outdated) university courses. Then some teaching assistant mentioned during some course when Ciro was at [École Polytechnique](ecole-polytechnique.md) that Python was a great integration tool. That sounded cool.

Then finally, [when the École Polytechnique mathematics department didn't let Ciro Santilli do his internship of choice due to grades](ecole-polytechnique.md#when-the-ecole-polytechnique-mathematics-department-didn-t-let-ciro-santilli-do-his-internship-of-choice-due-to-grades) and Ciro was at an useless last moment backup internship, he learned more Python instead of doing his internship job, and was hooked.

#### Python language feature

↑ **Parent:** [Python (programming language)](#python-programming-language)

##### Python classes

↑ **Parent:** [Python language feature](#python-language-feature)

###### Python special method

↑ **Parent:** [Python classes](#python-classes)

[https://docs.python.org/3/reference/datamodel.html#special-method-names](https://docs.python.org/3/reference/datamodel.html#special-method-names)

<h6 id="python-getitem">Python <code>__getitem__</code></h6>

↑ **Parent:** [Python special method](#python-special-method)

<h6 id="_file/python/getitem.py">python/getitem.py</h6>

↑ **Parent:** [Python `__getitem__`](#python-getitem)

<h6 id="_file/python/getitem_complex.py">python/getitem_complex.py</h6>

↑ **Parent:** [Python `__getitem__`](#python-getitem)

- [https://stackoverflow.com/questions/772124/what-does-the-ellipsis-object-do/33087462#33087462](https://stackoverflow.com/questions/772124/what-does-the-ellipsis-object-do/33087462#33087462)
- [https://stackoverflow.com/questions/43627405/understanding-getitem-method/75589367#75589367](https://stackoverflow.com/questions/43627405/understanding-getitem-method/75589367#75589367)

#### Python standard library

↑ **Parent:** [Python (programming language)](#python-programming-language)

##### Python `abc`

↑ **Parent:** [Python standard library](#python-standard-library)

<h6 id="_file/python/abc_cheat.py">python/abc_cheat.py</h6>

↑ **Parent:** [Python `abc`](#python-abc)

##### Python `ast`

↑ **Parent:** [Python standard library](#python-standard-library)

<h6 id="_file/python/ast_cheat.py">python/ast_cheat.py</h6>

↑ **Parent:** [Python `ast`](#python-ast)

##### Python `dataclass`

↑ **Parent:** [Python standard library](#python-standard-library)

<h6 id="python-infer-py">python/infer.py</h6>

↑ **Parent:** [Python `dataclass`](#python-dataclass)

<h6 id="python-dataclass-cheat-py">python/dataclass_cheat.py</h6>

↑ **Parent:** [Python `dataclass`](#python-dataclass)

<h6 id="python-dataclass-hash-py">python/dataclass_hash.py</h6>

↑ **Parent:** [Python `dataclass`](#python-dataclass)

##### Python `tkinter`

↑ **Parent:** [Python standard library](#python-standard-library)

###### Python `tkinter` image editor

↑ **Parent:** [Python `tkinter`](#python-tkinter)  
🏷️ **Tags:** [Image editor](computer.md#image-editor)

- [https://gist.github.com/nikhilkumarsingh/85501ee2c3d8c0cfa9d1a27be5781f06](https://gist.github.com/nikhilkumarsingh/85501ee2c3d8c0cfa9d1a27be5781f06)
- [https://stackoverflow.com/questions/78096353/how-to-create-a-gui-in-python-that-allows-users-to-draw-on-a-canvas](https://stackoverflow.com/questions/78096353/how-to-create-a-gui-in-python-that-allows-users-to-draw-on-a-canvas)
- [https://stackoverflow.com/questions/34777676/how-to-convert-a-python-tkinter-canvas-postscript-file-to-an-image-file-readable](https://stackoverflow.com/questions/34777676/how-to-convert-a-python-tkinter-canvas-postscript-file-to-an-image-file-readable)

###### Python `tkinter` image editor with image recognition

↑ **Parent:** [Python `tkinter` image editor](#python-tkinter-image-editor)

[https://stackoverflow.com/questions/72687998/drawing-digits-with-tkinter-and-entring-them-in-a-neural-network-trained-for-dig](https://stackoverflow.com/questions/72687998/drawing-digits-with-tkinter-and-entring-them-in-a-neural-network-trained-for-dig)

See [lenet/draw.py](lenet/draw.py) described at [lenet](machine-learning.md#_file/lenet).

##### Python `typing`

↑ **Parent:** [Python standard library](#python-standard-library)  
🏷️ **Tags:** [Good](cirism.md#good)

Examples under [python/typing_cheat](python/typing_cheat).

<h6 id="_file/python/typing_cheat/hello.py">python/typing_cheat/hello.py</h6>

↑ **Parent:** [Python `typing`](#python-typing)

The hello world!

<h6 id="_file/python/typing_cheat/infer.py">python/typing_cheat/infer.py</h6>

↑ **Parent:** [Python `typing`](#python-typing)

<h6 id="_file/python/typing_cheat/union.py">python/typing_cheat/union.py</h6>

↑ **Parent:** [Python `typing`](#python-typing)

###### Python `Protocol`

↑ **Parent:** [Python `typing`](#python-typing)

<h6 id="_file/python/typing_cheat/protocol.py">python/typing_cheat/protocol.py</h6>

↑ **Parent:** [Python `Protocol`](#python-protocol)

<h6 id="_file/python/typing_cheat/protocol_empty.py">python/typing_cheat/protocol_empty.py</h6>

↑ **Parent:** [Python `Protocol`](#python-protocol)

#### Zen of Python

↑ **Parent:** [Python (programming language)](#python-programming-language)  
🏷️ **Tags:** [The correlation between software engineers and Buddhism](software.md#the-correlation-between-software-engineers-and-buddhism)

#### Python version

↑ **Parent:** [Python (programming language)](#python-programming-language)

<h5 id="python-3-12">Python 3.12</h5>

↑ **Parent:** [Python version](#python-version)

[https://www.python.org/downloads/release/python-3120/](https://www.python.org/downloads/release/python-3120/)

#### Python implementation

↑ **Parent:** [Python (programming language)](#python-programming-language)

##### CPython

↑ **Parent:** [Python implementation](#python-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CPython)

###### CPython feature

↑ **Parent:** [CPython](#cpython)

###### Global Interpreter Lock

↑ **Parent:** [CPython](#cpython)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Global_Interpreter_Lock)

[https://stackoverflow.com/questions/1294382/what-is-the-global-interpreter-lock-gil-in-cpython](https://stackoverflow.com/questions/1294382/what-is-the-global-interpreter-lock-gil-in-cpython)

###### CPython JIT

↑ **Parent:** [CPython](#cpython)

Added in [CPython 3.13](#cpython-3-13).

To enable tested on [Ubuntu 25.04](systems-programming.md#ubuntu-25-04):
```
git clone https://github.com/python/cpython
cd cpython
git checkout v3.13.7
./configure --enable-experimental-jit
make -j
```

However, the JIT appears to be useless tested as of this Python version, lol:
- [https://news.ycombinator.com/item?id=44476023](https://news.ycombinator.com/item?id=44476023)
- [https://devclass.com/2025/07/09/despite-30-months-work-core-developer-says-pythons-jit-compiler-is-often-slower-than-the-interpreter/](https://devclass.com/2025/07/09/despite-30-months-work-core-developer-says-pythons-jit-compiler-is-often-slower-than-the-interpreter/)
- [https://fidget-spinner.github.io/posts/jit-reflections.html](https://fidget-spinner.github.io/posts/jit-reflections.html)

We can try to test it with [python/inc_loop.py](python/inc_loop.py):
```
time ./python python/inc_loop.py 10000000
```
but the result is just as pathetic as without JIT currently, taking about 1 second for only 10m loops.

This can be compared with the optimal assembly from [c/inc_loop_asm.c](c/inc_loop_asm.c):
```
time ./inc_loop_asm.out 1000000000
```
which does 1 billion loops in about half a second on [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd).

For comparison, [PyPy](#pypy) actually speeds things up and does 1 billion loops in about a second, so only 2x worse than native.

TODO triple check that JIT is enabled. Many threads say the command is:
```
./python -c 'import sysconfig; sysconfig.get_config_var("JIT_DEPS")'
```
but that fails with:
```
ModuleNotFoundError: No module named '_sysconfigdata__linux_x86_64-linux-gnu'
```

For comparison with a properly implemented dynamic language JIT running [nodejs/inc_loop.js](nodejs/inc_loop.js) does 1 billion loops in 0.6s on v22.14.0, close to native.

[https://tonybaloney.github.io/posts/python-gets-a-jit.html](https://tonybaloney.github.io/posts/python-gets-a-jit.html) documents what the initial "JIT" implementation does. It is just an extremely naive concatenation of instructions that avoids a for + switch. No wonder it doesn't speed things up much at all.

###### CPython version

↑ **Parent:** [CPython](#cpython)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CPython_version)

<h6 id="cpython-3-13">CPython 3.13</h6>

↑ **Parent:** [CPython version](#cpython-version)

##### Cython

↑ **Parent:** [Python implementation](#python-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cython)

##### Jython

↑ **Parent:** [Python implementation](#python-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jython)

##### Numba

↑ **Parent:** [Python implementation](#python-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Numba)

##### PyPy

↑ **Parent:** [Python implementation](#python-implementation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PyPy)

#### Python package manager

↑ **Parent:** [Python (programming language)](#python-programming-language)

##### pip (package manager)

↑ **Parent:** [Python package manager](#python-package-manager)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/pip_(package_manager))

How many stupid bugs. How many stupid bugs do we need to face???
- this fucking train-wreck cannot come up with a unified documented way of specifying dependencies:
  - [https://stackoverflow.com/questions/14399534/reference-requirements-txt-for-the-install-requires-kwarg-in-setuptools-setup-py](https://stackoverflow.com/questions/14399534/reference-requirements-txt-for-the-install-requires-kwarg-in-setuptools-setup-py)
  - [https://stackoverflow.com/questions/26900328/install-dependencies-from-setup-py](https://stackoverflow.com/questions/26900328/install-dependencies-from-setup-py)
  - [https://stackoverflow.com/questions/30797124/how-to-use-setup-py-to-install-dependencies-only/63743115](https://stackoverflow.com/questions/30797124/how-to-use-setup-py-to-install-dependencies-only/63743115)
  - [https://stackoverflow.com/questions/6947988/when-to-use-pip-requirements-file-versus-install-requires-in-setup-py](https://stackoverflow.com/questions/6947988/when-to-use-pip-requirements-file-versus-install-requires-in-setup-py)

  So basically `requirements.txt` is the `package-lock.json`. But how to generate it cleanly? You would need to create a virtualenv?
- `pip search` was disabled in 2020: [https://stackoverflow.com/questions/17373473/how-do-i-search-for-an-available-python-package-using-pip](https://stackoverflow.com/questions/17373473/how-do-i-search-for-an-available-python-package-using-pip). WTF. If server load is a problem, just create a token system! It is hard to understand how such a popular language can't raise enough money to keep such simple server functionality running.

##### Conda

↑ **Parent:** [Python package manager](#python-package-manager)  
🏷️ **Tags:** [Evil](cirism.md#evil), [Python virtualization](#python-virtualization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Conda)

Conda is like [pip](#pip-package-manager), except that it also manages shared library dependencies, including providing prebuilts.

This has made [Conda](#conda) very popular in the [deep learning](machine-learning.md#deep-learning) community around 2020, where using Python frontends like [PyTorch](machine-learning.md#pytorch) to configure faster precompiled backends was extremely common.

It also means that it is a full package manager and extremely overbloated and blows up all the time. People should just use [Docker](systems-programming.md#docker-software) instead for that kind of stuff: [https://www.reddit.com/r/learnmachinelearning/comments/kd88p8/comment/keco07k/](https://www.reddit.com/r/learnmachinelearning/comments/kd88p8/comment/keco07k/)

You also have to buy a license to use their repos if you are part of a large-enough organization: [https://stackoverflow.com/questions/74762863/are-conda-miniconda-and-anaconda-free-to-use-and-open-source](https://stackoverflow.com/questions/74762863/are-conda-miniconda-and-anaconda-free-to-use-and-open-source)

###### Install Conda on Ubuntu

↑ **Parent:** [Conda](#conda)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Install_Conda_on_Ubuntu)

Tested on [Ubuntu 20.04](systems-programming.md#ubuntu-20-04):
```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```
Add to your `.bashrc`:
```
PATH="$PATH:$HOME/miniconda3/bin"
```
and then to use it on a shell e.g. with Python 3.9 create the environment with:
```
conda create -y -n mytest3.9 python=3.9
```
and then use it with:
```
eval "$(command conda 'shell.bash' 'hook' 2> /dev/null)"
conda activate mytest3.9
```
Now you can use `python` and `pip` normally from inside that `mytest3.9` environment.

At that time, the exact installer under `latest` appears to have been: [https://repo.anaconda.com/miniconda/Miniconda3-py311_23.11.0-2-Linux-x86_64.sh](https://repo.anaconda.com/miniconda/Miniconda3-py311_23.11.0-2-Linux-x86_64.sh)

##### Poetry (Python package manager)

↑ **Parent:** [Python package manager](#python-package-manager)

#### Python Package Index

↑ **Parent:** [Python (programming language)](#python-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Python_Package_Index)

[https://pypi.org](https://pypi.org)

The best package ever is: [https://pypi.org/project/china-dictatorship/](https://pypi.org/project/china-dictatorship/) see also: [https://cirosantilli.com/china-dictatorship/mirrors](https://cirosantilli.com/china-dictatorship/mirrors)

#### Python virtualization

↑ **Parent:** [Python (programming language)](#python-programming-language)

##### Python version virtualization

↑ **Parent:** [Python virtualization](#python-virtualization)

Answers by [Ciro Santilli](ciro-santilli.md):
- [https://unix.stackexchange.com/questions/9711/what-is-the-proper-way-to-manage-multiple-python-versions/556519#556519](https://unix.stackexchange.com/questions/9711/what-is-the-proper-way-to-manage-multiple-python-versions/556519#556519)
- [https://stackoverflow.com/questions/10960805/apt-get-install-for-different-python-versions/59268046#59268046](https://stackoverflow.com/questions/10960805/apt-get-install-for-different-python-versions/59268046#59268046)
- [https://askubuntu.com/questions/682869/how-do-i-install-a-different-python-version-using-apt-get/1195153#1195153](https://askubuntu.com/questions/682869/how-do-i-install-a-different-python-version-using-apt-get/1195153#1195153)
- "inside project" question:
  - [https://stackoverflow.com/questions/41902497/define-python-version-inside-project/64479032#64479032](https://stackoverflow.com/questions/41902497/define-python-version-inside-project/64479032#64479032)
- [https://stackoverflow.com/questions/2547554/multiple-python-versions-on-the-same-machine/79448734#79448734](https://stackoverflow.com/questions/2547554/multiple-python-versions-on-the-same-machine/79448734#79448734)
- [https://www.reddit.com/r/learnpython/comments/uf4i6w/comment/mdfuyrj/](https://www.reddit.com/r/learnpython/comments/uf4i6w/comment/mdfuyrj/)

###### pyenv

↑ **Parent:** [Python version virtualization](#python-version-virtualization)

##### virtualenv

↑ **Parent:** [Python virtualization](#python-virtualization)

```
python3 -m pip install --user virtualenv
virtualenv .venv
. .venv/bin/activate
pip install -r requirements.txt
```

#### Python documentation generator

↑ **Parent:** [Python (programming language)](#python-programming-language)  
🏷️ **Tags:** [Documentation generator](software.md#documentation-generator)

##### Sphinx (documentation generator)

↑ **Parent:** [Python documentation generator](#python-documentation-generator)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Sphinx_(documentation_generator))

<h6 id="_file/python/sphinx">python/sphinx</h6>

↑ **Parent:** [Sphinx (documentation generator)](#sphinx-documentation-generator)

To run each example and see the output run:
```
./build.sh
xdg-open out/index.html
```

<h6 id="_file/python/sphinx/hello">python/sphinx/hello</h6>

↑ **Parent:** [Sphinx (documentation generator)](#sphinx-documentation-generator)

Minimal example. Gives a hint at how boilerplate heavy Sphinx can be!

<h6 id="_file/python/sphinx/union">python/sphinx/union</h6>

↑ **Parent:** [Sphinx (documentation generator)](#sphinx-documentation-generator)

[https://stackoverflow.com/questions/34647966/how-to-express-multiple-types-for-a-single-parameter-or-a-return-value-in-docstr/40801906#40801906](https://stackoverflow.com/questions/34647966/how-to-express-multiple-types-for-a-single-parameter-or-a-return-value-in-docstr/40801906#40801906)

<h6 id="_file/python/sphinx/class">python/sphinx/class</h6>

↑ **Parent:** [Sphinx (documentation generator)](#sphinx-documentation-generator)

Basic class example.

<h6 id="_file/python/sphinx/virtual_method">python/sphinx/virtual_method</h6>

↑ **Parent:** [Sphinx (documentation generator)](#sphinx-documentation-generator)

[Polymorphism](software.md#polymorphism-computer-science) example:
- [https://stackoverflow.com/questions/4714136/how-to-implement-virtual-methods-in-python/38717503#38717503](https://stackoverflow.com/questions/4714136/how-to-implement-virtual-methods-in-python/38717503#38717503)
- [https://stackoverflow.com/questions/17841323/how-to-annotate-a-member-as-abstract-in-sphinx-documentation/75634909#75634909](https://stackoverflow.com/questions/17841323/how-to-annotate-a-member-as-abstract-in-sphinx-documentation/75634909#75634909)

#### Python library

↑ **Parent:** [Python (programming language)](#python-programming-language)

##### Python scientific library

↑ **Parent:** [Python library](#python-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Python_scientific_library)

###### Jupyter Notebook

↑ **Parent:** [Python scientific library](#python-scientific-library)  
🏷️ **Tags:** [Evil](cirism.md#evil)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Project_Jupyter#Jupyter_Notebook)

A waste of time. Output in my source files [pollutes git](https://stackoverflow.com/questions/28908319/how-to-clear-an-ipython-notebooks-output-in-all-cells-from-the-linux-terminal/47774393#47774393) and prevents me from editing it in [Vim](software.md#vim). Just let me run the freacking code and render images as standalone PNGs which I can include from Markdown.

Some other basic hits due to how bad Jupyter is:
- [https://stackoverflow.com/questions/41159797/how-to-disable-password-request-for-a-jupyter-notebook-session/47509274#47509274](https://stackoverflow.com/questions/41159797/how-to-disable-password-request-for-a-jupyter-notebook-session/47509274#47509274)
- [https://stackoverflow.com/questions/36901154/how-export-a-jupyter-notebook-to-html-from-the-command-line/47773056#47773056](https://stackoverflow.com/questions/36901154/how-export-a-jupyter-notebook-to-html-from-the-command-line/47773056#47773056)

<h6 id="_file/python/jupyter/hello.ipynb">python/jupyter/hello.ipynb</h6>

↑ **Parent:** [Jupyter Notebook](#jupyter-notebook)

###### NumPy

↑ **Parent:** [Python scientific library](#python-scientific-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/NumPy)

The people who work on this will [go straight to heaven](cirism.md#good), no questions asked.

<h6 id="numpy-fft">numpy.fft</h6>

↑ **Parent:** [NumPy](#numpy)  
🏷️ **Tags:** [Discrete Fourier transform](calculus.md#discrete-fourier-transform)

[https://numpy.org/doc/1.24/reference/routines.fft.html](https://numpy.org/doc/1.24/reference/routines.fft.html)

<h6 id="_file/numpy/fft_plot.py">numpy/fft_plot.py</h6>

↑ **Parent:** [Numpy.fft](#numpy-fft)

Generates `numpy/fft_plot.svg`, the plot of $2 \sin(t) +  \cos(4t)$ with 25 points and its [DFT](calculus.md#discrete-fourier-transform).

The output was also uploaded to: [https://commons.wikimedia.org/wiki/File:DFT_2sin(t)_%2B_sin(4t).svg](https://commons.wikimedia.org/wiki/File:DFT_2sin(t)_%2B_sin(4t).svg) and added to [https://en.wikipedia.org/w/index.php?title=Discrete_Fourier_transform&oldid=1176616763](https://en.wikipedia.org/w/index.php?title=Discrete_Fourier_transform&oldid=1176616763) only to be later removed of course: [Deletionism on Wikipedia](website.md#deletionism-on-wikipedia).

<a id="image-dft-of-2-sin-t-plus-cos-4t-with-25-points"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/home/numpy/fft_plot.svg" alt="" height="600">

**[Figure 4](#image-dft-of-2-sin-t-plus-cos-4t-with-25-points). DFT of $2 \sin(t) +  \cos(4t)$ with 25 points**. Source code at: [numpy/fft_plot.py](numpy/fft_plot.py).

<h6 id="_file/numpy/fft.py">numpy/fft.py</h6>

↑ **Parent:** [Numpy.fft](#numpy-fft)

Output:
```
sin(t)
fft
real 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
imag 0 -10 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 10
rfft
real 0 0 0 0 0 0 0 0 0 0 0
imag 0 -10 0 0 0 0 0 0 0 0 0

sin(t) + sin(4t)
fft
real 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
imag 0 -10 0 0 -10 0 0 0 0 0 0 0 0 0 0 0 10 0 0 10
rfft
real 0 0 0 0 0 0 0 0 0 0 0
imag 0 -10 0 0 -10 0 0 0 0 0 0
```
With our understanding of the [discrete Fourier transform](calculus.md#discrete-fourier-transform) we see clearly that:
- the signal is being decomposed into [sinusoidal](calculus.md#sinusoidal) components
- because we are doing the [Discrete Fourier transform of a real signal](calculus.md#discrete-fourier-transform-of-a-real-signal), for the `fft`, $X_k = \conj{X_{N-k}}$ so there is redundancy in the. We also understand that `rfft` simply cuts off and only keeps half of the coefficients

###### SageMath

↑ **Parent:** [Python scientific library](#python-scientific-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SageMath)

A [Python](#python-programming-language) wrapper over a bunch of [numeric](software.md#numerical-software) and [computer algebra system](software.md#computer-algebra-system) packages to try and fully replace [MATLAB](mathematics.md#matlab) et. al.

For example, their 

Quickstart tutorial at: [https://www.sagemath.org/tour-quickstart.html](https://www.sagemath.org/tour-quickstart.html) From this we see that they are very opinionated, you don't need to import anything, everything has a pre-defined global name, which is convenient, e.g.:

$$
QQ^3
$$

is the [3D](calculus.md#real-coordinate-space-of-dimension-three) [vector space](linear-algebra.md#vector-space) over the [rationals](formalization-of-mathematics.md#rational-number). This also suggests that they are quite focused on [computer algebra](software.md#computer-algebra-system) as opposed to numerical.

###### Scikit-learn

↑ **Parent:** [Python scientific library](#python-scientific-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Scikit-learn)

Examples under [python/sklearn](python/sklearn)

```
. .venv/bin/activate
pip install sklearn matplotlib seaborn
```

##### Python web framework

↑ **Parent:** [Python library](#python-library)  
🏷️ **Tags:** [Web framework](web-technology.md#web-framework)

###### Django (web-framework)

↑ **Parent:** [Python web framework](#python-web-framework)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Django_(web-framework))

[React](react.md) setups:
- [https://stackoverflow.com/questions/41867055/how-to-get-django-and-reactjs-to-work-together](https://stackoverflow.com/questions/41867055/how-to-get-django-and-reactjs-to-work-together)
- [https://www.fullstackpython.com/react.html](https://www.fullstackpython.com/react.html)

One problem with Django is that it does not expose its [ORM](software.md#object-relational-mapping) as an external library: [https://stackoverflow.com/questions/33170016/how-to-use-django-1-8-5-orm-without-creating-a-django-project](https://stackoverflow.com/questions/33170016/how-to-use-django-1-8-5-orm-without-creating-a-django-project) which is wasteful of development time.

<h6 id="gothinkster-django-realworld-example-app">gothinkster/django-realworld-example-app</h6>

↑ **Parent:** [Django (web-framework)](#django-web-framework)  
🏷️ **Tags:** [Gothinkster/realworld implementation](web-technology.md#gothinkster-realworld-implementation)

As of 2021, last updated 2016, and python 3.5 appears to be mandatory or else:
```
RuntimeError: __class__ not set defining 'AbstractBaseUser' as <class 'django.contrib.auth.base_user.AbstractBaseUser'>. Was __classcell__ propagated to type.__new__?
```
which apparently broke in 3.6: [https://stackoverflow.com/questions/41343263/provide-classcell-example-for-python-3-6-metaclass](https://stackoverflow.com/questions/41343263/provide-classcell-example-for-python-3-6-metaclass) and `pyenv` install fails on Ubuntu 20.10, so... fuck. Workarounds at:
- [https://askubuntu.com/questions/1034475/the-python-ssl-extension-was-not-compiled-missing-the-openssl-lib-error-when](https://askubuntu.com/questions/1034475/the-python-ssl-extension-was-not-compiled-missing-the-openssl-lib-error-when)
- [https://stackoverflow.com/questions/52873193/error-the-python-ssl-extension-was-not-compiled-missing-the-openssl-lib-inst](https://stackoverflow.com/questions/52873193/error-the-python-ssl-extension-was-not-compiled-missing-the-openssl-lib-inst)
but am I in the mood considering that the ancient Django version would require an immediate port anyways? Repo is at Django 1.0, while newest is now already Django 3. The Rails one is broken for the same reason. Fuck 2.

### R (programming language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/R_(programming_language))

Ubuntu 23.04 install:
```
sudo apt install rbase
```

[Hello world](software.md#hello-world-program):
```
R -e 'print("hello world")'
```

Install  a package, e.g. [Bookdown](website.md#bookdown):
```
sudo R -e 'install.packages("bookdown")'
```

### Ruby (programming language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ruby_(programming_language))

#### Ruby on Rails

↑ **Parent:** [Ruby (programming language)](#ruby-programming-language)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ruby_on_Rails)

The only reason why [Ruby](#ruby-programming-language) exists.

This web framework is pretty good as of 2020 compared to others, because it managed to gain a critical community size, and there's a lot of basic setup already done for you.

it is just big shame it wasn't written in [Python](#python-programming-language) or even better, [Node.js](node-js.md), because learning [Ruby](#ruby-programming-language) is completely useless for anything else. As of 2020 for example, most [Node.js](node-js.md) web frameworks feel like crap compared to Rails, you just have to debug so much there.

Used in [GitLab](software.md#gitlab), which is why [Ciro Santilli](ciro-santilli.md) touched it.

##### Ruby on Rails React integration

↑ **Parent:** [Ruby on Rails](#ruby-on-rails)

Integrations [React](react.md) integration:
- [https://github.com/shakacode/react_on_rails](https://github.com/shakacode/react_on_rails): [webpack](webpack.md) and [server-side rendering](web-technology.md#server-side-rendering)
- [https://github.com/reactjs/react-rails](https://github.com/reactjs/react-rails) Official on the React side only. Demo app linked from package: [https://github.com/BookOfGreg/react-rails-example-app](https://github.com/BookOfGreg/react-rails-example-app) and how it fails: [https://github.com/BookOfGreg/react-rails-example-app/issues/30](https://github.com/BookOfGreg/react-rails-example-app/issues/30)... The related projects section has some good links:
- [shakacode/react\_on\_rails](#shakacode-react-on-rails)
- [https://github.com/hyperstack-org/hyperstack](https://github.com/hyperstack-org/hyperstack) [transpiles](software.md#source-to-source-compiler) Ruby to JavaScript + React. What could possibly go wrong? :-)

<h6 id="shakacode-react-on-rails">shakacode/react_on_rails</h6>

↑ **Parent:** [Ruby on Rails React integration](#ruby-on-rails-react-integration)

Uses Redux, while reactjs/react-rails appears to do that more manually

Lots of focus on [Heroku](computer-hardware.md#heroku) deployability, which is fantastic: [https://shakacode.gitbooks.io/react-on-rails/content/docs/additional-reading/heroku-deployment.html](https://shakacode.gitbooks.io/react-on-rails/content/docs/additional-reading/heroku-deployment.html)

Live instance: [https://www.reactrails.com/](https://www.reactrails.com/) with source at: [https://github.com/shakacode/react-webpack-rails-tutorial](https://github.com/shakacode/react-webpack-rails-tutorial) Not the most advanced web-app (a [gothinkster/realworld](web-technology.md#gothinkster-realworld)-level would be ideal). Also has clear dependency description, which is nice.

Trying at [https://github.com/shakacode/react-webpack-rails-tutorial/tree/8e656f97d7a311bbe999ceceb9463b8479fef9e2](https://github.com/shakacode/react-webpack-rails-tutorial/tree/8e656f97d7a311bbe999ceceb9463b8479fef9e2) on [Ubuntu](systems-programming.md#ubuntu) 20.10. Got some failures: [https://github.com/shakacode/react-webpack-rails-tutorial/issues/488](https://github.com/shakacode/react-webpack-rails-tutorial/issues/488) Finally got a version of it working at: [https://github.com/shakacode/react-webpack-rails-tutorial/issues/488#issuecomment-812506821](https://github.com/shakacode/react-webpack-rails-tutorial/issues/488#issuecomment-812506821)

Oh, and the guy behind that project lives in [Hawaii](united-states.md#hawaii) ([Ciro Santilli's ideal city to live in](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-ideal-city-to-live-in)), has an Asian-mixed son, and two [Kinesis Advantage 2 keyboards](computer-hardware.md#kinesis-advantage-2-keyboard) as seen at [https://twitter.com/railsonmaui/status/1377515748910755851](https://twitter.com/railsonmaui/status/1377515748910755851), [Ciro Santilli](ciro-santilli.md) was jealous of him.

### Rust (programming language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Rust_(programming_language))

#### Rust library

↑ **Parent:** [Rust (programming language)](#rust-programming-language)

### Short Code (programming-language)

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Short_Code_(computer_language))

### Tcl

↑ **Parent:** [List of programming languages](#list-of-programming-languages)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tcl)

One of the first big [interpreted programming languages](#interpreted-programming-language) to go a bit further than [Bash](#bash-unix-shell)' word replacement insanity.

To the modern viewer, it feels like a middle ground between [Bash](#bash-unix-shell) and [Python](#python-programming-language).

It was completely insane however, and it just died: [Python](#python-programming-language) is much saner, and [Bash](#bash-unix-shell), although totally insane still [golfs](software.md#code-golf) better, especially on the file manipulation context.

## ↑ Ancestors (6)

1. [Software](software.md)
2. [Computer](computer.md)
3. [Information technology](technology.md#information-technology)
4. [Area of technology](technology.md#area-of-technology)
5. [Technology](technology.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (5)

- [Ciro Santilli](ciro-santilli.md)
- [FutureAI](artificial-intelligence.md#futureai)
- [How computers work?](computer.md#how-computers-work)
- [Natural language](linguistics.md#natural-language)
- [Web framework](web-technology.md#web-framework)
