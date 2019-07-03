# Microbenchmarks

This is a collection of micro-benchmarks used to compare Julia's performance against
that of other languages.
It was formerly part of the Julia source tree.
The results of these benchmarks are used to generate the performance graph on the
[Julia homepage](https://julialang.org) and the table on the
[benchmarks page](https://julialang.org/benchmarks).

## To do:

This fork should try to fix some shortcomings in the original analysis.

  1. Improve Python code as described in [this
     post](https://www.ibm.com/developerworks/community/blogs/jfp/entry/Python_Meets_Julia_Micro_Performance?lang=en).
  1. Further improve Python code by using `transonic.jit`, `numba.njit` which
     do not require invasive changes to the code.
  1. Include PyPy3 to the list, allowing numpy to work with it.
  1. Update LuaJIT code, replacing scilua (abandoned?) with [Lunatic Python](https://labix.org/download/lunatic-python/) or
     [Lupa](https://github.com/scoder/lupa).
  1. Perf tune before benchmarks to reduce system jitter.
  1. Test the microbenchmarks for larger array sizes as done
     [here](https://www.ibm.com/developerworks/community/blogs/jfp/entry/A_Comparison_Of_C_Julia_Python_Numba_Cython_Scipy_and_BLAS_on_LU_Factorization?lang=en).
  1. Publish a blog post ;)

## Running benchmarks

This repository assumes that Julia has been built from source and that there exists
an environment variable `JULIAHOME` that points to the root of the Julia source tree.
This can also be set when invoking `make`, e.g. `make JULIAHOME=path/to/julia`.

To build binaries and run the benchmarks, simply run `make`.
Note that this refers to GNU Make, so BSD users will need to run `gmake`.

## Included languages:

* C
* Fortran
* Go
* Java
* JavaScript
* Julia
* LuaJIT
* Mathematica
* Matlab
* Python
* R
* Rust
* Scala
* Stata
