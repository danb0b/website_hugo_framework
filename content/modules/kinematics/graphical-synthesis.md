---
title: Graphical Synthesis
---

# Graphical Synthesis

A popular way of deriving the desired kinematics of a device graphically has also been employed for centures.


## By Hand Instructions

Download the [part]({{site.baseurl}}/assets/graphical-synthesis/part2.sldprt)

The following instructions can be done by hand or with a tool like Solidworks.  If you do it by hand you will need a ruler and straightedge.

1. Draw a constant length line (the output link) in three different positions.

    ![](../../figures/graphical-synthesis-hand/01.png){height=3in}
    
    ![](../../figures/graphical-synthesis-hand/02.png){height=3in}

1. Joint 1
    1. Draw a line from the left vertex of the output link in position 1 to the left vertex of the output link in position 2

        ![](../../figures/graphical-synthesis-hand/03.png){height=3in}
        
        ![](../../figures/graphical-synthesis-hand/04.png){height=3in}

        ![](../../figures/graphical-synthesis-hand/05.png){height=3in}

    
    1. Draw a line from the left vertex of the output link in position 2 to the left vertex of the output link in position 3
    1. Find the perpendicular bisector of these two lines.  Where they intersect is the location of joint 1
1. Joint 2 
    1. Draw a line from the right vertex of the output link in position 1 to the left vertex of the output link in position 2

        ![](../../figures/graphical-synthesis-hand/06.png){height=3in}

        ![](../../figures/graphical-synthesis-hand/07.png){height=3in}

        ![](../../figures/graphical-synthesis-hand/08.png){height=3in}
        
    1. Draw a line from the right vertex of the output link in position 2 to the left vertex of the output link in position 3
    1. Find the perpendicular bisector of these two lines.  Where they intersect is the location of joint 2
1. Links 1 and 3

    The next step is to draw the coupling links.

    1. Draw lines from joint 1 to the left vertex of the output link in position 1, 2, and 3

        ![](../../figures/graphical-synthesis-hand/09.png){height=3in}

    1. Draw lines from joint 2 to the right vertex of the output link in position 1, 2, and 3.
    
        ![](../../figures/graphical-synthesis-hand/10.png){height=3in}

1. Measure the length of your output and coupliing links, as well as the distance between joint 1 and 2 (this is the base/fixed link).  This is your four-bar design

With this design, a body will be guaranteed to move through these three positions.

![](../../figures/graphical-synthesis-hand/11.png){height=3in}

![](../../figures/graphical-synthesis-hand/12.png){height=3in}

![](../../figures/graphical-synthesis-hand/13.png){height=3in}

![](../../figures/graphical-synthesis-hand/14.png){height=3in}

![](../../figures/graphical-synthesis-hand/15.png){height=3in}


This graphical synthesis method is simplified, because there are more design variables at your fingertips than this rudimentary method permits...it just gets too complicated to solve for graphically.

<!--
Extensions to the four-bar linkage

Five bar linkages, surprisingly, have one more bar
-->

## Solidworks Instructions

Download the [part]({{site.baseurl}}/assets/graphical-synthesis/part1.sldprt)

If you want to use the ability of Solidworks to add constraints to objects, this can simplify the process.  Below are the steps.

1. Create a new part

    ![](../../figures/graphical-synthesis/00.png){height=3in}

1. Select the top plane and create a new sketch
 
    ![](../../figures/graphical-synthesis/01.png){height=3in}

1. Draw three lines

    ![](../../figures/graphical-synthesis/02.png){height=3in}

1. Select all three lines and add a constraint to make them equal length

    ![](../../figures/graphical-synthesis/03.png){height=3in}

    ![](../../figures/graphical-synthesis/04.png){height=3in}
    
1. Select the left vertex of each line and apply a "fixed" constraint

    ![](../../figures/graphical-synthesis/05.png){height=3in}

    ![](../../figures/graphical-synthesis/06.png){height=3in}

    ![](../../figures/graphical-synthesis/07.png){height=3in}

    ![](../../figures/graphical-synthesis/08.png){height=3in}

    ![](../../figures/graphical-synthesis/09.png){height=3in}

1. Starting with the left vertex of each line segment, draw three lines that meet at a common point

    ![](../../figures/graphical-synthesis/10.png){height=3in}

1. Select all three lines and add an "equal length" constraint

    ![](../../figures/graphical-synthesis/11.png){height=3in}

1. Starting with the right vertex of each line segment, draw three lines that meet at a common point

    ![](../../figures/graphical-synthesis/12.png){height=3in}


1. Select all three lines and add an "equal length" constraint

    ![](../../figures/graphical-synthesis/13.png){height=3in}

1. Establish three equal length constraints with the corresponding line segments

    ![](../../figures/graphical-synthesis/14.png){height=3in}


1. Add a fourth line segment and connect its left and right vertices to each of the common points.

    ![](../../figures/graphical-synthesis/15.png){height=3in}
    
    ![](../../figures/graphical-synthesis/16.png){height=3in}

1. Dimension the length of the line segment

    ![](../../figures/graphical-synthesis/17.png){height=3in}


1.  Select and drag the new line segment.  It should be able to move through each of the three positions you defined

    ![](../../figures/graphical-synthesis/18.png){height=3in}

    ![](../../figures/graphical-synthesis/19.png){height=3in}

    ![](../../figures/graphical-synthesis/20.png){height=3in}
