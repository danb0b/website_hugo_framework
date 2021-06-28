---
title: Rotations
types: [submodule,] 
---

## Introduction

While there may be many ways to navigate and describe the same three-dimensional space using reference frames, it is also necessary and desireable to be able to change representations; this can be useful for interpreting motion from a differet perspective, for adding forces or torques to a system using dirctional components which are a more natural description, or in order to perform mathematical operations between vectors which are represented by different basis vectors.  The method by which we represent one frame to another is through the concept of rotations.  

Rotations may be described in a number of ways, including axis,angle representations, quaternions, Euler parameters, Euler vectors, Rodrigues' parameters, etc.  Each representation has its benefits and drawbacks, but at the end of the day, each of these methods is simply a way to find the rotational relationships between reference frames and the basis vectors they contain.  A rotation is a specific type of vector transformation that **1)** Preserve length and **2)**, preserve angles between vectors.  Generically, we may think of rotational transformations as permitting the same vector to be represented using a new set of basis vectors, or, in another way of thinking, to actually rotate a body into a new orientation with relation to some other frame.  The first one is a change of representation, while the second indicates actual motion.

In *pynamics*, the rotation class can be created in a variety of ways.  You may supply a 3x3 matrix directly, generate one using an axis, angle pair, or create one by defining a rotation along an x,y,or z axis.  Rotations in *pynamics* are stored as $3x3$ matrices.  Rotations do not have to be fixed, as the matrices which encode their information can hold variables.  Thus, axis,angle pairs themselves may be composed of one or more variables.

Rotation classes *in pynamics* must be defined as the relationship between two existing frames.  Thus, rotations between frames must be created after the frames themselves.  Only one rotation may be stored between two reference frames.  (though there are ways to represent more than one).  Progrmmaticaly, this is because pynamics uses the rotational connections defined by the user in determining the shortest and simplest possible representation for vectors when performing vector operations, and having multiple pathways would undesireably increase computational cost and complexity.


## Theory

::: {style="text-align:center;"}
![rotation between frames](../../../figures/dynamics/rotation_matrix.png){height=3in}
:::

$$
\begin{array}{c|c c c}
  {}^N{\textbf{R}}^{A} & \hat{a}_x &\hat{a}_y & \hat{a}_z\\
  \hline
  \hat{n}_x &\cos q&-\sin q &0 \\
  \hat{n}_y &\sin q& \cos q &0 \\
  \hat{n}_z &0&0&1
 \end{array}
$$

Multiple rotations:

$$
{}^N{\textbf{R}}^{B} = {}^{N}{\textbf{R}}^{A} {}^N{\textbf{R}}^{B}
$$

## Example


```python
import pynamics
from pynamics.system import System
from pynamics.frame import Frame
import sympy

system = System()
pynamics.set_system(__name__,system)

a = sympy.symbols('a')

N = Frame('N')
A = Frame('A')

#system.set_newtonian(N)
A.rotate_fixed_axis_directed(N,[0,0,1],a,system)

A.getR(N)
```




    ⎡cos(a)  -sin(a)  0⎤
    ⎢                  ⎥
    ⎢sin(a)  cos(a)   0⎥
    ⎢                  ⎥
    ⎣  0        0     1⎦




```python
del system,N,A,a
```

## Usage

Rotations are used throughout pynamics but they are not utilized directly very often, other than for debugging purposes.  Use cases include

* Generating basis vectors for use in general-purpose vector creation
* They can be used with constants to generate fixed changes of reference
* They are used in conjunction with differentiable state variables to determine rotational velocity and acceleration between frames

Rotations in pynamics are typically generated in a sequential order from a base, or Newtonian frame (a non-accelerating world frame).  The ordering is not required, because internally pynamics establishes connections to neighboring rotations by creating a tree-like map of all frames connected to each other.  This can be done with or without explicitly defining the Newtonian frame first (though other functions dealing with differentiation require this declaration first)


```python
import pynamics
from pynamics.system import System
from pynamics.frame import Frame
import sympy

system = System()
pynamics.set_system(__name__,system)

a,b,c = sympy.symbols('a,b,c')

N = Frame('N')
A = Frame('A')
B = Frame('B')
C = Frame('C')

#system.set_newtonian(N)
A.rotate_fixed_axis_directed(N,[0,0,1],a,system)
B.rotate_fixed_axis_directed(A,[0,1,0],b,system)
C.rotate_fixed_axis_directed(N,[1,0,0],c,system)
```


```python
A.getR(N)
```




    ⎡cos(a)  -sin(a)  0⎤
    ⎢                  ⎥
    ⎢sin(a)  cos(a)   0⎥
    ⎢                  ⎥
    ⎣  0        0     1⎦




```python
B.getR(N)
```




    ⎡cos(a)⋅cos(b)  -sin(a)  sin(b)⋅cos(a)⎤
    ⎢                                     ⎥
    ⎢sin(a)⋅cos(b)  cos(a)   sin(a)⋅sin(b)⎥
    ⎢                                     ⎥
    ⎣   -sin(b)        0        cos(b)    ⎦




```python
C.getR(N)
```




    ⎡1    0        0   ⎤
    ⎢                  ⎥
    ⎢0  cos(c)  -sin(c)⎥
    ⎢                  ⎥
    ⎣0  sin(c)  cos(c) ⎦




```python
C.getR(B)
```




    ⎡cos(a)⋅cos(b)  sin(a)⋅cos(b)⋅cos(c) - sin(b)⋅sin(c)  -sin(a)⋅sin(c)⋅cos(b) - 
    ⎢                                                                             
    ⎢   -sin(a)                cos(a)⋅cos(c)                         -sin(c)⋅cos(a
    ⎢                                                                             
    ⎣sin(b)⋅cos(a)  sin(a)⋅sin(b)⋅cos(c) + sin(c)⋅cos(b)  -sin(a)⋅sin(b)⋅sin(c) + 
    
    sin(b)⋅cos(c)⎤
                 ⎥
    )            ⎥
                 ⎥
    cos(b)⋅cos(c)⎦




```python
del a,b,c,N,A,B,C
```
