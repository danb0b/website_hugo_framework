---
title: Sympy Example
type: tutorial
---


```python
import sympy
```


```python
a = sympy.Symbol('a')
b = sympy.Symbol('b')
x = sympy.Symbol('x')
y = sympy.Symbol('y')
```


```python
a
```




$\displaystyle a$




```python
f = a*x+b*y
f
```




$\displaystyle a x + b y$




```python
f = a*(x+y)
f
```




$\displaystyle a \left(x + y\right)$




```python
g = f.expand()
g
```




$\displaystyle a x + a y$




```python
g.diff(x)
```




$\displaystyle a$




```python
g.simplify()
```




$\displaystyle a \left(x + y\right)$



factor, collect are two other useful functions


```python
g.subs({x:b})
```




$\displaystyle a b + a y$




```python
h = g.subs({x:(3*b+5)})
h
```




$\displaystyle a y + a \left(3 b + 5\right)$




```python
eq = []
eq.append(x+5*y)
eq.append(x-1)
```


```python
solution = sympy.solve(eq,[x,y])
solution
```




    {x: 1, y: -1/5}




```python
i = x+5*y
j = i.subs(solution)
j
```




$\displaystyle 0$




```python
type(j)
```




    sympy.core.numbers.Zero




```python
type(j.evalf(5))
```




    sympy.core.numbers.Zero




```python

```
