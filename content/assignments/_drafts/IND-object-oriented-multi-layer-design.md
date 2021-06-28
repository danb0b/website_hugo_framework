---
subtitle: Individual Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
csl: ../../misc/ieee.csl
title: Object-Oriented Multilayer Design
week: "07"
type: assignment
module: manufacturing
---

# Object-Oriented Multilayer Design

## Overview

The purpose of this exercise is for your team to execute an initial design and manufacturing workflow to compute the cut files for each layer of a multi-layer device.

## Detailed Procedure

1. Create _any_ valid 5-layer hinge design consisting of (rigid, adhesive, flexible, adhesive, and rigid) material.  You may use a castellated hinge or a simple hinge for now. (5 points)
1. Find the *negative* of this geometry.  (5 points)
1. From your spherical kinematics assignment, use the location of your hinges to scale, translate, and rotate this hinge to match the end-points for each hinge in your spherical mechanism (5 points)
1. From the outer boundary of your mechanism, create a shapely polygon indicating the outer body of your robot.  Put this polygon in a layer.  Make a five layer laminate from this layer. (5 points)
1. Create one arbitrary hole/cut/feature of your choosing on one link of your device. (5 points)
1. Merge the hinge design with your body design by removing the _negative_ of the hinge design. (5 points)
1. Compute the manufacturing geometry including web and support(assuming laser cutting), ensuring that all scrap is cuttable and/or removable. (10 points)
1. Test your manufacturing to ensure that:
    * no floating parts of your design exist after the first cut.  _Discuss how you checked this._ (10 points)
    * your design is completely separated from your web.  _Discuss how you confirm this._ (10 points)
    * the result of your manufacturing process equals the design from #5.  _Discuss how you calculated this_ (10 points)

## Discussion 

Answer the following questions

* How could you check that your laminate device doesn't fall apart when separated from the scrap?  Discuss (in paragraph form, pseudocode, or code) how you would find connected material?  Remember, you know that some layers serve as adhesive. (30 points)

## Submission

Please include:

1. Code (may be supplied along with report as a single jupyter file) with answers to inline discussion questions.

Please follow the posted submission instructions.

## Suggestions

## Rubric

| Description | Points |
|:------------|-------:|
| Code        |     70 |
| Discussion  |     30 |
| **Total**   |     50 |

<!--
| Report      |        |
| Figures     |        |
| Pictures    |        |
| Videos      |        |
| CAD         |        |
| DXFs        |        |
| References  |        |
-->
