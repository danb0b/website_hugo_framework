---
title: Install Python
subtitle: Individual Assignment
module: python
week: "01"
points: 50
type: assignment
layout: page
---

# Install Python

## Assignment Overview

The goal here is to verify you have python installed correctly.  

## Resources

* [Installing Anaconda Python Tutorial](../modules/python/installing-anaconda.html)
* [Add folder to system path (Windows)](../modules/misc/add-folder-to-system-path.html)

## Procedure

<!--hide-->

1. Read the entire assignment before starting.
1. Follow the instuctions in the [Installing Anaconda Python Tutorial](../modules/python/installing-anaconda.html) for installing the anaconda distribution of python.
1. Download the windows build for [ffmpeg](https://www.ffmpeg.org/), a common video encoder.  Unzip and move it into a new root-level folder called "c:/binaries" or similar.  [Add this folder to your system path](../modules/misc/add-folder-to-system-path.html)
1. Open up jupyter notebook.  In windows 10, type "windows+x" and then select Windows Powershell or Command Prompt.  In the window that opens, type:

    ```bash
    jupyter notebook
    ```
    
    if installed correctly, a browser window should eventually pop open

1. Create a new python 3 notebook.
1. Practice navigating through a Jupyter environment
1. In the first code cell, add


    ```markdown
    ## EGR557: Install Python
    Full Name
    ``` 
    
1. Change the cell type to markdown and hit "shift+enter" to compile
1. Create a new code cell below the first one and enter:  

    ```python
    from matplotlib import animation, rc
    from IPython.display import HTML
    import shapely
    import idealab_tools
    import foldable_robotics
    import pynamics
    import pynamics_examples.pendulum_2_ways
    ```

1. Run that code by hitting shift+enter.  Some information should pop out, along with a blank plot.  There should be a new code window below the first.  In this window, enter:

    ```python
    HTML(pynamics_examples.pendulum_2_ways.points_output.anim.to_html5_video())
    ```

1. Run the code.
1. Enter and run this last snippet

    ```python
    from foldable_robotics.laminate import Laminate
    from foldable_robotics.layer import Layer
    import shapely.geometry as sg
    box = sg.box(-2,-1,2,1)
    box = Layer(box)
    circle =sg.Point((0,0))
    circle = Layer(circle)<<1.5
    lam = Laminate(box,circle)
    lam.plot()
    ```
    
1. Test saving your results as a pdf.  Did it work?  If not you may need to install Miktex (see the software list document).

## Suggestions

* If you already have Python installed, it may not be what you need.  We need the most up-to-date version of the Anaconda distribution with specific packages installed.
* You can update anaconda from the commandline or powershell with the following command:
 
    ```bash
    conda update --all
    ```

* Make sure you add anaconda to the system path in the installer

## Submission

* Submit your compiled jupyter file (.ipynb) to Canvas.
* Please follow the "Submission Best Practices" document posted on Canvas.

<!--unhide-->

## Rubric

| Description | Points |
|:------------|:-------|
| **Total**   | 50     |
