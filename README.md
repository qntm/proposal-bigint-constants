# ECMAScript Proposal: BigInt constants for mathematics

**Stage:** 0

**Author:** qntm

## Summary

A *mathematical constant* is a real number with a fixed and unambiguously defined value which is used, and useful, across multiple mathematical problems. Examples of mathematical constants are:

* *e*, the base of the natural logarithm, equal to 2.7182818284590452353602874713527...
* *ln*(10), the natural logarithm of 10, equal to 2.3025850929940456840179914546844...
* *ln*(2), the natural logarithm of 2, equal to 0.69314718055994530941723212145818...
* *log*(*e*), the base 10 logarithm of *e*, equal to 0.43429448190325182765112891891661...
* *log*<sub>2</sub>(*e*), the base 2 logarithm of *e*, equal to 1.4426950408889634073599246810019...
* *π*, the ratio of a circle's circumference to its diameter, equal to 3.1415926535897932384626433832795...
* √½, the square root of one-half, equal to 0.70710678118654752440084436210485...
* √2, the square root of 2, equal to 1.4142135623730950488016887242097...

In order to carry out mathematics using ECMAScript it is advantageous to be able to make use of mathematical constants. As a result, ECMAScript's `Math` object has, since the [very earliest versions of the programming language](https://ecma-international.org/wp-content/uploads/ECMA-262_1st_edition_june_1997.pdf), exposed [the following respective value properties](https://tc39.es/ecma262/multipage/numbers-and-dates.html#sec-value-properties-of-the-math-object), which have the following exact values:

* `Math.E` = 2.718281828459045090795598298427648842334747314453125
* `Math.LN10` = 2.30258509299404590109361379290930926799774169921875
* `Math.LN2` = 0.69314718055994528622676398299518041312694549560546875
* `Math.LOG10E` = 0.43429448190325181666793241674895398318767547607421875
* `Math.LOG2E` = 1.442695040888963387004650940070860087871551513671875
* `Math.PI` = 3.141592653589793115997963468544185161590576171875
* `Math.SQRT1_2` = 0.70710678118654757273731092936941422522068023681640625
* `Math.SQRT2` = 1.4142135623730951454746218587388284504413604736328125

Note that these values are, of necessity, *approximated*. They are not exactly equal to the actual mathematical constants, because the constants are all irrational and therefore impossible to represent as IEEE 754 64-bit floating point numbers. Despite this, these approximate values are still useful for doing mathematics in ECMAScript.

However, as of [ECMAScript 2020](https://tc39.es/ecma262/2020/), ECMAScript has a second numeric type, alongside the IEEE 754 64-bit floating point number: the BigInt.

Therefore, for symmetry, this proposal introduces a corresponding collection of mathematical constants for use with BigInt calculations. Again, these values are, of necessity, approximated. They are as follows:

* `BigInt.E` = 3
* `BigInt.LN10` = 2
* `BigInt.LN2` = 1
* `BigInt.LOG10E` = 0
* `BigInt.LOG2E` = 1
* `BigInt.PI` = 3
* `BigInt.SQRT1_2` = 1
* `BigInt.SQRT2` = 1

### But seriously though

When do we get `BigInt.abs()` and `BigInt.sign()`? Please? Yes, I can write these two-and-a-half lines of code myself every time but it's frankly humiliating.
