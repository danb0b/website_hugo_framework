---
title: Advanced Data Types
types: [submodule,] 
---

# Advanced Data Types

## Tuples


```python
tup1 = (0,1)
tup1
```




    (0, 1)




```python
tup2 = (3,-2)
tup2
```




    (3, -2)




```python
tup3 = tuple(range(5))
tup3
```




    (0, 1, 2, 3, 4)



tuple of tuples


```python
tup4 = (tup2,tup1)
tup4
```




    ((3, -2), (0, 1))



you can use the sorted method to create a sorted list of tuples


```python
sorted(tup4)
```




    [(0, 1), (3, -2)]



you can also pick how you sort based on a lambda method


```python
sorted(tup4,key=lambda x:x[1])
```




    [(3, -2), (0, 1)]



accessing tuples


```python
tup4[0]
```




    (3, -2)




```python
tup4[0][1]
```




    -2



## Lists
Construct a list


```python
list1 = [-1,1,2,3,4]
list1
```




    [-1, 1, 2, 3, 4]



Methods: use tab to autocomplete


```python
list1.append(5)
list1
```




    [-1, 1, 2, 3, 4, 5]




```python
list1.extend([6,7,8,9,0b101101,11.0])
list1
```




    [-1, 1, 2, 3, 4, 5, 6, 7, 8, 9, 45, 11.0]




```python
result = list1.pop(0)
list1
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9, 45, 11.0]




```python
list1.insert(0,14)
list1
```




    [14, 1, 2, 3, 4, 5, 6, 7, 8, 9, 45, 11.0]




```python
ii = list1.count(1)
ii
```




    1




```python
ii=list1.index(7)
ii
```




    7




```python
list1.remove(7)
list1
```




    [14, 1, 2, 3, 4, 5, 6, 8, 9, 45, 11.0]




```python
sorted(list1)
```




    [1, 2, 3, 4, 5, 6, 8, 9, 11.0, 14, 45]




```python
list1
```




    [14, 1, 2, 3, 4, 5, 6, 8, 9, 45, 11.0]




```python
list1.sort()
list1
```




    [1, 2, 3, 4, 5, 6, 8, 9, 11.0, 14, 45]




```python
#list1.clear()
```

Accessing the list


```python
list1
```




    [1, 2, 3, 4, 5, 6, 8, 9, 11.0, 14, 45]




```python
list1[0]
```




    1




```python
list1[2:4]
```




    [3, 4]




```python
list1[:4]
```




    [1, 2, 3, 4]




```python
list1[4:]
```




    [5, 6, 8, 9, 11.0, 14, 45]




```python
list1[::2]
```




    [1, 3, 5, 8, 11.0, 45]




```python
list1[-1::-1]
```




    [45, 14, 11.0, 9, 8, 6, 5, 4, 3, 2, 1]




```python
#list1.clear()
```

understanding types


```python
print(isinstance(list1,list))
```

    True
    


```python
list1
```




    [1, 2, 3, 4, 5, 6, 8, 9, 11.0, 14, 45]



# Dicts


```python
dict1 = {}
```


```python
dict1['key1']=123.45
```


```python
dict1['coordinate 1'] = tup1
```


```python
dict1['coordinate 2'] = tup2
```


```python
dict1['all_coordinates'] = list1
```


```python
dict1
```




    {'key1': 123.45,
     'coordinate 1': (0, 1),
     'coordinate 2': (3, -2),
     'all_coordinates': [1, 2, 3, 4, 5, 6, 8, 9, 11.0, 14, 45]}




```python
dict1['coordinate 1']
```




    (0, 1)



methods


```python
dict1.items()
```




    dict_items([('key1', 123.45), ('coordinate 1', (0, 1)), ('coordinate 2', (3, -2)), ('all_coordinates', [1, 2, 3, 4, 5, 6, 8, 9, 11.0, 14, 45])])




```python
dict1.keys()
```




    dict_keys(['key1', 'coordinate 1', 'coordinate 2', 'all_coordinates'])




```python
dict1.values()
```




    dict_values([123.45, (0, 1), (3, -2), [1, 2, 3, 4, 5, 6, 8, 9, 11.0, 14, 45]])



## Sets


```python
a = set([1,2,3])
a
```




    {1, 2, 3}




```python
b=set([2,3,4,3,2,2,3,2,4,2,3,4])
b
```




    {2, 3, 4}




```python
a&b
```




    {2, 3}




```python
a|b
```




    {1, 2, 3, 4}



## Strings & Formatting


```python
float1 = 12.345
```


```python
'the value of the first element is {0:07.1f}, as an int: {1:07d}'.format(float1,int(float1))
```




    'the value of the first element is 00012.3, as an int: 0000012'




```python

```
