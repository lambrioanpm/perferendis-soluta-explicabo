# @lambrioanpm/perferendis-soluta-explicabo <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Map? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isMap = require('@lambrioanpm/perferendis-soluta-explicabo');
assert(!isMap(function () {}));
assert(!isMap(null));
assert(!isMap(function* () { yield 42; return Infinity; });
assert(!isMap(Symbol('foo')));
assert(!isMap(1n));
assert(!isMap(Object(1n)));

assert(!isMap(new Set()));
assert(!isMap(new WeakSet()));
assert(!isMap(new WeakMap()));

assert(isMap(new Map()));

class MyMap extends Map {}
assert(isMap(new MyMap()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@lambrioanpm/perferendis-soluta-explicabo
[npm-version-svg]: https://versionbadg.es/inspect-js/@lambrioanpm/perferendis-soluta-explicabo.svg
[deps-svg]: https://david-dm.org/inspect-js/@lambrioanpm/perferendis-soluta-explicabo.svg
[deps-url]: https://david-dm.org/inspect-js/@lambrioanpm/perferendis-soluta-explicabo
[dev-deps-svg]: https://david-dm.org/inspect-js/@lambrioanpm/perferendis-soluta-explicabo/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@lambrioanpm/perferendis-soluta-explicabo#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@lambrioanpm/perferendis-soluta-explicabo.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@lambrioanpm/perferendis-soluta-explicabo.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@lambrioanpm/perferendis-soluta-explicabo.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@lambrioanpm/perferendis-soluta-explicabo
[codecov-image]: https://codecov.io/gh/inspect-js/@lambrioanpm/perferendis-soluta-explicabo/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@lambrioanpm/perferendis-soluta-explicabo/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@lambrioanpm/perferendis-soluta-explicabo
[actions-url]: https://github.com/lambrioanpm/perferendis-soluta-explicabo/actions
