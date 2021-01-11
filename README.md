## vapjs-rpc

<div>
  <!-- Dependency Status -->
  <a href="https://david-dm.org/vapjs/vapjs-rpc">
    <img src="https://david-dm.org/vapjs/vapjs-rpc.svg"
    alt="Dependency Status" />
  </a>

  <!-- devDependency Status -->
  <a href="https://david-dm.org/vapjs/vapjs-rpc#info=devDependencies">
    <img src="https://david-dm.org/vapjs/vapjs-rpc/dev-status.svg" alt="devDependency Status" />
  </a>

  <!-- Build Status -->
  <a href="https://travis-ci.org/vapjs/vapjs-rpc">
    <img src="https://travis-ci.org/vapjs/vapjs-rpc.svg"
    alt="Build Status" />
  </a>

  <!-- NPM Version -->
  <a href="https://www.npmjs.org/package/vapjs-rpc">
    <img src="http://img.shields.io/npm/v/vapjs-rpc.svg"
    alt="NPM version" />
  </a>

  <!-- Test Coverage -->
  <a href="https://coveralls.io/r/vapjs/vapjs-rpc">
    <img src="https://coveralls.io/repos/github/vapjs/vapjs-rpc/badge.svg" alt="Test Coverage" />
  </a>

  <!-- Javascript Style -->
  <a href="http://airbnb.io/javascript/">
    <img src="https://img.shields.io/badge/code%20style-airbnb-brightgreen.svg" alt="js-airbnb-style" />
  </a>
</div>

<br />

A super simple module for querying the Vapory RPC layer without formatting.

This module was influenced by: [`vap-query`](https://github.com/vaporycojs/vap-query).

## Install

```
npm install --save vapjs-rpc
```

## Usage

```js
const HttpProvider = require('vapjs-provider-http');
const VapRPC = require('vapjs-rpc');
const vap = new VapRPC(new HttpProvider('http://localhost:8545'));

// accounts
vap.sendAsync({ method: 'vap_accounts' }, (err, accounts1) => {
  // null ['0x...', '0x....']
});

// gasPrice
vap.sendAsync({ method: 'vap_gasPrice' }, (err, gasPrice) => {
  // null '0xe83922'
});

// getBalance
vap.sendAsync({
  method: 'vap_getBalance',
  params: ['0x5c517fffeacc03caaa8f0aa5722168b9ab3fb7a1', 'latest'],
}, (err, gasPrice) => {
  // null '0x5483de922'
});
```

## About

This simple module allows you to query the Vapory RPC layer at a very low level. You must specify your data payload method and params, if any. The module will handle payload RPC ids.

## Contributing

Please help better the ecosystem by submitting issues and pull requests to `vapjs-rpc`. We need all the help we can get to build the absolute best linting standards and utilities. We follow the AirBNB linting standard and the unix philosophy.

## Guides

You'll find more detailed information on using `vapjs-rpc` and tailoring it to your needs in our guides:

- [User guide](docs/user-guide.md) - Usage, configuration, FAQ and complementary tools.
- [Developer guide](docs/developer-guide.md) - Contributing to `vapjs-rpc` and writing your own code and coverage.

## Help out

There is always a lot of work to do, and will have many rules to maintain. So please help out in any way that you can:

- Create, enhance, and debug vapjs rules (see our guide to ["Working on rules"](./github/CONTRIBUTING.md)).
- Improve documentation.
- Chime in on any open issue or pull request.
- Open new issues about your ideas for making `vapjs-rpc` better, and pull requests to show us how your idea works.
- Add new tests to *absolutely anything*.
- Create or contribute to ecosystem tools, like modules for encoding or contracts.
- Spread the word.

Please consult our [Code of Conduct](CODE_OF_CONDUCT.md) docs before helping out.

We communicate via [issues](https://github.com/vapjs/vapjs-rpc/issues) and [pull requests](https://github.com/vapjs/vapjs-rpc/pulls).

## Important documents

- [Changelog](CHANGELOG.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [License](https://raw.githubusercontent.com/vapjs/vapjs-rpc/master/LICENSE)

## Licence

This project is licensed under the MIT license, Copyright (c) 2016 Nick Dodson. For more information see LICENSE.md.

```
The MIT License

Copyright (c) 2016 Nick Dodson. nickdodson.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
