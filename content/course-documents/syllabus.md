---
title: Syllabus for Foldable Robotics 
subtitle: Version 2022-01-11
author: Daniel M. Aukes
date: Spring 2021
menu:
  main:
    name: Syllabus
    weight: 2
    parent: Documents
geometry: 
  - top=1.5in
  - bottom=1in
  - left=1in
  - right=1in
mainfont: OpenSans
sansfont: OpenSans
---

## Overview 

***Foldable Robotics*** is a course organized around new types of robots being developed in research labs and industry across the country.  These devices are designed and built using layered, flat sheets of a wide variety of materials, and folded up to create both form and motion.  This class studies these devices from initial prototype and design through implementation and optimization, with a focus on application-specific projects which seek to solve problems of cost, parallelism, complexity, and time with a relatively fast and easy prototyping method.  

This class allows students to delve deeper into the analytical problems associated with these devices, in topics such as design, manufacturing, dynamics & simulation, optimization, kinematics & motion, and stiffness analysis.


## Class Basics {.allowframebreaks}

### Section Info and Meeting Times
**Class:** EGR557 -- Foldable Robotics  
**Class Schedule:** Monday/Wednesday, 3:00pm-4:15pm   
**Meeting Location:** Polytechnic Campus, Tech 162  
**Course Number:** [26449](https://webapp4.asu.edu/catalog/course?t=2221&r=26449)  
<!--**Group Office Hours:** Friday, 10:30-11:45, Tech 162, Polytechnic Campus-->
<!--**Zoom Link:** Available on <https://my.asu.edu>-->

### Instructor Contact Info

**Instructor:** Daniel M. Aukes  
**E-mail:** [danaukes@asu.edu](mailto://danaukes@asu.edu)  
**Instructor Office:** Tech 152, Polytechnic Campus  
**Office Phone:** 480-727-5851 
<!--**Cell Phone:** 650-353-1241 (during business hours only)  -->

### Office Hours 

Office Hours will held weekly starting week 2 or may be made by appointment.  I will run a survey to identify the best time to hold office hours within my own constraints.  This document will be updated to reflect the official office hours that start week 2.  This document will be updated to reflect up-to-date office hours as needed.

## Prerequisites

There are no formal prerequisites, but students taking _Foldable Robotics_ should be familiar with: 

* Programming fundamentals, ideally in a scripted language like Python or Matlab.
* Linear algebra, differential equations, calculus, trigonometry, vectors, etc.
* Working around rapid prototyping machines, and if not, willing to learn.
<!--* Should be willing to try a different operating system.-->

## Course Objectives

At the end of this course, students will demonstrate proficiency in synthesizing concepts from across a number of engineering domains including robotics, modeling and analysis, optimization, data collection and experimental validation, CAD/CAM design, and manufacturing & rapid prototyping. This includes:

* Using bio-inspired approaches in the development and design of mechanisms
* Understanding the kinematic relationships between forces and motion for rigid mechanical systems
* Understanding the relationships between force and deflection in compliant systems
* Being able to build and use physics-based models for understanding the dynamic motion of robotic systems
* Understanding how the limitations of fabrication processes translate to design constraints and guidelines for laminate systems.
* The basics of data collection and experiment design
* How to use optimization approaches in solving an engineering design problem.

## Expected Learning Outcomes

<!--
### Main Topics

* Foldable Robotics Background
* Introduction to Python
* Biomechanics and Bio-inspiration
* Kinematics, Jacobians, Forces, and Power
* Dynamics
* Compliance and System Stiffness
* Actuator Selection, Characterization, and Integration
* Optimization for model fitting and design improvement
* Prototyping, manufacturing, and computation
* Experimental Validation
* Teamwork, Communication, and Documentation
-->

### Foldable Robotics

* You will be able to identify key innovations in the foldable robotics timeline and their impact.
* You wil be able to identify persistent, recurring, or key mechanisms as well as why they are useful in the context of mechanisms and robotics.
* You will be able to contrast the key differences between origami in the context of art vs how folded systems are used in the development of robotic mechanisms.

### Python

* You will be able to identify and utilize the key differences between data types in writing Python code.
* You will be able to create and use functions for the purposes of modularizing Python code
* You will be able to plot multidimensional tabular data as figures using the matplotlib library.
* You will be able to demonstrate how to perform array and matrix-based operations using the Numpy and Scipy packages
* You will be able to compose and work with symbolic expressions using the Sympy package.
* You will be able to write and compile Jupyter Notebooks for the purposes of documenting your works.

### Biomechanics and Bio-inspiration

* You will be able to search for and critically read through research papers to identify key metrics related to animal locomotion
* You will be able to the biomechanics of a selected organism to a set of initial design goals or specifications.




### Kinematics, Jacobians, Forces, and Power

* Ideate a kinematic mechanism --  prototype it, draw it and demonstrate its motion
* Translate the kinematic rules of a mechanism to a computer program and visualise / plot its motion.
* Interpret the motion of a kinematic end-effector in robotics terms, such as:
    * The input/output speed relationship
    * The output/input force relationship
    * The power transferred during motion
* Utilize numerical or symbolic approaches to obtain the kinematics.

### Dynamics

* Create and populate a rigid body dynamical system composed of
    * Rigid Frames
    * Masses and Inertias
    * Joints
    * Forces
* Model the f=ma relationship of a dynamic system over time.
* Integrate the motion of a dynamic system over time

### Actuator Selection, Characterization, and Integration

* Select an actuator or power-storage mechanism
* Size an actuator or power-storage mechanism based on project specifications
* Model an actuator or power-storage mechanism
* Test an actuator or power-storage mechanism.
* Collect performance / model data on a selected actuator or power-storage mechanism.
* Integrate an actuator or power-storage mechanism into your kinematic mechanism

### Compliance and System Stiffness

* Describe the deflection of a beam using Euler-Bernoulli beam equations
* Model a beam in Solidworks and calculate its deflection under load using FEA.
* Experimentally measure the deflection of a beam and obtain its Young's modulus.
* Create an approximate model for beam compliance and add it to your system dynamics

### Optimization for model fitting and design improvement

* Understand basic approaches for minimizing or optimizing a function
* Use coding-based tools to optimize simple functions and perform a regression.
* Use a data-driven approach to fit unknown model parameters to a real system.
* Use a model-based approach for selecting ideal design parameters using optimization.

### Prototyping, manufacturing, and computation

* Design an origami-inspired mechanism using analog techniques
* Be able to enumerate the various manufacturing considerations of cutting and lamination
* Be able to compute a manufacturing-aware digital design file.
* Make a laminate device using digital techniques (optional)
* Make robots and mechanisms
  * Learn layer-based fabrication steps
  * Make mechanisms using rapid prototyping tools

### Experimental Validation

* Understand best practices for developing an experiment
* Understand ways to reduce noise and variation
* Develop a small experiment and collect data
* Interpret sources of error and corrective actions 

### Team-based project management, communication, etc.

* Develop a computation-focused project website for communicating progress in written form.
* Present work orally to the class

<!--
-->
<!--
### Design & Bioinspiration
* Identifying and conducting background reading on related research from the fields of biomechanics, robotics, and manufacturing.
* Creating origami-inspired mechanisms like a popup book using manual prototyping tools and techniques.
* Using a graphical design program to create a hinged design
* Using a scripting language to create a hinged design
* Distilling bio-inspired motion into a mechanism design
* Utilizing feedback from simulation and/or experimentation to improve design.

* mechanism synthesis techniques using physical prototypes

### Kinematics
* Translating a paper design to a set of coordinates and connections.
* Understanding degrees of freedom, constraints.
* Count DOF for simple mechanisms.
* Creating constraint equations using vectors.
* Solving nonlinear system of equations with Python
* plotting kinematic motion of foldable mechanisms with constraint equations
* Plotting and analyzing the motion of foldable mechanisms using kinematic constraint equations.
* Computing numerical force relationships between actuators and end-effectors using the concept of a Jacobian.
* Computing the optimal gear ratio for a motor given jacobian and motor characteristics.

### Dynamics
* Running a parameter-based dynamics simulation.
* Modifying a parameter-based dynamics simulation.
* Creating a parameter-based dynamics simulation.
* Simulating the motion of dynamic systems.
* Computing the stiffness of a flexible beam using Bernoulli-euler beam theory.
* Computing the stiffness of a composite beam using classical beam theory
* Experimentally determining the stiffness of a beam.
* Using simulations to identify potentially optimal designs.

### Robotics & Mechatronics
* Programming a microcontroller
* Demonstrating motion of an RC Servo Motor
* Integrating sensor signals in a microcontroller
* Collecting data experimentally via sensing
* Displaying experimental data in comparison to a model

## Programming
* Can write a self-contained script capable of computing and analyzing design.  Parameters at the top drive design, manufacturing and analysis.
* Demonstrating proficiency in Python, such as
    * Object-oriented programming techniques using Python
    * Understanding data types
    * Understanding classes
* Producing software packages in Python that give insight into design, robotics, and manufacturing.


### Teamwork and Documentation
* Working in teams to achieve a shared goal
* Presenting work to others via design review presentations
* Responding to and acting on feedback received in public design reviews.
* Writing a final report which documents the design process using all tools learned
* Communicating the essential features of the design and process to the public in outward-facing final videos.
* Documenting each iteration with animations, renderings, photos, and videos in a professional manner
* Retaining all code & design files
* Professionalism in Presentation
    * Homework, reports, and correspondance are clear and well-written.
    * photos/videos are not jerky/blurry do not have cluttered or messy background
    * audio is clean without background noise
    * Videos edited and narrated with a script
    * final project folder is organized according to instructions

### Geometry & Manufacturing
* Extracting and encoding design geometry from/to common file types such as .dxf
* Using constructive solid geometry techniques to construct complex, multi-layer, mechanical designs from design elements such as hinges and holes
* export a laminate to a .dxf file
* fabricate laminate mechanisms
* understand the limitations and constraints of different manufacturing techniques
* Applying the principles of layer-based process constraints to compute manufacturable laminate mechanisms with CSG
* Integrating manufacturing considerations into a design via programming
* Demonstrating rapid prototyping techniques using digital equipment like laser cutters, 3D printers, etc.

-->

<!--

## ASU Sync

This course uses Sync. ASU Sync is a technology-enhanced approach, designed to meet the dynamic needs of the class. During Sync classes, students learn remotely through live class lectures, discussions, study groups and/or tutoring. You can find out more information about ASU Sync for students here, <https://provost.asu.edu/sync/students> and <https://www.asu.edu/about/fall-2020>.

-->

## Textbook, Materials, Equipment, and Personal Laptops {.allowframebreaks}

### Textbook
There is no textbook.  Selected readings from will be provided on Canvas and/or linked to online.

### Software

You will be expected to install and use either the Anaconda distribution of Python, or google colab, for completing all assignments and following along in class.

This class is friendly to all operating systems.  Students have used Window, Ubuntu or OS/X on their own in the past with no problems.

Please see the software list posted on the course site for more information about required and recommended software.  The software listed is either open-source and freely available to download, available through ASU, or free for student use.

### Computers

It is expected that you can bring a laptop to class to complete in-class programming tasks.  

### Materials

Students will be responsible for selecting and obtaining the consumable materials used in their project, such as cardboard, adhesive, plastic, etc.  I may be able to supply a limited number of motors, sensors, and controllers which can be used for development, but if students wish to keep their robots they will need to purchase their own components.

### Equipment

Special equipment for making laminate robots is available  for use on the Poly Campus at your discretion.  If you wish to use the tools and equipment you will need to pass all safety training required by the Innovation Hub and follow all campus public health protocols.  See <https://poly.engineering.asu.edu/innovation-hub/> for more information.

### Checkout {.standout}

Checkout of equipment or reusable parts may be possible through Dr. Aukes, the Innovation Hub, or Peralta Labs.  Any checked-out tools or parts must be returned in order to receive a grade in the class.

### Zoom Policy

If attending class in-person, please bring earbuds and be prepared to use them in team breakout sessions; this is essential to reduce interference and cross-talk.

If attending remotely, you will need the following:

* Reliable home internet for accessing Zoom, Canvas, and other course content.
* A webcam or smartphone with camera for participating in class as well as for data collection.

If you are not able to personally finance the equipment needed to attend class remotely, please inform the course instructor.

<!--
-->

### Other recommended resources

* Adobe Creative Cloud, available to all ASU students for free: <https://uto.asu.edu/adobe-creative-cloud>.
* Microsoft Office ([Microsoft 365](https://myapps.asu.edu/app/microsoft-office-2016-home-usage) is free for all currently-enrolled ASU students)
* Solidwoks, available via <https://myapps.asu.edu>

<!--There are 20 workstations arranged around the perimeter of Tech 162 with computers.  Anaconda is already installed, but it will be difficult to follow along when you're pointed the other direction from the front of the room.  We will use the workstations for your device development, but if you are able, please bring laptops to class.  You'll be able to follow along in the front a lot easier.  If you don't have a laptop that you can bring, we'll try to put you in the closer workstations.
-->


## Project

The final project will involve designing a foldable robot using the methods introduced in this class.   The project will span the entire semester.  Teams of ~4 students will propose a research question they would like to focus on in the realm of foldable robotics.  They will survey the state of research on this topic, and craft a project of appropriate scope (with the guidance of the professor) and depth that can be accomplished in the time frame.   They will then develop a design workflow, analysis, manufacturing plan, a robot, and validating data that supports the design decisions made.

<!--
Each week, students will bring their assignments or projects to class and we will discuss their progress & roadblocks.

The goal for this project is to use all of the things you are learning in foldable robotics in order to create a small, lightweight foldable robot.
-->



# Class Schedule

The class schedule can be found on Canvas.  It is subject to change, and will be updated regularly. It is your responsibility to keep track of all due dates and times, which will all be found on canvas.

<!--**Consulting: ** I will ask that groups find a common time to meet with me for a regular consulting session prior to and throughout their final project, to be used to help identify a unique problem worth solving, and to craft a suitable scope, and to discuss issues, questions, and ideas.-->

<!--Unless otherwise specified, assignments are due before class time (10:30am) on the day it is due.-->

## Tentative Schedule[^1]

| **Week** | **Monday**                                | **Wednesday**                                   |
|:---------|:------------------------------------------|:------------------------------------------------|
| 1        | *Class 1:* Welcome                        | *Class 2:* Foldable Background                  |
| 2        | *Class 3:* Biomechanics I                 | *Class 4:* Laser Training                       |
| 3        | *Class 5:* Biomechanics II / Kinematics I | *Class 6:* Developing a Research Question, etc. |
| 4        | *Class 7:* Project Pitches                | *Class 8:* Kinematics II                        |
| 5        | *Class 9:* Kinematics III                 | *Class 10:* Kinematics IV                       |
| 6        | *Class 11:* Dynamics I                    | *Class 12:* Dynamics II                         |
| 7        | *Class 13:* Dynamics III                  | *Class 14:* Presentation I                      |
| 8        | *Class 15:* Mechanics and Compliance      | *Class 16:* Optimization I                      |
| 9        | *Class 17:* ***No Class: Spring Break***  | *Class 18:* ***No Class: Spring Break***        |
| 10       | *Class 19:* Laminate Fabrication Tutorial | *Class 20:* Manufacturing I                     |
| 11       | *Class 21:* In Class Cutting I            | *Class 22:* Presentation II                     |
| 12       | *Class 23:* Manufacturing II              | *Class 24:* In Class Cutting II                 |
| 13       | *Class 25:* Manufacturing III             | *Class 26:* Consulting / Flex Day               |
| 14       | *Class 27:* Optimization II               | *Class 28:*  In Class Cutting III               |
| 15       | *Class 29:* Experimental Validation       | *Class 30:* Consulting / Flex Day               |
| 16       | *Class 31:* TBD Seminar                   | *Class 32:* Presentation III                    |
| 16       | ***Finals Week***                         | ***Finals Week***                               |

<!--
-->

## Assignments

### Assignment Breakdown[^2]

| Item                |   Points | Percentage |
|:--------------------|---------:|-----------:|
| Individual Subtotal |     1940 |         44 |
| Team Subtotal       |     2450 |         56 |
| **Total**           | **4390** |    **100** |

### Tentative List of Assignments[^2]

#### Individual Assignments

| Week | Name                                                                  | Type                     |   Points |
|:-----|:----------------------------------------------------------------------|:-------------------------|---------:|
| 1    | Python for Loops. Arrays. and Plotting                                | Individual Assignment    |      100 |
| 1    | Make a Pop-up Book                                                    | Individual Assignment    |      200 |
| 1    | Install Python                                                        | Ungraded Individual Task |          |
| 1    | Incoming Survey                                                       | Individual Survey        |          |
| 2    | Install CAD                                                           | Ungraded Individual Task |          |
| 2    | Python Functions                                                      | Individual Assignment    |      100 |
| 3    | Project Pitch                                                         | Individual Assignment    |      100 |
| 3    | Project Selection Survey                                              | Individual Survey        |          |
| 4    | Kinematics Via Prototyping & CAD                                      | Individual Assignment    |      200 |
| 5    | Intro to Kinematics                                                   | Individual Assignment    |      200 |
| 7    | Intro to Dynamics                                                     | Individual Assignment    |      200 |
| 8    | Course Feedback I                                                     | Individual Survey        |       20 |
| 10   | Parameter Identification                                              | Individual Assignment    |      200 |
| 11   | Course Feedback II                                                    | Individual Survey        |       20 |
| 12   | Intro to Manufacturing Computation                                    | Individual Assignment    |      200 |
| 14   | Prototyping                                                           | Individual Assignment    |      200 |
| 15   | Design Optimization, Experiment Design, Data Collection, and Analysis | Individual Assignment    |      200 |
|      | **Individual Subtotal**                                               |                          | **1940** |

#### Team Assignments

| Week | Name                                                                       | Type                   |   Points |
|:-----|:---------------------------------------------------------------------------|:-----------------------|---------:|
| 3    | Develop a Research Question                                                | Team Assignment        |      200 |
| 4    | Biomechanics Background and Initial Specifications                         | Team Assignment        |      200 |
| 6    | Make a Website                                                             | Ungraded Team Task     |          |
| 6    | System Kinematics                                                          | Team Assignment        |      200 |
| 7    | Website Update I                                                           | Team Assignment        |      100 |
| 7    | Presentation I                                                             | Team Assignment        |      200 |
| 8    | System Dynamics I                                                          | Team Assignment        |      200 |
| 8    | Parameter Identification Plan                                              | In-Class Team Activity |       25 |
| 10   | System Dynamics II                                                         | Team Assignment        |      200 |
| 11   | Presentation II                                                            | Team Assignment        |      200 |
| 11   | Website Update II                                                          | Team Assignment        |      200 |
| 13   | Design and Manufacturing Workflow                                          | Team Assignment        |      200 |
| 13   | Design Optimization, Experiment Design, Data Collection, and Analysis Plan | In-Class Team Activity |       25 |
| 16   | Presentation III                                                           | Team Assignment        |      200 |
| 16   | Website Update III                                                         | Team Assignment        |      300 |
|      | **Team Subtotal**                                                          |                        | **2450** |



# How to Succeed in this Course

* Attend all class sessions
* Complete all pre-class preparation assignments and reading
* Complete all post-class follow up assignments and reading
* Participate in office hours
* Check your ASU email regularly
* Log in to the Canvas at least once each week
* Communicate proactively with your instructor
* Create a study schedule so that you don’t fall behind on assignments

# Grading Policies

The goal of assignments is to develop a fundamental understanding of the topics required to create foldable robots, using coding to design, manufacture, and analyze.

## Assignments are on Canvas

Assignments will be posted to Canvas throughout the semester.  It is the student's responsibility to check canvas periodically for announcements and posted material.  Assignments will cover many of the topics presented in class.  

## Type of Assignments

Assigned work may be in the form of a longer-form, weekly assignment intended to teach a new fundamental skill, or it may be a short, small-point-value assignment consisting of tasks that must be completed in order for you to complete other milestones.  Some surveys also have a small number of points assigned to them, to ensure student participation.  In-class work generally serves as a starting point for assigned homework and is typically ungraded, though it may be graded occasionally.  

Please see the _"Rubric"_ section of each assignment for assignment-specific expectations.

## Team vs. Individual Assignments 

Assigned work may be individual in nature or team-based project assignments.  Individual assignments will be graded on an individual basis, and are intended to reflect your own work.  Please use the discussion board feature on Canvas when you have a question. Copying others' work is not permitted. <!--Though you may work with other students to complete an assignment, -->

The grade for team-based assignments will be shared by all participating members.  

## Grading Scale

Final points will receive a letter grade according to the following table:

| Grade |    Range |
|:------|---------:|
| A+    | 97-100.0 |
| A     |  93-96.9 |
| A-    |  90-92.9 |
| B+    |  87-89.9 |
| B     |  83-86.9 |
| B-    |  80-82.9 |
| C+    |  77-79.9 |
| C     |  70-76.9 |
| D     |  60-69.9 |
| E     |   0-59.9 |

## Grading Rubric

Some assignments will be graded according to rubric with number values corresponding to a sliding qualitative scale .  The following is a general description of what each percentage means in this course:

| Description                                                                                                                                                                                                           |   % |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----:|
| Exceeds Expectations. Shows superior effort, quality, mastering of the concepts.  Innovation in the execution of submitted work.  Documentation is publication-ready.                                                 | 100 |
| Above expectations.  Demonstrates full understanding of the problem, and solution is well executed, documented, and presented.                                                                                        |  85 |
| Meets expectations.  Minor mistakes are present, but student demonstrates a general understanding of the concepts.  Documentation present but perhaps not comprehensive.                                              |  70 |
| Below expectations. Some effort shown, though there may be serios flaws in analysis or execution.  Documentation lacking in certain areas.                                                                            |  55 |
| Fails to meet minimum expections.  Minimal effort shown.  Does not show understanding and may not have thought through their methods.  Documentation is lacking substance, clarity, completeness, evidence of effort. |  40 |
| Not submitted, illegible, not readable, not properly linked                                                                                                                                                           |   0 |


<!--
## Peer Grading

Some aspects of the course will utilize student feedback during the grading process, including but not limited to peer evaluations of individual contributions to the project, as well as design review presentations.  Student feedback may be used as a direct grade or considered within the instructor's grade at the instructors' discretion.
-->

## Late Penalities

Due to the nature of this class, failing to turn in an assignment on time affects you and your classmates, as each concept builds on the last.  It is your responsibility to get in touch with the instructor regarding any questions before assignments are due.  Late submissions will lose one letter grade(10%) for every day they are late[^3].  **Any sumbission more than four days late will receive a zero.**  Additionally, due to the nature of the submission process, **late CATME assignments will not be accepted.**

All assignments must be submitted to Canvas by the date and time noted in Canvas.

<!--
557 Projects must participate in the Innovation Showcase on Friday, April 27.  Individual attendance is not required, but team attendance is.  Students should coordinate with their team and instructor to ensure that their project can be operated or displayed for the entirety of Innovation Showcase.
-->

## Submitting and Presenting work

Assignment submissions must follow the "Submission Best Practices" document shared on Canvas.  It outlines the expectations for well written assignments, reports, and presentations.

Assigned homework will be submitted for grading several different ways.  This is always indicated in the _"Submission"_ section of each assignment.

* It may be submitted for grading via Canvas.  
* Other work involving external tools (Google Surveys, CATME, etc) will be graded based on submitting to that external tool.  
* Some work will be presented in front of the class, and the grade derived from the presentation.  
* Other work will be compiled into the design notebook (in the form of a website or report) and graded priodically.

**_It is the student's responsibility to pay close attention to each assignment's submission instructions, as each assignment indicates the method by which the work must be submitted for grading.  Failure to submit work in the manner asked for in each assignment will result in a zero._**

# Course Policies

## Attendance & Participation {.allowframebreaks}

### Summary

* Attendance is **required**.  More than two absences result in -2% grade reduction per missed class.
* Absences and Tardies are treated the same
* Coordinate with fellow students to take notes if you are gone.
* Email me at once of technical difficulties over Zoom, but try to reconnect ASAP using other technology (Hotspot, cell-phone, call-in, etc.)

<!--
* Attend in-person or over Zoom, _however_ attendance is taken over Zoom, so **always sign on to Zoom**, even if attending in person
-->

### Details

This class is structured so that it can only be successful with your attendance.  Classes will be interactive, and will require you to come with questions, answers, and ideas to discuss.  Students should notify me if they will miss class, although this does not excuse them from learning the concepts or turning in their assignments on time.  

Missing more than **two** classes will result in noticeable penalties to students' grade, in the form of -2% off the student's final grade per missed class over two.[^4]

Please coordinate with your fellow students to make sure someone takes notes during class if you will be unavoidably gone.

If you are attending remotely, attendance _over Zoom_ will be required to count your participation.  Attendance will be taken each class by taking a snapshot of the Zoom participant list; this may occur more than once per class.  Students are expected to sign in to Zoom on time, as important issues are often introduced within the first few minutes of class.  Tardies are thus treated as absences.  If a student is found to be either absent or inactive on Zoom, they will be counted absent.

In the case of technical difficulty preventing your from attending via Zoom, please contact the instructor right away over email and explain the situation.  Please try another means of reconnecting to zoom, such as over your cell-phone (by calling in or by using the Zoom app).

<!--
As this is a Sync-enabled course, however, in-person attendance is not required.  It is possible to complete all assigned work remotely.  

_Attending the class in person doesn't change any of the above requirements.  You will still be required to sign in to Zoom to participate and be counted present._



-->


### Accommodations

Attendance and participation in class activities is an essential part of the learning process, and students are expected to attend class regularly. Some absences are, however, unavoidable. Excused absences for classes will be given without penalty to the grade in the case of (1) a university-sanctioned event [ACD 304-02]; (2) religious holidays [ACD 304-04; a list can be found here https://eoss.asu.edu/cora/holidays ]; (3) work performed in the line-of-duty according [SSM 201-18]; and (4) illness, quarantine or self-isolation related to illness as documented by a health professional.

Anticipated absences for university-sanctioned events, religious holidays, or line-of-duty activity should be communicated to the instructor by email at [danaukes@asu.edu](mailto://danaukes@asu.edu), at least 2 days before the expected absence.

Absences for illness, quarantine or self-isolation related to illness should be documented by a health professional and communicated to the instructor as soon as possible by email at [danaukes@asu.edu](mailto://danaukes@asu.edu).

Excused absences do not relieve students from responsibility for any part of the course work required during the period of absence. Faculty will provide accommodations that may include participation in classes remotely, access to recordings of class activities, and make-up work.

If there is a disagreement as to whether an absence should be accommodated, the instructor and student should contact the academic unit chair immediately for resolution.

<!--We will coordinate on the first day of class to determine an appropriate way to submit assignments and projects.  They will be due before class on the day indicated; this process will likely be automated,  so late assignments will not be recorded(or automatically marked as late).  It will be your responsibility to submit late assignments to me *via email* as well.  The date and time the email was received will determine the number of late days.-->

<!--
Students are allowed **five** late days to submit individual assignments, to be used as they see fit.  There are no late days available for group assignments or projects.  It is the responsibility of students to keep track of the number of late days they have used.
-->


# Classroom Behavior {.allowframebreaks}

## Novel Coronavirus 

[ASU returned to on-campus instruction in Fall 2021](https://www.asu.edu/about/fall-2021). The [ASU Face Cover Policy](https://www.asu.edu/about/fall-2021#face-coverings) requires the wearing of face covers in the majority of classrooms, teaching laboratories, studios and workshop settings. 

**_The space for this class has been designated as a space requiring face covers. Please wear a face covering over your nose and mouth at all times during class for the health and safety of yourself and others._**

For the most up-to-date information, please visit the [ASU Novel Coronavirus website](https://eoss.asu.edu/health/announcements/coronavirus/faqs).

### Summary

* Keep all communication professional
* Turn off all cell phones, pagers, and other personal devices when participating in class
* Use your laptops for classroom activities, not email, chats, web browsing, or other non-class related activities.

### Details

#### Professional Communication
Professional Communication in all forms is required.  This includes proper dress when attending class remotely and in-person.  Please refrain from using any background images in your zoom video feed, though you should consider blacking out your background for privacy and professionalism.

#### Cell phones, pagers, and other personal devices
Cell phones, pagers, and other personal devices must be turned off during class to avoid causing distractions.  The use of recording devices is not permitted during class.  Any violent or threatening conduct by an ASU student in this class will be reported to the ASU Police Department and the Office of the Dean of Students.  

#### Use of laptops in class
Laptops are strongly suggested for this course.  You may use your laptop to take notes, during tutorial sessions, or when giving presentations.  Please do not use class time for emails, chats, web browsing, or other non-class related activities.

## Reorganizing a Team 

### Summary
* Please try to work out any team-based issues.
* Please see me if the team is not working.  I may choose to split the team


### Details

Reorganizing teams is not a desired outcome of a group project but is sometimes necessary if dysfunction rises to a level that it cannot complete the project.  One or more teammates or the instructor may initiate the process to split or reorganize a team.  Splitting teams does not necessarily work in any members' best interests, as team-based Team Assignments, which each team member must contribute to, are afterwards spread across fewer people. 

However, if the need arises, members must work with the professor to outline the issues which are creating the need to reorganize and the measures which remaining teammates may take to rectify the situation.  This can take the form of changes made to communication, workload reallocation, new meeting times, etc.  The professor will have the final say in establishing a set of expectations for the team, which must be met within a week.  If members fail to live up to these expectations, the team may be split and reorganized, as deemed necessary by the instructor.

When reorganiztion occurs, each new team will set up their own folders starting with the former team's work, but  new material will be created by the new team, and old material adapted based on the new direction of each new team.  Any changes to the project definition due to the split (such as project scope, performance specifications, timeline, etc) will need to be coordinated with the instructor for all future submissions or presentations.

## {.standout}
**The instructor has the final say in the establishment and reoganization of teams.**

## Academic Integrity {.allowframebreaks}

This class is meant to teach you how to create and use your own design tools for creating folding robots using a variety of published resources, online resources, and classroom content.  I encourage you to plumb the depths of what's available; through this synthesis you might be able to create something unique.  However, I expect to be able to tell what is your work and what is someone else's.  For this reason, specific rules for this class are:


### Specific Rules
* Do your own work for individual assignments and tests.
* Include the your sources of inspiration within assignments and projects.  This will help grow the list of cool references, but more importantly, help distinguish inspiration from wholesale plagarism.
* Keep code/text/information you use from outside sources separate from your own original content (through the use of separate folders, for example).  Make it explicit what is yours and what is not.
* Include all the licenses or copyright statements as required by the things you reuse.  This will make your own code more reuseable for yourself and potentially others in the future.
* See <https://provost.asu.edu/academic-integrity/policy> for more info.

Students in this class must adhere to ASU’s academic integrity policy, which can be found at <https://provost.asu.edu/academic-integrity/policy>. Students are responsible for reviewing this policy and understanding each of the areas in which academic dishonesty can occur. In addition, all engineering students are expected to adhere to both the ASU Academic Integrity Honor Code and the Fulton Schools of Engineering Honor Code. All academic integrity violations will be reported to the Fulton Schools of Engineering Academic Integrity Office (AIO).  The AIO maintains record of all violations and has access to academic integrity violations committed in all other ASU college/schools. 

## Recordings

Note that class sessions may be recorded, and recordings provided to enrolled students, instructors or instructional support personnel as deemed necessary by the course instructor. If you have concerns about being recorded, please contact the course instructor.

## Copyright 

All course content and materials, including lectures (Zoom recorded lectures included), are copyrighted materials and students may not share outside the class, upload to online websites not approved by the instructor, sell, or distribute course content or notes taken during the conduct of the course (see [ACD 304–06](https://www.asu.edu/aad/manuals/acd/acd304-06.html), "Commercial Note Taking Services" and ABOR Policy [5-308 F.14](https://public.azregents.edu/Policy Manual/5-308-Student Code of Conduct.pdf) for more information).

You must refrain from uploading to any course shell, discussion board, or website used by the course instructor or other course forum, material that is not the student's original work, unless the students first comply with all applicable copyright laws; faculty members reserve the right to delete materials on the grounds of suspected copyright infringement.

## Policy against threatening behavior, per the Student Services Manual, [SSM 104–02](https://www.asu.edu/aad/manuals/ssm/ssm104-02.html)

Students, faculty, staff, and other individuals do not have an unqualified right of access to university grounds, property, or services. Interfering with the peaceful conduct of university-related business or activities or remaining on campus grounds after a request to leave may be considered a crime. All incidents and allegations of violent or threatening conduct by an ASU student (whether on- or off-campus) must be reported to the ASU Police Department (ASU PD) and the Office of the Dean of Students. 


<!--All students in this class are subject to ASU’s Academic Integrity Policy (available at <http://provost.asu.edu/academicintegrity>) and should acquaint themselves with its content and requirements, including a strict prohibition against plagiarism.  All violations will be reported to the Dean’s office, who maintain records of all offenses.  Students are expected to abide by the FSE Honor Code (<http://engineering.asu.edu/integrity/>).
You are also expected to abide by the [Computer, Internet, and Electronic Communications Information Management Policy](http://www.asu.edu/aad/manuals/acd/acd125.html).-->

<!--# Background
This class is emerging from a class called *Informal Robotics*, taught at the Harvard Graduate School of Design in 2015 and 2016.  This class was developed by Chuch Hoberman, Daniel Aukes, and Jonathan Grinham, and introduced this and similar manufacturing methods to a group of mostly graduate students in design along with students from Harvard College, the School of Engineering and Applied Science, and MIT Engineering Students.  Classes paired lessons on the essentials of design, deployable structures, kinematics, manufacturing, and mechatronics, while presentations by guest researchers provided the context by which students understood the impact these new prototyping methods are having in research labs.  This class was the first joint collaboration between the Wyss Institute and the Harvard Graduate School of Design, and resulted in a symposium titled "Informal Robotics" in October 2016 which brought several high-impact researchers to the GSD to speak about their work in the field.   
-->

<!--# Course Activities

The following activities will occupy the majority of your time in this class:

* Reading and research.
* Design & fabrication of laminate robots using rapid prototpying techniques.
* Completing assignments and projects by programming in Python
-->



<!--
## Proposed Focus
Laminate Robotics will focus more deeply on the engineering topics required to be able to develop not only this class of devices, but to enable students to craft their own design tools from scratch as new manufacturing methods emerge from the research lab.  This class will focus on topics essential to robot designers, from kinematic and dynamic analysis and simulation, to strength of materials and FEA.

### Kinematics
The kinematics of laminate devices is inherently complex, because the network of folds created in 2D are spherical, nonlinear, and begin moving from a kinematic singularity.  All of these factors makes it non-intuitive to visualize and design motion from a network of rotational hinges.  We will introduce the concept of reference frames, degrees of freedom, and transformations, and demonstrate how these tools can be applied to serial and parallel systems consisting of rotational and translational elements.
- Suggested reading: McCarthy

### Dynamics
Extending on the kinematics section, we will discuss the concepts of stiffness and damping as a function of the material properties of these multi-material systems, and analyze and discuss the impact rotational stiffness can have on an ideal kinematic system.  While the materials are typically lightweight, weight and inertia can also play a role in systems dominated by soft passive elements.  We will introduce tools for creating equations of motion and simulating multi-rigid-body systems.
- Suggested Reading: Kane

### Simulation
Students will be introduced to the basics of dynamic simulation and be given the opportunity to create a simulation for a particular dynamic system.  Performance of their device will be evaluated across several scenarios and parameter sets, with students being asked to find and optimize designs.

### Manufacturing
The analysis of flat laminate systems requires pairing an understanding of the mathematical representation of laminates with the abilities, constraints, and limitations of the manufacturing methods used to make them.  We will introduce concepts such as constructive solid geometry, tool workspace, assembly/disassembly in order to provide students an understanding of manufacturability for this process.
- Suggested Reading: ?

### Stiffness Analysis
As these systems are composed of materials as soft as plastic, paper, and cardboard, and as rigid as fiberglass, carbon fiber, and steel, there can be a wide range of performance with respect to the material systems used.  However, it has been observed that the precise kinematics of such systems can deviate widely from nominal in the presence of links which bend and deform under load.  This can have the effect of increasing the effective degrees of freedom, permitting unintended bending and twisting, which can result in shorter system lifespan and unintended, unmodeled behavior.  We will introduce the basic elements of FEA in order to analyze system performance.
-->
<!--
## Final Projects

### Design Tool Creation
We will ask students to create a design tool for a novel manufacturing system, programmed in Python.  This  project will permit students to create reusable planning software which they can use to

### Simulation Project
Simulate the performance of a class of designs, find global optimum

### Controls & Optimization
Create a controller which can be optimized for a quadruped / hexapod walking robot.

### Robotic Application
Make a robotic or active laminate device that encodes unique motion through a novel transmission design

-->


## Disability Accommodations {.allowframebreaks}


Suitable accommodations will be made for students having disabilities. Students needing accommodations must register with the ASU Disabilities Resource Center and provide documentation of that registration to the instructor. Students should communicate the need for an accommodation in sufficient time for it to be properly arranged. See [ACD 304-08](https://www.asu.edu/aad/manuals/acd/acd304-08.html) Classroom and Testing Accommodations for Students with Disabilities.  

The Americans with Disabilities Act (ADA) is a federal antidiscrimination statute that provides comprehensive civil rights protection for persons with disabilities. One element of this legislation requires that all qualified students with documented disabilities be guaranteed a learning environment that provides for reasonable accommodation of their disabilities. If you believe you have a disability requiring an accommodation please contact the Disability Resource Center at ASU Polytechnic located in Student Affairs Quad # 4 or call 480-727-1039 / TTY: 480-727-1009.  Eligibility and documentation policies are online at:  <http://www.asu.edu/studentaffairs/ed/drc/>


## Harassment and Sexual Discrimination {.allowframebreaks}


Arizona State University is committed to providing an environment free of discrimination, harassment, or retaliation for the entire university community, including all students, faculty members, staff employees, and guests. ASU expressly prohibits discrimination, harassment, and retaliation by employees, students, contractors, or agents of the university based on any protected status: race, color, religion, sex, national origin, age, disability, veteran status, sexual orientation, gender identity, and genetic information.

Title IX is a federal law that provides that no person be excluded on the basis of sex from participation in, be denied benefits of, or be subjected to discrimination under any education program or activity.  Both Title IX and university policy make clear that sexual violence and harassment based on sex is prohibited.  An individual who believes they have been subjected to sexual violence or harassed on the basis of sex can seek support, including counseling and academic support, from the university.  If you or someone you know has been harassed on the basis of sex or sexually assaulted, you can find information and resources at <https://sexualviolenceprevention.asu.edu/faqs>. 

As a mandated reporter, I am obligated to report any information I become aware of regarding alleged acts of sexual discrimination, including sexual violence and dating violence.  ASU Counseling Services, <https://eoss.asu.edu/counseling> is available if you wish to discuss any concerns confidentially and privately. ASU online students may access 360 Life Services, <https://goto.asuonline.asu.edu/success/online-resources.html>. 

## Student Support Services {.allowframebreaks}

* ASU Libraries - offers 24/7 access to librarians through "Ask a Librarian" online chat and help by librarians in person at the Reference Desk during most hours the libraries are open. <http://www.asu.edu/lib/>
* Counseling and Consultation – provides confidential mental health and career counseling services for all ASU students. <http://www.asu.edu/studentaffairs/counseling/>
* Learning Resource Center – provides students with academic support services such as tutoring, peer advising, computer assisted instruction, and supplemental instruction.  Offers both free and fee-based services.  <http://www.asu.edu/vpsa/lrc/>
* Writing Center – provides on-site tutors to help students increase their confidence as writers and improve writing skills free of charge.  <http://www.asu.edu/duas/wcenter/>
* Career Services – offers assistance to students in choosing a major, setting career goals, interviewing and job hunting strategies. <http://career.asu.edu/>
* Student Financial Aid Office – offers information and applications for student funding such as grants, loans, scholarships and student employment. <http://www.asu.edu/fa/>
* Student Health and Wellness Center – provides non-emergency medical health care to all ASU students regardless of insurance status. Most visits with a physician or nurse practitioner are free of charge, but fees will be incurred for x-rays, lab results, etc., <http://www.asu.edu/health/>
* Student Recreational Center – offers individual and group fitness opportunities, as well as information on nutrition and wellness, and massages. Use of the general facilities (weights, circuit training and cardio machines) are free, other services (yoga classes, massages) are fee-based.  <http://www.asu.edu/src/>
* Student Legal Assistance – provides legal advice and counsel free of charge to all ASU students in areas such as landlord-tenant law, credit reports and collection issues, taxability of scholarships and grants, etc. Notary service is also available at no charge. <http://www.asu.edu/mu/legal/>
* Help Wiki – provides a frequently asked questions resource for technology users at ASU. <http://wiki.asu.edu/help/>
* EMPACT Crisis Hotline – offers free 24-hour support for mental health crises. Call (480) 784-1500 in the Phoenix area, (866) 205-5229 for the toll-free number outside of Phoenix, and (480) 736-4949 for the sexual assault hotline. All services are free and confidential. <http://www.empact-spc.com/>


<!--
# Data Collection for Research Purposes

You will be given more information and an opportunity to participate in research investigating effective teaching methods with regard to manufacturing topics.  This will involve collecting assignment and project submissions as well as physical artifacts that you build in class for the purposes of studying effective teaching and learning practices with regards to building manufacturing knowledge.  I will also collect samples of your work, video submissions you make, and final presentations.  For more information, please refer to the disclosure form, which you will receive on the first day of class.
-->
## Notice {.standout}
Any information in this syllabus (other than grading and absence policies) may be subject to change with reasonable advance notice.

[^1]: The Schedule is subject to change.
[^2]: Assignments, totals, relative weighting, and due dates are subject to change with appropriate warning.
[^3]: meaning 10% of the total possible number of points
[^4]: counted as 2% of total points.
