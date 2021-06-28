---
title: Intro to Shapely
subtitle: Individual Assignment
class_name: EGR557
week: "11"
type: assignment
module: manufacturing
layout: page
points: 100
---

# Shapely & Manufacturing

## Overview

The purpose of this exercise is to get used to working with shapely polygons and to use it to compute some manufacturing geometry.  It is your job to determine how to compute the cut files using Python, shapely, and the foldable_robotics package

## Detailed Procedure

Display the result of each step

1. Import shapely.geometry, foldable.layer, foldable.laminate, and foldable.manufacturing modules for using various shapely geometries, Layer(), and Laminate() classes, as well as for performing advanced computations.
1. Create a new polygon a using shapely, with length and width rougly equal to $l$.
1. Initialize a ```Layer()``` ```b``` with polygon a.
1. Erode layer ```b``` by $\frac{l}{10}$ and save as ```c```.
1. Dilate layer ```b``` by $\frac{l}{10}$ and save as ```d```.
1. Compose a ```Laminate()``` ```e``` consisting of ```c```,```b```,and ```d```, in that order from bottom(first) to top.
1. Flip the layers of ```e``` and save as ```f```.
1. Identify the centroid of ```a``` and put that in a new layer ```g```.
1. Create a small circle of radius $\frac{l}{4}$ from ```g``` by dilating it by $\frac{l}{4}$ and saving it as ```h```
1. Initialize a ```Layer()``` ```h``` with ```g``` inside it.
1. Create a laminate ```k``` consisting of three layers of ```h```
1. subtract ```k``` from ```e``` and save as ```l```
1. rotate ```l``` by 30 degrees and save as ```m```
1. translate ```m``` by $(\frac{l}{2},\frac{l}{2})$ and save as ```n```
1. union ```n``` and ```l``` and save as ```o```
1. intersect ```l``` and ```n```
1. find the symmetric difference of ```l``` and ```n```.
1. subtract ```l``` from ```n```
1. subtract ```n``` from ```l```
1. apply a "unary union" to ```o``` and save as ```p```
1. turn ```p``` into a 3 layer laminate ```q```
1. dilate ```q``` by $\frac{l}{10}$ and save as ```r```
1. subtract ```q``` from ```r``` and save as ```s```
1. dilate ```r``` by $\frac{l}{5}$ and save as ```t```
1. identify the bounding box of ```t``` and save as ```u```
1. subtract ```r``` from ```u``` and save as ```v```
1. union ```v``` with ```s``` and ```o``` and save as ```w```
1. plot each layer of ```w``` individually. (3 points)

## Discussion

1. Assuming geometry ```o``` repesents the desired part, which element represents the "web"?
1. Assuming geometry ```o``` repesents the desired part, which element represents the "scrap"?
1. Assuming geometry ```o``` repesents the desired part, which element represents the fully supported device?
1. Is ```o``` as represented in its fully supported design manufacturable using laser cutting?  why or why not?

## Resources

* <https://github.com/idealabasu/code_foldable_robotics>
* [The Shapely User Manual](https://shapely.readthedocs.io/en/stable/manual.html)

## Rubric

| Description | Points |
|:------------|-------:|
| Steps       |     60 |
| Discussion  |     40 |
| **Total**   |    100 |
