---
title: Solve Triangle
types: [tutorial,] 
---


```python
%matplotlib inline
import matplotlib.pyplot as plt
import scipy.optimize
import numpy
```


```python
desired_length1=1 
desired_length2=2
desired_length3=1.5
p1_desired_location = 0,0
```


```python
def objective_function(variables):

    x1,y1,x2,y2,x3,y3 = variables
    p1 = numpy.array([x1,y1])
    p2 = numpy.array([x2,y2])
    p3 = numpy.array([x3,y3])
    v0 = p1-p1_desired_location
    v1 = p2-p1
    v2 = p3-p2
    v3 = p1-p3
    l0 = (v0.dot(v0))**.5
    l1 = (v1.dot(v1))**.5
    l2 = (v2.dot(v2))**.5
    l3 = (v3.dot(v3))**.5
    
    
    error = []
    error.append(l0)
    error.append(y2-0)
    error.append(l1-desired_length1)
    error.append(l2-desired_length2)
    error.append(l3-desired_length3)
    
    error = numpy.array(error)
    error = (error.dot(error))**.5
    return error    
```


```python
ini = [2,2,2,4,1,1]
ini = [1,2,2,6,2,-1]
result = scipy.optimize.minimize(objective_function,ini)
```


```python
print(result)
```

          fun: 2.3085907343075597e-08
     hess_inv: array([[ 9.48608434e-08,  1.72611133e-08,  8.77011379e-08,
             3.08116961e-09, -3.96175385e-08,  9.12975778e-08],
           [ 1.72611133e-08,  6.50516951e-08,  6.55326138e-09,
             1.61176317e-08, -4.73814986e-08,  5.52006207e-08],
           [ 8.77011379e-08,  6.55326138e-09,  1.17185562e-07,
             4.44984152e-09,  2.79299122e-08,  5.93862621e-08],
           [ 3.08116961e-09,  1.61176317e-08,  4.44984152e-09,
             3.09500982e-08,  2.04322549e-09,  2.71948650e-08],
           [-3.96175385e-08, -4.73814986e-08,  2.79299122e-08,
             2.04322549e-09,  4.61645501e-07, -2.54312467e-07],
           [ 9.12975778e-08,  5.52006207e-08,  5.93862621e-08,
             2.71948650e-08, -2.54312467e-07,  2.46184915e-07]])
          jac: array([ 0.36641926,  0.89598149,  0.66629281, -0.30097396,  0.04419924,
            0.22413009])
      message: 'Desired error not necessarily achieved due to precision loss.'
         nfev: 929
          nit: 59
         njev: 131
       status: 2
      success: False
            x: array([-1.14216757e-09,  9.14061190e-09,  1.00000000e+00, -1.99287241e-08,
           -3.75000037e-01, -1.45236874e+00])
    


```python
p = result.x.reshape((3,2))
plot_lines = numpy.concatenate((p,p[0:1]),0)
plt.plot(*(plot_lines.T))
plt.axis('equal')
for ii,item in enumerate(p):
    plt.text(item[0],item[1],'p'+str(ii))

```


    
![png](output_6_0.png)
    



```python
p
```




    array([[-1.14216757e-09,  9.14061190e-09],
           [ 1.00000000e+00, -1.99287241e-08],
           [-3.75000037e-01, -1.45236874e+00]])




```python

```
