---
title: System Kinematics
subtitle: Team Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
#bibliography: ../../misc/bibliography.bib
bibFile: data/bib.json # path relative to project root
#csl: ../../misc/ieee.csl
week: "06"
points: 200
type: assignment
module: kinematics
layout: page
---
# Create and Plot Kinematics

## Assignment Overview

The purpose of this assignment is to model the kinematics so that you can estimate the forces, and torques, power requirements, and speed of your system.  This will be done using a symbolic approach with the pynamics package

## Resources

<!--* []()-->

* Triple Pendulum Example
* EGR557 Kinematics Module
* EGR557 Dynamics Module
* pynamics repository


## Instructions


Meet with your team to go over each of the prototypes and mockups you have individually created through past homework assignments.  As a team, come up with a mechanism that satisfies your team's need for scope/tractability, manufacturability, and cost.

Decide as a team whether you will be using powered actuator(s) or passive energy storage device(s).  This will impact data collection assignments, how much your team spends, the complexity of your prototype, and the strength of the materials you use (you may need to upgrade from light cardboard to stiffer posterboard or even fiberglass)

1. Create a figure (either in python, in a vector-based drawing program like inkscape or illustrator, or as a solidworks rendering) of your system kinematics.  Annotate the image to include:
    * Names for each rotational reference frame.  You will need one for each rigid body (that moves independently), as well as one for the Newtonian reference frame (N).  Use the convention of a capital letter (A,B,C,...)
    * Labeled joint locations, such as $\vec{p}_{AB}$
    * A set of orthonormal basis vectors for each frame $(\hat{n}_x,\hat{n}_y,\hat{n}_z),(\hat{a}_x,\hat{a}_y,\hat{a}_z)$. It is best practice to align one of the basis vectors (like $\hat{a}_x$) with each rigid link.
    * variable names for each state variable $(q_1,q_2,x_1,y_1,\ldots)$
    * geometric constants such as link lengths (like $l_1,l_2$)
    
    Save this figure for reuse later.  You will need to add mass and inertial information as well as system stiffness information, so make sure you do your work in a way that permits reusing and modifying the figure.
    
1. Make the device in paper or cardboard.  You need an up-to-date model if it has changed from your individual assignments.  The paper model should dimensionally match your code.
1. Using a pynamics-based script, develop a kinematic model for your device.  Following the triple pendulum example, 
    1. Import packages
    1. Define variables and constants (you may want to add, remove, or rename variables to match your figure)
    1. Declare frames (you may need to add frames or rename them)
    1. Define frame rotations (you may want to switch the axis about which frames rotate)
    1. Compose kinematics (this depends entirely on the geometry of your system)
    1. Take time-derivatives of position vectors 
    1. Assemble into a Jacobian that maps input velocities to output velocities.

1. Select or Solve for a valid initial condition that represents the system in the middle of a typical gait, when it is both moving and when forces are being applied to it (or to the world by it)

    _Despite the fact that you will be using a symbolic representation, you still need to solve for a valid initial condition if your device is a "parallel mechanism".  This may be done using a nonlinear solver such as ```scipy.optimize.minimize```_

1. Plot the system in this position.
1. From your biomechanics-based specifications, define one or more force vector estimates (one for each end effector) that the system should be expected to experience.  Consider including, based on your research
    * the force of gravity exerted by the mass of a "payload" or the main body of the robot.
    * the acceleration the  system experiences during a typical gait 
    * ground reaction forces measured from biomechanics studies.

1. Calculate the force or torque required at the input to satisfy the end-effector force requirements
1. Estimate the velocity of the end-effector in this configuration.  Using the Jacobian, calculate the speed required by the input(s) to achieve that output motion.  
  
    _This may not be directly solvable based on your device kinematics; an iterative guess-and-check approach is ok._
  
1. Finally, using the two estimates about force and speed at the input, compute the required  power in this configuration.

<!--## Discussion

1. Identify the degrees of freedom of your device.

<!--
1. Solve the inverse kinematics problem for your system as its end effector moves through the given motion path.
1. Identify whether your kinematics are serial or parallel
1. Plot the motion of your device throughout its range of motion.
1. Identify the rotational joints or linear attachment points where actuators to the system (active or passive) will be mounted.  These joints or points are  where the actuators or springs will deliver torques or forces, respectively.  There should be at least one input for each of your system's degree of freedom.


<!--hide-->

<!--
1. Define (plot) the motion path of the end-effector in terms of the specific gait you are interested in (walk, run, forward hop, vertical jump). 
1. Identify a "critical portion" of your motion path, such as the stance phase of walking or the power stroke in swimming, as the worst-case portion of the motion path you would like to focus your analysis on.  This is where most of the power is being delivered from the motors.
1. Calculate dy and dq as your system moves through a motion path.  Use the trapezoidal rule to get a better estimate of the rate of change at each point in the path.
1. From dy and dq, calculate the Jacobian, J throughout the critical portion of your motion path
1. From your specifications, estimate the expected forces on the end-effector.  This may be ground reaction forces for a leg or thrust forces for swimming / flying.
1. Use the equation $\mathbf{\tau} = \mathbf{J}^T \mathbf{f}$ to calculate the expected joint torques
1. From your specifications, estimate the expected output velocity vector
1. Using $\dot{y}=J\dot{q}$, find the motor speeds required to achieve that forward velocity.
1. using either $P=\mathbf{f}^T\dot{\mathbf{y}}$ or $P=\mathbf{\tau}^T\dot{\mathbf{q}}$, identify the power required to achieve your specifications.

1. Adjust the design parameters such as mass, link lengths, etc to match your specifications.

-->
## Discussion

Answer the following questions

1. How many degrees of freedom does your device have?  How many motors?  If the answer is not the same, what determines the state of the remaining degrees of freedom? How did you arrive at that number?
1. If your mechanism has more than one degree of freedom, please describe how those multiple degrees of freedom will work togehter to create a locomotory gait or useful motion.  What is your plan for synchonizing, especially if passive energy storage?
1.  How did you estimate your expected end-effector forces
1.  How did you estimate your expected end-effector speeds

<!--1. What is the valid range of motion of your device for each internal degree of freedom?-->

<!--
1. In your motion path you plotted in step X, what did you plot?  A point?  A link?  More than one point or link?  How many degrees of freedom does it take to represent the motion of that element?
-->

## Submission

### Draft Submission

Please bring your (1) figure and (2) code to class on monday.  We will do a checkoff in class and go over questions.  You should attempt each step of the code, though it is fine if there are errors, or if it fails compute due to errors in previous sections.

### Final Submission

Please include a Jupyter notebook with the following:

1. Detailed description of the completed steps above (included as blocks alongside chunks of related code)
1. Code used in solving the problem (inline in the report in code blocks), along with descriptions detailing your approach
1. Answers to all discussion questions above.

Please follow the "Submission Best Practices" document posted on Canvas.  This assignment should be submitted to canvas as a .pdf document or a jupyter notebook (.ipynb).  If submitted as a notebook, make sure it is fully compiled.  This can be done by opening the file in the jupyter browser and in the top jupyter menu selecting "Kernel" --> "Restart and Run All".

Please also post the completed assignment to your team's website.  This may be posted as a jupyter notebook, a rendered jupyter notebook, or a static web page with embedded code and figures.  In addition to answering completing each point in the instructions and discussion, please also include:

* **Bibliography: **Please add to and refer to your Bibliography as needed
* Appendices
* Data - upload and link to all raw data collected in the generation of this report
* Code - upload and link to any other code created and by your team (other than the jupyter notebook itself) in the generation of this report.

## Rubric

| Description  |  Points |
|:-------------|--------:|
| Draft        |      30 |
| Step 1       |      30 |
| Step 2       |      10 |
| Step 3       |      30 |
| Step 4       |      10 |
| Step 5       |      10 |
| Step 6       |      10 |
| Step 7       |      10 |
| Step 8       |      10 |
| Step 9       |      10 |
| Discussion 1 |      10 |
| Discussion 2 |      10 |
| Discussion 3 |      10 |
| Discussion 4 |      10 |
| **Total**    | **200** |
