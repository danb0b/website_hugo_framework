---
title: Actuator Fitting
type: tutorial
---

## Introduction

The purpose of this assignment is to develop a model for your actuator.

## Steps
<!--hide-->

1. Decide as a team what kind of actuator you will use.  This semester you may choose any actuator or energy storage device you like, including
    * A stretched or wound spring
    * A preloaded beam
    * A deformed elastic shape
    * A motor, gear motor, or RC Servo
    * Shape Memory Alloy
    * ... (see the professor to get something else approved)
1. Develop a model which accurately captures the principal dynamics of the actuator.
    * For metal springs, you will need to know the spring constant as well as any nonlinear hard limits (as in when a compression spring bottoms out).
    * For elastic materials, you may need to capture
        * nonlinear stress/strain or force/displacement curve
        * rate-dependent loss (can be modeled as viscous damping)
    * For motors, you will need to include:
        * Coil resistance & inductance
        * inertia
        * input voltage
        * gear ratio
1. Measure or identify as many of the parameters as you can using scientific methods.
1. Develop an experiment that measures force and/or motion of a system powered by your actuator, while controlling for or reducing the impact of unmodeled effects.
    * include a picture and/or video of the experiment.
    * run the experiment and collect data on how it moves when the actuator is activated.
1. Include the actuator model developed above within a system-level model that includes the rest of your experiment
    * include the masses or inertias that your actuator is connected to
    * include other system compliance and damping effects as needed
    * include the kinematics of the surrounding mechanism  (such as the lever arm, external gear ratio, pulley diameter, etc)
    * if there are unknown parameters, consider using an optimization step to identify the parameters
1. Plot and compare the results of your model with simulation results.
1. (Optional)  If necessary, use optimization to improve your parameter estimates, and re-match your model to a second set of experimental data.

## Discussion

Write a detailed description of how you accomplisehd each of the steps above.  Be sure to include discussion on the following points:

* Assumptions you made
* Ways you eliminated unmodeled effects in the experiment
* Model elements you decided to approximate or simplify
* Description of your experiment
* Description of your system-level model
* Analysis of the quality of your model to capture the dynamics of your actuator, as well as a discussion of any optimization used to better fit your model.





<!--unhide-->

## Rubric

| Description        |          Points |
|:-------------------|----------------:|
| Actator Model      |              20 |
| Experimental Setup |              20 |
| System Model       |              20 |
| Discussion         |              20 |
| Figures            |              10 |
| Images             |              10 |
| **Total**          | **100** |
