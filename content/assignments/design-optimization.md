---
title: Design Optimization
subtitle: Team Assignment
type: assignment
module: optimization
points: 200
week: "13"
layout: page
---

# Design Optimization

## Introduction

The purpose of this assignment is to optimize the dynamics of your system to maximize performance against your team's selected research question and design goal.

## Procedure

<!--hide-->

1. Performance Measurement
    a. Explain, in words, how your team will evaluate the success of your robot's design.  This could be by measuring the forces produced by your design, the speed at which it walks, its thrust:weight ratio, the height it can jump, etc.  Explain, in words, how you will measure performance in simulation.  How will you measure performance in experiments?
    a. Are experimental vs. simulation metrics similar or vastly different?  If different, how will you equate $A$ with $B$?
    a. Do you have more than one performance metric you must use as for design goals?  If so, either identify the most important one or explain how you will balance two competing criteria.  
     
        _For example, if you need a robot to jump high AND far, which is more important, or how do you establish a relationship between these two possibly competing goals?_

    
    a. Explain, in math, the **measurable** performance metric(s) by which your team can estimate performance.
    a. Write, in code, a function that will evaluate the performance of your current system (as simulated in _System Dynamics II_).
1. Constraints
    a. Brainstorm and describe your team's design constraints.  Constraints are aspects of your design that are "bounded" by some physical limit (eg, the size of robot you can cut on a given laser cutter, the range of motion of a typical foldable hinge joint)
    a. Explain, in words, how you will track violation of design constraints.  For example, lets say your optimization routine suggests a design that cannot be made in a single sheet of paper.   Will you 
        a) parameterize your design space in such a way that $p=[-\infty,\infty]$ translates to a bounded design range?
        b) penalize design performance when design parameters are outside of that range
        c) explicitly bound your parameter space?
1. Execute the full optimization routine, using the code above, that
    1. permits you to parameterize your design space in one or more variable
    1. generates a scalar performance metric that implements your goal as stated above.
    1. selects an optimization approach based on your decisions above.  This may be a _global_ search or use one of the many optimization routines available in Python.
    1. bounds or penalizes designs outside of a permissable range
    1. Run your optimization and determine the optimal parameter value(s)
1. Generate a figure that shows that your parameter value is at or very near the optimal value.

<!--unhide-->

## Submission

Please include:

1. A Jupyter notebook with the following
    1. Detailed description / rationale of the steps you took (included as blocks alongside chunks of related code)
    1. Your code, detailing your approach to solving the problem
    1. Your plot of the mechanism, with labeled vertices
    1. Include answers to all questions above

This can be submitted as a single jupyter notebook file.  Please follow the posted submission instructions for Jupyter submissions

| Description | Points |
|:------------|-------:|
| 1a          |     20 |
| 1b          |     10 |
| 1c          |     10 |
| 1d          |     20 |
| 1e          |     40 |
| 2a          |     15 |
| 2b          |     10 |
| 3           |     50 |
| 4           |     25 |
| **Total**   |    200 |
