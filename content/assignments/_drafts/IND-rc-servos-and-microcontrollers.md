---
subtitle: Individual Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
bibFile: data/bib.json # path relative to project root
csl: ../../misc/ieee.csl
title: RC Servos & Microcontrollers
week: "10"
type: assignment
module: integration
---
# RC Servos & Microcontrollers

## Overview

Your assignment is to connect to and program a microcontroller connected to an RC servo.

## Steps

1. Set up your computer to connect to your selected microcontroller.  There are many ways to do this:
    <!--* Follow the instructions from lecture-->
    * Follow the instructions on Adafruit's website for the adafruit pro trinket or metro mini (links below)
    * Follow the adafruit pro-trinket tutorial in the course tuturials
    * Use the documentation that accompanies your particular microcontroller.

1. Set up a motor driver _(not necessary for servos)_.  If you are using a DC brushed motor, you will need an H-bridge for bi-directional control.  Pololu has a variety of these devices.  Peralta studios also usually carries some like the L293.

1. Create a program to send PWM commands from your microcontroller

    a. If using the Arduino IDE, you can start with the "file-->servo-->sweep" demo and save to a new file.  Edit the attach command to work with an address on the pro trinket (like "A0").  Test this code with your servo.  You can use this code as a starting point. (Then make sure you plug your servo's signal plug into pin "A0" as well.)
    a. To change the frequency of PWM systems, one usually sets an integer value (or runs a function with an integer input) that determines the on/off ratio of your PWM signal.  Find the maximum integer value you can send to your particular microcontroller's PWM system  using the data sheet or experimentation.  Describe how you found it.  Create a constant ```PWM_MAX``` in your program which stores that value.

1. Determine how to leverage your microcontroller.
    a. **Floating-point/integer conversion:** Create an expression or routine to scale a 0.0 to 1.0 floating point number input and convert it from 0 to PWM_MAX.
    a. **Time:**Find a way to read your system clock or otherwise keep track of the current time.
    a. Create a routine or expression to pause your subroutine for a given time step ```time_step```, or to only run a subroutine every ```time_step``` milliseconds.  Different IDE's have different commands, but the ```sleep()``` or ```pause()``` commands are common.

1. Now, approximate a sine wave to your motor or servo. 

    * Consider how you might create an oscillating motor output using the equation $o=A \sin (\omega t)+b$, where $o$ is the output signal, $A$ is the ampitude of your sine wave, $\omega$ is the frequency, $t$ is the current time, and $b$ is a DC offset.  
    * Make a function which takes in four variables and computes a PWM command, appropriately scaled for your microcontroller.  These variables ```amplitude```, ```offset```, ```frequency```, and ```time```, will determine the command sent to your PWM system.

1. Now run the function
    * ```time``` should be computed in your microcontroller's main loop and input to the function. If you use a function to pause the microcontroller, it can be computed as a function of how often this subroutine runs times the number of cycles it has run.
    * set ```offset``` to half the value of ```PWM_MAX```.
    * Set ```amplitude```, ```frequency```,and ```time_step``` according to the table below.
    * 
    * The amplitude variable should reflect a percentage of the servo's total range from 0 to 1.  1 meaning the servo hits its (mechanical) positive and negative travel limits, 0 meaning a DC signal.  Eliminate any dead zones in your amplitude variable by shifting and scaling your 0-1 range to match the limits that your pwm signal can actually move the servo, if necessary.  
    * if the amplitude is zero, a zero offset should reflect a DC signal where the output of your servo rests halfway between positive and negative limits of your motor. an offset of .5 should make your servo reach it maximum, and an offset of -.5 should make your servo reach its minimum limit.
    <!--* **optional:** learn how interrupts work in order to update your pwm command with a timer based interrupts instead of a sleep command.-->
1. create a video(or several short **labeled** videos) demonstrating how you can change these three values to generate different sine-wave sweeps.  Show the following cases.  

| case |    ```amplitude``` |  ```offset```   | ```frequency``` | ```time_step``` |
|-----:|-------------------:|:---------------:|:---------------:|:---------------:|
|    1 | ```PWM_MAX``` $*0$ | ```PWM_MAX```/2 |      5 Hz       |      20 ms      |
|    2 | ```PWM_MAX```$/10$ | ```PWM_MAX```/2 |      5 Hz       |      20 ms      |
|    3 |  ```PWM_MAX```$/2$ | ```PWM_MAX```/2 |      5 Hz       |      20 ms      |
|    4 |  ```PWM_MAX```$/2$ | ```PWM_MAX```/2 |      1 Hz       |      20 ms      |
|    5 |  ```PWM_MAX```$/2$ | ```PWM_MAX```/2 |      .5 Hz      |      20 ms      |
|    6 |  ```PWM_MAX```$/2$ | ```PWM_MAX```/2 |      .5 Hz      |     100  ms     |

## Discussion

1. How did you determine ```PWM_MAX```?
1. Why should ```offset``` and ```amplitude``` be set to half of ```PWM_MAX``` to obtain a full sweep?
1. What is the maximum frequency you can command at an amplitude of ```PWM_MAX``` before you notice the amplitude decreasing?
1. What value of ```time_step``` at .5 Hz produces a smooth motor output?
1. Briefly comment about the limitations of your motor/servo in the context of each of these tests.  
<!--
1. **optional** demonstrate a sawtooth wave generator as well
-->

## Submission

Please include:

1. Report with the following
    1. Detailed description of the steps you took, in paragraph form
    1. Include answers to the discussion points above
    1. links to videos posted on YouTube
1. Code

Please follow the posted submission instructions

## Suggestions

*  in the arduino IDE, don't forget to include the math library:

    ```#include <math.h>```
  
* your frequency variable can be used in conjunction with the time_division variable to assert a sleep command which divides up time in your sine wave to approximate the sine wave.  Based on the frequency (in Hz) and the ```time_step``` variable determines the number of approximate segments your sine wave is divided into within a single cycle.
    


## Links

* Adafruit pro trinket website: <https://www.adafruit.com/product/2000>
* pro trinket tutorial: <https://learn.adafruit.com/introducing-pro-trinket>
* Adafruit metro mini website: <https://www.adafruit.com/product/2590>
* Adafruit metro mini tutorial: <https://learn.adafruit.com/adafruit-metro-mini>
* Arduino IDE setup for adafruit products <https://learn.adafruit.com/adafruit-arduino-ide-setup/overview>
* L293 Motor Driver & Arduino tutorial: <https://mechatrofice.com/arduino/l293d-motor-driver>


## A note about motors

A motor will behave differently than a servo when receiving a pwm signal; instead of a position command it will affect the velocity.  This assignment may still be completed, however.

If you are using a motor in a unidirectional fashion with just a transistor driving it, the 6 cases should be exactly the same.

If you are planning to use a bi-directional motor, please follow the instructions in the assignment, but your code should be modified to send positive velocity commands to the forward/A pin and negative commands to the reverse/B pin of your h-bridge.  In this way you should be able to command forward and negative velocities.  Thus your offset should be 0 and your amplitude should instead be PWM_MAX rather than PWM_MAX/2

## Rubric

| Description | Points |
|:------------|-------:|
| Procedure   |     25 |
| Discussion  |     25 |
| Videos      |     30 |
| Code        |     20 |
| **Total**   |    100 |

<!--
-->