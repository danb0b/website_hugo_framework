---
title: Lecture 22 Code
types: [tutorial,] 
---


```python
import shapely.geometry as sg
from foldable_robotics.layer import Layer
from foldable_robotics.laminate import Laminate
```


```python
a = sg.Point(0,0)
a
```




    
![svg](output_2_0.svg)
    




```python
b = sg.box(0,0,1,1)
b
```




    
![svg](output_3_0.svg)
    




```python
c = Layer(b)
c
```




    
![svg](output_4_0.svg)
    




```python
c.translate(.5,.5)
```




    
![svg](output_5_0.svg)
    




```python
c|(c.translate(.5,.5))
```




    
![svg](output_6_0.svg)
    




```python
c.union((c.translate(.5,.5)))
```




    
![svg](output_7_0.svg)
    




```python
d = Layer(a.buffer(.25))
d
```




    
![svg](output_8_0.svg)
    




```python
e = c-d.translate(.5,.5)
e
```




    
![svg](output_9_0.svg)
    




```python
import foldable_robotics
foldable_robotics.resolution=4
e.dilate(.2)
```




    
![svg](output_10_0.svg)
    




```python
e.erode(.1)
```




    
![svg](output_11_0.svg)
    




```python
e.plot()
```


    
![png](output_12_0.png)
    



```python
e.erode(.1).plot()
```


    
![png](output_13_0.png)
    



```python
list(b.centroid.coords)
```




    [(0.5, 0.5)]




```python
d.bounding_box().plot()
d.plot()
```


    
![png](output_15_0.png)
    



```python
e<<(.1)
```




    
![svg](output_16_0.svg)
    




```python
e>>.1
```




    
![svg](output_17_0.svg)
    




```python
f = Laminate(e<<.1,e, e>>.1)
f
```




    
![svg](output_18_0.svg)
    




```python
g = [1,2,3]
g
```




    [1, 2, 3]




```python
g[::-1]
```




    [3, 2, 1]




```python
f[0]
```




    
![svg](output_21_0.svg)
    




```python
f[1]
```




    
![svg](output_22_0.svg)
    




```python
f[2]
```




    
![svg](output_23_0.svg)
    




```python
f[::-1]
```




    
![svg](output_24_0.svg)
    




```python
len(f+f)
```




    6




```python
[1,2,3]+[4,5,6]
```




    [1, 2, 3, 4, 5, 6]




```python
f<<.1
```




    
![svg](output_27_0.svg)
    




```python
g = f.rotate(30)
g
```




    
![svg](output_28_0.svg)
    




```python
h = g.translate(.5,.5)
h
```




    
![svg](output_29_0.svg)
    




```python
f|h
```




    
![svg](output_30_0.svg)
    




```python
f&h
```




    
![svg](output_31_0.svg)
    




```python
f.symmetric_difference(h)
```




    
![svg](output_32_0.svg)
    




```python
import foldable_robotics.manufacturing as fm
k  = fm.unary_union(f)
k
```




    
![svg](output_33_0.svg)
    




```python
l = (k<<.2).bounding_box()
m = Laminate(l,l,l)
m
```




    
![svg](output_34_0.svg)
    




```python
n = m-f
n
```




    
![svg](output_35_0.svg)
    




```python
# this can kill jupyter so do it last in your script or comment it out
f.plot_3d()
```


    An exception has occurred, use %tb to see the full traceback.


    SystemExit: 0



    /home/danaukes/anaconda3/lib/python3.7/site-packages/IPython/core/interactiveshell.py:3435: UserWarning: To exit: use 'exit', 'quit', or Ctrl-D.
      warn("To exit: use 'exit', 'quit', or Ctrl-D.", stacklevel=1)

