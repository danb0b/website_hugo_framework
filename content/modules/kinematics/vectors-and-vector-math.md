---
bibliography: ../../project/bibliography.bib
bibFile: data/bib.json # path relative to project root
csl: ../../project/ieee.csl
title: Vectors and Vector Math
type: submodule
---

# Vectors and Vector Math

A $\vec{v}$ defines a magnitude and direction in $n$-dimensional space.

The concept of a vector comes with a lot of baggage. The first thing you must think about is how many dimensions are you working in? Two or three-dimensional space is normal, but the concept of a vector extends to any dimension.

One way to interpret a vector is the *thing* which describes the difference in position between two points. But what is a point? I would argue that a point is a vector, whose magnitude and direction are referenced from a common origin. So it seems that if we use that definition, a vector is self referencing.

With the idea of Cartesian space comes the idea of axes -- such as x,y,z axes -- which represent orthonormal basis vectors. This allows one to mathematically define a vector with a set of scalar quantities, which represent the magnitude along the direction of each basis vector. Given a set of basis vectors $\hat{a}_x$,$\hat{a}_y$, and $\hat{a}_z$, for example, one can use three scalar quantities $v_x$, $v_y$, and $v_z$ to create an arbitrary vector $\vec{v}$ with the expression $$ \vec{v} = v_x \hat{a}_x + v_y \hat{a}_y + v_z \hat{a}_z. \label{eqn:vector_basisform} $$

The $\vec{}$ symbol is used to indicate a vector, while the the $\hat{}$ is used to indicate a vector with a magnitude of $1$ in $\eqref{eqn:vector_basisform}$.

### Scalar Multiplication

Vectors can be multiplied by scalars in order to change their magnitude while preserving their direction. The expression $a\vec{v}$ represents a vector which is $a$ times the magnitude of $\vec{v}$. Scalars may be positive or negative; negative scalars indicate an opposite orientation of the vector.

### Vector Addition and Subtraction

Vectors may be be added together in expressions, and are commutative and associative. $$
\vec{u} + \vec{v} = \vec{v} + \vec{u} \\
\vec{u} + (\vec{v}+\vec{w}) = (\vec{u}+\vec{v})+\vec{w}
$$

When multiplied by scalars, vector sums are also distributive $$
a(\vec{v}+\vec{w}) = a\vec{v}+a\vec{w}
$$

### Dot Product

The dot product is defined by the expression $$
\vec{v} \cdot \vec{w} \triangleq \left|\vec{v}\right|\left|\vec{w}\right|\cos{\theta},\label{eqn:vector_dot_product}
$$

where $\left|\vec{v}\right|$ indicates the magnitude of vector $\vec{v}$. The dot product has many uses. It can be used to determine the magnitude of a vector, as in $$
\left|v\right| = \sqrt{\vec{v} \cdot \vec{v}}. \label{eq:vector_dot_product_magnitude}$$

The result of a dot product is a scalar number. Since scalar algebra is distributive and commutative, expressions using the dot product are also distributive and commutative. $$\vec{u} \cdot \vec{v} = \vec{v} \cdot \vec{u} \\
\vec{u} \cdot \left(\vec{v}+\vec{w}\right) = \vec{u}\cdot\vec{v} + \vec{u}\cdot\vec{w} \label{eqn:vector_dot_distributive}$$

### Cross Product

The cross product is defined by the expression $$
\vec{v} \times \vec{w} \triangleq \left|\vec{v}\right|\left|\vec{w}\right|\sin{\theta}\hat{u}, \label{eqn:vector_cross_product}$$

where $\hat{u}$ is the unit vector orthogonal to $\vec{v}$ and $\vec{w}$, according to the right hand rule. Due to this definition, the cross product of $\vec{w}\times\vec{v}$ will produce a vector equal in magnitude and opposite direction to $\vec{v}\times\vec{w}$. Thus, the cross product can be said to be anticommutative. $$
\vec{u} \times \vec{v} = -\vec{v} \times \vec{u}$$ The cross product operator can also be distributed. $$
\vec{u} \times \left(\vec{v}+\vec{w}\right) = \vec{u}\times\vec{v} + \vec{u}\times\vec{w}$$

### Exercises {#exercises .unnumbered}

1.  Using , write an expression for a vector $a$ whose magnitude along $\hat{a}_x$ is 4, whose magnitude along $\hat{a}_y$ is 7, and whose magnitude along $\hat{a}_z$ is -3.
2.  Using , write an expression for a vector $b$ whose magnitude along $\hat{a}_x$ is 1, whose magnitude along $\hat{a}_y$ is 5, and whose magnitude along $\hat{a}_z$ is -2.
3.  Using , expand the expression $\vec{a}\cdot\vec{b}$, using the results of
4.  Look up the term orthogonal on google. What is the angle between two orthogonal vectors? What is the magnitude of an unit vector?
5.  Assuming $\hat{a}_x$,$\hat{a}_x$, and $\hat{a}_x$ are orthogonal unit vectors, and using , supply the following:
    a)  $\hat{a}_x\cdot\hat{a}_x = ?$
    b)  $\hat{a}_x\cdot\hat{a}_y = ?$
    c)  $\hat{a}_x\cdot\hat{a}_z = ?$
    d)  $\hat{a}_y\cdot\hat{a}_x = ?$
    e)  $\hat{a}_y\cdot\hat{a}_y = ?$
    f)  $\hat{a}_y\cdot\hat{a}_z = ?$
    g)  $\hat{a}_z\cdot\hat{a}_x = ?$
    h)  $\hat{a}_z\cdot\hat{a}_y = ?$
    i)  $\hat{a}_z\cdot\hat{a}_z = ?$

### Expanded basis vector forms

If two vectors $\vec{u}$ and $\vec{v}$ can be expanded into component basis vectors $\hat{a}_x$,$\hat{a}_y$,and $\hat{a}_z$ such that $$
\vec{u}=u_x\hat{a}_x + u_y\hat{a}_y+u_z\hat{a}_z \text{ and}\\
\vec{v}=v_x\hat{a}_x + v_y\hat{a}_y+v_z\hat{a}_z,$$ can then be rewritten as $$
\vec{v} \cdot \vec{w} = (u_x\hat{a}_x + u_y\hat{a}_y+u_z\hat{a}_z) \cdot (v_x\hat{a}_x + v_y\hat{a}_y+v_z\hat{a}_z)$$

which, using the distributive property equals $$
\vec{v} \cdot \vec{w} = u_x\hat{a}_x \cdot v_x\hat{a}_x + u_x\hat{a}_x \cdot v_y\hat{a}_y + u_x\hat{a}_x \cdot v_z\hat{a}_z  + \\
u_y\hat{a}_y \cdot v_x\hat{a}_x +u_y\hat{a}_y \cdot v_y\hat{a}_y + u_y\hat{a}_y \cdot v_z\hat{a}_z + \nonumber\\
u_z\hat{a}_z \cdot v_x\hat{a}_x +u_z\hat{a}_z \cdot v_y\hat{a}_y +u_z\hat{a}_z \cdot v_z\hat{a}_z \nonumber$$

grouping scalars, $$
\vec{v} \cdot \vec{w} = u_x v_x (\hat{a}_x \cdot \hat{a}_x) + u_x v_y (\hat{a}_x \cdot \hat{a}_y) + u_x v_z(\hat{a}_x \cdot \hat{a}_z)  + \label{eqn:dot_product_basis_simplification1} \\
u_y v_x(\hat{a}_y \cdot \hat{a}_x) +u_y v_y(\hat{a}_y \cdot \hat{a}_y) + u_y v_z(\hat{a}_y \cdot \hat{a}_z) + \nonumber\\
u_z v_x(\hat{a}_z \cdot \hat{a}_x) +u_z v_y(\hat{a}_z \cdot\hat{a}_y) +u_z v_z(\hat{a}_z \cdot \hat{a}_z) \nonumber$$

using the definition of the dot product, we can see that the dot product of orthogonal basis unit vectors is equal to 0 while the dot product of a basis vector with itself is equal to 1. This can be summarized by $$
\hat{a}_x\cdot\hat{a}_x = 1\\
\hat{a}_x\cdot\hat{a}_y = 0\\
\hat{a}_x\cdot\hat{a}_z = 0\\
\hat{a}_y\cdot\hat{a}_x = 0\\
\hat{a}_y\cdot\hat{a}_y = 1\\
\hat{a}_y\cdot\hat{a}_z = 0\\
\hat{a}_z\cdot\hat{a}_x = 0\\
\hat{a}_z\cdot\hat{a}_y = 0\\
\hat{a}_z\cdot\hat{a}_z = 1$$ This simplifies to $$
\vec{v} \cdot \vec{w} = u_x v_x +u_y v_y+u_z v_z$$

The expression for the cross product can similarly be simplified. Given the same $\vec{u}$ and $\vec{v}$, can be rewritten as $$\vec{v} \times \vec{w} = (u_x\hat{a}_x + u_y\hat{a}_y+u_z\hat{a}_z) \times (v_x\hat{a}_x + v_y\hat{a}_y+v_z\hat{a}_z)$$ which, using the distributive property equals $$\vec{v} \times \vec{w} = u_x\hat{a}_x \times v_x\hat{a}_x + u_x\hat{a}_x \times v_y\hat{a}_y + u_x\hat{a}_x \times v_z\hat{a}_z  + \\
u_y\hat{a}_y \times v_x\hat{a}_x +u_y\hat{a}_y \times v_y\hat{a}_y + u_y\hat{a}_y \times v_z\hat{a}_z + \nonumber\\
u_z\hat{a}_z \times v_x\hat{a}_x +u_z\hat{a}_z \times v_y\hat{a}_y +u_z\hat{a}_z \times v_z\hat{a}_z \nonumber$$

grouping scalars, $$\vec{v} \times \vec{w} = u_x v_x (\hat{a}_x \times \hat{a}_x) + u_x v_y (\hat{a}_x \times \hat{a}_y) + u_x v_z(\hat{a}_x \times \hat{a}_z)  + \label{eqn:cross_product_basis_simplification1}\\
u_y v_x(\hat{a}_y \times \hat{a}_x) +u_y v_y(\hat{a}_y \times \hat{a}_y) + u_y v_z(\hat{a}_y \times \hat{a}_z) + \nonumber\\
u_z v_x(\hat{a}_z \times \hat{a}_x) +u_z v_y(\hat{a}_z \times\hat{a}_y) +u_z v_z(\hat{a}_z \times \hat{a}_z) \nonumber$$

using the definition of the cross product, we can see that the cross product of orthogonal basis unit vectors produces an orthogonal unit vector to both according to the right hand rule, while the cross product of a basis vector with itself is equal to the zero vector. This can be summarized by $$\hat{a}_x\times\hat{a}_x = \vec{0}\\
\hat{a}_x\times\hat{a}_y = \hat{a}_z\\
\hat{a}_x\times\hat{a}_z = -\hat{a}_y\\
\hat{a}_y\times\hat{a}_x = -\hat{a}_z\\
\hat{a}_y\times\hat{a}_y = \vec{0}\\
\hat{a}_y\times\hat{a}_z = \hat{a}_x\\
\hat{a}_z\times\hat{a}_x = \hat{a}_y\\
\hat{a}_z\times\hat{a}_y = -\hat{a}_x\\
\hat{a}_z\times\hat{a}_z = \vec{0}$$ This simplifies to $$\vec{v} \times \vec{w} = u_x v_y\hat{a}_z - u_x v_z\hat{a}_y - u_y v_x\hat{a}_z + u_y v_z\hat{a}_x + u_z v_x\hat{a}_y - u_z v_y\hat{a}_x$$

<!--
## rotations and translations

who knows all about rotations what is a rotation in 2d what is a rotation in 3d how do you make a rotation about a point other than 0,0? definition of affine. what happens when i moulting everything by two? gets two times further from origin as well. what if I want to stretch scale and skew and trapezoid connection between 2d affine transformations and 3d perspective shift... length is preserved not angles\
take a look at your phone straight on

what is translation, what does it look like

matrix form

two steps or one to rotate translate?

define transformation matrix

simple polygon with plot class sympy to generate rotation matrix.\
do translate, rotate, translate, symbolically and find the theta and displacement elements in combined matrix\
pick center of polygon and scale

$$
\vec{v} = x\hat{a}_x +y\hat{a}_y + z\hat{a}_z
$$

$$
\left[
\begin{array}{ccc}
    cos(q) & sin(q) & 0 \\
    sin(q) & cos(q) & 0 \\
    0 & 0 & 1 \\
\end{array}
\right]
$$
-->