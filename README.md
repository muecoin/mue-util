# mue-util

[![npm version](https://img.shields.io/npm/v/mue-util.svg)](https://www.npmjs.com/package/muecoin/mue-util)
[![Build Status](https://travis-ci.org/muecoin/mue-util.svg?branch=master)](https://travis-ci.org/muecoin/mue-util)
[![Dependency Status](https://david-dm.org/muecoin/mue-util.svg)](https://david-dm.org/muecoin/mue-util)

**Utility functions for MonetaryUnit hashes and targets**

## Usage

`npm install muecoin/mue-util`

### Methods

#### `toHash(hex)`

Takes a hex string that contains a MonetaryUnit hash as input, and returns a MonetaryUnit-protocol-friendly little-endian Buffer. Throws an error if the hex string is not of length 64 (representing a 256-bit hash).

#### `compressTarget(target)`

Converts the difficulty target `target` to its compact representation (used in the "bits" field in block headers). `target` should be a `Buffer` (little-endian, the zeroes should be at the end). Returns a `number`.

#### `expandTarget(bits)`

Converts the compressed target integer `bits` to its target hash representation. Returns a `Buffer`.
