---
layout: lesson
title: Determinant and Cross Product
dept: math
course: calculus-III
unit: unit1
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 1
---

The cross product is one of the two ways of multiplying vectors. It can only be defined between vectors in exactly 3 dimensions. Despite this, there are ways to think about the cross product in 2 dimensions. Additionally, definitions of the cross product can be made in more than 3 dimensions, but that is outside the scope of this course. 

### The Determinant

Let us first define what a determinant is. If you have taken linear algebra already, you will be very familiar with the concept of a determinant: what it means, and how to calculate it. Here is a quick review to refresh your memory. A determinant is a type of function. It takes in vectors as input, and outputs a single scalar. The number of vectors that it takes in depends on the dimension of the vectors. In 2 dimensions, the determinant takes two 2 dimensional vectors. In 3 dimensions, the determinant takes three 3 dimensional vectors, and so on. 

##### Two Dimensions
If we have a vector \\(\textbf{a} = (a_1,a_2)\\) and another vector \\(\textbf{b} = (b_1,b_2)\\), then the *determinant* of them is defined as 

$$\begin{vmatrix} a_1 & a_2 \\ b_1 & b_2 \end{vmatrix} = a_1b_2 - a_2b_1$$

Where normally, we can put these vectors into a *matrix*

$$\begin{bmatrix} a_1 & a_2 \\ b_1 & b_2 \end{bmatrix}$$

and then the *determinant* operation is done on the matrix. Since this is not a course on linear algebra, we expect only the bare basics of linear algebra. Now we can define the cross product of two vectors \\(\textbf{a} = (a_1,a_2,a_3)\\) and \\(\textbf{b} = (b_1,b_2,b_3)\\). It is

$$ \textbf{a}\times\textbf{b} = \begin{vmatrix} \hat{\textbf{x}} & \hat{\textbf{y}} & \hat{\textbf{z}} \\ a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \end{vmatrix}$$

The reason we defined \\(2\times 2\\) determinants above is because this \\(3\times 3\\) determinant is evaluated in terms of them: 

$$\begin{vmatrix} \hat{\textbf{x}} & \hat{\textbf{y}} & \hat{\textbf{z}} \\ a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \end{vmatrix} = \begin{vmatrix} a_2 & a_3 \\ b_2 & b_3 \end{vmatrix} \hat{\textbf{x}} -  \begin{vmatrix} a_1 & a_3 \\ b_1 & b_3 \end{vmatrix} \hat{\textbf{y}} +  \begin{vmatrix} a_1 & a_2 \\ b_1 & b_2 \end{vmatrix} \hat{\textbf{z}} $$

Note that the negative sign in front of the middle term is not a mistake; this is how the \\(3\times 3\\) determinant is defined. There are many tricks for evaluating determinants of special matrices. For example, if a matrix has only elements on its diagonal, then the determinant is the product of those elements. Because this is not a course on linear algebra, we will not be discussing such methods.

### Geometric Intuition

The determinant of two vectors can be interpreted geometrically as the area of the parallelogram formed by the them. 

(insert picture here)



### The Cross Product
The cross product is very closely related to the determinant. 

