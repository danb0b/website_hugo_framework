---
subtitle: Individual Assignment
class_name: EGR557
copyright: Daniel M. Aukes
//overlay_text: DRAFT
bibliography: ../../misc/bibliography.bib
csl: ../../misc/ieee.csl
title: Python Functions
module: python
week: "03"
points: 100
type: assignment
module: python
layout: page
---

#  Python Functions

## Resources

* [*args and **kwargs in python explained](https://pythontips.com/2013/08/04/args-and-kwargs-in-python-explained/)
* [NumPy for Matlab users](https://docs.scipy.org/doc/numpy/user/numpy-for-matlab-users.html)

## Procedure

<!--hide-->

1. Become familiar with Python functions, including how you declare and call them.
1. Create a function ```sum1()``` that takes two arguments x and y and returns their sum. Demonstrate your working function by running the following commands: 

    ```python
    print(sum1(2,3))
    print(sum1(x=3,y=4))
    ```
    
1. Create a function ```sum2()``` that takes two arguments x and y with default values of 10 and 20, respectively, and returns their sum. Demonstrate your working function by running the following commands: 

    ```python
    print(sum2())
    print(sum2(2))
    print(sum2(y=5))
    ```
    
1. Create a list of 100 elements called ```list1``` using ```range()```.   
1. Create a function ```sum3()``` that takes n arguments and computes their sum.   Demonstrate your working function by running the following commands: 

    ```python
    print(sum3())
    print(sum3(2,3))
    print(sum3(*list1))
    ```
    
1. Create a dictionary using the following code: 

    ```python
    dict1={'item1':4, 'item2':7}
    ```
    
1. Create a function ```sum4()``` that takes n _keyword arguments_, prints each key, and computes the sum of all keyed values.  Demonstrate your working function by running the following commands 

    ```python
    print(sum4())
    print(sum4(x=2,y=3))
    print(sum4(**dict1))
    ```
    
1. Create a function ```sum5()``` which sums an arbitrary number of arguments and the values of any keyword arguments, and prints the key of each keyword arguments.  Demonstrate your working function by running the following commands

    ```python
    print(sum5())
    print(sum5(3,4,x=2,y=3))
    print(sum5(*list1,**dict1))
    ```
    
## Discussion

1. Describe what happens to x when supplying a function with ```*``` within a function call, as in ```function1(*x)```. 
1. Describe what happens to x when supplying a function with ```**``` within a function call, as in ```function1(**x)```. 
1. If a function is declared with variables ```x``` and ```y```, as specified below, using the ```*``` and ```**``` arguments, please describe in what form(data type) those variables are delivered to function, and how to access sub-elements contained within them. 

    ```python
    def arbitrary_function(*x,**y):
        #put code here
        return arbitrary_value
    ```
    
## Submission
    
Please include:

1. Report with the following
    1. Answers to the discussion points above
1. Code

Please follow the "Submission Best Practices" document posted on Canvas.  This assignment may be submitted as a .pdf document or a jupyter notebook (.ipynb).  If submitted as a notebook, make sure it is fully compiled.  This can be done by opening the file in the jupyter browser and in the top jupyter menu selecting "Kernel" --> "Restart and Run All".

<!--unhide-->

## Rubric

| Description |  Points |
|:------------|--------:|
| Report      |      30 |
| Code        |      70 |
| **Total**   | **100** |

