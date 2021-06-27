---
title: Plotting in 3D
type: submodule
---


```python

%matplotlib inline
```

# Plotting in 3D
* Visit this [matplotlib tutorial](http://matplotlib.org/mpl_toolkits/mplot3d/tutorial.html) on 3d Plotting
* Another useful [reference](https://jakevdp.github.io/PythonDataScienceHandbook/04.12-three-dimensional-plotting.html)



```python
import matplotlib.pyplot as plt
import numpy
from math import pi
from mpl_toolkits.mplot3d import Axes3D
import idealab_tools.matplotlib_tools
```


```python
theta = numpy.r_[0:2*pi:40j]

x = numpy.cos(theta)
y = .5*numpy.sin(theta)
z = numpy.sin(2*theta-pi/4)

xyz = numpy.array([x,y,z]).T
```


```python
fig = plt.figure();
ax = fig.add_subplot(111, projection='3d');
ax.view_init(30, 15)
ax.plot3D(xyz[:,0],xyz[:,1],xyz[:,2])
idealab_tools.matplotlib_tools.equal_axes(ax,xyz)
```


    
![png](output_5_0.png)
    



```python

```
