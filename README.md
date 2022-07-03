<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# fmtprodmsg

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Format an error message for production.

<section class="installation">

## Installation

```bash
npm install @stdlib/error-tools-fmtprodmsg
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

</section>

<section class="usage">

## Usage

```javascript
var fmtprodmsg = require( '@stdlib/error-tools-fmtprodmsg' );
```

#### fmtprodmsg( code, ...args )

Formats an error message for production.

```javascript
var msg = fmtprodmsg( '27', 'foo', 'bar' );
// returns 'https://stdlib.io/e/27?arg[]=foo&arg[]=bar'
```

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var fmtprodmsg = require( '@stdlib/error-tools-fmtprodmsg' );

var msg = fmtprodmsg( '3', 'foo' );
// returns 'https://stdlib.io/e?code=3&arg[]=foo'

msg = fmtprodmsg( '5', 'foo', 'bar' );
// returns 'https://stdlib.io/e/5?arg[]=foo&arg[]=bar'

msg = fmtprodmsg( '5', 'foo', 'bar', 123 );
// returns 'https://stdlib.io/e/5?arg[]=foo&arg[]=bar&arg[]=123'
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/error-tools-fmtprodmsg.svg
[npm-url]: https://npmjs.org/package/@stdlib/error-tools-fmtprodmsg

[test-image]: https://github.com/stdlib-js/error-tools-fmtprodmsg/actions/workflows/test.yml/badge.svg?branch=v0.0.2
[test-url]: https://github.com/stdlib-js/error-tools-fmtprodmsg/actions/workflows/test.yml?query=branch:v0.0.2

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/error-tools-fmtprodmsg/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/error-tools-fmtprodmsg?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/error-tools-fmtprodmsg.svg
[dependencies-url]: https://david-dm.org/stdlib-js/error-tools-fmtprodmsg/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/error-tools-fmtprodmsg/tree/deno
[umd-url]: https://github.com/stdlib-js/error-tools-fmtprodmsg/tree/umd
[esm-url]: https://github.com/stdlib-js/error-tools-fmtprodmsg/tree/esm
[branches-url]: https://github.com/stdlib-js/error-tools-fmtprodmsg/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/error-tools-fmtprodmsg/main/LICENSE

</section>

<!-- /.links -->
