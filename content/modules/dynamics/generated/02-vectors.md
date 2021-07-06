---
title: Frames, Basis Vectors, and Vectors
type: submodule
---

## Frames

When analyzing a system, sometimes it's convenient or simple to represent a system in a specific way.  We all know of the Cartesian system of coordinates which span a three dimensional space, but did you know that there are an infinte number of ways to describe that same space?  Just as we are familiar with the x,y, and z directions, we can use different reference frames to navigate and represent the same coordinates and vectors in different ways.

Take the example of your professor standing in front of you, giving a lecture.  If both of you were to stretch your right hand out to your right, you wouldn't be pointing in the same direction.  To get to the door behind youyour professor would say go forward.  Direction is relative to each of you based on your frame of reference.

Sometimes the ability to select your directional representation is useful in dynamics, because depending on the representation, it may take many more or far fewer variables to do so.  For example, when discussing the motion of a plane or car, it is often useful to describe the forces acting on the plane from the car's perspective, even if you're more interested in where the plane goes relative to your perspective standing on the ground.  The planes perspective and the grounds perspective, in terms of their directional components, can be considered separate reference frames.

## Basis Vectors
The purpose of a reference frame is to hold a set of unique *basis vectors* which in linear algebra terms span an $R^3$ space.  As long as these basis vectors span the space, they are capable of describing any vector within that space, a minimum requirement for a 3 dimensional reference frame.  However, there are some other useful qualities of these basis vectors which typically make life easier, which are also enforced in *pynamics*.

**Orthogonal:**  The basis vectors in an orthogonal reference frame are themselves orthogonal, or mutually perpendicular to each other.  This means that there are no shared components of vectors; each basis vector is completely independent of each other.  a more mathy way to describe this is that $\vec{b}_1 \cdot \vec{b}_2 =0$, where $\vec{b}_1$ and $\vec{b}_2$ are any two basis vectors in a reference frame.

**Normal:** Basis vectors in a pynamics reference frame are *normal*, meaning their lengths have been normalized.  They are *unit vectors*.

In Pynamics, frames are implemented as a Python class, and serve to hold three *orthonormal* (orthogonal and normal) vectors.  Frames can be named when created, and no two names can be the same; this name is applied to the x,y, and z basis vectors in each frame.  Thus, no two basis vectors may be named the same in *pynamics*.

## Vectors

Vectors in *pynamics* are represented as linear combinations of basis vectors from one or more frames.  Once frames are created, the basis vectors they contain may be combined with other literal or symbolic variables to create symbolic vector expressions.

Vectors are represented as a Python class, and leverage the ability to overload Python's mathematical operators with other functionality.  In this way, common operators such as $+$,$-$,$*$ and $/$ take on their own meaning when used in expressions with scalars, vectors, dyads, or dyadics.  In this way

Vectors cannot be created without a reference frame.  Therefore, each frame supplies three orthogonal unit basis vectors which contain all the frame's information and which can be used to construct a vector.  

## Math
Vectors have a number of general properties that are all made possible in pynamics.  Below is a list of valid operations and their result.

| Operation | Operator | Other  | Vector Order | Result                           | Commutative |
|:----------|:---------|:-------|:-------------|:---------------------------------|:------------|
| Addition  | +        | vector | before       | $\vec{v}+\vec{v}_{other}$        | y           |
| Addition  | +        | vector | after        | $s\vec{v}$                       | y           |
| Addition  | *        | vector | before       | $s\vec{v}$                       | y           |
| Addition  | *        | vector | after        | $s\vec{v}$                       | y           |
| dot       | .dot()   | vector | before       | $\vec{v}_{other} \cdot \vec{v}$  | y           |
| dot       | .dot()   | vector | after        | $\vec{v} \cdot \vec{v}_{other}$  | y           |
| cross     | .cross() | vector | before       | $\vec{v}_{other} \times \vec{v}$ | n           |
| cross     | .cross() | vector | after        | $\vec{v} \times \vec{v}_{other}$ | n           |

Note: at this time, division with scalars, ie
```{.python}
v/s
```
is not possible.  Instead, simply invert the scalar and then multiply, as with 
```{.python}
(1/s)*v
```


```python
import pynamics
from pynamics.system import System
from pynamics.frame import Frame

system = System()
pynamics.set_system(__name__,system)

A = Frame('A');
B = Frame('B');
C = Frame('C');
```

Vector addition works out of the box because vectors don't necessarily need to be represented using each others' basis vectors


```python
v = A.x + B.y + C.z;
v
```




    A.x + B.y + C.z



Additionally, multiplication with a scalar works well:


```python
s = 3
print(s*v)
print(v*s)
```

    3*A.x + 3*B.y + 3*C.z
    3*A.x + 3*B.y + 3*C.z
    

Furthermore, dot and cross product works well for vectors expressed by the same basis vectors:


```python
v1 = 1*A.x+2*A.y
v2 = 3*A.z+4*A.x
print(v1.dot(v2))
print(v1.cross(v2))
```

    4
    6*A.x - 3*A.y - 8*A.z
    

However, out of the box, performing a dot or cross product with vectors composed of different basis vectors will not work, because a relationship needs to be established between them.  For example, the following code will produce a custom error saying, "Frames don't share a common parent"

```python
v1 = A.x+B.y
v2 = B.z+C.x
print("v1.dot(v2)=",v1.dot(v2))
print("v1.cross(v2)=",v1.cross(v2))
```

This can be addressed by defining a relationship between frames through rotations.


```python
import sympy
a = sympy.symbols('a')
b = sympy.symbols('b')

B.rotate_fixed_axis_directed(A,[0,0,1],a,system)
C.rotate_fixed_axis_directed(B,[0,1,0],b,system)
```

Now the following code should work


```python
v1 = A.x+B.y
v2 = B.z+C.x
print("v1.dot(v2)=",v1.dot(v2))
print("v1.cross(v2)=",v1.cross(v2))
```

    v1.dot(v2)= cos(a)*cos(b)
    v1.cross(v2)= -A.y + B.x*(sin(a)*sin(b) - sin(b) + 1) + B.y*sin(b)*cos(a) + B.z*(sin(a)*cos(b) - cos(b))
    

## Other Functions
### Express

If enough information is supplied, vectors can also be expressed in other reference frames.  This uses the rotation information stored when the frame rotations are defined to transform all basis vectors stored within a vector type into a desired type.  This can be useful for finding the shortest representation of a vector, or the resulting math.  For example,


```python
print(v1.express(B))
print(v1.express(A))
```

    B.x*cos(a) + B.y*(1 - sin(a))
    A.x*(1 - sin(a)) + A.y*cos(a)
    

produces quite similar size representations, but complex expressions may benefit from shorter representations.  Take this example where v is the cross product of vectors expressed in frames separated by two separate rotations.


```python
v = (A.x+A.y+A.z).cross(C.x+C.y+C.z)
v
```




    B.x*((-sin(a) + cos(a))*(-sin(b) + cos(b)) - 1) + B.y*(-(sin(a) + cos(a))*(-sin(b) + cos(b)) + sin(b) + cos(b)) + B.z*(-(-sin(a) + cos(a))*(sin(b) + cos(b)) + sin(a) + cos(a))



When you express v in A, B, and C basis vectors, you will see that the middle frame is by far the shortest representation


```python
v.express(A)
```




    A.x*(((-sin(a) + cos(a))*(-sin(b) + cos(b)) - 1)*cos(a) - (-(sin(a) + cos(a))*(-sin(b) + cos(b)) + sin(b) + cos(b))*sin(a)) + A.y*(((-sin(a) + cos(a))*(-sin(b) + cos(b)) - 1)*sin(a) + (-(sin(a) + cos(a))*(-sin(b) + cos(b)) + sin(b) + cos(b))*cos(a)) + A.z*(-(-sin(a) + cos(a))*(sin(b) + cos(b)) + sin(a) + cos(a))




```python
v.express(B)
```




    B.x*((-sin(a) + cos(a))*(-sin(b) + cos(b)) - 1) + B.y*(-(sin(a) + cos(a))*(-sin(b) + cos(b)) + sin(b) + cos(b)) + B.z*(-(-sin(a) + cos(a))*(sin(b) + cos(b)) + sin(a) + cos(a))




```python
v.express(C)
```




    C.x*(((-sin(a) + cos(a))*(-sin(b) + cos(b)) - 1)*cos(b) - (-(-sin(a) + cos(a))*(sin(b) + cos(b)) + sin(a) + cos(a))*sin(b)) + C.y*(-(sin(a) + cos(a))*(-sin(b) + cos(b)) + sin(b) + cos(b)) + C.z*(((-sin(a) + cos(a))*(-sin(b) + cos(b)) - 1)*sin(b) + (-(-sin(a) + cos(a))*(sin(b) + cos(b)) + sin(a) + cos(a))*cos(b))




```python
del v,v1,v2,A,B,C,a,b,system
```

This can have a real-world impact on the time to compute and integrate pynamics expressions

### Derivatives
Vectors can also have their time derivatives taken.  For this to be possible, the variables that define the magnitude and direction of vectors need to be explicitly defined if they are time-differentiable.  For more information on time-differentiable variables, see the variable-types module.


```python
import pynamics

from pynamics.frame import Frame
from pynamics.variable_types import Differentiable,Constant,Variable
from pynamics.system import System

system = System()
pynamics.set_system(__name__,system)

N = Frame('N');
A = Frame('A');

qA,qA_d,qA_dd = Differentiable('qA',system)
x,x_d,x_dd = Differentiable('x',system)

system.set_newtonian(N)
A.rotate_fixed_axis_directed(N,[0,0,1],qA,system)

pos = x*A.x
vel=pos.time_derivative(N)
acc=vel.time_derivative(N)

print('pos = ',pos)
print('vel = ',vel)
print('acc = ',acc)
```

    pos =  x*A.x
    vel =  qA_d*x*A.y + x_d*A.x
    acc =  A.x*(-qA_d**2*x + x_dd) + A.y*(2*qA_d*x_d + qA_dd*x)
    

You can combine derivatives with the express function to print the derivative in other frames

```python
vel.express(N)
acc.express(N)
```

## Use Cases

Vectors are typically used in a number of cases

* describing the kinematics of a structure
* defining the magnitude and direction of a force, or the axis of rotation for a torque.
* vectors may 
