# Practical Numerical Analysis

`pengfei.jiang2018@gmail.com`

This note discuss the problem of numerical analysis in a practical context, particularly, in terms of accuracy derivation and choice of data type. The note intensively referes to [An Introduction to Numerical Analysis](http://www.nsc.ru/interval/Library/ApplBooks/InNumAnal.pdf) by [Arnold Neumaier](https://www.mat.univie.ac.at/~neum/).

## Typical data types

Algorithm design for application specified integrated circuit (ASIC) requires proper choice of data type, expecially, fixed point or float point data with base 2.

A fixed point data format can be declared `fixed<unsigned int W, int I, bool S>`. A float point data format consists of two fixed point data`float = MAN * 2^-EXP`, with mantissa `MAN = fixed<MW, MI, MS>` and exponent `EXP = fixed<EW, 0, ES>`. A determined data format corresponds to a set of discrete values it may represent: `[MIN, MIN + LSB, ... MAX - LSB, MAX]`. fixed point number has constant `LSB`, while float point number has variant `LSB`.

A functional data type requires a mapping rule from any number towards a representable number. The mapping rule consists of round-off rule for `MIN <= data <= MAX` and saturation rule for `data < MIN || data > MAX`. For simplicity, define the round-off rule as such:

* if `MIN <= data <= MAX`, drop the trailing bits. The result should equal the greatest representable number below or equal to `data`.

Saturation rule is tricky. Dropping leading bits is easy to implement but might make no sense mathematically. Thus designer should often avoid saturation by selecting proper bitwidth and/or rescaling the data in advance.

For floating point data type, always choose the representation with minimum sign bits. E.g. `1.00*2^-2 = 0.10 * 2^-1 = 0.01 * 2^-0`, but only the first representation is legal. For easy analysis, we ignore the *denormalized* case of `abs(data) < 2^-EXP_MAX`, e.g. `0.11 * 2^-EXP_MAX`, such that the mantissa is always full. It is the designer's responsibility to avoid such cases.

## Step, dynamic range, and accuracy

In this section, consdier `bool S = false`, i.e. all numbers are positive.

For fixed point data type
* `MIN = 0`
* `MAX = 2^I*(1-2^-W)`
* `LSB = 2^(I-W)`
* Worst absolute error `DELTA` equals `SETP`. E.g, a number `1.00111...` is mapped to three digits of `1.00`, with error approximate `0.01`
* Worst relative error `delta` indefinite. E.g a number `0.001` is mapped to `0.00`.
* Particularly, if the data format is filled, the worst `delta` is (slightly lower than) `2^(1-W)`, e.g `1.00111...` is mapped to `1.00` with relative error of `0.00111... / 1.00111...`, roughly `0.01 = 2^(1-3)`

For float point data type
* `MIN = 0`
* Minimum positive value is `2^(I-1-EXP_MAX) = 2^(I - (2^EXPW))` (mantissa is always full)
* `MAX = 2^I*(1-2^-W)` (since `EXP_MIN = 0`)
* `LSB = 2^(I-W-EXP)` is indefinite
* Worst absolute error `DELTA` equals `LSB` is indefinite
* Worst relative error is fixed to `2^(I-W)` (mantissa is always full)

Thus fixed point data has worst fixed error determined, and float point data has worst relative error determined.

Error varies according to data. E.g. suppose the data happens to match a representable value, it has zero eror. The worst error is emphasized here because it marks the performance lower bound. In specific context, stats or error, might be of interest, yet still hard to analyze.

## Typical computations




