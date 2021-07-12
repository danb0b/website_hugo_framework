---
subtitle: Team Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
bibFile: data/bib.json # path relative to project root
csl: ../../misc/ieee.csl
title: Final Report
week: "16"
points: 100
type: assignment
module: project
---

# Final Report

## Assignment Overview

The purpose of this assignment is to collect group work into the report and to update it as you learn more.

## Procedure

1. Update all sections.  If you have made major changes to your design, please update prior sections of the report as needed in order to provide the most recent snapshot.  The report should report on the final device, not the initial concept.  You may show the evolution from initial concept to final design, but the reports analyses should support the final design, not the initial.
    * Rather than a narrative(story) of what your team did in order from beginning to end, what failed, and what succeeded, focus on a complete analysis of the final device.  
    * Do not include biomechanics studies or references which no longer relate at all to your final device.  Find new references if needed.  Update your assumptions.
    * Do not include analyses which do not relate to your final device.  Recompute any analysis you performed previously to match your final device and components.  Make sure to update all variables, design parameters, motor parameters, control parameters, masses, stiffnesses, etc.
    * In contrast to analyses, ensure you include all revisions of your prototypes (even if your design changed drastically), including a discussion of what each prototype was intended to help your team understand, and what you learned from each iteration.  
1. Assemble new sections.  Take all submitted group assignments and insert them into your outline as appropriate.  This includes
    * Dynamics of Device: Discuss your procedure, results, and discussion points, including figures and a rendering/snapshot of the device in motion.
    * Data Collection: include procedure, results, and discussion.

## Submission

Please include:

1. Your updated report.

Please follow the posted submission instructions

## Suggestions

* Use illustrations & pictures whenever possible.
* Label your photos and renderings to highlight the parts of your system
* Label your axes on all figures, including units.  
* Put a title on your plots, and a caption below each figure. 
* Use full sentences in your captions.

## Points Distribution
  
1. Biomechanics
    a. Physics-based estimates
    a. Bibliography
1. Kinematics, connecting it to the prototype you brought
    a. Motion Path, highlighting how the motor moves the end-effector (not how your hand moves the end effector)
    a. Jacobian calculation
     External Forces, connecting it to your team's assumptions/requirements/constraints, considering springs too
    a. Torque, connecting it to your motor's capabilities
    a. Speed, connecting both to your motor capabilities and the estimated speed of your robot
    a. Power, connecting it to motor and battery specs
    a. Energy, connecting it to battery specs
    a. Motor Model, highlighting the ideal working range
1. Implementation
    a. Selected Motor 
    a. Selected Battery
    a. Selected Microcontroller
    a. Prototype revisions
1. Manufacturing 
    a. **Workflow - **what tools are you using for creating your manufacturing cut files? solidworks? popupCAD? dxf? foldable_robotics scripting?  Please show your workflow graphically
    a. **Consistency with kinematics**
        * How your kinematics works with your manufacturing plan.  Are you going to stack multiple layers, make pieces and connect them together with rivets, put everything side-by side on one 5-layer laminate?
        * Discuss the process of updating your kinematics code and manufacturing code to accomodate changes to your design, and how that process is being optimized.
    a. **Dimensions & Decisions -**
        * What hinge have you selected and why does that work well with your selected materials?  What width have you selected, and how have you determined it?
        * For all dimensions used in your design and manufacturing workflow, discuss why you have used those dimensions.  This includes support width, bounding boxes, resolution, etc.
    a. Pictures of our manufactured prototype.  _Refer to the posted submission instructions_. 
    a. Include your design and manufacturing workflow code, with each step described in paragraph form along with the output of each step, in the _body_ of your text.
1. Stiffness and Dynamics
    1. Cantilever Beam Assignment
    a. Combine your team's procedure, results, and discussion or select the best single assignment as the basis for your report.
    a Dynamics of Device: Discuss your procedure, results, and discussion points, including figures and a rendering/snapshot of the device in motion.
1. Data Collection: include procedure, results, and discussion.
1. References 

## Suggested Outline

1. Abstract
1. Introduction
1. Background
    1. Biomechanics
    1. Foldable Robots
    1. (Other Sections)
1. Theory of Operation
    1. Kinematics
        1. Motion Profile
        1. Jacobians
        1. Forces / Torques
        1. Power Requirements
    1. Manufacturing
        1. Layered Manufacturing Computation
    1. Energetics
        1. Member Stiffness
        1. Dynamics
1. Implementation
    1. Motor Selection
    1. Microcontroller Selected
    1. Cut-file generation specifics design description.
1. Experimentatal Setup
    1. Image / Figure of experimental setup
    1. Description of setup
1. Results & Discussion
    1. Plot of motion
    1. Force Measurements
1. Conclusions & Future Work
1. Bibliography

## Rubric
| Description                                                  | Points |
|:-------------------------------------------------------------|-------:|
| Biomechanics                                                 |     20 |
| Kinematics, connecting it to the prototype you brought       |     50 |
| Implementation                                               |     30 |
| Manufacturing                                                |     40 |
| Stiffness and Dynamics                                       |     20 |
| Data Collection: include procedure, results, and discussion. |     30 |
| References                                                   |     20 |
| Focusing on Outcome?                                         |     10 |
| Updated old content                                          |     30 |
| **Total**                                                    |    250 |



<!--
| Report      |        |
| Figures     |        |
| References  |        |
-->