---
layout: lesson
title: Chain Rule
dept: math
course: calculus-III
unit: unit3
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 3
---

The chain rule is often one of the more difficult sections for students to grasp in multivariable calculus. This is usually because of sloppy notation, both on the part of the instructor and student. Here we will try to be as explicit and clear as possible so that the student can learn good habits.

Let's first recall the chain rule from single variable calculus. If \\(y = f(g(x))\\), then 

$$ y' = f'(g(x))g'(x)$$

The chain rule for functions of several variables is a direct extension of this. Additionally, there is a single formula just like the one above. 

#### Chain Rule 1

Consider a function of the form \\(f(t) = g(x(t),y(t))\\). What is \\(f'(t)\\)? It is 

$$\frac{df}{dt} = \frac{\partial g}{\partial x}\frac{dx}{dt} + \frac{\partial g}{\partial y}\frac{dy}{dt}$$

which can be rewritten as 

$$\frac{df}{dt} = \nabla f \cdot \frac{d\textbf{r}}{dt}$$

where \\(\textbf{r}(t) = (x(t),y(t))\\). What does this mean physically? This represents how \\(f\\) changes as we move along the curve \\((x(t),y(t))\\) in the \\(xy\\) plane!

(insert a figure)

#### Chain Rule 2

What about functions of the form \\(f(x,y) = h(g(x,y))\\)? Now \\(f\\) is a function of two variables, so we can look at computing its partials. 

$$\frac{\partial f}{\partial x} = \frac{dh}{dg}\frac{\partial g}{\partial x}, \quad \frac{\partial f}{\partial y} = \frac{dh}{dg}\frac{\partial g}{\partial y}$$

This can be rewritten as 

$$ \nabla f = \frac{dh}{dg}\nabla g$$

#### Chain Rule 3

Now we combine the two concepts to look at functions of the form \\(f(x,y) = g(u(x,y),v(x,y))\\). This looks like 

$$\frac{\partial f}{\partial x} = \frac{\partial g}{\partial u}\frac{\partial u}{\partial x} + \frac{\partial g}{\partial v} \frac{\partial v}{\partial x}$$

$$\frac{\partial f}{\partial y} = \frac{\partial g}{\partial u}\frac{\partial u}{\partial y} + \frac{\partial g}{\partial v} \frac{\partial v}{\partial y}$$


#### Second Derivatives

The tricky part of all this is when it comes to second derivatives. We really need to be clear about what is a function of what!


### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
