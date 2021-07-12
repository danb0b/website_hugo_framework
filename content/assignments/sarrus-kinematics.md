---
title: Sarrus Kinematics
subtitle: Individual Assignment
#bibliography: ../misc/bibliography.bib
bibFile: data/bib.json # path relative to project root
#csl: ../misc/ieee.csl
week: "05"
points: 100
type: assignment
module: kinematics
layout: page
overlay_text: draft
---

# Spherical Kinematics

## Assignment Overview

The purpose of this assignment is to get you comfortable using the numerical computational capabilities of Python to start estimating the performance of your design.

![mechanism](../figures/kinematics/sarrus.png){width="50%"}

<!--![two views of the same folded spherical mechanism](../../figures/spherical-mechanism.png){width=50%}-->

## Instructions

<!--hide-->

### Numerically Solve for a Mechanism's Position

Using the examples on the foldable robotics website as a starting point, solve for the kinematics of the mechanism above.

1. Make a table of link lengths corresponding to the vectors defined by the six heavy black lines.  Please approximate the lengths of each link of the mechanism, as well as the device's initial position.  No need to match exactly with the original drawing.
1. Plot the mechanism in Python using the matplotlib.pyplot package, making sure to label each vertex over each line.
1. Create an objective function whose error is zero when:
    a. All of the length constraints of the mechanism are correctly estimated
    a. The base of the robot is fixed to the ground and in a specified orientation
    a. The end-effector(defined by the link between $p_3$ and $p_4$) is parallel to the base link($p_0$-$p_5$).
    a. The $\hat{n}_x$-component of the distance between $p_0$ and $p_4$ is zero.
    a. The internal degree of freedom defined by $q$ matches a value given or set by you.
1. Solve this function three times using the ```scipy.optimize.minimize``` function: once for each of three states where the input $q$ is varied by a small, constant amount. ^[consider using a for loop].  Select an initial guess for the state of the system that is close to the right answer but not exact; update the initial guess with the results of the prior solution after that.
    a. Show the result of each evaluation.  This should demonstrate that the error in the result after each calculation is small (less than ~1e-3).
    a. Plot the device in each of its three configurations (within a single figure)
1. Now approximate the rate of change of the middle point of the trajectory by finding the slope between the first and third point. Define a point on the mechanism that serves as the "output" or "end-effector".^[$p_3$ or $p_4$ would be a good choice.]
    a. Calculate the slope in python and print the result.
    a. Plot the 3-point trajectory.
    a. Overplot the slope on the middle point using an arrow.
1. Compute the Jacobian Matrix in that middle state.  This should be a 2x1 matrix, as it is a 2D mechanism.
1. Now, assume that a force $\vec{f}$ of $f=\left[\begin{matrix}10\\-10\end{matrix}\right]$(2D) <!--or $f=\left[\begin{matrix}10\\-10\\5\end{matrix}\right]$(3D)--> is applied to the end-effector.  Compute the force experienced at the input.
1. What happens when the force $\vec{f}$ applied to the end-effector changes to $f=\left[\begin{matrix}0\\-10\end{matrix}\right]$(2D).  Provide a rationale as to how or why this answer contrasts with the previous one.
<!--1. Discussion Question: Why is the input a force and not a torque?-->
1. Now, assume that the input is moving at a rate of 2.4 <!--depending on if you selected a linear or angular values-->.  How fast is the output moving?

## Submission

Please include:

1. A Jupyter notebook with the following
    1. Your plot of the mechanism with labeled vertices
    1. Your code detailing your approach to solving the problem
    1. Detailed description of the steps you took (included as blocks alongside chunks of related code)
    1. Include answers to all questions above

This can be submitted as a single jupyter notebook file.  Please follow the posted submission instructions for Jupyter submissions

## Rubric

| Description | Points |
|:------------|-------:|
| Step 1      |      5 |
| Step 2      |      5 |
| Step 3a     |      5 |
| Step 3b     |      5 |
| Step 3b     |      5 |
| Step 3c     |      5 |
| Step 3d     |      5 |
| Step 3e     |      5 |
| Step 4a     |      5 |
| Step 4b     |      5 |
| Step 5      |     10 |
| Step 6      |     10 |
| Step 7      |     10 |
| Step 8      |     10 |
| Step 9      |     10 |
| **Total**   |    100 |

