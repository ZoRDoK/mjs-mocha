# @eliseevnp/mjs-mocha
A very simple npm mocha mjs polyfill. No dependencies at all. Very small and light.

## Install
```shell
$ npm i -D @eliseevnp/mjs-mocha
```

## Usage
### Import

```js
import '@eliseevnp/mjs-mocha';

describe('My test', () => {
  ...
})
```

### CLI
Add the script to your `package.json`.

```json
{
  "scripts": {
    "test:mjs": "mjs-mocha --extension mjs",
    "test:js": "mjs-mocha --extension js"
  }
}
```

Then just run `npm test:mjs` or `npm test:js`.

mjs-mocha will run all files that match by specifying extension. Default regexp matches all `*.test.mjs` and `*.spec.mjs` files in your repository. If you want matching all `*.test.js` and `*.spec.js` files in your repository you must provide `--extension js` option.

Also you can specify test files to run by passing them as arguments.

#### Example
project structure:
- src
  - ...
- tests
  - first.test.mjs
  - second.test.mjs
  - third.test.mjs

```shell
mjs-mocha first second
```
