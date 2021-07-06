---
title: System Capture and Fitting
subtitle: Individual Assignment
type: tutorial
---

# System Capture and Fitting (camera)

## Introduction

The purpose of this assignment is to collect data on your system for use in fitting your model

## Course Resources

* Optimization Module
* Experimental Validation Module
* Dynamics Module

## Instructions

<!--hide-->

1. Attach 3 optical tracking markers to the fixed base frame, at the same camera depth as your experimental setup.  They must not be colinear, and would best be arranged orthogonally (as in x-y vectors)
1. Measure the distance between all three markers.
1. Measure the distance from your camera to the center of your experiment's z-plane.
1. Attach at least one marker to the output of your energy storage device / actuator so that it can alwyas be viewed by the camera.  Attach more markers if you intend to capture flexibility, bending, or compliance.
1. Attach your camera to the fixed/rigid frame using a tripod or fixed camera mount.
1. Take a practice video and run it through your capture software to ensure the markers are always visible.
1. Start recording.  Use high-quality mode.
1. Trigger your energy storage device or actuator with a step input.  The input signal must be measurable (voltage & current, distance, force, etc) or calculable (mass, energy).
1. Track the motion of your system until it stops moving.  Make sure motion is planar.
1. Export/save the video to your computer
1. Using open source motion tracking software export the x-y position  of all markers over time.
1. Using the base frame markers as reference points, size and rotate your data to get x-y values in SI units.
1. Using the model-fitting example in the optimization module, feed in the marker position data of the system output to the output of the model. 
1. Supply all known or measurable values
1. Run the optimization to identify unknown system parameters

## Discussion

* What optimizaiton method did you use?
* What worked? What didn't work?

## Suggestions

To add a known force, attach a known mass to a string, let it deflect and settle, then cut the string.

To displace a known distance, pull the device in a known direction with a string, measuring the displacement.  Let it settle, then cut the string.

If measuring voltage and current, a power supply's current reading may not be sufficiently fast enough to capture transient responses

If measuring anything that has a  digital readout (but no serial output), make sure the readout is visible by the camera.  You can then convert the voltage reading manually using the video time as a reference.

## Rubric

| Item    | Points |
|:--------|:-------|
| Writeup | 10     |
| Plots   | 10     |
| Code    | 10     |
| ...     | ...    |
| **Total**                              | |
<!--unhide-->

## Rubric

| Description | Points          |
|:------------|:----------------|
| **Total**   | |