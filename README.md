# astro-LIC

Applies Line Integral Convolution (LIC) to astronomical polarimetry. 

## Description

An astronomical implementation of [`LicPy`](https://rufat.be/licpy/) using Stokes polarization maps.

## Dependencies

Required packages for `LicPy`:
* pybind11
* tensorflow
* matplotlib
* pytest
* sympy

Additional required packages for `astro-LIC`:

* numpy
* aplpy
* astropy

## Installation

TBA.

## Running the code

TBA.

## Notes

This is a particular implementation of LIC meant for astronomical polarimetry which uses a specific coordinate system (IAU convention) not used in many other data sets. Therefore, `astro-LIC` is only meant to be used for astronomical polarization data and will not provide the correct orientation if used with other data sets.
