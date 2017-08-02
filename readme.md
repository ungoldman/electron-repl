# electron-repl

Interactive REPL for debugging Electron programs.

[![npm][npm-image]][npm-url]
[![travis][travis-image]][travis-url]
[![standard][standard-image]][standard-url]
[![downloads][downloads-img]][npm-url]

[npm-image]: https://img.shields.io/npm/v/electron-repl.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/electron-repl
[travis-image]: https://img.shields.io/travis/hypermodules/electron-repl/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/hypermodules/electron-repl
[standard-image]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[standard-url]: http://standardjs.com/
[downloads-img]: https://img.shields.io/npm/dm/electron-repl.svg?style=flat-square

## About

Run an electron program but also attach a REPL to the same context that your code runs in so you can inspect and mess with stuff as your program is running!

This command-line tool is a fork of [node-repl](https://github.com/maxogden/node-repl) by [maxogden](https://github.com/maxogden).

## Usage

```sh
$ npm i -g electron-repl
$ electron-repl
Usage: electron-repl <filename>

$ electron-repl your-program.js
>
```

If you have `npm@5.2+` installed, you can just do:

```sh
$ npx electron-repl your-program.js
>
```

## Example

Suppose we have a program called `hello.js` that has these contents:

```js
var pizza = 1
```

If you run `electron-repl hello.js` you will get a REPL, just like when you run `electron`.

The difference is that this REPL is running *in the same context as your program*.

```
$ electron-repl hello.js
> 1 + 1 // we are in an electron repl
2
> pizza // we can access variables in our program
1
>
```

## Credit

This is a fork of [node-repl](https://github.com/maxogden/node-repl) modified to work with [electron](https://github.com/electron/electron). Almost everything in this module was originally created by [maxogden](https://github.com/maxogden) and `node-repl` contributors. Thank you!

## License

BSD
