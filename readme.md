# electron-repl

Interactive REPL for debugging Electron programs.

## About

run an electron program but also attach a repl to the same context that your code runs in so you can inspect + mess with stuff as your program is running

available as a command-line tool

this is a fork of [node-repl](https://github.com/maxogden/node-repl) by [maxogden](https://github.com/maxogden)


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

## example

suppose we have a program called `hello.js` that has these contents:

```js
var pizza = 1
```

if you run `electron-repl hello.js` you will get a repl, just like when you run `electron`.

The difference is that this repl is running *in the same context as your program*.

```
$ electron-repl hello.js
> 1 + 1 // we are in an electron repl
2
> pizza // we can access variables in our program
1
>
```

## credit

This is a fork of [node-repl](https://github.com/maxogden/node-repl) modified to work with [electron](https://github.com/electron/electron). Almost everything in this module was originally created by [maxogden](https://github.com/maxogden) and `node-repl` contributors. Thank you!

## license

BSD
