---
title: Spherical Kinematics
subtitle: Individual Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
bibFile: data/bib.json # path relative to project root
csl: ../../misc/ieee.csl
week: "03"
points: 100
type: assignment
module: kinematics
---

# Spherical Kinematics
## Assignment Overview
![two views of the same folded spherical mechanism](../../figures/spherical-mechanism.png){width=50%}

## Instructions

<!--hide-->

1. Imagine a flat piece of paper(black lines) folded with four lines that meet in the center.  the angles $t_0$, $t_1$,$t_2$, and $t_3$ define the angles between each line.
1. pick your own values for $t_i$, as long as none of the hinges are co-linear when flat.
1. Fold a piece of paper to match the values of t you picked.  Play with it to get a physical sense of the kinematics.  Try not to let the "links" bend, only the "hinges", to get a sense of the rigid kinematics.
1. Select one configuration to answer the rest of this homework.
1. Plot the device kinematics in 2d using matplotlib in Python.
    1. use  red lines for your  mountain folds and blue lines for valley folds.
1. Create the kinematic constraint equations that describe this mechanism's motion, using the four-bar exercise from class as a starting point, and using $q_0$ as an input angle.  
    * it may be helpful to think of your paper mechanism as a set of unit-length vectors(fig 1b) rather than polygons, to make it easier to think about(and plot).
1. Pick an initial "guess" for your mechanism so that none of the folds are exactly on the x-y plane.  It will be useful to use the mountain/valley designation you specified earlier to "seed" your initial guess with a positive/negative z value.
    1. Solve the equations using the scipy.optimize.minimize function,
    1. Show the output of the minimize function to ensure it solved correctly (error is near zero).  The output should save and print the variable indicating final error.
    
    ```python
    result  = scipy.optimize.minimize(minimization_function,initial_values)
    print(result.fun)
    ```
    
1. Plot the motion(several configurations) of your device as $q_0$ changes.  
    * Only plot valid configurations.  This may be checked 
    * Use the guess from the previously-solved iteration as an initial guess for the next iteration.
    * Plot the resulting configurations in 3d.


## Discussion
    
Answer the following questions

1. With regard to step 2, 
    1. What values did you select for $t_0$, $t_1$,$t_2$, and $t_3$? (10 points)
    1. what do the angles $t_0, t_1,t_2,$ and $t_3$ sum up to?  Why is that constant for paper? What physical limitation or constraint of paper would you have break to get a different sum? (10 points)
1. Please describe how many unknown variables are used in your solver, and how many constraint equations you use to solve them with. (10 points)
1. With regard to step 6, 
    1. What remains constant as this mechanism moves in space?  What changes?  Answer with respect to $t_i, q_j,$ and $v_k$. (10 points)
    1. What about the code from class has to change to work for this assignment? (10 points)
    1. Did you have to add any new equation types?  If yes, please describe its function. (10 points)
1. With regard to step 7, what happens when you try to solve with all the vectors starting in the xy plane? (20 points)

1. With regard to step 3, include 2 pictures of your mechanism: one flattened, and one of it erected into a 3D shape. Identify mountain and valley folds by drawing dfferent line colors/patterns on your mechanism (10 points).

1. Include your plot from step 5. (10 points)
1. Include your plot from step 8. (20 points)
<!--    1.  **optional:** Referring to Figure 1b, is there something other than $t_i$ which would work just as well in a constraint equation?-->
<!--
1. Which are the mountain folds and which are the valley folds?  
1. Are there multiple answers? 
1. 
    (10 points)
    1. How would you make a mechanism where $\sum_{i=0}^3 t_i=480\text{deg}$ ? (10 points)
3. How many?
1.  **optional:** Instead of hard-coding how you color mountain-valley lines, can you alter your program to dynamically plot hinge line colors based on the solver results?
-->

## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include answers to the discussion points above
    1. Photos
1. Code, with the following
    1. Renderings, Figures, and Plots

This can be submitted as a single jupyter notebook file.  Please follow the posted submission instructions for Jupyter submissions

## Rubric

| Description |          Points |
|:------------|----------------:|
| Discussion  |              80 |
| Code        |              80 |
| Plots       |              30 |
| Pictures    |              10 |
| **Total**   | {{page.points}} |

<!--
-->

## References
[NumPy for Matlab users](https://docs.scipy.org/doc/numpy/user/numpy-for-matlab-users.html)

<!--unhide-->

## Rubric

| Description | Points          |
|:------------|:----------------|
| **Total**   | {{page.points}} |