<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# Absolute Value

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute an [absolute value][absolute-value] of a signed 32-bit integer.

<section class="intro">

The [absolute value][absolute-value] is defined as

<!-- <equation class="equation" label="eq:absolute_value" align="center" raw="|x| = \begin{cases} x & \textrm{if}\ x \geq 0 \\ -x & \textrm{if}\ x < 0\end{cases}" alt="Absolute value"> -->

```math
|x| = \begin{cases} x & \textrm{if}\ x \geq 0 \\ -x & \textrm{if}\ x < 0\end{cases}
```

<!-- <div class="equation" align="center" data-raw-text="|x| = \begin{cases} x &amp; \textrm{if}\ x \geq 0 \\ -x &amp; \textrm{if}\ x &lt; 0\end{cases}" data-equation="eq:absolute_value">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@dc413bd931fa2ac3d9d19d2cb44a08dbd5a3e9ad/lib/node_modules/@stdlib/math/base/special/labs/docs/img/equation_absolute_value.svg" alt="Absolute value">
    <br>
</div> -->

<!-- </equation> -->

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import labs from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-labs@deno/mod.js';
```

#### labs( x )

Computes an [absolute value][absolute-value] of a signed 32-bit integer.

```javascript
var v = labs( -1|0 );
// returns 1

v = labs( 2|0 );
// returns 2

v = labs( 0|0 );
// returns 0
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   The implementation assumes two's complement.

-   In two's complement systems, the absolute value of the minimum signed 32-bit integer is out-of-range. The absolute value for the minimum signed 32-bit integer is thus undefined.

    ```javascript
    // -2^31
    var x = -2147483648|0;

    var v = labs( x );
    // returns -2147483648
    ```

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@deno/mod.js';
import round from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-round@deno/mod.js';
import labs from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-labs@deno/mod.js';

var x;
var i;

for ( i = 0; i < 100; i++ ) {
    x = round( randu() * 100.0 ) - 50;
    console.log( 'abs(%d) = %d', x, labs( x|0 ) );
}
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math-base/special/abs`][@stdlib/math/base/special/abs]</span><span class="delimiter">: </span><span class="description">compute the absolute value of a double-precision floating-point number.</span>

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-labs.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-labs

[test-image]: https://github.com/stdlib-js/math-base-special-labs/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-special-labs/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-labs/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-labs?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-labs.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-labs/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-labs/tree/deno
[umd-url]: https://github.com/stdlib-js/math-base-special-labs/tree/umd
[esm-url]: https://github.com/stdlib-js/math-base-special-labs/tree/esm
[branches-url]: https://github.com/stdlib-js/math-base-special-labs/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-labs/main/LICENSE

[absolute-value]: https://en.wikipedia.org/wiki/Absolute_value

<!-- <related-links> -->

[@stdlib/math/base/special/abs]: https://github.com/stdlib-js/math-base-special-abs/tree/deno

<!-- </related-links> -->

</section>

<!-- /.links -->
