---
title: Cantilever Beams
types: [tutorial,] 
---

# Cantilever Beams

## Overview

Compute the stiffness of a laminate beam

## Summary of Steps


![example](../../figures/unsorted/weight-measurement.png){width=6.5in}

1. Prepare 4 rectangular samples of the rigid material your team is using (cardboard, posterboard,fiberglass) in the dimensions of 25mm x 125mm.  
1. Measure the thickness of each of the samples in at least two places.  You should have at least 8 measurements.
1. Clamp two beams flat on top of one another on a table with 100mm hanging off the side.   
    **Optional:** Print out and vertically mount a grid pattern behind the beam for taking measurements via photos
    
1. Tape a string to the bottom sample so the string hangs off the end of the lower beam
1. Mount/place camera directly in front of the beam  
    **Suggestion:** use a tripod to ensure consistent measurements shot-to-shot.
    
1. Take picture of the bottom beam unloaded.
1. Measure the deflection of the bottom beam with respect to the top beam material as a function of a small of load.  
    1. Take deflection / force readings for each beam with at least 5 different loads by measuring the distance between the loaded and unloaded beam
    **Suggestion:** You can use calibrated weights or paperclips, small amounts of water, etc. and then measure or calculate the mass afterwards.  Or you can use a fish scale or digital load cell, but be sure to take consistent deflection/force readings.

    1. Take a picture of the beam at each load value.  
    **Suggestion:** Do not permanently bend or plasticly deform the material, otherwise the test will produce poor results.
    
1. Repeat the test for the remaining two beams.  You should have $3*5=15$ experimental values.  Leave the same beam on the top throughout the tests.

---

1. Prepare 4 rectangular samples of the laminate material your team is using in the dimensions of 25mm x 125mm
1. Repeat the prior experiment for your laminate.

---

1. Plot the force/deflection data for your single-layer experiment and extract the slope.
1. Using the code introduced in class, compute the Young's modulus for the this material based on the slope of your experimental data and the dimensions of the beam.
1. Using the estimate for Young's modulus, compute the stiffness of a 5-layer composite with those materials on the top and bottom layer.  
    1. Assume the other layers do not contribute any stiffness, just thickness
    1. Assume a symmetric laminate
    1. You may use the laminate thickness measurement minus the layer thickness measurements to obtain the total thickness of the other non-contributing layers.
1. Overplot the **computed** beam stiffness against the **experimental** stiffness data you obtained for the laminate.

<!--
## Discussion

Answer the following questions

1. Describe any error in each of your results, and explain their potential sources.  
    1. Consider both modeling error and experimental error, and explain how both may contribute.  
    1. Make an educated guess what was the dominant source of error.

## Submission

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include answers to the discussion points above
    1. Pictures
    1. Code
    1. Figures

    -->
<!--This assignment should be submitted as a writeup of your individual process.  Describe your approach to each of the steps in the assignment.  Provide pictures, code, and figures as necessary to make the point.   -->


## Suggestions

* Test individual layers to start
* You have permission to adapt the geometry to suit your own project as needed, but describe the differences in your setup
* Document your process
* I will be forgiving on precision, but I want to know what you did and how you did it
* You may use scissors, but you will need to measure what you actually cut.
* This work can be combined and put in your group's final report, but the work for this assignment should be individual.  You may coordinate with your group, however, so that each of your teammates test different design points however

