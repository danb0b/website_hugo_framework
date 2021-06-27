---
title: Unit Scaling
type: submodule
---

# Unit Scaling


```python
import idealab_tools.units
```


```python
idealab_tools.units.force
```




     kg*m/s^2




```python
idealab_tools.units.force.base_units
```




    {'kg': 1, 'm': 1, 's': -2}




```python
idealab_tools.units.force.compute_scaling()
```




    1




```python
idealab_tools.units.Unit.set_scaling(m=10)
idealab_tools.units.Unit.set_scaling(kg=.1)
```


```python
idealab_tools.units.force.compute_scaling()
```




    1.0




```python
idealab_tools.units.length.compute_scaling()
```




    10




```python
idealab_tools.units.energy.compute_scaling()
```




    10.0




```python

```
