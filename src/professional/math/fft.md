# A note on FFT computations

## [Algebraic formation of the FFT](https://sci-hub.wf/10.1109/mcas.1981.6323745)

* eq 2: factorization of the size N into M factors
* eq 3/4: express n/k as a summation of M elements.
    * Consider n/k represented as multi digit number, each digit with its own carry rule; n/k have carry rule in reversed order
    * E.g. consider N = 6 = 2 x 3. k in {0...5} = (0, 0), (0, 1), (1, 0) ... (2, 1); where as n in {0...5} = (0, 0), (0, 1), (0, 2), ... (1, 2)
    * The carry out rule corresponds to the ordering of M factors, thus N options. Carry out rule is a bijection to number 0...N-1
* 10: rewrite product of nk as their carry version.

* 11: Some cross terms in the product of nk in carry version is multiple of N, thus can be ignored in periodic twiddle
    * Specificly, counting carry digit from 0 to M-1, if the sum of the rank pair of the carry digits is no less than M, then their cross term can be ignored.
    * E.g. for a factorization of 2, only 1+1 rank pair can be ignored; for a factorization of 5, 15 outof 25 digit pairs can be ignored
* eq 14: FFT can be performed factor by factor.
    * The FFT size N in twiddle denominator is replaced by `r_1`; the spectral index k is replaced with `k_1`

* eq 15,16: FFT on each factor takes previous stage with a prerotation

FFT algorithms expands the M dimensional N element array into one dimensional

**DIT algorithms: decimation in time**


* In place algorithms: each butterfly puts their output to the mem unit of the inputs
* T1: digit reverse/bit reverse. Perform stage FFT from the highest time digit to the lowest; Largest butterfly to the smallest butterfly
    * X(n0, n1, n2, n3, ...) => X(n0, n1, n2, ... k0)
* T2: flip inter/outer digit (expression `X_{m}^2(...)_c`, denote tensor rotation by `c`)

* Note how row/column expansion has symmetric butterfly graph

* Sequential algorithms: TODO
* T3: remove the 'in place' restriction: after each FFT, the k index is not placed to its n factor correspondence
    * X(n0, n1, n2, n3, ...) => X(n0, n1, n2, ... k0, k1, ...)
    * Decimation is performed stage by stage, instead of before/after all stages
    * Not practical: both io are in bit revsered order
* T4: column version of T3. Pratical, both io in sequential order
    * TODO lm is a function of m (at each stage, the data order changes?)
    * TODO consider X to be power of 2. At each stage, the X pairs with distance N/2 is always computed with the same butterfly

* T5: X(n0, n1, n2, n3, ...) => X(k0, k1, ... n0, n1, ...)
    * Not practical: both io are in bit revsered order
* T6: column version of T5 
    * At each stage, the X pairs with distance N/2 is always required as butterfly input, revsered from T4
* T7: X(km, ... k0, n0, n1, ...)
    * reversed digit input, sequential output
* T8: column version of T7

**Post multiplication algorithms**

**Other DIT algorithms**

* if computation is not restircted to one stage process in a FFT stage
* sequential input/output, identical computation geometry, variation of T4/T6
* By putting the active stage at last (data reordering)
    * X4(k0, k1, ... km, n0, n1, ...) => X4(k0, k1, ..., n0, n1, ... km)
* Sequential input, sequential output, and isogeometric

**Decimation in frequency algorithms**
