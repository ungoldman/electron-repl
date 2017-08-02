# electron-repl [![stability][0]][1]

Interactive REPL for debugging Electron programs.

[![npm][2]][3]
[![travis][4]][5]
[![standard][6]][7]
[![downloads][8]][3]

[0]: https://img.shields.io/badge/stability-experimental-orange.svg?style=flat-square
[1]: https://nodejs.org/api/documentation.html#documentation_stability_index
[2]: https://img.shields.io/npm/v/electron-repl.svg?style=flat-square
[3]: https://www.npmjs.com/package/electron-repl
[4]: https://img.shields.io/travis/hypermodules/electron-repl/master.svg?style=flat-square
[5]: https://travis-ci.org/hypermodules/electron-repl
[6]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[7]: http://standardjs.com/
[8]: https://img.shields.io/npm/dm/electron-repl.svg?style=flat-square

## About

Run an electron program but also attach a REPL to the same context that your code runs in so you can inspect and mess with stuff as your program is running!

**This is alpha quality and not guaranteed to work with complex programs! Please report issues and contribute fixes if you can.**

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

## Contributing

Contributions welcome! Please read the [contributing guidelines](contributing.md) first.

## Credit

This is a fork of [node-repl](https://github.com/maxogden/node-repl) modified to work with [electron](https://github.com/electron/electron). Almost everything in this module was originally created by [maxogden](https://github.com/maxogden) and `node-repl` contributors. Thank you!

## License

BSD
