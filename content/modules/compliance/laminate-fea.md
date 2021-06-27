---
title: FEA Modeling
type: tutorial
---

#  FEA Modeling

## Introduction

The goal of this tutorial is to get you familiar computing the stiffness of a laminate using FEA.  You may use any FEA tool you are comfortable with, or the code supplied in class as a starting point.

## Resources

* [Euler-Bernoulli Beams](generated/euler-bernoulli-beams/euler-bernoulli-beams.html)
* [Solidworks FEA Tutorial](solidworks-fea-tutorial.html)


## Procedure

1. Pick one or more geometries of your team's robot design to focus on.  Perhaps a "rigid" link which you would like to program to exhibit a certain springyness, a long skinny link which exhibits too much deflection, or, if your system is sufficiently rigid already, your flexible joint material, in order to "program" a desired springiness into your team's joint dynamics.
1. Create a CAD or scripted model for that link, replicating the geometry and using the experimentally-collected value for Young's modulus you extracted from your previous individual assignment.
    * You may use any finite element software you are comfortable with.
1. Define boundary conditions that are appropriate for your team's particular design and use case.
1. Define loading conditions that are appropriate for your team's particular design and use case.
1. Compute and plot the deflection of your geometry under load.
1. Compute and plot the stress in your design.  Identify the region(s) of maximum stress.  (Von Mises stress is fine)
1. Implement a design change which improves the performance of this geometry for your stated use case.


## Discussion Points

Answer the following questions when writing up your report

1. What is your identified geometry, and why was it selected? How will modeling the deformation of this geometry inform the development of your robot?
1. What FEA simulation tool did you select and why?
1. What boundary conditions did you use, and why did you use them?  Connect your answer back to the geometry you have selected and how you are considering that item's deflection in your prototype.
1. What loading conditions did you use, and why did you use them?  Connect your answer back to the geometry you have selected and how you are considering that item's deflection in your prototype.
1. How do you expect your geometry to fail, and under what conditions?
1. What design change did you implement, and how did that impact/improve the desired peformance of your element and system?
1. Compare the simulated results against your experiences testing your prior prototype.

<!--
## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include answers to the discussion points above
    1. Plots of deflection and stress.
    1. Pictures of actual link failure under similar conditions.
1. Design file (CAD or python script)
1. Stiffness Analysis (CAD or python script)

This can/should be submitted as a single jupyter notebook file.  Please follow the posted submission instructions

-->