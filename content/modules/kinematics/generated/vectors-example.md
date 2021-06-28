---
title: Pynamics Vectors Example
types: [tutorial,] 
---


```python
import pynamics
from pynamics.system import System
from pynamics.frame import Frame

system = System()
pynamics.set_system(__name__,system)
```


```python
A = Frame('A')
B = Frame('B')
C  = Frame('C')
```


```python
v = A.x +B.y + C.z
```


```python
v
```




    A.x + B.y + C.z




```python
3*v
```




    3*A.x + 3*B.y + 3*C.z




```python
3*v - A.x
```




    2*A.x + 3*B.y + 3*C.z


import sympy
a = sympy.symbols('a')
b = sympy.symbols('b')

B.rotate_fixed_axis_directed(A,[0,0,1],a,system)
C.rotate_fixed_axis_directed(B,[0,1,0],b,system)

```python
from pynamics.variable_types import Differentiable,Constant
a, a_d, a_dd = Differentiable('a',system)
b, b_d, b_dd = Differentiable('b',system)

system.set_newtonian(A)
B.rotate_fixed_axis_directed(A,[0,0,1],a,system)
C.rotate_fixed_axis_directed(B,[0,1,0],b,system)
```


```python
v.express(A)
```




    A.x*(-sin(a) + sin(b)*cos(a) + 1) + A.y*(sin(a)*sin(b) + cos(a)) + A.z*cos(b)




```python
output_velocity = v.time_derivative(A)
output_velocity
```




    -a_d*B.x + a_d*C.y*sin(b) + b_d*C.x




```python
output_velocity.express(A)
```




    -b_d*A.z*sin(b) + A.x*(-a_d*sin(a)*sin(b) - a_d*cos(a) + b_d*cos(a)*cos(b)) + A.y*(-a_d*sin(a) + a_d*sin(b)*cos(a) + b_d*sin(a)*cos(b))




```python
vx = output_velocity.dot(A.x)
vx
```




    -a_d⋅sin(a)⋅sin(b) - a_d⋅cos(a) + b_d⋅cos(a)⋅cos(b)




```python
vy = output_velocity.dot(A.y)
vy
```




    -a_d⋅sin(a) + a_d⋅sin(b)⋅cos(a) + b_d⋅sin(a)⋅cos(b)




```python
vz = output_velocity.dot(A.z)
vz
```




    -b_d⋅sin(b)




```python
import sympy
cartesian_velocities = sympy.Matrix([vx,vy,vz])
```


```python
J = cartesian_velocities.diff(sympy.Matrix([a_d,b_d]))
J
```




    ⎡⎡-sin(a)⋅sin(b) - cos(a)⎤⎤
    ⎢⎢                       ⎥⎥
    ⎢⎢-sin(a) + sin(b)⋅cos(a)⎥⎥
    ⎢⎢                       ⎥⎥
    ⎢⎣           0           ⎦⎥
    ⎢                         ⎥
    ⎢     ⎡cos(a)⋅cos(b)⎤     ⎥
    ⎢     ⎢             ⎥     ⎥
    ⎢     ⎢sin(a)⋅cos(b)⎥     ⎥
    ⎢     ⎢             ⎥     ⎥
    ⎣     ⎣   -sin(b)   ⎦     ⎦


