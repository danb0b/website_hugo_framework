---
subtitle: Team Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
bibFile: data/bib.json # path relative to project root
csl: ../../misc/ieee.csl
title: Design and Manufacturing Workflow
week: "13"
type: assignment
module: integration
points: 200
#layout: page
---
# Design and Manufacturing Workflow

## Overview

The purpose of this exercise is for your team to execute a full design workflow to compute the cut files for each layer of your device. The input should be a dxf file.  The output should be a set of dxf files, one for each layer of your laminate

## Detailed Procedure

<!--hide-->
1. Create a design in solidworks, python, dxf, or popupCAD of your complete robot, based on your most recent prototype.
    1. If you wish to connect some parts together, include alignment holes for rivets that permit layers to be aligned and attached
    1. Identify each design element with a different layer or variable, such as 
        * The outline of your robot.
        * Hinge Locations (one for each hinge type you plan to use)
        * Holes 
        * Cut lines
        * Identifying Layer text
        * Alignment Holes
1. Create a script or popupCAD design which extracts each of these elements separately. For example, plot all the hinges, all the cuts, all the bodies, all the holes with separate plot commands.
    * embed a labeled figure of each design element(bodies, hinges, cuts, holes) in your report, or indicate there are none of those particular design elements
1. Merge those design elements into your _laminate design_.
    * embed a labeled figure of your laminate design in your report
1. Compute support geometry, ensuring that it is cuttable.  Use your discretion as to how detailed to make your support design
    * embed a labeled figure of your support in your report
1. Compute first pass and second pass cuts, ensuring it does not cut into the design.  Use your discretion as to how detailed to make your cuts
    * embed a labeled figure of each in your report
1. Compute all removable scrap, separated into up/down/both categories.
1. Compute the outer sheet of material you will start with.
1. Place four 5mm holes in a square pattern, spaced Nx20mm apart, on your scrap.
1. Identify each layer with text somewhere in the scrap
1. Add holes and layer text to scrap geometry
1. embed a figure of your final scrap design in your report.
1. Test your manufacturing to ensure that:
    * no floating parts of your design exist after the first cut
    * your design is completely separated from your web.
    * the result of your manufacturing process results in your desired parts
    * embed a labeled figure of each computation in your report


<!--## Alternate method
If you choose to use popupCAD, that is fine.  Please indicate input dxf(s), along with-->


## Discussion

Answer the following questions

1. Justify your design decisions.
    * Why have you selected your particular hinge design? (15)
    * Why are hinges the width you have selected?  (15)
    * other project specific decisions you made (15)
    * Which removable scrap are you using?  why? (15)

## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Figures of your design workflow as requested in the procedure above.
    1. Include answers to the discussion points above
1. Code (may be supplied along with report as a single jupyter file)

Please follow the posted submission instructions.

## Suggestions

## Rubric
<!--unhide-->


| Description | Points |
|:------------|-------:|
| Code        |     20 |
| Images      |     20 |
| Discussion  |     60 |
| **Total**   |    {{page.points}} |

<!--
| Figures     |        |
| Videos      |        |
| CAD         |        |
| DXFs        |        |
| References  |        |
-->
