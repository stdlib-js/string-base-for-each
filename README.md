<!--

@license Apache-2.0

Copyright (c) 2023 The Stdlib Authors.

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

# forEach

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Invokes a function for each UTF-16 code unit in a string.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import forEach from 'https://cdn.jsdelivr.net/gh/stdlib-js/string-base-for-each@deno/mod.js';
```

#### forEach( str, clbk\[, thisArg ] )

Invokes a function for each UTF-16 code unit in a string.

```javascript
function log( value, index ) {
    console.log( '%d: %s', index, value );
}

forEach( 'Beep!', log );
/* =>
    0: B
    1: e
    2: e
    3: p
    4: !
*/
```

The invoked function is provided three arguments:

-   **value**: character.
-   **index**: character index.
-   **str**: input string.

To set the function execution context, provide a `thisArg`.

```javascript
function clbk() {
    this.count += 1;
}

var str = '👉🏿';

var ctx = {
    'count': 0
};

forEach( str, clbk, ctx );

var cnt = ctx.count;
// returns 4
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import forEach from 'https://cdn.jsdelivr.net/gh/stdlib-js/string-base-for-each@deno/mod.js';

function log( value, index ) {
    console.log( '%d: %s', index, value );
}

forEach( 'presidential election', log );
forEach( 'Iñtërnâtiônàlizætiøn', log );
forEach( '🌷🍕', log );
forEach( '\uD834\uDD1E', log );
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/string-base-for-each.svg
[npm-url]: https://npmjs.org/package/@stdlib/string-base-for-each

[test-image]: https://github.com/stdlib-js/string-base-for-each/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/string-base-for-each/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/string-base-for-each/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/string-base-for-each?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/string-base-for-each.svg
[dependencies-url]: https://david-dm.org/stdlib-js/string-base-for-each/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/string-base-for-each/tree/deno
[umd-url]: https://github.com/stdlib-js/string-base-for-each/tree/umd
[esm-url]: https://github.com/stdlib-js/string-base-for-each/tree/esm
[branches-url]: https://github.com/stdlib-js/string-base-for-each/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/string-base-for-each/main/LICENSE

</section>

<!-- /.links -->
