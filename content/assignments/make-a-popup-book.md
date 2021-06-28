---
title: Make a Pop-up Book
subtitle: Individual Assignment
week: "01"
type: assignment
module: manufacturing
#bibliography: ../project/bibliography.bib
#csl: ../project/ieee.csl
points: 200
layout: page
---

# Make a Pop-up Book

## Assignment Overview

The goal of this assignment is to search externally for origami-inspired mechanisms you could use for your project.  Additionally, this assignment is meant to make you think critically about how the manufacturing of foldable robots is intertwined with cutting and joining processes, and to appreciate the automation

## Procedure

1. Read the entire assignment before starting.
1. Read this paper[1].  Look through other references you can find, including the book by Birmingham [2] or search via other online resources such as <https://scholar.google.com>
1. Make a table of 5 unique popup mechanisms online including an image, link, and short description.
1. Now, makine a two-page popup book...essentially the two covers.  When you open the book, your mechanism is revealed by popping up.  
    * You can pick your input mechanism to be the book opening, or to be some other input device like a tab-and-slot, or both, but it should be clear what simple translations or rotations power your book's motion.
    * the machine should be composed of more than one mechanism, connected in series or parallel as you see fit, and you should use an example of a planar and spherical mechanism somewhere in it.  Identify what is what.  If you don't know the difference, _ask in class!_
    * pick a material: something like poster-board or stiff cardstock (I have some available, please come see me)
    * Focus on generating interesting motion, _not tesselations or repeating patterns_, using the opening of the book or some other constrained input mechansim like a tab/slot.
1. Draw/plot the cut pattern for each layer of your popup book.  Use mountain/valley/cut notation.  If you don't know what that is, _ask in class!_
    * Either find and reference a standard way of drawing cut patterns, or define the line styles you use for each.  

      ![An Example. This is an example for showing the kind of figure I expect, not to demonstrate the level of detail I expect in your own assignment.](../figures/make-a-popup-book/example.png){width="50%" class="img-fluid"}

1. Take 3 photos of your final popup book in  open, closed, and midway positions.  The simple example from above is shown in those three states, for example.

    ![Open](../figures/make-a-popup-book/open.jpg){width="50%" class="img-fluid"} 

    ![Midway](../figures/make-a-popup-book/midway.jpg){width="50%" class="img-fluid"} 

    ![Closed](../figures/make-a-popup-book/closed.jpg){width="50%" class="img-fluid"} 
    
1. Take a video of your popup book and post to youtube.
1. Bring to class.

<!--
1. Identify the number of degrees of freedom of the device
1. Describe the output motion produced, relative to the input motion
1. Solve for and plot the *motion* of at least one sub-mechanism in your device using Python/Jupyter.
-->

## Discussion

Discuss the following points:

<!--1.  What is the hardest part of fabrication: planning or executing?  
1.  How did you cut your material, by hand or using a computerized tool? 
1.  Would your answer to the  question 1. be different if you had cut it using a different tool?-->
1. What is the maximum amount one foldable hinge or joint can rotate from its neutral position?  
1. Discuss the impact of your answer to question 1 with regard to the types of mechanisms one is _and is not_ able to make.
1. Discuss the deficiency of using the same material at your link as your joint.  
1. Describe strategies you could use to stiffen a link.  
    1. Consider at least two alternatives.   Find an example of each.
    1. What are the benefits and drawbacks of each?
1. Describe strategies you could use to weaken a joint.  
    1. Consider at least two alternatives.   Find an example of each.
    1. What are the benefits and drawbacks of each?

<!--
1. Discuss strategies you turned to at joints and in links in order to address deficiencies with your material.
1. Did you use more than one layer to create your mechanism?  Where?
1. Provide one alternate design to the one
Can you see any obvious problems with the way you solved your kinematics?
-->

## Suggestions

What Worked Well Last year

* Being Precise
    * If you cut by hand, use a straightedge and x-acto.
    * Consider using a laser cutter to score sheet or weaken.
* Making things out of one piece 
* Making hinges with flexible materials
    * Consider taping or reinforcing joints.
* Making links with stiff materials
* Scoring hinges
* Practicing 

What didn't work well last year

* flaps & slides (they catch and jam)
* small features
* overlapping parts / features
* corrugated cardboard
* misalignments due to assembly
* your first try
* hysteresis
* superglue

## External Resources

* Video Series by D. Birmingham:  
<https://www.youtube.com/watch?v=aGJZbNh9Phs>
* Itai Cohen Explains The Physics of Origami  
<http://www.cornell.edu/video/itai-cohen-explains-origami-physics>
* KMMODL Linkage Collection
<http://kmoddl.library.cornell.edu/index.php>

## Submission

Please include:

1. Report with the following
    1. Detailed narrative of the steps you took, in paragraph form
    1. Include answers to the discussion points above
    1. Include the mechansims you found online (image, link, description)
    1. Include photos of your popup book open, closed, and midway.
    1. Include plot/figure of your pattern
    1. Include References(preferred) or Links to examples.
    1. Include your video link

Please follow the "Submission Best Practices" document posted on Canvas.  This may be a .pdf document or a jupyter notebook (.ipynb).  Make sure the notebook is fully compiled.

Please also bring your popup book to class on Wednesday.

## Rubric

| Description | Points |
|:------------|-------:|
| Report      |     80 |
| Figure(s)   |     40 |
| Pictures    |     40 |
| Videos      |     20 |
| References  |     20 |
| **Total**   |    200 |

<!--
| Narrative   |     20 |
-->

## Bibliography

[1] B. G. Winder, S. P. Magleby, and L. L. Howell, “Kinematic Representations of Pop-Up Paper Mechanisms,” J. Mech. Robot., vol. 1, no. 2, p. 021009, 2009, doi: 10.1115/1.3046128.

<https://asmedigitalcollection-asme-org.ezproxy1.lib.asu.edu/mechanismsrobotics/article/1/2/021009/478086/Kinematic-Representations-of-Pop-Up-Paper>

[2] D. Birmingham, “Pop-Up! A manual of paper mechanisms.” .