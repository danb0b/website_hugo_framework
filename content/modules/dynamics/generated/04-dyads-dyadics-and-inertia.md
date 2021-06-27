---
title: Dyads, Dyadics, and Inertia
type: submodule
---
## Dyads

Dyads and dyadics are a difficult concept to understand, initially.  Dyads may be defined in a number of ways, but the way which makes most sense to me is that dyads are the vector-based mathematical representation for physical phenomena that contain coupled, multi-dimensional information.  An example of a physical system that contains multi-dimensional information is inertia.  Inertia describes the spatial distribution of mass throughout a rigid body, and this spatial distribution comes encoded in a structure in which mass is represented in two-vector pairs.  

Mathematically, operating on a dyad from the left or the right produces a different answer.  if ${d}=(\vec{v}_1,\vec{v}_2)$, then $\vec{v}_3\cdot d=(\vec{v}_3\cdot \vec{v}_1)\vec{v}_2$.  The ordering of vectors in a dyad is fixed, meaning that $\vec{v} \cdot d \neq d \cdot \vec{v}$.  Dyads may be multiplied by scalars, which are commutative.  Thus $3*(v1,v2) = (3v1,v2) = (v1,3v2)$ are all equivalent statements.  Thus, most often, scalar values are brought out of dyads so that only unit vectors are conatined within the dyad itself.

In *pynamics*, the dyad class represents a two-vector collection.  Dot and cross product operations are supported between vectors and dyads.  A dyad class in *pynamics* may be constructed by supplying any two basis vectors.


```python
import pynamics

from pynamics.frame import Frame
from pynamics.dyadic import Dyad
from pynamics.system import System

system = System()
pynamics.set_system(__name__,system)

A = Frame('A')
d = Dyad(A.x,3*A.y)

v = A.x+A.y+A.z
```


```python
d.dot(v)
```




    3*A.x




```python
v.dot(d)
```




    3*A.y



## Dyadics
A dyadic is a linear combination of dyads, just as a vector is a linear combination of one or more basis vectors.  In *pynamics*, dot product, cross product, and addition operations between dyadics and vectors are supported.


```python
d = Dyad(A.x,3*A.y)
e = Dyad(A.z,3*A.x)
my_dyadic = d+e
my_dyadic
```




    (A.x, 3*A.y)+(A.z, 3*A.x)




```python
type(my_dyadic)
```




    pynamics.dyadic.Dyadic




```python
v.dot(d+e)
```




    3*A.x + 3*A.y



## Inertia

Inertia is the term for the distribution of mass throughout a rigid body.  Depending on the point about which your system rotates, that distribution of mass is different.  That is why, in *pynamics* the inertia class needs quite a bit of information before you can use it.
