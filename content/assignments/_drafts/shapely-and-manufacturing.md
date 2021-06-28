---
title: Shapely & Manufacturing
subtitle: Individual Assignment
class_name: EGR557
copyright: Daniel M. Aukes
#overlay_text: DRAFT
#bibliography: ../../misc/bibliography.bib
#csl: ../../misc/ieee.csl
week: "11"
type: assignment
module: manufacturing
#layout: page
points: 100
---

# Shapely & Manufacturing

## Overview

The purpose of this exercise is to get used to working with shapely polygons and to use it to compute some manufacturing geometry.  It is your job to determine how to compute the cut files using Python, shapely, and the foldable_robotics package

## Detailed Procedure

You have been given the goal of making the  2-layer laminate device shown in Figure 1:

![desired device](../../figures/unsorted/assignment-8.png){height=2in}

<!--1. Update your foldable robotics package:

    ```bash
    pip uninstall foldable_robotics
    pip install foldable_robotics
    ```
-->
1. Create the two-layer design by creating each of the two shapes as two separate shapely polygons.  Plot them in the same plot using matplotlib, using transparency and color to differentiate the layers.  This *could* be done a number of ways:
    1. extracting the points directly from shapely and plotting using the matplotlib.pyplot.fill command,
    1. by embedding shapely geometries in a Layer object and using the Layer.plot() method with color specified, or
    1. by embedding two Layer objects in a Laminate object and using the Laminate.plot() method, which automatically assigns colors.  

    **Please use the third method**
    
1. Define the rectangular sheets of material from which each layer is originally cut.  Both layers' sheets should be identical sizes.  The sheets should be larger than the devices.  The device should be located in the center of the sheets.  Plot the resulting laminate.
1. Compute the laser "keepout" of the device.  Remember, this is the area you must not cut in order to protect your device, given laser-based cutting assumptions(that lasers cut through everything). Plot the resulting laminate.
1. From the laser keepout, compute valid support material which connects scrap to device.  This material should be _cuttable_
1. Use the laser keepout definition from class to define a valid second-pass cut.  From that, compute the scrap which remains after the release(second-pass) cut and plot the resulting laminate.  This material should be _removable_.
1. Using the equation $Sheet=Scrap_{firstpass} \cup Scrap_{secondpass} \cup Device$ , compute the first pass cut and plot the resulting laminate.
<!--
1. Repeat steps 3-5 assuming CNC milling, with a relatively small but non-zero-diameter mill.( Try just a bit smaller than the center hole in the top figure.)  Describe the major differences in your computation and the result.-->

## Discussion

Answer the following questions

1. How would you compute a keepout for CNC milling?  How is this different from a keepout for laser cutting?  
1. How would the resulting geometry look different? 
1. Say you have been supplied with sets of lines which define where a user would like to connect inner and outer islands of material for a stencil.  How would you merge support material

## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include Answers to the discussion points above
1. Code

This should be submitted as a single jupyter notebook file.  Please follow the posted submission instructions

## Suggestions
* to set the color of a Layer object called "layer1" to red(1,0,0,1) try:

```python
layer1.plot(color=(1,0,0,1),new=True)
```

* use the keyword argument new=True when plotting layers or laminates to automatically generate a new figure. 

## Rubric

| Description | Points |
|:------------|:-------|
| Code        | 50     |
| Description | 25     |
| Discussion  | 25     |
| **Total**   | 100    |


## References
<!--
| Figures     | 30     |
-->
