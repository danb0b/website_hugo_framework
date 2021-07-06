---
title: Forces and Torques
type: submodule
---

# Forces and Torques

## Introduction

## Non-Conservative Forces

### Damping

$$\vec{f} = -b\vec{v}$$

### Friction

Friction is typically formulated as the forces acting between two bodies $A$ and $B$

$$\vec{f} = \mu|\vec{n}|\frac{\vec{v}}{|\vec{v}|}$$ 

where $\mu$ is the coefficient of friction, determined experimentally, $\vec{n}$ is the magnitude of the normal force between two rigid bodies, and $\vec{v}$ is the relative velocity of the contact point on $B$ with respect to the contact point on $A$. If $|\vec{v}|==0$, you must be careful to ensure that the expression does not evaluate as ```NaN```.


### Torsional Friction

Because the normal force not easily derived from a rigid body analysis, we often apply a 

$$\vec{f} = -f\frac{\vec{v}}{|\vec{v}|}$$ 

where f is a constant value determined experimentally and where $\vec{v}$ is a unit vector describing the rotational velocity.  If $|\vec{v}|==0$, you must be careful to ensure that the expression does not evaluate as ```NaN```.


### Applying Forces in Pynamics

Forces and torques are added to the system with the generic ```addforce``` method.  The first parameter supplied is a vector describing the force applied at a point or the torque applied along a given rotational axis.  The second parameter is the  vector describing the linear speed (for an applied force) or the angular velocity(for an applied torque)

## Conservative Forces

### Springs

Traditional Hookian springs obey the rule

$$\vec{f}=-k\vec{x}$$

where $k$ is a constant value obtained experimentally and $\vec{x}$ indicates the stretch of the spring from its neutral point.

#### Springs in Pynamics

Spring forces are a special case because the energy stored in springs is conservative and should be considered when calculating the system's potential energy.  To do this, use the ```add_spring_force``` command.  In this method, the first value is the linear spring constant.  The second value is the "stretch" vector, indicating the amount of deflection from the neutral point of the spring.  The final parameter is, as above, the linear or angluar velocity vector (depending on whether your spring is a linear or torsional spring)

In this case, the torques applied to each joint are dependent upon whether qA, qB, and qC are absolute or relative rotations, as defined above.

### Gravity

$$\vec{f} = m\vec{g}$$

#### Gravity in Pynamics
Again, like springs, the force of gravity is conservative and should be applied to all bodies.  To globally apply the force of gravity to all particles and bodies, you can use the special ```addforcegravity``` method, by supplying the acceleration due to gravity as a vector.  This will get applied to all bodies defined in your system.
