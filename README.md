The arithmetic package
======================

The [arithmetic package][] is a [Haskell][] library of natural number
arithmetic, including:

- Montgomery multiplication
- The Miller-Rabin primality test
- Lucas sequences
- The Williams p+1 factorization method
- Continued fraction representations of natural number square roots
- The Jacobi symbol
- The Tonelli-Shanks algorithm for finding square roots modulo a prime
- The Chakravala method for solving the Pell equation

This software is released under the [MIT License][].

Install
-------

Installing the arithmetic package requires [cabal][]:

    git clone https://github.com/gilith/arithmetic.git
    cd arithmetic
    cabal install --enable-tests

Test
----

Use [cabal][] to run the test suite:

    cabal test

Run
----

The arithmetic package contains an executable called arithmetic, which
is run as follows:

    Usage: arithmetic OPERATION [OPTION...]
      -a ALGORITHM    select algorithm
      -n NATURAL      select n parameter
      -x NATURAL      select x parameter
      -k NATURAL      select k parameter
    where OPERATION is one of {factor,modexp,timelock},
      ( factor.........factorize n                       )
      ( modexp.........compute (x ^ k) `mod` n           )
      ( timelock.......compute (x ^ 2 ^ k) `mod` n       )
    ALGORITHM is one of {modular,montgomery,williams},
      ( modular........naive modular arithmetic          )
      ( montgomery.....Montgomery multiplication         )
      ( williams.......Williams p+1 factorization method )
    and NATURAL is either a natural number or has the form [bitwidth].

[cabal]: https://www.haskell.org/cabal/ "Cabal"
[Haskell]: https://www.haskell.org/ "Haskell"
[arithmetic package]: https://hackage.haskell.org/package/arithmetic "arithmetic package"
[MIT License]: https://github.com/gilith/arithmetic/blob/master/LICENSE "MIT License"
