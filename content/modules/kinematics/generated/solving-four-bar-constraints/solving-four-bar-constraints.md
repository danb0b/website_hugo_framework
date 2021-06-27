---
title: Solving Four-Bar Constraints
type: submodule
---
# Solving Four-Bar Constraints


Turn on inline plotting


```python
%matplotlib inline
```

import required packages


```python
import pynamics
from pynamics.frame import Frame
from pynamics.variable_types import Differentiable,Constant
from pynamics.system import System
#from pynamics.body import Body
#from pynamics.dyadic import Dyadic
from pynamics.output import Output,PointsOutput
#from pynamics.particle import Particle
import pynamics.integration
import sympy
import numpy
import matplotlib.pyplot as plt
plt.ion()
from math import pi
#from pynamics.constraint import Constraint
import scipy.optimize

```

Create a pynamics system


```python
system = System()
pynamics.set_system(__name__,system)
```

Declare constants


```python
lA = Constant(2,'lA',system)
lB = Constant(1.5,'lB',system)
lC = Constant(1,'lC',system)
lD = Constant(1,'lD',system)
```

Create three differentiable state variables


```python
qA,qA_d,qA_dd = Differentiable('qA',system)
qB,qB_d,qB_dd = Differentiable('qB',system)
qC,qC_d,qC_dd = Differentiable('qC',system)
```

Create an initial guess for their starting positions.  Note that this is not necessarily accurate given the constraint that they are supposed to be connected with given, constant length.  We will use these initial values to seed the solver that will find a valid initial state


```python
initialvalues = {}
initialvalues[qA]=-90*pi/180
initialvalues[qA_d]=0*pi/180
initialvalues[qB]=90*pi/180
initialvalues[qB_d]=0*pi/180
initialvalues[qC]=90*pi/180
initialvalues[qC_d]=0*pi/180
```

Retrieve state variables in the order they are stored in the system


```python
statevariables = system.get_state_variables()
```

Create four frames


```python
N = Frame('N')
A = Frame('A')
B = Frame('B')
C = Frame('C')
```

Declare N as the Newtonian (fixed) frame


```python
system.set_newtonian(N)
```

Rotate A,B, and C about their local Z axes.


```python
A.rotate_fixed_axis_directed(N,[0,0,1],qA,system)
B.rotate_fixed_axis_directed(A,[0,0,1],qB,system)
C.rotate_fixed_axis_directed(B,[0,0,1],qC,system)
```

Define vectors that will be used to solve for kinematics.  Note: this can be done several possible ways as in the figure below:

![Four Bar Representations](../../../../sketches/four-bar-representations.png)

Define my rigid body kinematics


```python
pNA=0*N.x+0*N.y+0*N.z

pAB=pNA+lA*A.x

pBC = pAB + lB*B.x

pCtip = pBC + lC*C.x

pD = lD*N.x
```


```python
type(pNA)
```




    pynamics.vector.Vector




```python
type(A)
```




    pynamics.frame.Frame




```python
type(A.x)
```




    pynamics.vector.Vector




```python
pout = pAB + 3*B.x-2*B.y
```

Declare a list of points that will be used for plotting


```python
points = [pNA,pAB,pBC,pCtip]
```

create a list of initial values ini0 in the order of the system's state variables


```python
statevariables = system.get_state_variables()
ini0 = [initialvalues[item] for item in statevariables]
```

Define the closed loop kinematics of the four bar linkage.


```python
eq_vector = pCtip-pD
```

Dot the vector equation with N.x and N.y to create two scalar equations.  This will remove two degrees of freedom from our system.


```python
eq = []
eq.append((eq_vector).dot(N.x))
eq.append((eq_vector).dot(N.y))
eq_d=[(system.derivative(item)) for item in eq]
```

## Solve for valid initial condition determined by independent variable

identify independent and dependent variables


```python
qi = [qA]
qd = [qB,qC]
```

for dependent variables, create an initial guess

Create a copy of symbolic constants dictionary and add the initial value of qi to it


```python
constants = system.constant_values.copy()
defined = dict([(item,initialvalues[item]) for item in qi])
constants.update(defined)
```

substitute constants in equation


```python
eq = [item.subs(constants) for item in eq]
```

convert to numpy array

sum the error


```python
error = (numpy.array(eq)**2).sum()
```

Convert to a function that scipy can use.  Sympy has a "labmdify" function that evaluates an expression, but scipy needs a slightly different format.


```python
f = sympy.lambdify(qd,error)

def function(args):
    return f(*args)
```

Take the derivative of the equations to linearize with regard to the velocity variables


```python
guess = [initialvalues[item] for item in qd]
```


```python
result = scipy.optimize.minimize(function,guess)
if result.fun>1e-3:
    raise(Exception("out of tolerance"))
```


```python
ini = []
for item in system.get_state_variables():
    if item in qd:
        ini.append(result.x[qd.index(item)])
    else:
        ini.append(initialvalues[item])
```


```python
points = PointsOutput(points, constant_values=system.constant_values)
points.calc(numpy.array([ini0,ini]))
points.plot_time()
```

    2021-02-15 16:31:49,166 - pynamics.output - INFO - calculating outputs
    2021-02-15 16:31:49,167 - pynamics.output - INFO - done calculating outputs





    <AxesSubplot:>




    
![png](output_53_2.png)
    



```python
result.fun
```




    5.147432205526916e-14



## Find Internal Jacobian

Now, given a valid configuration, solve for the linearized, velocity-based constraint equation.  If 

$$eq = \textbf{A} q_i + \textbf{B} q_d = 0$$
then, solving for $q_d$, 
$$-\textbf{B}q_d = \textbf{A}q_i$$
$$q_d = -\textbf{B}^{-1}\textbf{A}q_i$$

Turn constraint equations into a vector


```python
eq_d = sympy.Matrix(eq_d)
```

Turn qi and qd into sympy vectors


```python
qi = sympy.Matrix([qA_d])
qd = sympy.Matrix([qB_d,qC_d])
```

take partial derivative of constraints with respect to independent and dependent variables:


```python
AA = eq_d.jacobian(qi)
BB = eq_d.jacobian(qd)
```

Solve for internal input/output Jacobian


```python
J = -BB.inv()*AA
J
```




    ⎡                                                       (-sin(qA)⋅sin(qB)⋅sin(
    ⎢                                                     - ──────────────────────
    ⎢                                                                             
    ⎢                                                                             
    ⎢                                                                             
    ⎢  (-lA⋅sin(qA) - lB⋅sin(qA)⋅cos(qB) - lB⋅sin(qB)⋅cos(qA) + lC⋅(sin(qA)⋅sin(qB
    ⎢- ───────────────────────────────────────────────────────────────────────────
    ⎢                                                                             
    ⎣                                                                             
    
    qC) + sin(qA)⋅cos(qB)⋅cos(qC) + sin(qB)⋅cos(qA)⋅cos(qC) + sin(qC)⋅cos(qA)⋅cos(
    ──────────────────────────────────────────────────────────────────────────────
                                                         2        2               
                                                   lB⋅sin (qA)⋅sin (qB)⋅sin(qC) + 
                                                                                  
    ) - cos(qA)⋅cos(qB))⋅sin(qC) + lC⋅(-sin(qA)⋅cos(qB) - sin(qB)⋅cos(qA))⋅cos(qC)
    ──────────────────────────────────────────────────────────────────────────────
                           2        2                        2                2   
                  lB⋅lC⋅sin (qA)⋅sin (qB)⋅sin(qC) + lB⋅lC⋅sin (qA)⋅sin(qC)⋅cos (qB
    
    qB))⋅(lA⋅cos(qA) - lB⋅sin(qA)⋅sin(qB) + lB⋅cos(qA)⋅cos(qB) + lC⋅(-sin(qA)⋅sin(
    ──────────────────────────────────────────────────────────────────────────────
          2                2             2                2                     2 
    lB⋅sin (qA)⋅sin(qC)⋅cos (qB) + lB⋅sin (qB)⋅sin(qC)⋅cos (qA) + lB⋅sin(qC)⋅cos (
                                                                                  
    )⋅(lB⋅sin(qA)⋅sin(qB) - lB⋅cos(qA)⋅cos(qB) + lC⋅sin(qA)⋅sin(qB)⋅cos(qC) + lC⋅s
    ──────────────────────────────────────────────────────────────────────────────
                 2                2                        2        2             
    ) + lB⋅lC⋅sin (qB)⋅sin(qC)⋅cos (qA) + lB⋅lC⋅sin(qC)⋅cos (qA)⋅cos (qB)         
    
    qB) + cos(qA)⋅cos(qB))⋅cos(qC) + lC⋅(-sin(qA)⋅cos(qB) - sin(qB)⋅cos(qA))⋅sin(q
    ──────────────────────────────────────────────────────────────────────────────
           2                                                                      
    qA)⋅cos (qB)                                                                  
                                                                                  
    in(qA)⋅sin(qC)⋅cos(qB) + lC⋅sin(qB)⋅sin(qC)⋅cos(qA) - lC⋅cos(qA)⋅cos(qB)⋅cos(q
    ──────────────────────────────────────────────────────────────────────────────
                                                                                  
                                                                                  
    
    C))   (-sin(qA)⋅sin(qB)⋅cos(qC) - sin(qA)⋅sin(qC)⋅cos(qB) - sin(qB)⋅sin(qC)⋅co
    ─── - ────────────────────────────────────────────────────────────────────────
                                                                                  
                                                                               lB⋅
                                                                                  
    C))   (lA⋅cos(qA) - lB⋅sin(qA)⋅sin(qB) + lB⋅cos(qA)⋅cos(qB) + lC⋅(-sin(qA)⋅sin
    ─── - ────────────────────────────────────────────────────────────────────────
                                                                                  
                                                                                  
    
    s(qA) + cos(qA)⋅cos(qB)⋅cos(qC))⋅(-lA⋅sin(qA) - lB⋅sin(qA)⋅cos(qB) - lB⋅sin(qB
    ──────────────────────────────────────────────────────────────────────────────
       2        2                     2                2             2            
    sin (qA)⋅sin (qB)⋅sin(qC) + lB⋅sin (qA)⋅sin(qC)⋅cos (qB) + lB⋅sin (qB)⋅sin(qC)
                                                                                  
    (qB) + cos(qA)⋅cos(qB))⋅cos(qC) + lC⋅(-sin(qA)⋅cos(qB) - sin(qB)⋅cos(qA))⋅sin(
    ──────────────────────────────────────────────────────────────────────────────
                               2        2                        2                
                      lB⋅lC⋅sin (qA)⋅sin (qB)⋅sin(qC) + lB⋅lC⋅sin (qA)⋅sin(qC)⋅cos
    
    )⋅cos(qA) + lC⋅(sin(qA)⋅sin(qB) - cos(qA)⋅cos(qB))⋅sin(qC) + lC⋅(-sin(qA)⋅cos(
    ──────────────────────────────────────────────────────────────────────────────
        2                     2        2                                          
    ⋅cos (qA) + lB⋅sin(qC)⋅cos (qA)⋅cos (qB)                                      
                                                                                  
    qC))⋅(-lB⋅sin(qA)⋅cos(qB) - lB⋅sin(qB)⋅cos(qA) + lC⋅sin(qA)⋅sin(qB)⋅sin(qC) - 
    ──────────────────────────────────────────────────────────────────────────────
    2                2                2                        2        2         
     (qB) + lB⋅lC⋅sin (qB)⋅sin(qC)⋅cos (qA) + lB⋅lC⋅sin(qC)⋅cos (qA)⋅cos (qB)     
    
    qB) - sin(qB)⋅cos(qA))⋅cos(qC))                                               
    ───────────────────────────────                                               
                                                                                  
                                                                                  
                                                                                  
    lC⋅sin(qA)⋅cos(qB)⋅cos(qC) - lC⋅sin(qB)⋅cos(qA)⋅cos(qC) - lC⋅sin(qC)⋅cos(qA)⋅c
    ──────────────────────────────────────────────────────────────────────────────
                                                                                  
                                                                                  
    
           ⎤
           ⎥
           ⎥
           ⎥
           ⎥
    os(qB))⎥
    ───────⎥
           ⎥
           ⎦



That expression is quite long.  We can use the simplify function provided by sympy to shorten the expression:


```python
J.simplify()
J
```




    ⎡ ⎛lA⋅sin(qB)                  ⎞  ⎤
    ⎢-⎜────────── + lA⋅cos(qB) + lB⎟  ⎥
    ⎢ ⎝ tan(qC)                    ⎠  ⎥
    ⎢──────────────────────────────── ⎥
    ⎢               lB                ⎥
    ⎢                                 ⎥
    ⎢lA⋅(lB⋅sin(qB) + lC⋅sin(qB + qC))⎥
    ⎢─────────────────────────────────⎥
    ⎣          lB⋅lC⋅sin(qC)          ⎦



Solving for the dependent variables $q_d$:


```python
qd2 = J*qi
qd2
```




    ⎡      ⎛lA⋅sin(qB)                  ⎞  ⎤
    ⎢-qA_d⋅⎜────────── + lA⋅cos(qB) + lB⎟  ⎥
    ⎢      ⎝ tan(qC)                    ⎠  ⎥
    ⎢───────────────────────────────────── ⎥
    ⎢                  lB                  ⎥
    ⎢                                      ⎥
    ⎢lA⋅qA_d⋅(lB⋅sin(qB) + lC⋅sin(qB + qC))⎥
    ⎢──────────────────────────────────────⎥
    ⎣            lB⋅lC⋅sin(qC)             ⎦



Now we can create a substitution dictionary to replace all occurrances of $\dot{q}_b$ and  $\dot{q}_c$


```python
subs = dict([(ii,jj) for ii,jj in zip(qd,qd2)])
subs
```




    ⎧            ⎛lA⋅sin(qB)                  ⎞                                   
    ⎪      -qA_d⋅⎜────────── + lA⋅cos(qB) + lB⎟                                   
    ⎨            ⎝ tan(qC)                    ⎠         lA⋅qA_d⋅(lB⋅sin(qB) + lC⋅s
    ⎪qB_d: ─────────────────────────────────────, qC_d: ──────────────────────────
    ⎩                        lB                                     lB⋅lC⋅sin(qC) 
    
                ⎫
                ⎪
    in(qB + qC))⎬
    ────────────⎪
                ⎭



Now pick an end-effector


```python
pout
```




    lA*A.x + 3*B.x - 2*B.y




```python
vout = pout.time_derivative()
```


```python
vout
```




    lA*qA_d*A.y + B.x*(2*qA_d + 2*qB_d) + B.y*(3*qA_d + 3*qB_d)




```python
vout = vout.subs(subs)
```


```python
vout
```




    lA*qA_d*A.y + B.x*(2*qA_d - 2*qA_d*(lA*sin(qB)/tan(qC) + lA*cos(qB) + lB)/lB) + B.y*(3*qA_d - 3*qA_d*(lA*sin(qB)/tan(qC) + lA*cos(qB) + lB)/lB)




```python

```


```python

```
