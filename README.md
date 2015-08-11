# es-6-template-regex [![NPM version](https://badge.fury.io/js/es-6-template-regex.svg)](http://badge.fury.io/js/es-6-template-regex)  [![Build Status](https://travis-ci.org/jonschlinkert/es-6-template-regex.svg)](https://travis-ci.org/jonschlinkert/es-6-template-regex)

> Regular expression for matching es6 template delimiters in a string.

## Install

Install with [npm](https://www.npmjs.com/)

```sh
$ npm i es-6-template-regex --save
```

## Usage

The top-level export of this module is a function:

```js
var re = require('es-6-template-regex');

function interpolate(str, data) {
  return str.replace(re(), function(m, prop) {
    return data[prop] || prop;
  });
}

var str = 'foo ${bar} baz ${quux}';
var data = {bar: 'AAA', quux: 'BBB'};
interpolate(str, data);
//=> 'foo AAA baz BBB'
```

## Running tests

Install dev dependencies:

```sh
$ npm i -d && npm test
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/es-6-template-regex/issues/new)

## Author

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2015 Jon Schlinkert
Released under the MIT license.

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on August 10, 2015._