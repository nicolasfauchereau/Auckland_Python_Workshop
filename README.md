# Python for Climate and Meteorological Data Analysis and Visualisation

[NIWA Auckland](http://www.niwa.co.nz/) / Climate and Weather Applications, Forecasting Services
Auckland, New Zealand, 31 August and 1 September 2017

Contact:

Nicolas Fauchereau

+ [@gmail](mailto:Nicolas.Fauchereau@gmail.com)
+ [@niwa](mailto:Nicolas.Fauchereau@niwa.co.nz)

<hr size=5>

### Table of contents

- [The Anaconda python distribution](#the-anaconda-python-distribution)
- [Installation of Some additional libraries](#installation-of-additional-libraries)
- [Running the Jupyter notebooks](#running-the-jupyter-notebooks)

<hr size=5>

## The Anaconda python distribution

For this tutorial, I **strongly** recommend installing the **Anaconda Python distribution**. It is a completely free enterprise-ready Python distribution for large-scale data processing, predictive analytics, and scientific computing. It includes the python interpreter itself, the python standard library as well as a set of packages exposing data structures and methods for data manipulation and scientific computing and visualization. In particular it provides [Numpy](http://www.numpy.org/), [Scipy](http://www.scipy.org/), [Pandas](http://pandas.pydata.org/), [Matplotlib](http://matplotlib.org/), etc ... i.e. all the main packages we will be using during the tutorial. The full list of packages is available at:

[http://docs.continuum.io/anaconda/pkgs.html](http://docs.continuum.io/anaconda/pkgs.html)

The Anaconda python distribution (**NOTE**: select the version shipping with Python 3.6) must be downloaded from:

[http://continuum.io/downloads](http://continuum.io/downloads)

For your platform.

Once you have installed Anaconda, you can update to the latest compatible versions of all the pre-installed packages by running (at the command line, i.e. in Windows(r) select `Cmd.exe`, on Mac the `Terminal` application in `Utilities`):

```
$ conda update conda
```

Then

```
$ conda update anaconda
```

You also might want to install [pip](https://github.com/pypa/pip) to install packages from the [Python Package Index](http://pypi.python.org/pypi).

```
$ conda install pip
```

## Installation of additional libraries

### netcdf4

[netcdf4](https://github.com/Unidata/netcdf4-python) allows you to read and write netcdf files (version 3 and 4 supported), install it by:

```
$ conda install netcdf4
```

### Basemap

**Basemap** is a graphic library for plotting (static, publication quality) geographical maps (see [http://matplotlib.org/basemap/](http://matplotlib.org/basemap/)). **Basemap** is available directly in **Anaconda** using the conda package manager, install with:

```
$ conda install basemap
```

### Seaborn

[seaborn](http://web.stanford.edu/~mwaskom/software/seaborn/) is a Python visualization library based on matplotlib. It provides a high-level interface for drawing attractive statistical graphics. You should be able to install it with ```conda``` as well:

```
$ conda install seaborn
```
### xarray

[xarray](https://github.com/xarray/xarray) (previously *xray*) is a library aimed at bringing the power of Pandas to multidimensional labelled arrays, such as the ones usually associated with geophysical quantities varying along time and space dimensions (e.g. [time, latitudes, longitudes], [time, level, latitudes, longitudes], etc) and supports reading and writing netcdf files. It can be installed via `conda`:

```
$ conda install xarray
```

## Running the Jupyter notebook
