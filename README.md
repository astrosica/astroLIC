# astroLIC

An implementation of [`LicPy`](https://rufat.be/licpy/) using astronomical polarimetry. An example is given in a Jupyter notebook which reproduces Figure 3 in Campbell et al. (2020).

## Dependencies

Required packages for `LicPy`:
* [pybind11](https://pypi.org/project/pybind11/)
* [tensorflow](https://www.tensorflow.org/)
* [matplotlib](https://matplotlib.org/3.1.1/index.html)
* [pytest](https://docs.pytest.org/en/stable/contents.html)
* [sympy](https://www.sympy.org/en/index.html)

Additional required packages for `astroLIC`:

* [numpy](https://numpy.org/)
* [aplpy](https://aplpy.github.io/index.html)
* [astropy](https://www.astropy.org/)

There is currently a bug with using the latest version of `tensorflow` that results in the error `AttributeError: module 'tensorflow' has no attribute 'placeholder'` when running `LicPy`. To work around this, you'll want to open the `lic.py` file; for me this is located in `/opt/anaconda3/lib/python3.7/site-packages/licpy-0.2-py3.7-macosx-10.9-x86_64.egg/licpy/`. When the error is raised, you should be able to read off the directory that is causing the error. Then, simply change `import tensorflow as tf` to the following:

`import tensorflow.compat.v1 as tf
tf.disable_v2_behavior()`.

## Installation

TBA.

## Usage

`astroLIC(I_dir,Q_dir,U_dir,length=0.25,toIAU=False,wcs=True)`

## Notes

This is a particular implementation of LIC meant for astronomical polarimetry which uses a specific coordinate system (IAU convention) not used in many other data sets. Therefore, `astro-LIC` is only meant to be used for astronomical polarization data and will not provide the correct orientation if used with other data sets.
