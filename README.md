# pyhsmm-autoregressive
Modified version of `mattjj`'s `pyhsmm-autoregressive`, which allows HSMM fitting with autoregressive emissions.

## Installation
1. Clone the repository
    ```bash
    git clone git://github.com/bccho/pyhsmm-autoregressive.git autoregressive
    ```
2. Install with your favorite method (e.g. `python setup.py develop` for developer mode)

## Note about Cythonization
* The compiled code component is optional (it can be turned off with the `--no-compile` flag; see `setup.py` for details)
* Compilation currently requires GCC (for its OpenMP support). Recent versions of Clang (3.7.0 and later) also support OpenMP but require the flag `-fopenmp=libomp`. See [Issue #4](https://github.com/mattjj/pyhsmm-autoregressive/issues/4).
* Compilation also requires C++ 11, so a GCC version of 4.8.1 or higher is required.
* If compilation succeeds but you see errors about `GOMP_parallel` or similar errors, ensure that your Python distribution has been compiled with the correct libraries. If you are not sure, compile CPython from source.
