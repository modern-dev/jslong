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
*Will be added soon.*

## :green_book: License

[Licensed under the Apache License 2.0.](https://github.com/modern-dev/jslong/blob/master/LICENSE)

Based on the [Long implementation](https://github.com/google/closure-library/blob/e7bfe67bf37f5df41f4b0bbab1724ad1272fca66/closure/goog/math/long.js#L82) for Google's [Closure Library](https://github.com/google/closure-library).

Copyright 2009 The Closure Library Authors. All Rights Reserved.
Copyright (c) 2020 Bohdan Shtepan

---

> [modern-dev.com](http://modern-dev.com) &nbsp;&middot;&nbsp;
> GitHub [@virtyaluk](https://github.com/virtyaluk) &nbsp;&middot;&nbsp;
> Twitter [@virtyaluk](https://twitter.com/virtyaluk)