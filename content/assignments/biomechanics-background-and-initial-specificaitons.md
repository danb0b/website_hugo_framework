---
title: Biomechanics Background and Initial Specifications
subtitle: Team Assignment
bibliography: ../project/bibliography.bib
csl: ../project/ieee.csl
week: "04"
points: 200
module: biomechanics
type: assignment
layout: page
overlay_text: draft
---

# Biomechanics Background and Initial Specifications

## Assignment Overview

The goal of this part is to encourage you to get "bio-inspired", to get you thinking about the scale of your robot, and to think about how to replicate the efficiencies of biological systems.  You may refer to the [developing specifications](../modules/biomechanics/developing-specifications.html) page for more information

_Please Read this whole assignment first._

## Suggestions

* It will be useful to start using a program like [Mendeley](https://www.mendeley.com/?interaction_required=true) to collect and organize references.
* Be creative in your search terms. Use [@Dickinson2000] to find good starting points for references and keywords.
* Start writing down search keywords from class.

## External Resources
  * <https://en.wikipedia.org/wiki/Kleiber%27s_law>

## Procedure

<!--hide-->

### Constraints

* This year we will be focusing on one or two system models that you can modify to answer your question^[These will be determined during week 3 in conjunction with project selection and team formation.] These will involve arrangements of parallel mechanisms:
    * Planar mechanisms, such as four and five-bar mechanisms
    * Spherical mechanisms such as _spherical_ four or five-bar systems
    * Sarrus linkages (a particular straight-line mechanism)
* The source of bioinspiration can be extant(living) or extinct, but you should be able to find enough information about it to make a set of reasonable assumptions about what you don't know.
* Focus on an animal in a size range that you can make at scale, at a reasonable cost, rather than scaling a different-sized animal up or down.

*Please check with Dr. Aukes if you need further clarification / approval.*

### Steps

1. Identify a candidate organism you wish to focus on its biomechanics.  This consists of a specific animal species, its body plan, and the motion of interest.  Search in Google scholar, using keywords such as "anatomy", "morphology", "mechanics", "biomechanics", "ground reaction forces", etc. along with the animal's informal or scientific name along with the type of locomotion.  
    1. List five of the most closely related research references on topics pertinent to your project, in IEEE format.
    1. Identify three citations which are most useful in creating initial specifications for your robot(use an asterisk in the previous list).  Now discuss these three papers, highlighting the information you can draw from each.  Be specific.  Why is each paper valuable? (At least one paragraph each)
1. Search for existing _bio-inspired robots_ based on the same animal, subsystem, and motion.
    1. List five of the most closely-related research references on topics pertinent to your project in IEEE format. 
    1. Identify three citations which are most useful in creating initial specifications for your robot(use an asterisk in the previous list).  Now discuss these three papers, highlighting the information you can draw from each.  Be specific.  Why is each paper valuable?  (At least one paragraph each)
1. Collect all the information you have found from your references into one place. A well-formatted table may do, with supplementary figures from literature as needed.  A specifications table is a handy way to collect parameters.  Use SI units.  Example below:

    | Parameter                    | Unit            | Value Range | Reference |
    |:-----------------------------|:----------------|:------------|:----------|
    | Total Mass                   | kg              | .2-.4       | [1]       |
    | Maximum Landing Force        | N               | 6           | [1]       |
    | Maximum Takeoff Force        | N               | 4           | [2]       |
    | Average Takeoff acceleration | $\frac{m}{s^2}$ | 13          | [3]       |
    | ...                          | ...             | ...         |           |

    Examples of the types of information to include: 

      * Typical mass of the animal as a whole, and of key anatomical parts
      * Average speed of the animal.
      * Key points in a stride: leg motion such as stride length and maximum foot height, trunk motion and orientation, etc.
      * Typical ground reaction forces during locomotion(plot is best)
      * Metabolic energy/power consumed to locomote (respiration).
      * Mechanical energy/power generated during locomotion
      * Key biological materials and their mechanical properties (bone, ligaments, tendons, and the resulting link/joint stiffnesses and damping properties)
      * Muscle forces

    
1. Fill in the information gaps from your biomechanics investigation with informed assumptions you can make.   For example, if you know ground reaction forces from your paper, and some masses, try to find peak accelerations.  If you know forces and velocities, calculate  power usage.  If you know maximum jump height and mass, find energy required for a jump.  The most important pieces of information you can gather at this point are elements like "how much energy is consumed in accomplishing this gait", "What are the forces involved", etc.
1. Supply at least two figures from literature, highlighting key aspects of the biological system.  This should include one from each of the following categories:
    1. Figures/drawings of skeleton, anatomy,  exoskeleton, body plan, musculature, kinematics
    1. Motion plots, freeze frames of gait cycle, plot of ground reaction forces
    1. ... other aspects of the parameters above.
1. Draw the simplest engineering representation of the system you can of your proposed mechanical system. How many rigid bodies are there?  How many can be approximated as massless(1/10 of the total mass or less)?  Where are the springs?  Where is the (main) actuator?



<!--
## Table Example
1. Make a paper mockup of a laminate implementation of 3. This does not need to be made with a laser cutter but must clearly communicate where a motor is connected, and what touches the ground. Show it in multiple configurations of its walk cycle. (20 points)
-->
<!--
1. Draw free body diagrams for those bodies.
-->
<!--
1. What is the total energy used to complete a single locomotion cycle?  What is the power required?  How did you calculate this?
-->



<!--
* Can you find a reference that tells you how to scale respiration energy across different size animals? (10 points)
1. Find the ground reaction forces involved with completing a typical locomotion cycle.  (10 points)
* A figure from literature (with the appropriate references) of the animal during a locomotion cycle typical of the one you are studying will suffice.  Make sure you include the units.
-->
## Discussion

In addition to answering completing each point in the procedure and discussion, please also include answers to the following questions:

1. Discuss / defend your rationale for the size animal you selected in terms of your ability to replicate key features remotely with limited material selection.
1. Find a motor and battery that can supply the mechanical power needs obtained above.  Consider that motor efficiencies may be as high as 95%, but if you can't find it listed, assume you find a more affordable motor at 50-70% efficiency.  Compare the mechanical watts/kg for the necessary motor and battery vs the animal's mechanical power/mass above?  Which one is more energy dense?

## Submission

Please include a report with the following


1. The requested steps of the procedure, in paragraph form (no sentence fragments).
1. Answers to the discussion points above
1. plots & figures
1. Bibliography
1. Appendices(optional), consisting of
    * Data - any raw data collected in the generation of this report
    * Code - any code created and by your team to in the generation of this report.  If you are using a jupyter notebook, to generate this assignment, you can supply your code inline or at the end.


Please follow the "Submission Best Practices" document posted on Canvas.  This assignment should be submitted to canvas as a .pdf document or a jupyter notebook (.ipynb).  If submitted as a notebook, make sure it is fully compiled.  This can be done by opening the file in the jupyter browser and in the top jupyter menu selecting "Kernel" --> "Restart and Run All".

Please also post this completed assignment to your team's website.  This may be posted as a rendered jupyter notebook or a static markdown file with code and figures uploaded separately; details on how to do each may be found in the [Jupyter Notebooks in Websites](../modules/project/jupyter-notebooks-in-websites.html) tutorial.


<!--unhide-->

## Rubric

| Description                | Points |
|:---------------------------|-------:|
| Bio Inspiration            |     20 |
| Other bio-inspired robots  |     20 |
| Table                      |     40 |
| Other Assumptions          |     10 |
| Figures                    |     20 |
| Engineering Representation |     20 |
| Discussion                 |     40 |
| Bibliography               |     30 |
| **Total**                  |    200 |

<!--
| Report      |              70 |
| References  |              10 |
| Videos      |        |
| Code        |        |
| CAD         |        |
| DXFs        |        |
| References  |        |
-->

<!--[@Bennett1985],[@Kramer2011],[@DeLong2010],[@Makarieva2008],[@Hanna2011],[@Taylor1982],[@Weir1949]-->

## Bibliography
