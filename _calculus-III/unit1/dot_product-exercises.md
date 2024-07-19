---
layout: exercises
title: Dot Product - Exercises
dept: math
course: calculus-III
unit: unit1
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 1
---

### Exercises

<ol>
<li> <div class="exercise"> Calculate the dot product between the vectors \(\textbf{a} = (3,1)\) and \(\textbf{b} = (-2,1)\). 

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
This is a straightforward computation in two dimensions, which gives 
$$\textbf{a}\cdot\textbf{b} = (3)(-2)+(1)(1) = -6 + 1 = -5$$ 
</div> 
</div>
</div>
</li>

<li> <div class="exercise"> Calculate the dot product between the vectors \(\textbf{x} = (3,1,-5)\) and \(\textbf{y} = (4,-2,1)\)

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a straightforward computation in three dimensions, which gives
$$\textbf{x}\cdot\textbf{y} = (3)(4) + (1)(-2) + (-5)(1) = 12 - 2 - 5 = 6$$
</div> 
</div>
</div>
</li>

<li> <div class="exercise"> Calculate the angle between the two vectors \(\textbf{a} = (1,-1,3)\) and \(\textbf{b} = (2,2,3)\)

<div class="answerBox">
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
</div> 
</div>
</div>
</li>

<li> <div class="exercise"> Find the value(s) of \(a\) such that the two vectors are orthogonal: \(\textbf{p} = (2,1,a)\), \(\textbf{q} = (a,-3,3)\)

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer">
Two vectors are orthogonal if their dot product is zero. Thus we compute the dot product and then solve for \(a\).

$$\textbf{p}\cdot\textbf{q} = (2)(a) + (1)(-3) + (a)(3) = 2a - 3 + 3a = 5a - 3$$

This gives \(a = 3/5\).
</div> 
</div>
</div>
</li>
</ol>
