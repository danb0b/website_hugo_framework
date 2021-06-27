---
bibliography: ../../project/bibliography.bib
csl: ../../project/ieee.csl
title: Foldable Robotics Background
type: submodule
description: A short history of foldable robotics
---

# Foldable Robotics Background

## Laminate Fabrication Techniques

![[@Pister1992]](../../figures-external/background/Picture1.png)

Foldable, laminate, and origami-inspired robots have origins in early MEMS work using planar processes to make three-dimensional mechansims in silicon [@Pister1992], where $\mu m$-scale hinges were fabricated in silicon to create articulated assemblies which folded out of a 2D plane.  These devices were fabricated using layered MEMS techniques. Follow on work by this group combined actuation with mechansims to create motion [@Yeh].  Magnets were also used to actuate and erect pop-up structures [@Yi1999]. This work was later echoed and expanded in [@Vaccaro2003; @Stellman2005].  At the heart of the technologies that make these robots feasible is the concept of being able to create complex,  nonlinear motion through the synthesis of common mechanical elements such as joints, springs, dampers, actuators, and sensors.  Unlike common mechanical elements found in more traditional robotic systems, however, these components are fabricated with a collection of planar fabrication techniques in which a palette of compatible materials are iteratively added and removed to create a monolithic, multi-material, electro-mechanical system.  These concepts have been demonstrated at nano, micro, milli, and centi-meter scales, in materials as disparate as silicon [@Pister1992], carbon fiber[@Wood2003], titanium [@Sreetharan2012], plastic, and cardboard [@Birkmeyer2009].  These technologies make it possible to solve novel problems, either at size scales where traditional mechanical devices such as gears, bearings, and motors are unavailable, or at cost-scales which envision industrial-scale processes fabricating large numbers of cheap robots [@Cybulski2014; @Shigemune2015; @Niiyama2015].

The ideas of foldable mechanisms have been realized by solving a number of problems related to design, fabrication, assembly, and 

* design - tools for making design process go faster and for plannig manufacturing
* manufacturing - methods for automating fabrication and utilizing planar processes
* assembly - self folding techniques, support structures

Foldable devices have been used to address issues in bio-inspired locomotion such as walking (Hoover, 2008), running (Birkmeyer 2009), (Haldane, 2013), (Mulgaonkar, 2018), jumping [@Koh2013; @Jung2014], and flying [@Teoh2012].  A variety of strategies for actuating and powering foldable devices has also been investigated [@Sitti2003; @Karpelson2008; @Niiyama2014].

### Robots
Laminate fabrication techniques have recently gained attention as a complete solution for rapidly developing active mechanisms at small scales for use in robots that fly [@Sreetharan2012; @Teoh2012; @Jafferis2019], walk [@Hoover2008a; @Zhakypov2017], and run[@Hoover2010a; @Birkmeyer2009; @Baisch2014; @Mulgaonkar2016]. Laminate devices can be manufactured quickly using a variety of materials such as carbon fiber, fiberglass, or cardboard, which plays a role in determining system stiffness[@Sreetharan2012]. These robots may also be generated in an automated or semi-automated fashion from basic user needs[@Aukes2014a; @Mehta2014; @Mehta2015; @Schulz2017]. A variety of sensing modalities are compatible with laminates, including capacitive [@Atalay2017; @Shin], optical[@Gafford2016], inductive[@Shin] and strain[@Gafford2013b; @Sun2015] based sensing modes. These sensors may be powered through conductive layers within the laminate itself; this has been demonstrated for self-folding [@Felton2013a; @felton_method_2014] and sensing and communication[@Gafford2017]. High-speed quadruped robots made using laminate techniques represent some of the fastest robots for their size; they have demonstrated speeds of up to 10 body lengths per second at \~1 g scales [@Baisch2014] and up to 47 body lengths per second [@Haldane2015] at \~50 g scales.

### Design Tools

While these robots have continued to be developed and demonstrated across a variety of niche-based tasks, more is now understood about how to design [@Aukes2014], plan for manufacturing [@Aukes2014a], and analyze these robots.  A number of design tools have been developed for understanding the motion created from hinged, origami-inspired designs using FEA-based approaches [@Shenk2011], for enunciating functional needs and combining modular elements [@Mehta2015], or for analytically understanding the resulting dynamics of these devices [@Doshi2015; @Khodambashi2018].  This is necessary due to the dependence upon flexure-based hinges which rely on material deformation to create virtual joints, which can affect system stiffness and damping.

<!--
| Tool                    | Author  | Link | Citation |
|:------------------------|:--------|:-----|:---------|
| Treemaker               | Lang    |      |          |
| Origamizer              | Tachi   |      |          |
| Rigid Origami Simulator | Tachi   |      |          |
| popupCAD                | Aukes   |      |          |
| ?                       | Mehta   |      |          |
| ?                       | Mueller |      |          |
|                         | Sung    |      |          |
-->

### Self-folding

As origami  technicques have been increasingly used as engineering solutions, researchers have sought ways to address the need to create and fold shapes automatically using either active materials or embedded actuation.  Self folding structures have been realized using shape memory alloys [@Hawkes2010; @Paik2012; @Peraza-Hernandez2014a], light-based stimulation [@Liu2012; @Ryu2012],  lasers[@Laflin2012], shape memory polymers [@Felton2013; @Tolley2013; @An2014; @Miyashita2013a; @Mao2015; @Felton2015a], and paper-based actuators [@Shigemune2015; @Hamedi2016].  A comprehensive review can be found in [@Peraza-Hernandez2014].  Self-folding principles can beused to create morphing structures [@Miyashita2017]


### My Work

My research as a PhD student at Stanford University, postdoctoral researcher in the Harvard Microrobotics Lab and currently as the principal investigator of the IDEAlab at Arizona State University has contributed to the literature surrounding the automated design, manufacturing, and analysis of foldable robotic systems, including the representation and computation of laminate systems[@Aukes2014], algorithms tailored to compute manufacturable robots[@Aukes2014a], and generating and solving the dynamics of parallel laminate mechanisms using experimentally-determined models[@Doshi2015c; @Khodambashi2018]. This work has resulted in several design tools, including **popupCAD**, a design and manufacturing planning tool for developing laminate robotic systems. More recent work in our lab has explored the use of machine learning approaches to learn or improve robotic system control in the real world. We have been applying the CMA-ES algorithm for identifying optimal gait parameters and finding preferred fin designs for a fish-inspired swimming robot [@Sharifzadeh2018a; @Sharifzadeh2019]. We have used other techniques such as neural networks to learn the nonlinear kinematics of a spherical five-bar linkage in [@Sharifzadeh2019a]. Furthermore, we have used a a sample-efficient reinforcement learning strategy with a turtle-inspired robot design that drags itself across a sandy surface to compare locomotion strategies learned in the lab against similar experiments performed in the Arizona desert [@Luck2017; @Jansen2017].

Our lab's research into the development, modeling, and experimental validation of robotic systems can be found across a number of journal and conference papers, including foldable linkage kinematics [@Shuch2019], underwater swimming gaits [@Sharifzadeh2018a; @Sharifzadeh2019] and laminate mechanism dynamics [@Doshi2015c; @Khodambashi2018]; we have applied experimental validation to specific platforms including laminate jumping robots [@Knaup2019], foldable-robotic quad-rotors, [@Yang2019; @Mulgaonkar2016], jump-gliding devices [@Lighthouse2019], and hydrogel-based gait controllers[@Khodambashi2019]. Prior work in robotic hands and grasping includes the modeling of force interactions between compliant, underactuated hands and externally grasped objects while considering contact and friction. These models were used to optimize hand designs as well as used to understand grasp acquisition and retention[@Aukes2011; @Aukes2012; @Aukes2013; @Aukes2013a; @Aukes2014d; @Stuart2014].

## Terminology

The same types of device have been described by a large number of different terms, including "SCM", "nanostructured origami", "pop-up book MEMS", "printed-Circuit MEMS(PC-MEMS)", "origami-inspired robots", "printable robots", "lamina-emergent mechanisms", "informal robots", "laminate robots", "foldable robots", "robogami", and "print-and-fold origami"


<!--
The table below describes many of the most common terms for foldable mechanisms.

| Term                           | Author       | Citation |
|:-------------------------------|:-------------|:---------|
| Articulated Microrobots        | Pister       |          |
| SCM                            | Fearing      |          |
| Nanostructured origami         | Barbastathis |          |
| "Pop-up book" MEMS             | Wood         |          |
| Printed-Circuit MEMS (PC-MEMS) | Wood         |          |
| origami-inspired robot         | Rus          |          |
| printable robot                | Rus          |          |
| Lamina-emergent mechanisms     | Howell       |          |
| Informal Robots                | Hoberman     |          |
| Laminate robots                | Aukes        |          |
| Foldable robots                | Aukes        |          |
| Robogami                       | Paik         |          |
| print-and-fold origami         | ?            |          |
-->

<!--

## Timeline

*  1992 - 1996

    ![[@Pister1992]](../../figures-external/background/Picture1.png)


    ![[@Yeh]](../../figures-external/background/Picture2.png)                   

    ![[@Reid1998]](../../figures-external/background/Picture4.png)              

### 1998 

 ![[@Shimada2000]](../../figures-external/background/Picture5.png)           

### 2000 

 ![[@Fearing2000]](../../figures-external/background/Picture6.png)           

### 2001 

 ![[@Yan]](../../figures-external/background/Picture7.png)                   

### 2003 

 ![[@Sahai2003]](../../figures-external/background/Picture8.png)             

 ![[@Wood2003]](../../figures-external/background/Picture9.png)              

### 2004

  ![[@Buchner2004]](../../figures-external/background/Picture10.png)   
         
###  2005 

 ![[@Avadhanula2005]](../../figures-external/background/Picture11.png)      

 ![[@Wood2005]](../../figures-external/background/Picture12.png)            
 
### 2006 

 ![[@Sahai2006]](../../figures-external/background/Picture13.png)          
  
### 2008 

 ![[@Hoover2008]](../../figures-external/background/Picture14.png)          

 ![[@Wood2008a]](../../figures-external/background/Picture15.png)           

 ![[@Hoover2008a]](../../figures-external/background/Picture16.png)         

### 2009 

 ![[@Birkmeyer2009]](../../figures-external/background/Picture17.png)       

### 2010 

 ![[@Hoover2008a]](../../figures-external/background/Picture20.png)          
 
  ![[@Hawkes2010]](../../figures-external/background/Picture24.png)    
        
###  2011

 ![[@Peterson2011]](../../figures-external/background/Picture18.png)        


 ![[@Peterson2011a]](../../figures-external/background/Picture22.png)       

 ![[@Hoffman2011]](../../figures-external/background/Picture27.png)    
      
###  2012 

 ![[@Sreetharan2012]](../../figures-external/background/Picture28.png)      

###  2013 

 ![[@Koh2013a]](../../figures-external/background/Picture19.png)            

 ![[@Haldane2013]](../../figures-external/background/Picture21.png)         

 ![[@Lee2013b]](../../figures-external/background/Picture23.png)            

 ![[@Lee2013a]](../../figures-external/background/Picture25.png)            

 ![[@Kohut2013]](../../figures-external/background/Picture26.png)           

 ![[@Felton2013]](../../figures-external/background/Picture29.png)          

###  2014 

 ![[@Baisch2014]](../../figures-external/background/Picture30.png)          

![[@Felton2014]](../../figures-external/background/Picture31.png)          

###  2015

 ![[@Miyashita2015a]](../../figures-external/background/Picture33.png)      

 ![[@Firouzeh2015]](../../figures-external/background/Picture36.png)    
 
 [@Haldane2015]

###  2016 

 ![[@Mulgaonkar2016]](../../figures-external/background/Picture32.png)      

 ![[@Wang2016]](../../figures-external/background/Picture38.png)            

### 2017

 ![[@Overvelde2017]](../../figures-external/background/Picture34.png)       

 ![[@Karras2017]](../../figures-external/background/Picture35.png)          

 ![[@Li2017]](../../figures-external/background/Picture37.png)              

 [@Zhakypov2017]                                                

 ![[@Schulz2017]](../../figures-external/background/Picture39.png)          

###  2018 

 ![[@McClintock2018]](../../figures-external/background/milliDelta-6168.jpg)

-->

<!-- Todo Term | Author | Papers | Year of appearance-->



<!--
| Workflow                | Kwon    |
-->

<!--
At this point, a large number of laminate devices has been created, and -- like traditional robotics -- there is a wide range of purposes for these devices.  Many are bio-inspired: flying, crawling, walking, and jumping feature heavily in the capabilities of these robots.  They are often small.  Almost all fit in your hand, and some weigh on the order of tens of grams.

Method Papers
------



Terrestrial
------------

| Robot          | Lab             |
|:---------------|:----------------|
| Roach          | SMA             |
| DynaRoaCH      | Geared DC Motor |
| HAMR I-IV      | SMA             |
| HAMR V         | Piezo           |
| DASH           | Geared DC       |
| Dash with pogo |                 |

Flying
-------
| Robot              | Lab   |
|:-------------------|:------|
| RoboBee            | Wood  |
| Intermittent Flyer | Sahai |
| Flying Monkey      | Koh   |

Bio-inspired
-------

| Robot                 | Lab |
|:----------------------|:----|
| flea                  |     |
| water strider         |     |
| Inchworm              |     |
| Self-folding inchworm |     |

Wheeled
-------
| Robot | Lab |
|:------|:----|
|       |     |

Arms
-----
| Robot | Lab |
|:------|:----|
|       |     |
Hand / Gripper
----------
| Robot    | Lab     |
|:---------|:--------|
| Tweezers | Gafford |

Self-folding
---------
| Robot     | Lab    |
|:----------|:-------|
| ?         | Shuhei |
| ?         | Felton |
| ?         | Tolley |
| SMA-Based | Paik   |

Origami

Tachi

<!--
Origami
* Miura
* Tomohiro Tachi
* Robert Lang
* Eric Demaine
* Rigid Analysis

Design Community
* Deployable Structures

Who's big in this community?

* Kyujin Cho
* Jamie Paik
* Rob Wood
* Ranjana Sahai
* Sam Felton
* Mike Tolley
* Dan Aukes(me)
* Zhi Ern Teoh
* Larry Howell
* Ron Fearing
* Aaron Hoover
* The Team @ Dash Robotics
* Cagdas Onal
* Onur Ozcan
* Ben Goldberg
* Neel Doshi
* Sheila Russo
* Tomasso Russo

-->

<!--
-->
