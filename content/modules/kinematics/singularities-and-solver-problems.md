---
title: Singularities and Solver Problems
type: submodule
bibliography: ../../project/bibliography.bib
csl: ../../project/ieee.csl
---

# Singularities and Solver Problems

Many of the devices you will prototype are highly nonlinear mechanisms which may have certain charactersitics which are hard to solve for in your typical CAD sketcher.

Singularities can be described as a mathematical or mechanical condition in which one or more degrees of freedom of your device or of your description of the device -- can no longer be controlled or solved for. A typical kinematic singularity may be seen

## Mechanism Singularities

![Singular Kinematics](../../figures/design/singular_kinematics.png){class="img-fluid"}

One of the biggest challegnes of foldable devices is that they all start off flat. Which means they all start off in a mechanism singularity. This is probably the worst way to start, as it means that the device, when assembled or erected into its final configuration, could be pushed into more than one valid state. Furthermore, if designed wrong, a mechanism may slip past a singularity and be unable to escape it. This is exacerbated by the fact that foldable mechanisms cannot rotate freely more than +/- 180 degrees, meaning that you have to go back the way you came, rather than rotate through a second singularity.

This means that the user has to take care during the design process to avoid mechanism singularities during assembly and operation.

## Representational Singularities

Another type of singularity occurs when the mathematical framework used to describe your mechanism loses a degree of freedom due to redundancy in the description. A trivial example would be using a three-dimensional space to describe a planar mechanism. Consider a four-bar mechanism for example, in which all of the vectors used to describe the mechanism exist in the x-y plane. If you use a three-dimensional description, ie, include the z values for all the points in your mechanism -- then solving for your system will always result in a singular matrix, as the column of z values may take any value and still produce a consistent and valid mechanism. Even though the mechanism may be in a valid configuration, the description cannot be used to solve for it.

## Solver problems

The solvers used to solve a constrained sketch are typically fairly robust, as they must permit interaction with human designers in such a way that humans can drag sketch elements around throughout the sketch's degrees of freedom, yet must also remain accurate. However, these sketchers often have some problems associated with them that you will also see in complex, nonlinear assemblies. First, the software may not always expose all the degrees of freedom or permit the user to freely drag sketch elements around in an inuitive fashion. A user may see only one or two degrees of freedom when the sketch has many more which are simply not moving in accordance to the user's specific motion commands. There are several ways to explore the degrees of freedom of a device with more surety

* Lock all degrees of freedom but one - You can either fix elements or establish temporary relational constratints between elements to lock down parts of your mechanism you are not interested in.
* Switch your handle or dragged element. Often the solver uses a users's motion command filtered through the element and at the point specified by the user. By subtley changing the location or body which is being dragged, the user can find additional degrees of freedom.

## Kinematics via Sketches

Another great way to explore designs is by sketching kinematics in 2D or 3D in CAD software. This section describes how to use engineering sketches in CAD to accomplish basic motion studies.

Let's assume you would like to create a folding mechanism in two dimensions. The two dimensional assumption is easier to discuss in book form, as 2D images are easier to understand. The exention to a 3d design is trivial in concept, but in practice it is much harder to sketch due to the same issues of typically having a 2d interaction with a 3d design space. So for the purposes of simplicity we'll discuss 2d mechanisms.

## Kinematics Computation

We now enter the part of the process which can be assisted by scripting. The workflow is simple. You have been working in the physical world, and have translated your physical prototype to a sketch

The next step is to compute the kinematics of this device. There are several limitations to foldable devices which must be discussed. First, most origami-inspired devices typically start flat, as they are typically manufactured from flat sheets of material(paper, plastic, cardboard, fiberglass, carbon fiber, metal). The ability of a mechanism to be foldable from a flat sheet is defined as "flat-foldability". This makes manufacturing easier but comes with several implications.

First, when a device starts as a flat sheet, it can be considered to be in a "singular" configuration. This occurs when one or more of the mechanism's joints simultaneously align on a plane, making it impossible to move the mechanism in ways it would otherwise be able to. Singularities in the middle of a mechanism's workspace typically need to be avoided, as these conditions typically make the device uncontrollable.

![Kinematic Inversion](../../sketches/inversion.png){class="img-fluid"}

A singularity is often also accompanied by a kinematic inversion. An inversion occurs when links in a devices kinematics pass through an inversion, occupying a valid state in which many of the other links occupy the same states as in the uninverted state. With an inverted four-bar linkage, as seen above, the implications on the motion of this transmission is that the motion of the lower link no longer leads to the same motion of the upper link. The rates of change, being state-based, are quite different (the rates of change of the links are opposite each other when compared to the uninverted state). This means that the motion of the input linkage cannot be used to drive the motion of the output to and through its singularity alone. If it emerges on the other side of a singularity in an inverted state, the input link cannot move it in the same way nor can it get it out on its own through its own rotation.

As a foldable mechanism typically starts in a flat state when it emerges from the manufacturing stages, care must be taken to assemble it (often by hand) into its desired configuration, and that the resulting design must be kept appropriately away from singularities. The problem can become harder with soft mechanisms, as soft mechanisms may bend and flex in ways unintended by the rigid kinematics, which pushes the devices through a singularity.

![Inversion Due to Flexibility](../../sketches/inversion2.png){class="img-fluid"}

Singularities also make the analysis of flat-foldable mechanisms tricky, as the user must supply the intended state of the mechanism in order to
<!--TODO: Finish
The next step is to compute from the
-->
If trying to replicate a traditional robot, there are several caveats to making a paper robot which can do the same thing. First, a device constructed from hinges is limited by the travel of each hinge. At most, an ideally-thin sheet of material may only bend +/- 180 degrees. Any continuous rotations must be handled outside of your hinging mechanism. That is fine, and later sections deal with integrating other devices with your printable mechanism.

Hinge lines may be imported for kinematics study, just as body lines are imported for manufacturing file generation. For this we recommend importing just the body and hinge information in order to infer link-link connections to establish the topology, for plotting.

## Further Reading
{{< cite "Gosselin1990" >}},{{< cite "McCarthy2011" >}},{{< cite "Waldron1966" >}}

## Bibliography

{{< bibliography cited >}}
