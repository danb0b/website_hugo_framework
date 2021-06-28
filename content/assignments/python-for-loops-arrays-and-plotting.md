---
title: Python for Loops. Arrays. and Plotting
subtitle: Individual Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
csl: ../../misc/ieee.csl
module: python
week: "02"
points: 100
type: assignment
module: python
layout: page
---

# Python ```for``` loops, Arrays, and Plotting
 
## References {#asdf}

### Python 

* [Basic Intro](https://docs.python.org/3/tutorial/introduction.html){target="_blank"}
* [Control Flow: For, if, etc](https://docs.python.org/3/tutorial/controlflow.html){target="_blank"}
* [For loops](https://wiki.python.org/moin/ForLoop){target="_blank"}
* [List Comprehensions in Python](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python){target="_blank"}

### Arrays

* [NumPy for Matlab users](https://docs.scipy.org/doc/numpy/user/numpy-for-matlab-users.html){target="_blank"}
* [Quickstart Tutorial](https://numpy.org/doc/stable/user/quickstart.html){target="_blank"}
* [Absolute Beginners Tutorial](https://numpy.org/doc/stable/user/absolute_beginners.html){target="_blank"}

### Plotting with Matplotlib

* [Matplotlib Tutorials](https://matplotlib.org/3.3.3/tutorials/index.html){target="_blank"}, specifically the [pyplot](https://matplotlib.org/3.3.3/tutorials/introductory/pyplot.html#sphx-glr-tutorials-introductory-pyplot-py){target="_blank"} tutorial
* [General Examples](https://matplotlib.org/3.3.3/gallery/index.html){target="_blank"} and pyplot [examples](https://matplotlib.org/3.3.3/tutorials/introductory/sample_plots.html#sphx-glr-tutorials-introductory-sample-plots-py){target="_blank"}
* [titles](https://matplotlib.org/3.1.1/gallery/subplots_axes_and_figures/figure_title.html){target="_blank"}
* [equal axis](https://matplotlib.org/3.1.1/gallery/subplots_axes_and_figures/axis_equal_demo.html){target="_blank"}
* [```savefig()``` examples](https://matplotlib.org/3.3.3/api/_as_gen/matplotlib.pyplot.savefig.html#examples-using-matplotlib-pyplot-savefig){target="_blank"}



## Introduction

The purpose of this assignment is to get to know Python and Juptyer Notebook.

## Procedure

<!--hide-->

1. open jupyter notebook by opening a command prompt and typing ```jupyter notebook```
1. in the first code window add this command: ```%matplotlib inline```.  This will generate inline plots.   Run the command by typing "shift+enter".

### Looping
1. Read through the above [references](#asdf) as well as searching online to become familiar with Python ```for``` loops and lists.
1. create a list called ```list1``` filled with the values ```1,2,4,'a'``` and ```True```
<!--
    ```python
    list1=[1,2,4,'a',True]
    ```
-->
1. iterate through and ```print()``` each item in the list.
<!--
    ```python
    for item in list1:
        print item
    ```

    ```python
    [print(item) for item in list1]
    ```
-->

### Arrays
1. Read through the above [references](#asdf) as well as searching online to become familiar with numpy arrays, and their differences from Matlab
1. Create a new list(call it list2) using the ```range()``` function, from 0 to 5
1. Create a numpy array from list2.  Call it ```x```
1. Use the ```numpy.sin()``` function to compute the sin of x.  Call the answer ```y```.

### Plotting
1. Read through the above [references](#asdf) as well as searching online to become familiar with plotting using the matplotlib package.
1. Create a new matplotlib figure, call it ```f```
1. plot ```x``` vs ```y``` from the previous step
1. set axes to equal proportions
1. Title your figure and axes with something descriptive.
1. Save your figure as a pdf in your python script.

## Submission

Please include:

1. Fully compiled jupyter notebook (.ipynb) code

Please follow the "Submission Best Practices" document posted on Canvas.

<!--unhide-->

## Rubric

| Description | Points |
|:------------|:-------|
| Looping     | 30     |
| Arrays      | 30     |
| Plotting    | 40     |
| **Total**   | 100    |
