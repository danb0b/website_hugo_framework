---
title: Developing Specifications
type: submodule
---

# Developing Specifications

## Introduction

Developing specifications for a novel robot is difficult, especially considering how wide-open the potential design space is.  I recommend a bio-inspired approach in order to simplify your design workspace.  Other difficulties might involve not being able to find information in research literature.  This will require a bit more inference on your part. 

## Workflow


1. Synthesize the information you have from your biomechanics investigation  into an initial specifications table.   For example, if you know ground reaction forces from your paper, and some masses, try to find peak accelerations.  If you know forces and velocities, try to find the power usage.  If you know maximum jump height and mass, find energy required for a jump.  Your template should have some critical information which must be synthesized. (10 points)
1. Discuss whether/how you will need to scale your robot up or down, or how you can mitigate the differences. (10 points)

### Anatomy / Kinematics

Identify a biological template you would like to start from.  How does it move?  How many appendages does it use to move around?

1. Draw the simplest engineering representation of the system you can of your proposed mechanical system. How many rigid bodies are there?  How many can be approximated as massless(1/10 of the total mass or less)?  Where are the springs?  Where is the (main) motor? (10 points)
1. Identify all the joints that move during this animal's gait^[Bodies / links that don't move (or whose motion is negligible) can be lumped together as one rigid body for the purposes of the model.  For example, in human walking models, the whole upper body is often lumped together as the trunk<!--TODO: cite-->].  Identify the type of motion of each joint.  Is it a simple one degree of freedom joint, like a knee, or can it move about more than one axis (like an ankle or a hip)?  Can you simplify the joint for one particular type of motion or does it use all its degrees of freedom during a gait?

## Parameters

Next, identify key parameters about this template

a. size: what size scale are we talking about?
a. mass: how much mass does the animal move around?
a. forces: what kind of forces does the animal exert on the world?  
a. energy & efficiency: energy consumed and produced by the animal.
a. kinematics

### Scale

How are animals' bodies scaled?
Talk about scaling laws

What is this animal's overall scale?  

Anatomically, what are the lengths of key moving body parts, such as the femur, tibia, etc?  

1. body length



### Mass

1. what are the major body parts and how big are they?  What about inertias?
1. does the animal often carry a "payload"?  What is the upper limit of body mass reported?


### Motion

* What are the ways that motion data is collected by biologists and biomechanicists?
    * Ghost Crab
    * Gecko
    * Cockroach

* Bob Full, Dan Goldman, Hugh Herr, George Lauder

* What does a gait cycle look like?  
    * Can you find examples of this animal's motion as it moves in the literature?
    * Would it be possible to collect motion data "in the wild" with a video camera?
* What is the stride length during a typical gait cycle?
* Distance & Speed
    *   how far does the animal move in a single stride
    *   how fast does the animal move?
Unscaled
Scaled

### Forces
1. Find the ground reaction forces involved with completing a typical locomotion cycle.  (10 points)
    * A figure from literature (with the appropriate references) of the animal during a locomotion cycle typical of the one you are studying will suffice.  Make sure you include the units.

### Energy

1. Based on mass and a knowledge of the duration and magnitude of the ground/world reaction forces involved in a single stride, what mechanical energy / power would be required to complete a single locomotion cycle?  
1. How much energy is metabolized to create that output motion
1. What is the locomotion effcicency?
1. How could you calculate this?
1. How much respiration energy / power is used?  If you can't find it, are there references for a similar animal you could scale?  
    1. Can you find a reference that tells you how to scale respiration energy across different size animals?

### Mechanical Analogs

## Exercise:  Finish the following table.

| item                       | var           | ref | calc                 | value | unit                        |
|:---------------------------|:--------------|:----|:---------------------|:------|:----------------------------|
| Mass                       | $m$           |     |                      |       | kg                          |
| Size                       | $l_0$         |     |                      |       | m                           |
| Running speed              | $v_{x}$       |     |                      |       | $\frac{\text{m}}{\text{s}}$ |
| Ground reaction force(max) | $f_{y_{max}}$ |     |                      |       | N                           |
| Kinetic Energy             | $K$           |     | $\frac{mv_{x}^2}{2}$ |       | J                           |
| Respiration Rate           |               |     |                      |       | J                           |

Live document posted here: <https://docs.google.com/spreadsheets/d/1cUHzWVrsvnuZnJfA5co5CvMN9mpavxyOL-AWfa9b9Bc/edit?usp=sharing>

<!--TODO: Finish Example
## Example: Roadrunner
-->


