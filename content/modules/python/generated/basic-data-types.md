---
title: Basic Data Types
type: submodule
---

# Basic Data Types


```python
type(4.1)
```




    float




```python
type(int(4.1))
```




    int



## Bool


```python
True
```




    True




```python
False
```




    False




```python
1==2
```




    False




```python
3!=5
```




    True



## Integer


```python
1
```




    1




```python
1+2
```




    3




```python
2-1
```




    1




```python
a = 1
b = 2
```


```python
a+b
```




    3



## Float Operations


```python
import math
```


```python
1.1 
```




    1.1




```python
1.1*2.2 
```




    2.4200000000000004




```python
2*1.1 
```




    2.2




```python
round(1.4)
```




    1




```python
round(1.5)
```




    2




```python
round(-1.4)
```




    -1




```python
round(-1.5)
```




    -2




```python
math.trunc(1.8)
```




    1




```python
math.floor(1.8)
```




    1




```python
math.trunc(-1.8)
```




    -1




```python
math.floor(-1.8)
```




    -2




```python
math.ceil(1.8)
```




    2




```python
math.ceil(-1.8)
```




    -1



## Conversions


```python
int(8.1)
```




    8




```python
float(8)
```




    8.0




```python
int(8)
```




    8




```python
str(9.815)
```




    '9.815'




```python
bool(8.15)
```




    True




```python
float(str(8.15))
```




    8.15




```python
int(str(8))
```




    8




```python
int(str(8.15))
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-33-87f9af5e8496> in <module>
    ----> 1 int(str(8.15))
    

    ValueError: invalid literal for int() with base 10: '8.15'

