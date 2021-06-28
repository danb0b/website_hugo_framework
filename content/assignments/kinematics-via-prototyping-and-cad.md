---
title: Kinematics Via Prototyping & CAD
subtitle: Individual Assignment
points: 100
week: "04"
type: assignment
module: kinematics
layout: page
overlay_text: draft
---

# Kinematics Via Prototyping & CAD

## Introduction

The goal of this assignment is to 1) propose a mechanism that your team can study as part of a larger laminate system, and 2) to get you comfortable sketching the kinematics of foldable systems in CAD, establishing constraints, and counting degrees of freedom.

<!--hide-->

## Prerequisites

1. Solidworks should be installed.  It may be downloaded from <https://myapps.asu.edu>.


## Steps

Pick one of the three basic kinematic elements we will be working with this semester: a planar four (or five) bar mechanism, a spherical four(or five) bar mechanism, or a sarrus linkage.  If you are not familiar with the operation of this mechanism, look it up online.
    
1. Distill the kinematics of this device into a paper-compatible mockup and take a picture of it in several positions.
1. Studying your device, conclude whether your system can be represented as a planar system, or if it is composed of three-dimensional elements^[spherical mechanisms are considered 3D, for example.]
1. Following the solidworks tutorial from class for creating 2D or 3D kinematic models, create a 2D or 3D representation of your system kinematics.
    1. Make sure you fully "ground" one "base" link.

### DOF

1. **Determine the degrees of freedom** of the system.  Further constrain your system by adding one dimension at a time (more than those that are needed to ground the base and connect the links together) to further fix/lock your system.  Count how many additional dimensions you needed for your system to become immobilized.  Record how many degrees of freedom you determined for your mechanism

    *Hint:* Try to add dimensions that define a variable innate to the mechanism -- like the angle between two links -- rather than a world-based dimension, like a horizontal distance measurement to a point, to keep this process simple.


### Input & Output

1. **Define the input(s).**  You will need one input per the device's degrees of freedom to fully define the position of the output.  The simplest and most straightforward way to think of an input, from the perspective of an origami-inspired robot, is the joint angle between two neighboring links of your mechanism.
1. **Define the output** of the mechanism by selecting a point on a rigid link that moves with the device's maximum degrees of freedom.  Just like the number of inputs, the motion of the device is determined -- and limited -- by its internal degrees of freedom.

### Range of motion

Now move your device around to the minimum and maximum limits of motion.  If more than a one degree-of-freedom device, configure the system to move along the desired path.  It may make sense for you to create one iteration of your device at each of its limits.

1. Measure and record the input(s)' and output's total range of motion.

## Discussion

Please discuss each of the following points.

<!--1. How many degrees of freedom is your system?-->
1. Do any of your joints need to move more than +/- 180 degrees as it moves between its minimum and maximum limit or throughout its workspace?  Given the constraints of folded paper, will this be a problem?  How do you plan to address it?
1. Can you identify any singularities your mechanism might move through?  Is this desirable? How would you avoid unwanted singularities?
1. How do you interpret the relationship between the amount of input and output motion you calculated when studying your device's range of motion?  What implications will this have on actuator selection or external "gearing"?
1. Based on the variables / locations you indicated as inputs, will these spots be good positions to locate actuators?  Do you plan to add springs to any joints or between any additional points?  Which joints do you plan to leave completely unactuated?

<!--unhide-->

## Rubric

| Description           | Points |
|:----------------------|-------:|
| Picture of prototype  |     25 |
| Evaluation of 2D/3D   |      5 |
| Drawing of Kinematics |     25 |
| DOF                   |      5 |
| Input/Output          |     10 |
| Range of Motion       |     10 |
| discussion            |     20 |
| **Total**             |    100 |
