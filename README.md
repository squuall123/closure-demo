[![CircleCI](https://circleci.com/gh/angular/closure-demo.svg?style=svg)](https://circleci.com/gh/angular/closure-demo)

This repo is the demo/seed for bunding an Angular application with Google Closure Compiler.
It contains a minimal Hello World application with a single component.

**The compressed JS size for an Angular 5.0.1 Hello World app is 39.99kb.**

```
-rw-r--r--  1 29055 Nov  9 18:42 dist/bundle.js.brotli
-rw-r--r--  1 32554 Nov  9 18:42 dist/bundle.js.gz
-rw-r--r--  1 11896 Nov  9 18:42 node_modules/zone.js/dist/zone.min.js.brotli
-rw-r--r--  1 12988 Nov  9 18:32 node_modules/zone.js/dist/zone.min.js.gz
```

See https://github.com/angular/angular/issues/8550 for more context.

# Try it

First, install [brotli], which is a more modern compression algorithm than gzip.
It gives a 13% smaller JS file, no work required!
The commands below use it, but you don't have to.

On Mac, `brew install brotli`.

``` shell
$ yarn install
$ yarn run build
$ yarn run serve
```

[brotli]: https://github.com/google/brotli

## Where does the size come from?

``` shell
$ yarn run explore
```

# Notes

Requires Node >= 6.x since the `ngc` tool (and its deps) are now shipped as ES6 as well.

Requires Java installed to run the Closure Compiler. We recommend installing http://zulu.org/download-dev/.
