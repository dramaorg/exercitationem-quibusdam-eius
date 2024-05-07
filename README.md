# @dramaorg/exercitationem-quibusdam-eius <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Object-related atoms: Object, ToObject, RequireObjectCoercible.

## Example

```js
const assert = require('assert');

const $Object = require('@dramaorg/exercitationem-quibusdam-eius');
const ToObject = require('@dramaorg/exercitationem-quibusdam-eius/ToObject');
const RequireObjectCoercible = require('@dramaorg/exercitationem-quibusdam-eius/RequireObjectCoercible');

assert.equal($Object, Object);
assert.throws(() => ToObject(null), TypeError);
assert.throws(() => ToObject(undefined), TypeError);
assert.throws(() => RequireObjectCoercible(null), TypeError);
assert.throws(() => RequireObjectCoercible(undefined), TypeError);

assert.deepEqual(RequireObjectCoercible(true), true);
assert.deepEqual(ToObject(true), Object(true));

const obj = {};
assert.equal(RequireObjectCoercible(obj), obj);
assert.equal(ToObject(obj), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@dramaorg/exercitationem-quibusdam-eius
[npm-version-svg]: https://versionbadg.es/ljharb/@dramaorg/exercitationem-quibusdam-eius.svg
[deps-svg]: https://david-dm.org/ljharb/@dramaorg/exercitationem-quibusdam-eius.svg
[deps-url]: https://david-dm.org/ljharb/@dramaorg/exercitationem-quibusdam-eius
[dev-deps-svg]: https://david-dm.org/ljharb/@dramaorg/exercitationem-quibusdam-eius/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@dramaorg/exercitationem-quibusdam-eius#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@dramaorg/exercitationem-quibusdam-eius.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@dramaorg/exercitationem-quibusdam-eius.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/es-object.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@dramaorg/exercitationem-quibusdam-eius
[codecov-image]: https://codecov.io/gh/ljharb/@dramaorg/exercitationem-quibusdam-eius/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@dramaorg/exercitationem-quibusdam-eius/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@dramaorg/exercitationem-quibusdam-eius
[actions-url]: https://github.com/dramaorg/exercitationem-quibusdam-eius/actions
