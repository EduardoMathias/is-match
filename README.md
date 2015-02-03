# is-match [![NPM version](https://badge.fury.io/js/is-match.svg)](http://badge.fury.io/js/is-match)  [![Build Status](https://travis-ci.org/jonschlinkert/is-match.svg)](https://travis-ci.org/jonschlinkert/is-match) 

> Create a matching function from a glob pattern, regex, string, array or function.

## Install with [npm](npmjs.org)

```bash
npm i is-match --save
```

## Usage

```js
var isMatch = require('is-match');
```

### Create matchers:

**from a string:**

```js
var isMatch = matcher('a')

isMatch('a');
//=> true

isMatch('b');
//=> false
```

**from a glob pattern:**

```js
var isMatch = matcher('*')
isMatch('a'); //=> true

var isMatch = matcher('!b')
isMatch('a'); //=> true

var isMatch = matcher('!b')
isMatch('b'); //=> false
```

**from an array of glob patterns:**

```js
var isMatch = matcher(['b'])
isMatch('a'); //=> false

var isMatch = matcher(['b', 'a'])
isMatch('a'); //=> true

var isMatch = matcher(['b', 'c', '*'])
isMatch('a'); //=> true
```

**from a regex:**

```js
var isMatch = matcher(/a/);

isMatch('a');
//=> true

isMatch('b');
//=> false
```

**from a function:**

```js
var isMatch = matcher(function  (val) {
  return val === 'a';
});
isMatch('a');
//=> true

isMatch('b');
//=> false
```

## Run tests

Install dev dependencies:

```bash
npm i -d && npm test
```

## Contributing
Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/is-match/issues)

## Author

**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2015 Jon Schlinkert  
Released under the MIT license

***

_This file was generated by [verb](https://github.com/assemble/verb) on February 03, 2015._