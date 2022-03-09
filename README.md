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

# formatProdErrorMessage

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

</section>

<section class="usage">

## Usage

```javascript
var formatProdErrorMessage = require( '@stdlib/error-tools-fmtprodmsg' );
```

#### formatProdErrorMessage( code, ...args )

Formats an error message for production.

```javascript
var msg = formatProdErrorMessage( '27', 'foo', 'bar' );
// returns 'Minified stdlib error code: 27. Visit https://stdlib.io/docs/api/latest/error-decoder.html?code=27&arg[]=foo&arg[]=bar for the full message.'
```

#### formatProdErrorMessage.factory( options )

Returns a `function` which formats an error message for production.

```javascript
var opts = {};
var fcn = formatProdErrorMessage.factory( opts );
// returns <Function>

var msg = fcn( '3' );
// returns 'Minified stdlib error code: 3. Visit https://stdlib.io/docs/api/latest/error-decoder.html?code=3 for the full message.'
```

The function accepts the following `options`:

-   **url**: website URL for full error message.
-   **message**: error message template with `{{url}}` and `{{code}}` placeholders that will be replaced.

To set a custom URL, use the `url` option:

```javascript
var opts = {
    'url': 'https://stdlib.io/error-decoder.html'
};

var fcn = formatProdErrorMessage.factory( opts );
// returns <Function>

var msg = fcn( '8' );
// returns 'Minified stdlib error code: 8. Visit https://stdlib.io/error-decoder.html?code=8 for the full message.'
```

To change the error message template, use the `message` option:

```javascript
var opts = {
    'message': 'Error code: {{code}}. See: {{url}}.'
};

var fcn = formatProdErrorMessage.factory( opts );
// returns <Function>

var msg = fcn( '27', 'foo', 'bar' );
// returns 'Error code: 27. See: https://stdlib.io/docs/api/latest/error-decoder.html?code=27&arg[]=foo&arg[]=bar.'
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var formatProdErrorMessage = require( '@stdlib/error-tools-fmtprodmsg' );

var msg = formatProdErrorMessage( '3', 'foo' );
// returns 'Minified stdlib error code: 3. Visit https://stdlib.io/docs/api/latest/error-decoder.html?code=3&arg[]=foo for the full message.'

msg = formatProdErrorMessage( '5', 'foo', 'bar' );
// returns 'Minified stdlib error code: 5. Visit https://stdlib.io/docs/api/latest/error-decoder.html?code=5&arg[]=foo&arg[]=bar for the full message.'

msg = formatProdErrorMessage( '5', 'foo', 'bar', 123 );
// returns 'Minified stdlib error code: 5. Visit https://stdlib.io/docs/api/latest/error-decoder.html?code=5&arg[]=foo&arg[]=bar&arg[]=123 for the full message.'
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

[test-image]: https://github.com/stdlib-js/error-tools-fmtprodmsg/actions/workflows/test.yml/badge.svg?branch=v0.0.1
[test-url]: https://github.com/stdlib-js/error-tools-fmtprodmsg/actions/workflows/test.yml?query=branch:v0.0.1

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

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/error-tools-fmtprodmsg/main/LICENSE

</section>

<!-- /.links -->
