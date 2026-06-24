Bitcore Library (Zero)
======================

[![NPM Package](https://img.shields.io/npm/v/bitcore-lib.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-lib)

A pure and powerful JavaScript library for the Zero (ZER) chain. `bitcore-lib-zero`
is the lowest layer of the Zero Insight stack: it provides addresses, transactions,
scripts, and serialization primitives that `bitcore-node-zero` and `insight-api-zero`
build on. It is a fork of BitPay's `bitcore-lib`, retargeted to Zero's parameters.

> Source-of-record copy. This README is the corrected version staged under
> `error/bitcore-lib-zero/` in the Insight docs repo: dead upstream links pruned
> and the generic-Bitcoin framing replaced with the actual Zero usage.

Lineage: this is the Zero rename-fork of the Zcash Insight stack
([str4d/insight-api-zcash](https://github.com/str4d/insight-api-zcash),
[str4d/insight-ui-zcash](https://github.com/str4d/insight-ui-zcash)), itself
derived from BitPay's [bitcore-node](https://github.com/bitpay/bitcore-node) and
[bitcore-lib](https://github.com/bitpay/bitcore-lib).

## Get Started

```sh
npm install zerocurrencycoin/bitcore-lib-zero
```

```sh
bower install zerocurrencycoin/bitcore-lib-zero
```

This library is normally pulled in transitively when you install
`bitcore-node-zero`; install it directly only when developing against the
primitives.

## Documentation

The upstream BitPay [bitcore documentation](http://bitcore.io/guide/) and
[API reference](http://bitcore.io/api/) still describe the shared API surface.
Zero-specific differences (network magic, address version bytes, the Sapling/
shielded transaction fields) live in this fork's source, not in the upstream docs.

- [Developer Guide (upstream)](http://bitcore.io/guide/)
- [API Reference (upstream)](http://bitcore.io/api/)

## Examples

The upstream example set applies to the transparent-address API:

* [Generate a random address](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#generate-a-random-address)
* [Generate an address from a SHA256 hash](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#generate-a-address-from-a-sha256-hash)
* [Import an address via WIF](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#import-an-address-via-wif)
* [Create a Transaction](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#create-a-transaction)
* [Sign a message](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#sign-a-bitcoin-message)
* [Verify a message](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#verify-a-bitcoin-message)
* [Create an OP_RETURN transaction](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#create-an-op-return-transaction)
* [Create a 2-of-3 multisig P2SH address](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#create-a-2-of-3-multisig-p2sh-address)
* [Spend from a 2-of-2 multisig P2SH address](https://github.com/bitpay/bitcore-lib/blob/master/docs/examples.md#spend-from-a-2-of-2-multisig-p2sh-address)

## Security

Use common sense when handling anything related to finances; this code carries no
warranty. If you find a security issue in the Zero fork, report it to the
zerocurrencycoin maintainers via the repository issue tracker.

## Building the Browser Bundle

To build a full browser bundle:

```sh
gulp browser
```

This generates `bitcore-lib.js` and `bitcore-lib.min.js`.

## Development & Tests

```sh
git clone https://github.com/zerocurrencycoin/bitcore-lib-zero
cd bitcore-lib-zero
npm install
```

Run all the tests:

```sh
gulp test
```

You can also run just the Node.js tests with `gulp test:node`, just the browser
tests with `gulp test:browser`, or a coverage report (open
`coverage/lcov-report/index.html`) with `gulp coverage`.

> Built and tested under **Node.js v8.17.0**, matching the rest of the Zero Insight
> stack. The dependency tree is frozen circa 2021; newer Node is not supported.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore-lib/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.
