---
layout: lesson
title: Dot Product
dept: math
course: calculus-III
unit: unit1
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 1
---

The dot product is one of the two ways of multiplying vectors. It can be defined between vectors in 1, 2, 3 or even more dimensions. There are two equivalent definitions of the dot product. One is very geometric, and helps us to get an intuition of what the dot product means. Unfortunately, it is not very useful when performing complex calculations. For this, the abstract definition will come in handy. 

### Geometric Definition
Suppose we have two vectors \\(\textbf{a}\\) and \\(\textbf{b}\\), in any number of dimensions. Then we define the *dot product*

$$\textbf{a}\cdot\textbf{b} = \|\textbf{a}\|\|\textbf{b}\|\cos\theta$$

where \\(\theta\\) is the angle between the two vectors. This can be represented graphically by (insert picture here)

This should be thought of as calcaulting the *projection* of one vector onto the other. But, which vector is being projected onto which? Actually, it doesn't matter which vector is being projected onto which, because both results turn out to be the exact same!

If we project 

### Abstract Definition
The more abstract definition of the dot product uses the *components* of the vector. The dot product between the vectors \\(\textbf{a} = (a_1,a_2,a_3)\\) and \\(\textbf{b} = (b_1,b_2,b_3)\\) is 

$$\textbf{a}\cdot\textbf{b} = a_1b_1 + a_2b_2 + a_3b_3$$

The definition for vectors in dimensions other than 3 has the same form. For example, in 2 dimensions with vectors \\(\textbf{a} = (a_1,a_2)\\) and \\(\textbf{b} = (b_1,b_2)\\), the dot product is 

$$\textbf{a}\cdot\textbf{b} = a_1b_1 + a_2b_2$$

### Properties

Some basic facts about the dot product which you should keep in mind are:

1. The dot product takes place between two (and only two) *vectors*, not between scalars. 
2. The dot product *produces* a *scalar* out of two vectors
3. If the dot product is zero, then that means that the two vectors are *perpendicular*, or, *orthogonal*, to one another.

The dot product has a few nice properties which are familiar from multiplication between scalars. 

Commutativity: 

$$\textbf{a}\cdot\textbf{b} = \textbf{b}\cdot\textbf{a}$$

Distributivity: 

$$\textbf{a}\cdot(\textbf{b} + \textbf{c}) = \textbf{a}\cdot\textbf{b} + \textbf{a}\cdot\textbf{c}$$

### Terminology and Notation
Other terms that are synonymous with *dot product* are

1. Inner product
2. Scalar product

### Equivalence of the Definitions
Now we will show that the two definitions of the dot product are actually identical. This will be done by using the cosine law, and the proof applies in either 2 or 3 (or more!) dimensions. Here, we will do it for 2 dimensions, but it can be extended to more dimensions without much effort.

We start with the geometric definition: 

$$\textbf{a}\cdot\textbf{b} = \|\textbf{a}\|\|\textbf{b}\|\cos\theta$$

By the cosine law, we know that \\(\|\textbf{c}\|^2 = \|\textbf{a}\|^2 + \|\textbf{b}\|^2 - 2\|\textbf{a}\|\|\textbf{b}\|\cos\theta\\). Rearranging this, we get 

$$\|\textbf{a}\|\|\textbf{b}\|\cos\theta = \frac{\|\textbf{a}\|^2 + \|\textbf{b}\|^2 - \|\textbf{c}\|^2}{2}$$

so this means that 

$$\textbf{a}\cdot\textbf{b} = \frac{\|\textbf{a}\|^2 + \|\textbf{b}\|^2 - \|\textbf{c}\|^2}{2}$$

Since we have that \\(\textbf{c} = \textbf{a} - \textbf{b}\\), we can substitute this in

$$\textbf{a}\cdot\textbf{b} = \frac{\|\textbf{a}\|^2 + \|\textbf{b}\|^2 - \|\textbf{a} - \textbf{b}\|^2}{2}$$

expanding this out in terms of components, we get

$$\begin{eqnarray}
\textbf{a}\cdot\textbf{b} &=& \frac{\|\textbf{a}\|^2 + \|\textbf{b}\|^2 - \|\textbf{a} - \textbf{b}\|^2}{2}\\
&=& \frac{a_1^2 + a_2^2 + b_1^2 + b_2^2 - ((a_1-b_1)^2 + (a_2-b_2)^2))}{2}\\
&=& \frac{a_1^2 + a_2^2 + b_1^2 + b_2^2 - (a_1^2 - 2a_1b_1 + b_1^2 + a_2^2 - a_2b_2 + b_2^2)}{2}\\
&=& \frac{2a_1b_1 + 2a_2b_2}{2}\\
&=& a_1b_1 + a_2b_2
\end{eqnarray}$$

which is precisely the second definition.

