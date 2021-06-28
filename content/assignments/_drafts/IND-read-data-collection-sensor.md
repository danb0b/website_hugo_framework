---
subtitle: Individual Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
csl: ../../misc/ieee.csl
title: Read Data Collection Sensor
week: "11"
type: assignment
module: integration
---

# Read Data Collection Sensor

## Assignment Overview

## Procedure

1. Refer to your sensor datasheet / documentation to learn how to read and write to it from your microcontroller
1. Create a small program which converts your sensor data to serial text and sends that on your debug port back to your computer.  Ideally, send a formatted line in which your data is formatted to output legibly to a terminal even at a high data rate.

    Worse:

    ```
    1.0
    101.0
    101.2
    .3
    ...
    ```

    Better:

    ```
      1.0,
    101.0,
    101.2,
      0.3,
      ...,
    ```

1. Connect your computer's serial port to your sensor, read some data, and save it to your computer.  
1. Plot the imported data in matlab, python, or excel.

## Discussion

Answer the following questions

1. Describe the workflow you will use to collect data on your robot and extract the data from this sensor.  
1. Discuss in general how do you ensure that you measure only what you want to measure, and eliminate noise?  Detail the steps you have taken.
    1. Where will your sensor be located, and why is that the best location for it?
    1. Will you collect data using wires?  Will the wires affect your experiment? How do you plan to mitigate their effect?

## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include answers to the discussion points above
1. $\mu$c Code
1. Figure of Data

Please follow the posted submission instructions

## Suggestions

* Use a .csv format to save your data as comma separated values.  This can be easily read into excel, matlab, or python for plotting.

## Rubric

| Description | Points |
|:------------|-------:|
| Report      |     50 |
| Code        |     25 |
| Figures     |     25 |
| **Total**   |    100 |

<!--
| Pictures    |        |
| Videos      |        |
| CAD         |        |
| DXFs        |        |
| References  |        |
-->