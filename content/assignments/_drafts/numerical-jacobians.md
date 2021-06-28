---
subtitle: Team Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
csl: ../../misc/ieee.csl
title: Numerical Jacobians
week: "06"
points: 100
type: assignment
module: kinematics
---

# Numerical Jacobians

## Assignment Overview

The purpose of this exercise is to concretely identify the forces and torques involved with at least one mechanism in your system.  

## Procedure

_These steps may have been done already, but please revisit them now if you have received feedback_

1. Propose an foldable-compatible mechanism representing a subsystem on the scale of one leg, wing, hand, etc. This can be the device you modeled last week, but must be updated based on feedback from meeting with the instructor or design review feedback.
1.  Make the device in paper or cardboard.  This should have already been done for your last presentation, but you need an up-to-date model if it has changed.  The paper model should dimensionally match your code.
1. Start with the kinematics of your device using the method you learned in your "Spherical Kinematics" Homework and used last week for your team's kinematics assignment

_New Tasks:_

1. Select an output point(end-effector). This can / should be a point on your device where forces and/or torques will be transmitted to something else, like the ground, an object, etc.  Plot its motion. (5 points)
1. If applicable, select a portion of the path corresponding to a known force condition(such as the stance phase of walking).  This depends on your motion and should be explained. (5 points)
1. Numerically compute the Jacobian of your device by computing the differential output motion over the differential input motion of each / all motors.  If you have a multi-DOF mechanism, compute a subspace of the volume/surface/path the output traces and find the numerical Jacobian of that. (5 points)
1. From your previous biomechanics assignment literature review (or calculations you did), estimate the accelerations on your biological template's center of mass due to ground reaction forces.  Remember, $\vec{F}=m\vec{a}$.  Supply accelerations for all dimensions of your analysis(typically 2 or 3).  Scale this by any scaling assumption you will be making for your robot.  (5 points)
1. Estimate (or supply from your previous assignment) the mass of your biological template.  Scale this by any scaling assumption you will be making for your robot. (5 points)
1. Now is a good time to start thinking about the (heavy) parts you will need, specifically motors/servos, batteries, etc.  Select a motor where the stall current, stall torque, no-load speed, free-running current, and mass are available from the manufacturer.  You will be using these values later. A rule of thumb is to select the stall torque to be twice your needed running torque.  We will explain in a future lecture.  (5 points)
1. Compute a mass budget estimate for your device based on your parts list and multiply by the acceleration due to gravity.  Divide by the number of legs/feet/hands/fins which will be sharing this load. (5 points)

    | Item      | Part # | link            | # | mass      |
    |:----------|:-------|:----------------|:--|:----------|
    | Motor     | XYZ123 | [masked link]() | 2 | 100g      |
    | battery   | LIT456 | [masked link]() | 1 | 250g      |
    | **Total** |        |                 |   | **2000g** |

1. Estimate (or supply from your previous assignment) the ground reaction forces of your robot's end effector pushing up the mass of your robot. (5 points)
1. Using the formula $\tau=J^Tf$, the ground reaction force estimate, and the Jacobian you calculated from 3, determine the torques required by your motor. (10 points)
1. Estimate, supply, or specify the average velocity of your end effector during this motion.  Supply at least one dimension.  You may calculate this from the desired speed of your robot, divided by the travel of one cycle of your leg. (10 points)
1. Using the equation $\dot{q}_{out} = J\dot{q}_{in}$, determine a motor speed which satisfies the desired output velocity by testing numbers until you achieve your desired output speed. (10 points)
1. Using $P=f^Tv=\tau^T\omega$, compute the required power of your motors. (10 points)
1. Re-evaluate your motor above.  Doe it meet the power, torque, and speed requirements? If not, please repeat steps 6-12 until you achieve consistency.  _**Include all steps of your process in your final writeup.**_

## Discussion

Answer the following questions:

1. How many degrees of freedom are driven by motors?  How many remain?  How will you define the motion of any remaining degrees of freedom? (5 points)
1. Compare the mass of your biological analog to your mass budget you have created.  Which is higher?   (5 points)
1. What assumptions did you make during this process?  How off could those assumptions be in the final robot? (5 points)
1. Does your system include springs?  How do you plan to identify the correct spring for the job?  How will you merge the spring design into this analysis?  (Hint, you can treat a spring as a separate end-effector) (5 points)


## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include answers to the discussion points above
1. Code

This can/should be submitted as a single jupyter notebook file.  Please follow the posted submission instructions.

## Rubric

| Description | Points |
|:------------|:-------|
| **Total**   | 100    |

<!--
| Report      |        |
| Code        |        |
| Figures     |        |
| Pictures    |        |
| CAD         |        |
| DXFs        |        |
| References  |        |
-->
