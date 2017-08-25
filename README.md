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

You should not need administrator rights, as Anaconda is completely self-contained and can be installed in your `HOME` directory. I suggest installing `Anaconda` in `/Users/USERNAME/anaconda` on Macs, and `C:\Users\USERNAME\anaconda` on Windows

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

All of this can also be done using the Anaconda Navigator GUI (Graphical User Interface) which looks like below

![](https://github.com/nicolasfauchereau/Auckland_Python_Workshop/raw/master/images/navigator.png)

If you go the `Environments` tab on the left, and select the `root` environment (we will talk about the concept of Python environments later in the workshop) you can then search, select and install available packages, including the ones mentionned above.


## Running the Jupyter notebook

The material of the tutorial is in the form of [Jupyter notebooks](http://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html). In a nutshell a Jupyter notebook is a web-based (i.e. running in the browser) interactive computational environment where you can combine Python code execution, text, rendered mathematic expression, plots, images, and rich media into a **single document**.

It is in my opinion the best environment when you are doing **exploratory data analysis**, and it allows you to weave comments, background information, interpretations and references along with the code itself, and it can be exported to a variety of formats (HTML, pdf) for sharing with colleagues. I **strongly** recommend spending some time learning about the notebook and its many features.

After uncompressing the archive of the repo (or after cloning it with ```git```), navigate to the `notebooks` directory (containing the ```*.ipynb``` files) and type:

```
$ jupyter notebook
```

That should bring up the Jupyter notebook dashboard (looking as below) in your default Browser, you should be ready to go !

![](https://github.com/nicolasfauchereau/Auckland_Python_Workshop/raw/master/images/jupyter_dashboard.png)

## contents

+ `test.ipynb`: 

  A simple test Jupyter notebook to test the installation of the main libraries and their version 

+ `Jupyter_notebook`: 

  Introduction to the main features of the **Jupyter notebook **

+ `introduction_python.ipynb`: Introduction the **basics** of the python language:

  + what's an *interpreted programming language*, what is the python *interpreter*
  + how to write a python script
  + basic native data types 
    + dealing with numbers in native Python 
    + dealing with `strings` and their formatting 
    + `lists`, `tuples`, `dictionnaries`, ...
  + arithmetic operators (`+. -, *, =`)
  + logical operators (`==, >=, <=, !=`) and how they relate to booleans (`True / False`)
  + control flow structures (`for, if / elif / else, while` etc.)
  + reusing your code: writing *functions*, *modules* and *packages*

+ `Numpy.ipynb`: 

  A introduction to Numpy: numpy introduces in particular a data structure called the `ndarray` (*N-dimensional* array) which can store numerical values. It is the foundational library of the Python scientific *ecosystem*. In this notebook we'll learn the main principles of manipulating numpy *ndarrays*. While you might actually not spend much time dealing with numpy itself, it is necessary to understand its basic principles, as (almost) everything else in scientific Python is built on top of `numpy`.

  + how to create numpy arrays 
  + indexing, slicing, reshaping, transposing, etc. 
  + main methods and functions in numpy operating on numpy `ndarrays`

+ `plotting.ipynb`:

  In this notebook we'll go over the basics of **Matplotlib**, the main plotting library in python. This is more or less the equivalent of *numpy* but for plotting: *i.e.* this is the main foundational library of the Python Scientific ecosystem. A number of — more specialised — plotting libraries have been built on top of Matplotlib. One we will briefly go over in particular is *seaborn*, a plotting library handy for statistical plots. A short and non-exhaustive list of plotting libraries in Python is provided covering both static plots (i.e. *plotnine*, *altair*, etc) and interactive plots (*bokeh*, *plotly*, *holoviews*, etc)

+ `mapping.ipynb`: 

  Making maps in Python: a brief overview of **basemap**, **cartopy**, and — for interactive maps — **folium**. We'll see also briefly how to read shapefiles (with [geopandas](http://geopandas.org/)), transform into a [geojson](http://geojson.org/) and edit in the browser. 

  ​

+ `pandas.ipynb`

  This is where we're gonna spend quite a bit of time ! [Pandas](http://pandas.pydata.org/) is **THE** library that you need to use when dealing with *tabular* data, *i.e.* "spreadsheet-like" data, where data is stored in 2D arrays with rows and column labels, the type of data you find in csv, tab-delimited or space-delimited or Excel files.

  ​