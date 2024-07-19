---
layout: lesson
title: DOT PRODUCT
course: calculus-III
unit: unit1
lessonID: dot-product
nextID: determinant-cross-product
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

### Exercises

<ol>
<li> <div> Calculate the dot product between the vectors \(\textbf{a} = (3,1)\) and \(\textbf{b} = (-2,1)\). </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
This is a straightforward computation in two dimensions, which gives 
$$\textbf{a}\cdot\textbf{b} = (3)(-2)+(1)(1) = -6 + 1 = -5$$ 
</div> </li>

<li> <div> Calculate the dot product between the vectors \(\textbf{x} = (3,1,-5)\) and \(\textbf{y} = (4,-2,1)\) </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a straightforward computation in three dimensions, which gives
$$\textbf{x}\cdot\textbf{y} = (3)(4) + (1)(-2) + (-5)(1) = 12 - 2 - 5 = 6$$
</div> </li>

<li> <div> Calculate the angle between the two vectors \(\textbf{a} = (1,-1,3)\) and \(\textbf{b} = (2,2,3)\)</div>

<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
For this, we can use the two different definitions of the dot product to obtain the formula
$$\cos\theta = \frac{\textbf{a}\cdot\textbf{b}}{|\textbf{a}||\textbf{b}|}$$

Then we calculate the dot product in terms of the components and the magnitudes of the vectors
$$\textbf{a}\cdot\textbf{b} = (1)(2) + (-1)(2) + (3)(3) = 2 - 2 + 9 = 9$$ 
$$|\textbf{a}| = \sqrt{1^2 + (-1)^2 + 3^2} = \sqrt{1+1+9} = \sqrt{11}$$
$$|\textbf{b}| = \sqrt{2^2+2^2 + 3^2} = \sqrt{4+4+9} = \sqrt{17}$$

Now plugging these in, we get

$$\cos\theta = \frac{9}{\sqrt{11}\sqrt{17}} =  0.65814$$

and then plugging this into a calculator, we get

$$\theta = 0.85244\,\text{rad} =   48.841^\circ$$
</div> </li>

<li> <div> Find the value(s) of \(a\) such that the two vectors are orthogonal: \(\textbf{p} = (2,1,a)\), \(\textbf{q} = (a,-3,3)\) </div>

<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer">
Two vectors are orthogonal if their dot product is zero. Thus we compute the dot product and then solve for \(a\).

$$\textbf{p}\cdot\textbf{q} = (2)(a) + (1)(-3) + (a)(3) = 2a - 3 + 3a = 5a - 3$$

This gives \(a = 3/5\).
</div> </li>
</ol>
