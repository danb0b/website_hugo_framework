---
type: submodule
title: Packages in Python
---

# Packages in Python

## Introduction

The most important packages that I use when creating python code are those packages which make a python more Matlab-like.

## Common Packages

### Numpy

<https://www.scipy.org/getting-started.html>

this package permits one to store and access data in arrays multidimensional arrays as one would do natively in Matlab. While python permits nested lists, the Paradigm of being able to slice multidimensional arrays of data, to index through it, too reshape and analyze it across dimensions in multiple ways is provided by this package

### Scipy

<https://docs.scipy.org/doc/scipy/reference/index.html>

Scipy complements numpy in that it permits low-level arrays defined in numpy to be analyzed across a wide array of linear algebra and scientific functions. The most notable packages with inside Pi include modules for integration, interpolation, linear algebra, optimization, nonlinear optimization, sparse matrices, spatial operations such as triangulation convex hole Etc and statistics

Module list: <https://docs.scipy.org/doc/scipy/reference/py-modindex.html>

### Matplotlib

Matplotlib is a package which permits the visualization of data, especially Ray base data used in numpy. matplotlib also provides an interface which is similar to Matlab, making it easy to make the transition between Matlab plotting and plotting in Python. Not live also permits object-oriented-style access to its structures in classes, making it possible to embed object-oriented style code and enhance it with plotting functionality. specialty modules within matplotlib start with pi plot, the scripted interface for creating python plots. Other modules which are worth noting are the path modules, which allow you to access complex geometric classes such as lines and polygons, and to program these shapes at a very low level in order to get the exact type of drawing you want. Another module within matplotlib which is worth knowing about is the color map capability, which allows you to specify and generate colors along a spectrum. A variety of Spectra are predefined, permitting you to ship the color of your plots for different uses very easily. Other common modules are the figure and axis modules, which provide access to the axis and figure classes. One of their module to know about is the image module, which allows you to display image data or bitmapdata and to operate on pictures and images within figures and plots.

[_https://matplotlib.org/tutorials/index.html_](https://matplotlib.org/tutorials/index.html)

Other things that you can do in that pot live include animation, simple interactions with data such as clicking and dragging, 3D plotting of all kinds including surfaces contour lines and custom triangulated data. you can do subplots in matplotlib just as you do with Matlab

## Other packages

| package                                             | Description / Use                                                                                                                                                       |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [python](https://docs.python.org/3/)                | Get Python 3                                                                                                                                                            |
| [numpy](http://docs.scipy.org/doc/numpy-dev/dev/)   | basic array types and operations                                                                                                                                        |
| [scipy](http://docs.scipy.org/doc/scipy/reference/) | huge, multipurpose numpy-enhancing package, covering many topics including optimization, matrix operations & linear algebra, spatial data, transforms, and integration. |
| [sympy]()                                           | symbolic equation manipulation                                                                                                                                          |
| [shapely]()                                         | 2d constructive solid geometry, based on libgeos                                                                                                                        |
| [matplotlib]()                                      | the definitive plotting tool for python                                                                                                                                 |
| pyqt / pyside                                       | QT GUI development                                                                                                                                                      |
| pyyaml                                              | yaml file type support                                                                                                                                                  |
| spyder                                              | great GUI for python editing / debug                                                                                                                                    |
| jupyter                                             | great web-based editor for ipython                                                                                                                                      |

## Packages, modules, etc

One of the hardest things to understand once you started scripting in Python is how to get access to all of the good code that is already out there, and how to use it once you've got it installed. At the heart of this issue is the import command, which permits you to load packages of code. packages are term for many different python files, and the folder structure, support files, and data files which support and Surround it. Packages are distributed in a variety of ways, some historically used more and better than others,. once installed, packages typically live within the python distribution folder system itself. A package is a collection of more than just python files, it is the structure of how those files interact. Python packages, when run, can store data inside them, and access files from within their package, and load other modules. Module is a term for a reusable python file that has functions variables and data inside of it.

typically the import statement can be used to load both packages and modules. Import can be used in a variety of ways, which makes it unclear exactly how it's being used except for on a case-by-case basis. the simplest import statement looks like this

```python
import math
```
what I just done is imported the math package so that I can use it . just from this line of code it is impossible to tell whether the math is a module parentheses file, for a package, folder structure with many files,. Find out I type

```python
type(math)
```

I do know running or after running this line of code, is that when I want to access functions within math, I will have to access them by typing

math. Math function

the ```import``` statement imported