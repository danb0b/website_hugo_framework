---
title: Data Collection and Experimental Validation
subtitle: Team Assignment
week: "14"
type: assignment
module: validation
points: 200
layout: page
---
# Data Collection and Experimental Validation

## Assignment Overview

The purpose of this assignment is to collect data on your system and compare against the results estimated from simulation.

## Procedure

<!--hide-->

1. Perform an experiment to collect either trajectory or force information over 5 cycles of motion (if cyclic) or 5 separate experiments (if single-run).
1. Take a picture of your setup.  Annotate the photo with arrows, text boxes etc to help us undestand how you tested your device
1. Record a video of at least one run of your experiment.
1. Plot experimental data against dynamics model output (that is using the same parameters as the prototyped device).

## Discussion

Answer the following questions:

1. What do you consider the top five sources of error in your data collection experiment?
1. What steps did you take to reduce the error?
1. What was difficult to control?
1. How would you improve your testing setup or procedure next time?
1. How well does your data mirror your simulated results?  What is similar, what is different?
1. Is it possible to add a modeling element which models/captures discrepencies between these two results?  What element if added to your simulation what have the biggest impact on its fidelity? 
1. What additional equations and parameters would you need in order to add this element?

## Suggestions

Potential sources of error in the experiment could include, but are not limited to:

* mounting issues: floppy parts, using tape to hold things down
* mass distribution
* unanticipated stiffness issues
* noisy sensors
* uncontrollable/un-repeatable effects in the environment
* wires
* human in the loop
* degradation of the prototype
* loss of signal
* programming bugs
* latency / timing issues.

## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include answers to the discussion points above
    1. Figures
    1. Pictures

The report should be submitted as a jupyter notebook, and should include a link to your video, which can either be embedded and uploaded to your site or shared via YouTube.  Please follow the posted submission instructions.


## Rubric

| Description           | Points |
|:----------------------|-------:|
| Report Narrative      |     50 |
| Figure(s) of Data     |     50 |
| Image of Experimental |     25 |
| Video                 |     25 |
| Discussion            |     50 |
| **Total**             |    200 |
