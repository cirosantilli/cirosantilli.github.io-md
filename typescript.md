# TypeScript

↑ **Parent:** [JavaScript](programming-language.md#javascript)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/TypeScript)

TypeScript is good. It does find errors in your [JavaScript](programming-language.md#javascript). But it is a form of "turd polishing". But [Ciro Santilli](ciro-santilli.md) would rather have a polished turd than a non-polished one.

Part of the reason TypeScript became popular is due to the universality of [asset bundlers](web-technology.md#asset-bundler). Once you are already using an asset bundler, changing the `.js` extension into `.ts` to get a less shitty experience is an easy choice.

The other big reason is that JavaScript is so lose with type conversions, notably undefined happily converting to strings without problems, and any missing properties of Object happily being undefined. We should actually use ES6 Map everywhere instead of using Objects as maps.

Since TypeScript is not the default form of the language however, it inevitably happens that you need to add external types for a gazillion projects that are using raw JavaScript, and sometimes fight a lot to get things to work. And so we have: [https://github.com/DefinitelyTyped/DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped). Not sure if this is beautiful, or frightening.

But in the end, as with other type of static [linters](software.md#linting), TypeScript generally transforms a few hard to debug runtime issues, into a bunch of stupid to solve compile time issues, which is generally a good thing.

The fact that this it parses comments JSDoc comments in JavaScript files is quite amazing.

Examples under [typescript](typescript). Run each one of them with:
```
npx tsc example.ts
node example.js
```
Helper:
```
tsr() (
  # ts Run
  f="$1"
  npx tsc "$f"
  node "${f%.*}.js"
)
tsr example.ts
```

- [typescript/inferFromInit.ts](typescript/inferFromInit.ts). Should fail with:> hello.ts:2:1 - error TS2322: Type 'string' is not assignable to type 'number

  since TypeScript infers the type of `i` from first assignment as `string`, and we then attempt a `number` assignment later on
- [typescript/inferAfterInit.ts](typescript/inferAfterInit.ts). Does not fail, as the first assignment cannot be computationally determined at runtime without breaking computer science.
- [typescript/js-from-ts/main.ts](typescript/js-from-ts/main.ts): call [JavaScript](programming-language.md#javascript) file [typescript/js-from-ts/notmain.js](typescript/js-from-ts/notmain.js) from [TypeScript](typescript.md).
  ```
  npx tsc jsFromTs.ts && node jsFromTs.js
  ```

  TODO we are unable to make it typecheck that require, i.e. make that fail, but we've seen cases in complex codebases where that did happen and [https://www.typescriptlang.org/docs/handbook/intro-to-js-ts.html](https://www.typescriptlang.org/docs/handbook/intro-to-js-ts.html) has infinite information on supporting it. So... how to make it fail??
- [typescript/functionArgument.ts](typescript/functionArgument.ts): basic argument tests
  - [typescript/functionOptionalArgument.ts](typescript/functionOptionalArgument.ts): `f(n?: number)`
- [typescript/functionOptions.ts](typescript/functionOptions.ts): `f({n, s}: {n: number, s: string})`

Some major annoyances of TypeScript:
- destructuring assignment in function arguments requires repeating all arguments:
  - [https://stackoverflow.com/questions/42108807/using-named-parameters-javascript-based-on-typescript/71679344#71679344](https://stackoverflow.com/questions/42108807/using-named-parameters-javascript-based-on-typescript/71679344#71679344)
  - [https://stackoverflow.com/questions/54513548/destructure-a-function-parameter-in-typescript](https://stackoverflow.com/questions/54513548/destructure-a-function-parameter-in-typescript)
  - [https://github.com/Microsoft/TypeScript/issues/29526](https://github.com/Microsoft/TypeScript/issues/29526)
- [https://stackoverflow.com/questions/12710905/how-do-i-dynamically-assign-properties-to-an-object-in-typescript](https://stackoverflow.com/questions/12710905/how-do-i-dynamically-assign-properties-to-an-object-in-typescript) how to dynamically assign properties to objects without defining explicit interfaces? We really need a syntax of type:
  ```
  const myobj = {
    i: 2,
    [s string],
  }
  if (something) {
    myobj.s = 'asdf'
  }
  ```

## ↑ Ancestors (9)

1. [JavaScript](programming-language.md#javascript)
2. [List of programming languages](programming-language.md#list-of-programming-languages)
3. [Programming language](programming-language.md)
4. [Software](software.md)
5. [Computer](computer.md)
6. [Information technology](technology.md#information-technology)
7. [Area of technology](technology.md#area-of-technology)
8. [Technology](technology.md)
9. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (6)

- [List of personal knowledge base software](brain.md#list-of-personal-knowledge-base-software)
- [Next.js](react.md#next-js)
- [Next.js example](react.md#next-js-example)
- [Quartz (personal knowledge base)](brain.md#quartz-personal-knowledge-base)
- [TypeScript](typescript.md)
- [webpack](webpack.md)
