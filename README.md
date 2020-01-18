jslong
========

[![Build Status](https://travis-ci.org/modern-dev/jslong.svg?branch=master)](https://travis-ci.org/modern-dev/jslong)
[![codecov](https://codecov.io/gh/modern-dev/jslong/branch/master/graph/badge.svg)](https://codecov.io/gh/modern-dev/jslong)
![npm](https://img.shields.io/npm/v/@modern-dev/jslong)
![NPM](https://img.shields.io/npm/l/@modern-dev/jslong)

The `jslong` - is a pure JavaScript implementation of Long class for representing a 64-bit two's-complement integer value.

```shell script
$ npm install -save @modern-dev/jslong
```

## :clipboard: Usage

```js
import { Long } from '@modern-dev/jslong';

const val = Long.getMinValue().subtract(Long.fromInt(1024)).toString(16);
console.log(val); // '7ffffffffffffc00'

```

## :mortar_board: API Reference

### Constructor
```typescript
/**
 * @param {number} low  The low (signed) 32 bits of the long.
 * @param {number} high  The high (signed) 32 bits of the long.
 */
constructor(low: number, high: number)
```

### Methods

| Method signature | Description |
| --- | --- |
| `toInt(): number` | The value, assuming it is a 32-bit integer. |
| `toNumber(): number` | The closest floating-point representation to this value. |
| `isSafeInteger(): boolean` | if can be exactly represented using number (i.e. abs(value) < 2^53). |
| `toString(radix?: number): string` | The textual representation of this value. |
| `getHighBits(): number` | The high 32-bits as a signed value. |
| `getLowBits(): number` | The low 32-bits as a signed value. |
| `getLowBitsUnsigned(): number` | The low 32-bits as an unsigned value. |
| `getNumBitsAbs(): number` | Returns the number of bits needed to represent the absolute value of this *Long*. |
| `isZero(): boolean` | Whether this value is zero. |
| `isNegative(): boolean` | Whether this value is negative. |
| `isOdd(): boolean` | Whether this value is odd. |
| `equals(other: Long): boolean` | Whether this Long equals the other. |
| `notEquals(other: Long): boolean` | Whether this Long does not equal the other. |
| `lessThan(other: Long): boolean` | Whether this Long is less than the other. |
| `lessThanOrEqual(other: Long): boolean` | Whether this Long is less than or equal to the other. |
| `greaterThan(other: Long): boolean` | Whether this Long is greater than the other. |
| `greaterThanOrEqual(other: Long): boolean` | Whether this Long is greater than or equal to the other. |
| `compare(other: Long): number` | 0 if they are the same, 1 if the this is greater, and -1 if the given one is greater. |
| `negate(): Long` | The negation of this value. |
| `add(other: Long): Long` | The sum of this and the given Long. |
| `subtract(other: Long): Long` | The difference of this and the given Long. |
| `multiply(other: Long): Long` | The product of this and the other. |
| `div(other: Long): Long` | This Long divided by the given one. |
| `modulo(other: Long): Long` | This Long modulo the given one. |
| `not(): Long` | The bitwise-NOT of this value. |
| `and(other: Long): Long` | The bitwise-AND of this and the other. |
| `or(other: Long): Long` | The bitwise-OR of this and the other. |
| `xor(other: Long): Long` | The bitwise-XOR of this and the other. |
| `shiftLeft(numBits: number): Long` | This shifted to the left by the given amount. |
| `shiftRight(numBits: number): Long` | This shifted to the right by the given amount. |
| `shiftRightUnsigned(numBits: number): Long` | This shifted to the right by the given amount, with zeros placed into the new leading bits. |
| `static fromInt(value: number): Long` | The corresponding Long value. |
| `static fromNumber(value: number): Long` | The corresponding Long value. |
| `static fromBits(lowBits: number, highBits: number): Long` | The corresponding Long value. |
| `static fromString(str: string, opt_radix?: number): Long` | The corresponding Long value. |
| `static isStringInRange(str: string, opt_radix: number): boolean` | Whether the string is within the range of a Long. |

## :green_book: License

[Licensed under the Apache License 2.0.](https://github.com/modern-dev/jslong/blob/master/LICENSE)

Based on the [Long implementation](https://github.com/google/closure-library/blob/e7bfe67bf37f5df41f4b0bbab1724ad1272fca66/closure/goog/math/long.js#L82) for Google's [Closure Library](https://github.com/google/closure-library).

Copyright 2009 The Closure Library Authors. All Rights Reserved.

Copyright (c) 2020 Bohdan Shtepan

---

> [modern-dev.com](http://modern-dev.com) &nbsp;&middot;&nbsp;
> GitHub [@virtyaluk](https://github.com/virtyaluk) &nbsp;&middot;&nbsp;
> Twitter [@virtyaluk](https://twitter.com/virtyaluk)
