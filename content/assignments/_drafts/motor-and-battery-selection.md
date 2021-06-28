---
subtitle: Team Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
csl: ../../misc/ieee.csl
title: Motor & Battery Selection
week: ""
points: 200
type: assignment
module: integration
---
# Motor & Battery Selection

From last week you made some initial specifications based on your device's needs pertaining to the motor and battery.  This week you will model your selected motor and confirm it is the correct one.

## Procedure

<!--hide-->

_You may start with the motors you selected last week.  Pololu motors are a natural choice because of the number of gear ratios available._

1. Create a motor model in Jupyter/Python for your selected (gear) motor using information such as stall torque, stall current, no-load current, operating voltage, and no-load speed.  Create a torque/velocity plot.  (This would be a good time to ensure your motor and battery voltages match, and that your calculations here are performed at the right voltage)
1. Identify the maximum power of your motor.  Mark it on your torque/velocity plot.
1. Identify the maximum efficiency of your motor.  Mark it on your torque/velocity plot.
1. Using the gear ratios of your motor and kinematics, confirm you are using your motor somewhere between the point of maximum power and maximum efficiency.  Use the worst-case scenario (the point or points in your path which consume(s) the majority of power) to evaluate your motor.
1. If the motor is not operating between those points, adjust specifications until it does.   You may adjust your kinematics, select a different motor gear ratio, adjust your payload, use a different voltage, etc to make it work.
1. Update your plots for the torque/angular velocity, voltage/current given any changes above.
1. Return to last week's kinematic model.  Instead of looking at one portion of your gait, identify all the forces acting on your leg throughout a full gait cycle, including springs, portions where there are no loads, and portions where the foot is carrying the weight of your robot.  Construct a force vector encompassing all end effectors for the entire gait cycle.
1. As a function of your kinematics and these specified forces, re-evaluate the speed your robot will operate at throughout its gait using the motor model you created above.  (The speed of your robot is no longer dictated by you the designer, this is now set by the motor you have selected)
1. Using the velocity at each point along the gait cycle, find the total time it takes to complete a cycle.
1. Find the power used throughout the gait cycle (now using your motor model)
1. Using the power at each point throughout the gait cycle, find the total energy consumed by a single cycle.
1. Identify the current used by the motor throughout its gait.
1. Double-check the battery you selected last week.  Ensure the calculations performed above match the battery voltage.  Does it deliver the necessary current required by your robot?  Given the energy consumed by one gait cycle, how long will your battery last?
<!--1. Once you have identified the motor Add the motor to the purchase list.-->

<!--
1. Find motors which can exert required torques, update your mass budget, and then repeat all steps until your device can locomote under its own weight.  Feel free to use any optimization tools at your disposal to accelerate this iterative process.
1. Find a (low-cost) motor online which matches the estimates you made for 
1. Update your mass requirements using any changes to motor mass
1. Run the motor model using motor-specfic information.
-->



## Discussion

Answer the following questions

1. Which point or points did you use to identify the worst-case scenario in #4?  Justify this decision.
1. Given your design, would you rather operate your robot at maximum torque or maximum efficiency?  What drives that goal?
1. Explain what you did in #5 to make your design work.
1. Regarding #7, what new end-effectors did you consider?  What other loads did you consider?  What other portions of your gait cycle from those used last week?
1. Does your leg move the desired distance in the desired time?  What options does your team have?
1. With regard to #13, Justify your robot's battery life in context of your team's specifications

## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include answers to the discussion points above
    1. Updated specifications
    1. Updated Kinematics, Jacobian, Force/Torque computations
    1. Motor-specific information
        1. Stall Torque
        1. Maximum Speed
        1. No-Load Current
        1. Maximum Current
        1. KV
        1. other pertinent information
        1. link to part
    1. Motor model code and plots
        1. Indicate maximum power point
        1. Indicate maximum efficiency point
        1. Indicate worse case point for your motor
1. Purchase Request
1. Code

Please follow the posted submission instructions

## Rubric

| Description | Points |
|:------------|:-------|
| Report      | 50       |
| Figures     |  20      |
| Code        |  30      |
| **Total**   | 100    |

<!--unhide-->

## Rubric

| Description | Points          |
|:------------|:----------------|
| **Total**   | {{page.points}} |

<!--
| Pictures    |        |
| CAD         |        |
| DXFs        |        |
| References  |        |
-->
