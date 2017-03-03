UglifyCSS is a port of [YUI Compressor](https://github.com/yui/yuicompressor) to [NodeJS](http://nodejs.org) for its CSS part. Its name is a reference to the awesome [UglifyJS](https://github.com/mishoo/UglifyJS) but UglifyCSS is not a CSS parser. Like YUI CSS Compressor, it applies many regexp replacements. Note that a [port to JavaScript](https://github.com/yui/ycssmin) is also available in the YUI Compressor repository.

UglifyCSS passes successfully the test suite of YUI compressor CSS.

Be sure to submit valid CSS to UglifyCSS or you could get weird results.

### Installation

```sh
$ npm install uglifycss
```

### API

2 functions are provided:

* `processString( content, options )` to process a given string

Options available:
* `<int> maxLineLen` for `--max-line-len n`
* `<bool> expandVars` for `--expand-vars`
* `<bool> uglyComments` for `--ugly-comments`
* `<bool> cuteComments` for `--cute-comments`
* `<string> convertUrls` for `--convert-urls d`
* `<bool> debug` for `--debug`

#### Example

```js
var uglifycss = require('uglifycss');

var uglified = uglifycss.processString(
    'body { color: #000000 }',
    { maxLineLen: 500, expandVars: true }
);

console.log(uglified);
```

### License

UglifyCSS is MIT licensed.
