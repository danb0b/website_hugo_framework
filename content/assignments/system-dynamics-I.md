---
title: System Dynamics I
subtitle: Team Assignment
week: "07"
points: 200
type: assignment
module: dynamics
layout: page
---

# System Dynamics I

## Assignment Overview

This assignment is intended to get you familiar with the dynamics of your system.  We will start with the triple pendulum example and turn it into a leg.  

## Resources

* dynamics [modules]({{site.baseurl}}/modules/dynamics)

## Procedure

<!--hide-->

Starting with system kinematics code as well as the pendulum code shared on Wednesday (2/17/2021),

1. **Scale:** Ensure your system is using SI units.  You should be specifying lengths in meters (so millimeters should be scaled down to the .001 range), forces in Newtons, and radians (not degrees), and masses in kg.  You may make educated guesses about mass for now.
1. **Define Inertias:**  Add a center of mass and a particle or rigid body to each rotational frame.  You may use particles for now if you are not sure of the inertial properties of your bodies, but you should plan on finding these values soon for any "payloads" or parts of your system that carry extra loads (other than the weight of paper).
1. **Add Forces:** Add the acceleration due to gravity.  Add rotational springs in the joints (using k=0 is ok for now) and a damper to at least one rotational joint.  You do not need to add external motor/spring forces but you should start planning to collect that data.
1. **Constraints:** Keep mechanism constraints in, but follow the pendulum example of double-differentiating all constraint equations.
    * If you defined your mechanism as unattached to the Newtonian frame, add enough constraints so that it is fully attached to ground (for now).  you will be eventually removing these constraints.
1. **Solution:** Add the code from the bottom of the pendulum example for solving for f=ma, integrating, plotting, and animating.  Run the code to see your results.  It should look similar to the pendulum example with constraints added, as in like a rag-doll or floppy
1. **Tuning:** Now adjust the damper value $b$ to something nonzero, that over 10s shows that the system is settling.
1. _(Optional):_ Adjust joint stiffness values so that your system looks more realistic.


### Draft Submission

Please bring your code to class on Wednesday (2/26/2021).  We will do a checkoff in class and go over questions.  You should show each step of the code in class, though it is fine if there are errors, or if it fails compute due to errors in previous sections.

### Final Submission

Please include a Jupyter notebook with the following:

1. Detailed description of the completed steps above (included as blocks alongside chunks of related code)
1. Code used in solving the problem (inline in the report in code blocks), along with descriptions detailing your approach.

Please follow the "Submission Best Practices" document posted on Canvas.  This assignment should be submitted to canvas as a .pdf document or a jupyter notebook (.ipynb).  If submitted as a notebook, make sure it is fully compiled.  This can be done by opening the file in the jupyter browser and in the top jupyter menu selecting "Kernel" --> "Restart and Run All".

Please also post the completed assignment to your team's website.  This may be posted as a jupyter notebook, a rendered jupyter notebook, or a static web page with embedded code and figures.

## Rubric

| Description |  Points |
|:------------|--------:|
| Draft       |      30 |
| Step 1      |      30 |
| Step 2      |      30 |
| Step 3      |      30 |
| Step 4      |      30 |
| Step 5      |      30 |
| Step 6      |      20 |
| **Total**   | **200** |
